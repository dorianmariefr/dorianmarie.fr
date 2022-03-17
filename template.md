---
title: How to make a templating language
layout: default
indexed: true
---

A simple template could be:

```
Hello {{user.first_name}}
```

And would be rendered like this:

```ruby
template = "Hello {{user.first_name}}"
Template.new(template).render(
  locals: { user: { first_name: "Dorian" } }
)
# => "Hello Dorian"
```

A template could be more complex like:

```
{define render(item)}
  <p>{{link_to(item.user.name, item.user.url)}}</p>
  
  {{item.content | markdown}}
  
  <p>{{link_to(item.created_at.to_formatted_s(:long), item.url)}}</p>
  
  {if item.parent}
    {{render(item.parent)}}
  {end}
{end}

{{render(item)}}
```

We will need a parser and an interpreter. I prefer to write both in ruby.

## Parser

I will use [parslet](https://github.com/kschiess/parslet) for the parser.

### Text

Let's start with something simple:

```ruby
require 'parslet'

class Template
  class Parser < Parslet::Parser
    rule(:empty) { str('') }
    rule(:template) do
      any.repeat(1).as(:text).repeat(1) |
        empty.as(:text).repeat(1, 1)
    end
    root(:template)
  end
end
```

And two simple tests:

```ruby
require_relative "../../template/parser"

RSpec.describe Template::Parser do
  let!(:template) { "" }
  subject { described_class.new.parse(template) }

  it { is_expected.to eq([{ text: "" }]) }

  context "with only text" do
    let!(:template) { "Hello" }
    it { is_expected.to eq([{ text: "Hello" }]) }
  end
end
```

`any` is the same as `match('.')`, e.g. it matches any character

then `repeat(1)` tells the parser the character can be repeated 1 or more times.

`as(:text)` captures the text under the `text` key, e.g. `{ text: "Hello" }`

I add another `repeat(1)` because I will want to have an array of matches at the end, e.g. `[text, interpolation, expression, text, expression, etc.]`

`empty.as(:text).repeat(1, 1)` is just so that it gives the same format for the output when an empty string is passed.

### Empty Interpolations

I would like to be able to do `Hello {{}}` (which would render `Hello `) and `Hello \{\{World\}\}` which would render `Hello {{World}}`) (e.g. escaping the interpolation)

As tests, I write:

```ruby
  context "with an interpolation" do
    let!(:template) { "Hello {{user.first_name}}" }
    it {
      is_expected.to eq([
        { text: "Hello " },
        { interpolation: "user.first_name" }
      ])
    }
  end

  context "with an escaped interpolation" do
    let!(:template) { "Hello \\{\\{user.first_name\\}\\}" }
    it {
      is_expected.to eq([
        { text: "Hello {{user.first_name}}" },
      ])
    }
  end
```

The parser is getting a bit more complex:

```ruby
require 'parslet'

class Template
  class Parser < Parslet::Parser
    rule(:empty) { str('') }
    rule(:backslash) { str('\\') }
    rule(:opening_bracket) { str('{') }
    rule(:closing_bracket) { str('}') }

    # text
    rule(:unescaped_text_character) do
      opening_bracket.absent? >> closing_bracket.absent? >> any
    end
    rule(:escaped_text_character) { backslash.ignore >> any }
    rule(:text_character) { escaped_text_character | unescaped_text_character }
    rule(:text) { text_character.repeat(1) }

    # interpolation
    rule(:opening_interpolation) { opening_bracket >> opening_bracket }
    rule(:closing_interpolation) { closing_bracket >> closing_bracket }
    rule(:interpolation) do
      opening_interpolation.ignore >> expression >> closing_interpolation.ignore
    end

    # expression
    rule(:expression_character) do
      opening_interpolation.absent? >> closing_interpolation.absent? >> any
    end
    rule(:expression) { expression_character.repeat(0) }

    rule(:template) do
      (
        interpolation.as(:interpolation) |
        text.as(:text)
      ).repeat(1) |
        empty.as(:text).repeat(1, 1)
    end

    root(:template)
  end
end
```

For now the expression in the interpolation can be any character except `{{` or `}}` but we are going to change that later.

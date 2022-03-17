---
title: How to make a templating language
layout: default
indexed: true
---

A simple template could be:

```liquid
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

```liquid
{define render(item)}
  <p>{{link_to(item.user.name, item.user.url)}}</p>
  
  {{item.content | markdown}}
  
  <p>{{link_to(item.created_at.to_formatted_s(:long), item.url)}}</p>
  
  {if item.parent}
    {render(item.parent)}
  {end}
{end}

{render(item)}
```

We will need a parser and an interpreter. I prefer to write both in ruby.

## Parser

I will use [parslet](https://github.com/kschiess/parslet) for the parser.

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

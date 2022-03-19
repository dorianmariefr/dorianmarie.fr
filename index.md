---
title: Thoughts
title: Dorian Marié
layout: default
indexed: false
---

Hi 👋<br>
I'm french 🇫🇷<br>
I'm a programmer 🧑‍💻<br>
<a href="/resume/Dorian Marie - CV.pdf">My resume</a> 📁

I like working with: ❤️<br>
<b>Ruby</b> with Ruby on Rails 💎<br>
<b>Javascript</b> with React ⚛️  and/or Stimulus ⚡️<br>
<b>SQL</b> with PostgreSQL 🐘<br>

My email is <a href="mailto:dorian@dorianmarie.fr">dorian@dorianmarie.fr</a> ✉️<br>
My GitHub is <a href="https://github.com/dorianmariefr">@dorianmariefr</a> 🐙<br>
My Twitter is <a href="https://twitter.com/dorianmariefr">@dorianmariefr</a> 🐦<br>

<ul>
  {% for page in site.pages %}
    {% if page.indexed %}
      <li><a href="{{ page.url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

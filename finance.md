---
layout: home
title: Financial Analysis
permalink: /finance/
---

Here are my thoughts on the market, macroeconomics, and investment strategies.

<ul>
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h3>
    </li>
  {% endfor %}
</ul>

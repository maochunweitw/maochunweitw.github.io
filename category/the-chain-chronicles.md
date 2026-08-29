---
layout: default
title: "08 鏈上冒險者札記 / The Chain Chronicles"
category_name: "08 鏈上冒險者札記 / The Chain Chronicles"
permalink: /category/the-chain-chronicles/
---

<section class="latest">
  <div class="section-heading">
    <h2>08 鏈上冒險者札記 / The Chain Chronicles</h2>
    <span>THE CHAIN CHRONICLES</span>
  </div>

  {% for post in site.posts %}
    {% if post.category == page.category_name or post.categories contains page.category_name %}
      <article class="post-card">
        <div class="post-meta">{{ post.date | date: "%Y.%m.%d" }}</div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt | strip_html | strip_newlines | truncate: 120 }}</p>
        <a class="read-more" href="{{ post.url | relative_url }}">閱讀全文 →</a>
      </article>
    {% endif %}
  {% endfor %}
</section>

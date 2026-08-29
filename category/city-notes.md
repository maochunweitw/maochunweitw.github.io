---
layout: default
title: "04 城市觀察 / City Notes"
category_name: "04 城市觀察 / City Notes"
permalink: /category/city-notes/
---

<section class="latest">
  <div class="section-heading">
    <h2>04 城市觀察 / City Notes</h2>
    <span>CITY NOTES</span>
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

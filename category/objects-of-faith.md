---
layout: default
title: "07 信仰之物 / Objects of Faith"
category_name: "07 信仰之物 / Objects of Faith"
permalink: /category/objects-of-faith/
---

<section class="latest">
  <div class="section-heading">
    <h2>07 信仰之物 / Objects of Faith</h2>
    <span>OBJECTS OF FAITH</span>
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

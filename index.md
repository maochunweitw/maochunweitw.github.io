---
layout: default
title: 淳文字。
---

<section class="hero">
  <p class="eyebrow">CHUN WEN ZI · PERSONAL JOURNAL</p>

  <h1>淳文字。</h1>

  <p class="hero-en">Journal of Words, Memories & Human Stories</p>

  <p class="hero-intro">
    寫下那些值得留下的文字。<br>
    關於人、生活、記憶，以及我們如何成為現在的自己。
  </p>
</section>

<section class="latest">
  <div class="section-label">
    <span>01</span>
    <h2>最新文字</h2>
  </div>

  {% for post in site.posts limit:3 %}
  <article class="post-card">
    <p class="post-date">{{ post.date | date: "%Y.%m.%d" }}</p>

    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>

    {% if post.excerpt %}
    <p class="post-excerpt">
      {{ post.excerpt | strip_html | truncate: 140 }}
    </p>
    {% endif %}

    <a class="read-more" href="{{ post.url | relative_url }}">
      閱讀全文 →
    </a>
  </article>
  {% endfor %}
</section>

<section class="index-section">
  <div class="section-label">
    <span>02</span>
    <h2>文字索引</h2>
  </div>

  <div class="index-grid">

    <a href="{{ '/posts/' | relative_url }}" class="index-item">
      <span class="index-number">01</span>
      <span>
        <strong>人與人的關係</strong>
        <small>Relationships</small>
      </span>
    </a>

    <a href="{{ '/posts/' | relative_url }}" class="index-item">
      <span class="index-number">02</span>
      <span>
        <strong>生命經驗</strong>
        <small>Life Stories</small>
      </span>
    </a>

    <a href="{{ '/posts/' | relative_url }}" class="index-item">
      <span class="index-number">03</span>
      <span>
        <strong>閱讀與創作</strong>
        <small>Reading & Creation</small>
      </span>
    </a>

    <a href="{{ '/posts/' | relative_url }}" class="index-item">
      <span class="index-number">04</span>
      <span>
        <strong>城市觀察</strong>
        <small>City Notes</small>
      </span>
    </a>

    <a href="{{ '/posts/' | relative_url }}" class="index-item">
      <span class="index-number">05</span>
      <span>
        <strong>記憶收藏</strong>
        <small>Memory Archive</small>
      </span>
    </a>

    <a href="{{ '/posts/' | relative_url }}" class="index-item">
      <span class="index-number">06</span>
      <span>
        <strong>情感片段</strong>
        <small>Emotional Fragments</small>
      </span>
    </a>

    <a href="{{ '/posts/' | relative_url }}" class="index-item">
      <span class="index-number">07</span>
      <span>
        <strong>信仰之物</strong>
        <small>Objects of Faith</small>
      </span>
    </a>

    <a href="{{ '/posts/' | relative_url }}" class="index-item">
      <span class="index-number">08</span>
      <span>
        <strong>其他筆記</strong>
        <small>Other Notes</small>
      </span>
    </a>

  </div>
</section>

<section class="manifesto">
  <p class="eyebrow">A NOTE TO MYSELF</p>

  <blockquote>
    「有些文字不是為了被看見，<br>
    而是為了讓某一個瞬間不至於消失。」
  </blockquote>

  <a href="{{ '/關於.html' | relative_url }}" class="text-link">
    關於淳文字 →
  </a>
</section>

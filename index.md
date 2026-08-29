---
layout: default
---

<section class="hero">

  <div class="eyebrow">PERSONAL JOURNAL</div>

  <h1>淳文字</h1>

  <p class="intro">
    走過半生，慢慢明白——人生很多時候，不在於贏，而在於看清。
  </p>

</section>

<section class="latest">

  <div class="section-heading">
    <h2>最新文字</h2>
    <span>WRITINGS</span>
  </div>

  {% for post in site.posts %}

  <article class="post-card">

    <div class="post-meta">
      {{ post.date | date: "%Y.%m.%d" }}
      {% if post.categories %}
      · {{ post.categories | first }}
      {% endif %}
    </div>

    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>

    <p>
      {{ post.excerpt | strip_html | strip_newlines | truncate: 120 }}
    </p>

    <a class="read-more" href="{{ post.url | relative_url }}">
      閱讀全文 →
    </a>

  </article>

  {% else %}

  <p class="empty">目前尚無文章。</p>

  {% endfor %}

</section>

<section class="about-block">

  <h2>關於這裡</h2>

  <p>
    記錄生活裡的起落，記錄修行中的體悟，也記錄那些在人群與歲月之間，逐漸明白的道理。
  </p>

  <a href="{{ '/about.html' | relative_url }}">
    閱讀關於淳文字 →
  </a>

</section>

<section class="manifesto">

  <p>
    人生不求處處勝出，<br>
    只願在關鍵時刻，<br>
    能守住本心，也能全身而退。
  </p>

</section>

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


<section class="categories-home">

  <div class="section-heading">
    <h2>文章分類</h2>
    <span>CATEGORIES</span>
  </div>

  <div class="category-list">

    <a class="category-card" href="{{ '/category/relationships/' | relative_url }}">
      <strong>01 人與人的關係 / Relationships</strong>
      <span>那些在轉身與留步之間，無聲堆疊的牽絆。</span>
    </a>

    <a class="category-card" href="{{ '/category/life-stories/' | relative_url }}">
      <strong>02 生命經驗 / Life Stories</strong>
      <span>痛楚、跨越，與所有讓我們成為現在自己的瞬間。</span>
    </a>

    <a class="category-card" href="{{ '/category/reading-creation/' | relative_url }}">
      <strong>03 閱讀與創作 / Reading &amp; Creation</strong>
      <span>在別人的文字裡流浪，在自己的筆尖下定居。</span>
    </a>

    <a class="category-card" href="{{ '/category/city-notes/' | relative_url }}">
      <strong>04 城市觀察 / City Notes</strong>
      <span>漫步在水泥與街角陰影中，那些被忽略的日常切片。</span>
    </a>

    <a class="category-card" href="{{ '/category/memory-archive/' | relative_url }}">
      <strong>05 記憶收藏 / Memory Archive</strong>
      <span>泛黃的物件、過期的車票，與時間對抗的私人博物館。</span>
    </a>

    <a class="category-card" href="{{ '/category/emotional-fragments/' | relative_url }}">
      <strong>06 情感片段 / Emotional Fragments</strong>
      <span>轉瞬即逝的碎念、悸動，以及無法歸類的夜半情緒。</span>
    </a>

    <a class="category-card" href="{{ '/category/objects-of-faith/' | relative_url }}">
      <strong>07 信仰之物 / Objects of Faith</strong>
      <span>支撐著靈魂繼續前行，無論是神祇、信念，還是一首歌。</span>
    </a>

    <a class="category-card" href="{{ '/category/the-chain-chronicles/' | relative_url }}">
      <strong>08 鏈上冒險者札記 / The Chain Chronicles</strong>
      <span>密碼學構築的當代淘金夢，那些關於風險的抉擇、信念的崩塌與重建。</span>
    </a>

  </div>

</section>


<section class="latest">

  <div class="section-heading">
    <h2>最新文字</h2>
    <span>WRITINGS</span>
  </div>

  {% for post in site.posts limit:5 %}

  <article class="post-card">

    <div class="post-meta">
      {{ post.date | date: "%Y.%m.%d" }}
      {% if post.category %}
      · {{ post.category }}
      {% elsif post.categories %}
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


<section class="manifesto">

  <p>
    人生不求處處勝出，<br>
    只願在關鍵時刻，<br>
    能守住本心，也能全身而退。
  </p>

</section>

---
layout: default
---

<style>
  /* 徹底隱藏 Minimal 主題預設產生的左上角/頂部 header 標題 */
  header,
  .wrapper > header,
  body > div.wrapper > header {
    display: none !important;
  }
  
  /* 修正版面寬度與邊距，讓內容居中 */
  .wrapper {
    max-width: 800px !important;
    margin: 0 auto !important;
    padding: 40px 20px !important;
  }
  
  section {
    width: 100% !important;
    float: none !important;
  }

  /* 分類索引按鈕樣式 */
  .index-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
    margin: 20px 0;
  }
  .index-card {
    display: block;
    padding: 16px;
    border: 1px solid #eee;
    border-radius: 6px;
    text-decoration: none;
    color: inherit;
    transition: all 0.2s ease;
  }
  .index-card:hover {
    border-color: #999;
    background-color: #fafafa;
  }
  .index-num {
    font-size: 0.8rem;
    color: #999;
    display: block;
    margin-bottom: 4px;
  }
</style>

<div style="letter-spacing: 2px; font-size: 0.85rem; color: #888; margin-bottom: 8px;">CHUN WEN ZI · PERSONAL JOURNAL</div>

# 淳文字。

*Journal of Words, Memories & Human Stories*

> 寫下那些值得留下的文字。  
> 關於人、生活、記憶，以及我們如何成為現在的自己。

---

## 01 最新文字

{% for post in site.posts limit:3 %}
<div style="margin-bottom: 24px;">
  <span style="font-size: 0.85rem; color: #999;">{{ post.date | date: "%Y.%m.%d" }}</span>
  <h3 style="margin: 4px 0;">
    <a href="{{ post.url | relative_url }}" style="color: #222; text-decoration: none;">{{ post.title }}</a>
  </h3>
  {% if post.excerpt %}
  <p style="margin: 8px 0; color: #666; font-size: 0.95rem;">
    {{ post.excerpt | strip_html | truncate: 140 }}
  </p>
  {% endif %}
  <a href="{{ post.url | relative_url }}" style="font-size: 0.85rem; color: #888;">閱讀全文 →</a>
</div>
{% endfor %}

---

## 02 文字索引

<div class="index-grid">
  <a href="{{ '/posts/' | relative_url }}" class="index-card">
    <span class="index-num">01</span>
    <strong>人與人的關係</strong>
    <span style="display:block; font-size: 0.8rem; color: #888;">Relationships</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" class="index-card">
    <span class="index-num">02</span>
    <strong>生命經驗</strong>
    <span style="display:block; font-size: 0.8rem; color: #888;">Life Stories</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" class="index-card">
    <span class="index-num">03</span>
    <strong>閱讀與創作</strong>
    <span style="display:block; font-size: 0.8rem; color: #888;">Reading & Creation</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" class="index-card">
    <span class="index-num">04</span>
    <strong>城市觀察</strong>
    <span style="display:block; font-size: 0.8rem; color: #888;">City Notes</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" class="index-card">
    <span class="index-num">05</span>
    <strong>記憶收藏</strong>
    <span style="display:block; font-size: 0.8rem; color: #888;">Memory Archive</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" class="index-card">
    <span class="index-num">06</span>
    <strong>情感片段</strong>
    <span style="display:block; font-size: 0.8rem; color: #888;">Emotional Fragments</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" class="index-card">
    <span class="index-num">07</span>
    <strong>信仰之物</strong>
    <span style="display:block; font-size: 0.8rem; color: #888;">Objects of Faith</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" class="index-card">
    <span class="index-num">08</span>
    <strong>其他筆記</strong>
    <span style="display:block; font-size: 0.8rem; color: #888;">Other Notes</span>
  </a>
</div>

---

<div style="margin-top: 40px; color: #777; font-size: 0.9rem;">
  <em>A NOTE TO MYSELF</em><br>
  「有些文字不是為了被看見，而是為了讓某一個瞬間不至於消失。」
  <br><br>
  <a href="{{ '/about' | relative_url }}" style="color: #444;">關於淳文字 →</a>
</div>

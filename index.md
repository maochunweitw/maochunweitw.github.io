---
layout: default
---

<style>
  /* 強制隱藏 Minimal 主題預設產生的 header 區塊 */
  header,
  .wrapper > header {
    display: none !important;
  }
  
  /* 讓 main 內容佔滿整頁，維持原本主題質感 */
  section {
    width: 100% !important;
    float: none !important;
  }
</style>

<div style="letter-spacing: 2px; font-size: 0.8rem; color: #888; margin-bottom: 6px;">CHUN WEN ZI · PERSONAL JOURNAL</div>

# 淳文字。

*Journal of Words, Memories & Human Stories*

> 寫下那些值得留下的文字。  
> 關於人、生活、記憶，以及我們如何成為現在的自己。

---

## 01 最新文字

{% for post in site.posts limit:3 %}
<div style="margin-bottom: 24px;">
  <span style="font-size: 0.85rem; color: #999;">{{ post.date | date: "%Y.%m.%d" }}</span>
  <h3 style="margin: 4px 0 8px 0;">
    <a href="{{ post.url | relative_url }}" style="color: #222; text-decoration: none;">{{ post.title }}</a>
  </h3>
  {% if post.excerpt %}
  <p style="margin: 8px 0 12px 0; color: #555; font-size: 0.95rem; line-height: 1.6;">
    {{ post.excerpt | strip_html | truncate: 140 }}
  </p>
  {% endif %}
  <a href="{{ post.url | relative_url }}" style="font-size: 0.85rem; color: #777;">閱讀全文 →</a>
</div>
{% endfor %}

---

## 02 文字索引

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 12px; margin: 20px 0 30px 0;">
  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">01</span>
    <strong style="font-size: 0.95rem;">人與人的關係</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Relationships</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">02</span>
    <strong style="font-size: 0.95rem;">生命經驗</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Life Stories</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">03</span>
    <strong style="font-size: 0.95rem;">閱讀與創作</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Reading & Creation</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">04</span>
    <strong style="font-size: 0.95rem;">城市觀察</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">City Notes</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">05</span>
    <strong style="font-size: 0.95rem;">記憶收藏</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Memory Archive</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">06</span>
    <strong style="font-size: 0.95rem;">情感片段</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Emotional Fragments</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">07</span>
    <strong style="font-size: 0.95rem;">信仰之物</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Objects of Faith</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">08</span>
    <strong style="font-size: 0.95rem;">其他筆記</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Other Notes</span>
  </a>
</div>

---

<div style="margin-top: 30px; color: #888; font-size: 0.85rem;">
  <em>A NOTE TO MYSELF</em><br>
  「有些文字不是為了被看見，而是為了讓某一個瞬間不至於消失。」
  <br><br>
  <a href="{{ '/about' | relative_url }}" style="color: #444;">關於淳文字 →</a>
</div>

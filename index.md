---
layout: default
---

<style>
  /* 隱藏 Minimal 主題預設的 header */
  header,
  .wrapper > header {
    display: none !important;
  }
  
  /* 讓 main 內容佔滿整頁 */
  section {
    width: 100% !important;
    float: none !important;
  }

  /* 確保全頁與 02 以下區域套用優雅的明體字型與顏色 */
  body, section, p, em, blockquote {
    font-family: "Noto Serif TC", "Songti TC", "PMingLiU", serif !important;
    color: #333333;
  }
</style>

CHUN WEN ZI · PERSONAL JOURNAL

# 淳文字。

*Journal of Words, Memories & Human Stories*

> 寫下那些值得留下的文字。  
> 關於人、生活、記憶，以及我們如何成為現在的自己。

---

## 01 最新文字

{% for post in site.posts limit:3 %}
{{ post.date | date: "%Y.%m.%d" }}

### [{{ post.title }}]({{ post.url | relative_url }})

{% if post.excerpt %}
{{ post.excerpt | strip_html | truncate: 140 }}
{% endif %}

[閱讀全文 →]({{ post.url | relative_url }})
{% endfor %}

---

## 02 文字索引

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 12px; margin: 20px 0 30px 0;">
  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">01</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif;">人與人的關係</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Relationships</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">02</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif;">生命經驗</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Life Stories</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">03</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif;">閱讀與創作</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Reading & Creation</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">04</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif;">城市觀察</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">City Notes</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">05</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif;">記憶收藏</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Memory Archive</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">06</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif;">情感片段</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Emotional Fragments</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">07</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif;">信仰之物</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Objects of Faith</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px;">08</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif;">其他筆記</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px;">Other Notes</span>
  </a>
</div>

---

*A NOTE TO MYSELF*

「有些文字不是為了被看見，而是為了讓某一個瞬間不至於消失。」

[關於淳文字 →]({{ '/about' | relative_url }})

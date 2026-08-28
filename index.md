---
layout: default
---

<style>
  /* 徹底隱藏 Minimal 主題預設的 header */
  header,
  .wrapper > header {
    display: none !important;
  }
  
  /* 讓 main 內容佔滿整頁 */
  section {
    width: 100% !important;
    float: none !important;
  }

  /* 強制將頁面內文與文字索引恢復為標準明體 */
  body, section, p, em, blockquote, strong, h1, h2, h3, h4, a {
    font-family: "Noto Serif TC", "Songti TC", "PMingLiU", serif !important;
    color: #333333;
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
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px; font-family: -apple-system, sans-serif;">01</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif !important;">人與人的關係</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px; font-family: -apple-system, sans-serif;">Relationships</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px; font-family: -apple-system, sans-serif;">02</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif !important;">生命經驗</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px; font-family: -apple-system, sans-serif;">Life Stories</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px; font-family: -apple-system, sans-serif;">03</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif !important;">閱讀與創作</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px; font-family: -apple-system, sans-serif;">Reading & Creation</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px; font-family: -apple-system, sans-serif;">04</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif !important;">城市觀察</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px; font-family: -apple-system, sans-serif;">City Notes</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px; font-family: -apple-system, sans-serif;">05</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif !important;">記憶收藏</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px; font-family: -apple-system, sans-serif;">Memory Archive</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px; font-family: -apple-system, sans-serif;">06</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif !important;">情感片段</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px; font-family: -apple-system, sans-serif;">Emotional Fragments</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px; font-family: -apple-system, sans-serif;">07</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif !important;">信仰之物</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px; font-family: -apple-system, sans-serif;">Objects of Faith</span>
  </a>

  <a href="{{ '/posts/' | relative_url }}" style="display: block; padding: 14px; border: 1px solid #eaeaea; border-radius: 6px; text-decoration: none; color: inherit; background-color: #fafafa;">
    <span style="font-size: 0.75rem; color: #aaa; display: block; margin-bottom: 2px; font-family: -apple-system, sans-serif;">08</span>
    <strong style="font-size: 0.95rem; font-family: 'Noto Serif TC', 'Songti TC', serif !important;">其他筆記</strong>
    <span style="display: block; font-size: 0.75rem; color: #888; margin-top: 2px; font-family: -apple-system, sans-serif;">Other Notes</span>
  </a>
</div>

---

*A NOTE TO MYSELF*

「有些文字不是為了被看見，而是為了讓某一個瞬間不至於消失。」

[關於淳文字 →]({{ '/about' | relative_url }})

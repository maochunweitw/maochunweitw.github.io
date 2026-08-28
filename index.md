---
layout: default
---

<style>
  /* 徹底隱藏 Minimal 主題預設產生的頂部 header */
  header,
  .wrapper > header {
    display: none !important;
  }
  
  /* 保持原本主題的寬度佈局 */
  section {
    width: 100% !important;
    float: none !important;
  }
</style>

<div style="letter-spacing: 2px; font-size: 0.8rem; color: #888; margin-bottom: 6px;">CHUN WEN ZI · PERSONAL JOURNAL</div>

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

* **01** [人與人的關係 · Relationships]({{ '/posts/' | relative_url }})
* **02** [生命經驗 · Life Stories]({{ '/posts/' | relative_url }})
* **03** [閱讀與創作 · Reading & Creation]({{ '/posts/' | relative_url }})
* **04** [城市觀察 · City Notes]({{ '/posts/' | relative_url }})
* **05** [記憶收藏 · Memory Archive]({{ '/posts/' | relative_url }})
* **06** [情感片段 · Emotional Fragments]({{ '/posts/' | relative_url }})
* **07** [信仰之物 · Objects of Faith]({{ '/posts/' | relative_url }})
* **08** [其他筆記 · Other Notes]({{ '/posts/' | relative_url }})

---

*A NOTE TO MYSELF*

「有些文字不是為了被看見，而是為了讓某一個瞬間不至於消失。」

[關於淳文字 →]({{ '/about' | relative_url }})

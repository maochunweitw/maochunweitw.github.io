---
layout: default
title: "公告"
---

<div style="display:flex;gap:15px;margin-bottom:20px;font-size:0.95em;">
  <a href="/" style="color:#0366d6;text-decoration:none;">首頁</a>
  <a href="/announcement.html" style="color:#0366d6;text-decoration:none;font-weight:bold;">公告</a>
  <a href="/#about" style="color:#0366d6;text-decoration:none;">關於</a>
  <a href="/#disclaimer" style="color:#0366d6;text-decoration:none;">聲明</a>
</div>

# 公告事項

<ul>
  {% for post in site.tags.公告 %}
    <li style="margin-bottom: 10px;">
      <span style="color: #666; font-size: 0.9em; margin-right: 10px;">{{ post.date | date: "%Y-%m-%d" }}</span>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% else %}
    <p style="color: #888;">目前尚無公告文章。</p>
  {% endfor %}
</ul>

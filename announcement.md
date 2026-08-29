---
layout: default
title: 公告
permalink: /announcement.html
---
<div class="page-header"><span>ANNOUNCEMENT</span><h1>公告事項</h1></div>
{% assign notices = site.tags.公告 %}{% if notices.size > 0 %}<ul class="notice-list">{% for post in notices %}<li><span>{{ post.date | date: "%Y.%m.%d" }}</span><a href="{{ post.url }}">{{ post.title }}</a></li>{% endfor %}</ul>{% else %}<p class="empty">目前尚無公告文章。</p>{% endif %}

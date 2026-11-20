---
layout: default
title: "Arsip Artikel"
permalink: /arsip/
---
# Arsip Artikel

Temukan seluruh artikel INFOKILAS berdasarkan bulan penerbitan.

{% assign archive_groups = site.posts | group_by_exp: 'post', "post.date | date: '%Y-%m'" %}
{% for group in archive_groups %}
## <span id="bulan-{{ group.name }}">{{ group.items.first.date | date: '%B %Y' }}</span>
{% for post in group.items %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: '%d-%m-%Y' }}
{% endfor %}
{% endfor %}

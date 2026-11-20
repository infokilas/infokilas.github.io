---
layout: default
title: Arsip Artikel
permalink: /arsip/
---
# Arsip Artikel

{% for post in site.posts %}
<div class="archive-item"><time>{{ post.date | date: "%d-%m-%Y" }}</time> <a href="{{ post.url | relative_url }}">{{ post.title }}</a></div>
{% endfor %}

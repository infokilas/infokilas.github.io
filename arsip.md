---
layout: default
title: Arsip Artikel
permalink: /arsip/
---
<h1>Arsip Artikel</h1>
{% assign archive_groups = site.posts | group_by_exp: 'post', "post.date | date: '%Y-%m'" %}
{% for group in archive_groups %}
{% assign first_post = group.items.first %}
<section id="bulan-{{ group.name }}" class="archive-list"><h2>{{ first_post.date | date: '%B %Y' }}</h2><ul>{% for post in group.items %}<li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <small>({{ post.date | date: '%d-%m-%Y' }})</small></li>{% endfor %}</ul></section>
{% endfor %}

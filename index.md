---
layout: default
title: Beranda
description: "Artikel terbaru INFOKILAS seputar teknologi, budaya digital, dan informasi menarik."
---
<section class="intro"><span class="eyebrow">PORTAL INFORMASI DIGITAL</span><h1>Informasi Terkini, <em>Perspektif Baru.</em></h1><p>Temukan artikel pilihan mengenai teknologi, tren, budaya, dan perkembangan dunia digital.</p></section>
{% assign sorted_posts = site.posts %}
{% if sorted_posts.size > 0 %}
{% assign featured = sorted_posts.first %}
<section class="section"><div class="section-heading"><h2>Sorotan Utama</h2><span>Artikel pilihan</span></div><a class="featured" href="{{ featured.url | relative_url }}"><div class="featured-image">{% if featured.image %}<img src="{{ featured.image | relative_url }}" alt="{{ featured.title | escape }}">{% endif %}</div><div class="featured-copy"><span class="eyebrow">{% for cat in featured.categories limit:1 %}{{ cat }}{% endfor %}</span><h3>{{ featured.title }}</h3><p>{{ featured.description | default: featured.excerpt | strip_html | truncate: 155 }}</p><span class="read-more">Baca selengkapnya →</span></div></a></section>
<section class="section"><div class="section-heading"><h2>Artikel Terbaru</h2><a href="{{ '/arsip/' | relative_url }}">Lihat semua →</a></div><div class="post-grid">{% for post in sorted_posts limit:12 %}<a class="post-card" href="{{ post.url | relative_url }}"><div class="thumb">{% if post.image %}<img src="{{ post.image | relative_url }}" alt="{{ post.title | escape }}" loading="lazy">{% endif %}</div><div class="card-body"><span class="eyebrow">{% for cat in post.categories limit:1 %}{{ cat }}{% endfor %}</span><h3>{{ post.title }}</h3><div class="meta">{{ post.date | date: '%d %B %Y' }}</div></div></a>{% endfor %}</div></section>
{% else %}<p>Artikel akan segera hadir.</p>{% endif %}

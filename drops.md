---
layout: default
title: Drops
permalink: /drops/
---
<section class="page-hero compact-hero"><p class="eyebrow">Release archive</p><h1>Drops</h1><p>Each drop captures a moment in Hockey Stock’s evolution.</p></section>
<section class="drop-list section-pad">
{% assign ordered = site.drops | sort: 'title' %}
{% for drop in ordered %}<a href="{{ drop.url | relative_url }}"><span>{{ drop.title }}</span><strong>{{ drop.description }}</strong><em>Explore →</em></a>{% endfor %}
</section>

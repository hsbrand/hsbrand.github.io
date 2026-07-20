---
layout: default
title: All Designs
permalink: /designs/
---
<section class="page-hero compact-hero"><p class="eyebrow">The archive</p><h1>All Designs</h1><p>Every release, every idea, and the story behind it.</p></section>
<section class="design-index section-pad"><div class="card-grid">
{% assign ordered = site.designs | sort: 'code' %}
{% for design in ordered %}
<a class="design-card" href="{{ design.url | relative_url }}"><div class="media-shell card-media" data-image-shell><img src="{{ design.hero | relative_url }}" alt="" loading="lazy" onerror="this.closest('[data-image-shell]').classList.add('is-missing'); this.remove();"><span class="image-fallback">{{ design.code }}<br>{{ design.title }}</span></div><div class="card-meta"><span>{{ design.code }}</span><span>{{ design.title }}</span><span>{{ design.drop }}</span></div></a>
{% endfor %}
</div></section>

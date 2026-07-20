---
layout: default
title: Team Editions
permalink: /team-editions/
---

<section class="page-hero section-pad">
  <p class="eyebrow">Custom collections</p>
  <h1>Team Editions</h1>
  <p>
    Exclusive Hockey Stock collections created with teams and adapted to
    their colours and identity.
  </p>
</section>

<section class="section-pad section-rule">
  <div class="card-grid">
    {% assign editions = site.team_editions | sort: "team_edition" %}

    {% for edition in editions %}
      <a class="design-card" href="{{ edition.url | relative_url }}">
        <div class="media-shell card-media" data-image-shell>
          <img
            src="{{ '/assets/images/team-editions/' | append: edition.slug | append: '/' | append: edition.hero_image | relative_url }}"
            alt="{{ edition.title }}"
            loading="lazy"
            onerror="this.closest('[data-image-shell]').classList.add('is-missing'); this.remove();"
          >

          <span class="image-fallback">
            {{ edition.team_edition }}<br>{{ edition.title }}
          </span>
        </div>

        <div class="card-meta">
          <span>{{ edition.team_edition }}</span>
          <span>{{ edition.title }}</span>
          <span>View collection →</span>
        </div>
      </a>
    {% endfor %}
  </div>
</section>
---
layout: default
title: Team Editions
permalink: /team-editions/
---

<section class="page-hero compact-hero">
  <p class="eyebrow">Collections</p>
  <h1>Team Editions</h1>
  <p>
    Custom Hockey Stock collections created in collaboration with teams.
    Each Team Edition brings together multiple designs under a unique team
    identity and colour palette.
  </p>
</section>

<section class="section-pad section-rule">
  <div class="drop-list">

    {% assign editions = site.team_editions | sort: "team_edition" %}

    {% for edition in editions %}

      <a href="{{ edition.url | relative_url }}">

        <span>{{ edition.team_edition }}</span>

        <div>
          <strong>{{ edition.title }}</strong><br>
          <em>{{ edition.season }}</em>
        </div>

        <span>
          {{ edition.designs | size }} Design{% if edition.designs.size != 1 %}s{% endif %} →
        </span>

      </a>

    {% endfor %}

  </div>
</section>
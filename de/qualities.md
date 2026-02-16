---
layout: default
lang: de
title: "Qualitätsmerkmale"
description: "Übersicht über alle Qualitätsmerkmale nach ISO 25010:2011"
---

<div class="qualities-page">
    <div class="container">
        <h1>Qualitätsmerkmale</h1>
        <p class="page-description">
            Die Taktiken sind nach den Qualitätsmerkmalen der ISO 25010:2011 organisiert.
        </p>

        <div class="qualities-list">
            {% assign lang_tactics = site.tactics | where: "lang", "de" %}
            {% for quality in site.data.quality_characteristics.de %}
            {% assign tactics = lang_tactics | where: "quality_characteristic_slug", quality.slug %}

            <article class="quality-item" data-quality="{{ quality.slug }}">
                <a href="{{ '/de/' | append: quality.slug | append: '/' | relative_url }}" class="quality-link">
                    <div class="quality-item-header">
                        <div class="quality-icon-large">{% include emoji.html name=quality.icon alt=quality.name %}</div>
                        <div class="quality-item-content">
                            <h2>{{ quality.name }}</h2>
                            <p class="quality-item-description">{{ quality.description }}</p>
                        </div>
                        <div class="quality-item-meta">
                            <span class="tactics-count">{{ tactics.size }}</span>
                            <span class="tactics-label">Taktiken</span>
                        </div>
                    </div>
                </a>
            </article>
            {% endfor %}
        </div>
    </div>
</div>

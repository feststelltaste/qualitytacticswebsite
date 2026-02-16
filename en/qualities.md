---
layout: default
lang: en
title: "Quality Characteristics"
description: "Overview of all quality characteristics according to ISO 25010:2011"
---

<div class="qualities-page">
    <div class="container">
        <h1>Quality Characteristics</h1>
        <p class="page-description">
            The tactics are organized according to the quality characteristics of ISO 25010:2011.
        </p>

        <div class="qualities-list">
            {% assign lang_tactics = site.tactics | where: "lang", "en" %}
            {% for quality in site.data.quality_characteristics.en %}
            {% assign tactics = lang_tactics | where: "quality_characteristic_slug", quality.slug %}

            <article class="quality-item" data-quality="{{ quality.slug }}">
                <a href="{{ '/en/' | append: quality.slug | append: '/' | relative_url }}" class="quality-link">
                    <div class="quality-item-header">
                        <div class="quality-icon-large">{% include emoji.html name=quality.icon alt=quality.name %}</div>
                        <div class="quality-item-content">
                            <h2>{{ quality.name }}</h2>
                            <p class="quality-item-description">{{ quality.description }}</p>
                        </div>
                        <div class="quality-item-meta">
                            <span class="tactics-count">{{ tactics.size }}</span>
                            <span class="tactics-label">Tactics</span>
                        </div>
                    </div>
                </a>
            </article>
            {% endfor %}
        </div>
    </div>
</div>

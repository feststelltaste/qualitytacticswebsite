---
layout: default
lang: de
title: "Start"
---

<div class="home">
    <section class="hero">
        <div class="container">
            <h1 class="hero-title">Qualitätstaktiken</h1>
            <p class="hero-subtitle">Umfassendes Handbuch für Software-Architekten</p>
            <p class="hero-description">
                Über 450 bewährte Qualitätstaktiken zur Verbesserung der Qualität von Softwaresystemen.
                Basierend auf ISO 25010:2011. Die Taktiken sind von den naheliegendsten bis zu den selten betrachteten geordnet.
            </p>
            <div class="hero-actions">
                <a href="{{ '/de/qualities/' | relative_url }}" class="btn btn-primary">{% include t.html key="explore_qualities" %}</a>
                <a href="{{ '/de/about/' | relative_url }}" class="btn btn-secondary">{% include t.html key="about" %}</a>
            </div>
        </div>
    </section>

    <section class="quality-overview">
        <div class="container">
            <h2>Qualitätsmerkmale nach ISO 25010</h2>
            <div class="qualities-grid">
                {% assign lang_tactics = site.tactics | where: "lang", "de" %}
                {% for quality in site.data.quality_characteristics.de %}
                {% assign tactics = lang_tactics | where: "quality_characteristic_slug", quality.slug %}
                <a href="{{ '/de/' | append: quality.slug | append: '/' | relative_url }}" class="quality-card" data-quality="{{ quality.slug }}">
                    <div class="quality-icon">{% include emoji.html name=quality.icon alt=quality.name %}</div>
                    <h3>{{ quality.name }}</h3>
                    <p class="quality-count">{{ tactics.size }} Taktiken</p>
                </a>
                {% endfor %}
            </div>
        </div>
    </section>
</div>

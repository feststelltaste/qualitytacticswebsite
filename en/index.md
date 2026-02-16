---
layout: default
lang: en
title: "Home"
---

<div class="home">
    <section class="hero">
        <div class="container">
            <h1 class="hero-title">Quality Tactics</h1>
            <p class="hero-subtitle">Comprehensive handbook for software architects</p>
            <p class="hero-description">
                Over 400 proven quality tactics to improve the quality of software systems.
                Based on ISO 25010:2011. The tactics are ordered from the most obvious to the seldom considered ones.
            </p>
            <div class="hero-actions">
                <a href="/en/qualities/" class="btn btn-primary">{% include t.html key="explore_qualities" %}</a>
                <a href="/en/about/" class="btn btn-secondary">{% include t.html key="about" %}</a>
            </div>
        </div>
    </section>

    <section class="quality-overview">
        <div class="container">
            <h2>Quality Characteristics per ISO 25010</h2>
            <div class="qualities-grid">
                {% assign lang_tactics = site.tactics | where: "lang", "en" %}
                {% for quality in site.data.quality_characteristics.en %}
                {% assign tactics = lang_tactics | where: "quality_characteristic_slug", quality.slug %}
                <a href="/en/{{ quality.slug }}/" class="quality-card" data-quality="{{ quality.slug }}">
                    <div class="quality-icon">{% include emoji.html name=quality.icon alt=quality.name %}</div>
                    <h3>{{ quality.name }}</h3>
                    <p class="quality-count">{{ tactics.size }} Tactics</p>
                </a>
                {% endfor %}
            </div>
        </div>
    </section>
</div>

---
layout: default
lang: de
title: "Über das Buch"
description: "Informationen über das Buch Qualitätstaktiken und den Autor Markus Harrer"
---

<div class="about-page">
    <div class="container">
        <h1>Über das Buch</h1>

        <div class="book-hero">
            <div class="book-cover">
                <a href="https://leanpub.com/qualitaetstaktiken" target="_blank" rel="noopener">
                    <img src="{{ '/assets/images/book-cover-de.png' | relative_url }}" alt="Qualitätstaktiken Buchcover" class="cover-image" />
                </a>
            </div>
            <div class="book-info">
                <h2>Qualitätstaktiken</h2>
                <p class="book-subtitle">Handbuch für Software-Architekten</p>
                <p class="book-author">von {{ site.author }}</p>
                <a href="https://leanpub.com/qualitaetstaktiken" target="_blank" rel="noopener" class="btn btn-primary btn-large">
                    {% include emoji.html name="book" alt="Book" %} Buch auf Leanpub kaufen
                </a>
            </div>
        </div>

        <section class="content-section">
            <h2>Das Buch</h2>
            <p>
                <strong>Qualitätstaktiken</strong> ist das umfassende Nachschlagewerk für Software-Architekten,
                die hochwertige Softwaresysteme entwickeln möchten. Das Buch bietet über 400 konkrete,
                praxiserprobte Taktiken zur systematischen Verbesserung der Softwarequalität.
            </p>
            <p>
                Jede Taktik ist strukturiert beschrieben und nach den Qualitätsmerkmalen der ISO 25010:2011
                organisiert. Das Buch dient als Ideenquelle für verschiedene Situationen und Kontexte –
                von der Anforderungsanalyse über die Architekturentscheidung bis zur Implementierung und
                dem Betrieb.
            </p>
            <p>
                Egal ob Sie ein konkretes Qualitätsproblem lösen, eine Architektur-Review durchführen oder
                sich einfach inspirieren lassen möchten – die Qualitätstaktiken bieten Ihnen fundierte
                Lösungsansätze für nahezu jede Herausforderung in der Softwareentwicklung.
            </p>
        </section>

        <section class="content-section">
            <h2>Für wen ist dieses Buch?</h2>
            <ul class="audience-list">
                <li><strong>Software-Architekten</strong> – die fundierte Entscheidungen treffen müssen</li>
                <li><strong>Entwicklungsteams</strong> – die Qualität systematisch verbessern wollen</li>
                <li><strong>Technical Leads</strong> – die ihre Teams zu besserer Qualität führen möchten</li>
                <li><strong>Qualitätsbeauftragte</strong> – die konkrete Maßnahmen benötigen</li>
                <li><strong>Studierende</strong> – die praktische Softwarequalität verstehen wollen</li>
            </ul>
        </section>

        <section class="content-section">
            <h2>Struktur und Inhalt</h2>
            <p>
                Die über 400 Taktiken sind nach den <strong>8 Qualitätsmerkmalen der ISO 25010:2011</strong> organisiert, ergänzt durch eine zusätzliche Kategorie <strong>Qualitätsillusionen</strong>:
            </p>
            <div class="qualities-overview">
                {% for quality in site.data.quality_characteristics.de %}
                {% assign lang_tactics = site.tactics | where: "lang", "de" %}
                {% assign tactics = lang_tactics | where: "quality_characteristic_slug", quality.slug %}
                <div class="quality-item-mini">
                    <span class="quality-icon">{% include emoji.html name=quality.icon alt=quality.name %}</span>
                    <strong>{{ quality.name }}</strong>
                    <span class="quality-count">({{ tactics.size }} Taktiken)</span>
                </div>
                {% endfor %}
            </div>
            <p>
                Jede Taktik beschreibt einen konkreten Lösungsansatz mit:
            </p>
            <ul>
                <li>Prägnanter Beschreibung der Taktik</li>
                <li>Zuordnung zu Qualitätsmerkmalen und Teilmerkmalen</li>
                <li>Konsequenzen und Trade-offs</li>
                <li>Praktischen Hinweisen zur Umsetzung</li>
            </ul>
        </section>

        <section class="content-section">
            <h2>Über den Autor</h2>
            <p>
                <strong>{{ site.author }}</strong> ist Software-Architekt mit langjähriger Erfahrung in der
                Entwicklung und Bewertung von Softwaresystemen. Als Experte für Softwarequalität hat er
                zahlreiche Projekte begleitet und Teams dabei unterstützt, qualitativ hochwertige Software
                zu entwickeln.
            </p>
        </section>

        <section class="content-section">
            <h2>Wie nutze ich das Buch?</h2>
            <p>
                Die Qualitätstaktiken können auf vielfältige Weise genutzt werden:
            </p>
            <ul>
                <li><strong>Als Nachschlagewerk:</strong> Gezielt nach Lösungen für spezifische Qualitätsprobleme suchen</li>
                <li><strong>Als Checkliste:</strong> Bei Architektur-Reviews systematisch verschiedene Qualitätsaspekte prüfen</li>
                <li><strong>Als Inspirationsquelle:</strong> Neue Ideen für Verbesserungen entdecken</li>
                <li><strong>Als Lernressource:</strong> Systematisch Wissen über Softwarequalität aufbauen</li>
                <li><strong>Im Team:</strong> Gemeinsame Basis für Qualitätsdiskussionen schaffen</li>
            </ul>
        </section>

        <section class="content-section">
            <h2>Online-Version</h2>
            <p>
                Diese Website bietet Ihnen kostenfreien Zugang zu allen Taktiken aus dem Buch.
                Durchsuchen Sie die Taktiken nach Qualitätsmerkmalen, nutzen Sie die Sprachumschaltung
                zwischen Deutsch und Englisch, und finden Sie schnell die passende Lösung für Ihr Problem.
            </p>
            <p>
                Das vollständige Buch mit ausführlichen Erläuterungen, zusätzlichen Beispielen und
                weiterführenden Informationen ist auf Leanpub erhältlich.
            </p>
        </section>

        <section class="content-section">
            <h2>ISO 25010:2011</h2>
            <p>
                Die Struktur des Buches basiert auf dem internationalen Standard
                <strong>ISO/IEC 25010:2011</strong> (Systems and software engineering — Systems and software
                Quality Requirements and Evaluation — System and software quality models).
                Dieser Standard definiert ein Qualitätsmodell für Software-Produkte und -Systeme mit acht
                primären Qualitätsmerkmalen.
            </p>
            <p>
                Zusätzlich enthält das Buch das Kapitel <strong>Qualitätsillusionen</strong>, das vermeintliche
                Qualitätsverbesserungen behandelt, die in Wirklichkeit keine echten Verbesserungen darstellen
                oder sogar kontraproduktiv sein können.
            </p>
        </section>

        <div class="cta-box">
            <h3>{% include emoji.html name="book" alt="Book" %} Buch kaufen</h3>
            <p>Holen Sie sich das vollständige Buch mit allen Details und Hintergründen</p>
            <a href="https://leanpub.com/qualitaetstaktiken" target="_blank" rel="noopener" class="btn btn-primary">
                Auf Leanpub kaufen
            </a>
            <p class="cta-note">oder <a href="{{ '/de/qualities/' | relative_url }}">kostenlos die Online-Version nutzen</a></p>
        </div>
    </div>
</div>

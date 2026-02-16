---
layout: default
lang: en
title: "About the Book"
description: "Information about the Quality Tactics book and author Markus Harrer"
---

<div class="about-page">
    <div class="container">
        <h1>About the Book</h1>

        <div class="book-hero">
            <div class="book-cover">
                <a href="https://leanpub.com/qualitytactics" target="_blank" rel="noopener">
                    <img src="{{ '/assets/images/book-cover-en.png' | relative_url }}" alt="Quality Tactics Book Cover" class="cover-image" />
                </a>
            </div>
            <div class="book-info">
                <h2>Quality Tactics</h2>
                <p class="book-subtitle">Handbook for Software Architects</p>
                <p class="book-author">by {{ site.author }}</p>
                <a href="https://leanpub.com/qualitytactics" target="_blank" rel="noopener" class="btn btn-primary btn-large">
                    {% include emoji.html name="book" alt="Book" %} Buy Book on Leanpub
                </a>
            </div>
        </div>

        <section class="content-section">
            <h2>The Book</h2>
            <p>
                <strong>Quality Tactics</strong> is the comprehensive reference work for software architects
                who want to develop high-quality software systems. The book offers over 400 concrete,
                proven tactics for the systematic improvement of software quality.
            </p>
            <p>
                Each tactic is described in a structured way and organized according to the quality
                characteristics of ISO 25010:2011. The book serves as a source of ideas for different
                situations and contexts – from requirements analysis through architecture decisions to
                implementation and operations.
            </p>
            <p>
                Whether you want to solve a specific quality problem, conduct an architecture review, or
                simply get inspired – Quality Tactics provides you with well-founded solution approaches
                for almost every challenge in software development.
            </p>
        </section>

        <section class="content-section">
            <h2>Who is this book for?</h2>
            <ul class="audience-list">
                <li><strong>Software Architects</strong> – who need to make informed decisions</li>
                <li><strong>Development Teams</strong> – who want to systematically improve quality</li>
                <li><strong>Technical Leads</strong> – who want to guide their teams to better quality</li>
                <li><strong>Quality Managers</strong> – who need concrete measures</li>
                <li><strong>Students</strong> – who want to understand practical software quality</li>
            </ul>
        </section>

        <section class="content-section">
            <h2>Structure and Content</h2>
            <p>
                The over 400 tactics are organized according to the <strong>8 quality characteristics of ISO 25010:2011</strong>, plus an additional special category <strong>Quality Illusions</strong>:
            </p>
            <div class="qualities-overview">
                {% for quality in site.data.quality_characteristics.en %}
                {% assign lang_tactics = site.tactics | where: "lang", "en" %}
                {% assign tactics = lang_tactics | where: "quality_characteristic_slug", quality.slug %}
                <div class="quality-item-mini">
                    <span class="quality-icon">{% include emoji.html name=quality.icon alt=quality.name %}</span>
                    <strong>{{ quality.name }}</strong>
                    <span class="quality-count">({{ tactics.size }} tactics)</span>
                </div>
                {% endfor %}
            </div>
            <p>
                Each tactic describes a concrete solution approach with:
            </p>
            <ul>
                <li>Concise description of the tactic</li>
                <li>Assignment to quality characteristics and sub-characteristics</li>
                <li>Consequences and trade-offs</li>
                <li>Practical hints for implementation</li>
            </ul>
        </section>

        <section class="content-section">
            <h2>About the Author</h2>
            <p>
                <strong>{{ site.author }}</strong> is a software architect with many years of experience
                in developing and evaluating software systems. As an expert in software quality, he has
                accompanied numerous projects and supported teams in developing high-quality software.
            </p>
        </section>

        <section class="content-section">
            <h2>How to use the book?</h2>
            <p>
                Quality Tactics can be used in various ways:
            </p>
            <ul>
                <li><strong>As a reference:</strong> Search specifically for solutions to specific quality problems</li>
                <li><strong>As a checklist:</strong> Systematically review different quality aspects during architecture reviews</li>
                <li><strong>As inspiration:</strong> Discover new ideas for improvements</li>
                <li><strong>As a learning resource:</strong> Systematically build knowledge about software quality</li>
                <li><strong>In teams:</strong> Create a common basis for quality discussions</li>
            </ul>
        </section>

        <section class="content-section">
            <h2>Online Version</h2>
            <p>
                This website provides you with free access to all tactics from the book.
                Browse tactics by quality characteristics, use the language switch between German and English,
                and quickly find the right solution for your problem.
            </p>
            <p>
                The complete book with detailed explanations, additional examples, and further information
                is available on Leanpub.
            </p>
        </section>

        <section class="content-section">
            <h2>ISO 25010:2011</h2>
            <p>
                The structure of the book is based on the international standard
                <strong>ISO/IEC 25010:2011</strong> (Systems and software engineering — Systems and software
                Quality Requirements and Evaluation — System and software quality models).
                This standard defines a quality model for software products and systems with eight primary
                quality characteristics.
            </p>
            <p>
                Additionally, the book contains the chapter <strong>Quality Illusions</strong>, which addresses
                supposed quality improvements that do not actually represent real improvements or may even be
                counterproductive.
            </p>
        </section>

        <div class="cta-box">
            <h3>{% include emoji.html name="book" alt="Book" %} Buy the Book</h3>
            <p>Get the complete book with all details and background information</p>
            <a href="https://leanpub.com/qualitytactics" target="_blank" rel="noopener" class="btn btn-primary">
                Buy on Leanpub
            </a>
            <p class="cta-note">or <a href="{{ '/en/qualities/' | relative_url }}">use the online version for free</a></p>
        </div>
    </div>
</div>

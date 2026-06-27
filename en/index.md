---
layout: home
lang: en
title: "Engineering Notes"
permalink: /en/
alternate_url: /kr/
---

<section class="hero">
  <p class="eyebrow">SOFTWARE · GAME DEVELOPMENT · AI WORKFLOW</p>
  <h1>Development Standards<br>and Rationale.</h1>
  <p class="hero-copy">
    A technical document repository for Codex workflow rules, Design.html standards, Unity C# conventions, and development methodology.
    It keeps reusable rules and decision rationale in one place.
  </p>
  <div class="hero-actions">
    <a class="button button-primary" href="#notes">Browse notes</a>
    <a class="button button-secondary" href="https://github.com/{{ site.github.repository_nwo }}">GitHub repository</a>
  </div>
</section>

<section class="section" id="notes">
  <div class="section-heading">
    <div>
      <p class="eyebrow">COLLECTIONS</p>
      <h2>Notes By Topic</h2>
    </div>
    <p>Currently publishing 4 notes across 3 topics.</p>
  </div>

  <div class="collection-grid">
    <a class="collection-card collection-card-codex" href="{{ "/en/codex/" | relative_url }}">
      <span class="card-index">01</span>
      <span class="card-label">AI WORKFLOW</span>
      <h3>Codex</h3>
      <p>Shared working rules and planning-document standards for producing consistent agent outputs.</p>
      <span class="card-link">View 2 notes <span aria-hidden="true">→</span></span>
    </a>

    <a class="collection-card collection-card-unity" href="{{ "/en/unity/" | relative_url }}">
      <span class="card-index">02</span>
      <span class="card-label">GAME DEVELOPMENT</span>
      <h3>Unity</h3>
      <p>Practical C# writing rules and structural standards for Unity projects.</p>
      <span class="card-link">View 1 note <span aria-hidden="true">→</span></span>
    </a>

    <a class="collection-card collection-card-essay" href="{{ "/en/essays/debuggingless-development/" | relative_url }}">
      <span class="card-index">03</span>
      <span class="card-label">ENGINEERING ESSAY</span>
      <h3>Development Philosophy</h3>
      <p>Thinking about logical design during code writing before reactive debugging takes over.</p>
      <span class="card-link">Read essay <span aria-hidden="true">→</span></span>
    </a>
  </div>
</section>

<section class="section latest-section">
  <div class="section-heading">
    <div>
      <p class="eyebrow">ALL NOTES</p>
      <h2>All Notes</h2>
    </div>
  </div>

  <div class="note-list">
    <a class="note-row" href="{{ "/en/codex/common-work-guidelines.html" | relative_url }}">
      <span class="note-type">GUIDELINE</span>
      <span class="note-title">Codex Common Work Guidelines</span>
      <span class="note-topic">Codex</span>
      <span class="note-arrow" aria-hidden="true">↗</span>
    </a>
    <a class="note-row" href="{{ "/en/codex/guideline-design-generation.review.html" | relative_url }}">
      <span class="note-type">REVIEW</span>
      <span class="note-title">Design.html Planning Document Standard</span>
      <span class="note-topic">Codex</span>
      <span class="note-arrow" aria-hidden="true">↗</span>
    </a>
    <a class="note-row" href="{{ "/en/unity/csharp-coding-convention.html" | relative_url }}">
      <span class="note-type">CONVENTION</span>
      <span class="note-title">Unity C# Coding Convention</span>
      <span class="note-topic">Unity</span>
      <span class="note-arrow" aria-hidden="true">↗</span>
    </a>
    <a class="note-row" href="{{ "/en/essays/debuggingless-development/" | relative_url }}">
      <span class="note-type">ESSAY</span>
      <span class="note-title">Debuggingless Development</span>
      <span class="note-topic">Architecture</span>
      <span class="note-arrow" aria-hidden="true">↗</span>
    </a>
  </div>
</section>
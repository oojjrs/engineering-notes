---
layout: home
title: "Engineering Notes"
permalink: /
---

<section class="hero">
  <p class="eyebrow">SOFTWARE · GAME DEVELOPMENT · AI WORKFLOW</p>
  <h1>덜 헤매고,<br>더 오래 쓰는 설계.</h1>
  <p class="hero-copy">
    소프트웨어 아키텍처와 개발 규칙을 실제로 다시 찾아볼 수 있는 형태로 정리합니다.
    짧은 메모보다 오래 유지되는 기준과 판단 근거를 남기는 문서 저장소입니다.
  </p>
  <div class="hero-actions">
    <a class="button button-primary" href="#notes">문서 둘러보기</a>
    <a class="button button-secondary" href="https://github.com/{{ site.github.repository_nwo }}">GitHub 저장소</a>
  </div>
</section>

<section class="section" id="notes">
  <div class="section-heading">
    <div>
      <p class="eyebrow">COLLECTIONS</p>
      <h2>주제별 문서</h2>
    </div>
    <p>현재 3개 주제, 4개 문서를 공개하고 있습니다.</p>
  </div>

  <div class="collection-grid">
    <a class="collection-card collection-card-codex" href="{{ "/codex/" | relative_url }}">
      <span class="card-index">01</span>
      <span class="card-label">AI WORKFLOW</span>
      <h3>Codex</h3>
      <p>에이전트가 일관된 결과물을 만들기 위한 작업 원칙과 문서 생성 기준.</p>
      <span class="card-link">문서 2개 보기 <span aria-hidden="true">→</span></span>
    </a>

    <a class="collection-card collection-card-unity" href="{{ "/unity/" | relative_url }}">
      <span class="card-index">02</span>
      <span class="card-label">GAME DEVELOPMENT</span>
      <h3>Unity</h3>
      <p>Unity 프로젝트에서 바로 적용할 수 있는 C# 작성 규칙과 구조적 기준.</p>
      <span class="card-link">문서 1개 보기 <span aria-hidden="true">→</span></span>
    </a>

    <a class="collection-card collection-card-essay" href="{{ "/essays/debuggingless-development/" | relative_url }}">
      <span class="card-index">03</span>
      <span class="card-label">ENGINEERING ESSAY</span>
      <h3>개발 철학</h3>
      <p>디버깅 기술보다 버그가 생기기 어려운 시스템 설계를 먼저 생각합니다.</p>
      <span class="card-link">에세이 읽기 <span aria-hidden="true">→</span></span>
    </a>
  </div>
</section>

<section class="section latest-section">
  <div class="section-heading">
    <div>
      <p class="eyebrow">ALL NOTES</p>
      <h2>전체 문서</h2>
    </div>
  </div>

  <div class="note-list">
    <a class="note-row" href="{{ "/codex/common-work-guidelines.html" | relative_url }}">
      <span class="note-type">GUIDELINE</span>
      <span class="note-title">Codex 공통 작업 지침</span>
      <span class="note-topic">Codex</span>
      <span class="note-arrow" aria-hidden="true">↗</span>
    </a>
    <a class="note-row" href="{{ "/codex/guideline-design-generation.review.html" | relative_url }}">
      <span class="note-type">REVIEW</span>
      <span class="note-title">Design.html / Guidelines.html 생성 기준</span>
      <span class="note-topic">Codex</span>
      <span class="note-arrow" aria-hidden="true">↗</span>
    </a>
    <a class="note-row" href="{{ "/unity/csharp-coding-convention.html" | relative_url }}">
      <span class="note-type">CONVENTION</span>
      <span class="note-title">Unity C# 코딩 컨벤션</span>
      <span class="note-topic">Unity</span>
      <span class="note-arrow" aria-hidden="true">↗</span>
    </a>
    <a class="note-row" href="{{ "/essays/debuggingless-development/" | relative_url }}">
      <span class="note-type">ESSAY</span>
      <span class="note-title">디버깅이 거의 필요 없는 시스템을 설계하기</span>
      <span class="note-topic">Architecture</span>
      <span class="note-arrow" aria-hidden="true">↗</span>
    </a>
  </div>
</section>

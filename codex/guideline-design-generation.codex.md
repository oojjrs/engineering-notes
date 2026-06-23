# Guidelines/Design Generation Review Companion

Mandatory first rule for Codex: before creating, adding to, reviewing, or editing any `Design.html` or `Guidelines.html`, use the matching skill and reopen the live project documents. This companion and the HTML review page are review surfaces, not substitutes for the skills.

Last updated: 2026-06-15 KST

This file is a companion note for the human review page, not the authoritative Codex skill source.

Authoritative Codex-facing rules live in:

- `C:\Users\oojjr\.codex\skills\project-guidelines-builder\SKILL.md`
- `C:\Users\oojjr\.codex\skills\overlord-design-document\SKILL.md` when the work is specifically about `H:\Overlord\Design.html`

Human review page:

- `C:\Users\oojjr\Documents\Codex\GlobalReviews\guideline-design-generation.review.html`

Bundled sample snapshots:

- `C:\Users\oojjr\Documents\Codex\GlobalReviews\samples\ImageStudio.Guidelines.sample.html`
- `C:\Users\oojjr\Documents\Codex\GlobalReviews\samples\Overlord.Design.sample.html`

## Rolling Sample Model

- The best sample is not permanently bound to ImageStudio or Overlord once their rules have propagated.
- Use the most recently edited and validated live document of the same type as the rolling benchmark.
- ImageStudio Guidelines and Overlord Design remain historical seeds and project-specific authorities for themselves, not fixed global winners.
- Bundled samples are offline snapshots only.

## Current Source-Of-Truth Model

- `Guidelines.html`: practical work instructions for Codex threads. It records workflow rules, queue/card state, validation expectations, active risks, and handoff notes.
- `Design.html`: game planning instructions for humans and Codex. It records what the game is, why decisions were made, and how future design work should stay consistent.
- `README.md`: usually GitHub/public-facing. Do not treat it as the work-instruction source unless the project explicitly uses it that way.
- `AGENTS.md`: no longer assumed inside each project. If it exists, read it, but do not require it for new project docs.
- Personal Codex settings: useful but not enough, because the user may open Codex from multiple places where personal settings are not synchronized.

## What To Duplicate Into Project Docs

Do not copy every personal setting into every project. Duplicate only project-critical rules that would cause real damage or confusion if missing:

- irreversible operations require explicit approval unless the immediately preceding user instruction already authorizes them
- preserve source encoding and line endings; new text defaults to UTF-8 No-BOM and CRLF
- feedback and document writing should be Korean when the user/project preference is Korean
- read live `Guidelines.html` and `Design.html` before project work when they exist
- when code has changed after the latest design artifact, code is authoritative for implemented behavior and Design.html should be updated to match it
- update `Guidelines.html` when task state, validation state, shared workflow rules, or queue cards change
- keep unrelated dirty changes intact
- do not turn ordinary third-party dependency, SDK, package, API workaround, or compatibility patch work into `Guidelines.html` task cards unless the user explicitly asks, the integration is a core product surface, or tracked QA/risk is genuinely needed

## Start Of Work

1. Reopen the live project docs that actually exist, especially `Guidelines.html` and `Design.html`.
2. Read `README.md` only for public/product context unless the project says it is also an operations guide.
3. Read `AGENTS.md` if it exists, but do not assume every project has one.
4. Check `git status --short --branch` before planning edits.
5. Treat current repo-local files as the source of truth. Do not rely on old memory or external drafts when live files exist.

## Guidelines.html Creation

Create `Guidelines.html` only when the repo lacks a comparable live guide or the user asks for one.

Include the smallest useful set of sections:

- project purpose and current direction
- start-of-thread checklist
- irreversible-operation approval rules
- encoding, line-ending, Korean-feedback, and unrelated-change handling rules
- build, validation, and test commands known to work
- task queues for waiting, active, verification, future, and done when parallel work is expected
- task-code-based `git worktree` and `codex/<task-code>` branch rules when multiple Codex threads may work in parallel
- recent decisions, open risks, and validation history

Do not add board cards for ordinary third-party workaround tasks. Most third-party patching should stay as inline work, not durable queue state.

Maintenance rules:

- Treat `Guidelines.html` as an operational board, not disposable notes.
- Keep changes scoped to the current task.
- Preserve existing layout, classes, scripts, queue marker comments, and card shape.
- When queue cards exist, update card status, visible badge, current state, next step, file list, validation, and timestamp together.
- Do not move implementation cards to done until user QA or integration-owner confirmation is recorded.

Rolling guideline benchmark:

- Live: most recently edited and validated `Guidelines.html` carrying the current shared rules
- Historical seed: `H:\ImageStudio\Guidelines.html`
- Snapshot: `C:\Users\oojjr\Documents\Codex\GlobalReviews\samples\ImageStudio.Guidelines.sample.html`

## Design.html Creation

Create or update `Design.html` as the planning source for both humans and Codex.

Design documents must move from high abstraction to concrete detail:

- start with the largest frame: goal, genre, progression mode, and core promise
- then explain progression: how play advances, where fun comes from, how the player becomes better, and what the designer intends
- group sections at the same abstraction level before moving into narrower details
- keep the first broad section expanded
- collapse later sections so dense detail does not overload the surface

The design document should answer "why" especially well:

- why this feature/system exists
- why a direction was chosen over alternatives
- what problem the decision solved
- what constraints or risks shaped the decision
- what future Codex threads should preserve when extending the design

Recommended sections:

- current game/product direction
- user experience goals
- core systems or feature areas
- screen, flow, content, or rules plans
- decision records with rationale
- rejected alternatives when they explain the chosen direction
- open questions and risks
- asset/reference notes
- change log

Design document rules:

- Keep visible planning content readable for the user and precise enough for Codex.
- Treat `Design.html` as the final decision and rationale surface, not a transcript or archive of every intermediate result.
- Remove obsolete drafts, rejected intermediate outputs, process history, and temporary comparison notes when a next version or final artifact replaces them.
- Put planning-document intermediate files such as candidate images/video/audio, comparison sheets, temporary conversion outputs, contact sheets, and discarded drafts under the project-root `$Trash/...`; keep `DesignAssets` and `GuidelinesAssets` for final or currently referenced document assets only.
- Keep the document aligned with the current implemented state; unimplemented assumptions should be clearly separated as open questions or risks.
- If source code and Design.html disagree after code was manually changed, treat the code as the implemented truth and revise the design document to match the code and latest user intent.
- Prefer images, video, audio, previews, and other directly understandable evidence over long prose.
- Use prose mainly to explain the reasoning, constraints, and future-preservation intent that the media cannot show.
- Add compact `?` tooltip help for domain-limited terms, proper nouns, project-internal names, abbreviations, art jargon, and system terms that need explanation. If Codex does not know what the term means in the user's project, it must ask the user and add the answer instead of guessing.
- Put operational workflow rules in `Guidelines.html`, skills, or review docs instead of mixing them into the planning body.
- Use collapsible sections or compact summaries when the document becomes long.
- Prefer concrete project-specific wording over generic templates.

## Default Game Planning Categories

When creating a first `Design.html` for a game, start from these reusable categories, then delete categories that do not apply after the project direction is known. Do not add highly genre-local sections by default; put puzzle-stage, factory-logistics, strategy-diplomacy, survival-hunger, or similar genre-specific topics under the nearest general category unless the project truly needs a dedicated section.

1. Core Direction - identity, genre, progression mode, core promise, target experience, victory/loss, difficulty, mastery.
2. World And Space - worldbuilding, story premise, factions, world map, regions, dungeons, environment, traversal, discovery.
3. Level And Content Structure - stages, chapters, missions, scenarios, campaigns, level packs, content cadence, difficulty curve.
4. Characters And Growth - characters, roles/classes, stats, skills, traits, status effects, leveling, party/companions, enemies where appropriate.
5. Rules And Calculation Model - turns/ticks, formulas, scoring, probability, generation rules, AI behavior, economy simulation, combat resolution.
6. Items And Economy - items, equipment, resources, currencies, rewards, drops, inventory, shops/trading, blueprints, crafting, upgrades.
7. Quests And Events - quests, missions, requests, events, achievements, ranking goals, tutorials, repeatable and endgame content.
8. Interaction And Combat - controls, targeting, board/tile rules, action feedback, combat rules, boss patterns, failure/retry flow.
9. Presentation And Communication - dialogue, voice, cutscenes, camera, sound/BGM/SFX, UI copy, notifications, logs, reactions.
10. UI And Convenience - HUD, menus, settings, save/load, accessibility, input/keybinds, localization, help, tooltips, profile/account.
11. Meta And Live Systems - unlocks, collections, progression memory, multiplayer, lobby/matching, social/guilds, server sync, live operations.
12. Undecided And Exclusions - open questions, deferred items, rejected directions, risks, next-version candidates.

These categories are a scaffold, not a checklist to preserve forever. A strong project document may merge, rename, or remove categories so the final document matches the actual implemented game.


Rolling design benchmark:

- Live: most recently edited and validated `Design.html` carrying the current shared rules
- Historical seed: `H:\Overlord\Design.html`
- Snapshot: `C:\Users\oojjr\Documents\Codex\GlobalReviews\samples\Overlord.Design.sample.html`

## Skill Maintenance

The skill layer must stay tidy and explicit:

- `project-guidelines-builder` owns generic `Guidelines.html` creation and maintenance.
- `image-first-art-workflow` owns the imagegen-first rule for image, UI art, game asset, sprite, and visual reference work. Human review page: `C:\Users\oojjr\Documents\Codex\GlobalReviews\image-first-art-workflow.review.html`.
- A design-document skill should own reusable `Design.html` creation rules. Today the strongest concrete design skill is `overlord-design-document`; if the same pattern becomes cross-project, extract a generic design-document skill instead of overloading the guideline skill.
- Each skill should describe the rolling live benchmark policy and name bundled snapshots as historical references only.
- Skills should point to current project files first, then memory, then historical examples.

## Validation

Before finishing, check the relevant subset:

- `git diff --check`
- encoding and line-ending preservation
- HTML marker presence and obvious tag balance
- tooltip coverage for domain-specific terms and proper nouns that need explanation
- project-specific build/test commands
- skill validator if a skill was changed
- final diff review for accidental broad rewrites

If a check cannot be run, report it plainly with the reason.

# AGENTS.md – Build Plan for lemn**IQ** Prompting Cookbook

_Instructions and task breakdown for autonomous or semi‑autonomous agents charged with completing and polishing the cookbook._

## 1. Purpose
This file orchestrates multiple specialized agents (or agentic “steps”) to flesh out, refine, and QA every Markdown page inside the lemn**IQ** Prompting Cookbook project.

## 2. Directory Overview
```
lemniq_prompting_cookbook/
├── README.md
├── fundamentals.md
├── advanced_techniques.md
├── troubleshooting.md
├── quick_reference.md
├── resources.md
├── AGENTS.md      <-- (this file)
└── recipes/
    ├── Writing_Marketing.md
    ├── Analysis_Strategy.md
    ├── Automation_Scripting.md
    └── Learning_Coaching.md
```

## 3. Agent Roles & Responsibilities

| Agent Name | Primary Goal | Key Skills | Output File(s) |
|------------|--------------|-----------|----------------|
| **Lead Editor Agent** | Maintain voice, coherence, and structure across cookbook. Approve merges. | Style guidance, editing, project mgmt. | All |
| **Content Author Agent** | Draft missing sections & expand stubs to ~80% maturity. | Domain expertise, prompt engineering, instructional design. | fundamentals.md, advanced_techniques.md, recipes/\*.md |
| **Example Curator Agent** | Populate each template with two concrete worked examples using GPT‑4o. | Prompt testing, summarization. | recipes/\*.md |
| **Formatter Agent** | Ensure Markdown tables, code fences, and lists render correctly. | Markdown linting, regex rewrites. | All |
| **Link Checker Agent** | Validate URLs, ensure HTTPS, add archive links if needed. | HTTP requests, status check. | resources.md |
| **QA Agent** | Run hallucination check, spell‑check, and consistency sweep. | Fact‑checking, language tools. | QA report (QA_REPORT.md) |

## 4. Task Breakdown by File

### 4.1 README.md
1. **Content Author:** Add high‑level cookbook summary (≤120 words).
2. **Formatter:** Verify directory tree code block uses backticks & fixed‑width font.
3. **QA:** Spell‑check and ensure “lemn**IQ**” styling (lowercase “lemn”, bold IQ where context allows).

### 4.2 fundamentals.md
* Flesh out **2.4** section on *Prompt Iteration Cycle* (plan‑write‑critique‑revise).
* Insert diagram description (alt text) that visualizes the lemn**IQ** Formula flow.
* Provide two prompts demonstrating temperature extremes (0.2 vs 0.8) with outputs.

### 4.3 advanced_techniques.md
* Add section **4.5 Multi‑Agent Prompt Orchestration** (simple JSON schema + example).

### 4.4 troubleshooting.md
* [x] Expand table with at least three more common issues (rate‑limits, policy refusal, formatting loss).
* [x] Add “When to escalate to human” checklist.

### 4.5 quick_reference.md
* [x] Convert shortcut list into a two‑column table if width permits.

### 4.6 resources.md
* [x] Add 3 podcasts, 2 YouTube channels, and 1 newsletter relevant to prompt engineering.

### 4.7 recipes/\*.md
* [x] Each recipe file must reach **min. 5** use‑cases with template + 1 example each.
* [x] Example Curator Agent to run prompts in GPT‑4o and paste trimmed outputs (<120 words).

## 5. Workflow & Dependencies
1. **Content Author** drafts/expands sections (label commit `content-draft`).
2. **Example Curator** injects examples (`examples-added`).
3. **Formatter Agent** runs automatic linting (`style-fix`).
4. **Link Checker Agent** validates links (`link-pass`).
5. **QA Agent** runs checks; if pass, notifies **Lead Editor**.
6. **Lead Editor Agent** merges into `main`.

## 6. Acceptance Criteria
* No TODOs or “Lorem ipsum”.
* Spelling & grammar score ≥ 95 % (Grammarly or equivalent).
* All links 200 OK.
* Markdown renders correctly in GitHub preview.
* Cookbook <= 25 MB total (for repo portability).

## 7. Stretch Tasks
* **Diagram Agent**: Generate SVG flow diagrams for lemn**IQ** Formula and Prompt Lifecycle.
* [x] **Localization Agent**: Draft a Spanish‑language README.es.md.
* **Packaging Agent**: Create a GitHub Action that zips and publishes the latest cookbook as a downloadable artifact on every tag.

## Completed Tasks
* [x] README summary added
* [x] Section 2.4 on Prompt Iteration Cycle
* [x] Recipe expansions

## Upcoming Improvements
* [x] Expand "About This Cookbook" with a benefits/use-cases bullet list.
* [x] Add a Table of Contents to `fundamentals.md` and `advanced_techniques.md`.
* Include more detailed examples in the recipes.
* Link cross-references between related sections.
* Add a glossary of prompt-engineering terms.
* [x] Ensure diagrams (e.g., `lemniq-formula.svg`) have descriptive alt text.
* [x] Document additional pitfalls such as instruction-following failures.
* [x] Improve quick-reference docs with shortcuts or cheat‑sheet prompts.
* Diversify learning resources beyond podcasts and YouTube.
* [x] Provide at least one translated README (e.g., Spanish).
* Create a visual diagram of the Prompt Iteration Cycle.
* Summarize each section with a short TL;DR box.
* Maintain a version history or changelog.
* Embed code snippets (Python/Bash) where relevant.
* Check header hierarchy for accessibility.
* Insert a usage warning about data privacy or responsible AI.
* Introduce a linter or GitHub Action for automatic testing.
* Include screenshots of real model outputs if available.
* Document contribution guidelines for external PRs.

---
*Last updated: 17 May 2025 by lemn**IQ** AI Ops.*

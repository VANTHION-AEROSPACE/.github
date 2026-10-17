# Brand and documentation guidelines

These guidelines govern how Vanthion Aerospace presents itself in public: the organisation profile, repository documentation, and any text that accompanies the work. They exist for one reason. The company's credibility rests on its engineering discipline, so its writing must demonstrate that discipline.

**Contents**

1. [Identity](#1-identity)
2. [Three levels of messaging](#2-three-levels-of-messaging)
3. [Voice](#3-voice)
4. [Terminology](#4-terminology)
5. [Claims policy](#5-claims-policy)
6. [Markdown conventions](#6-markdown-conventions)
7. [Link style](#7-link-style)
8. [Repository naming and metadata](#8-repository-naming-and-metadata)
9. [Visual rules](#9-visual-rules)
10. [Pre-publication checklist](#10-pre-publication-checklist)

---

## 1. Identity

### Names

| Use | Do not use |
|:--|:--|
| Vanthion Aerospace | VANTHION AEROSPACE in running text, Vanthion Aerospace Pvt Ltd, VA |
| Vanthion (short form, after first full mention) | Vanthion Space, Vanthion Labs |
| SATSentinel-X | SATSentinel X, SatSentinel-X, SATSentinelX (except in a legacy repository name) |
| SX-OD1 | SX OD1, SXOD1 |

The capitalised form appears only in the logo artwork and in the GitHub organisation login.

### Logo

Two approved identity files are kept in [`assets/brand/`](assets/brand/):

| File | Use |
|:--|:--|
| `vanthion-aerospace-logo.png` | The company mark and wordmark. |
| `satsentinel-x-emblem.png` | The SATSentinel-X programme emblem, which carries the line "A technology programme by Vanthion Aerospace". |

Rules:

- Use the files unchanged. Do not recolour, stretch, crop through the mark, add effects, or redraw them.
- Both files have a pure black background. Place them on black, or use the prepared banners.
- Do not present a new or modified mark as the official logo.
- Provenance and file hashes are recorded in [`assets/brand/README.md`](assets/brand/README.md).

**Replacing the logo.** When a final vector logo exists, replace the two PNG files in `assets/brand/`, update the hashes in the provenance file, and regenerate the banners in `profile/assets/`.

---

## 2. Three levels of messaging

Each piece of writing belongs to exactly one level. The level decides the audience, the vocabulary, and what may be claimed.

| | Company | Programme | Technical repository |
|:--|:--|:--|:--|
| **Subject** | Vanthion Aerospace | SATSentinel-X, SX-OD1 | One repository |
| **Reader** | Collaborators, institutions, the public | Researchers, engineers evaluating the work | Contributors, reviewers, reproducers |
| **Purpose** | State identity, mission, and direction | Explain what a programme is, what exists, and how it is progressing | Document exactly what the code and data do |
| **Tone** | Ambitious but restrained | Precise, structured | Exact, procedural |
| **May claim** | Mission, direction, working approach | Capabilities that exist, with their boundary | Only what the repository's tests and runs show |
| **Must not claim** | Any capability not yet demonstrated | Capabilities of another programme | Results without population, protocol, denominator, and limitation |

**Rules of containment**

- Company text describes direction, not performance. It does not quote metrics.
- Programme text may quote a metric only with its qualification beside it.
- Repository text is the source of truth. Company and programme text must never state more than the repository documents.
- SATSentinel-X and SX-OD1 are never interchangeable. Do not imply that the proposed spacecraft is integrated with the platform.

---

## 3. Voice

The brand is precise, sophisticated, restrained, ambitious, reliable, disciplined, long-term, and scientifically credible. It is confident because it is exact.

**Write like this**

- State the fact, then its boundary.
- Prefer short paragraphs and concrete nouns.
- Use plain verbs: *build, measure, test, verify, escalate*.
- Admit what is unproven, in the same place as the claim.
- Use British English: *organisation, recognise, licence (noun), behaviour*.
- Use sentence case for headings.

**Do not write like this**

- Superlatives and hype: *revolutionary, cutting-edge, game-changing, world-class*.
- Motivational slogans and generic startup language.
- Exclamation marks, rhetorical questions in body text, and emoji.
- Upper case for emphasis. Reserve it for status labels in code spans.
- Vague authority: *industry-leading, trusted, proven*.

| Instead of | Write |
|:--|:--|
| "Our revolutionary AI autonomously repairs satellites." | "We are developing toward autonomous fault management. Today, a synthetic policy demonstrator exists." |
| "State-of-the-art accuracy." | "The detector flagged 30 of 30 evaluated events; it also flagged 40 of 170 control periods." |

---

## 4. Terminology

Three phrases describe three different levels of ambition. Never conflate them.

| Phrase | Describes | Use for |
|:--|:--|:--|
| **autonomous spacecraft** | The company mission | Company-level text only |
| **AI-assisted spacecraft telemetry intelligence** | What SATSentinel-X is today | Programme-level description of current work |
| **autonomous fault management** | The long-term technical objective | Direction, always marked as an objective |

### Status vocabulary

Use these labels, in code spans, and nothing else.

| Label | Meaning |
|:--|:--|
| `IN DEVELOPMENT` | Work exists and is progressing. |
| `INTEGRATION` | Components exist and are being joined or connected to hardware. |
| `PLANNED` | Intended. No implementation exists. |
| `RESEARCH DIRECTION` | An open question being explored, not a commitment. |
| `LONG-TERM OBJECTIVE` | A goal that depends on earlier stages succeeding. |

### Validation vocabulary

State the highest level actually reached, and no higher.

| Term | Meaning |
|:--|:--|
| Simulated | Run against a model the team wrote. |
| Synthetic | Run against constructed data. |
| Recorded | Run against real data captured elsewhere. |
| Bench-tested | Run on physical hardware on the ground. |
| Hardware-in-the-loop | Run with flight-like hardware in a closed loop. |
| Flight-proven | Operated successfully in space. *Not currently applicable to any Vanthion system.* |

Call simulation outputs *simulation and development artifacts*. Do not call them a digital twin or real telemetry.

---

## 5. Claims policy

### Never publish, unless independently verified and approved

- "India's first autonomous CubeSat" or "India's first fully autonomous satellite"
- Flight-proven, space-qualified, launch-ready
- Industry-leading accuracy, revolutionary breakthrough
- Trusted by leading aerospace companies
- Backed by, or an official partner of, any space agency
- Government-funded
- Successfully operating in orbit
- Any customer, partner, investor, or institutional logo or endorsement
- Any launch date, launch provider, funding, mission approval, regulatory authorisation, or flight heritage
- Any claim about a mission specification (form factor, payload, orbit) that is not in an approved document

### Prefer

- "Developing toward autonomous spacecraft."
- "Building the foundations for onboard fault management."
- "Exploring intelligent telemetry interpretation."
- "Progressing from simulation toward integrated hardware validation."
- "Working toward a potential orbital technology demonstration."

### The evidence rule

Every quantitative result states, in the same place:

1. **Population.** What data it was measured on.
2. **Protocol.** How it was measured.
3. **Denominator.** *n* of *N*, never a bare percentage.
4. **Limitation.** What the result does not show.

Never publish: 100% accuracy, a low or confirmed false-alarm rate without nominal controls, broad generalisation, operational or flight validation, or a comparison that the evidence does not support. Report negative results as plainly as positive ones.

### Review

A claim enters public text only when a reviewer can follow it to a file, test, or run in a repository. If it cannot be followed, remove it or mark it as intended.

---

## 6. Markdown conventions

GitHub sanitises styling. Rely on structure, not decoration.

**Structure**

- One `#` heading per document. Do not skip levels.
- Short paragraphs: three sentences or fewer.
- Use `---` to separate major sections only.
- Lead with the point; put detail after it.

**Tables**

- Prefer two or three columns so tables read on a phone.
- Left-align text columns: `|:--|`.
- Keep cells to a sentence or two.
- Every table has a header row.

**Code**

- Always specify a fence language. Use `text` for output and diagrams.
- Commands must be copy-pasteable and must have been run.

**Allowed HTML** (GitHub-safe): `<p align="center">`, `<h1 align="center">`, `<img>` with `width` and `alt`, `<br>`, `<sub>`, `<em>`, and HTML comments. Do not use CSS, `<style>`, `<script>`, or `<iframe>`.

**Do not use:** emoji, badge collections, visitor counters, contribution animations, third-party statistics widgets, or decorative dividers.

**Images:** every image has meaningful `alt` text. Banners are 1800 × 600 pixels and keep their key content within the central 90 percent.

**Diagrams:** prefer a table or a text outline. Use Mermaid only after it has been rendered and checked on GitHub.

---

## 7. Link style

- Link text describes the destination. Never use "click here" or a bare URL in prose.
- Link only to resources that have been opened and confirmed.
- Use relative links for files inside the same repository.
- Use absolute links across repositories.
- When citing evidence, link to a commit-pinned path so the reference does not drift.
- State ownership accurately. A repository under a personal account is not described as an organisation repository.
- Do not link to a page that does not exist yet.

---

## 8. Repository naming and metadata

### Names

- New repositories use lower-case words separated by hyphens.
- Programme repositories begin with the programme: `satsentinel-x-<component>`, `sx-od1-<subsystem>`.
- Names describe function, not hype: `satsentinel-x-telemetry-simulator`, not `satsentinel-x-ultra`.
- Existing repositories keep their names unless a rename is deliberately planned. GitHub redirects old URLs, but external references and citations may still break.

### Required metadata for every repository

| Field | Rule |
|:--|:--|
| Description | One sentence, no superlatives, states what it is. |
| Topics | Three to eight, lower-case, factual. |
| Licence | A `LICENSE` file, or an explicit "all rights reserved" statement in the README. A licence badge without a file is not acceptable. |
| README | Built from [`templates/REPOSITORY_README_TEMPLATE.md`](templates/REPOSITORY_README_TEMPLATE.md). |
| Committed artefacts | No `node_modules`, credentials, or large generated outputs. Document how to regenerate them. |

---

## 9. Visual rules

The identity is strictly monochrome: black, white, and restrained neutral grey.

### Palette

| Name | Hex | Use |
|:--|:--|:--|
| Black | `#000000` | Banner and logo background |
| Graphite | `#3A3A3A` | Hairline dividers |
| Grey | `#8C8C8C` | Secondary text on black |
| Off-white | `#F5F5F5` | Primary text on black |
| White | `#FFFFFF` | Logo artwork |

### Typography

Banners use Inter (SIL Open Font Licence), Light weight for headlines and Regular for secondary text. In Markdown, GitHub's default type applies. Do not attempt to set fonts.

### Prohibited

Colour, colourful gradients, emoji, generic AI brain or circuit graphics, badge collections, visitor counters, fake metrics, partner or customer logos, and stock imagery. The tonal shading inside the official logo artwork is part of the logo and is not to be reproduced elsewhere.

### Composition

Generous whitespace, strong hierarchy, one idea per section. A page should read as editorial and technical, not promotional.

---

## 10. Pre-publication checklist

Before any public page or repository README is published:

- [ ] Every claim can be traced to a file, test, or run.
- [ ] No prohibited claim from section 5 appears.
- [ ] Status labels are from section 4 and match the evidence.
- [ ] Each result has population, protocol, denominator, and limitation.
- [ ] SATSentinel-X, SX-OD1, and the company are not conflated.
- [ ] Every link has been opened and every relative path resolves.
- [ ] Heading levels do not skip.
- [ ] No emoji, badges, counters, or colour.
- [ ] British English, sentence-case headings.
- [ ] Readable at phone width, with no sideways scrolling in body text.
- [ ] Reviewed three ways:
  - an experienced spacecraft engineer would find the claims suitably qualified;
  - a prospective collaborator can say what is being built and where they could help;
  - the page looks deliberate and restrained.

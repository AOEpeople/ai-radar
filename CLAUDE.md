# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

Content repository for the **AOE AI Technology Radar** (published at https://ai-radar.aoe.com/). The radar covers development of professional AI Agents, RAG systems, and LLMOps. There is no application code here — the rendering engine is the npm dependency `aoe_technology_radar` (github:AOEpeople/aoe_technology_radar#v5). This repo contains only radar articles (markdown), configuration, and assets. The audience is AI engineers, developers, and data scientists.

## Commands

```bash
npm i               # install
npm run serve       # build + serve locally → http://localhost:3000/techradar
npm run dev         # dev mode
npm run build       # static build into build/
```

There are no tests or linters. CI (GitHub Actions `.github/workflows/main.yml`, GitLab CI mirror in `.gitlab-ci.yml`) runs `npm run build` and **fails if the workspace is dirty after the build** — generated files that the build touches must be committed. Deployment to Pages happens automatically on push to `main`.

## Structure

- `radar/<date>/*.md` — radar articles ("blips"), one file per item. **Do not create a new date folder on your own; always add to the latest existing folder** (currently `radar/2026-07-17/`). A new date folder is only created when a new radar release is explicitly prepared. The filename becomes the item's URL id.
- `config.json` — radar configuration: segments, rings, colors, labels. The allowed segment and ring ids are defined here.
- `about.md` — the radar's "How to use" page, including RAG/agent basics.
- `public/images/` — images for articles, referenced in markdown as `/images/<name>.png`.
- `custom.css` — small style overrides.

## Writing radar articles

Every article starts with this frontmatter:

```yaml
---
title: "The Title"
ring: assess
segment: frameworks
tags: [evaluation, security]
---
```

- **ring** — one of: `adopt`, `trial`, `assess`, `hold`
- **segment** — one of: `architecture-pattern`, `frameworks`, `models-platforms`, `evaluation`, `data-features`, `tools`
- **tags** — use established tags only (see Readme.md): UI, automation, chat, extraction, benchmarking, evaluation, knowledge, patterns, platform, prompting, protocol, retrieval, security, workflow, sovereignty, observability, vector-db, model-serving

### Updating an existing article in a new release

The frontend shows an article's **history**: the old entry and the new entry after it. An update file (same filename, new release folder) must therefore **not repeat the article** — it contains only the frontmatter (with the possibly changed ring), what changed, and a short justification for the update/ring move. Start the body with something like `**Update 07/2026 (trial → adopt):** …`.

### Style rules (from .cursor/rules/radar.md)

- Be precise and concise; add mentionable insights and recommendations. No marketing language, no superlatives.
- Link to related radar articles with the path `/<segment>/<filename-without-.md>/`, e.g. `ragas.md` in segment `evaluation` → `/evaluation/ragas/`.
- Add links to official pages and relevant internet resources.
- Existing articles typically use sections like "Key Features", "Use Cases", "Team Insights", "Recommendation", "Related Topics" — follow that pattern for consistency, especially the honest first-hand "Team Insights" and a concrete "Recommendation".

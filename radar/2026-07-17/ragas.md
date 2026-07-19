---
title: "Ragas"
ring: hold
segment: evaluation
tags: [evaluation]
---

**Update 07/2026 (trial → hold):** We moved Ragas to hold. Our documented team experience (documentation gaps, setup complexity, breaking upgrades, intransparent evaluations) has not improved, and the pattern repeated over the past year - we do not recommend starting new projects with Ragas.

What changed since our last assessment:

- The project moved to a new organization: [vibrantlabsai/ragas](https://github.com/vibrantlabsai/ragas) (previously explodinggradients).
- **v0.4** (December 2025) reworked the API - and again introduced breaking changes for existing setups (e.g. import breakage with langchain-community in 0.4.3).
- Functionally Ragas has fallen behind alternatives, while remaining a useful conceptual reference for RAG metrics and testset generation.

Existing Ragas integrations can keep running, but for new evaluation setups we recommend [Deepeval](/evaluation/deepeval/).

---
title: "Open Knowledge Format (OKF)"
ring: assess
segment: architecture-pattern
tags: [knowledge, protocol]
---

The Open Knowledge Format (OKF) is an open specification (Google Cloud, v0.1, June 2026) for representing knowledge as a directory of **Markdown files with YAML frontmatter** (the only required field is `type`) - Git-friendly, vendor-neutral, explicitly "a format, not a platform". It formalizes the "LLM wiki" pattern for sharing curated knowledge and context between AI systems, adjacent to the AGENTS.md / llms.txt ecosystem.

- Reference implementations exist; first adopter is Google Cloud's Knowledge Catalog.
- Very early (v0.1, one month old, Google-driven) - broad adoption not yet demonstrated. Worth watching because a neutral, plain-text interchange format fits the [Context Engineering](/architecture-pattern/context-engineering/) direction.
- Not to be confused with the Open Knowledge Foundation (unrelated).

## Resources

- [OKF specification](https://github.com/GoogleCloudPlatform/knowledge-catalog/tree/main/okf)
- [Announcement](https://cloud.google.com/blog/products/data-analytics/how-the-open-knowledge-format-can-improve-data-sharing/)

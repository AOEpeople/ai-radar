---
title: "chroma db"
ring: adopt
segment: data-features
tags: [retrieval]
---

**Update 07/2026:** Chroma has outgrown the "prototyping only" positioning of our previous entry:

- **Rust rewrite** (1.x series): significantly better performance, and dense/sparse vector search, full-text, regex and metadata filters are now combined in one query API - hybrid search without a second system.
- **Chroma Cloud** is generally available: managed, serverless, usage-based pricing.

Our recommendation update: the single-node OSS variant remains the pragmatic choice for prototypes and small-to-medium applications; with Chroma Cloud, staying on Chroma for production is now a valid path. For large self-hosted setups, [Qdrant](/data-features/qdrant/) or [Weaviate](/data-features/weaviate/) remain the more proven options.

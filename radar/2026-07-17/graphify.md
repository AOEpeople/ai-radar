---
title: "Graphify"
ring: assess
segment: tools
tags: [harness, retrieval]
---

Graphify (MIT) builds a traversable **knowledge graph of a codebase** as a skill for coding agents (Claude Code, Cursor, Codex, Gemini CLI via `/graphify`). It parses code deterministically via tree-sitter AST (locally, no LLM); docs/PDFs optionally via an LLM. Every edge is marked `EXTRACTED` or `INFERRED` for traceability, and hooks steer the agent to the graph before grep/read calls.

- Not classic Graph-RAG: codebase-centric, deterministic (AST instead of LLM extraction), no embeddings, packaged as an assistant skill rather than a retrieval pipeline. Distinct from Neo4j (generic graph DB), Graphiti (agent memory graph) and LightRAG/GraphRAG (embedding-based).
- Young and 0.x (YC S26, rapid growth); verify the benefit over native agent search on your own large codebases. OSS core with an "Enterprise" always-on variant.

## Resources

- [GitHub Repository](https://github.com/Graphify-Labs/graphify)
- [Website](https://graphify.net/)

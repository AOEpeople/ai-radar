---
title: "Headroom"
ring: assess
segment: tools
tags: [workflow]
---

Headroom (Apache 2.0) is a token-compression layer for LLM inputs: it compresses tool outputs, logs, files and RAG chunks before they enter the context window - the "compress" building block of [Context Engineering](/architecture-pattern/context-engineering/). Compression is reversible (originals stay retrievable), and specialized compressors target JSON, code and prose.

- Ships as Python/TypeScript library, a transparent proxy, an MCP server and agent wrappers for Claude Code, Cursor and others - easy to trial without rewriting the pipeline.
- Claims ~20% token reduction for coding agents and 60-95% for JSON at "equal answers" - validate these on your own workloads.
- Young and 0.x: API stability not guaranteed; OSS core is local/free, with a managed cloud as the business model.

## Resources

- [GitHub Repository](https://github.com/headroomlabs-ai/headroom)

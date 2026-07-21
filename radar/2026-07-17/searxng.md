---
title: "SearXNG"
ring: trial
segment: tools
tags: [retrieval, sovereignty]
---

SearXNG is a free, self-hostable metasearch engine (AGPL-3.0) that aggregates and deduplicates results from ~260 upstream engines without tracking or profiling. Beyond its origins as a privacy search frontend, it has become a common **private web-search backend for AI agents and RAG/deep-research pipelines**.

- Clean JSON API plus several active MCP servers make it usable from Claude, Cursor and any MCP client; official LangChain tool, integrations with LlamaIndex, Open WebUI and ready-made stacks (Perplexica, Crawl4AI+SearXNG RAG servers).
- Enables web grounding for agents **without** commercial search APIs (Google/Bing/Tavily) - no query leakage to third parties, no API keys or per-call cost. Attractive for data-sovereign/EU setups.
- Mature and highly active (rolling releases); AGPL requires publishing your own modifications when run as a network service.

## Resources

- [GitHub Repository](https://github.com/searxng/searxng)
- [Documentation](https://docs.searxng.org/)

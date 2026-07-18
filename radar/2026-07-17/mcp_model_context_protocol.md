---
title: "MCP - Model Context Protocol"
ring: adopt
segment: architecture-pattern
tags: [protocol]
---

**Update 07/2026 (trial → adopt):** MCP has become the de-facto standard for connecting LLMs to tools and data. It is supported first-party by Anthropic, OpenAI, Google, Microsoft, GitHub and most agent frameworks and IDEs. For tool integration in agentic systems there is currently no serious alternative.

What changed since our last assessment:

- **Transport:** "HTTP with SSE" was replaced by **Streamable HTTP** (spec release 2025-03-26). New servers should not implement the deprecated SSE transport anymore.
- **Spec evolution:** Active release cadence with active roadmap and features. There is now a formal deprecation policy.
- **Ecosystem:** The [official MCP Registry](https://registry.modelcontextprotocol.io/) lists thousands of servers.
- **Security:** Treat third-party MCP servers as untrusted input - tool descriptions and tool results can carry indirect prompt injections. Restrict which servers are allowed, prefer read-only tools where possible and see [Prompt Injection Awareness](/architecture-pattern/prompt_injection_awareness/). The NSA/CISA guidance on MCP security ([PDF, May 2026](https://media.defense.gov/2026/Jun/02/2003943289/-1/-1/0/CSI_MCP_SECURITY.PDF)) summarizes recommended controls.

Updated links: [Official MCP Specification](https://modelcontextprotocol.io/specification/latest) 
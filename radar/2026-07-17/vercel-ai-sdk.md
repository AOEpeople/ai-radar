---
title: "Vercel AI SDK"
ring: adopt
segment: frameworks
tags: [ui]
---

**Update 07/2026 (trial → adopt):** With [AI SDK 6](https://vercel.com/blog/ai-sdk-6) (December 2025) the SDK grew from a UI/streaming toolkit into a full agent framework:

- `Agent` abstraction (tool loop with configurable stopping conditions)
- Human-in-the-loop tool approval (`needsApproval`)
- Stable [MCP](/architecture-pattern/mcp_model_context_protocol/) support including OAuth
- Reranking support and DevTools for inspecting agent runs

Migration from v5 is largely automated via codemods. In the TypeScript ecosystem the AI SDK has become the default choice for LLM integration in web applications, which is why we moved it to "adopt". 

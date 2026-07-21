---
title: "Context Hub"
ring: trial
segment: architecture-pattern
tags: [patterns, knowledge]
---

A Context Hub is a central, versioned source that supplies agents with the knowledge and conventions they need at runtime - up-to-date API documentation, domain knowledge, project conventions - instead of relying on the model's training cutoff or scattering context across ad-hoc prompts. It is the "provisioning" side of [Context Engineering](/architecture-pattern/context-engineering/): one curated place agents pull from, rather than each team re-solving context per project.

Building blocks seen in practice:

- **Documentation registries** for coding agents that serve current, versioned API docs (e.g. Andrew Ng's Context Hub / `chub`, Context7) - they close the "model doesn't know the latest library version" gap.
- **[MCP](/architecture-pattern/mcp_model_context_protocol/) resources / servers** as the delivery mechanism to any agent.
- **Convention files** (AGENTS.md/CLAUDE.md) and neutral knowledge formats such as [OKF](/architecture-pattern/open_knowledge_format/) as the storage layer.

Treat the hub as versioned, reviewed content - it is shared context that also becomes an [attack surface](/architecture-pattern/prompt_injection_awareness/) if it can be poisoned.

---
title: "Agent-to-Agent Protocol (A2A)"
ring: assess
segment: architecture-pattern
tags: [ protocol]
---

**Agent-to-Agent (A2A)** is an open, HTTP-based protocol that enables AI agents—built on different frameworks to coordinate tasks, exchange information, and collaborate. Backed by companies like Google, Salesforce, and LangChain, A2A standardizes inter-agent communication and discovery, preparing the way for modular, scalable multi-agent systems. This protocol is especially suitable when agents must operate independently but collaborate via clearly defined interfaces.

While MCP standardizes LLM-to-environment interaction, A2A focuses on agent-to-agent coordination. These protocols are complementary: MCP enables agents to reason with tools and context, while A2A enables those agents to talk to each other.

## Key Concepts

- A2A introduces three core actors: **User** (initiates requests), **A2A Client** (that makes requests on the user's behalf) and **A2A Server** (remote agent that fulfills requests and returns results)
- **AgentCard**: JSON descriptor of an agent’s identity, capabilities, skills, endpoint, and auth requirements.
- **Discovery**: Agents can be found via `.well-known` URLs, registries, or static configuration.
- **Communication**: JSON-RPC over HTTP(S) using tasks and artifacts. Supports:
  - Synchronous (`sendTask`)
  - Asynchronous polling
  - Streaming (SSE)
  - Push (webhooks)
- **Security**: AgentCard-defined auth schemes (API keys, OAuth2)

## Resources
- [Google A2A GitHub Repository](https://github.com/google-a2a/A2A)

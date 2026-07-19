---
title: "Multi-Agent System"
ring: trial
segment: architecture-pattern
tags: []
---

**Update 07/2026:** Our core recommendation has proven itself: maximize the single agent first - practice reports show coordination overhead can multiply cost without improving accuracy when tasks don't decompose cleanly.

What changed:

- The **supervisor/subagent pattern** has established itself as the production default: a lead agent delegates self-contained subtasks to subagents with isolated contexts and merges condensed results (also a context-management technique, see [Context Engineering](/architecture-pattern/context-engineering/)).
- The framework list from our previous entry is outdated: **AutoGen was absorbed into the Microsoft Agent Framework**, and `llama-agents` was discontinued in its described form. Current options: [LangGraph](/frameworks/langgraph/), [CrewAI](/frameworks/crew-ai/), Microsoft Agent Framework, plus the provider SDKs (OpenAI Agents SDK, Claude Agent SDK, Google ADK) - the latter are a pragmatic choice when already committed to one provider.
- For securing multi-agent setups see the [OWASP Agentic Top 10](/architecture-pattern/owasp_llm_top_10/) (inter-agent communication, cascading failures).

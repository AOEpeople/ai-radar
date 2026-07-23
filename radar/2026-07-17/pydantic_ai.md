---
title: "Pydantic AI"
ring: trial
segment: frameworks
tags: [framework]
---

Pydantic AI is the agent framework of the Pydantic team: agents are typed Python objects, tool signatures and structured outputs are validated by Pydantic - type-safe and well testable, with a leaner surface than the LangChain ecosystem.

- **V2 stable since June 2026**: "capabilities" as the core primitive - a composable unit bundling an agent's tools, hooks, instructions and model settings ([announcement](https://pydantic.dev/articles/pydantic-ai-v2)).
- The built-in harness ships memory systems, guardrails, context management and **CodeMode** (the model writes Python that orchestrates tools in one execution instead of many individual tool calls).
- Model-agnostic; natural fit for teams already using Pydantic in their stack.

## Resources

- [Documentation](https://ai.pydantic.dev/)
- [GitHub Repository](https://github.com/pydantic/pydantic-ai)

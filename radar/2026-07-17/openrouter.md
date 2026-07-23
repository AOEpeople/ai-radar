---
title: "OpenRouter"
ring: trial
segment: models-platforms
tags: [platform, model-serving]
---

OpenRouter is one of the most used model aggregator: one OpenAI-compatible API and one API key for hundreds of models across all major providers, with pay-per-use pricing, automatic fallbacks and provider routing. Useful for model evaluation, fast switching between frontier models and avoiding per-provider onboarding; its public usage rankings double as a practical adoption signal.

- **BYOK** (bring your own provider keys) is supported: 1M requests/month free, then a 5% fee on the equivalent platform cost.
- **Data residency needs attention**: standard usage may process data in the US; **EU in-region routing** (`eu.openrouter.ai`, hard-locked EU processing) is an enterprise-only feature since June 2026 and covers a subset of models.
- It is a SaaS marketplace, not gateway software - for self-hosted governance (budgets, keys, audit) see [LiteLLM](/tools/litellm/).

## Resources

- [Website](https://openrouter.ai/)
- [Documentation](https://openrouter.ai/docs)

---
title: "LiteLLM"
ring: trial
segment: tools
tags: [platform]
---

LiteLLM is the de-facto standard among self-hosted **LLM gateways**: a proxy that exposes one OpenAI-compatible API over 100+ providers, with virtual keys, budgets and rate limits per team, cost tracking, load balancing/fallbacks, caching, guardrail hooks (e.g. [Presidio](/evaluation/presidio/) for PII masking) and observability integrations ([Langfuse](/evaluation/langfuse/), OTel).

- **Open-core**: MIT core; SSO, RBAC, audit logs and enforcement features require a commercial license.
- Self-hosting via Docker/Helm; production scale needs Postgres + Redis.
- **Security track record 2026 demands operational discipline**: compromised PyPI releases (March 2026, credential stealer) and a reported vulnerability chain allowing privilege escalation on the gateway (June 2026). Pin versions, patch promptly and never expose the gateway publicly. Long-standing criticism of code quality and breaking changes between minor versions persists.

Kong AI Gateway (for existing Kong users), [OpenRouter](/models-platforms/openrouter/) (SaaS model marketplace, no self-hosted governance layer).

## Resources

- [GitHub Repository](https://github.com/BerriAI/litellm)
- [Documentation](https://docs.litellm.ai/)

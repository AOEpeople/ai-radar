---
title: "Sensitive Data Scanning"
ring: trial
segment: architecture-pattern
tags: [security]
---

**Update 07/2026:** The practice has become more concrete - two patterns established themselves:

- **PII guardrail as gateway**: a proxy between application and LLM that detects and masks PII in prompts and responses centrally (e.g. LiteLLM proxy with a PII-masking guardrail), instead of per-application filtering. This also covers agentic data flows that are hard to audit application-side.
- **Microsoft Presidio** has become the de-facto open-source standard for PII detection and de-identification (analyzer + anonymizer, extensible recognizers) and integrates with the common gateway/guardrail stacks.

Note the division of labor: [Gitleaks](/evaluation/gitleaks/) covers secrets/credentials in code - PII in prompts, documents and logs needs the patterns above. (The gitleaks links in our previous entry pointed to a wrong path.)

Resources: [Presidio](https://microsoft.github.io/presidio/), [LiteLLM PII masking guardrails](https://docs.litellm.ai/docs/proxy/guardrails/pii_masking_v2)

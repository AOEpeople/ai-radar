---
title: "Sensitive Data Scanning"
ring: trial
segment: architecture-pattern
tags: [security]
---

**Update 07/2026:** The practice has become more concrete - two patterns established themselves:

- **PII guardrail as gateway**: a proxy between application and LLM that detects and masks PII in prompts and responses centrally (e.g. a [LiteLLM](/tools/litellm/) proxy with a PII-masking guardrail), instead of per-application filtering. This also covers agentic data flows that are hard to audit application-side.
- **[Presidio](/evaluation/presidio/)** has become the de-facto open-source standard for PII detection and de-identification (analyzer + anonymizer, extensible recognizers) and integrates with the common gateway/guardrail stacks - including reversible pseudonymization setups, see the Presidio entry.

---
title: "Presidio"
ring: trial
segment: evaluation
tags: [security]
---

Presidio (MIT) is the de-facto open-source standard for PII detection and de-identification: analyzer (regex/checksum recognizers plus NER via spaCy/Transformers/GLiNER), anonymizer with configurable operators, image redaction and structured-data support. In LLM pipelines it is the established building block for PII guardrails - including a native integration as [LiteLLM](/tools/litellm/) guardrail hook.

- **Governance change 2026**: Presidio moved from Microsoft to the community-run "Data Privacy Stack" organization (Microsoft remains on the steering committee); license and APIs unchanged.
- **German PII recognizers** landed in mid-2026 (tax ID, ID card, social security, health insurance and more, with checksum validation - disabled by default).
- Know the limits: structured identifiers are detected reliably, free-text names/addresses depend on the NER model and language configuration.

## Reversible pseudonymization

Presidio replaces PII with placeholders, but has no built-in way to map them back to the original values after the LLM response. For the replace-before-LLM-call / re-identify-after pattern, the most complete ready-made implementation is **[LLM-Guard](https://protectai.github.io/llm-guard/)** - a separate open-source toolkit (Protect AI, MIT) that uses Presidio internally for detection and adds a vault (stores the placeholder-to-original mapping) plus a deanonymize output scanner. Note from 2026 research: LLMs can partially re-identify pseudonymized text from context clues - pseudonymization reduces risk, it does not eliminate it. See [Sensitive Data Scanning](/architecture-pattern/sensitive_data_scanning/) for the surrounding pattern.

## Resources

- [Documentation](https://presidio.dataprivacystack.org/)
- [GitHub Repository](https://github.com/data-privacy-stack/presidio)

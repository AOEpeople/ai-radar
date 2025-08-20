---
title: "Prompt Injection Awareness"
ring: adopt
segment: architecture-pattern
tags: [security, prompting]
---

Prompt injection is a critical security vulnerability where attackers manipulate LLM inputs to bypass security controls, leak data, or alter model behavior. It ranks as #1 in the [OWASP LLM Top 10](/architecture-pattern/owasp_llm_top_10/).

## Attack Types

- **Direct Injection**: Malicious prompts overriding system instructions
- **Indirect Injection**: Attacks through contaminated data sources
- **Context Manipulation**: Exploiting model's context handling
- **Chain Attacks**: Multi-step manipulation sequences

## Key Risks

- System prompt exposure
- Sensitive data leakage
- Security control bypass
- Unauthorized actions
- Output manipulation

## Mitigations

- Input validation and sanitization
- Guardrails
- Output filtering and monitoring
- Permission boundaries
- Regular security testing with [Garak](/evaluation/garak/)
- Comprehensive logging

## Resources

- [OWASP LLM Top 10](/architecture-pattern/owasp_llm_top_10/)
- [Prompt Injection Papers & Guides](https://github.com/FonduAI/awesome-prompt-injection)
- [Gandalf Challenge](https://gandalf.lakera.ai/)

## Related Topics

- [Prompt Engineering](/architecture-pattern/prompt_engineering/)

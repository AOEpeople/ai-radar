---
title: "Gitleaks"
ring: adopt
segment: data-features
tags: [security]
---

[Gitleaks](https://github.com/gitleaks/gitleaks) is a SAST tool for detecting hardcoded secrets in Git repositories. It integrates cleanly into development workflows via pre-commit hooks and CI/CD pipelines. Rules are defined using TOML files, allowing flexible regular expression patterns and contextual matching — including organization-specific configurations.

**Recommendation**: Embed Gitleaks into CI pipelines for any codebase involving LLMs or external APIs. Maintain custom rules and update detection patterns regularly to minimize false positives and blind spots.

## Related Topics

- [OWASP LLM Top 10](/architecture-pattern/owasp_llm_top_10/)

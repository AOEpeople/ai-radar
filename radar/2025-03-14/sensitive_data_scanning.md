---
title: "Sensitive Data Scanning"
ring: trial
segment: architecture-pattern
tags: [security]
---

Sensitive Data Scanning is a critical security practice for AI applications, focusing on identifying, protecting, and managing sensitive information throughout the AI development and deployment lifecycle. This technique is essential for maintaining privacy, compliance, and security in AI systems, and aligns with the [OWASP LLM Top 10](/architecture-pattern/owasp_llm_top_10/) security guidelines.

## Key Concepts

### Detection Capabilities

The system should be able to detect various types of sensitive data: Personally Identifiable Information (PII), financial records, healthcare information, sensitive business data, credentials or API keys.
Check tools like [Gitleaks](/security/gitleaks/).


### Protection Mechanisms

Once sensitive data is identified, multiple protection mechanisms are possible. This includes data hiding, data masking or encryption. 

### Access Control

Limit access to sensitive data based on the principle of least privilege. If data access depends on permissions, a granular access control system can manage data visibility.

## Use Cases

Sensitive data scanning plays a crucial role in several key areas of AI development:
- During training and data preparation
- For model output validation, it verifies that no protected information is inadvertently exposed. 
- Document processing workflows - e.g. when preparing document content for RAG
- During logging to ensure data privacy

## See also

- [Gitleaks](/security/gitleaks/) for comprehensive code scanning
- [OWASP LLM Top 10](/architecture-pattern/owasp_llm_top_10/) for security guidelines
- [Garak](/evaluation/garak/) for LLM security testing
- SIEM platforms for security monitoring


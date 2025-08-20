---
title: "Model Discovery & Selection"
ring: adopt
segment: models-platforms
tags: [benchmarking]
---

Model discovery refers to the systematic search and selection of the most suitable machine learning and AI models for a specific use case. The focus is not just on finding models, but on targeted evaluation and comparison across multiple dimensions.

Since models and their capabilities are constantly evolving, model discovery is a continuous task. A test-driven approach and an applications architecture that ensures model interchangeability (e.g., via standardized interfaces and model cards) are important.

## Recommended selection steps:

- Start with your use-case (thinking about what is important to optimize for)
- Choose a model before choosing an API provider
- Choose an API Provider (throughput, latency, cost, security, limits, etc.)

## Evaluation criterias:

- Does the use case really require a LLM or can a smaller model or "traditional" machine learning be used?
- Check the best model for your defined use-case. Use benchmarks and [leaderboards](/models-platforms/model_leaderboards/) as a starting point for model selection.
- Consider your requirements for speed and latency (for example reasoning models are normally slower)
- Consider your cost requirements (e.g., inference cost, licensing)
- Consider your compliance and governance requirements (e.g., data privacy, licensing)
- Consider the available Model serving platforms and providers.

## Organisational recommendations

- Maintain a list or registry of models evaluated in your organisation for certain use-cases.
- Use some kind of model cards (e.g. [Model Cards Paper](https://arxiv.org/abs/1810.03993)) to document model details and characteristics.
- Document evaluation criteria
- Consider both open and commercial options
- Plan for model updates
- Implement monitoring

## Tools & Platforms

- [Hugging Face](/models-platforms/huggingface/): Leading model hub and evaluation platform
- [Model Leaderboards](/models-platforms/model_leaderboards/): Performance benchmarks

## Related Topics

- [OWASP LLM Top 10](/architecture-pattern/owasp_llm_top_10/)
- [Prompt Engineering](/architecture-pattern/prompt_engineering/)

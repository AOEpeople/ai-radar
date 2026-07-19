---
title: "Microsoft Foundry"
ring: adopt
segment: models-platforms
tags: [platform, model-serving]
---

Microsoft Foundry (formerly Azure AI Foundry) is Microsoft's unified platform for building AI applications and agents on Azure. It replaces the standalone "Azure OpenAI Service" branding - OpenAI models are now consumed as "Azure OpenAI in Microsoft Foundry Models".

## Key Features

- **Model catalog**: OpenAI frontier models (currently GPT-5.1 with adaptive reasoning, GPT-5.5 with 1M token context) plus open-weight and third-party models (Meta, Mistral, DeepSeek, xAI and others) behind one API.
- **Agent tooling**: Foundry Agent Service for hosting agents, with built-in evaluations, guardrails/content safety and observability.
- **Enterprise integration**: Entra ID, private networking, regional data residency and compliance certifications - the same reasons Azure OpenAI was our enterprise default.

## Recommendation

For teams already in the Microsoft/Azure ecosystem, Foundry is the default way to consume OpenAI models with enterprise requirements. Note that Azure retires models on fixed schedules (e.g. the GPT-4.1 family on 2026-10-14) - plan model upgrades as recurring maintenance, pin API versions and test before switching defaults ([retirement schedule](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/model-retirement-schedule)).

Alternatives: [AWS Bedrock](/models-platforms/aws-bedrock/) for multi-model access in the AWS ecosystem, [Hugging Face](/models-platforms/huggingface/) or [Replicate.ai](/models-platforms/replicate/) for lower onboarding hurdles.

## Resources

- [Microsoft Foundry Documentation](https://learn.microsoft.com/en-us/azure/foundry/)
- [Azure OpenAI in Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/openai/)

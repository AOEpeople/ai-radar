---
title: "Model News H1 2026"
ring: adopt
segment: models-platforms
tags: [knowledge]
---

The most relevant foundation-model releases of the first half of 2026.

## Trends - what moved

- **Extreme release cadence, smaller jumps.** OpenAI went GPT-5.2→5.5 and Anthropic Opus 4.6→4.8 plus Sonnet 5 within six months, with fast deprecation of old versions. For engineering teams this shifts the effort from "which model" to model pinning, regression evals and planned migration paths (see [Model Discovery & Selection](/models-platforms/model_discovery/)).
- **From chatbot to agent teams.** Agent Teams (Opus 4.6), Dynamic Workflows (Opus 4.8) and software-operation capabilities (GPT-5.5) shift the focus to orchestrated knowledge work. 1M-token context became standard across vendors through more efficient attention mechanisms.
- **Open weights reached the frontier - and roles reversed.** DeepSeek V4, Qwen 3.5 and Mistral Medium 3.5 deliver near-frontier quality at fractional cost (DeepSeek V4: ~80% SWE-bench Verified as MIT open weights). Meanwhile Meta of all companies pivoted to closed source with Muse Spark and pushed Llama 5 to 2027.
- **The mid-tier got frontier-grade.** Sonnet 5 and Gemini 3.5 Flash deliver near-Opus/near-Pro performance at workhorse prices - for most agent workloads the mid-tier is now the rational default.

## Releases by player

- **Anthropic**: Claude Opus 4.6 (Feb, 1M context beta, Agent Teams), Sonnet 4.6 (Feb), Opus 4.7 (Apr), Opus 4.8 (May, Dynamic Workflows), Sonnet 5 (Jun) 
- **OpenAI**: GPT-5.4 (Mar, consolidated frontier lineup), GPT-5.5 (Apr, agentic work across documents/spreadsheets/software, 1M context) 
- **Google**: Gemini 3.1 Pro (Feb, ~doubled reasoning, unchanged pricing), Gemini 3.5 Flash (May, beats 3.1 Pro on coding/agents at 4x speed); Gemini 3.5 Pro still pending as of July - [blog.google](https://blog.google/products/gemini/)
- **Meta**: Muse Spark (Apr) - first proprietary, API-only frontier model; strategic departure from the open-weight Llama course


## Notable open-weight releases

- **DeepSeek V4 Preview** (DeepSeek, China) - V4-Pro (1.6T/49B active) and V4-Flash, MIT license, 1M context, ~80% SWE-bench Verified at a fraction of frontier prices; final release mid-July 2026
- **Qwen 3.5** (Alibaba, China) - 397B-A17B, natively multimodal, 201 languages; Medium/Small series followed
- **Mistral Small 4 / Medium 3.5** (Mistral, France) - Small 4: multimodal instruct/reasoning/coding hybrid with 256k context; Medium 3.5: 128B dense, ~78% SWE-bench Verified, self-hostable on 4 GPUs

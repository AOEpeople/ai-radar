---
title: "Model News H2 2026"
ring: adopt
segment: models-platforms
tags: [knowledge]
---

The most relevant foundation-model releases of the second half of 2026. This edition is continuously updated during the half-year (last update: 2026-07-20).

## Trends - what moved

- **Frontier access became a governance question.** Anthropic's Claude 5 launch went through export controls and back: the "Mythos-class" tier above Opus is now split into Fable 5 (generally available, with safety classifiers for dual-use domains) and Mythos 5 (restricted to vetted partners in cyber defense and research). A regulatorily gated capability tier is a first - and likely not the last.
- **Chinese open-weight models scaled into the multi-trillion range.** Kimi K3 (2.8T) and the Qwen3.8-Max preview (2.4T) push trillion-scale MoE with 1M context into the open-weight space; Meituan's LongCat-2.0 was trained entirely without NVIDIA hardware.
- **Competition is shifting from benchmarks to cost per agent task.** Grok 4.5 at $2/$6, DeepSeek's peak/off-peak pricing, introductory pricing everywhere - pricing models are becoming as differentiating as capability.

## Releases by player

- **Anthropic**: Claude Fable 5 / Mythos 5 (globally available Jul 1 after the export-control episode; 1M context, $10/$50 per MTok; Mythos tier restricted to vetted partners) - [announcement](https://www.anthropic.com/news/claude-fable-5-mythos-5)
- **OpenAI**: GPT-5.6 GA (Jul 9) as a three-tier family - Sol ($5/$30), Terra ($2.50/$15), Luna ($1/$6); 1M context, programmatic tool calling and subagents in the API; rolled out across ChatGPT, ChatGPT Work and Codex
- **xAI**: Grok 4.5 (Jul 8) - co-trained with Cursor, coding/agent focus, aggressive $2/$6 pricing
- **Google**: Gemini 3.5 Pro still pending (limited preview only); smaller releases instead (image/video models, Jul 2)
- **Meta**: Muse Spark 1.1 (Jul 9, 1M-context agentic update) plus Muse Image/Video - the Muse line continues to replace Llama frontier releases

## Notable open-weight releases

- **Kimi K3** (Moonshot AI, China) - 2.8T sparse MoE, largest open-weight model to date; 1M context, native vision, new attention architecture
- **DeepSeek V4 final** (DeepSeek, China) - graduation from the April preview announced for mid-July, introducing peak/off-peak API pricing (date not yet confirmed by a primary source)
- **Qwen3.8-Max Preview** (Alibaba, China) - 2.4T multimodal MoE; open weights announced but not yet published
- **LongCat-2.0** (Meituan, China) - 1.6T MoE, trained entirely on Chinese accelerators

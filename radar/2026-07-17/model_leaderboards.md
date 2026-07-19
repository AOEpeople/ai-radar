---
title: "Model Benchmarks & Leaderboards"
ring: adopt
segment: models-platforms
tags: [benchmarking, knowledge]
---

**Update 07/2026:** The benchmark landscape has shifted fundamentally. Classic benchmarks (MMLU, HumanEval, GSM8K) are **saturated** - frontier models score >90% and no longer differentiate. For assessing SOTA models in 2026, look at three things instead: **composite indexes** for the overview, **agentic/long-horizon evals** for differentiation, and **autonomy measurements** for the trend.

## Composite indexes: the SOTA overview

[Artificial Analysis](https://artificialanalysis.ai/) has become the most cited independent reference. Their **Intelligence Index (v4.1)** is a weighted average over 9 evaluations in 4 categories - Agents 34% (GDPval-AA, τ³-Banking), Coding 24% (Terminal-Bench, SciCode), Scientific Reasoning 24% (HLE, GPQA Diamond, CritPt), General 18% (incl. a hallucination-aware knowledge eval). They also publish a Coding Agent Index, an Openness Index for open-weight models, and consistently measured cost/speed/verbosity data.

Know the limits of composite indexes: the weighting is a judgment call, index version changes break time series, and a single number hides domain weaknesses. Use the index for shortlisting, then check the category scores that match your use case.

## Autonomy: METR time horizons

[METR](https://metr.org/time-horizons/) measures the **task-completion time horizon**: how long (in human-expert working time) can a task be such that the model still succeeds with 50% probability. This is the only established metric that expresses progress as *autonomy duration* rather than benchmark percent - directly relevant for judging what agentic workloads a model can carry. The measured horizon currently doubles roughly every ~4 months; estimates beyond ~16h are considered unreliable, and the suite covers mainly coding/research tasks. Raw data is public.

## Coding & agentic evals

- [SWE-bench Verified](https://www.swebench.com/) - real GitHub issues, the de-facto coding standard; increasingly saturated at the top and with known contamination concerns.
- [DeepSWE](https://deepswe.datacurve.ai/) (Datacurve, since May 2026) - contamination-free by design: 113 freshly written long-horizon tasks across 5 languages (average solution ~670 lines across 7 files), behavior-testing verifiers. Methodically convincing and already used by Artificial Analysis, but young and run by a commercial data vendor - watch how it establishes itself.
- [Terminal-Bench](https://www.tbench.ai/) and [OSWorld](https://os-world.github.io/) - agentic terminal/computer use.
- [BFCL V4](https://gorilla.cs.berkeley.edu/leaderboard.html) - function calling with agentic evaluation.
- [GDPval](https://openai.com/index/gdpval/) - economically relevant knowledge work.
- [ARC-AGI-2](https://arcprize.org/) - abstraction/reasoning differentiation at the frontier.

## Still recommended

[LMArena](https://lmarena.ai/leaderboard) (user-preference elo - measures preference, not correctness), [MTEB](https://huggingface.co/spaces/mteb/leaderboard) for embeddings, [Vectara Hallucination Leaderboard](https://www.vectara.com/blog/introducing-the-next-generation-of-vectaras-hallucination-leaderboard) (relaunched May 2026 with a harder dataset). **Removed:** the Hugging Face Open LLM Leaderboard was officially retired in June 2025.

General caution: vendor-reported scores at model launch are marketing until independently reproduced - prefer leaderboards with independent methodology and published raw data.

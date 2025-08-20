---
title: "Model Benchmarks & Leaderboards"
ring: adopt
segment: models-platforms
tags: [benchmarking, knowledge]
---

Model benchmarks and leaderboards are available for various evaluation dimensions relevant to [model choosing and discovery](/models-platforms/model_discovery/).

In this article we will provide an overview of the most relevant benchmarks and leaderboards, as well as a summary of model limitations that one should have in mind.

## Performance & Benchmarks (MMLU etc.):

As large language models (LLMs) and generative AI (GenAI) are rapidly advancing, robust and targeted benchmarks are essential to assess their real-world capabilities, domain-specific expertise, reasoning power, thrustworthiness and environmental impact. The following benchmarks represent a selection of most relevant benchmarks used to evaluate the next generation of AI models.

### Overview Important Benchmarks:

| Category                                | Benchmark(s)                                                                                               | Purpose & Focus Area                                                                                                                                                       |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| General Knowledge & Reasoning           | MMLU-Pro, GPQA, BIG-Bench Hard, AGIEval, [Humanity’s Last Exam](https://agi.safe.ai/)                      | Measures domain-specific and general expertise (law, physics, medicine) at different difficulty.                                                                           |
| Mathematical Reasoning                  | Math (OpenAI), MathVista, FrontierMath                                                                     | Symbolic and numerical reasoning, including chain-of-thought and visual math. Mathematic task solving.                                                                     |
| Instruction Following & Multi-Hop Logic | IFEval, MUSR, [LongBench](https://github.com/THUDM/LongBench)                                              | Evaluates complex instruction following, task planning, and stepwise logic                                                                                                 |
| Data Analytics & Querying               | [BIRD](https://bird-bench.github.io/), DataSciBench, [Spider 2.0](https://spider2-sql.github.io/)          | SQL generation, structured data understanding, table-to-text generation                                                                                                    |
| Coding, Software & Data Science         | LiveCodeBench, DS-1000, CodeContests, MultiPL-E, [DSBench](https://arxiv.org/abs/2409.07703)               | Functional correctness of code generation, Complex algorithmic tasks, data science workflows (e.g. pandas, sklearn), multi-programming language, data science expert tasks |
| Multimodal Reasoning                    | MMMU, MathVista                                                                                            | Text + image reasoning in STEM and professional domains                                                                                                                    |
| Tool Use & Agent Behavior               | ToolBench, WebArena                                                                                        | Real-world agent performance using tools, APIs, browsers                                                                                                                   |
| Specific Tool Benchmarks                | [SpreadSheetBench](https://spreadsheetbench.github.io/),[BrowseComp](https://openai.com/index/browsecomp/) | Benchmarks specific for common tools like Browser, Excel, ..                                                                                                               |
| Safety & Trustworthiness                | TruthfulQA, ToxiGen, HHEM                                                                                  | Hallucination resistance, ethical alignment, toxicity filtering                                                                                                            |
| Efficiency & Environmental Impact       | CO2-Cost                                                                                                   | Energy usage and carbon emissions of training/inference pipelines                                                                                                          |
| Vision Models (LVLMs) & Multimodality   | VLMEvalKit, MMMU, VizWiz                                                                                   | Evaluation of Models that can deal with Image and Text                                                                                                                     |

## Leaderboards

**1.Popular Leaderboards**

- [Chatbot Arena LLM Leaderboard: Community-driven Evaluation for Best LLM and AI chatbots](https://lmarena.ai/?leaderboard)
- [Artificial Analysis Leaderboards](https://artificialanalysis.ai/)
- [Hugging Face List of Leaderboards on the Hub](https://huggingface.co/blog?tag=leaderboard) & [Model Catalogs in Hugging Face](https://huggingface.co/models)
- [Multilingual MMLU](https://huggingface.co/spaces/StarscreamDeceptions/Multilingual-MMLU-Benchmark-Leaderboard)

**2. Open Model Benchmarks:**

- [Hugging Face Open LLM Leaderboard (Open Models)](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard#/)

**3. Multimodal & Vision Model:**

- [OpenVLM Leaderboard of VLMEvalKit Evaluations](https://huggingface.co/spaces/opencompass/open_vlm_leaderboard)
- [MMMU Leaderboard - Understanding and Reasoning Benchmark for Expert AGI](https://mmmu-benchmark.github.io/#leaderboard)
- [TTS (Text to Speech) natural sounding Arena](https://huggingface.co/spaces/Pendrokar/TTS-Spaces-Arena)

**4. Function-Calling:**

- [Berkeley Function-Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html)

**5. Code:**

- [Can AI Code Leaderboard](https://huggingface.co/spaces/mike-ravkine/can-ai-code-results)
- [Vellum LLM Leaderboard for SOTA (State of the art) models](https://www.vellum.ai/llm-leaderboard)

**6. Embedding Models:**

- [Embedding Leaderboard](https://huggingface.co/spaces/mteb/leaderboard)

**7. Safety & Trustworthiness / Censored Models:**

- [LLM Safety Leaderboard](https://huggingface.co/spaces/AI-Secure/llm-trustworthy-leaderboard)
- [UGI Uncensored General Intelligence Leaderboard](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard)

**8. Cost (Model Provider Cost):**

- [LLM API Providers Leaderboard](https://artificialanalysis.ai/leaderboards/providers)

**9. Hardware Performance:**

- [MLPerf Inference Speed on different Hardware](https://mlcommons.org/benchmarks/inference-datacenter/)

**9. Hallucination:**

- [Hallucinations Leaderboard](https://huggingface.co/spaces/vectara/leaderboard)

## Links

- For a broader overview of model discovery, see [Model Discovery](/models-platforms/model_discovery/).

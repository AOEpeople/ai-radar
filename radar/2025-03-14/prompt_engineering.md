---
title: "Prompt Engineering"
ring: adopt
segment: architecture-pattern
tags: [prompting]
---

Prompt engineering is the process where you guide generative artificial intelligence (generative AI) solutions to generate desired outputs.

It is foundational knowledge for anyone working with or developing applications based on large language models (LLMs). The quality and structure of prompts directly influence the output, making systematic prompt design a core competency for AI engineers and data scientists.

## Motivation

> "Language model without system prompt is like a star chef without a recipe request, he can cook great, but if you don't tell him you're eating vegetarian, you might get a steak."

> "An AI model without context is like a lawyer who argues without knowing the case: He can argue, but maybe for the wrong side."

Understanding prompt engineering is essential because LLMs do not possess intrinsic task awareness; their behavior is guided by the instructions and context provided. Effective prompts lead to more reliable, relevant, and safe outputs.

## Systematic Approach: Design, Optimize, Test

Prompt engineering is not a one-off task but a systematic process:

- **Design:** Formulate the initial prompt based on the task requirements.
- **Optimize:** Iteratively refine the prompt to improve performance and clarity.
- **Test:** Evaluate prompt effectiveness using both qualitative review and quantitative metrics (see also the [evaluation quadrant](/evaluation/)).

## Key Prompting Know How

- **open** vs **narrow** prompts: Depending on the objective, a distinction can also be made between more open, general instructions (heuristic prompting) vs. narrow and more clearly described instructions (more rigid). And especially with very clear and narrow instructions, it is also possible to utilize cost-efficient and smaller models.

- **Instruction vs. Inquiry-Based Prompting:**

  - _Instruction-based_ prompts guide the model with explicit tasks (e.g., "Summarize the following text").
  - _Inquiry-based_ prompts elicit information or reasoning (e.g., "What are the main points in this text?").

- **Different Prompting Techniques:**
  - There are many prompting formulas, that help with comprehensive prompt construction. Examples are **TCEPFTM** (Task, Context, Examples, Persona, Format, Tone, Magic) or **RISE** (Role, Input, Steps, Expectation).
  - You can give examples (Zero-shot, One-shot, Few-shot) to guide the model.
  - **Chain of Thought:** Prompts that encourage the model to reason step-by-step ([paper](https://arxiv.org/abs/2201.11903)).
  - **Chain of Density:** Gradually increasing information density in the prompt ([resource](https://arxiv.org/abs/2309.02772)).
  - Techniques evolve and the models are getting better at understanding prompts.

## Model-Specific Prompting

Prompt effectiveness depends on the underlying model. For example, reasoning-optimized models may require different prompt phrasing or structure compared to general-purpose LLMs. Always consult model documentation and experiment with variations.

## Prompt Chaining

For complex workflows, chaining multiple LLM calls (prompt chaining) can yield higher quality or more controllable outputs. This technique is especially useful in multi-step reasoning, data extraction, or when combining outputs from different models.

## Recommendations

- Treat prompt engineering as an iterative, test-driven process.
- Stay updated on new prompting techniques and evaluation tools.
- Document and version-control effective prompts for reproducibility.

## Further Reading:

- [Prompt Engineering Guide](https://www.promptingguide.ai/)
- [Prompting Guides for GPT-4.1 as an example](https://cookbook.openai.com/examples/gpt4-1_prompting_guide)
- [Claude Prompt engineering overview, including tips for "thinking models"](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)

## Related Topics

- [Prompt Injection Prevention](/architecture-pattern/prompt_injection_awareness/)
- [OWASP LLM Top 10](/architecture-pattern/owasp_llm_top_10/)
- [Model Discovery](/models-platforms/model_discovery/)

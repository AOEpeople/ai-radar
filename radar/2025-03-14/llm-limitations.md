---
title: "Know LLM Limitations"
ring: adopt
segment: models-platforms
tags: [benchmarking, security]
---


SOTA (state of the art) LLM and generative models are very powerful and can do amazing things, but it is important to know and consider their current limitations.

## Hallucination:

One of the most known one is _Hallucination_.
Hallucination is the phenomenon of producing misleading, factually incorrect, or entirely fabricated responses. One differenciates two types of hallucination:

- **Factuality hallucinations**: The model generates responses that are factually incorrect or entirely fabricated.
- **Faithfulness hallucination**: when the generated content does not align with the user's instructions or the given context.
  [reference](https://arxiv.org/abs/2311.05232)

Models hallucinate, and you have to deal with that.

## Limitations:

There are also Task where current models are not performing well, such as complex reasoning tasks.
There are for example benchmarks like PlanBench, GAIA, WorkArena++, WebArena or [MathArena](https://matharena.ai/), that show the current limitations of LLMs and where human still outperforms current models.

Apple published a paper on that topic as well:  ["The Illusion of Thinking: Understanding the Strengths and Limitations of Reasoning Models via the Lens of Problem Complexity"](https://machinelearning.apple.com/research/illusion-of-thinking). It was discussed in the AI community a lot.

## Danger of "Average" content and false facts:

 With the use of LLMs, the generation of "average" quality content is just a keystroke away. As a result, the internet is flooded with masses of irrelevant and sometimes incorrect content. [example of well of knowledge poisoning](https://www.linkedin.com/posts/piers-young_watching-the-well-of-knowledge-being-poisoned-activity-7318707672566935554-PvBO), [Github code quality decline](https://www.gitclear.com/coding_on_copilot_data_shows_ais_downward_pressure_on_code_quality).
Also glitches in AI training may result in quality problems. [Example of "vegetative electron microscopy"](https://theconversation.com/a-weird-phrase-is-plaguing-scientific-papers-and-we-traced-it-back-to-a-glitch-in-ai-training-data-254463)

We should not contribute to this unreflected use with "naive" AI applications, but do everything we can to ensure high quality and relevance.

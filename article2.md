---
layout: single
permalink: /article2/
---
<h1>LLMs — Pure Reason Without The Critique, October 2023</h1>
<p style="font-size: 16px;"><b>Motivation.</b><br>
In the world of generative AI, Large Language Models (LLMs) have witnessed remarkable progress [1] that has largely been driven by their use of attention blocks [2]. Attention enables LLMs to adapt their understanding of input information based on contextual cues, facilitating their general reasoning capabilities. Put simply, attention is how LLMs discern different meanings for ‘Apple’ in sentences like ‘Apple has exceptional touchscreen technology’ and ‘Apple pie is my favourite dessert’. Despite their remarkable abilities, LLMs occasionally generate content that ranges from being overly simplistic to outright harmful [3]. The dual nature of LLMs, marked equally by their intelligence and their ignorance, prompts us to question what factors are causing this unpredictability. <br>

<p style="font-size: 16px;">Some researchers argue that the only problem is size and anticipate that scaling up LLMs will invariably lead to more robust intellectual abilities. However, it’s also possible that there are inherent limitations that will persist regardless of their size. In this article, we will explore the idea that LLMs are limited by their inability to critique their own reasoning. But why is self-critique so important? We previously noted that the success of LLMs can be largely attributed to attention, which enables a flexible representation of prompts. However, the way LLMs then process this representation exhibits a degree of rigidity, as it is converted directly into a response without an opportunity for reflection. <br>

<p style="font-size: 16px;">We believe that this inflexibly produces fragile and unpredictable models, as it prevents them from self-correcting or re-exploring a problem with renewed insight. In developing flexible LLMs, models must not only be capable of reasoning but also possess the capacity to vet (Paper 1) and adapt (Paper 2) their thought processes. In this article, we consider two papers from Google-Deepmind that attempt to push LLMs beyond pure reason and incorporate self-critique.

<p style="font-size: 16px;"><b>Paper 1 — “LM vs LM: Detecting Factual Errors via Cross Examination.”</b><br>
The core idea of this paper is that when an LLM makes incorrect claims, they are likely to conflict with other statements the model produces [4]. As such, the authors prompt an ‘examiner LLM’ to interrogate the claims of an ‘examinee LLM’ in order to discover inconsistencies. The examiner repeatedly questions the examinee until it deems that it has sufficient information to determine the factual accuracy of the examinee’s claim. At this point, the examiner is prompted to render a verdict, categorising the claim as either correct or incorrect. Notably, the examiner and examinee LLM could be one and the same, essentially performing self-critique, albeit with distinct prompts that define the respective roles. An example of this interrogation is given below:
<p align="center">
  <img src="/art2_1.webp" alt="Alt Text">
</p>
<p style="font-size: 16px;">Impressively, the performance of ‘LM vs. LM’ was 17–20% better than the next best fact-checking baseline on challenging language tasks. But perhaps more importantly, ‘LM vs. LM’ provides an initial demonstration of how self-critique can reduce the incoherence of LLMs. However, this method only critiques the products of reasoning and doesn’t allow for an adaptation of the reasoning process itself. In contrast, the next paper produces improvements to LLM reasoning by evolving increasingly effective prompts.<br>

<p style="font-size: 16px;"><b>Paper 2 — “PromptBreeder: Self-Referential Self-Improvement Via Prompt Evolution.”</b><br>
Much like humans can gain clarity by reframing a problem, the performance of LLMs can be improved by tailoring their prompts to specific tasks [5]. To clarify this concept, envision how an LLM’s capacity to solve mathematical problems could be enhanced by instructing it to “emulate Stephen Hawking.” In contrast to this speculative, man-made example, Promptbreeder systematically and automatically evolves prompts tailored to a specific domain. In other words, it iteratively critiques and adapts the way that it frames a given class of problems.<p align="center">

<p style="font-size: 16px;">Promptbreeder starts with a semi-random collection of prompts and progressively mutates them, retaining only the best, until it generates effective task-specific prompts. Leveraging the ability of transformers to rephrase ideas, an LLM is used to mutate the task-prompts by using a mutation-prompt such as “Make a variant of this prompt.” Notably, to avoid diminishing returns, Promptbreeder doesn’t solely improve task-prompts but also evolves better mutation-prompts, thereby enhancing its own prompt creation process. For those who are interested, a helpful diagram depicting this self-improvement process is located just after the conclusion. As a result of this highly self-referential search process, Promptbreeder was able to evolve detailed, effective prompts — the following example was produced to precede hate speech classification:

<p align="center">
  <img src="/art2_2.webp" alt="Alt Text">
</p>

<p style="font-size: 16px;"><b>Conclusion.</b><br>
Both of these papers fold some form of self-critique into LLMs, encouraging deliberate reasoning. In doing so, they produce models that are more robust and reliable in their reasoning capacity. However, there remains considerable scope [6,7,8,9,10] for future research to facilitate a more general critique of pure reason in LLMs and, in doing so, produce the next generation of generative AI.

<p align="center">
  <img src="/art2_3.webp" alt="Alt Text">
</p>

<p style="font-size: 16px;"><b>References.</b><br>
[1] Bubeck, Sébastien, et al. “Sparks of artificial general intelligence: Early experiments with gpt-4.” arXiv:2303.12712 (2023).<br>
<br>
[2] Vaswani, Ashish, et al. “Attention is all you need.” NeurIPS (2017). <br>
<br>
[3] OpenAI. “GPT-4 Technical Report.” arXiv:2303.08774 (2023). <br>
<br>
[4] Cohen, Roi, et al. “LM vs LM: Detecting Factual Errors via Cross Examination.” arXiv:2305.13281 (2023). <br>
<br>
[5] Creswell, Antonia, Murray Shanahan, and Irina Higgins. “Selection-inference: Exploiting large language models for interpretable logical reasoning.” ICLR (2023).<br>
<br>
[6] Dhuliawala, Shehzaad, et al. “Chain-of-Verification Reduces Hallucination in Large Language Models.” arXiv:2309.11495 (2023).<br>
<br>
[7] Xue, Tianci, et al. “RCOT: Detecting and Rectifying Factual Inconsistency in Reasoning by Reversing Chain-of-Thought.” arXiv:2305.11499 (2023).<br>
<br>
[8] Bai, Yuntao, et al. “Constitutional ai: Harmlessness from ai feedback." arXiv:2212.08073 (2022).<br>
<br>
[9] Beck, Jacob, et al. “A survey of meta-reinforcement learning.” arXiv:2301.08028 (2023).<br>
<br>
[10] Clune, Jeff. “AI-GAs: AI-generating algorithms, an alternate paradigm for producing general artificial intelligence.” arXiv:1905.10985 (2019).<br>
<br>
<p style="font-size: 16px;"> <b>Acknowledgments:</b> The title of this article was inspired by a Q and A session following a talk given by Dr. Beatrice Fazi at the Warwick CIM Conference 2023. The title is merely a play on words and the article, hopefully clearly, makes no attempt to discuss Kant’s work.
<p align="center">
  <img src="/art2_4.webp" alt="Alt Text">
</p>
<p align="center" style="font-size: 11px;"> AI-generated art for this post
 </p>
</p>

---
layout: single
permalink: /article4/
---
<h1>Title</h1>

<p style="font-size: 16px;"><b>Introduction.</b><br>
The rapid evolution of foundation models has led to a new era of AI [1] capabilities characterised by increasingly reliable and versatile reasoning. As these highly-capable models emerge, AI laboratories are divided on whether to restrict access or open-source them [2]. By openly publishing all of the relevant code and weights, open-sourced models foster collaborative innovation and the collective advancement of AI capabilities. Once released, they can be utilised, scrutinised, and customised by a global research community. <br>

<p style="font-size: 16px;">However, the openness of these models poses a challenge, as their release into the public domain makes it nearly impossible to prevent misuse by scammers, terrorists, and any other bad actors. This article aims to briefly outline typical approaches to model accessibility, ranging from tight restrictions to open-source availability. Additionally, we will introduce an approach we call Natural Language Access (NLA), which strikes a balance between the more open and closed levels of model access. <br>

<p style="font-size: 16px;"><b>Categorising Model Access.</b><br>
Broadly speaking, highly-capable foundation models currently fall into three tiers of accessibility [3]:<br>
<ol style="font-size: 16px;">
<li>Closed models, like Gopher [4] from DeepMind, keep their code entirely inaccessible beyond the lab or company that produced it.</li>
<li>Queryable models, like Chat-GPT [5] by OpenAI, allow users to iteratively prompt it, with responses appearing on a user interface.</li>
<li>Open-source models, like GPT-J [6] from EleutherAI, make both the code and model weights publicly available.</li>
</ol>
<p style="font-size: 16px;">But how do we determine the appropriate level of accessibility? To arrive at an answer, we must examine the challenges associated with each level of model access.
<br>

<p style="font-size: 16px;"><b>Considerations in Model Access.</b><br>
Model access presents a fundamental tension between distributing power and preventing misuse. Closed models concentrate the power of LLMs within the hands of a select few, while open-source models remain perpetually accessible to bad actors. Straddling these extremes, queryable models mitigate the worst aspects of both open and closed models. Unlike closed models, they allow anyone to utilise and scrutinise their capabilities via prompting. However, unlike open-source models, the activity of queryable models can be monitored and constrained by safeguards to prevent misuse. Even in the event of a critical vulnerability, model access can be temporarily rolled back while patches are applied. <br>

<p align="center">
  <img src="/art5_1.png" alt="Alt Text">
</p>

<p style="font-size: 16px;">Our analysis so far suggests that queryable models avert the worst aspects of both open and closed models. However, it hasn’t yet accounted for a crucial factor - the impact of model access on AI progress. Closed and queryable models, by withholding information on the weights and architecture, stifle innovation. They therefore have an increased risk of falling behind [7] the more transparent and customisable open-source models. <br>

<p style="font-size: 16px;">Regardless of whether accelerated AI progress is a generally desirable goal, there is a practical case for ensuring models are competitive (innovative and customisable) as well as safe. Put simply, we can’t let safeguarded and thoughtful models be outpaced by innovative (but perhaps reckless) alternatives. The next section introduces a potential solution—Natural Language Access—that retains the strengths of queryable models while allowing for increased user customization.<br>

<p align="center">
  <img src="/art5_2.png" alt="Alt Text">
</p>

<p style="font-size: 16px;"><b>Natural Language Access.</b><br>
NLA models, such as GPT-Store [8] from OpenAI, represent a fourth level of access. As a definition, NLA models are queryable with the additional property that they can be reprogrammed through natural language conversations. Unlike traditional approaches where developers require direct access to the code and weights, NLA allows an individual to shape model behaviour indirectly. 
<br>

<p style="font-size: 16px;">This novel level of access is enabled by advancements in the programming and action-selection capabilities of foundation models, allowing them to serve as intermediaries between users and source code. Through natural language conversations, users can refine and customise their model without the need for direct access to potentially sensitive source code. To prevent undesirable customisations, companies or labs can monitor and restrict the set of actions available to the model in response to human prompting. As such, NLA retains the safety of queryable models while enabling a higher degree of customizability. <br>

<p style="font-size: 16px;"><b>Conclusion.</b><br>
In relation to model access, developers and governments must thoughtfully consider [9] the balance between democratisation, innovation, and safety. While closed models and open-source alternatives present distinct challenges, queryable models emerge as a pragmatic compromise. Building upon this foundation, this article introduces NLA as an innovation-friendly level of model accessibility. By retaining the safety features of queryable models while amplifying customization, we hope that NLA will serve as an important tool for navigating the evolving landscape of increasingly capable foundation models.<br>

<p style="font-size: 16px;"><b>Footnote:</b>
In this article, we excluded a discussion of gated access, in which architectures and weights are only made available to trusted groups. This decision stems from our belief that gated access is inherently unstable in the face of leaks or hacks and, as such, likely to collapse into an almost-completely closed or open-source state.<br>

<p style="font-size: 16px;"><b>Acknowledgements:</b>
 I would highly recommend “Open-Sourcing Highly Capable Foundation Models” [2] for more details on some of the topics discussed in this article. <br>
  
<p style="font-size: 16px;"><b>References.</b><br>
[1]Bubeck, et al. “Sparks of artificial general intelligence: Early experiments with gpt-4.” arXiv preprint arXiv:2303.12712 (2023). <br>
<br>
[2] Seger, Dreksler, Moulange, Dardaman, Schuett, Wei, et al. “Open-Sourcing Highly Capable
Foundation Models: An Evaluation of Risks, Benefits, and Alternative Methods for Pursuing Open-Source Objectives”. Centre for the Governance of AI (2023).<br>
<br>
[3]  Solaiman. "The gradient of generative AI release: Methods and considerations." ACM Conference on Fairness, Accountability, and Transparency (2023). <br>
<br>
[4] Rae, et al. “Scaling language models: Methods, analysis & insights from training gopher.” arXiv:2112.11446 (2021). <br>
<br>
[5] Brockman, et al. “Introducing ChatGPT and Whisper APIs.” https://openai.com/blog/introducing-chatgpt-and-whisper-apis (2023) - Vitised Nov 2023. <br>
<br>
[6] Wang and Komatsuzaki. “GPT-J-6B: A 6 Billion Parameter Autoregressive Language Model.” https://github.com/kingoflolz/mesh-transformer-jax (2021) - Vitised Nov 2023. <br>
<br>
[7] Milmo. “Google engineer warns it could lose out to open-source technology in AI race.” The Guardian (2023). <br>
<br>
[8] OpenAI. “Introducing GPTs.” https://openai.com/blog/introducing-gpts (2023) - Vitised Nov 2023. <br>
<br>
[9] Anderljung and Hazell. “Protecting Society from AI Misuse: When are Restrictions on Capabilities Warranted?” Centre for the Governance of AI (2023). <br>
<br>
[10] Seger, et al. "Democratising ai: Multiple meanings, goals, and methods." AAAI Conference on AI, Ethics, and Society (2023). <br>

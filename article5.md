---
layout: single
permalink: /article5/
---
<h1>Natural Language Access: A Safer Alternative to Open-Sourcing Foundation Models</h1>

<p style="font-size: 16px;"><b>Introduction.</b><br>
Foundation models have rapidly become reliable and versatile reasoning machines [1]. As these highly capable models emerge, AI laboratories are divided on whether to restrict access or open-source them [2]. By openly publishing all of the relevant code and weights, open-sourced models foster collaborative innovation and the collective advancement of AI capabilities. Once released, they can be utilised, scrutinised, and customised by a global research community.  <br>

<p style="font-size: 16px;">However, the openness of these models poses a challenge, as their release into the public domain makes it nearly impossible to prevent misuse by scammers, terrorists, and any other bad actors. This article aims to briefly outline typical approaches to model accessibility, ranging from tight restrictions to open-source availability. Additionally, we will introduce an approach we call Natural Language Access (NLA), which strikes a balance between the more open and closed levels of model access. <br>

<p style="font-size: 16px;"><b>Categorising Model Access.</b><br>
Broadly speaking, highly capable foundation models currently fall into three tiers of accessibility [3]:<br>
<ol style="font-size: 16px;">
<li>Closed models, like Gopher [4], keep their model entirely inaccessible beyond the lab or company that produced it.</li>
<li>Queryable models, like Chat-GPT [5], can be prompted, with responses appearing on a user interface - but the code and weights are kept from the public domain.</li>
<li>Open-Source models, like GPT-J [6], make both the code and model weights publicly available.</li>
</ol>
<p style="font-size: 16px;">But how do we determine the appropriate level of accessibility? To answer this, we must examine the challenges associated with each level of model access. <br>

<p style="font-size: 16px;"><b>Considerations in Model Access.</b><br>
Model access presents a fundamental tension between distributing power and preventing misuse. Closed models concentrate power in the hands of a select few, while open-source models remain perpetually accessible to bad actors. Straddling these extremes, queryable models arguably mitigate the worst aspects of both open and closed models. Unlike closed models, they allow anyone to utilise and scrutinise their capabilities via prompting. However, unlike open-source models, the activity of queryable models can be monitored and constrained by safeguards to prevent misuse. Even in the event of a critical vulnerability, model access can be temporarily rolled back while patches are applied. <br>

<p style="font-size: 16px;">However, this comparison has so far neglected a crucial factor - the public's capacity to develop and customise the model’s code. Queryable models utilise context (user prompts) to provide intelligent responses, but in order to prevent misuse, the underlying code is inaccessible and unaltered between prompts. As such, although safer than open-source models, queryable approaches stifle the public's ability to develop and customise foundation models. There is a danger that these safe and thoughtful models will be outpaced by innovative (but perhaps reckless) open-source alternatives whose code can be directly accessed and altered by the public [7]. In the next section, we introduce a novel solution, which we call Natural Language Access (NLA), that retains the safety of queryable models while allowing for increased user customisation.<br>

<p align="center">
  <img src="/art5_1.png" alt="Alt Text">
</p>

<p style="font-size: 16px;"><b>Natural Language Access.</b><br>
NLA represents a fourth level of model accessibility that strikes a balance between being queryable and open-source. NLA models are queryable but, crucially, also allow the public to indirectly alter their code through natural language conversations. Along with prompting intelligent responses, by simply talking to the model, users can guide it to reprogram itself in alignment with their suggestions. This novel level of access is made possible due to recent advancements in the programming capabilities of foundation models, allowing them to serve as intermediaries between users and source code. <br>

<p style="font-size: 16px;">But how is this more customisable than a queryable approach? In a queryable model, a user can engage in a conversation with the user-interface to produce increasingly precise responses. However, these changes are transient, and the code itself is left unchanged by a user-specific conversation. In contrast, NLA involves a conversation aimed at producing lasting impacts to the model itself, rather than responding appropriately to a given set of prompts. These altered and customised models can be made accessible for the general public to utilise and scrutinise. In summary, unlike queryable approaches, in NLA models there is an option to permanently and systematically change the way that a model operates, perhaps for others to use as well. <br>

<p style="font-size: 16px;">But how is this safer than an open source model? Although the public can still alter the code, we believe that NLA’s indirect approach is much less dangerous than the direct access provided via open-sourcing To prevent undesirable customisations, NLA can restrict and safeguard the range of possible changes that the model can make to itself. This can range from narrow restrictions, like the GPT-store [8], to a slightly broader potential for self-improvement. Crucially, in NLA models, unlike open-source, alterations to the code can be monitored and constrained by the AI labs that produce them. As such, NLA retains the safety of queryable models while enabling a higher degree of customisability. <br>
  
<p align="center">
  <img src="/art5_2.png" alt="Alt Text">
</p>

<p style="font-size: 16px;"><b>Conclusion.</b><br>
In relation to model access, developers and governments must thoughtfully consider the balance between democratisation, innovation, and safety [9]. While closed models and open-source alternatives present distinct challenges, queryable models emerge as a safe but unadaptable compromise. Building upon this foundation, this article introduces NLA as an innovation-friendly level of model accessibility. By retaining the safety features of queryable models while amplifying customisation, we hope that NLA will serve as an important tool for navigating the evolving landscape of increasingly capable foundation models. <br>

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

<p align="center">
  <img src="/art5_3.png" alt="Alt Text">
</p>
<p align="center" style="font-size: 11px;"> An AI generated figure inspired by this article </p>
<p style="font-size: 16px;"> November 2023 </p>

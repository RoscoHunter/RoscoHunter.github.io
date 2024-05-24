---
layout: single
permalink: /article7/
---
<h1>Strategies for Responsible AI Dissemination</h1>

<p style="font-size: 16px;"><b>1. Motivation</b><br>
Large language models (LLMs) have rapidly matured into sophisticated reasoning machines. Their ability to approximate, or even outperform, human responses across a broad spectrum of intellectual tasks has garnered the world’s attention. The success of these models raises an important question: Should the general public be able to access a model’s code, given its potential impact on society?<br>

<p style="font-size: 16px;">Currently, developers are divided on whether to release (i.e., open-source) or restrict access to the inner workings of their most capable models. Some developers favour open-sourcing, publishing every detail of their model so that anyone can utilise, scrutinise, and customise the code. Proponents of this approach argue that it fosters innovation and distributes the economic and epistemic value that their models generate. In contrast, some developers prefer to keep their code private, limiting access to a select group of trusted collaborators. They argue that withholding their code from the public domain is the only way to guarantee that it won’t be fine-tuned for malicious applications, from writing fake news to designing malware.<br>

<p style="font-size: 16px;">In this article, we examine the benefits and drawbacks of various strategies for AI dissemination. We start by considering the three main approaches to model release, and end by outlining some lesser-known tactics. The goal is to provide an introduction to the field of model dissemination, rather than a comprehensive survey. That being said, most models can be broadly categorised into one of the following three descriptions:<br>
<ol style="font-size: 16px;">
<li>Closed models, like Gopher, are entirely inaccessible beyond the lab or company that produced them. </li>
<li>Queryable models, like Chat-GPT, can be prompted, with responses appearing on a user interface, but the code and weights are kept from the public domain. </li>
<li>Open-Source models, like GPT-J, make both the code and model weights publicly available. </li>
</ol>

<p style="font-size: 16px;"><b>2. Three Common Strategies for Model Dissemination</b><br>
<p style="font-size: 16px;"><b>2.1 Closed Models </b><br>
Closed models minimise the likelihood of misuse by restricting access to a small group of trusted individuals. This approach has been applied to control other dangerous technologies where legislator’s main concern is preventing misuse. For instance, countries that restrict firearm ownership tend to have lower rates of firearm-related homicides. On a more existential scale, nuclear non-proliferation treaties prevent countries without nuclear weapons from acquiring them. The logic is that an LLM, firearm, or nuclear weapon can’t be misused by someone who can’t even access it. <br>

<p style="font-size: 16px;">However, the secrecy of these models blunts their effectiveness and social value. Firstly, there is a loss in terms of the model’s quality and objectivity. The development and evaluation of a closed model can only draw from the skills and perspectives of a limited number of individuals. As a result, its design might be naive, and the resulting outputs could exhibit bias [1]. Secondly, there is a loss in terms of the public interest. Being unable to access the model in any form, the general public is excluded from the knowledge that these models offer. This leads to an epistemic inequality in favour of the highly-resourced AI companies. <br>

<p style="font-size: 16px;"><b>2.2 Open-Source Models </b><br>
On the other extreme, open-source models provide unfettered access to the widest possible audience. Proponents argue that open-sourcing facilitates external scrutiny from a global community of researchers, helping to rectify any lingering biases or limitations of the original model [2]. Furthermore, it fosters innovation, as every developer has the opportunity to read, reuse, or build upon the code and weights of an open-source model. This is particularly consequential for the most capable models, as their training requires a scale of computational resources that only a few companies possess. <br>

<p style="font-size: 16px;">The momentum and scale of open-source innovation is staggering. Meta’s core family of open-source language models, LLaMA, became available in February 2023. By September, Meta reported that LLaMA-based models had been downloaded through Hugging Face over 30 million times, with tens of thousands of startups using their latest model [3]. In this same report, Meta claimed that the open-source community had produced variants of LLaMA with “improvements of up to 46% for benchmark datasets”. <br>

<p style="font-size: 16px;">However, the openness of these models also poses risks, as anyone can access and misuse them. In July 2023, members of the Senate Subcommittee on Privacy, Technology, and the Law expressed their concerns in a letter to Meta’s CEO [4]. In this letter, they warned of the potential for LLaMA to facilitate “misuse in spam, fraud, malware, privacy violations, harassment, and other wrongdoing and harms.” They followed this by noting that “even in the short time that generative AI tools have been available to the public, they have been dangerously abused.” <br>

<p style="font-size: 16px;">Not only do open-source models lack robust safeguards to prevent direct misuse, but their weights can even be finetuned specifically for malicious applications. Fine-tuning tailors the weights of a model by training it to perform well on a specific task. This is often employed to improve a model’s performance for tasks, such as grammar correction or medical diagnostics. However, it can also make a model more dangerous, especially if the training data is harmful. By fine-tuning LLaMA for 100 GPU hours on adversarial data, Gade et al. [5] almost completely removed all safeguards, observing a 97% drop in the number of harmful instructions that the model refused to answer. <br>

<p style="font-size: 16px;">Even more concerning, after an open-source model is released, there is no way to retract it from the public domain if it causes excessive harm. Instead, it remains perpetually accessible for direct misuse or malicious fine-tuning, with a digital footprint that is impossible to erase. This perpetual accessibility would be catastrophic to society in the event that an open-source model could describe novel toxins [6] or ransomware, when appropriately prompted and fine-tuned. While we are yet to witness any truly catastrophic capabilities of open-source LLMs [7], there are already concerning signs [8]. Moreover, the likelihood of such risks increase with each successive generation of language models. Given the potential for harm with open-source models and the over centralisation of closed models, is there a compromise?  <br>

<p style="font-size: 16px;"><b>2.3 Queryable Models </b><br>
Straddling the extremes, queryable models mitigate undesirable aspects of both approaches. Unlike closed models, anyone can elicit their knowledge and scrutinise their outputs through prompting. However, unlike open-sourcing, the activity of queryable models can be monitored and constrained. Even in the event of unexpected harm, model access can be temporarily rolled back while patches are applied. Unfortunately, despite these advantages, queryable models still exhibit a number of concerning faults. 

<p style="font-size: 16px;">Firstly, queryable models don’t quite offer the same safety guarantees as closed models. While language models are improving at solely producing benign responses, outputs that are harmful or inaccurate still occur. Given a queryable model, members of the public are bound to actively seek or inadvertently encounter these harmful outputs. Secondly, these models can’t be scrutinised to quite the same extent as an open-source approach. Although a queryable model’s outputs can be statistically tested for various biases, they fall short of providing all of the relevant information that external auditors might require.  <br>

<p style="font-size: 16px;">Perhaps the largest deficit of queryable models is that their code can’t be modified. In order to prevent misuse, the code that underlies a queryable model is inaccessible and unaltered between prompts. This stifles the public’s capacity to improve the model’s performance or tailor its code for a specialised task. There is a danger that these safe and thoughtful models will be outpaced by innovative (but perhaps reckless) open-source alternatives whose code can be directly altered by the public [9]. <br>

<p style="font-size: 16px;"><b>3. Alternative Approaches </b><br>
Closed, queryable, and open-source models each exhibit a significant drawback with respect to one aspect of a model’s successful release. We will now briefly consider three alternative paradigms for releasing an LLM:

<p style="font-size: 16px;">1) Downloadable models [10], such as Craiyon, allow users to download the model’s code, subject to approval. This differs from both closed and queryable models, which restrict source code access to a single company or lab. It also differs from open-souring, where the code is made publicly accessible, without exception. In theory, downloadable releases can help to stress-test an LLM before it’s released more broadly. Nevertheless, some researchers argue that downloadable release is inherently unstable as it can prematurely collapse into open-sourcing. In particular, the downloadable approach rests on the assumption that none of the model-holders will disseminate, or even accidentally leak, the code. As such, for models with a high risk of misuse, this approach would typically be regarded as too risky. <br>

<p style="font-size: 16px;">2) Structured Access [11] attempts to provide users with “controlled, arm’s length interactions with their AI systems.” This arm’s length approach prevents a user from obtaining the information required to recreate and disseminate the model themselves, which was our concern with downloadable release. One example of structured access is GPT-3, which allows users to fine-tune an LLM or integrate it into their own application using OpenAI’s API. Crucially, while OpenAI lets a user modify aspects of GPT-3 through their API, the user would struggle to discern the details of the model’s inner workings. <br>

<p style="font-size: 16px;">More recently, structured access has also been associated with the idea of minimal sufficiency - where AI researchers are given the minimum level of access they need to do their individual jobs [12]. For instance, a researcher evaluating an LLM would be granted different forms of access to the model than a researcher working on interpretability. Once again, this hides most of the model’s inner workings from any individual user. In summary, structured access represents a broad range of approaches to model release that prevent users from accessing unnecessary information about a model's inner workings. <br>

<p style="font-size: 16px;">3) Staged Disclosure [13] involves gradually releasing the model’s components over time. Examples of this include GPT-2, whose parameters were originally released in four stages, with the number of released parameters increasing at each stage. This gradual deployment allows developers to test their safeguards in a low-capability regime before releasing their most capable models. However, staged disclosure says nothing about exactly which of the model’s capabilities should be released. As such, it is often viewed as a coarse tactic that can be applied alongside the dissemination strategies that we’ve discussed so far. In particular, for almost any strategy of model release, companies might be wise to initially release smaller versions of their model. <br>

<p style="font-size: 16px;"><b>4. Conclusion.</b><br>
Clearly, there is no silver bullet that resolves the tensions regarding the dissemination of an LLM. Instead, practitioners and policymakers must thoughtfully consider the balance between democratisation, innovation, and safety, with no simple solutions. If you are interested in learning more about this topic then please check out the references below. For a draft paper on an alternative release paradigm, see <a href="../Conversational_Access.pdf">Releasing the Source Code of Language Models via Conversational Access</a>

<p style="font-size: 16px;"><b>References.</b><br>
[1] E. Seger, A. Ovadya, D. Siddarth, B. Garfinkel, A. Dafoe. Democratising AI: Multiple Meanings, Goals, and Methods (2023) <br>
<br>
[2] E. Seger, N. Dreksler, R. Moulange, E. Dardaman, J. Schuett, K. Wei, C. Winter, M. Arnold, S. Ó. hÉigeartaigh, A. Korinek, et al. Open-Sourcing Highly Capable Foundation Models: An Evaluation of Risks, Benefits, and Alternative Methods for Pursuing Open-Source Objectives (2023) <br>
<br>
[3] J. Spisak, S. Edunov. The LLaMA Ecosystem: Past, Present, and Future (2023) <br>
<br>
[4] R. Blumenthal, J. Hawley. Meta LLaMA Model Leak Letter (2023) <br>
<br>
[5] P. Gade, S. Lermen, C. Rogers-Smith, J. Ladish. BadLLaMA: Cheaply Removing Safety Fine-Tuning from LLaMA 2-chat 13b (2023) <br>
<br>
[6] F. Urbina, F. Lentzos, C. Invernizzi, S. Ekins. A Teachable Moment for Dual-Use (2022) <br>
<br>
[7] M. Kinniment, L. J. K. Sato, H. Du, B. Goodrich, M. Hasin, L. Chan, L. H. Miles, T. R. Lin, H. Wijk, J. Burget, et al. Evaluating Language-Model Agents on Realistic Autonomous Tasks (2023) <br>
<br>
[8] J. Achiam, S. Adler, S. Agarwal, L. Ahmad, I. Akkaya, F. L. Aleman, D. Almeida, J. Altenschmidt, S. Altman, S. Anadkat, et al. GPT-4 Technical Report (2023) <br>
<br>
[9] D. Milmo. Google Engineer Warns it Could Lose Out to Open-Source Technology in AI Race (2023) <br>
<br>
[10] I. Solaiman. The Gradient of Generative AI Release: Methods and Considerations (2023) <br>
<br>
[11] T. Shevlane. Structured Access: An Emerging Paradigm for Safe AI Deployment (2022) <br>
<br>
[12] B. S. Bucknall, R. F. Trager. Structured Access For Third-Party Research on Frontier AI Models: Investigating Researchers’ Model Access Requirements (2023) <br>
<br>
[13] I. Solaiman, M. Brundage, J. Clark, A. Askell, A. Herbert-Voss, J. Wu, A. Radford, G. Krueger, J. W. Kim, S. Kreps, et al. Release Strategies and the Social Impacts of Language Models (2019) <br>
  
<p align="center">
  <img src="/art7.png" alt="Alt Text">
</p>
<p align="center" style="font-size: 11px;"> AI-generated art for this article </p>

<p style="font-size: 16px;"> May 2024 </p>

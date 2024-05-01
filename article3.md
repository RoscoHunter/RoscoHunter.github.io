---
layout: single
permalink: /article3/
---
<h1>Automating Intelligence: How AutoML Brings Precision to AI Development</h1>

<p style="font-size: 16px;"><b>Motivation.</b><br>
At the outset of 2023, OpenAI unveiled GPT-4 [1], claiming it to be “at or beyond human-level for many tasks… showing sparks of artificial general intelligence (AGI)”. This mirrors the breakthrough that marked the start of the 20th century when the Wright Brothers achieved the first sustained and controlled heavier-than-air powered flight [2,3]. In this article we will draw further parallels between artificial flight and intelligence to frame our progress on AI and offer insights into what’s to come. For example, early models in both fields were inspired by nature and limited to the most rudimentary of abilities. Aviation’s pioneers drew inspiration from bird wings for early gliders, and similarly, AI developers were initially inspired by biological neurons.<br>

<p style="font-size: 16px;">After years of incremental advancements, the Wright Brothers and OpenAI demonstrated humanity’s capacity to compete with nature for the very first time — in the realms of flight and intelligence, respectively. Following the Wright brothers’ flight, aviation witnessed a surge of investment that turned aircraft production into a science. After AI’s “Chat-GPT” moment, a similar precision is now required to (carefully) fan the sparks of AGI. Enter Automated Machine Learning (AutoML), a field that aims to systematize and streamline the design of AI models. In this article, we will delve into two instances of AutoML, highlighting its impact on architecture design and learning algorithms. These examples will hopefully illustrate how AutoML is revolutionizing AI development, elevating it from the realm of hobbyist aircraft design to the precision of supersonic jet production.<br>

<p style="font-size: 16px;"><b>Architecture Design.</b><br>
Traditionally, AI models were hand-designed based on the judgments of seasoned AI researchers. A branch of AutoML, Neural Architecture Search (NAS), challenges this setup with a more rigorous framework, using methods like reinforcement learning [4] or gradient descent [5] to locate high-performance networks from a space of possible designs. Instead of relying on intuition or tedious human-made experiments, NAS automates the entire procedure by efficiently searching through the innumerate ways that network components can be combined [6]. However, during search, it typically needs to train the networks that it samples, thereby slowing the pace of development.<br>

<p style="font-size: 16px;">In aircraft design, before costly human testing, prototypes are probed with wind tunnels or mathematical models. In the domain of network design, analogous techniques (Zero-cost NAS) are employed to cheaply assess prospective network designs without training them. Among these zero-cost methods is GenNAS [7], which could be described as the wind tunnel of network design. It uses a series of proxy tasks to quickly estimate an architecture’s ability to capture spectral and spatial information — aiming to approximate its post-training performance on real-world tasks.<br>

<p style="font-size: 16px;">Another approach involves zero-cost metrics [8], which are formulas that analyse network characteristics before training. Specifically, these formulas probe the gradients and activations of a network at initialization in order to predict its performance after training — much like how mathematical equations for fluid-flow can be used as an estimate of an aircraft’s performance before it even flies. While many methods in NAS are still in their infancy, they lay the foundation for a more scientific approach to designing proficient and efficient neural networks.<br>

<p style="font-size: 16px;"><b>Algorithm Design.</b><br>
Even if a neural network is optimally designed, it relies on a learning algorithm, much like an aircraft relies on its propulsion system. Designing and fine-tuning these learning algorithms presents a significant challenge for Machine Learning. Once again, AutoML attempts to bring structure to this process. For example, a team at Google [9], employed symbolic evolution (AutoML) to generate novel learning algorithms. Their best algorithm, LION, consistently outperforms established approaches like AdamW, achieving an impressive 3x learning speedup in certain tasks.<br>
  
<p style="font-size: 16px;">Yet, even after establishing a sound learning strategy, there’s the task of fine-tuning a multitude of hyperparameters, including variables like the learning rate, momentum, batch size, etc. Currently, engineers ‘babysit’ GPTs [10] and make adjustments to their learning algorithm during training in an ad-hoc manner — an unsustainable and unscientific process. This is where a specialized branch of AutoML called Hyperparameter Optimization (HPO) comes into play. HPO typically employs Bayesian [11] or evolutionary [12] techniques to efficiently search for optimal hyperparameter settings, automating a once-imprecise human-dependent task. This automation in hyper-parameter selection not only saves time but also leads to improvements in model performance.<br>
  
<p style="font-size: 16px;"><b>Conclusion.</b><br>
In summary, the pace at which Artificial Intelligence will advance remains uncertain, but it is clear that AutoML stands as an indispensable tool for shaping the future of AI systems. It brings precision and efficiency to our exploration of intelligence, which will hopefully mirror humanity’s journey from fragile manually-designed gliders to precise supersonic jets. If you are interested in exploring any of these ideas further then please check out the references for more in-depth information.

<p style="font-size: 16px;"><b>References.</b><br>
[1] Bubeck, Sébastien, et al. “Sparks of artificial general intelligence: Early experiments with gpt-4.” arXiv preprint arXiv:2303.12712 (2023). <br>
<br>
[2] Russell, Stuart J. “Artificial intelligence a modern approach.” Pearson Education (2010). <br>
<br>
[3] Culick, Fred. E. C. “The Wright brothers: first aeronautical engineers and test pilots.” AIAA (2003). <br>
<br>
[4] Zoph, Barret, and Quoc V. Le. “Neural architecture search with reinforcement learning.” ICLR (2017). <br>
<br>
[5] Liu, Haoxiao, et al. “DARTS: Differentiable Architecture Search.” ICLR (2019). <br>
<br>
[6] Dong, Xuanyi, et al. “NATS-Bench: Benchmarking nas algorithms for architecture topology and size.” Transactions on Pattern Analysis and Machine Intelligence (2021). <br>
<br>
[7] Li, Yuhong, et al. “Generic neural architecture search via regression.” NeurIPS (2021). <br>
<br>
[8] White, Colin, et al. “A Deeper Look at Zero-Cost Proxies for Lightweight NAS.” ICLR Blog Track (2022). <br>
<br>
[9] Chen, Xiangning, et al. “Symbolic discovery of optimization algorithms.” arXiv preprint arXiv:2302.06675 (2023). <br>
<br>
[10] OpenAI. “GPT-4 Technical Report.” arXiv preprint arXiv:2303.08774 (2023). <br>
<br>
[11] Snoek, Jasper, et al. “Practical Bayesian optimization of machine learning algorithms.” NeurIPS (2012). <br>
<br>
[12] Loshchilov, Ilya, and Frank Hutter. “CMA-ES for hyperparameter optimization of deep neural networks.” ICLR (2016). <br>
  
<p align="center">
  <img src="/art3.webp" alt="Alt Text">
</p>
<p align="center" style="font-size: 11px;"> An AI generated figure inspired by this article </p>
<p style="font-size: 16px;"> November 2023 </p>

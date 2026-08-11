---
layout: default
title: "Horizon Summary: 2026-08-11 (EN)"
date: 2026-08-11
lang: en
---

> From 37 items, 9 important content pieces were selected

---

1. [New Paper Shows Encrypted LLM Reasoning Traces Can Be Stolen](#item-1) ⭐️ 9.0/10
2. [Meta Releases Muse Glimmer, a 30B Open-Weights Agentic Model](#item-2) ⭐️ 9.0/10
3. [Nvidia Launches Nemotron 3.5 Lightning and Open-Source NeMo Switchyard](#item-3) ⭐️ 8.0/10
4. [Compression Is Prediction: Ngrok Blog Post Sparks Debate on Information Theory](#item-4) ⭐️ 8.0/10
5. [Mojo 1.0 Released: Python-Compatible Language for AI Performance](#item-5) ⭐️ 8.0/10
6. [Nvidia&\#x27;s AI Dominance Faces Demand and Software Lock-In Risks](#item-6) ⭐️ 8.0/10
7. [London Underground expands live facial recognition trial, sparking privacy fears](#item-7) ⭐️ 8.0/10
8. [Decoupled Descent Uses AMP Onsager Corrections to Certify Train-Test Error Match](#item-8) ⭐️ 8.0/10
9. [Graphene-Powered Soft Lens Promises Compact Auto-Focusing](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [New Paper Shows Encrypted LLM Reasoning Traces Can Be Stolen](https://simonwillison.net/2026/Aug/11/stealing-reasoning-traces/#atom-everything) ⭐️ 9.0/10

Researchers demonstrated a practical attack on Anthropic, OpenAI, and Google APIs that recovers hidden chain-of-thought reasoning from encrypted blocks. The blocks were replayed into weaker sibling models, which were then jailbroken to output the stronger model&\#x27;s reasoning in plaintext. This exposes a significant privacy flaw in proprietary LLM APIs and raises serious questions about the security of encrypted reasoning traces. It also highlights broader risks for AI safety and model alignment, especially as providers increasingly offer paid reasoning features. The attack worked because models in the same family shared the same encryption key, and the encrypted blobs were portable across sessions, users, and models. Claude Haiku 4.5 was reportedly the easiest to attack, and while the providers have now fixed the issue, the paper&\#x27;s appendix includes extensive extracted reasoning traces that reveal what hidden chain-of-thought looks like for proprietary models.

rss · Simon Willison · Aug 11, 22:40

**Background**: State-of-the-art LLMs often generate an internal chain of thought before answering, and API providers may hide this reasoning behind encrypted blocks so that it cannot be read directly by users. This design assumes the encrypted blocks are safe to store and replay, but the paper shows they can be replayed into a weaker sibling model. By jailbreaking the weaker model, attackers can force it to decode the trace and reveal the original reasoning. The research is a reminder that encryption alone does not guarantee privacy when models within the same provider share keys and behavior.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.09867">[2608.09867] Stealing Reasoning Traces from Proprietary LLM APIs</a></li>
<li><a href="https://www.alphaxiv.org/abs/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs | alphaXiv</a></li>
<li><a href="https://runtimewire.com/article/openai-anthropic-and-google-blocked-a-cross-model-reasoning-attack">OpenAI, Anthropic and Google blocked a cross-model reasoning attack</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly intrigued and some questioned the word &quot;stealing,&quot; arguing users already pay for the tokens and noting that training on other model outputs should be normal practice. Others were curious whether the cross-model replay behavior was intentionally allowed, and one commenter pointed out a simpler workaround using a thinking tool instead. Several appreciated the paper&\#x27;s confirmation that API summaries often hide messy, non-linear reasoning traces.

**Tags**: `#LLM`, `#Security`, `#Chain-of-Thought`, `#AI Privacy`, `#Research`

---

<a id="item-2"></a>
## [Meta Releases Muse Glimmer, a 30B Open-Weights Agentic Model](https://simonwillison.net/2026/Aug/10/introducing-muse-glimmer/#atom-everything) ⭐️ 9.0/10

Meta introduced Muse Glimmer, a 30B-parameter open-weights model released under the Apache 2.0 license. It is optimized for end-to-end agentic task completion, reliable tool use, and multi-step reasoning, with Simon Willison testing it locally via LM Studio. This marks Meta&\#x27;s return to open-weight releases with a permissive license, moving away from the more restrictive Llama licenses. The 30B size is significant for local deployment, as it can run on machines with 32GB+ RAM while leaving room for other applications. Muse Glimmer is a vision model capable of describing images, and Simon Willison ran it against his llm-coding-agent plugin on a Datasette codebase. The model is available via LM Studio as an 18.16GB quantized version, and was tested with a patch for LLM 0.32 compatibility.

rss · Simon Willison · Aug 10, 23:56

**Background**: Agentic AI models are designed to go beyond simple text generation by planning, using tools, and completing multi-step tasks autonomously. Benchmarks like MCP-Atlas evaluate tool-use competency against real MCP servers, while τ-bench simulates user-agent interactions to test reliability. The Apache 2.0 license is a permissive open-source license that allows broad use and modification.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/scaleapi/mcp-atlas">GitHub - scaleapi/mcp-atlas: MCP Atlas</a></li>
<li><a href="http://taubench.com/">τ-bench — Benchmarking AI Agents on Real-World Tasks</a></li>
<li><a href="https://www.masaischool.com/blog/what-is-agentic-ai/">What Is Agentic AI ? A Complete Beginner&#x27;s Guide (2026)</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Meta`, `#open-weights`, `#agentic-models`, `#LLM`

---

<a id="item-3"></a>
## [Nvidia Launches Nemotron 3.5 Lightning and Open-Source NeMo Switchyard](https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/) ⭐️ 8.0/10

Nvidia has released Nemotron 3.5 Lightning, an open 30B mixture-of-experts model with 3B active parameters, alongside NeMo Switchyard, an open-source Rust-based proxy and library for LLM traffic routing. The model is available on Hugging Face and ready for commercial use. This release strengthens the industry’s shift toward smaller, more efficient models and cost-aware model selection for agentic AI. Enterprises and developers can now reduce latency and inference cost by routing requests to the most suitable model rather than always using a large flagship. Nemotron 3.5 Lightning delivers up to 4x faster output speed and about 30% faster agentic task completion compared with peers in its class, and it can be post-trained with NVIDIA NeMo on domain data. NeMo Switchyard supports tuning-free and tunable routers that balance model capability, cost, and latency.

hackernews · droidjj · Aug 11, 19:35 · [Discussion](https://news.ycombinator.com/item?id=49263340)

**Background**: Mixture-of-experts \(MoE\) models improve efficiency by activating only a few of many expert subnetworks for each token, and a router decides which experts to use. Model routing, a complementary technique, decides which LLM should answer a given request based on complexity, cost, and latency. These two directions are part of a broader push to make LLM deployment more economical and sustainable.

<details><summary>References</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/">NVIDIA Nemotron 3.5 Lightning and NeMo Switchyard Deliver Faster, Smarter, More Efficient Agentic AI | NVIDIA Blog</a></li>
<li><a href="https://developer.nvidia.com/blog/route-ai-agent-workloads-across-models-with-nvidia-nemo-switchyard/">Route AI Agents Across Models with NVIDIA NeMo Switchyard | NVIDIA Technical Blog</a></li>
<li><a href="https://github.com/NVIDIA-NeMo/Switchyard">GitHub - NVIDIA-NeMo/Switchyard · GitHub</a></li>

</ul>
</details>

**Discussion**: Commenters welcomed the wave of small efficient models and one noted pleasant results running the 30B MLX version on Apple Silicon. Others raised practical concerns, including how routers handle prompt caching when requests are sent to different models, and criticized NVIDIA for omitting most Qwen models from a comparison chart.

**Tags**: `#AI`, `#NVIDIA`, `#LLM`, `#Open Source`, `#Model Routing`

---

<a id="item-4"></a>
## [Compression Is Prediction: Ngrok Blog Post Sparks Debate on Information Theory](https://ngrok.com/blog/compression-is-prediction) ⭐️ 8.0/10

The ngrok blog published a post titled &\#x27;Compression is prediction,&\#x27; arguing that compression is fundamentally prediction and tying machine learning to information theory. The post drew 188 points and 81 comments, with commenters adding historical and technical nuance. This argument connects core ideas in compression, prediction, and machine learning, suggesting that understanding compression can illuminate how models generalize. It resonates with longstanding theories like Solomonoff induction and the minimum description length principle, affecting how researchers think about AI. The post&\#x27;s thesis is that a good compressor is equivalent to a good predictor, but community commenters noted this holds strictly when the data distribution exactly represents future problems. When test distributions differ, lossy compression may discard rare edge cases that matter for generalization.

hackernews · nikolay · Aug 11, 19:49 · [Discussion](https://news.ycombinator.com/item?id=49263497)

**Background**: The idea that compression equals prediction has roots in algorithmic information theory, particularly Solomonoff induction, which formalizes Occam&\#x27;s razor by favoring shorter explanations. Kolmogorov complexity measures the shortest program that outputs a given object, and the minimum description length \(MDL\) principle applies this to model selection in statistics and machine learning.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Solomonoff_induction">Solomonoff induction</a></li>
<li><a href="https://en.wikipedia.org/wiki/Minimum_description_length">Minimum description length</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kolmogorov_complexity">Kolmogorov complexity</a></li>

</ul>
</details>

**Discussion**: Commenters pointed to prior art: Schmidhuber&\#x27;s work on compression progress, Grant Sanderson&\#x27;s &\#x27;Compression is Intelligence&\#x27; video series, and Ted Chiang&\#x27;s &\#x27;ChatGPT is a blurry JPEG of the web.&\#x27; A notable counterpoint from ssivark argued that compression and prediction are only functionally equivalent when the training distribution exactly matches future problems, and that generalization complicates the story.

**Tags**: `#compression`, `#prediction`, `#information theory`, `#machine learning`, `#AI`

---

<a id="item-5"></a>
## [Mojo 1.0 Released: Python-Compatible Language for AI Performance](https://www.modular.com/blog/modular-26-5-mojo-1-0-is-here) ⭐️ 8.0/10

Modular has officially released Mojo 1.0, the first stable version of its high-performance programming language for AI/ML. The release delivers a complete toolchain for writing fast, portable code across CPUs, GPUs, and other hardware. Mojo 1.0 offers Python developers a familiar syntax while enabling C-like performance and low-level control, potentially accelerating AI/ML development. It also strengthens the case for a unified language that spans everything from data centers to edge devices. Mojo uses a Python-like syntax but includes systems-programming features such as static typing and a borrow checker inspired by Rust. Its compiler is built on MLIR, allowing it to target CPUs, GPUs, TPUs, ASICs, and other accelerators, and Modular still plans to open-source the Mojo compiler and toolchain in 2026.

hackernews · dayanruben · Aug 11, 16:56 · [Discussion](https://news.ycombinator.com/item?id=49261128)

**Background**: Mojo is an in-development systems programming language created by Modular, originally intended to be a superset of Python. That goal was later abandoned or postponed indefinitely, with the roadmap now saying Mojo may or may not evolve into a full superset. By building directly on MLIR rather than LLVM, Mojo can use higher-level compiler passes and target diverse hardware, making it well suited for AI workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_%28programming_language%29">Mojo (programming language)</a></li>
<li><a href="https://mojolang.org/">Mojo - Modular</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters are cautiously hopeful but critical of the closed-source compiler, with some arguing that Python already has high-performance libraries like Pydantic backed by Rust. Others ask for a clearer one-page overview and express concern that Mojo has quietly walked back its goal of becoming a full Python superset.

**Tags**: `#Mojo`, `#AI`, `#programming language`, `#performance`, `#Python`

---

<a id="item-6"></a>
## [Nvidia&\#x27;s AI Dominance Faces Demand and Software Lock-In Risks](https://stratechery.com/2026/nvidias-risky-business/) ⭐️ 8.0/10

A Stratechery analysis argues that Nvidia&\#x27;s dominant position in AI compute is risky, questioning whether its growth is sustainable given deep CUDA software lock-in and potentially overblown expectations for AI demand growth. The piece has generated substantial community discussion, with 130 comments. Nvidia has become the central supplier of AI compute, and its market valuation depends on continued demand growth and its ability to maintain its ecosystem moat. If demand growth slows or competitors erode CUDA&\#x27;s lock-in, the impact would ripple across the entire AI industry, cloud providers, and investors. The analysis highlights CUDA, Nvidia&\#x27;s proprietary parallel computing platform, as both a strategic moat and a potential vulnerability due to its poor developer experience compared with modern alternatives. It also notes that first-order demand for compute is real, but second-order growth expectations are likely exaggerated, and points to Nvidia&\#x27;s expansion into robotics and the geopolitical split between the West and China.

hackernews · jonbaer · Aug 11, 10:02 · [Discussion](https://news.ycombinator.com/item?id=49255710)

**Background**: CUDA is a proprietary parallel computing platform and API introduced by Nvidia in 2007 that allows software to use GPUs for general-purpose processing, especially in AI, scientific computing, and high-performance computing. Nvidia&\#x27;s GPUs became the de facto standard for training and running large AI models, and CUDA&\#x27;s deep integration into machine learning frameworks created a powerful ecosystem lock-in that competitors have struggled to break.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nvidia_CUDA">Nvidia CUDA</a></li>
<li><a href="https://grokipedia.com/page/NVIDIA_CUDA">NVIDIA CUDA</a></li>

</ul>
</details>

**Discussion**: Commenters generally appreciated the nuanced take, with some arguing that Nvidia&\#x27;s real advantage is software entrenchment rather than raw hardware performance, while others criticized CUDA&\#x27;s developer experience as one of the worst ecosystems. Several agreed that demand for compute is real but that current growth expectations are likely exaggerated, and a few noted Nvidia&\#x27;s moves into robotics and the West-versus-China dynamic as additional factors.

**Tags**: `#Nvidia`, `#AI`, `#business strategy`, `#semiconductors`, `#CUDA`

---

<a id="item-7"></a>
## [London Underground expands live facial recognition trial, sparking privacy fears](https://www.btp.police.uk/news/btp/news/england/btp-expands-live-facial-recognition-lfr-trial-into-london-underground-stations/) ⭐️ 8.0/10

British Transport Police have expanded their live facial recognition \(LFR\) trial to London Underground stations, according to an announcement on their website. This extends the surveillance technology from earlier deployments into the capital&\#x27;s transit network. This expansion is significant because it brings live facial recognition into the daily commute of millions, normalizing biometric surveillance in public spaces. It raises urgent concerns about civil liberties, wrongful identification, and the erosion of anonymous travel. Live facial recognition works by scanning CCTV feeds and comparing facial feature measurements against a watchlist. However, accuracy can drop by 10–40% in real-world CCTV conditions due to lighting, angle, and resolution, which raises the risk of false positives.

hackernews · BlueBerry2001 · Aug 11, 09:40 · [Discussion](https://news.ycombinator.com/item?id=49255496)

**Background**: Live facial recognition is a biometric technology that maps facial landmarks, such as the distance between the eyes and jawline length, to create a unique &\#x27;faceprint&\#x27; for identification. UK police have been trialing it in public spaces, but critics warn it is prone to error and lacks legal safeguards. Additionally, travel on the London Underground has not been anonymous since contactless bank cards became the primary payment method, meaning some see facial recognition as a further step in an ongoing erosion of privacy rather than a sudden departure.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sciencefocus.com/future-technology/live-facial-recognition-how-is-it-used">Live facial recognition: how is it used? - BBC Science Focus ...</a></li>
<li><a href="https://www.technolynx.com/post/facial-recognition-video-surveillance-accuracy">Facial Recognition in Video Surveillance: Why Lab Accuracy Doesn’t Transfer to CCTV | TechnoLynx</a></li>

</ul>
</details>

**Discussion**: The discussion is overwhelmingly critical. Commenters argue the trial is pointless because there is no clear failure case, describe Britain as an &\#x27;Orwellian society,&\#x27; and sarcastically ask whether facial recognition will finally solve street crime. A recurring theme is that anonymity was already lost when contactless payment became standard, so this is &\#x27;boiling the frog&\#x27; slowly rather than a sudden shock.

**Tags**: `#facial recognition`, `#privacy`, `#surveillance`, `#civil liberties`, `#London`

---

<a id="item-8"></a>
## [Decoupled Descent Uses AMP Onsager Corrections to Certify Train-Test Error Match](https://www.reddit.com/r/MachineLearning/comments/1vlu1se/decoupled_descent_enforcing_exact_traintest_error/) ⭐️ 8.0/10

The paper introduces Decoupled Descent \(DD\), a training method that applies approximate message passing Onsager corrections to guarantee that training error asymptotically equals test error at each parameter iterate. It is validated on full-batch gradient descent for a stylized Gaussian mixture model, with simulations on a high-dimensional XOR model. This work targets the fundamental train-test generalization gap, a core challenge in training neural networks. If the theoretical guarantees hold, it could enable principled optimal stopping and hyperparameter tuning, and inspire new training algorithms beyond gradient descent. The method is theoretical, rooted in high-dimensional statistics, and the paper emphasizes it is a first step toward large-scale models. The author plans to release a PyTorch-compatible package, and the current experiments cover a two-layer network on a high-dimensional XOR model.

reddit · r/MachineLearning · /u/mlovik1 · Aug 11, 21:06

**Background**: Approximate message passing \(AMP\) is an iterative algorithm from high-dimensional statistics that uses Onsager correction terms to keep iterates statistically tractable, enabling precise performance prediction through state evolution. In AMP, the Onsager correction is a memory term that corrects for the dependence between the current signal estimate and the measurement matrix, ensuring that the error dynamics follow a predictable recursion. The paper applies these ideas to neural network training to mitigate the data reuse bias inherent in full-batch gradient descent.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2105.02180">A unifying tutorial on Approximate Message Passing</a></li>
<li><a href="https://www.emergentmind.com/topics/approximate-message-passing-amp-algorithms">Approximate Message Passing Algorithms</a></li>
<li><a href="https://www.stat.berkeley.edu/~songmei/Teaching/STAT260_Spring2021/Lecture_notes/scribe_lecture19.pdf">Approximate message passing algorithms</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#generalization`, `#approximate message passing`, `#optimization`, `#statistical theory`

---

<a id="item-9"></a>
## [Graphene-Powered Soft Lens Promises Compact Auto-Focusing](https://www.qmul.ac.uk/news/latest-news/2026/science-and-engineering/se/new-graphene-powered-soft-lens-could-pave-the-way-for-smarter-glasses-cameras-and-medical-devices.html) ⭐️ 8.0/10

Researchers at Queen Mary University of London have developed a transparent soft lens powered by reduced graphene oxide that changes focal length when an electric field is applied. The work, published in Advanced Functional Materials, eliminates the need for bulky moving parts in traditional lenses. This breakthrough could pave the way for compact auto-focusing systems in cameras, VR/AR headsets, and miniaturized medical imaging devices. By mimicking the human eye, it addresses a key bottleneck in adaptive optics and could accelerate the adoption of smart glasses and wearable displays. The team integrated ultra-thin transparent graphene electrodes directly into the actuator layer beneath the lens, overcoming the previous limitation where opaque electrodes could only be placed at the lens edge. The prototype still requires further optimization of electrode transparency and overall performance before commercialization.

telegram · zaihuapd · Aug 11, 12:27

**Background**: Graphene is a single layer of carbon atoms with exceptional electrical, optical, and mechanical properties. Reduced graphene oxide is a cost-effective derivative that bridges graphene&\#x27;s properties with practical applications, making it suitable for transparent electrodes and flexible devices. Adaptive lenses change focal length by altering shape or refractive index, typically using mechanisms such as fluid-filled chambers or liquid crystal pixels. This new approach uses an electric field to stretch a soft membrane, mimicking the focusing action of the human eye.

<details><summary>References</summary>
<ul>
<li><a href="https://powdernano.com/exploring-reduced-graphene-oxide-properties-applications-and-innovations/">Exploring Reduced Graphene Oxide : Properties , Applications , and...</a></li>
<li><a href="https://mojoglasses.com/how-do-adaptive-lenses-work/">How Do Adaptive Lenses Work? | Mojo Glasses</a></li>
<li><a href="https://manlykicks.com/blogs/knowledge/is-adaptive-eyewear-the-future-of-modern-vision">Is Adaptive Eyewear the Future of Modern Vision?</a></li>

</ul>
</details>

**Tags**: `#graphene`, `#optics`, `#adaptive lens`, `#VR/AR`, `#materials science`

---
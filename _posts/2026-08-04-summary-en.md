---
layout: default
title: "Horizon Summary: 2026-08-04 (EN)"
date: 2026-08-04
lang: en
---

> From 33 items, 11 important content pieces were selected

---

1. [Qwen Releases 3.8-Max: 2.4T Parameters, First Open-Source Max Model](#item-1) ⭐️ 9.0/10
2. [LLMs Amplify Existing Expertise Rather Than Replace It](#item-2) ⭐️ 8.0/10
3. [OpenAI Lists Ten AI-Powered Advances in Mathematics and CS](#item-3) ⭐️ 8.0/10
4. [Devtools must be open source so LLMs can modify them directly](#item-4) ⭐️ 8.0/10
5. [MiniMax H3 Day-0 Support in ComfyUI: Open Weights, Native Audio, 2K Video](#item-5) ⭐️ 8.0/10
6. [Andy Pavlo Joins ClickHouse to Launch ClickHouse Labs](#item-6) ⭐️ 8.0/10
7. [Jane Street&\#x27;s Bonsai Brings OCaml to Full-Stack Web Development](#item-7) ⭐️ 8.0/10
8. [Kimi K3 Architecture Analyzed: Memory, Depth Attention, Latent Experts](#item-8) ⭐️ 8.0/10
9. [DNA Device Flaw Exposes 30 Years of Crime Evidence to Tampering](#item-9) ⭐️ 8.0/10
10. [Nvidia CMP 170HX miners cracked to unlock 80GB memory, prices surge](#item-10) ⭐️ 8.0/10
11. [Apple Sues UK Government Over iCloud Backdoor Demand](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen Releases 3.8-Max: 2.4T Parameters, First Open-Source Max Model](https://qwen.ai/blog?id=qwen3.8) ⭐️ 9.0/10

Qwen released Qwen 3.8-Max, a 2.4-trillion-parameter Mixture-of-Experts model with 95 billion active parameters, and announced that model weights will be open-sourced next week — the first time Qwen has opened a Max-level model. This marks a major milestone in open-source AI, as Qwen&\#x27;s largest and most capable model becomes accessible to the community. It could significantly boost research and development around MoE architectures and ultra-large-scale inference. Built on the Qwen 3.5 architecture, the model excels in coding, work, research, and long-horizon tasks. In a coding test it ran autonomously for over 10 days, and it beat 458 of 526 teams in the WWW2025 multimodal conversation intent recognition competition; API access is already available via QwenCloud.

telegram · zaihuapd · Aug 3, 02:31

**Background**: Qwen 3.8-Max uses a Mixture-of-Experts \(MoE\) architecture, which scales up total parameter count while keeping computation efficient by activating only a subset of parameters per token. In MoE models, total parameters represent the full knowledge capacity, while active parameters determine the compute cost per inference step. This approach has become a standard for state-of-the-art large language models.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://medium.com/@csburakkilic/understanding-moe-architectures-the-difference-between-total-and-active-parameters-ad1d161fccaa">Understanding MoE Architectures: The Difference Between Total and Active Parameters | by Burak Kılıç | Medium</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Qwen`, `#open-source`, `#large language model`, `#model release`

---

<a id="item-2"></a>
## [LLMs Amplify Existing Expertise Rather Than Replace It](https://www.seangoedecke.com/llms-reward-expertise/) ⭐️ 8.0/10

In his essay &\#x27;LLMs reward expertise&\#x27;, Sean Gedecke argues that large language models provide disproportionate productivity gains to domain experts, while offering limited benefit to novices without the same background knowledge. This challenges the popular narrative that AI will democratize expertise or make individual expertise less valuable. It suggests that organizations and professionals should focus on cultivating deep knowledge to maximize the benefits of LLMs, and that AI could widen the productivity gap between experts and novices. The article&\#x27;s argument centers on experts&\#x27; ability to evaluate, question, and steer LLM outputs, which novices lack. Commenters also note that &\#x27;signalling expertise&\#x27; in prompts can significantly change the quality of responses, and that using LLMs as an extension of one&\#x27;s mind works better than using them as a replacement.

hackernews · MaxMussio · Aug 3, 21:13 · [Discussion](https://news.ycombinator.com/item?id=49161518)

**Background**: Large language models \(LLMs\) are AI systems trained on vast text data to generate human-like text. A common assumption is that these tools could eventually replace human experts in fields like coding, writing, or research. This essay pushes back, arguing that the ability to judge the output — knowing what is correct, relevant, or good — is exactly where domain expertise matters, so LLMs act as a force multiplier for those who already have it.

**Discussion**: Community reaction largely agrees with the essay&\#x27;s thesis, using analogies like an &\#x27;amplifying mirror&\#x27; and emphasizing that LLMs reflect the user&\#x27;s own expertise and care. Some commenters warn that taking AI&\#x27;s effectiveness for granted could cause a generation of domain experts to be lost, and that hands-on familiarity with a codebase remains essential even when general knowledge is strong.

**Tags**: `#LLMs`, `#expertise`, `#AI`, `#software engineering`, `#productivity`

---

<a id="item-3"></a>
## [OpenAI Lists Ten AI-Powered Advances in Mathematics and CS](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 8.0/10

OpenAI published an article enumerating ten recent advances in mathematics and theoretical computer science enabled by AI, showcasing concrete results where AI contributed to proofs and discoveries. The post underscores AI&\#x27;s growing, measurable impact on mathematical research, where tools like LLMs are moving from novelties to essential instruments. It has generated substantial community debate about whether AI progress is following an exponential curve and which fields will be transformed next. The full list is not reproduced in the summary, but commenters point to problems including high-dimensional sphere packing and multicolor Ramsey numbers. The announcements connect to recent breakthroughs such as OpenAI&\#x27;s disproof of the unit distance conjecture and the proof of Erdős problem 1196.

hackernews · milkshakes · Aug 3, 16:27 · [Discussion](https://news.ycombinator.com/item?id=49157930)

**Background**: Automated theorem proving \(ATP\) is a subfield that uses computer programs to prove mathematical theorems, with roots in early computer science. Proof assistants such as Lean and Coq support human–machine collaboration to develop formal proofs. Increasingly, large language models are being used to suggest conjectures and search for proofs, enabling discoveries like solving long-standing problems or disproving conjectures. AI is thus becoming a &\#x27;centaur&\#x27; partner for mathematicians, combining machine search with human insight.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automated_theorem_proving">Automated theorem proving</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>
<li><a href="https://scitechdaily.com/ai-helps-crack-an-87-year-old-math-conjecture-with-one-tiny-formula/">AI Helps Crack an 87-Year-Old Math Conjecture With One Tiny Formula</a></li>

</ul>
</details>

**Discussion**: Overall sentiment is enthusiastic but tempered: commenters note that AI can handle grinding, case-checking labor that humans cannot, though it still lacks the intuition to generate conjectures. Some see a y=2^x exponential trend and ask which fields will resist it, while others point to specific problems in OpenAI&\#x27;s list as surprisingly intuitive.

**Tags**: `#AI`, `#mathematics`, `#theoretical computer science`, `#OpenAI`, `#research`

---

<a id="item-4"></a>
## [Devtools must be open source so LLMs can modify them directly](https://blog.exe.dev/devtools-must-be-open-source) ⭐️ 8.0/10

A new blog post from exe.dev argues that developer tools must be open source so LLMs can directly modify their code, eliminating the need for configuration systems. The post has sparked a lively community debate. It challenges a core assumption in tool design and proposes that AI coding agents replace configuration with direct source modification. If adopted, it could shift how devtools are built, maintained, and forked, affecting developers and maintainers across the ecosystem. The article reportedly proposes setting up a nightly cron job that fetches upstream changes and rebases local AI-generated modifications, checking that the software still works. Community commenters point out this is unreliable, wasteful, and underestimates the maintenance burden of downstream forks.

hackernews · bryanmikaelian · Aug 3, 14:15 · [Discussion](https://news.ycombinator.com/item?id=49156111)

**Background**: The post contends that traditional config systems are a workaround because users cannot easily change the behavior of closed-source tools. With LLMs able to read and modify source code, making devtools open source would let users directly edit the program and eliminate configuration layers. This idea draws on long-standing open-source ideals but faces practical questions about maintenance and efficiency.

**Discussion**: Commenters largely agree devtools should be open source but dispute the radical conclusion. simonw notes LLMs make the original open-source dream more feasible, while kelnos and theamk argue that replacing configuration with AI rebuilding is inefficient and unreliable; lalitmaganti, a maintainer of a devtool, warns the approach is too idealistic because engineers just want tools that work.

**Tags**: `#open-source`, `#devtools`, `#LLM`, `#software-engineering`

---

<a id="item-5"></a>
## [MiniMax H3 Day-0 Support in ComfyUI: Open Weights, Native Audio, 2K Video](https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui) ⭐️ 8.0/10

ComfyUI announced Day-0 support for MiniMax H3, a new open-weights multimodal video model that accepts text, images, video, and audio inputs and generates video with native stereo sound, up to 2K resolution and 15 seconds per clip. This release lets creators run a next-generation open-weights video model locally in ComfyUI immediately, with native audio generation and 2K output. The strong community response shows it could significantly impact AI media generation workflows. According to the model card, roughly 40% of the model&\#x27;s parameters \(modulation weights\) can be pruned and replaced with a lookup table, cutting total memory from 123.6 GB to 42.5 GB with no quality loss. Users report that a 10-second 480p video takes about 10 minutes on an RTX 4070 Ti Super.

hackernews · vblanco · Aug 3, 13:34 · [Discussion](https://news.ycombinator.com/item?id=49155629)

**Background**: MiniMax H3 is a family of open-weights multimodal video models that support text-to-video, image-to-video, and frame-to-frame generation. ComfyUI is a popular node-based interface for building AI image and video pipelines. Day-0 support means MiniMax H3 is natively integrated into ComfyUI on the same day it was released, allowing users to load the model and run it locally.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui">MiniMax H3 Day - 0 Support in ComfyUI : Open Weights, Native Audio...</a></li>
<li><a href="https://huggingface.co/Comfy-Org/MiniMax-H3">Comfy-Org/ MiniMax - H 3 · Hugging Face</a></li>
<li><a href="https://hailuoai.video/tools/minimax-h3">MiniMax H 3 Multimodal AI Video Model | Hailuo AI</a></li>

</ul>
</details>

**Discussion**: Community comments are largely enthusiastic but raise technical questions. One user questions whether pruning 40% of weights truly yields &quot;no loss in output quality&quot; and whether the approach could apply to LLMs. Other users share performance reports, praising overall quality but noting jank in unusual scenarios and a lingering &quot;AI smoothing&quot; effect in some clips.

**Tags**: `#ComfyUI`, `#MiniMax H3`, `#AI video generation`, `#Open weights`, `#Text-to-video`

---

<a id="item-6"></a>
## [Andy Pavlo Joins ClickHouse to Launch ClickHouse Labs](https://clickhouse.com/blog/andy-pavlo-joins-clickhouse) ⭐️ 8.0/10

Andy Pavlo, a prominent database researcher, has joined ClickHouse as VP of Database Research to establish and lead ClickHouse Labs, a new research group. The launch was announced on August 3, 2026. This move bridges academic database research and industry practice, signaling ClickHouse&\#x27;s significant investment in long-term research. It could influence the future direction of OLAP database architecture and inspire more industry-academia collaboration. ClickHouse Labs will be led by Pavlo, who is known for his work on database systems and the popular &\#x27;Database Systems&\#x27; course at Carnegie Mellon. The group will focus on database research, with plans to bridge academic findings into ClickHouse&\#x27;s open-source OLAP engine.

hackernews · nikolay\_sivko · Aug 3, 14:09 · [Discussion](https://news.ycombinator.com/item?id=49156011)

**Background**: ClickHouse is an open-source, column-oriented DBMS designed for online analytical processing \(OLAP\) of large datasets. By creating a dedicated research lab, ClickHouse aims to explore new database technologies and maintain its edge in a competitive OLAP market.

<details><summary>References</summary>
<ul>
<li><a href="https://clickhouse.com/blog/andy-pavlo-founding-clickhouse-labs">ClickHouse launches ClickHouse Labs with Andy Pavlo as VP of Database Research | ClickHouse</a></li>
<li><a href="https://www.businesswire.com/news/home/20260803890510/en/ClickHouse-Launches-ClickHouse-Labs-With-Andy-Pavlo-as-VP-of-Database-Research">ClickHouse Launches ClickHouse Labs With Andy Pavlo as VP of Database Research</a></li>
<li><a href="https://en.wikipedia.org/wiki/ClickHouse">ClickHouse - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters welcomed the news, with several expressing hope that ClickHouse will fund academic database research amid declining government support. Some also speculated about convergence trends among fast OLAP products, and one commenter praised Pavlo&\#x27;s CMU lectures and the inspiration they provided.

**Tags**: `#ClickHouse`, `#database research`, `#Andy Pavlo`, `#OLAP`, `#industry news`

---

<a id="item-7"></a>
## [Jane Street&\#x27;s Bonsai Brings OCaml to Full-Stack Web Development](https://github.com/janestreet/bonsai) ⭐️ 8.0/10

Jane Street&\#x27;s Bonsai, a UI library for building reactive web applications in OCaml, has drawn significant community attention for enabling shared types between backend and frontend. It is currently available publicly on GitHub. Bonsai matters because it lets OCaml developers write full-stack applications with the same language and types, reducing boilerplate and increasing type safety. It also represents a notable production-grade UI framework from a major financial technology firm, potentially influencing OCaml&\#x27;s adoption in web development. Bonsai is partly inspired by Elm and is designed for building reusable UI components within Incremental-style frameworks such as Incr\_dom or React. At Jane Street, it has been used to build many internal web applications, including tools that interact with trading systems.

hackernews · KolmogorovComp · Aug 3, 08:29 · [Discussion](https://news.ycombinator.com/item?id=49152842)

**Background**: Bonsai is an OCaml library from Jane Street, a quantitative trading firm known for using OCaml extensively. Many of Jane Street&\#x27;s internal systems previously had only terminal UIs, and Bonsai made it easier to port existing typed business logic to the web. The library supports reactive programming and helps developers build dynamic web apps with OCaml&\#x27;s strong type system.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/janestreet/bonsai">GitHub - janestreet / bonsai : A library for building dynamic webapps...</a></li>
<li><a href="https://en.mycoding.id/bonsai-janestreet-s-ui-library-57684.html">Bonsai : Janestreet &#x27;s Ui Library</a></li>
<li><a href="https://opam.ocaml.org/packages/bonsai/">opam - bonsai</a></li>

</ul>
</details>

**Discussion**: Community sentiment is cautiously positive. Some developers ask about real-world production adoption beyond Jane Street, while others are excited about sharing types across frontend and backend. There is also discussion comparing Bonsai to Melange, and some criticism of its default aesthetics, though performance is acknowledged.

**Tags**: `#OCaml`, `#UI`, `#Jane Street`, `#Frontend`, `#Functional Programming`

---

<a id="item-8"></a>
## [Kimi K3 Architecture Analyzed: Memory, Depth Attention, Latent Experts](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

SemiAnalysis published a deep-dive analysis of Kimi K3, focusing on its compressed memory, attention across depth, latent expert routing, and inference performance. The article details how these architectural components differ from previous large language model designs. Kimi K3 combines memory compression, depth-wise attention, and latent expert routing in a way that could substantially improve long-context handling and inference efficiency. This analysis from a respected source gives AI researchers and systems engineers a rare technical look at a cutting-edge production model. The architecture uses compressed memory similar to Compressive Transformers, which compress older activations instead of discarding them, extending effective context length. It also implements attention across model depth \(analogous to attention residuals\) and employs latent expert routing that makes expert selection decisions in a low-dimensional latent space.

rss · Semianalysis · Aug 3, 19:42

**Background**: Compressed memory, introduced in Compressive Transformers, extends the cache of past hidden states by applying a learned compression operation to activations that would otherwise be evicted, allowing the model to attend over a much longer history. Attention across depth, sometimes called attention residuals, lets attention heads read representations from previous layers in addition to the current layer, enabling information flow along the network&\#x27;s depth rather than only across token positions. Latent expert routing, such as Mixture of Latent Experts \(MoLE\), keeps routing decisions in a low-dimensional latent space, improving expert selection efficiency and scalability in large Mixture-of-Experts models.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/1911.05507">COMPRESSIVE TRANSFORMERS FOR LONG-RANGE SEQUENCE MODELLING Jack W. Rae∗∗† ‡</a></li>
<li><a href="https://sebastianraschka.com/llm-architecture-gallery/attention-residuals/">Attention Residuals (AttnRes) | Sebastian Raschka, PhD</a></li>
<li><a href="https://www.emergentmind.com/topics/mixture-of-latent-experts-mole">Mixture of Latent Experts (MoLE)</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Model Architecture`, `#Inference`, `#Machine Learning`, `#Kimi K3`

---

<a id="item-9"></a>
## [DNA Device Flaw Exposes 30 Years of Crime Evidence to Tampering](https://www.wsj.com/tech/cybersecurity/security-flaw-placed-30-years-of-dna-evidence-at-risk-of-hacking-1932775a) ⭐️ 8.0/10

Researchers discovered a critical vulnerability in DNA analysis machines used by most U.S. crime labs, allowing undetectable modification of DNA scan data. Thermo Fisher Scientific acknowledged the flaw in July and released a security advisory and a software update with digital signatures last Friday. This flaw could allow attackers to tamper with forensic DNA evidence dating back to 1995, potentially affecting criminal investigations and convictions. It also underscores the inconsistent cybersecurity protections across more than 200 U.S. crime labs, which lack unified regulation. Using AI-generated code from Anthropic&\#x27;s Claude, the researchers altered DNA scan files in about 45 minutes, and the modified files did not trigger alerts in commonly used analysis software. Thermo Fisher stated no real-world exploitation has been reported, and it is coordinating with the U.S. Cybersecurity and Infrastructure Security Agency \(CISA\).

telegram · zaihuapd · Aug 3, 05:15

**Background**: DNA analysis devices, such as genetic analyzers, are used in forensic laboratories to generate DNA profiles from crime-scene samples, producing data files that specialized software interprets for matches. Digital signatures are based on asymmetric cryptography, allowing a receiver to verify that a file has not been altered since it was signed. The vulnerability affected how these instruments handle data files, making tampering possible if laboratory access controls are bypassed.

<details><summary>References</summary>
<ul>
<li><a href="https://ip.net.coffee/claude/news/20260803b.html">美犯罪实验室 DNA 设 备 曝漏洞：30...</a></li>
<li><a href="https://aiplus.360.cn/cjwt/5305.html">数字签名：保证数据安全的关键技术 - 360亿方智能</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#DNA analysis`, `#forensics`, `#vulnerability`, `#Thermo Fisher`

---

<a id="item-10"></a>
## [Nvidia CMP 170HX miners cracked to unlock 80GB memory, prices surge](https://finance.sina.com.cn/tech/roll/2026-08-03/doc-inikzqsf4659769.shtml) ⭐️ 8.0/10

Researchers at Arizona State University publicly released a method to crack Nvidia CMP 170HX mining cards, exploiting a stack overflow in the Falcon security coprocessor to bypass OTP fuse locks. The hack unlocks up to 80GB of memory and boosts FP32 performance from 0.39 TFLOPS to 94 TFLOPS, causing second-hand prices to soar. This is significant because it turns a heavily restricted mining card into a cheap AI compute option, threatening Nvidia&\#x27;s product segmentation strategy and affecting the market for affordable AI hardware. It also highlights security weaknesses in Nvidia&\#x27;s GPU protection mechanisms. The CMP 170HX uses the same GA100 die as the A100, but with 4480 CUDA cores and 8GB HBM2e factory-limited by OTP fuses. The exploit uses a DMA unbounded overflow in the Falcon coprocessor to hijack privileges; community tests show unlocked cards can run AI image generation and LLM inference on Windows and Linux, though stability and per-batch unlock limits remain uncertain.

telegram · zaihuapd · Aug 3, 11:29

**Background**: The CMP 170HX is a cryptocurrency mining card released by Nvidia in 2021, based on a cut-down GA100 GPU with a massive heatsink and no active cooling, originally priced around $5000. Nvidia uses OTP fuses to permanently lock down hardware features like compute and memory, and Falcon coprocessors embedded in GPUs are designed to prevent misprogramming. These constraints were previously considered irreversible, making this exploit notable.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techpowerup.com/289310/nvidia-cmp-170hx-mining-card-tested-based-on-ga100-gpu-sku">NVIDIA CMP 170HX Mining Card Tested, Based on GA100 GPU SKU | TechPowerUp</a></li>
<li><a href="https://videocardz.com/newz/nvidia-cmp-170hx-mining-card-with-ga100-gpu-has-a-massive-heatspreader">NVIDIA CMP 170HX mining card with GA100 GPU has a massive heatspreader - VideoCardz.com</a></li>
<li><a href="https://download.nvidia.com/open-gpu-doc/Falcon-Security/1/Falcon-Security.html">NVIDIA Falcon Security</a></li>

</ul>
</details>

**Discussion**: Community sentiment is largely enthusiastic, with users validating the unlock on live systems and noting the huge price-performance improvement for AI workloads. Some express concerns about long-term reliability, potential Nvidia countermeasures, and variability in unlock success across different card batches. No official comments are included in the news item.

**Tags**: `#hardware`, `#security`, `#Nvidia`, `#AI computing`, `#exploit`

---

<a id="item-11"></a>
## [Apple Sues UK Government Over iCloud Backdoor Demand](https://www.ft.com/content/2cc9c96a-0e5b-4c33-a95a-3d11072a145c?syn-25a6b1a6=1) ⭐️ 8.0/10

Apple has filed a legal challenge with the UK&\#x27;s Investigatory Powers Tribunal against the government&\#x27;s Technical Capability Notice, which would require Apple to provide access to encrypted iCloud backups of UK users. This case tests the UK government&\#x27;s power to compel technology companies to weaken encryption, with significant implications for global privacy, security, and the future of end-to-end encryption. The ruling could set a precedent for how democratic governments balance law enforcement needs against user privacy. Apple withdrew iCloud Advanced Data Protection \(end-to-end encryption\) for UK users in February 2025, after an earlier demand affecting UK and US users was withdrawn and replaced with a notice targeting only UK users. Privacy International and Liberty have also challenged the TCN, and the tribunal has scheduled a case management hearing for next month.

telegram · zaihuapd · Aug 3, 15:40

**Background**: The Technical Capability Notice is a legal instrument under the UK&\#x27;s Investigatory Powers Act 2016, which allows the Home Secretary to impose obligations on operators to assist with interception of communications. The Investigatory Powers Tribunal is a UK court that hears complaints about surveillance by public bodies. Apple&\#x27;s Advanced Data Protection is an optional iCloud feature that encrypts data end-to-end, so even Apple lacks the keys to decrypt it.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Technical_capability_notice">Technical capability notice</a></li>
<li><a href="https://en.wikipedia.org/wiki/Investigatory_Powers_Tribunal">Investigatory Powers Tribunal</a></li>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#encryption`, `#privacy`, `#UK law`, `#iCloud`

---
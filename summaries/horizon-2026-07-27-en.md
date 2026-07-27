# Horizon Daily - 2026-07-27

> From 33 items, 15 important content pieces were selected

---

1. [vLLM v0.26.0: Inkling support, DeepSeek-V4 tuning, fp32 lm\_head](#item-1) ⭐️ 9.0/10
2. [Moonshot AI Releases Kimi-K3, 3T MoE Model](#item-2) ⭐️ 9.0/10
3. [Fastjson2 RCE Vulnerability Disclosed, No Patch Available](#item-3) ⭐️ 9.0/10
4. [PGSimCity: 3D Interactive Visualization of PostgreSQL Internals](#item-4) ⭐️ 8.0/10
5. [US citizen charged after duress PIN wipes GrapheneOS phone at border](#item-5) ⭐️ 8.0/10
6. [Proof Automation Goes Practical with Verified zstd Decoder](#item-6) ⭐️ 8.0/10
7. [Data-Oriented Design PDF Sparks Community Debate](#item-7) ⭐️ 8.0/10
8. [EU Proposes Browser-Level Privacy to Kill Cookie Banners](#item-8) ⭐️ 8.0/10
9. [Token Relay Market Drives AI Fraud and Abuse](#item-9) ⭐️ 8.0/10
10. [Small 4B open-weight models rival o3 on Swedish medical QA](#item-10) ⭐️ 8.0/10
11. [Claude shared links leak user data via search engine indexing](#item-11) ⭐️ 8.0/10
12. [SpaceX Rejects Future Falcon 9 Orders, Bets Big on Starship](#item-12) ⭐️ 8.0/10
13. [Huawei Reportedly Building DRAM Fab with 140k Monthly Wafer Capacity](#item-13) ⭐️ 8.0/10
14. [Google reveals Gemini 4 as its most ambitious pretraining project](#item-14) ⭐️ 8.0/10
15. [Alibaba Launches Qianwen Office AI with Computer Control](#item-15) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0: Inkling support, DeepSeek-V4 tuning, fp32 lm\_head](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 was released with 411 commits from 212 contributors, adding full support for the Inkling model family, significant DeepSeek-V4 performance optimizations \(including a specialized routing kernel and fused\_topk\_bias\), and fp32 lm\_head support via the new head\_dtype option. This release expands vLLM&\#x27;s model ecosystem to include the emerging Inkling open-weights family and delivers substantial throughput gains for DeepSeek-V4, which is widely used in production. The fp32 lm\_head feature improves generation accuracy for models that require higher precision in the language modeling head. Inkling support includes piecewise CUDA graphs, Hopper FA4 relative attention, MTP=1 speculative decoding, LoRA, and NVFP4 quantization. DeepSeek-V4 improvements involve a 2.94% E2E TPOT gain from a routing kernel and 1.5–2x speedup in fused\_topk\_bias. The fp32 lm\_head is extended to LoRA and has a fast ROCm path.

github · khluu · Jul 27, 01:06

**Background**: vLLM is an open-source high-throughput LLM inference engine designed for production use. Inkling is a new open-weights multimodal model family from Thinking Machines Lab that supports text, image, and audio inputs. Flash Attention 4 \(FA4\) is a GPU kernel that optimizes attention computation for Hopper architectures \(e.g., H100, H200\). NVFP4 is a 4-bit floating-point quantization format introduced with NVIDIA Blackwell GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/model-card/inkling/">Inkling Model Card - Thinking Machines Lab</a></li>
<li><a href="https://arxiv.org/html/2603.05451v1">FlashAttention-4: Algorithm and Kernel Pipelining Co-Design for Asymmetric Hardware Scaling</a></li>
<li><a href="https://build.nvidia.com/spark/nvfp4-quantization">NVFP4 Quantization | DGX Spark</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#DeepSeek`, `#performance optimization`, `#model serving`

---

<a id="item-2"></a>
## [Moonshot AI Releases Kimi-K3, 3T MoE Model](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 9.0/10

On July 27, 2026, Moonshot AI open-sourced Kimi-K3 on HuggingFace, a 3-trillion-parameter Mixture-of-Experts model with native mxfp4 precision. It is the first open-weight model in the 3T class. Kimi-K3 sets a new scale for open-weight models, potentially driving down inference costs through competition, as seen with earlier models like GLM-5.2. It also pressures major players like Meta to deliver competitive open-weight alternatives. The model requires approximately 1.5 TB of VRAM for hosting due to its mxfp4 format, pushing the limit of eight NVIDIA B200 GPUs \(16 for optimization\). It is a data-center-class model, not suitable for individual or small-scale deployment.

hackernews · nateb2022 · Jul 27, 06:18 · [Discussion](https://news.ycombinator.com/item?id=49065752)

**Background**: Mixture-of-Experts \(MoE\) is an architecture that divides a model into specialized sub-networks \(experts\), activating only a subset per input to improve efficiency. This allows Kimi-K3 to achieve the knowledge capacity of a dense 3T model while keeping inference costs closer to a much smaller model. Moonshot AI claims Kimi-K3 is the world&\#x27;s first open-source model in the 3-trillion-parameter class, released on July 27, 2026.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://localaihandbook.com/resources/kimi-k3-open-model-local-ai/">Kimi K3: What the World&#x27;s First Open 3 - Trillion - Parameter Model ...</a></li>
<li><a href="https://officeforge.co/blog/kimi-k3-open-weight-frontier">Kimi K 3 : First Open 3 T-Class Model Arrives for AI Teams | OfficeForge</a></li>

</ul>
</details>

**Discussion**: Community members are focused on the model&\#x27;s hosting cost and VRAM requirements, with one user estimating 1.5 TB VRAM and noting that 16 B200s would be needed for practical use. Others discuss how competition from Kimi-K3 could further drive down API prices, referencing the 45% drop for GLM-5.2 over 1.5 months. There is also speculation about when the model might be fully &quot;decensored&quot; and what risks that could bring.

**Tags**: `#LLM`, `#Model Release`, `#MoE`, `#HuggingFace`, `#AI Infrastructure`

---

<a id="item-3"></a>
## [Fastjson2 RCE Vulnerability Disclosed, No Patch Available](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

On July 27, Chaitin Tech disclosed a remote code execution vulnerability in Fastjson2 affecting all versions up to 2.0.62, allowing attackers to bypass AutoType checks via malicious JSON. The project maintainers have confirmed the issue, but no official patch has been released. This critical vulnerability in a widely-used Java JSON library poses a severe risk to countless applications, particularly those relying on default AutoType settings. With no fix yet available, users must disable AutoType or implement workarounds, which may break legitimate functionality. The vulnerability is similar to previous Fastjson deserialization attacks, and while full exploit details are not yet public, it is considered highly exploitable. The maintainers closed a related pull request \(PR \#7695\) without merging it into the main branch, leaving all released versions unpatched.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson2 is a popular JSON parsing library for Java, widely used in Alibaba&\#x27;s ecosystem and beyond. AutoType is a feature that allows dynamic class binding during deserialization, which has been a frequent target for remote code execution vulnerabilities. Similar flaws in the earlier Fastjson 1.x series \(e.g., CVE-2022-25845, CVE-2026-16723\) have been patched, but the Fastjson2 lineage remains vulnerable.

<details><summary>References</summary>
<ul>
<li><a href="https://jfrog.com/blog/cve-2022-25845-analyzing-the-fastjson-auto-type-bypass-rce-vulnerability/">CVE-2022-25845 - Fastjson RCE vulnerability analysis</a></li>
<li><a href="https://medium.com/@knownsec404team/fastjson-deserialization-vulnerability-history-5206714ceed1">Fastjson Deserialization Vulnerability History | by Knownsec 404 team | Medium</a></li>
<li><a href="https://github.com/alibaba/fastjson2/wiki/Security-Advisory:-Remote-Code-Execution-in-fastjson-1.2.68%E2%80%931.2.83">Security Advisory: Remote Code Execution in fastjson 1.2.68–1 ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#fastjson2`, `#rce`, `#java`

---

<a id="item-4"></a>
## [PGSimCity: 3D Interactive Visualization of PostgreSQL Internals](https://nikolays.github.io/PGSimCity/) ⭐️ 8.0/10

PGSimCity is an explorable 3D city that animates how PostgreSQL works, including processes like query parsing, planning, execution, and buffer pool management. It was released as an open-source tool on GitHub, allowing users to interactively explore database internals. This tool makes complex database internals accessible to developers and students, bridging the gap between abstract architecture diagrams and real-time system behavior. Its interactive approach could inspire similar educational visualizations for other systems like Kubernetes or cloud computing. The visualization is built with Three.js and runs in the browser, showing PostgreSQL components as buildings and processes as moving entities. It currently includes a guided tour mode but lacks a custom query input feature, which has been a common user request.

hackernews · jonbaer · Jul 27, 00:19 · [Discussion](https://news.ycombinator.com/item?id=49063754)

**Background**: PostgreSQL is a relational database with a complex client-server architecture involving parsers, planners, executors, and a shared buffer pool. Understanding these internals is crucial for performance tuning and debugging, but traditional documentation often relies on static diagrams. PGSimCity provides a dynamic, 3D representation of these components in action.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/NikolayS/PGSimCity">GitHub - NikolayS/PGSimCity: An explorable 3D city that shows how Postgres actually works · GitHub</a></li>
<li><a href="https://blog.algomaster.io/p/postgresql-internal-architecture">How PostgreSQL Works: Internal Architecture Explained</a></li>
<li><a href="https://www.postgresql.org/docs/current/overview.html">PostgreSQL: Documentation: 18: Chapter 51. Overview of ...</a></li>

</ul>
</details>

**Discussion**: The community response is largely positive, with users praising the innovative approach to teaching database internals. However, feedback highlights that the guided tour can be overwhelming due to rapid visual changes, and many users wish for an interactive mode where they could input custom queries to see step-by-step processing. Some commenters also raised concerns about the accuracy of the simulation, given it was built quickly using vibe-coding techniques.

**Tags**: `#PostgreSQL`, `#visualization`, `#educational tool`, `#database internals`

---

<a id="item-5"></a>
## [US citizen charged after duress PIN wipes GrapheneOS phone at border](https://www.techspot.com/news/113236-us-prosecutors-charge-atlanta-man-after-grapheneos-phone.html) ⭐️ 8.0/10

A US citizen was charged after his GrapheneOS phone wiped itself when he entered a duress PIN during a search by US border agents. The incident occurred at an airport, where the duress PIN triggered an irreversible device wipe. This case highlights the legal risks of using duress PIN features at borders, where destroying data may lead to obstruction charges. It underscores the tension between privacy-enhancing tools and government search powers at ports of entry. GrapheneOS&\#x27;s duress PIN feature irreversibly wipes the device and any installed eSIMs when entered. The defendant reportedly used this feature during a border search, leading to federal charges for obstruction or destruction of evidence.

hackernews · eecc · Jul 26, 22:21 · [Discussion](https://news.ycombinator.com/item?id=49063022)

**Background**: GrapheneOS is an open-source, security-hardened mobile OS based on Android, designed for privacy and security. It offers a duress PIN that, when entered, instantly wipes the device to protect data in coercive situations. U.S. border patrol agents have broad authority to search electronic devices, and intentionally destroying evidence can be charged as obstruction of justice.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS</a></li>
<li><a href="https://discuss.grapheneos.org/d/14722-using-duress-password-example">Using duress password example - GrapheneOS Discussion Forum</a></li>
<li><a href="https://www.androidauthority.com/grapheneos-duress-pin-3584795/">I use a duress PIN to protect my data — here’s how it works</a></li>

</ul>
</details>

**Discussion**: Comments on the article debate the threat model, with some noting that border agents have enormous power and that intent matters in law. Others argue that users must accept legal consequences when choosing to use duress features. Suggestions include decoy OS approaches like VeraCrypt&\#x27;s hidden volumes to avoid triggering wipe in plain sight.

**Tags**: `#GrapheneOS`, `#border search`, `#phone security`, `#privacy`, `#legal`

---

<a id="item-6"></a>
## [Proof Automation Goes Practical with Verified zstd Decoder](https://www.imperialviolet.org/2026/07/26/zstd-lean.html) ⭐️ 8.0/10

Adam Langley \(ImperialViolet\) published an experiment on July 26, 2026, implementing a complete Zstandard decoder in Lean, with formal proofs generated by several large language models in about 20 minutes. This demonstrates that proof automation can drastically reduce the cost of formal verification, potentially making it practical for real-world security-critical software like compression decoders. The author noted that traditional formal verification is roughly 20 times more expensive than conventional development, but LLM-assisted proof generation lowered the effort significantly. The experiment used Lean, a proof assistant with dependent types, and the proofs covered a full zstd decoder.

hackernews · zdw · Jul 26, 20:53 · [Discussion](https://news.ycombinator.com/item?id=49062291)

**Background**: Formal verification uses mathematical proofs to ensure software correctness, but has historically been too expensive for most projects. Proof automation aims to reduce this cost using tools like theorem provers and, more recently, large language models. Lean is an interactive theorem prover that can encode complex properties, and its dependently typed system allows expressing and verifying invariants directly in code.

<details><summary>References</summary>
<ul>
<li><a href="https://www.remio.ai/post/lean-proof-automation-just-crossed-from-research-into-real-software">Lean Proof Automation Just Crossed From Research Into Real...</a></li>
<li><a href="https://elsolitario.org/en/2026/07/26/lean-llm-formal-proofs-zstd/">LLMs Test Code in Lean: How a zstd Decoder Was Verified</a></li>

</ul>
</details>

**Discussion**: Commenters debated the trade-offs: some highlighted the high cost of formal verification \(20x\) and questioned whether LLMs can handle scaling; others voiced concerns about maintenance burden of dependent types. However, there was optimism that embedding theorem provers in programming languages, combined with LLMs, could reduce the need for traditional testing.

**Tags**: `#formal verification`, `#proof automation`, `#compression`, `#software reliability`, `#dependent types`

---

<a id="item-7"></a>
## [Data-Oriented Design PDF Sparks Community Debate](https://www.gamedevs.org/uploads/introduction-to-data-oriented-design.pdf) ⭐️ 8.0/10

A seminal PDF presentation by Mike Acton on data-oriented design \(DoD\) for performance-critical software is gaining renewed attention in the game development community. DoD is a key paradigm shift from object-oriented programming, focusing on CPU cache efficiency and data layout, which can greatly improve performance in games and real-time systems. The PDF emphasizes designing algorithms by analyzing data flow and using structures of arrays \(SoA\) rather than arrays of structures \(AoS\). Mike Acton has also released an LLM skill for data-oriented programming.

hackernews · tosh · Jul 26, 18:11 · [Discussion](https://news.ycombinator.com/item?id=49060724)

**Background**: Data-oriented design \(DoD\) is an optimization approach motivated by efficient CPU cache usage, often used in video game development. It contrasts with object-oriented design by prioritizing data layout and transformations over abstractions. The main example is using parallel arrays \(SoA\) to improve cache locality.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Data-oriented_design">Data-oriented design</a></li>
<li><a href="https://www.dataorienteddesign.com/dodmain/">Richard Fabian - Data-oriented design</a></li>
<li><a href="https://github.com/dbartolini/data-oriented-design">GitHub - dbartolini/data-oriented-design: A curated list of data oriented design resources. · GitHub</a></li>

</ul>
</details>

**Discussion**: Comments show mixed sentiments: some praise the approach for performance gains, while others question its practicality in dynamic project environments with changing requirements. A comment notes Mike Acton&\#x27;s release of an LLM skill for DoD.

**Tags**: `#data-oriented design`, `#software engineering`, `#performance`, `#game development`

---

<a id="item-8"></a>
## [EU Proposes Browser-Level Privacy to Kill Cookie Banners](https://killthecookiebanner.eu/) ⭐️ 8.0/10

The European Commission has proposed a solution to eliminate cookie banners by allowing users to set their privacy preferences once in their browser, which would then be communicated to websites automatically. This could significantly reduce user annoyance and consent fatigue, while also streamlining compliance for website operators. It represents a major shift from website-by-website consent to browser-enforced privacy signals. The proposal builds on existing standards like the Global Privacy Control \(GPC\), which allows users to signal their preference to opt out of data selling or sharing. However, adoption remains voluntary for websites, raising questions about enforcement.

hackernews · rapnie · Jul 26, 11:53 · [Discussion](https://news.ycombinator.com/item?id=49057175)

**Background**: Cookie banners became widespread after the EU&\#x27;s ePrivacy Directive and GDPR required websites to obtain informed consent for non-essential cookies. However, many banners are designed to nudge users into accepting tracking, leading to &\#x27;consent fatigue.&\#x27; Browser-level privacy preferences aim to address this by enabling a single, user-friendly signal.

<details><summary>References</summary>
<ul>
<li><a href="https://www.w3.org/TR/gpc/">Global Privacy Control (GPC)</a></li>
<li><a href="https://globalprivacycontrol.org/">Global Privacy Control — Take Control Of Your Privacy</a></li>
<li><a href="https://secureprivacy.io/blog/sec-gpc-explained">sec-GPC Explained: The Future of Browser ... | Secure Privacy Blog</a></li>

</ul>
</details>

**Discussion**: Community members expressed mixed reactions: some argued that cookie banners should never constitute informed consent, while others praised the browser-level approach for bypassing manipulative designs. A few commenters suggested that better technical defaults, such as isolating third-party cookies by default, could also solve the problem.

**Tags**: `#privacy`, `#cookie banners`, `#web standards`, `#EU legislation`, `#browser settings`

---

<a id="item-9"></a>
## [Token Relay Market Drives AI Fraud and Abuse](https://vectoral.com/blog/token-relay-market) ⭐️ 8.0/10

An investigation by Matt Lenhard reveals a thriving relay market where stolen API keys, abused free cloud credits, and subscription model loopholes enable resellers to offer LLM tokens at steep discounts—often exceeding 90% off standard pricing. This undermines AI/ML token economies, hurts legitimate providers, and creates an uneven playing field where fraudsters gain competitive advantages. It also exposes systemic vulnerabilities in how cloud and AI services handle billing and usage limits. Resellers typically operate via proxy APIs that pool tokens from multiple sources, including stolen credentials, fraudulently obtained free credits from AWS/Azure, and shared subscription accounts. The practice is especially prevalent in China and targets services like Claude and Codex.

hackernews · mlenhard · Jul 26, 15:17 · [Discussion](https://news.ycombinator.com/item?id=49058993)

**Background**: LLM providers sell tokens as a metered resource, often with free tiers or credits to attract customers. However, these systems create arbitrage opportunities when the actual market clearing price is higher than the provider&\#x27;s listed price—similar to ticket touting for events. Fraudsters exploit billing loopholes to obtain tokens at near-zero cost, then resell them at a profit.

<details><summary>References</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/ai-token-black-market-claude-resellers-distillation-2026">AI Token Black Market: Claude Resellers at 70–93% Off (2026 ...</a></li>
<li><a href="https://simonwillison.net/2026/Jul/26/relay-market/">An Inside Look at the Relay Market Powering Token Resellers ...</a></li>

</ul>
</details>

**Discussion**: Commenters highlight that this is not new—similar resale markets existed for ad impressions. They emphasize the role of free cloud credits \(e.g., AWS\) in enabling the fraud, and note that subscription models are fundamentally vulnerable to automation and abuse. Some suggest that the core issue is pricing far below market clearing price, creating inevitable arbitrage.

**Tags**: `#token resale`, `#fraud`, `#cloud credits`, `#AI tokens`, `#subscription models`

---

<a id="item-10"></a>
## [Small 4B open-weight models rival o3 on Swedish medical QA](https://www.reddit.com/r/MachineLearning/comments/1v71wds/openweight_4b_models_approach_o3level_medical/) ⭐️ 8.0/10

Open-weight 4B parameter models \(Gemma4-E4B and Qwen3.5-4B\) achieve 77% accuracy zero-shot on the Swedish medical licensing exam dataset MedQA-SWE, and with reasoning enabled, Qwen3.5-4B reaches 87% accuracy, approaching o3&\#x27;s 88%. This demonstrates that small open-weight models can rival frontier models like GPT-4 and o3 on domain-specific tasks when properly post-trained, highlighting the potential for efficient, accessible medical AI systems in low-resource languages. The Qwen3.5-4B model performs reasoning in English despite Swedish prompts, and an early exit intervention from the S-GRPO paper was used to prevent reasoning traces from spiraling into infinite loops.

reddit · r/MachineLearning · /u/AccomplishedCat4770 · Jul 26, 11:58

**Background**: MedQA-SWE is the first open-source multiple-choice clinical question dataset in Swedish, created from exams for foreign doctors seeking Swedish medical licenses. Post-training techniques like supervised fine-tuning \(SFT\) and reasoning enablement improve small model performance significantly. The S-GRPO paper introduces an early exit method to cap reasoning trace length and prevent overthinking.

<details><summary>References</summary>
<ul>
<li><a href="https://aclanthology.org/2024.lrec-main.975/">MedQA-SWE - a Clinical Question &amp; Answer Dataset for Swedish</a></li>
<li><a href="https://arxiv.org/abs/2505.07686">S - GRPO : Early Exit via Reinforcement Learning in Reasoning Models</a></li>
<li><a href="https://huggingface.co/datasets/nicher92/medqa-swe">nicher92/medqa-swe · Datasets at Hugging Face</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#medical AI`, `#language models`, `#open-weight models`, `#Swedish`

---

<a id="item-11"></a>
## [Claude shared links leak user data via search engine indexing](https://search.brave.com/search?q=site%3Aclaude.ai%2Fshare&amp;amp;source=android) ⭐️ 8.0/10

Anthropic&\#x27;s Claude AI shared conversation links are being indexed by Google, Bing, and Brave search engines, exposing sensitive user data such as API keys, cryptocurrency wallets, and personal information without users&\#x27; knowledge. This privacy vulnerability affects millions of Claude users who have shared conversation links, potentially exposing confidential business data, financial credentials, and personally identifiable information, with no fix yet from Anthropic. The shared URLs lack a &\#x27;noindex&\#x27; tag to prevent search engine crawling, and while Google has blocked the indexed pages, Brave and Bing still return them in search results as of the report.

telegram · zaihuapd · Jul 26, 11:16

**Background**: Search engines use crawlers to index publicly accessible web pages. When Claude users share conversation links, the URLs become public and can be discovered if not properly restricted. A similar issue occurred with ChatGPT about a year ago and was quickly fixed. Users can mitigate the risk by deleting sensitive shared conversations in their Claude settings.

<details><summary>References</summary>
<ul>
<li><a href="https://thecybersecguru.com/news/claude-shared-chats-google-search-privacy/">Claude Shared Chats Indexed by Search Engines Raise Privacy ...</a></li>
<li><a href="https://www.digitalphablet.com/ai/claude-conversation-link-shared-google-indexes-it-exposing-user-chats/">Claude Conversation Link Shared, Google Indexes It, Exposing ...</a></li>
<li><a href="https://cyberpress.org/google-indexed-claude-share-links/">Google Indexed Claude Share Links Containing Sensitive User ...</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#security`, `#Claude`, `#AI`, `#data leak`

---

<a id="item-12"></a>
## [SpaceX Rejects Future Falcon 9 Orders, Bets Big on Starship](https://www.bloomberg.com/news/articles/2026-07-23/spacex-is-turning-away-falcon-customers-in-major-bet-on-starship) ⭐️ 8.0/10

SpaceX has begun rejecting dedicated launch requests from satellite operators for Falcon 9 missions after 2028 and is no longer accepting future reservations for its rideshare program. The company is also scaling back production of non-reusable Falcon components to accelerate the transition to Starship. This strategic shift could create a launch capacity gap if Starship is not commercially operational by 2028, affecting numerous space companies that rely on SpaceX for orbital access. It signals SpaceX&\#x27;s full commitment to Starship as the future platform for Starlink expansion and crewed missions to the Moon and Mars, despite recent delays and a 25% stock decline since its IPO. SpaceX may still retain Falcon 9 missions for the U.S. Department of Defense and NASA, but commercial customers beyond 2028 are being turned away. Starship&\#x27;s first contract for an externally built commercial satellite \(Superbird-9\) and a planned single-piece launch of the Starlab space station are among its future payloads.

telegram · zaihuapd · Jul 26, 12:42

**Background**: Falcon 9 is SpaceX&\#x27;s reusable workhorse rocket that has dominated the commercial launch market with its rideshare program, offering frequent and affordable access to orbit. Starship is a fully reusable next-generation rocket designed to carry large payloads and crew to deep space, but it has not yet entered commercial service. SpaceX&\#x27;s shift away from Falcon 9 for future orders reflects a high-risk bet that Starship will be operational before the Falcon 9 production line winds down.

<details><summary>References</summary>
<ul>
<li><a href="https://www.spacex.com/rideshare">Smallsat Rideshare Program - SpaceX</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_Starship_launches">List of Starship launches - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Starship">SpaceX Starship - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#Starship`, `#Falcon 9`, `#Space Industry`, `#Launch Services`

---

<a id="item-13"></a>
## [Huawei Reportedly Building DRAM Fab with 140k Monthly Wafer Capacity](https://www.xda-developers.com/huawei-is-building-its-own-dram-fab-and-it-could-reshape-ram-prices-for-everyone/) ⭐️ 8.0/10

Huawei is reportedly planning to build a large 12-inch DRAM fabrication plant in China in partnership with Shenzhen-based chip company Shengweixu, with a projected monthly capacity of approximately 140,000 wafers. Huawei has denied the report, but analysts believe the move aims to secure memory supply for its Ascend AI chips and reduce reliance on external suppliers like ChangXin Memory Technologies. If confirmed, this factory could significantly alter the global DRAM supply landscape, potentially easing tight supply and impacting pricing for consumers and datacenters alike. It also underscores Huawei&\#x27;s strategic push for semiconductor self-sufficiency amid US sanctions, particularly to support its growing AI chip business. The plant is planned as a 12-inch wafer fab, a common size for advanced DRAM production, but Huawei has publicly denied involvement in the project. Even if construction begins soon, mass production is likely several years away, meaning immediate impacts on consumer DRAM prices are unlikely.

telegram · zaihuapd · Jul 27, 03:17

**Background**: DRAM \(Dynamic Random-Access Memory\) is a type of semiconductor memory used in computing devices for temporary data storage. Huawei&\#x27;s Ascend AI chips, such as the Ascend 950 series, require high-bandwidth memory for AI inference and training tasks. Under US sanctions, Huawei has been working to develop domestic alternatives for critical components, making a dedicated DRAM fab a logical step to secure its supply chain for AI and server products.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Huawei_Ascend_%28chip%29">Huawei Ascend (chip)</a></li>
<li><a href="https://www.tsmc.com/english/dedicatedFoundry/manufacturing/gigafab">GIGAFAB® Facilities - Taiwan Semiconductor Manufacturing ...</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#DRAM`, `#semiconductor`, `#AI chips`, `#supply chain`

---

<a id="item-14"></a>
## [Google reveals Gemini 4 as its most ambitious pretraining project](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

Google CEO Sundar Pichai announced during Alphabet&\#x27;s Q2 2026 earnings call that the next-generation model Gemini 4 is already in training, describing it as the company&\#x27;s most ambitious pretraining project to date. The model is expected to launch by late November or December 2026. This announcement signals Google&\#x27;s continued aggressive investment in frontier AI, aiming to maintain leadership against competitors like OpenAI and Anthropic. Gemini 4&\#x27;s release could set new benchmarks in reasoning, coding, and multimodal capabilities, impacting developers and enterprises relying on Google&\#x27;s AI ecosystem. Pichai emphasized that Google will prioritize allocating compute resources to cutting-edge AGI research to ensure Gemini 4 remains at the forefront upon launch. Additionally, the Gemini 3.x Flash series will maintain a near-monthly update cadence, with a focus on improving coding intelligence and other capabilities.

telegram · zaihuapd · Jul 27, 04:06

**Background**: Large language models \(LLMs\) like Gemini are typically pretrained on massive datasets to predict the next word, then fine-tuned for specific tasks. Google&\#x27;s Gemini family, introduced in December 2023, includes models like Gemini Pro, Flash, and Flash Lite, designed for different performance and cost trade-offs. Pretraining is the most compute-intensive phase, and ambitious pretraining projects imply significant investment in data, compute, and algorithmic innovation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3 .6 Flash — Google DeepMind</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Google`, `#Gemini`, `#Large Language Model`, `#AGI`

---

<a id="item-15"></a>
## [Alibaba Launches Qianwen Office AI with Computer Control](https://qwenwork.cn/) ⭐️ 8.0/10

Alibaba has launched the beta version of &\#x27;Qianwen Office&\#x27; \(千问办公\), an all-in-one AI office platform that can generate and edit documents, spreadsheets, PPTs, web pages, code, and multimedia via natural language, and also controls the computer to perform clicks, input, and data extraction across applications. This launch marks Alibaba&\#x27;s entry into the competitive AI office space, offering a comprehensive tool that integrates document creation with desktop automation, potentially increasing productivity for knowledge workers and small businesses. It also introduces a clear monetization model with free and paid tiers, challenging existing players like Microsoft Copilot or WPS AI. Qianwen Office is available on web, Windows, macOS \(version 14+\), and is integrated with DingTalk; paid plans start at 78 yuan/month for 2000 credits, with a free trial of 2000 credits for new users valid 90 days. The Computer Use feature can automate desktop tasks but may capture screen content and perform irreversible actions, requiring user confirmation by default.

telegram · zaihuapd · Jul 27, 05:45

**Background**: Computer Use \(电脑操控\) refers to AI agents that simulate human behavior to control desktop applications, such as clicking buttons or entering text. It is part of Alibaba&\#x27;s larger AgentBay ecosystem, which provides developers tools to build automation workflows. This functionality enables AI to go beyond text generation and directly interact with software the way a human user would.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithome.com/0/981/982.htm">阿里千问办公官网现身，鸿蒙电脑 Beta 版同步上线 AppGallery 应用尝...</a></li>
<li><a href="https://help.aliyun.com/zh/agentbay/computeruse">Computer Use-无影 Agent 开发套件 AgentBay ... - 阿里云</a></li>

</ul>
</details>

**Tags**: `#AI办公`, `#千问办公`, `#阿里巴巴`, `#自动办公`, `#电脑操控`

---


---
layout: default
title: "Horizon Summary: 2026-08-23 (EN)"
date: 2026-08-23
lang: en
---

> From 30 items, 6 important content pieces were selected

---

1. [How Complex Systems Fail: Classic 1998 Essay on Inevitable Failure](#item-1) ⭐️ 9.0/10
2. [Nvidia Invests $1B and Licenses Poolside for $6B to Build Open-Weight AI Rival](#item-2) ⭐️ 9.0/10
3. [What Is a Harness? The Orchestration Layer for LLM Agents](#item-3) ⭐️ 8.0/10
4. [ShardFlow Hits 28 TPS on Qwen2.5-7B Across Cloud Regions via Speculative Decoding and CUDA Graphs](#item-4) ⭐️ 8.0/10
5. [Ulanqab Becomes China&\#x27;s AI Computing Hub with 12.5 GW Capacity](#item-5) ⭐️ 8.0/10
6. [Microsoft Quietly Deploys App to Force Bing as Default Search on Windows 11](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [How Complex Systems Fail: Classic 1998 Essay on Inevitable Failure](https://how.complexsystems.fail/) ⭐️ 9.0/10

The 1998 essay &\#x27;How Complex Systems Fail&\#x27; was posted to Hacker News and generated substantial discussion, earning a 9.0 score with 212 points and 58 comments. It argues that failures are an inherent property of complex systems and that conventional root cause analysis is often misguided. This essay is foundational to resilience engineering and has strongly influenced how software engineers approach distributed systems, incident review, and chaos engineering. It reframes failures not as individual errors but as system-level phenomena, shaping modern SRE practices. The essay contends that complex systems operate in a degraded mode most of the time, that failures arise from normal operations, and that post-accident attribution of a single root cause is usually a fool&\#x27;s errand. It also notes that failure-free operations require experience with failure, a principle that directly inspired Chaos Engineering.

hackernews · shortcrct · Aug 23, 15:13 · [Discussion](https://news.ycombinator.com/item?id=49409473)

**Background**: Resilience engineering is a safety science subfield that studies how complex adaptive systems cope with surprises, focusing on capabilities to anticipate, monitor, respond, and learn. Normal accident theory similarly holds that accidents are inevitable in systems that are both interactively complex and tightly coupled. These ideas provide the intellectual context for the essay&\#x27;s claim that failure cannot be designed away; it can only be understood and managed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Resilience_engineering">Resilience engineering</a></li>
<li><a href="https://psychsafety.com/normal-accidents/">Normal Accidents - Psych Safety</a></li>

</ul>
</details>

**Discussion**: Practitioners strongly endorsed the essay: tptacek called it extremely important and emphasized that root cause analysis on complex systems is a fool&\#x27;s errand, while jedberg noted it directly inspired the creation of Chaos Engineering. Other commenters recommended John Gall&\#x27;s Systemantics, and one pointed out an apparent typo in the opening sentence. Overall sentiment was highly positive.

**Tags**: `#complex systems`, `#resilience engineering`, `#failure analysis`, `#distributed systems`, `#systems thinking`

---

<a id="item-2"></a>
## [Nvidia Invests $1B and Licenses Poolside for $6B to Build Open-Weight AI Rival](https://www.wsj.com/tech/ai/nvidia-is-spending-6-billion-to-build-a-powerful-u-s-alternative-to-chinese-ai-c51c38cc) ⭐️ 9.0/10

Nvidia has agreed to invest $1 billion in AI startup Poolside at a $12 billion pre-money valuation, and pay $6 billion to license its technology and absorb most of its engineers. Over 100 Poolside employees will join Nvidia to work on the open-weight Nemotron model project. This deal signals Nvidia&\#x27;s pivot from primarily selling AI hardware to building frontier AI models, intensifying competition with Chinese open-weight labs like DeepSeek and Kimi, as well as U.S. closed-source labs such as OpenAI and Anthropic. It could reshape the open-weight ecosystem by giving Nvidia a leading position. The deal includes a $1 billion equity investment at a $12 billion pre-money valuation, plus $6 billion in licensing fees, with more than 100 Poolside employees joining Nvidia. Nvidia plans to use the technology to build one of the world&\#x27;s most powerful open-weight models, targeting DeepSeek and Kimi K3.

telegram · zaihuapd · Aug 23, 04:20

**Background**: Open-weight models release their trained parameters publicly, allowing anyone to download and modify them, unlike closed models. Nvidia&\#x27;s Nemotron family is a set of open-source models with open weights and training recipes, designed for building AI agents. Poolside, founded in 2023 by ex-GitHub CTO Jason Warner, focuses on foundation models for software development and general work.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Poolside_AI">Poolside AI - Wikipedia</a></li>
<li><a href="https://developer.nvidia.com/topics/ai/nemotron">Nemotron AI Models | NVIDIA Developer</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#AI`, `#Open-Source Models`, `#Investment`, `#Competition`

---

<a id="item-3"></a>
## [What Is a Harness? The Orchestration Layer for LLM Agents](https://earendil.com/posts/what-is-a-harness/) ⭐️ 8.0/10

The post &\#x27;What Is a Harness?&\#x27; defines a harness as the orchestration and control layer that manages LLM agents, turning raw model outputs into reliable software behavior. It argues that harness design, not the model alone, determines how effectively agents can be built and operated. As LLM agents move from demos to production, the harness becomes the key infrastructure for controllability, debugging, and tool use. Engineers building agentic systems need a shared vocabulary and patterns for this layer, making the concept timely and significant for the AI engineering community. The author likens the harness to a chassis and the model to an engine, with tokens as fuel and the agent as the car. Commenters add practical details: an internal CLI can be extremely useful for agents, and extension systems like Pi&\#x27;s can turn a harness into a flexible platform.

hackernews · tosh · Aug 23, 14:24 · [Discussion](https://news.ycombinator.com/item?id=49409092)

**Background**: A large language model \(LLM\) is an AI model trained on vast text data that can generate, summarize, and analyze language. An LLM agent uses a model to reason and take actions, often calling tools, but without extra structure it will just &\#x27;continue to generate&\#x27;. A harness is the execution control layer that turns the agent into a controllable software system, typically handling tool use, memory, step boundaries, and external integrations. This pattern is increasingly discussed in AI engineering as a complement to model choice.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://gist.github.com/manhay212/1611ddd826ef0ac8dc5719baadaf7cbe">The Harness Matters More Than the Model — patterns for building...</a></li>
<li><a href="https://blog.ayqy.net/en/articles/harness-design-for-ai-agents/">Harness Design For AI Agents : Why harness affects delivery more...</a></li>

</ul>
</details>

**Discussion**: Commenters share hands-on experience, such as building a CLI-based harness for accounting agents and finding that internal CLIs are both fun and extremely useful for agents. One user asks about handoff capabilities between terminals, team members, and models, while another argues that harnesses are the real value providers, praising Pi&\#x27;s extension system. The author also participates, offering the chassis/engine analogy and asking whether it resonates.

**Tags**: `#LLM`, `#agents`, `#orchestration`, `#harness`, `#AI infrastructure`

---

<a id="item-4"></a>
## [ShardFlow Hits 28 TPS on Qwen2.5-7B Across Cloud Regions via Speculative Decoding and CUDA Graphs](https://www.reddit.com/r/MachineLearning/comments/1vw5ysj/28_tps_on_qwen257b_across_two_separate_cloud/) ⭐️ 8.0/10

ShardFlow, a new distributed inference framework, achieved 28.10 TPS peak and 20.31 TPS average on Qwen2.5-7B using two T4 nodes in separate GCP regions connected over public WAN with ~86ms RTT. It combines neural speculative decoding with CUDA Graphs to mitigate WAN latency. This result shows that distributed LLM inference across geographically separate cloud regions is viable, potentially lowering infrastructure costs for organizations that rely on multiple data centers. It also validates that speculative decoding can effectively turn per-token WAN latency into a per-round cost, a significant optimization for latency-sensitive inference. The benchmark used K=8 drafting, accepting 4.07 tokens per round trip, and the CUDA Graphs optimization captured the full 0.5B forward pass, cutting draft latency from 112ms to 25ms. Additional stack details include a zero-copy Rust TCP relay, StaticCache with in-place KV rewind, and meta-device model slicing to avoid CPU RAM overflow. The framework also achieved 14.43 TPS average on Qwen2.5-14B with NF4 4-bit quantization on the same two nodes.

reddit · r/MachineLearning · /u/katua\_bkl · Aug 23, 12:30

**Background**: Speculative decoding is an inference-time optimization where a small auxiliary model generates draft tokens, which a larger model then verifies, producing identical results to greedy decoding while reducing latency. CUDA Graphs reduce CPU-side kernel launch overhead by capturing a sequence of GPU operations into a single graph that can be replayed with one launch. ShardFlow is a general-purpose distributed inference framework that automatically partitions any HuggingFace transformer across multiple GPU machines and exposes an OpenAI-compatible endpoint. WAN latency between cloud regions is typically high, making distributed inference challenging; speculative decoding helps by moving latency out of the per-token critical path.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/rautaditya2606/Shardflow">GitHub - rautaditya2606/ Shardflow</a></li>
<li><a href="https://docs.nvidia.com/cuda/cuda-programming-guide/04-special-topics/cuda-graphs.html">4.2. CUDA Graphs — CUDA Programming Guide</a></li>
<li><a href="https://developers.redhat.com/articles/2026/06/12/how-speculative-decoding-delivers-faster-llm-inference">How speculative decoding delivers faster LLM inference | Red Hat Developer</a></li>

</ul>
</details>

**Tags**: `#distributed inference`, `#speculative decoding`, `#CUDA Graphs`, `#LLM inference`, `#performance optimization`

---

<a id="item-5"></a>
## [Ulanqab Becomes China&\#x27;s AI Computing Hub with 12.5 GW Capacity](https://www.wired.com/story/the-unlikely-place-at-the-center-of-chinas-ai-boom/) ⭐️ 8.0/10

Ulanqab, a city in Inner Mongolia, has become a major AI computing hub, with Chinese companies committing 12.5 gigawatts of data center capacity—exceeding OpenAI&\#x27;s Stargate project&\#x27;s planned 10 GW. Over 70% of this committed capacity was announced in the past year. This scale of AI infrastructure investment signals China&\#x27;s aggressive push into AI computing, potentially giving it a strategic advantage in model training and deployment. It also underscores the global trend of building massive data centers in remote, low-cost regions, which raises significant energy and environmental questions. Nearly 100 data centers have opened or broken ground in Ulanqab since 2016, including facilities by DeepSeek, ByteDance, Alibaba, and Xiaohongshu. The area&\#x27;s cold climate, low electricity prices, and proximity to Beijing are major draws, but water scarcity is a concern: annual precipitation is only about 14 inches, and a local water plant was recently forced to shut off supply for seven hours each night.

telegram · zaihuapd · Aug 23, 00:55

**Background**: AI data centers need massive amounts of electricity to power servers and cooling systems. Ulanqab&\#x27;s cold climate and cheap power—though about 37% still comes from coal—make it an attractive location. Stargate, a joint AI infrastructure venture by OpenAI, SoftBank, Oracle, and MGX, aims to raise $500 billion, with $100 billion deployed immediately and the rest over four years.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aol.com/know-stargate-openais-venture-announced-175055247.html">What to Know About &#x27; Stargate ,&#x27; OpenAI &#x27;s New Venture Announced by....</a></li>
<li><a href="https://www.linkedin.com/posts/deepakpros_stargateproject-openai-oracle-activity-7296196541579464705-gcRw">#stargateproject # openai #oracle #ai #nvidia | Deepak Wadhwani</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#data centers`, `#China`, `#computing power`, `#energy`

---

<a id="item-6"></a>
## [Microsoft Quietly Deploys App to Force Bing as Default Search on Windows 11](https://www.windowslatest.com/2026/08/22/microsoft-built-a-dedicated-app-that-forces-bing-everywhere-on-windows-11-including-chrome-firefox-and-brave/) ⭐️ 8.0/10

Microsoft has released a dedicated app called &\#x27;Microsoft Recommended Search Settings&\#x27; that automatically changes the default search engine to Bing in Chrome, Firefox, and Brave on Windows 11. The app is hosted on Microsoft&\#x27;s official servers, bypasses Windows Update and the Store, and redirects users to Microsoft Rewards after installation. This move intensifies Microsoft&\#x27;s push to steer users toward Bing, raising anti-competitive concerns and affecting millions of Windows users who prefer other search engines. It also highlights the ongoing browser default-search competition that has drawn regulatory scrutiny. In testing, Chrome displayed a prompt asking whether users want to revert to Google, while Microsoft added a &\#x27;Wait, don&\#x27;t switch back&\#x27; message to retain them. The associated Bing extension reportedly shows 5 million users, though it&\#x27;s unclear how many actually installed the app.

telegram · zaihuapd · Aug 23, 05:18

**Background**: Default search engines determine which service a browser uses for search queries, and most browsers let users set this preference. Microsoft has previously used Edge and Windows prompts to encourage Bing adoption, but this dedicated app represents a more aggressive approach. The app reportedly appears without going through standard distribution channels, potentially catching users off guard. This is part of a broader pattern of default-browser battles between major tech companies.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Microsoft">Microsoft - Wikipedia</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-products-and-apps">Microsoft products, apps, and devices built to support you</a></li>

</ul>
</details>

**Tags**: `#Microsoft`, `#Bing`, `#Browser`, `#Default Search`, `#Anti-competitive`

---
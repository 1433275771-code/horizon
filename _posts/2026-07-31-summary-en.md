---
layout: default
title: "Horizon Summary: 2026-07-31 (EN)"
date: 2026-07-31
lang: en
---

> From 37 items, 8 important content pieces were selected

---

1. [DeepSeek V4 Flash 0731: Frontier-Level Intelligence at $0.28/M Output Tokens](#item-1) ⭐️ 9.0/10
2. [Stateless MCP 2.0 Reignites Simon Willison&\#x27;s Interest, Inspiring New Tools](#item-2) ⭐️ 9.0/10
3. [Huawei Open-Sources 505B-Parameter MoE Model openPangu-2.0-Pro](#item-3) ⭐️ 9.0/10
4. [Elevator Scheduling Algorithms Explored with Simulations and Community Insights](#item-4) ⭐️ 8.0/10
5. [YC-Backed QM Launches Multiplayer Agent Harness for Collaborative Work](#item-5) ⭐️ 8.0/10
6. [OpenAI cuts GPT-5.6 Luna price 80%, Terra 20%](#item-6) ⭐️ 8.0/10
7. [MiniMax to Open-Source Multimodal Video Model H3 on August 3](#item-7) ⭐️ 8.0/10
8. [German Court Rules AI Music Firm Suno Violated Copyright](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Flash 0731: Frontier-Level Intelligence at $0.28/M Output Tokens](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 9.0/10

DeepSeek officially released the V4 Flash 0731 API, an upgraded version of its V4-Flash model with substantially enhanced agentic capabilities. It achieves frontier-level scores on the Artificial Analysis Intelligence Index while priced at just $0.28 per million output tokens. This release brings frontier-level model quality to an unusually low price point, intensifying price-performance competition among top AI labs. It makes agentic coding and heavy LLM usage far more affordable for developers, and raises expectations for an imminent V4 Pro update. DeepSeek V4 Flash 0731 is a sparse mixture-of-experts model with 284B total parameters and 13B active, supporting a 1M-token context window. Compared to the preview, only post-training changed; it natively supports the Responses API and is adapted for Codex, with benchmark scores including 82.7 on Terminal Bench 2.1.

hackernews · theanonymousone · Jul 31, 07:59 · [Discussion](https://news.ycombinator.com/item?id=49120299)

**Background**: LLM APIs typically bill separately for input and output tokens, and output tokens cost more because they require autoregressive generation, which is computationally expensive. DeepSeek is a Chinese AI lab known for releasing powerful open-weight models at low prices; V4 Flash is a sparse mixture-of-experts model, meaning only a subset of parameters is active per token. &\#x27;Frontier-level&\#x27; indicates the model ranks among the best available on aggregate intelligence benchmarks.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek-ai/DeepSeek-V4-Flash-0731 · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-0731">DeepSeek V4 Flash 0731 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://www.silicondata.com/blog/llm-cost-per-token">Understanding LLM Cost Per Token: A 2026 Practical Guide - Silicon Data — GPU Performance Data for Companies</a></li>

</ul>
</details>

**Discussion**: Community sentiment is broadly positive, with users praising the model&\#x27;s price-performance as a daily driver with &\#x27;no token anxiety.&\#x27; Some commenters question the use of a minimal DeepSeek Harness mode in benchmarks and wonder if an optimized coding agent harness will be announced; others speculate about when V4 Pro will arrive and discuss the economics of hosting models on Hugging Face.

**Tags**: `#AI`, `#LLM`, `#DeepSeek`, `#benchmarking`, `#price-performance`

---

<a id="item-2"></a>
## [Stateless MCP 2.0 Reignites Simon Willison&\#x27;s Interest, Inspiring New Tools](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 9.0/10

Simon Willison reported that the 2026-07-28 stateless MCP specification \(MCP 2.0\) reignited his interest in the Model Context Protocol. He built three implementations this week, including the mcp-explorer CLI and datasette-mcp. This is the most significant change to MCP since its launch: the stateless core removes the need to track server-side sessions, cutting implementation complexity for clients and servers. It makes MCP a stronger fit for scalable web applications and easier for smaller, locally-runnable models to drive, which could accelerate adoption of auditable, controlled tool use by AI agents. The spec replaces the old two-request flow—initialize to get a Mcp-Session-Id, then call the tool—with a single HTTP request using MCP-Protocol-Version and Mcp-Method headers. Willison also pushed back on shell-and-curl agent designs, arguing MCP tools are easier to audit and control, while a terminal environment is &\#x27;fraught with risk&\#x27;.

rss · Simon Willison · Jul 31, 23:13

**Background**: The Model Context Protocol is an open standard introduced by Anthropic in November 2024 to standardize how LLM-powered agents connect to external tools and data sources. Through much of 2025 it saw huge interest, but was partly eclipsed by Anthropic&\#x27;s Claude Skills when it appeared that an agent with a terminal and curl could flexibly accomplish many tasks—an approach Willison now considers risky. The 2026-07-28 specification, released after a release candidate in May, makes MCP stateless at the protocol layer.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.modelcontextprotocol.io/posts/2026-07-28/">The 2026 - 07 - 28 Specification | Model Context Protocol Blog</a></li>
<li><a href="https://claude.com/blog/bringing-mcp-2026-07-28-to-claude">MCP 2026 - 07 - 28 spec : stateless core, coming... | Claude by Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#AI`, `#LLM`, `#agents`, `#protocol`

---

<a id="item-3"></a>
## [Huawei Open-Sources 505B-Parameter MoE Model openPangu-2.0-Pro](https://huggingface.co/openpangu/openPangu-2.0-Pro) ⭐️ 9.0/10

Huawei has released openPangu-2.0-Pro on Hugging Face, a 505B-parameter Mixture-of-Experts model that activates about 18B parameters per token and supports a 512k-token context. The open-source release includes a Thinking version that scored 95.4 on AIME 2026 and 87.9 on GPQA-Diamond. This is one of the largest open-source MoE models from a major vendor, narrowing the gap between open and proprietary large models. Its strong reasoning benchmarks and efficient architecture could influence how other labs design scalable, long-context models. The model is trained on Ascend NPUs using roughly 34T tokens, and its architecture combines Multi-head Latent Attention \(MLA\) with a hybrid DSA+SWA design and a 3-head Multi-Token Prediction \(MTP\) self-speculative decoding module. After training, it underwent fast-and-slow unified fine-tuning and multi-task reinforcement learning.

telegram · zaihuapd · Jul 31, 06:50

**Background**: MoE models use multiple specialized sub-networks \(experts\) but only activate a subset per token, allowing huge parameter counts with manageable compute. MLA reduces the KV-cache memory bottleneck during inference via low-rank latent compression, while hybrid attention layers such as SWA help handle long contexts efficiently. MTP improves inference speed by letting the model predict several future tokens at once, enabling speculative decoding. The model is also notable for being trained on Huawei&\#x27;s Ascend NPU ecosystem rather than mainstream GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://machinelearningmastery.com/a-gentle-introduction-to-multi-head-latent-attention-mla/">A Gentle Introduction to Multi-Head Latent Attention (MLA) - MachineLearningMastery.com</a></li>
<li><a href="https://jianyuh.github.io/llm/2026/04/26/DeepSeek-V4-Arch-Train.html">DeepSeek-V4 Architecture &amp; Training: Hybrid Attention, Muon ...</a></li>
<li><a href="https://arxiv.org/pdf/2404.19737">Better &amp; Faster Large Language Models via Multi-token Prediction</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#LLM`, `#MoE`, `#Huawei`, `#AI`

---

<a id="item-4"></a>
## [Elevator Scheduling Algorithms Explored with Simulations and Community Insights](https://john.fun/elevators) ⭐️ 8.0/10

The article presents a technical deep dive into elevator scheduling algorithms, featuring simulations and comparisons of different approaches such as SCAN, LOOK, and destination dispatch. It sparked an active Hacker News discussion with 807 points and 208 comments. Elevator scheduling directly affects daily life in tall buildings, and the algorithmic trade-offs mirror broader problems in operating systems and logistics. The discussion bridges elevator engineering with disk scheduling, offering insights applicable to any system that must serve ordered requests with a single moving head. The author apparently found that destination dispatch can be worse under random destinations, while LOOK-style algorithms performed well; commenters note that real-world patterns such as mass ground-floor departures and group lunches may change the comparison. The piece connects elevator algorithms to the SCAN disk-scheduling family and references Elevator Saga as a hands-on simulation game.

hackernews · Jrh0203 · Jul 31, 15:17 · [Discussion](https://news.ycombinator.com/item?id=49124218)

**Background**: The elevator algorithm, also known as SCAN, is a classic disk-scheduling method where the read/write arm moves in one direction, serving requests along the way, then reverses direction. In elevators, the same idea keeps a car moving up or down while picking up passengers whose destinations lie ahead. Destination dispatch is a more modern approach that groups passengers by destination using keypad entry rather than floor buttons. Understanding these algorithms matters for optimizing latency, throughput, and energy use in both elevators and hard drives.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Elevator_algorithm">Elevator algorithm - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/operating-systems/difference-between-scan-and-cscan-disk-scheduling-algorithms/">Difference Between SCAN and CSCAN Disk Scheduling Algorithms</a></li>
<li><a href="https://www.geeksforgeeks.org/operating-systems/c-scan-disk-scheduling-algorithm/">C-SCAN Disk Scheduling Algorithm - GeeksforGeeks</a></li>

</ul>
</details>

**Discussion**: Commenters made several valuable points: one linked elevator algorithms to HDD disk scheduling and noted that SCAN is literally a disk-scheduling algorithm; another argued that destination dispatch may outperform random-destination simulations in real buildings because traffic is highly skewed to ground-floor trips and group lunches. Others shared nostalgic programming projects, recommended the Elevator Saga game, and one game developer said he used a LOOK-like algorithm to match player expectations. A user also complained about the lack of a toggle to un-press accidentally pressed elevator buttons.

**Tags**: `#algorithms`, `#scheduling`, `#elevators`, `#simulation`, `#systems`

---

<a id="item-5"></a>
## [YC-Backed QM Launches Multiplayer Agent Harness for Collaborative Work](https://github.com/yc-software/qm) ⭐️ 8.0/10

QM, a YC-backed multiplayer agent harness for work, uses per-person scopes and shared rooms to coordinate multiple AI agents in collaborative settings across Slack and the web. The project bridges personal AI assistants and company-wide automation by giving each employee an isolated workspace while enabling shared coordination. Per-person scopes combined with shared rooms directly address the hardest problem in multiplayer agents: scoping and coordination, making it a sane answer for company-wide assistants. This validates the emerging category of agent harnesses for collaborative work and signals growing YC interest in team-oriented AI infrastructure. QM operates across Slack and web interfaces, giving each employee an isolated workspace for personal agents while shared rooms allow cross-agent coordination. The project joins adjacent tools like Orca and AQ, both also exploring multiplayer agent systems for coding and work.

hackernews · tosh · Jul 31, 18:04 · [Discussion](https://news.ycombinator.com/item?id=49126604)

**Background**: An agent harness is an orchestration layer that gives AI agents tools, permissions, and a structured environment to accomplish tasks reliably. Multiplayer agent systems extend this to multiple agents and humans working together, but they face hard problems around scoping — deciding which data and tools each agent can access — and coordination. QM&\#x27;s approach of per-person scopes plus shared rooms is a common design pattern emerging in this space, also seen in tools like Claude Cowork and agent chat rooms. Y Combinator backing signals growing interest in this category.

<details><summary>References</summary>
<ul>
<li><a href="https://aitoolly.com/ai-news/article/2026-08-01-qm-a-new-multiplayer-ai-agent-harness-for-collaborative-startup-workflows-in-slack-and-web">QM: Multiplayer AI Agent Harness for Startups and Slack</a></li>
<li><a href="https://learn.microsoft.com/en-us/agent-framework/agents/harness">Agent Harnesses | Microsoft Learn</a></li>
<li><a href="https://www.arthur.ai/column/access-management-ai-agents-scope-permissions">Access Management for AI Agents: Scope What They Touch | Arthur</a></li>

</ul>
</details>

**Discussion**: Commenters were largely enthusiastic, with builders in adjacent spaces calling the direction &\#x27;validating and a little surreal&\#x27; and praising per-person scopes as a smart answer for company-wide assistants. One person joked about agents scheduling meetings autonomously, while others questioned how QM differentiates from existing products like Claude Cowork and asked for a direct comparison.

**Tags**: `#AI agents`, `#multiplayer`, `#LLM`, `#collaboration`, `#Y Combinator`

---

<a id="item-6"></a>
## [OpenAI cuts GPT-5.6 Luna price 80%, Terra 20%](https://simonwillison.net/2026/Jul/30/luna-price-drop/#atom-everything) ⭐️ 8.0/10

On July 30, 2026, OpenAI announced price reductions of 20% for GPT-5.6 Terra and 80% for GPT-5.6 Luna. OpenAI attributes the cuts to GPT-5.6 Sol, which optimized load balancing and inference to reduce serving costs by 20%. Luna&\#x27;s new pricing – $0.20 per million input tokens and $1.20 per million output tokens – makes it cheaper than Google&\#x27;s Gemini 3.1 Flash-Lite and roughly one-fifth the input price of Anthropic&\#x27;s Claude Haiku 4.5. This shifts the competitive landscape for budget LLM deployments and shows that AI models can be used to optimize their own serving infrastructure. Sol optimized the forward pass by finding work that could be precomputed, avoided, or parallelized, and autonomously rewrote production kernels in Triton and Gluon with Codex. These optimizations reduced end-to-end serving costs by 20%, enabling the price drop; note the Gemini Flash-Lite input price in the article appears as $0.25 per million tokens.

rss · Simon Willison · Jul 30, 23:58

**Background**: GPT-5.6 is OpenAI&\#x27;s model family released on July 9, 2026, consisting of three tiers: Luna \(fastest and cheapest\), Terra \(balanced\), and Sol \(flagship\). The price cuts are notable because they stem from using Sol itself to improve inference efficiency, including rewriting kernels in Triton and Gluon, two open-source GPU programming languages maintained by OpenAI.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://openai.com/index/gpt-5-6/">GPT‑5.6: Frontier intelligence that scales with ... - OpenAI</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-5.6`, `#AI pricing`, `#inference optimization`, `#machine learning`

---

<a id="item-7"></a>
## [MiniMax to Open-Source Multimodal Video Model H3 on August 3](https://modelscope.cn/models/MiniMax/MiniMax-H3) ⭐️ 8.0/10

MiniMax announced that its new general-purpose multimodal video model H3 will be open-sourced on the ModelScope community on August 3, 2026. The model natively supports understanding and generation of text, images, audio, and video, and can produce up to 15-second 2K resolution content with native dual-channel audio. This release is a significant step for open-source multimodal AI, as H3 combines unified understanding and generation across four modalities in a single model. It is expected to impact creative and commercial applications such as film, advertising, e-commerce, and game development by making advanced video generation accessible to developers. H3 offers multi-dimensional precise editing control and supports native dual-channel audio-video output, with a maximum of 15 seconds at 2K resolution. It uses Contextual Omni Representation and Omni Reference capabilities to fuse multiple reference materials for coherent creation.

telegram · zaihuapd · Jul 31, 12:37

**Background**: MiniMax H3 is a general-purpose all-modal generative model officially released on July 31, 2026. Multimodal video models combine understanding and generation of text, images, audio, and video; open-sourcing such models on ModelScope, Alibaba&\#x27;s AI model community, allows developers and researchers to deploy and customize them for real-world tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithome.com/0/984/379.htm">MiniMax H3 通用多模态视频模型将于 8 月 3 日开源，最高可支持 15s 2...</a></li>
<li><a href="https://baike.baidu.com/item/MiniMax+H3/68391253">MiniMax H3 - 百度百科</a></li>
<li><a href="https://apidot.ai/zh/blog/minimax-h3-review">MiniMax H3 全面评测：功能、画质、价格与早期实测 | APIDot</a></li>

</ul>
</details>

**Tags**: `#multimodal`, `#video model`, `#open source`, `#AI`, `#MiniMax`

---

<a id="item-8"></a>
## [German Court Rules AI Music Firm Suno Violated Copyright](https://www.dw.com/en/german-court-rules-that-ai-music-firm-suno-violated-copyrights/a-78152227) ⭐️ 8.0/10

The Munich Regional Court ruled on Friday that U.S. AI music company Suno infringed copyright, ordering it to disclose illegal proceeds and pay damages, with the exact amount still to be determined. Suno stated it disagrees with the ruling and is evaluating all options, including appeal. This is one of the first major court rulings testing how copyright law applies to AI music training, potentially setting a precedent for licensing practices across the AI industry. It could push AI music companies to obtain proper licenses for training data, affecting both AI developers and the broader music ecosystem. The lawsuit was filed by GEMA, Germany&\#x27;s music rights collective, in January 2025, alleging Suno trained its AI models on copyrighted music without permission or compensation. During the trial, GEMA demonstrated that songs generated by Suno were highly similar to original works, though the exact damages amount has not yet been determined.

telegram · zaihuapd · Jul 31, 13:11

**Background**: GEMA represents the music rights of over 95,000 German musicians and more than 2 million rights holders worldwide. Suno is an AI music generator that creates original songs from text prompts. The broader legal question is whether using copyrighted works to train AI models constitutes infringement or qualifies as fair use, a subject of ongoing debate in courts and legislatures globally.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GEMA_%28German_organization%29">GEMA ( German organization) - Wikipedia</a></li>
<li><a href="https://suno.com/">Suno | AI Music Generator</a></li>
<li><a href="https://astraea.law/insights/ai-training-data-copyright">AI Training Data Copyright: Fair Use, Licensing, and ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#copyright`, `#music`, `#legal`, `#Suno`

---
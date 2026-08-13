---
layout: default
title: "Horizon Summary: 2026-08-13 (EN)"
date: 2026-08-13
lang: en
---

> From 34 items, 10 important content pieces were selected

---

1. [Spaghettifying DRAM: Reverse-Engineering Address Scrambling to Unlock Hidden Memory](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Pro 0813 Launches via API; Open Weights Hit Hugging Face](#item-2) ⭐️ 9.0/10
3. [Gemini 3.7 Flash](#item-3) ⭐️ 8.0/10
4. [OpenAI and Cerebras Launch GPT-5.6 Sol Ultrafast, 7x Faster Inference](#item-4) ⭐️ 8.0/10
5. [DeepSeek releases open-source Harness developer preview](#item-5) ⭐️ 8.0/10
6. [Choose Boring Technology: Dan McKinley&\#x27;s Innovation Tokens Essay Endures](#item-6) ⭐️ 8.0/10
7. [Trump signs memo allowing private firms to conduct US-endorsed overseas cyber attacks](#item-7) ⭐️ 8.0/10
8. [DeepMind launches SL2T sign language-to-text model on Pixel 11](#item-8) ⭐️ 8.0/10
9. [CXMT Overtakes Tencent as Most Valuable Chinese Company](#item-9) ⭐️ 8.0/10
10. [OpenAI Previews Ultrafast Mode, Speeding Up GPT-5.6 Sol by 14x](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Spaghettifying DRAM: Reverse-Engineering Address Scrambling to Unlock Hidden Memory](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

Christopher Domas&\#x27;s project skitter-creek-bath-salts demonstrates how to reverse-engineer DRAM address scrambling using the z3 solver, transforming coherent physical addresses into a scrambled &\#x27;spaghettified&\#x27; view. This allows an attacker with ring-0 access to reach normally protected memory regions such as PSP private memory, SMRAM, and the C6 idle-state on AMD Jaguar \(AMD16h\) systems. This research breaks hardware-level memory isolation, revealing that DRAM scrambling is not a security boundary but a bypassable obfuscation layer. It could undermine protections on consoles like Xbox and PlayStation or any platform relying on memory scrambling to hide firmware from the CPU, escalating a single ring-0 compromise into full platform domination. The solved transform is described as a &\#x27;rosetta stone&\#x27; that maps any target address in the coherent memory view to an alias in the spaghettified view, bypassing platform fences and security checks. The README notes that Zen 3 uses a different base address for the memory controller registers, leaving newer CPU generations potentially unaffected but warranting further investigation.

hackernews · matt\_d · Aug 13, 14:17 · [Discussion](https://news.ycombinator.com/item?id=49286341)

**Background**: DRAM address scrambling is a technique used by memory controllers to shuffle physical addresses across channels, ranks, banks, and rows to improve performance and thermal distribution. This mapping is typically kept secret as a security measure, but researchers have shown it can be reverse-engineered using side-channel techniques and formal solvers. The project name references spaghettification, the tidal stretching of objects in extreme gravity, as a metaphor for the distorted memory view.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/xoreaxeaxeax/skitter-creek-bath-salts">GitHub - xoreaxeaxeax/skitter-creek-bath-salts: Unlocking _everything_ on the CPU with DRAM scrambling · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Memory_scrambling">Memory controller - Wikipedia</a></li>
<li><a href="https://arxiv.org/pdf/2004.02354">DRAMDig: A Knowledge-assisted Tool to Uncover DRAM Address Mapping</a></li>

</ul>
</details>

**Discussion**: Commenters are enthusiastic about Christopher Domas&\#x27;s upcoming Black Hat talk, citing his previous work on reverse engineering and hardware backdoors. Some express nostalgia for the simpler, understandable DRAM of early computers, while others worry about the implications for Xbox and PlayStation security groups. Several questions remain about which newer CPU families, if any, are vulnerable beyond AMD Jaguar.

**Tags**: `#DRAM`, `#hardware security`, `#reverse engineering`, `#memory hacking`, `#exploitation`

---

<a id="item-2"></a>
## [DeepSeek V4 Pro 0813 Launches via API; Open Weights Hit Hugging Face](https://simonwillison.net/2026/Aug/12/deepseek-v4-pro-0813/) ⭐️ 9.0/10

The latest DeepSeek Pro model, DeepSeek V4 Pro 0813, is now available via API through OpenRouter and other providers. The open weights were subsequently released on Hugging Face, totaling 1.7 trillion parameters and 893 GB in size. As DeepSeek again ships a large open-weights model, this release gives developers and researchers a state-of-the-art alternative to closed commercial APIs, likely intensifying price competition and accelerating local deployments. With 1.7T parameters available for download, it significantly strengthens the open-weights ecosystem at the frontier scale. The model enhances agent capabilities and natively supports the Responses API format for Codex compatibility, with reasoning levels low, high, and max newly available on V4-Pro and V4-Flash. Peak/off-peak API pricing takes effect August 17, 2026, with off-peak time costing half the peak rate; the Hugging Face weights are 893 GB with 1.7T parameters.

rss · Simon Willison · Aug 12, 23:59

**Background**: Open-weights models make the numerical parameters of a trained neural network public, allowing others to inspect, fine-tune, and run them locally, which promotes transparency even if the full training data and code are not released. OpenRouter is a unified API gateway that lets developers access hundreds of LLMs from different vendors through a single interface, which is why it often becomes the announcement channel for new models. Parameters are the learned weights and biases inside a neural network; 1.7T is exceptionally large, placing this model at the frontier scale of contemporary LLMs.

<details><summary>References</summary>
<ul>
<li><a href="https://promptengineering.org/llm-open-source-vs-open-weights-vs-restricted-weights/">Openness in Language Models: Open Source vs Open Weights vs...</a></li>
<li><a href="https://www.codecademy.com/article/what-is-openrouter">What is OpenRouter ? A Guide with Practical Examples | Codecademy</a></li>
<li><a href="https://news.ycombinator.com/item?id=37804839">Ask HN: GPT-4 has 1.7T parameters. What&#x27;s a parameter? | Hacker News</a></li>

</ul>
</details>

**Tags**: `#AI`, `#DeepSeek`, `#machine-learning`, `#open-weights`, `#model-release`

---

<a id="item-3"></a>
## [Gemini 3.7 Flash](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 8.0/10

Google introduces Gemini 3.7 Flash, a new AI model with competitive vision performance and introductory pricing.

hackernews · thisisauserid · Aug 13, 17:23 · [Discussion](https://news.ycombinator.com/item?id=49289112)

**Tags**: `#Gemini`, `#Google`, `#AI`, `#LLM`, `#Model Release`

---

<a id="item-4"></a>
## [OpenAI and Cerebras Launch GPT-5.6 Sol Ultrafast, 7x Faster Inference](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

OpenAI and Cerebras announced GPT-5.6 Sol Ultrafast mode, which answered all 2,500 HLE questions in 11 hours and 11 minutes, compared to 78 hours and 27 minutes for Claude Fable 5 — achieving comparable accuracy nearly 7x faster. The mode also runs 11x faster than Fable 5 and 5x faster than Opus 4.8 on Fast mode based on output speeds reported by Artificial Analysis. This collaboration demonstrates that ultra-fast LLM inference is achievable on wafer-scale hardware, potentially lowering latency and cost for real-time AI applications. It also sparks an industry-wide debate about whether inference speed comes at the cost of reasoning quality, which could shape how future AI models are deployed and optimized. Neither the Cerebras nor the OpenAI post explicitly states that Ultrafast mode produces results identical to the regular GPT-5.6 Sol, leaving the exact performance parity unconfirmed. No pricing information was released for Ultrafast mode, which could indicate an enterprise-focused offering or that the companies are gauging market interest before setting a price.

hackernews · pr337h4m · Aug 13, 18:10 · [Discussion](https://news.ycombinator.com/item?id=49289844)

**Background**: Cerebras Systems develops the Wafer-Scale Engine \(WSE\), the world&\#x27;s largest AI processor, with the WSE-3 containing 4 trillion transistors, 900,000 AI-optimized cores, 44GB of on-chip SRAM, and 21 petabytes per second of memory bandwidth. Traditional LLM inference relies on GPU clusters, but Cerebras&\#x27;s wafer-scale architecture offers a radically different approach that can dramatically accelerate token generation. This partnership with OpenAI aims to explore how custom silicon can push the limits of inference speed for frontier models.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://www.cerebras.ai/chip">Product - Chip - Cerebras</a></li>
<li><a href="https://introl.com/blog/cerebras-wafer-scale-engine-cs3-alternative-ai-architecture-guide-2025">Cerebras Wafer-Scale Engine | Introl Blog</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters expressed excitement about the OpenAI-Cerebras collaboration, with some highlighting how speed enables iterative thinking and higher-quality reasoning in LLMs. However, others were skeptical: they noted the lack of an explicit statement that Ultrafast mode matches the original model&\#x27;s quality, and pointed out that missing pricing details suggest the offering may be prohibitively expensive or still in an exploratory stage.

**Tags**: `#AI`, `#LLM`, `#Inference`, `#OpenAI`, `#Cerebras`

---

<a id="item-5"></a>
## [DeepSeek releases open-source Harness developer preview](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek released a developer preview of DeepSeek Harness \(dsh\), an open-source agent harness built on Cordis&\#x27;s plugin system, with source code available on GitHub under the MIT license. The preview introduces traceable append-only session logs and an everything-is-a-plugin architecture. Agent harness infrastructure is becoming critical for production LLM agents, and DeepSeek open-sourcing this tool with full traceability and a plugin system could influence the broader developer ecosystem. It also puts pressure on other AI labs to offer similar transparency in their agent tooling. The harness is powered by Cordis v4, which supports hot-reloading and dynamically enabling or disabling plugins without restarting the running process, and can revert plugin side effects. Session logs are append-only and record system prompts, reasoning, tool calls, subagent scheduling, and context injections; the Trajectory view supports resume, fork, search, and replay on the same event stream.

hackernews · bjin · Aug 13, 12:58 · [Discussion](https://news.ycombinator.com/item?id=49285244)

**Background**: An agent harness is the software infrastructure surrounding a large language model that manages tool use, memory, state persistence, execution environments, and feedback loops, enabling the model to act on tasks rather than just respond to prompts. DeepSeek Harness adopts an everything-is-a-plugin architecture and builds on Cordis, a plugin system originally used in projects like Koishi for hot-loading and unloading plugins.

<details><summary>References</summary>
<ul>
<li><a href="https://www.deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">GitHub - deepseek -ai/ deepseek - harness : DeepSeek Harness ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agent_harness">Agent harness - Wikipedia</a></li>

</ul>
</details>

**Discussion**: One author confirmed it is an early developer preview under the MIT license and welcomed feedback despite rough edges. Commenters praised full traceability as a killer feature compared to US models&\#x27; obfuscated traces, while others discussed the underlying Cordis v4 paper and expressed fatigue over everything-as-a-plugin designs.

**Tags**: `#AI`, `#developer-tools`, `#open-source`, `#agent-harness`, `#plugin-system`

---

<a id="item-6"></a>
## [Choose Boring Technology: Dan McKinley&\#x27;s Innovation Tokens Essay Endures](https://mcfunley.com/choose-boring-technology) ⭐️ 8.0/10

Dan McKinley&\#x27;s 2015 essay &\#x27;Choose Boring Technology&\#x27; is being highlighted as a timeless, high-scoring piece on pragmatic tech choices. It argues that companies should default to mature, unexciting tools and spend limited &\#x27;innovation tokens&\#x27; only where novelty provides a real competitive edge. The essay gives engineering leaders a memorable framework for resisting hype-driven rewrites and constant tool churn. Its &\#x27;innovation tokens&\#x27; metaphor has become a widely used shorthand for explaining the trade-off between stability and novelty in architecture decisions. McKinley proposes that a company gets roughly three innovation tokens to spend over a long period, and each new technology choice consumes one token. He draws on his experience at Etsy, where deliberately boring choices like MySQL and PHP supported fast product development without overwhelming operational complexity.

hackernews · tosh · Aug 13, 17:48 · [Discussion](https://news.ycombinator.com/item?id=49289512)

**Background**: &\#x27;Boring technology&\#x27; does not mean outdated technology; it means mature, well-understood tools such as PostgreSQL, whose behavior is predictable and well-documented. The innovation-tokens concept was popularized by McKinley&\#x27;s essay and has become a way to remind teams that every novel component adds operational and cognitive cost, so novelty should be rationed carefully.

<details><summary>References</summary>
<ul>
<li><a href="https://www.lessannoyingbusiness.com/post/innovation-tokens">Innovation Tokens - When to break from the status quo</a></li>
<li><a href="https://xebia.com/blog/how-innovation-tokens-can-change-your-life/">How Innovation Tokens Can Change Your Life | Xebia</a></li>
<li><a href="https://www.peal.dev/blog/boring-technology-principle-why-we-pick-proven-tools">The Boring Technology Principle : Why We Reach for... — peal.dev</a></li>

</ul>
</details>

**Discussion**: Commenters largely praise the essay; one calls innovation tokens &\#x27;one of the most useful concepts&\#x27; they have encountered as a PM and engineering leader. Others add caveats, noting that in-house expertise can make a normally &\#x27;boring&\#x27; choice right in a specific context, and that in the age of AI agents, teams may want to spend all their tokens on agents while keeping the surrounding technology boring. A dissenting comment pushes back against the advice, though its argument is truncated.

**Tags**: `#technology strategy`, `#engineering culture`, `#software architecture`, `#innovation tokens`, `#pragmatism`

---

<a id="item-7"></a>
## [Trump signs memo allowing private firms to conduct US-endorsed overseas cyber attacks](https://www.bloomberg.com/news/articles/2026-08-13/trump-enlists-private-sector-to-boost-cyber-offensive-arsenal) ⭐️ 8.0/10

President Trump signed a memorandum authorizing private companies, under direct federal control and supervision, to conduct overseas surveillance and cyber attacks against foreign networked transnational criminal organizations. This marks a significant expansion of private-sector involvement in state-backed offensive cyber operations, blurring the line between corporate and government action. It could reshape how the US conducts cyber defense and affect legal and tech communities worldwide. The Department of Homeland Security \(DHS\) will run the program in coordination with the Department of Justice \(DOJ\). Participating firms must maintain at least $1 million in bond or escrow, forfeited if they violate contract terms.

telegram · zaihuapd · Aug 13, 05:10

**Background**: A presidential memorandum is an executive directive that does not require congressional approval. This memo enlists private cybersecurity firms to carry out offensive operations that have traditionally been the exclusive domain of government agencies like the NSA and Cyber Command. The $1 million bond acts as a financial guarantee of compliance. Critics may question the legal basis and accountability of private entities conducting surveillance and attacks abroad.

**Tags**: `#cybersecurity`, `#surveillance`, `#US policy`, `#offensive cyber operations`, `#private sector`

---

<a id="item-8"></a>
## [DeepMind launches SL2T sign language-to-text model on Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 8.0/10

Google DeepMind unveiled SL2T, a large multilingual sign language-to-text model, now available in Gboard and Live Transcribe on Pixel 11 for American Sign Language translation, with more devices and languages to follow. This is the first time a sign language AI model has shipped directly in consumer products, significantly improving accessibility for deaf and hard-of-hearing users. It also demonstrates that on-device, privacy-preserving sign language translation has become practical. SL2T was trained on over 100,000 hours of data spanning more than 50 sign languages and achieves a zero-shot BLEURT score of 70 on the FLEURS-ASL benchmark, far exceeding previous results. For privacy, it analyzes only hand and body pose keypoints, not raw video frames.

telegram · zaihuapd · Aug 13, 08:55

**Background**: Sign language translation to text usually requires vast annotated video datasets. SL2T instead takes a privacy-first approach by estimating body, hand, and face keypoints from video and translating directly from those coordinates. FLEURS-ASL extends the FLEURS speech benchmark to American Sign Language, and BLEURT is a neural metric that scores generated text against a reference. A “zero-shot” result means the model worked on this benchmark without being fine-tuned on it.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/">Putting sign language AI into users’ hands — Google DeepMind</a></li>
<li><a href="https://arxiv.org/html/2408.13585">FLEURS - ASL : Including American Sign Language in Massively...</a></li>
<li><a href="https://github.com/google-research/bleurt">GitHub - google-research/ bleurt : BLEURT is a metric for Natural...</a></li>

</ul>
</details>

**Tags**: `#DeepMind`, `#sign language`, `#translation`, `#accessibility`, `#AI model`

---

<a id="item-9"></a>
## [CXMT Overtakes Tencent as Most Valuable Chinese Company](https://www.bloomberg.com/news/articles/2026-08-13/cxmt-overtakes-tencent-to-become-most-valuable-chinese-company) ⭐️ 8.0/10

ChangXin Memory Technologies \(CXMT\) surpassed Tencent to become China&\#x27;s most valuable listed company, with a market capitalization of about $524 billion. The company listed on Shanghai&\#x27;s STAR Market last month, surged 467% on its first day, and has continued to climb. This marks a major shift in China&\#x27;s tech landscape: a semiconductor memory maker now outranks the country&\#x27;s long-time internet giant. It reflects strong investor demand for domestic chip companies amid China&\#x27;s push for semiconductor self-sufficiency and global supply-chain concerns. CXMT priced its STAR Market IPO at CNY 8.66 per share. Tencent shares fell 4.5% on Thursday and have dropped more than 26% this year as the company aggressively increases AI-related investment.

telegram · zaihuapd · Aug 13, 10:10

**Background**: ChangXin Memory Technologies \(CXMT\) is a Chinese semiconductor company founded in 2016 and headquartered in Hefei, Anhui. It designs and manufactures DRAM memory chips used in mobile phones, PCs, tablets, and servers, and is currently China&\#x27;s largest and the world&\#x27;s fourth-largest DRAM maker. DRAM is a type of volatile memory that temporarily stores data and is essential in nearly every computing device.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ChangXin_Memory_Technologies">ChangXin Memory Technologies</a></li>
<li><a href="https://www.cxmt.com/en/">About cxmt - cxmt</a></li>
<li><a href="https://www.binance.com/en/square/post/344907979167714">#changxintechsetsipopriceatcny8.66 AI Hardware Boom</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#market-cap`, `#China tech`, `#CXMT`, `#Tencent`

---

<a id="item-10"></a>
## [OpenAI Previews Ultrafast Mode, Speeding Up GPT-5.6 Sol by 14x](https://openai.com/index/previewing-ultrafast/) ⭐️ 8.0/10

OpenAI has previewed an Ultrafast mode for GPT-5.6 Sol that delivers up to 14x faster processing than standard, reaching 750 tokens per second on the OpenAI API. The service, powered by Cerebras, is initially available only to a limited set of customers. This speedup could make OpenAI&\#x27;s frontier model practical for latency-sensitive applications such as fraud response, financial research, customer service, and e-commerce. It also signals that Cerebras&\#x27;s wafer-scale hardware is becoming a serious alternative to GPUs for high-speed inference. The Ultrafast mode is currently a limited preview; OpenAI says it will expand access as compute capacity grows. The maximum throughput is 750 tokens per second, a level previously unattainable for a model of this scale on standard infrastructure.

telegram · zaihuapd · Aug 13, 17:04

**Background**: Cerebras is a US-based AI infrastructure company whose Wafer-Scale Engine is purpose-built for fast AI processing, claiming to be much larger and faster than GPUs. GPT-5.6 Sol is OpenAI&\#x27;s flagship model, known for a 1,050,000-token context window and strong performance on coding and agentic workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cerebras.ai/">Cerebras is the go-to platform for fast and effortless AI training.</a></li>
<li><a href="https://www.edenai.co/providers/cerebras">Cerebras API: Models, Pricing &amp; Speed</a></li>
<li><a href="https://openrouter-web.vercel.app/openai/gpt-5.6-sol">GPT - 5 . 6 Sol - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-5`, `#AI performance`, `#Cerebras`, `#API`

---
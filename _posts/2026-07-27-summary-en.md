---
layout: default
title: "Horizon Summary: 2026-07-27 (EN)"
date: 2026-07-27
lang: en
---

> From 29 items, 9 important content pieces were selected

---

1. [vLLM v0.26.0 released with Inkling support and major performance improvements](#item-1) ⭐️ 9.0/10
2. [Moonshot AI Releases 2.8 Trillion Parameter Kimi K3 Model](#item-2) ⭐️ 9.0/10
3. [Critical RCE Vulnerability in Fastjson2 Unpatched in All Versions](#item-3) ⭐️ 9.0/10
4. [Anthropic Clarifies Open-Weights Stance, Supports Mandatory Safety Testing](#item-4) ⭐️ 8.0/10
5. [Judge Rejects Google&\#x27;s DMCA Attempt to Block Scraping](#item-5) ⭐️ 8.0/10
6. [Case study: Replacing React with HTMX for forum UI interactivity](#item-6) ⭐️ 8.0/10
7. [Huawei reportedly plans DRAM fab to secure AI chip memory supply](#item-7) ⭐️ 8.0/10
8. [Google CEO Teases Gemini 4 as Most Ambitious Pre-training Yet](#item-8) ⭐️ 8.0/10
9. [China Begins Mass Production of Domestic DUV Lithography Machines](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 released with Inkling support and major performance improvements](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 introduces full support for the Inkling model family, significant DeepSeek-V4 performance enhancements, fp32 lm\_head for generation models, flexible attention backends, and mature KV offloading and tiered storage. This release substantially expands vLLM&\#x27;s model coverage and inference efficiency, enabling production deployment of cutting-edge multimodal models like Inkling and delivering speedups across AMD, Intel, and NVIDIA hardware. The release includes 411 commits from 212 contributors, featuring specialized routing kernels for DeepSeek-V4 \(2.94% E2E TPOT gain\), Hopper FA4 relative attention for Inkling, per-KV-cache-group attention backend selection, and Transformers 5.13.0 migration for several models.

github · khluu · Jul 27, 01:06

**Background**: vLLM is an open-source library for fast LLM inference and serving, widely used in production. Inkling is a 975B-parameter multimodal Mixture-of-Experts model from Thinking Machines Lab supporting text, image, and audio inputs. FlashAttention-4 \(Hopper FA4\) optimizes attention for Hopper GPUs. MTP \(Multi-Token Prediction\) is a speculative decoding method that predicts multiple tokens per forward pass to boost throughput.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://arxiv.org/html/2603.05451v1">FlashAttention-4: Algorithm and Kernel Pipelining Co-Design ...</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#release`, `#performance`, `#open-source`

---

<a id="item-2"></a>
## [Moonshot AI Releases 2.8 Trillion Parameter Kimi K3 Model](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

Moonshot AI released the weights for its 2.8 trillion parameter Kimi K3 model on Hugging Face under a modified MIT license that imposes revenue-tiered restrictions for large Model-as-a-Service businesses. This release marks the first openly available 3 trillion-parameter-level model, rivaling frontier models from OpenAI and Anthropic, and provides the AI community with a powerful open-weight model for research and deployment. The Kimi K3 model uses 896 experts with 16 activated per token, supports up to 1 million token context, and is natively multimodal \(text, image, video\). The new license requires a separate agreement for any Model-as-a-Service business exceeding $20 million in annual revenue.

rss · Simon Willison · Jul 27, 23:39

**Background**: Open-weight models allow developers to self-host and fine-tune large AI models, but they are not necessarily &\#x27;open source&\#x27; as they may come with usage restrictions. Moonshot AI previously released Kimi K2 under a modified MIT license that required attribution for large commercial entities. Kimi K3 extends this approach with revenue-based licensing for cloud service providers.

<details><summary>References</summary>
<ul>
<li><a href="https://wan27.org/blog/kimi-k3-open-source">Is Kimi K3 Open Source? License, Weights, GitHub, and What ...</a></li>
<li><a href="https://aitoolsrecap.com/Blog/kimi-k3-weights-live-download-huggingface-july-27-2026">Kimi K3 Weights Are Live: Download From HuggingFace, Modified ...</a></li>
<li><a href="https://www.unite.ai/moonshot-opens-kimi-k3-weights-under-a-revenue-tiered-license/">Moonshot Opens Kimi K3 Weights Under a Revenue-Tiered License</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open-source`, `#large language model`, `#weights release`, `#Moonshot AI`

---

<a id="item-3"></a>
## [Critical RCE Vulnerability in Fastjson2 Unpatched in All Versions](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

A remote code execution vulnerability has been disclosed in Fastjson2 up to version 2.0.62, allowing attackers to bypass AutoType checks via malicious JSON data. No official patch is available for any released version. This vulnerability is critical because Fastjson2 is a widely-used Java JSON library, and exploitation could lead to full server compromise. Java developers and security teams must take immediate mitigation steps. The vulnerability affects all versions of Fastjson2 up to 2.0.62, and the maintainer has acknowledged the issue but closed the pull request \(PR \#7695\) without merging it. The only recommended workaround is to completely disable AutoType until a fix is released.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson2 is a high-performance Java JSON library developed by Alibaba, commonly used for serializing and deserializing Java objects. The AutoType feature allows polymorphic type resolution during deserialization, which has historically been a source of remote code execution vulnerabilities when not properly restricted.

<details><summary>References</summary>
<ul>
<li><a href="https://jxausea.medium.com/spring-boot-integrated-fastjson2-quick-start-demo-d3c359a3f33b">Medium</a></li>
<li><a href="https://lilting.ch/en/articles/fastjson-1x-rce-spring-boot-fat-jar">Fastjson CVE-2026-16723: no AutoType , no gadgets... | lilting channel</a></li>
<li><a href="https://kkm-mako.com/en/blog/articles/fastjson-cve/">Fastjson RCE (CVE-2026-16723) puts Spring Boot apps at risk — act...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#fastjson2`, `#RCE`, `#java`

---

<a id="item-4"></a>
## [Anthropic Clarifies Open-Weights Stance, Supports Mandatory Safety Testing](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic published a policy statement clarifying that it does not advocate banning open-weights AI models, but instead supports mandatory safety testing for all sufficiently capable models, both open and closed. This statement reflects the ongoing tension between AI openness and safety, and critics argue that mandatory testing could effectively serve as a barrier to open-weight distribution, especially if costs or administrative hurdles are high. Anthropic&\#x27;s CEO Dario Amodei also endorsed banning chip sales to China and cracking down on smuggling, which some commenters see as contradicting the company&\#x27;s stated position against bans.

hackernews · surprisetalk · Jul 27, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49076057)

**Background**: Open-weights models make the trained neural network weights publicly available, but unlike open-source models, they often do not include the full training code or data. This allows others to run and fine-tune the model, but raises concerns about misuse. The debate about how to regulate such models is central to AI governance discussions.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@aruna.kolluru/exploring-the-world-of-open-source-and-open-weights-ai-aa09707b69fc">Exploring the World of Open Source and Open Weights AI | Medium</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2025/04/open-weight-models/">What are Open Source and Open Weight Models ? | Analytics Vidhya</a></li>

</ul>
</details>

**Discussion**: Community comments are highly critical, accusing Anthropic of hypocrisy and of advocating de facto bans through mandatory testing and chip export controls. Some users point out contradictions between Anthropic&\#x27;s statements on bans and its support for hardware restrictions targeting China.

**Tags**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#AI policy`

---

<a id="item-5"></a>
## [Judge Rejects Google&\#x27;s DMCA Attempt to Block Scraping](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

A federal judge ruled that Google cannot use the DMCA to prevent third parties from scraping its search results, rejecting Google&\#x27;s argument that its search engine results pages are copyrighted compilations. This decision clarifies that search result listings are not subject to copyright protection under the DMCA, preserving the legality of web scraping for research, journalism, and competitive analysis. The ruling stems from a lawsuit where Google accused SerpAPI of scraping its search results; the court found that the selection and arrangement of search results lack the creativity required for copyright protection.

hackernews · cdrnsf · Jul 27, 18:15 · [Discussion](https://news.ycombinator.com/item?id=49073513)

**Background**: Google&\#x27;s business model relies on both scraping the open web and protecting its own data. The DMCA was originally designed to combat piracy, not to restrict data access. This case highlights the tension between copyright law and the openness of the web, especially as Google has deprecated its search API, leaving scraping as the only alternative.

**Discussion**: Commenters noted the irony of Google, built on crawling the web, suing a scraper after removing its own API. Some argued that Google&\#x27;s lawsuit was a bullying tactic against a small company, and that scrapable search results are vital for exposing scams.

**Tags**: `#scraping`, `#DMCA`, `#Google`, `#copyright`, `#legal`

---

<a id="item-6"></a>
## [Case study: Replacing React with HTMX for forum UI interactivity](https://misago-project.org/t/removing-reactjs-from-the-codebase-and-adapting-htmx-for-ui-interactivity/1267/) ⭐️ 8.0/10

A forum software project, Misago, publicly documented its migration from React.js to HTMX for achieving UI interactivity, detailing the practical steps and rationale behind the switch. This case study provides real-world insights into replacing a heavy client-side framework with a lightweight hypermedia-driven approach, which is valuable for developers evaluating simpler alternatives to SPA frameworks. HTMX allows server-rendered HTML snippets to be dynamically swapped into the DOM using custom HTML attributes, eliminating the need for a virtual DOM and reducing client-side complexity.

hackernews · Ralfp · Jul 27, 09:58 · [Discussion](https://news.ycombinator.com/item?id=49067301)

**Background**: HTMX is a small open-source JavaScript library that extends HTML with attributes for AJAX, WebSockets, and CSS transitions, enabling dynamic interfaces without writing JavaScript. Traditional SPAs like React require significant client-side JavaScript for state management and rendering, whereas HTMX offloads logic to the server, simplifying the frontend architecture.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">Htmx</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>

</ul>
</details>

**Discussion**: Commenters largely praised the move, noting that HTMX is well-suited for content-heavy sites like forums. Some shared positive experiences with HTMX in other applications, while one user pointed out performance issues when sending back large HTML fragments. Another recommended alternative tools like PyView.

**Tags**: `#HTMX`, `#React`, `#web development`, `#frontend architecture`, `#server-side rendering`

---

<a id="item-7"></a>
## [Huawei reportedly plans DRAM fab to secure AI chip memory supply](https://www.xda-developers.com/huawei-is-building-its-own-dram-fab-and-it-could-reshape-ram-prices-for-everyone/) ⭐️ 8.0/10

Huawei is reportedly collaborating with Shenzhen-based memory chip company SwaySure to build a 12-inch DRAM wafer fab with a planned monthly capacity of about 140,000 wafers. Huawei has denied the reports, but analysts believe the move is aimed at securing memory supply for its Ascend AI chips. This could reshape the DRAM market by adding significant capacity, potentially lowering prices and reducing reliance on external suppliers like ChangXin Memory Technologies. It also underscores the strategic importance of memory for AI chip performance, especially amid geopolitical tensions. The reported fab would be 12-inch \(300mm\) and target a monthly capacity of 140,000 wafers, which is substantial but would take years to build and ramp production. Huawei has officially denied the plan, so the information remains unconfirmed.

telegram · zaihuapd · Jul 27, 03:17

**Background**: DRAM is a type of volatile memory used as main memory in computers, servers, and AI accelerators; it requires periodic refreshing to retain data. The DRAM market is dominated by three major suppliers: Samsung, SK Hynix, and Micron. Huawei&\#x27;s Ascend AI chips are designed to compete with Nvidia&\#x27;s GPUs for AI workloads and rely on high-bandwidth memory \(HBM\) and DRAM.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Dynamic_random-access_memory">Dynamic random-access memory - Wikipedia</a></li>
<li><a href="https://e.huawei.com/cn/products/computing/ascend">昇腾计算-华为Ascend-AI计算-华为企业业务</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#DRAM`, `#semiconductor`, `#AI chips`, `#supply chain`

---

<a id="item-8"></a>
## [Google CEO Teases Gemini 4 as Most Ambitious Pre-training Yet](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

Google CEO Sundar Pichai announced during the Alphabet Q2 2026 earnings call that Gemini 4 is currently in training, calling it the company&\#x27;s most ambitious pre-training project to date, with an expected release by the end of 2026. This signals Google&\#x27;s continued heavy investment in frontier AI models, potentially setting a new benchmark for large language models and intensifying competition with other AI leaders like OpenAI and Anthropic. Pichai emphasized that compute resources are being prioritized for frontier AGI research, and Gemini 4 is expected to launch in November or December 2026 based on historical release rhythms. Additionally, the Gemini 3.x Flash series will maintain near-monthly iteration cadences focused on coding capabilities.

telegram · zaihuapd · Jul 27, 04:06

**Background**: Gemini is Google&\#x27;s family of large language models \(LLMs\) designed to compete with GPT-4 and other state-of-the-art AI systems. Pre-training refers to the initial phase where a model learns from vast amounts of unlabeled data to develop broad language understanding, which is computationally intensive and often determines the model&\#x27;s capabilities.

**Tags**: `#Google`, `#AI`, `#Gemini`, `#large language models`, `#pre-training`

---

<a id="item-9"></a>
## [China Begins Mass Production of Domestic DUV Lithography Machines](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 8.0/10

China has started mass production of domestically developed immersion deep ultraviolet \(DUV\) lithography machines, with a target of producing about 5 units this year and 20 units by 2027, to be delivered to domestic chipmakers like SMIC and Hua Hong. This marks a significant milestone in China&\#x27;s semiconductor self-sufficiency efforts and could gradually erode ASML&\#x27;s dominance in the Chinese market, especially if Western export controls tighten. The domestic DUV machines still lag behind ASML in performance and reliability; chips require months of testing before adoption. Key components are sourced domestically, but some critical parts still come from Japan, and local supply chain delays have affected progress.

telegram · zaihuapd · Jul 27, 14:10

**Background**: Deep ultraviolet \(DUV\) lithography uses light at 193 nm or 248 nm wavelengths to pattern microchip features, and immersion lithography uses a liquid between the lens and wafer to improve resolution. ASML is the dominant supplier of such machines globally, and China&\#x27;s domestication aims to reduce reliance on foreign technology amid US-led export restrictions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/china-begins-mass-production-of-domestic-immersion-duv-lithography-machines">China begins mass production of homegrown immersion chipmaking machines in major breakthrough, report claims — first DUV lithography units will be delivered this year to SMIC, Hua Hong, and CXMT | Tom&#x27;s Hardware</a></li>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography - Wikipedia</a></li>
<li><a href="https://www.asml.com/en/products/duv-lithography-systems">DUV lithography systems | Products - ASML</a></li>

</ul>
</details>

**Tags**: `#半导体`, `#光刻机`, `#中国芯片`, `#DUV`, `#国产替代`

---
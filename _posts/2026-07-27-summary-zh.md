---
layout: default
title: "Horizon Summary: 2026-07-27 (ZH)"
date: 2026-07-27
lang: zh
---

> 从 29 条内容中筛选出 9 条重要资讯。

---

1. [vLLM v0.26.0 发布，支持 Inkling 模型并大幅提升性能](#item-1) ⭐️ 9.0/10
2. [月之暗面发布 2.8 万亿参数 Kimi K3 模型](#item-2) ⭐️ 9.0/10
3. [Fastjson2 曝未修复的远程代码执行漏洞](#item-3) ⭐️ 9.0/10
4. [Anthropic 阐明开放权重立场：支持强制安全测试](#item-4) ⭐️ 8.0/10
5. [法官驳回谷歌利用 DMCA 阻止数据抓取](#item-5) ⭐️ 8.0/10
6. [案例研究：用 HTMX 替换 React 实现论坛界面交互](#item-6) ⭐️ 8.0/10
7. [华为被指筹建 DRAM 工厂，确保 AI 芯片内存供应](#item-7) ⭐️ 8.0/10
8. [谷歌 CEO 透露 Gemini 4 为迄今最雄心预训练项目](#item-8) ⭐️ 8.0/10
9. [中国开始量产国产 DUV 光刻机](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布，支持 Inkling 模型并大幅提升性能](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 引入了对 Inkling 模型家族的全面支持、DeepSeek-V4 的显著性能提升、生成模型的 fp32 lm\_head、灵活的后端选择，以及成熟的 KV 卸载与分层存储功能。 本次发布大幅扩展了 vLLM 的模型覆盖范围与推理效率，支持 Inkling 等前沿多模态模型的生产部署，并在 AMD、Intel 和 NVIDIA 硬件上实现了速度提升。 该版本包含来自 212 位贡献者的 411 次提交，包括 DeepSeek-V4 专门路由内核（端到端 TPOT 提升 2.94%）、Inkling 的 Hopper FA4 相对注意力、每个 KV 缓存组独立选择注意力后端，以及多个模型迁移至 Transformers 5.13.0。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个用于快速大模型推理和服务的开源库，广泛应用于生产环境。Inkling 是 Thinking Machines Lab 推出的 975B 参数多模态混合专家模型，支持文本、图像和音频输入。FlashAttention-4 \(Hopper FA4\) 针对 Hopper GPU 优化了注意力机制。MTP（多令牌预测）是一种推测解码方法，每次前向传播预测多个令牌以提升吞吐量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://arxiv.org/html/2603.05451v1">FlashAttention-4: Algorithm and Kernel Pipelining Co-Design ...</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#release`, `#performance`, `#open-source`

---

<a id="item-2"></a>
## [月之暗面发布 2.8 万亿参数 Kimi K3 模型](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

月之暗面在 Hugging Face 上发布了其 2.8 万亿参数的 Kimi K3 模型权重，采用修改版 MIT 许可证，对大型模型即服务业务设定了收入分级限制。 此次发布标志着首个公开可用的 3 万亿参数级别模型，可与 OpenAI 和 Anthropic 的前沿模型相媲美，为人工智能社区提供了用于研究和部署的强大开放权重模型。 Kimi K3 模型使用 896 个专家，每个 token 激活 16 个，支持高达 100 万 token 上下文窗口，并原生支持多模态（文本、图像、视频）。新许可证要求，任何年收入超过 2000 万美元的模型即服务企业必须另行签订协议。

rss · Simon Willison · 7月27日 23:39

**背景**: 开放权重模型允许开发者自行托管和微调大型 AI 模型，但不一定是“开源”的，因为它们可能附带使用限制。月之暗面此前在修改版 MIT 许可证下发布了 Kimi K2，要求大型商业实体进行署名。Kimi K3 将此方法扩展到基于收入的云服务提供商许可。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wan27.org/blog/kimi-k3-open-source">Is Kimi K3 Open Source? License, Weights, GitHub, and What ...</a></li>
<li><a href="https://aitoolsrecap.com/Blog/kimi-k3-weights-live-download-huggingface-july-27-2026">Kimi K3 Weights Are Live: Download From HuggingFace, Modified ...</a></li>
<li><a href="https://www.unite.ai/moonshot-opens-kimi-k3-weights-under-a-revenue-tiered-license/">Moonshot Opens Kimi K3 Weights Under a Revenue-Tiered License</a></li>

</ul>
</details>

**标签**: `#AI`, `#open-source`, `#large language model`, `#weights release`, `#Moonshot AI`

---

<a id="item-3"></a>
## [Fastjson2 曝未修复的远程代码执行漏洞](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

长亭科技披露 Fastjson2 2.0.62 及之前版本存在远程代码执行漏洞，攻击者可通过恶意 JSON 数据绕过 AutoType 检查执行任意代码。目前所有已发布版本均无官方补丁。 该漏洞极为严重，因为 Fastjson2 是广泛使用的 Java JSON 处理库，利用漏洞可能导致服务器完全失陷。Java 开发者和安全团队需立即采取缓解措施。 漏洞影响 Fastjson2 2.0.62 及之前所有版本，项目维护者已确认但关闭了 PR \#7695 并未合入主分支。目前唯一推荐的缓解方案是彻底禁用 AutoType，等待正式补丁发布。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson2 是阿里巴巴开发的高性能 Java JSON 库，常用于 Java 对象的序列化和反序列化。AutoType 特性允许在反序列化时解析多态类型，历史上若不加以限制，容易成为远程代码执行漏洞的源头。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jxausea.medium.com/spring-boot-integrated-fastjson2-quick-start-demo-d3c359a3f33b">Medium</a></li>
<li><a href="https://lilting.ch/en/articles/fastjson-1x-rce-spring-boot-fat-jar">Fastjson CVE-2026-16723: no AutoType , no gadgets... | lilting channel</a></li>
<li><a href="https://kkm-mako.com/en/blog/articles/fastjson-cve/">Fastjson RCE (CVE-2026-16723) puts Spring Boot apps at risk — act...</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#fastjson2`, `#RCE`, `#java`

---

<a id="item-4"></a>
## [Anthropic 阐明开放权重立场：支持强制安全测试](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic 发布政策声明，澄清其不主张禁止开放权重 AI 模型，而是支持对所有达到一定能力的模型（包括开放和封闭模型）进行强制性安全测试。 该声明反映了 AI 开放性与安全性之间的持续张力，批评者认为强制测试可能实际上成为开放权重分发的障碍，特别是如果测试成本高昂或行政门槛很高。 Anthropic 的 CEO Dario Amodei 还赞成禁止向中国出售芯片并打击走私，一些评论者认为这与公司反对禁令的立场相矛盾。

hackernews · surprisetalk · 7月27日 22:03 · [社区讨论](https://news.ycombinator.com/item?id=49076057)

**背景**: 开放权重模型公开训练好的神经网络权重，但与开源模型不同，它们通常不包含完整的训练代码或数据。这使得他人可以运行和微调模型，但也引发了对滥用的担忧。如何监管此类模型的辩论是 AI 治理讨论的核心。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@aruna.kolluru/exploring-the-world-of-open-source-and-open-weights-ai-aa09707b69fc">Exploring the World of Open Source and Open Weights AI | Medium</a></li>
<li><a href="https://www.analyticsvidhya.com/blog/2025/04/open-weight-models/">What are Open Source and Open Weight Models ? | Analytics Vidhya</a></li>

</ul>
</details>

**社区讨论**: 社区评论非常批评，指责 Anthropic 言行不一，并通过强制测试和芯片出口管制实际上主张禁令。一些用户指出 Anthropic 关于禁令的声明与其支持针对中国的硬件限制之间存在矛盾。

**标签**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#AI policy`

---

<a id="item-5"></a>
## [法官驳回谷歌利用 DMCA 阻止数据抓取](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

一名联邦法官裁定，谷歌不能利用《数字千年版权法》（DMCA）阻止第三方抓取其搜索结果，驳回了谷歌关于其搜索引擎结果页面属于受版权保护的汇编的主张。 这一裁决明确了搜索结果列表不受 DMCA 版权保护，维护了网络抓取用于研究、新闻和竞争分析的合法性。 该裁决源于谷歌起诉 SerpAPI 抓取其搜索结果的案件；法院认为，搜索结果的选择和编排缺乏版权保护所需的创造性。

hackernews · cdrnsf · 7月27日 18:15 · [社区讨论](https://news.ycombinator.com/item?id=49073513)

**背景**: 谷歌的商业模式既依赖于抓取开放网络，也依赖于保护自身数据。DMCA 最初旨在打击盗版，而非限制数据访问。此案凸显了版权法与网络开放性之间的紧张关系，尤其是在谷歌已弃用其搜索 API、导致抓取成为唯一替代方案的情况下。

**社区讨论**: 评论者指出，谷歌本身靠爬取网络起家，却在移除自家 API 后起诉抓取者，颇具讽刺意味。一些人认为谷歌的诉讼是对小公司的霸凌，而可被抓取的搜索结果对于揭露诈骗至关重要。

**标签**: `#scraping`, `#DMCA`, `#Google`, `#copyright`, `#legal`

---

<a id="item-6"></a>
## [案例研究：用 HTMX 替换 React 实现论坛界面交互](https://misago-project.org/t/removing-reactjs-from-the-codebase-and-adapting-htmx-for-ui-interactivity/1267/) ⭐️ 8.0/10

一个名为 Misago 的论坛软件项目公开记录了其从 React.js 迁移到 HTMX 以实现界面交互的过程，详细说明了切换的步骤和理由。 该案例研究为开发者评估更简单的替代方案提供了有价值的真实世界经验，展示了用轻量级超媒体驱动方法替代繁重客户端框架的可能性。 HTMX 通过自定义 HTML 属性实现服务端渲染的 HTML 片段动态交换到 DOM 中，消除了虚拟 DOM 的需求，降低了客户端的复杂性。

hackernews · Ralfp · 7月27日 09:58 · [社区讨论](https://news.ycombinator.com/item?id=49067301)

**背景**: HTMX 是一个小型开源 JavaScript 库，通过属性扩展 HTML 以支持 AJAX、WebSocket 和 CSS 过渡，无需编写 JavaScript 即可实现动态界面。传统的 SPA（如 React）需要大量客户端 JavaScript 进行状态管理和渲染，而 HTMX 将逻辑卸载到服务器，简化了前端架构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">Htmx</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞这一转变，认为 HTMX 非常适合内容密集型网站（如论坛）。一些人分享了在其他应用中使用 HTMX 的积极体验，而一位用户指出在返回大型 HTML 片段时存在性能问题。另有人推荐了 PyView 等替代工具。

**标签**: `#HTMX`, `#React`, `#web development`, `#frontend architecture`, `#server-side rendering`

---

<a id="item-7"></a>
## [华为被指筹建 DRAM 工厂，确保 AI 芯片内存供应](https://www.xda-developers.com/huawei-is-building-its-own-dram-fab-and-it-could-reshape-ram-prices-for-everyone/) ⭐️ 8.0/10

据报道，华为正与深圳存储芯片企业昇维旭合作，建设一座 12 英寸 DRAM 晶圆厂，规划月产能约 14 万片。华为已否认相关说法，但分析人士认为，此举主要是为了保障其昇腾 AI 芯片的内存供应。 这可能通过增加产能重塑 DRAM 市场，有望降低价格并减少对外部供应商如长鑫存储的依赖。同时凸显了内存对 AI 芯片性能的战略重要性，尤其是在地缘政治紧张的背景下。 报道中的工厂为 12 英寸（300 毫米）晶圆厂，目标月产能 14 万片，规模可观但建设和量产需数年时间。华为已正式否认该计划，因此该信息仍未得到证实。

telegram · zaihuapd · 7月27日 03:17

**背景**: DRAM 是一种易失性存储器，用作计算机、服务器和 AI 加速器的主内存，需要定期刷新以保持数据。DRAM 市场由三星、SK 海力士和镁光三大供应商主导。华为的昇腾 AI 芯片旨在与英伟达 GPU 在 AI 工作负载上竞争，依赖高带宽内存（HBM）和 DRAM。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Dynamic_random-access_memory">Dynamic random-access memory - Wikipedia</a></li>
<li><a href="https://e.huawei.com/cn/products/computing/ascend">昇腾计算-华为Ascend-AI计算-华为企业业务</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#DRAM`, `#semiconductor`, `#AI chips`, `#supply chain`

---

<a id="item-8"></a>
## [谷歌 CEO 透露 Gemini 4 为迄今最雄心预训练项目](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

谷歌 CEO Sundar Pichai 在 Alphabet 2026 年第二季度财报电话会议上透露，下一代大模型 Gemini 4 已投入训练，称这是该公司迄今为止最具雄心的预训练项目，预计于 2026 年底发布。 这表明谷歌继续大力投资前沿 AI 模型，可能为大型语言模型树立新标杆，并加剧与 OpenAI 和 Anthropic 等其他 AI 领导者的竞争。 Pichai 强调算力将优先分配给前沿 AGI 研发，按往年节奏，Gemini 4 预计在 2026 年 11 月或 12 月发布。此外，Gemini 3.x Flash 系列将保持几乎每月一次的迭代频率，重点提升智能编码能力。

telegram · zaihuapd · 7月27日 04:06

**背景**: Gemini 是谷歌推出的大型语言模型（LLM）系列，旨在与 GPT-4 及其他最先进的 AI 系统竞争。预训练是指模型从大量无标签数据中学习以发展广泛语言理解的初始阶段，这一过程计算密集且通常决定模型的能力。

**标签**: `#Google`, `#AI`, `#Gemini`, `#large language models`, `#pre-training`

---

<a id="item-9"></a>
## [中国开始量产国产 DUV 光刻机](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 8.0/10

中国已开始量产自主研发的浸没式深紫外（DUV）光刻机，目标是今年生产约 5 台，2027 年约 20 台，将交付给中芯国际、华虹半导体等国内芯片制造商。 这标志着中国半导体自给自足努力的重要里程碑，可能逐步削弱 ASML 在中国市场的主导地位，尤其是在西方收紧出口管制的情况下。 国产 DUV 光刻机在性能和可靠性上仍落后于 ASML；芯片商需数月测试才能采用。关键部件主要来自国内，但部分关键零件仍来自日本，且本土供应链延误已影响进度。

telegram · zaihuapd · 7月27日 14:10

**背景**: 深紫外（DUV）光刻技术使用 193 纳米或 248 纳米波长的光来刻画芯片特征，浸没式光刻在透镜和晶圆之间加入液体以提高分辨率。ASML 是全球此类设备的主导供应商，中国旨在通过国产化减少对国外技术的依赖，以应对美国主导的出口限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/china-begins-mass-production-of-domestic-immersion-duv-lithography-machines">China begins mass production of homegrown immersion chipmaking machines in major breakthrough, report claims — first DUV lithography units will be delivered this year to SMIC, Hua Hong, and CXMT | Tom&#x27;s Hardware</a></li>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography - Wikipedia</a></li>
<li><a href="https://www.asml.com/en/products/duv-lithography-systems">DUV lithography systems | Products - ASML</a></li>

</ul>
</details>

**标签**: `#半导体`, `#光刻机`, `#中国芯片`, `#DUV`, `#国产替代`

---
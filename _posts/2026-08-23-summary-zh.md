---
layout: default
title: "Horizon Summary: 2026-08-23 (ZH)"
date: 2026-08-23
lang: zh
---

> 从 30 条内容中筛选出 6 条重要资讯。

---

1. [复杂系统如何失败：1998 年经典论文论述失败的必然性](#item-1) ⭐️ 9.0/10
2. [英伟达 60 亿美元授权 Poolside 技术，打造开源权重 AI 模型](#item-2) ⭐️ 9.0/10
3. [什么是 Harness？LLM 智能体的编排层](#item-3) ⭐️ 8.0/10
4. [ShardFlow 借助投机解码与 CUDA Graphs 在跨云区域实现 Qwen2.5-7B 28 TPS](#item-4) ⭐️ 8.0/10
5. [乌兰察布成中国 AI 算力热土，承诺容量 12.5 吉瓦](#item-5) ⭐️ 8.0/10
6. [微软悄悄部署应用，强制 Windows 11 默认搜索为 Bing](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [复杂系统如何失败：1998 年经典论文论述失败的必然性](https://how.complexsystems.fail/) ⭐️ 9.0/10

1998 年的经典文章《复杂系统如何失败》被发布到 Hacker News 后引发广泛讨论，获得了 9.0 分、212 个点赞和 58 条评论。文章指出，失败是复杂系统的固有属性，而传统的根因分析往往具有误导性。 这篇文章是韧性工程领域的奠基之作，深刻影响了软件工程师处理分布式系统、事故复盘和混沌工程的方式。它将失败重新定义为系统级现象而非个人失误，从而塑造了现代站点可靠性工程（SRE）的实践。 文章认为，复杂系统大部分时间都处于降级运行状态，失败源于正常运行过程，而事后将事故归因于单一根因通常是一种徒劳。它还指出，无失败运行需要以失败经验为基础，这一原则直接启发了混沌工程。

hackernews · shortcrct · 8月23日 15:13 · [社区讨论](https://news.ycombinator.com/item?id=49409473)

**背景**: 韧性工程是安全科学的一个子领域，研究复杂适应系统如何应对意外情况，重点关注系统预判、监控、响应和学习的能力。常态事故理论同样认为，在交互复杂且紧密耦合的系统中，事故是不可避免的。这些思想为文章的核心主张——失败无法通过设计消除，只能被理解和应对——提供了理论背景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Resilience_engineering">Resilience engineering</a></li>
<li><a href="https://psychsafety.com/normal-accidents/">Normal Accidents - Psych Safety</a></li>

</ul>
</details>

**社区讨论**: 从业者们对这篇文章给予高度评价：tptacek 称其极为重要，并强调对复杂系统进行根因分析是徒劳；jedberg 指出它直接启发了混沌工程的创立。还有评论者推荐了 John Gall 的《系统学》（Systemantics），也有人指出开头句子中似乎存在笔误。整体讨论情绪非常积极。

**标签**: `#complex systems`, `#resilience engineering`, `#failure analysis`, `#distributed systems`, `#systems thinking`

---

<a id="item-2"></a>
## [英伟达 60 亿美元授权 Poolside 技术，打造开源权重 AI 模型](https://www.wsj.com/tech/ai/nvidia-is-spending-6-billion-to-build-a-powerful-u-s-alternative-to-chinese-ai-c51c38cc) ⭐️ 9.0/10

英伟达已同意以 120 亿美元投前估值向 AI 初创公司 Poolside 投资 10 亿美元，并支付 60 亿美元获得其技术授权及吸纳大部分工程师。超过 100 名 Poolside 员工将加入英伟达，参与开源权重模型 Nemotron 项目。 这笔交易标志着英伟达从主要销售 AI 硬件转向构建前沿 AI 模型，加剧了与 DeepSeek、Kimi 等中国开源权重实验室以及 OpenAI、Anthropic 等美国闭源模型公司的竞争。这可能重塑开源权重生态系统，使英伟达占据领先地位。 交易包括以 120 亿美元投前估值进行的 10 亿美元股权投资，外加 60 亿美元授权费，超过 100 名 Poolside 员工将加入英伟达。英伟达计划利用该技术打造全球最强开源权重模型之一，目标是 DeepSeek 和 Kimi K3。

telegram · zaihuapd · 8月23日 04:20

**背景**: 开放权重模型公开发布训练后的参数，任何人都可以下载和修改，这与闭源模型不同。英伟达的 Nemotron 系列是一组开放权重和训练配方的开源模型，旨在构建 AI 智能体。Poolside 由前 GitHub CTO Jason Warner 于 2023 年创立，专注于软件开发及通用工作的基础模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Poolside_AI">Poolside AI - Wikipedia</a></li>
<li><a href="https://developer.nvidia.com/topics/ai/nemotron">Nemotron AI Models | NVIDIA Developer</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI`, `#Open-Source Models`, `#Investment`, `#Competition`

---

<a id="item-3"></a>
## [什么是 Harness？LLM 智能体的编排层](https://earendil.com/posts/what-is-a-harness/) ⭐️ 8.0/10

《What Is a Harness?》一文将 harness 定义为管理 LLM 智能体的编排与控制层，把模型输出转化为可靠的软件行为。文章认为，harness 的设计（而非仅靠模型本身）决定了智能体能否被高效构建和运行。 随着 LLM 智能体从演示走向生产，harness 成为实现可控性、调试和工具调用的关键基础设施。构建智能体系统的工程师需要关于这一层的共同词汇和模式，因此这个概念对 AI 工程社区来说具有及时性和重要意义。 作者把 harness 比作底盘、模型比作发动机、token 比作燃料、智能体比作汽车。评论者补充了实践细节：内部 CLI 对智能体非常有用，而像 Pi 这样的扩展系统可以把 harness 变成灵活的平台。

hackernews · tosh · 8月23日 14:24 · [社区讨论](https://news.ycombinator.com/item?id=49409092)

**背景**: 大语言模型（LLM）是在海量文本上训练的 AI 模型，能够生成、总结和分析语言。LLM 智能体利用模型进行推理并采取行动，常常调用工具，但如果缺少额外结构，它只会“继续生成”。Harness 就是执行控制层，能把智能体变成可控的软件系统，通常负责工具调用、记忆、步骤边界和外部集成。这一模式在 AI 工程领域越来越受关注，被视为对模型选择的重要补充。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://gist.github.com/manhay212/1611ddd826ef0ac8dc5719baadaf7cbe">The Harness Matters More Than the Model — patterns for building...</a></li>
<li><a href="https://blog.ayqy.net/en/articles/harness-design-for-ai-agents/">Harness Design For AI Agents : Why harness affects delivery more...</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了实践经验，例如为会计智能体构建基于 CLI 的 harness，并发现内部 CLI 既有趣又非常实用。有用户询问在终端、团队成员和模型之间的交接（handoff）能力，也有人认为 harness 才是真正的价值提供者，并称赞 Pi 的扩展系统。作者也参与了讨论，提出底盘/发动机的类比并询问大家是否认同。

**标签**: `#LLM`, `#agents`, `#orchestration`, `#harness`, `#AI infrastructure`

---

<a id="item-4"></a>
## [ShardFlow 借助投机解码与 CUDA Graphs 在跨云区域实现 Qwen2.5-7B 28 TPS](https://www.reddit.com/r/MachineLearning/comments/1vw5ysj/28_tps_on_qwen257b_across_two_separate_cloud/) ⭐️ 8.0/10

ShardFlow 作为一个新的分布式推理框架，在 GCP 两个不同区域、通过公共广域网（约 86ms RTT）连接的两个 T4 节点上，对 Qwen2.5-7B 实现了 28.10 TPS 峰值和 20.31 TPS 平均吞吐。它结合了神经投机解码与 CUDA Graphs 来缓解广域网延迟。 这一结果表明，在地理位置分离的云区域之间进行分布式 LLM 推理是可行的，有可能降低依赖多个数据中心的基础设施成本。同时验证了投机解码能有效将逐 token 的广域网延迟转化为每轮往返成本，对延迟敏感的推理场景意义重大。 基准测试采用 K=8 草稿，每轮往返接受 4.07 个 token；CUDA Graphs 优化捕获了完整的 0.5B 前向传播，将草稿延迟从 112ms 降至 25ms。其他技术细节包括零拷贝 Rust TCP 中继、支持图兼容的 StaticCache 和就地 KV 回退，以及避免 CPU 内存溢出的 meta-device 模型切片。该框架在同样的两个节点上，对 Qwen2.5-14B（NF4 4 位量化）实现了 14.43 TPS 的平均吞吐。

reddit · r/MachineLearning · /u/katua\_bkl · 8月23日 12:30

**背景**: 投机解码是一种推理时优化技术：一个小型辅助模型生成草稿 token，再由大模型进行验证，其结果与贪心解码完全一致，同时降低延迟。CUDA Graphs 通过将一系列 GPU 操作捕获为单个图并以一次启动重放，减少 CPU 端的 kernel 启动开销。ShardFlow 是一个通用的分布式推理框架，可自动将任意 HuggingFace transformer 分区到多台 GPU 机器，并提供 OpenAI 兼容端点。云区域之间的广域网延迟通常较高，使得分布式推理具有挑战性；投机解码通过将延迟移出逐 token 的关键路径来缓解问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/rautaditya2606/Shardflow">GitHub - rautaditya2606/ Shardflow</a></li>
<li><a href="https://docs.nvidia.com/cuda/cuda-programming-guide/04-special-topics/cuda-graphs.html">4.2. CUDA Graphs — CUDA Programming Guide</a></li>
<li><a href="https://developers.redhat.com/articles/2026/06/12/how-speculative-decoding-delivers-faster-llm-inference">How speculative decoding delivers faster LLM inference | Red Hat Developer</a></li>

</ul>
</details>

**标签**: `#distributed inference`, `#speculative decoding`, `#CUDA Graphs`, `#LLM inference`, `#performance optimization`

---

<a id="item-5"></a>
## [乌兰察布成中国 AI 算力热土，承诺容量 12.5 吉瓦](https://www.wired.com/story/the-unlikely-place-at-the-center-of-chinas-ai-boom/) ⭐️ 8.0/10

内蒙古乌兰察布已成为中国重要的 AI 算力中心，中企承诺的数据中心容量达 12.5 吉瓦，超过 OpenAI 星际之门项目规划的 10 吉瓦。其中超过 70%的容量是在过去一年内宣布的。 如此大规模的 AI 基础设施投资表明中国正在积极发展 AI 算力，可能在模型训练和部署方面获得战略优势。这也凸显了全球在偏远低成本地区建设大型数据中心的趋势，带来了能源和环境方面的重大问题。 自 2016 年以来，乌兰察布已有近 100 个数据中心开业或开工，包括 DeepSeek、字节跳动、阿里和小红书自建的数据中心。该地区的高寒气候、低电价和邻近北京是主要吸引力，但缺水问题令人担忧：年降水量仅约 14 英寸，最近当地水厂被迫每晚停水 7 小时。

telegram · zaihuapd · 8月23日 00:55

**背景**: AI 数据中心需要大量电力来驱动服务器和冷却系统。乌兰察布的高寒气候和低廉电价使其成为有吸引力的选址，但当地约 37%的电力仍来自煤电。Stargate 是 OpenAI、软银、甲骨文和 MGX 联合开展的人工智能基础设施项目，计划筹集 5000 亿美元，其中 1000 亿美元立即部署，其余在四年内逐步到位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aol.com/know-stargate-openais-venture-announced-175055247.html">What to Know About &#x27; Stargate ,&#x27; OpenAI &#x27;s New Venture Announced by....</a></li>
<li><a href="https://www.linkedin.com/posts/deepakpros_stargateproject-openai-oracle-activity-7296196541579464705-gcRw">#stargateproject # openai #oracle #ai #nvidia | Deepak Wadhwani</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data centers`, `#China`, `#computing power`, `#energy`

---

<a id="item-6"></a>
## [微软悄悄部署应用，强制 Windows 11 默认搜索为 Bing](https://www.windowslatest.com/2026/08/22/microsoft-built-a-dedicated-app-that-forces-bing-everywhere-on-windows-11-including-chrome-firefox-and-brave/) ⭐️ 8.0/10

微软发布了一款名为“Microsoft Recommended Search Settings”的独立应用，会自动将 Windows 11 上 Chrome、Firefox 和 Brave 的默认搜索引擎改为 Bing。该应用托管在微软官方服务器，绕过 Windows Update 和应用商店，安装后会跳转至 Microsoft Rewards。 此举加强了微软引导用户使用 Bing 的力度，引发反竞争担忧，并影响偏好其他搜索引擎的数百万 Windows 用户。这也凸显了浏览器默认搜索领域持续存在的竞争，该问题已受到监管机构关注。 测试中，Chrome 会弹出提示询问用户是否恢复 Google 搜索，而微软则添加了“等等，别换回去”的消息以挽留用户。相关 Bing 扩展程序显示已有 500 万用户，但尚不清楚实际安装该应用的人数。

telegram · zaihuapd · 8月23日 05:18

**背景**: 默认搜索引擎决定了浏览器在搜索时使用哪个服务，大多数浏览器都允许用户自行设置。微软此前曾通过 Edge 和 Windows 提示来鼓励用户使用 Bing，但这款独立应用代表了更激进的策略。据报道，该应用未通过标准分发渠道就出现在设备上，可能会让用户措手不及。这也是大型科技公司之间浏览器默认设置之争的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Microsoft">Microsoft - Wikipedia</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-products-and-apps">Microsoft products, apps, and devices built to support you</a></li>

</ul>
</details>

**标签**: `#Microsoft`, `#Bing`, `#Browser`, `#Default Search`, `#Anti-competitive`

---
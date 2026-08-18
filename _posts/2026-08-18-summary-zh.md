---
layout: default
title: "Horizon Summary: 2026-08-18 (ZH)"
date: 2026-08-18
lang: zh
---

> 从 31 条内容中筛选出 5 条重要资讯。

---

1. [Mojo 语言现以 Apache 2.0 许可证开源](#item-1) ⭐️ 9.0/10
2. [亚马逊税：搜索沦为营销工具](#item-2) ⭐️ 8.0/10
3. [Linux 7.3 提升 VRAM 超量分配性能](#item-3) ⭐️ 8.0/10
4. [实地研究发现数据中心废热使下风向气温升高约 0.8°C](#item-4) ⭐️ 8.0/10
5. [Qwen 3.8 27B 在 AI 指数上追平 GPT-5.6 Luna](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Mojo 语言现以 Apache 2.0 许可证开源](https://simonwillison.net/2026/Aug/18/mojo-is-now-open-source/) ⭐️ 9.0/10

Modular 在发布 Mojo 1.0 后不久，便以 Apache 2.0 许可证开源了 Mojo 编译器与工具链。这兑现了 Mojo 于 2023 年 5 月首次公布时所作的开源承诺。 Mojo 旨在让 GPU 编程像 Python 一样简单，同时提供系统级性能，因此对 AI 和高性能计算领域极具意义。以宽松许可证开源编译器，有望加速社区采用、提升透明度，并影响 Python 生态周边语言工具的发展。 Mojo 最初想成为 Python 完整超集的目标在 2025 年 8 月左右被放弃，现在它可以独立发展，尽管 AI 辅助工具可以帮助将 Python 代码迁移到 Mojo。Mojo 采用类 Python 语法，但与现有 Python 代码并非完全兼容，并针对 GPU 编程进行了优化。

rss · Simon Willison · 8月18日 21:39

**背景**: Mojo 是一种面向 Linux 和 macOS 的系统编程语言，将静态类型和借用检查器等受 Rust 启发的特性与类 Python 语法相结合。它旨在成为跨越计算栈（从底层硬件到高层 AI 工作负载）进行编程的统一语言。以 Apache 2.0 许可证开源，意味着任何人都可以审查、修改并为编译器和工具链做贡献。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mojo_%28programming_language%29">Mojo ( programming language ) - Wikipedia</a></li>
<li><a href="https://mojolang.org/">Mojo</a></li>

</ul>
</details>

**标签**: `#mojo`, `#open-source`, `#programming-language`, `#compiler`, `#python`

---

<a id="item-2"></a>
## [亚马逊税：搜索沦为营销工具](https://seths.blog/2026/08/the-amazon-tax/) ⭐️ 8.0/10

赛斯·戈丁在 2026 年 8 月的博文中指出，亚马逊的搜索结果已变成一种“亚马逊税”，平台优先考虑自身商业利益，而非提供顾客真正想要的结果。文章强调，赞助广告和推广列表正在削弱亚马逊搜索的实用性。 这之所以重要，是因为亚马逊是数百万消费者默认的商品搜索引擎，它从“相关性优先”转向“变现优先”会扭曲消费者选择并推高实际成本。这也反映了整个行业的趋势——平台搜索正变成广告位，影响信任和用户体验。 这篇文章用“亚马逊税”来描述顾客和卖家承担的隐性成本——自然搜索结果被赞助列表挤到下方。评论者反映，某些亚马逊搜索结果中多达四分之三是赞助广告，连最好的空气炸锅厂商也不得不参与广告竞价来保住销量。

hackernews · herbertl · 8月18日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49345263)

**背景**: 亚马逊的搜索排名由 A9 等算法驱动，传统上基于相关性、销量历史、评论和定价来对商品排序。近年来，亚马逊加入了更多信号，如客户满意度、库存管理和个性化行为，同时也在搜索结果中整合了赞助商品。这种自然结果与付费展示的混合，导致越来越多批评认为搜索现在更服务于亚马逊的广告业务，而非顾客的真实意图。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://epinium.com/en/blog/amazon-a9-algorithm-2/">Amazon A 9 Algorithm Guide | Epinium</a></li>
<li><a href="https://amazoniac.agency/amazon-ranking-factors/">Amazon Ranking Factors: What Matters Most for Organic Visibility</a></li>
<li><a href="https://sellerise.com/blog/what-actually-makes-amazon-rank-your-product-higher/">What Actually Makes Amazon Rank Your Product Higher in 2026 - Sellerise</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者普遍赞同戈丁的观点，称亚马逊搜索“几乎完全不可用”，并指出搜索已从“找到准确商品”变成“展示平台希望你购买的商品”。有人分享了自己转向 Etsy 等平台的行为，也有评论者提出更中立的看法，认为广告有时也能提供相关性，比如在搜索丰田 RAV4 时出现马自达 CX-50 的广告。

**标签**: `#Amazon`, `#Search`, `#Advertising`, `#E-commerce`, `#User Experience`

---

<a id="item-3"></a>
## [Linux 7.3 提升 VRAM 超量分配性能](https://pixelcluster.dev/VRAM-Overcommit/) ⭐️ 8.0/10

Linux 内核 7.3 针对 VRAM 过度分配场景引入了显著的性能改进，即 GPU 内存需求超过物理显存时的情况。该更新减少了应用程序耗尽显存时的卡顿和冻结问题，受到 Linux 游戏与图形社区的强烈期待。 这一点很重要，因为 VRAM 超量分配是 Linux 游戏和 GPU 计算的常见痛点；当显存耗尽时，性能可能急剧下降。通过改进这一路径，Linux 在高性能图形工作负载中变得更具可用性，缩小了与 Windows 在类似场景下的差距。 据称，这些改进包括更好地处理内存碎片化，以及更高效地在显存与系统内存之间进行分页。社区讨论指出，驱动程序的支持仍然参差不齐——尤其是 Nvidia 缺乏完整的分页支持，有人建议内核侧可以进行额外的碎片整理。

hackernews · flaburgan · 8月18日 07:51 · [社区讨论](https://news.ycombinator.com/item?id=49342719)

**背景**: VRAM 超量分配发生在 GPU 应用程序请求的视频内存超过显卡物理可用显存时；此时驱动会使用系统内存作为溢出，即一种分页形式。Linux 历来对此处理不佳，导致冻结和卡顿，而 7.3 更新正是为了解决这一问题。Linux 内核还有一套针对系统内存的独立超量分配策略，由 vm.overcommit\_memory 控制，但 GPU 显存的超量分配由驱动特有的逻辑处理。该文章指出，VRAM 超量分配的支持自 GPU 驱动出现以来就已存在，但性能一直时好时坏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pixelcluster.dev/VRAM-Overcommit/">VRAM Management Part 2: Beyond the Limits of Physical VRAM | pixelcluster&#x27;s GPU blog</a></li>
<li><a href="https://www.kernel.org/doc/Documentation/vm/overcommit-accounting">The Linux kernel supports the following overcommit handling modes</a></li>

</ul>
</details>

**社区讨论**: 社区反响热烈——用户赞赏内核开发的速度，并将其与 Windows 更新进行有利对比。不过，也有人对 Nvidia 缺乏分页支持表示担忧，并建议内核进一步进行虚拟内存碎片整理。有评论提到了作者观察到年轻跨性别人群对底层性能工程的贡献，获得了不少赞同回应。

**标签**: `#Linux`, `#kernel`, `#VRAM`, `#performance`, `#graphics`

---

<a id="item-4"></a>
## [实地研究发现数据中心废热使下风向气温升高约 0.8°C](https://asmedigitalcollection.asme.org/sustainablebuildings/article/7/2/024501/1233035/Data-Center-Waste-Heat-as-an-Emerging-Urban) ⭐️ 8.0/10

研究人员发布了在亚利桑那州凤凰城都市区进行的数据中心社区尺度气温影响的首批实地测量结果。他们观察到下风向平均气温升高约 0.8°C，影响范围延伸约 500 米。 这项研究提供了确凿的实地数据，证实数据中心是局部热源，可能增加周边社区的制冷需求和热暴露。研究结果对城市规划、数据中心选址和可持续发展政策具有重要意义，尤其是在凤凰城这样酷热的地区。 观测到的温差（ΔT）约 0.8°C 出现在设施下风向，平均气温从 42.7°C 升至 43.5°C。对同一项目的其他分析报告显示，峰值升温可达 4°F（约 2.2°C），在下风向三分之一英里（约 536 米）范围内均可检测到影响。

hackernews · cwwc · 8月18日 17:24 · [社区讨论](https://news.ycombinator.com/item?id=49349147)

**背景**: 数据中心消耗大量电力为服务器供电，计算和冷却系统产生的废热通常排入周围空气。当大量数据中心集中在城市区域时，这些废热会加剧城市热岛效应，使局部气温升高。凤凰城都市区是重要的数据中心枢纽，同时属于炎热的沙漠气候，是研究热影响的理想地点。这项研究是利用实地观测直接测量数据中心社区尺度温度影响的首批研究之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://asmedigitalcollection.asme.org/sustainablebuildings/article/7/2/024501/1233035/Data-Center-Waste-Heat-as-an-Emerging-Urban">Data Center Waste Heat as an Emerging Urban Thermal Hazard: First Field Measurements of Neighborhood-Scale Air Temperature Impacts | J. Eng. Sustain. Bldgs. Cities | ASME Digital Collection</a></li>
<li><a href="https://news.asu.edu/20260518-environment-and-sustainability-turning-down-heat-data-centers">Turning down the heat from data centers | ASU News</a></li>
<li><a href="https://techxplore.com/news/2026-05-centers-nearby-temperatures-degrees-phoenix.html">Data centers raise nearby temperatures by up to 4 degrees in Phoenix</a></li>

</ul>
</details>

**社区讨论**: 评论区既有怀疑也有理性讨论。一些用户质疑对数据中心的担忧是否被夸大或出于政治目的，另一些人指出实测约 0.8°C 的平均升温比标题暗示的要小。少数评论者哀叹该话题容易引发两极化和意识形态化的争论，还有人指出与炼油厂和加油站相比，对数据中心的关注不成比例。

**标签**: `#data centers`, `#urban heat`, `#sustainability`, `#climate`, `#environment`

---

<a id="item-5"></a>
## [Qwen 3.8 27B 在 AI 指数上追平 GPT-5.6 Luna](https://simonwillison.net/2026/Aug/17/qwen-38-27b-scores-52/) ⭐️ 8.0/10

27B 参数的 Qwen 3.8 27B 在 Artificial Analysis Intelligence Index 上获得 52 分，追平 GPT-5.6 Luna（最高分），仅比分别为 753B 和 1.7T 参数的 GLM-5.2 与 DeepSeek V4 Pro 低 1 分。 这一结果表明，相对较小的开源权重模型可以匹敌其数倍规模的边缘模型，标志着一次重大效率突破，可能降低高级 AI 能力的成本并扩大其可获得性。 Artificial Analysis Intelligence Index 综合衡量推理、编程、知识、指令遵循、科学推理和多步任务等能力。Qwen 3.8 27B 还支持视觉与推理，提供 256K 上下文窗口，并可在 17GB 内存/显存的本地设备上运行。

rss · Simon Willison · 8月17日 23:58

**背景**: Qwen 3.8 是阿里巴巴 Qwen 团队在 2026 年推出的新模型系列，包含 27B 等版本。GPT-5.6 Luna 是 OpenAI 于 2026 年 7 月发布的 GPT-5.6 系列中最具成本效益的型号。这一基准对比突显了较小模型正逐步缩小与更大规模前沿系统之间的差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index">Artificial Analysis Intelligence Index</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>
<li><a href="https://unsloth.ai/docs/models/qwen3.8">Qwen3.8 - How to Run Locally | Unsloth Documentation</a></li>

</ul>
</details>

**标签**: `#qwen`, `#llms`, `#benchmark`, `#ai`, `#efficiency`

---
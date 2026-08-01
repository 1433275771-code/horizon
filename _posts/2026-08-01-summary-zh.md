---
layout: default
title: "Horizon Summary: 2026-08-01 (ZH)"
date: 2026-08-01
lang: zh
---

> 从 38 条内容中筛选出 6 条重要资讯。

---

1. [OpenAI 的 Astra 破解十道长期未解数学难题](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4-Flash-0731：304B 参数智能体模型，性价比突出](#item-2) ⭐️ 9.0/10
3. [EA 以 550 亿美元卖身沙特财团，下周完成](#item-3) ⭐️ 9.0/10
4. [微软确认今年推出 Copilot「超级应用」](#item-4) ⭐️ 9.0/10
5. [NetBSD 11.0 发布，带来 MicroVM 内核和更新的 NPF 防火墙](#item-5) ⭐️ 8.0/10
6. [研究探究 KataGo 神经网络内部如何学习对称性](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 的 Astra 破解十道长期未解数学难题](https://simonwillison.net/2026/Aug/1/ten-advances-in-mathematics/#atom-everything) ⭐️ 9.0/10

2026 年 8 月 1 日，OpenAI 宣布其下一代模型家族 Astra 的内部版本解决了数学与理论计算机科学中的十个开放问题，每个问题在 GPT-5.6 Sol token 价格下花费不到 2000 美元。相关成果包含 openai/ten-proofs 仓库中的 Lean 4 形式化证明以及一篇描述解法的论文。 这可能标志着 AI 推理能力的重大进步，表明大语言模型能够产生真正的数学发现。它还可能加速向陶哲轩所说的“大数学”转型，即人类与 AI 协作，由机器承担大量技术性基础工作。 这些解决的难题涵盖高维球体堆积、非索菲克群、Connes 刚性猜想、算术电路下界、量子平行重复、最近向量问题以及多色 Ramsey 数。OpenAI 没有披露有多少问题尝试后未获成功；此外，该公司还发布了一份由 LLM 生成的 PDF，模型基于未公开的推理轨迹重建证明的来龙去脉。

rss · Simon Willison · 8月1日 20:34

**背景**: 像 Lean 4 这样的形式化证明验证系统可以让计算机逐行检查数学证明的正确性，提供比传统同行评审更强的保障。OpenAI 表示，数学模型自行生成了数学论证，而人类负责整理这些论证并将其形式化为 Lean 代码。这延续了前沿 AI 实验室展示研究能力的趋势——此前 Anthropic 声称 Claude 借助 Mythos Preview 以约 10 万美元的 token 成本发现了加密弱点。这一事件的文化冲击让人联想到 1997 年深蓝战胜国际象棋世界冠军，在数学界引发了存在主义的疑问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://the-decoder.com/openai-announces-its-next-major-model-astra-by-dropping-ten-previously-unsolved-math-solutions/">OpenAI announces its &quot;next major model&quot; Astra by dropping ten ...</a></li>
<li><a href="https://www.bitsminds.com/news/openai-astra-ten-open-math-problems-lean-proofs-2026">OpenAI Names Its Next Model Family Astra — and Says It Solved Ten ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#mathematics`, `#OpenAI`, `#research`, `#theoretical computer science`

---

<a id="item-2"></a>
## [DeepSeek V4-Flash-0731：304B 参数智能体模型，性价比突出](https://simonwillison.net/2026/Jul/31/deepseek-v4-flash-0731/#atom-everything) ⭐️ 9.0/10

DeepSeek 发布了 DeepSeek-V4-Flash-0731，这是一款拥有 3040 亿参数、智能体能力大幅增强的模型。该模型已在 Hugging Face 和 OpenRouter 上提供，输入价格每百万 tokens 0.14 美元，输出价格每百万 tokens 0.27 美元。 Artificial Analysis 将其排在 MiniMax M3（4280 亿参数）之前，尽管其规模更小，而其定价使其目前可能是最具智能性价比的模型。这可能会加剧大语言模型市场的价格竞争，并让开发者更容易获得先进的智能体 AI。 该模型在 Hugging Face 上的大小为 167GB，并支持可调的推理强度；Simon Willison 通过 OpenRouter 将 reasoning\_effort 设为 high 后，输出质量显著提升。在 Artificial Analysis 的智能指数与成本对比图中，它以约 0.028 美元/任务和 50 分的智能得分独自位于最具吸引力的象限。

rss · Simon Willison · 7月31日 23:59

**背景**: 智能体能力（agentic capabilities）指的是大语言模型自主规划并执行多步骤任务的能力，例如搜索文件、编写代码、运行测试并完善输出，而无需人类持续监督。Artificial Analysis 智能指数是一个综合基准，衡量推理、编程、知识、指令遵循、科学推理和多步任务完成能力。此次发布是 DeepSeek V4 系列的一部分，其出色的性价比凸显了高性价比开源权重模型的快速进步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://labs.adaline.ai/p/what-are-agentic-llms-a-comprehensive">What Are Agentic LLMs? Use Cases, Risks, and How They Work</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-ai">What is Agentic AI? | IBM</a></li>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index">Artificial Analysis Intelligence Index</a></li>

</ul>
</details>

**标签**: `#deepseek`, `#ai`, `#language-models`, `#llm`, `#model-release`

---

<a id="item-3"></a>
## [EA 以 550 亿美元卖身沙特财团，下周完成](https://www.gamersky.com/news/202607/2180618.shtml) ⭐️ 9.0/10

EA 宣布以 550 亿美元出售给由沙特公共投资基金（PIF）领衔、银湖资本和 Affinity Partners 参与的财团，交易已获全部监管批准。预计 2026 年 8 月 4 日完成，届时 EA 将转为私营公司，不再公开财务数据。 这是游戏史上第二大收购案，仅次于 2023 年微软以 754 亿美元收购动视暴雪。主权财富基金掌控全球最大游戏发行商之一，标志着行业格局发生重大变化，可能改写竞争态势和未来投资方向。 收购财团由沙特公共投资基金（PIF）、银湖资本和 Affinity Partners 组成。交易完成后 EA 将成为私营公司，财务数据不再对外公开。PIF 此前已全资收购 Scopely、Niantic 等开发商，持续扩大在游戏领域的布局。

telegram · zaihuapd · 8月1日 09:10

**背景**: 沙特公共投资基金（PIF）成立于 1971 年，是沙特的主权财富基金，为具有战略意义的商业项目提供融资。银湖资本是专注于科技及科技赋能投资的知名私募股权公司。这笔交易延续了主权基金和大型私募进军游戏业的趋势；2023 年微软以 754 亿美元收购动视暴雪仍是游戏行业最大收购案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tmtpost.com/6830849.html">沙 特 主权 基 金 PIF 是 何来头？ -钛媒体官方网站</a></li>
<li><a href="https://zh.wikipedia.org/wiki/%E9%93%B6%E6%B9%96%E8%B5%84%E6%9C%AC">银湖资本 - 维基百科，自由的百科全书</a></li>
<li><a href="https://en.wikipedia.org/wiki/Affinity_Partners">Affinity Partners - Wikipedia</a></li>

</ul>
</details>

**标签**: `#EA`, `#收购`, `#游戏行业`, `#沙特PIF`, `#重大新闻`

---

<a id="item-4"></a>
## [微软确认今年推出 Copilot「超级应用」](https://www.theverge.com/tech/972927/microsoft-copilot-super-app-confirmed) ⭐️ 9.0/10

这一公告标志着微软将分散的 AI 产品整合为单一入口的战略举措，加剧了与 OpenAI 的 ChatGPT Work 及其他 AI 助手的竞争。依赖 Copilot 进行生产力工作和编程任务的开发者、企业客户及普通用户都将受到影响。 纳德拉描述了 Copilot 从聊天工具向 Cowork 和 Autopilots 的演进，并预计超级应用将在本季度推出。微软上季度营收达到 900 亿美元，主要由 AI 和云业务增长驱动。

telegram · zaihuapd · 8月1日 13:18

**背景**: Copilot 是微软嵌入 Windows、Microsoft 365 和 GitHub 的 AI 助手，而 Copilot Cowork 是一种智能体（agentic）功能，可自动执行发送电子邮件、安排会议、创建文档等任务。Agentic AI 指能够追求目标并以不同程度自主性采取行动的系统，通常运行在人类设定的目标和约束内。这一举措与 OpenAI 近期整合 ChatGPT 和 Codex 推出 ChatGPT Work 的动向相呼应，反映了行业向统一 AI 工作空间发展的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/microsoft-365-copilot/cowork">Copilot Cowork: Automate Tasks and Workflows | Microsoft</a></li>
<li><a href="https://learn.microsoft.com/en-us/microsoft-365/copilot/cowork/">Copilot Cowork overview | Microsoft Learn</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-365/blog/2026/03/09/copilot-cowork-a-new-way-of-getting-work-done/">Copilot Cowork: A new way of getting work done | Microsoft 365 Blog</a></li>

</ul>
</details>

**标签**: `#AI`, `#Copilot`, `#Microsoft`, `#Product announcement`, `#Cloud`

---

<a id="item-5"></a>
## [NetBSD 11.0 发布，带来 MicroVM 内核和更新的 NPF 防火墙](https://blog.netbsd.org/tnf/entry/netbsd_11_0_released) ⭐️ 8.0/10

NetBSD 11.0 正式发布，引入了面向 x86 的全新 MICROVM 内核，可在约 10 毫秒内完成启动，并大幅改进了 NPF 防火墙过滤功能。该版本还包含大量硬件改进和其他增强。 这一主版本发布为广泛使用的 BSD 操作系统 NetBSD 带来了有意义的性能和安全性进步。启动速度极快的 MICROVM 内核可能为微服务和虚拟化环境带来新的应用场景，而 NPF 的更新则增强了简单和复杂部署场景下的防火墙能力。 MICROVM 内核利用 PVH 引导、VirtIO MMIO 以及多项内核优化来实现快速启动，支持 i386 和 amd64 两种架构。NPF 防火墙的改进包括二层过滤和用户/组过滤，在传统的三层/四层规则之外提供了更灵活的策略选项。

hackernews · jaypatelani · 8月1日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49136736)

**背景**: NetBSD 是一款免费开源的类 Unix 操作系统，以可移植性、简洁设计和对多种硬件平台的支持而闻名。NPF 是 NetBSD 的有状态数据包过滤防火墙，类似于 Linux 的 iptables 或 OpenBSD 的 PF。新的 MICROVM 内核是专为虚拟机环境调优的特殊内核配置，旨在最小化面向服务工作负载的启动延迟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.netbsd.org/releases/formal-11/NetBSD-11.0.html">Announcing NetBSD 11.0 RC7 (July 21, 2026)</a></li>
<li><a href="https://man.netbsd.org/npf.7">npf (7) - NetBSD Manual Pages</a></li>
<li><a href="https://wiki.netbsd.org/users/imil/microvm/">microvm</a></li>

</ul>
</details>

**社区讨论**: 评论者讨论了 BSD 与 Linux 相比的整体现状，有人称赞 NPF 的二层和用户/组过滤功能很有价值，MICROVM 的 10 毫秒启动时间则开辟了新可能。还有人询问实际兼容性问题，例如在 NetBSD 上通过 Wine 运行 SDR 软件，也有评论者指出该版本对已知问题的表述几乎像是在道歉。

**标签**: `#NetBSD`, `#BSD`, `#Operating Systems`, `#Release`

---

<a id="item-6"></a>
## [研究探究 KataGo 神经网络内部如何学习对称性](https://www.reddit.com/r/MachineLearning/comments/1vcrki2/how_symmetric_are_the_insides_of_a_go_network_r/) ⭐️ 8.0/10

开源围棋程序 KataGo 的作者 David Wu 发布了一项研究，分析了超人类水平的围棋神经网络如何仅通过数据增强来处理棋盘的 8 重旋转和反射对称性。研究表明，网络既学习了与方向无关的内部概念，也在一定程度上按方向记忆了特征，其中有一项发现出人意料。 这项研究意义重大，因为它揭示了神经网络是会自然利用已知的对称性，还是会通过记忆来弥补，这对游戏 AI 及其他对称领域的数据增强策略和架构设计有参考价值。同时，它也来自开源围棋 AI 的顶尖开发者，为可解释性研究做出了贡献。 模型并没有在架构上强制对称性，而是依赖随机的 8 重数据增强，对每个训练批次随机进行旋转或翻转。这篇研究报告主要由 AI 撰写，但经过了人类细致的指导和反馈，代码链接也附在对应的研究页面上。

reddit · r/MachineLearning · /u/icosaplex · 8月1日 16:18

**背景**: 围棋是一种具有完全旋转和反射对称性的棋盘游戏，任何一个局面都可以变换成 8 种等价朝向。KataGo 是 David Wu 开发的开源计算机围棋程序，使用深度学习与自对弈强化学习，达到了超人类水平。数据增强是一种通过生成修改过的训练样本以提升泛化能力的技术；这里使用的随机 8 重增强会在训练中让网络看到所有朝向，但并不显式约束网络的内部表征。这项研究探讨由此训练出的网络是构建了方向无关的概念，还是对每个方向分别记忆。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/KataGo">KataGo</a></li>
<li><a href="https://arxiv.org/html/2405.09591v3">A Comprehensive Survey on Data Augmentation - arXiv.org</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#interpretability`, `#neural networks`, `#Go`, `#symmetry`

---
---
layout: default
title: "Horizon Summary: 2026-07-31 (ZH)"
date: 2026-07-31
lang: zh
---

> 从 37 条内容中筛选出 8 条重要资讯。

---

1. [DeepSeek V4 Flash 0731：前沿级智能，输出每百万 Token 仅 0.28 美元](#item-1) ⭐️ 9.0/10
2. [无状态 MCP 2.0 重燃 Simon Willison 兴趣，激发新工具](#item-2) ⭐️ 9.0/10
3. [华为开源 505B 参数 MoE 大模型 openPangu-2.0-Pro](#item-3) ⭐️ 9.0/10
4. [电梯调度算法深入解析：仿真、对比与社区讨论](#item-4) ⭐️ 8.0/10
5. [YC 支持的 QM 推出多人智能体协作框架](#item-5) ⭐️ 8.0/10
6. [OpenAI 将 GPT-5.6 Luna 价格下调 80%，Terra 下调 20%](#item-6) ⭐️ 8.0/10
7. [MiniMax 多模态视频模型 H3 将于 8 月 3 日开源](#item-7) ⭐️ 8.0/10
8. [德国法院裁定 AI 音乐公司 Suno 侵犯版权](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Flash 0731：前沿级智能，输出每百万 Token 仅 0.28 美元](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 9.0/10

DeepSeek 正式发布了 V4 Flash 0731 API，这是 V4-Flash 模型的升级版，智能体能力大幅增强。它在 Artificial Analysis 智能指数上达到前沿水平，而输出价格仅为每百万 Token 0.28 美元。 这一发布将前沿级模型质量带到了异常低的价位，加剧了各大 AI 实验室在性价比上的竞争。它让开发者使用智能体编程和大量调用 LLM 的成本大幅降低，也让人们对即将推出的 V4 Pro 更新充满期待。 DeepSeek V4 Flash 0731 是一款稀疏混合专家模型，总参数 284B、激活参数 13B，支持 100 万 Token 上下文窗口。与预览版相比，它仅重新进行了后训练；原生支持 Responses API 并针对 Codex 适配，Terminal Bench 2.1 得分达 82.7。

hackernews · theanonymousone · 7月31日 07:59 · [社区讨论](https://news.ycombinator.com/item?id=49120299)

**背景**: LLM API 通常对输入和输出 Token 分别计费，输出 Token 更贵，因为需要自回归生成，计算成本很高。DeepSeek 是一家以低价发布高性能开源权重模型而知名的中国 AI 实验室；V4 Flash 是稀疏混合专家模型，意味着每个 Token 只激活部分参数。“前沿级”表示该模型在综合智能基准上跻身现有最强模型之列。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek-ai/DeepSeek-V4-Flash-0731 · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash-0731">DeepSeek V4 Flash 0731 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://www.silicondata.com/blog/llm-cost-per-token">Understanding LLM Cost Per Token: A 2026 Practical Guide - Silicon Data — GPU Performance Data for Companies</a></li>

</ul>
</details>

**社区讨论**: 社区整体评价积极，用户称赞该模型的性价比，称其可作为日常主力模型，“没有 Token 焦虑”。一些评论者质疑基准测试使用了 DeepSeek Harness 的最小模式，并猜测是否会发布优化版智能体编程框架；还有人推测 V4 Pro 何时推出，并讨论在 Hugging Face 上托管模型的经济性。

**标签**: `#AI`, `#LLM`, `#DeepSeek`, `#benchmarking`, `#price-performance`

---

<a id="item-2"></a>
## [无状态 MCP 2.0 重燃 Simon Willison 兴趣，激发新工具](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 9.0/10

Simon Willison 表示，2026-07-28 无状态 MCP 规范（MCP 2.0）重新点燃了他对模型上下文协议的兴趣。他本周构建了三个实现，包括 mcp-explorer 命令行工具和 datasette-mcp。 这是 MCP 发布以来最重要的变化：无状态核心无需再维护服务端会话，大幅降低了客户端和服务端的实现复杂度。这使得 MCP 更适合可扩展的 Web 应用，也更容易让较小、可在本地运行的模型驱动，从而可能加速 AI 代理采用可审计、可控的工具调用。 该规范将旧的两次请求流程——先初始化获取 Mcp-Session-Id，再调用工具——替换为使用 MCP-Protocol-Version 和 Mcp-Method 头部的单次 HTTP 请求。Willison 还反驳了“shell 加 curl”的代理方案，认为 MCP 工具更易于审计和控制，而终端环境“充满风险”。

rss · Simon Willison · 7月31日 23:13

**背景**: 模型上下文协议（MCP）是 Anthropic 于 2024 年 11 月推出的开放标准，旨在标准化大语言模型代理连接外部工具和数据源的方式。2025 年大部分时间里它获得了巨大关注，但在 Anthropic 推出 Claude Skills 后一度被部分遮蔽，因为当时看来，拥有终端和 curl 的代理就能以更灵活的方式完成许多任务——而 Willison 现在认为这种做法风险很大。2026-07-28 规范（此前于 5 月发布候选版）在协议层将 MCP 变为无状态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.modelcontextprotocol.io/posts/2026-07-28/">The 2026 - 07 - 28 Specification | Model Context Protocol Blog</a></li>
<li><a href="https://claude.com/blog/bringing-mcp-2026-07-28-to-claude">MCP 2026 - 07 - 28 spec : stateless core, coming... | Claude by Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**标签**: `#MCP`, `#AI`, `#LLM`, `#agents`, `#protocol`

---

<a id="item-3"></a>
## [华为开源 505B 参数 MoE 大模型 openPangu-2.0-Pro](https://huggingface.co/openpangu/openPangu-2.0-Pro) ⭐️ 9.0/10

华为在 Hugging Face 上发布了 openPangu-2.0-Pro，这是一个总参数约 505B 的混合专家（MoE）模型，每个 token 激活约 18B 参数，并支持 512k 的上下文长度。该开源版本包含 Thinking 版本，在 AIME 2026 数学测评中得分 95.4，在 GPQA-Diamond 上得分为 87.9。 这是主流厂商发布的最大开源 MoE 模型之一，进一步缩小了开源模型与闭源大模型之间的差距。其出色的推理性能和高效架构，可能会影响其他实验室设计可扩展、长上下文的模型。 该模型基于昇腾 NPU 训练，训练数据约 34T tokens；架构上融合了多头潜在注意力（MLA）、DSA+SWA 独立分层混合设计，以及 3 头多 token 预测（MTP）自投机解码模块。后训练阶段完成了快慢合一微调和多专项强化学习。

telegram · zaihuapd · 7月31日 06:50

**背景**: MoE（混合专家）模型包含多个专门的子网络（专家），但每个 token 只激活其中一部分，从而在计算开销可控的情况下实现很大的参数量。MLA（多头潜在注意力）通过低秩潜在压缩，在推理时降低 KV 缓存的内存瓶颈；而 SWA（滑动窗口注意力）等混合注意力层则有助于高效处理长上下文。MTP（多 token 预测）让模型同时预测多个未来 token，从而加速推理。该模型还值得关注的一点是，它是在华为昇腾 NPU 生态上训练的，而非主流 GPU。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://machinelearningmastery.com/a-gentle-introduction-to-multi-head-latent-attention-mla/">A Gentle Introduction to Multi-Head Latent Attention (MLA) - MachineLearningMastery.com</a></li>
<li><a href="https://jianyuh.github.io/llm/2026/04/26/DeepSeek-V4-Arch-Train.html">DeepSeek-V4 Architecture &amp; Training: Hybrid Attention, Muon ...</a></li>
<li><a href="https://arxiv.org/pdf/2404.19737">Better &amp; Faster Large Language Models via Multi-token Prediction</a></li>

</ul>
</details>

**标签**: `#open-source`, `#LLM`, `#MoE`, `#Huawei`, `#AI`

---

<a id="item-4"></a>
## [电梯调度算法深入解析：仿真、对比与社区讨论](https://john.fun/elevators) ⭐️ 8.0/10

这篇文章对电梯调度算法进行了技术性深入剖析，通过仿真模拟比较了 SCAN、LOOK 和目的地派送等不同方案。文章在 Hacker News 上引发了热烈讨论，获得了 807 分和 208 条评论。 电梯调度直接影响高层建筑中人们的日常通勤，而其算法权衡也对应着操作系统和物流领域中的普遍问题。讨论将电梯工程与磁盘调度联系起来，对任何需要用单一移动头服务有序请求的系统都具有借鉴意义。 作者发现，在随机目的地假设下，目的地派送的表现可能更差，而类似 LOOK 的算法表现良好；评论者指出，真实场景中的出行规律（如大量人群同时前往一楼、结伴午餐）会改变对比结果。文章将电梯算法与 SCAN 磁盘调度算法家族联系起来，并提到 Elevator Saga 这款模拟游戏。

hackernews · Jrh0203 · 7月31日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=49124218)

**背景**: 电梯算法又称 SCAN，是一种经典的磁盘调度方法：读写磁头沿一个方向移动，沿途处理请求，到达端点后再反向。在电梯中，这一思想让轿厢保持向上或向下运行，同时接上目的地在前方的乘客。目的地派送是一种更现代的方式，通过键盘输入目标楼层来按目的地分组乘客，而不是使用楼层按钮。理解这些算法有助于优化电梯和硬盘的延迟、吞吐量及能耗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Elevator_algorithm">Elevator algorithm - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/operating-systems/difference-between-scan-and-cscan-disk-scheduling-algorithms/">Difference Between SCAN and CSCAN Disk Scheduling Algorithms</a></li>
<li><a href="https://www.geeksforgeeks.org/operating-systems/c-scan-disk-scheduling-algorithm/">C-SCAN Disk Scheduling Algorithm - GeeksforGeeks</a></li>

</ul>
</details>

**社区讨论**: 评论者提出了多个有价值的观点：有人将电梯算法与硬盘磁盘调度联系起来，指出 SCAN 本身就是一个磁盘调度算法；还有人认为在真实建筑中，由于客流高度集中在往返一楼和结伴午餐，目的地派送可能比随机目的地仿真表现更好。其他人分享了当年的编程项目，推荐了 Elevator Saga 游戏；一位游戏开发者表示他采用了类似 LOOK 的算法以符合玩家预期。还有用户抱怨电梯缺少“再按一次取消”的功能，误按后无法取消。

**标签**: `#algorithms`, `#scheduling`, `#elevators`, `#simulation`, `#systems`

---

<a id="item-5"></a>
## [YC 支持的 QM 推出多人智能体协作框架](https://github.com/yc-software/qm) ⭐️ 8.0/10

QM 是一个由 YC 支持的多人智能体协作框架，利用每人独立的作用域和共享房间，在 Slack 和 Web 上协调多个 AI 智能体协作。它通过为每位员工提供隔离工作空间，同时支持共享协调，将个人 AI 助手与全公司自动化连接起来。 “每人作用域 + 共享房间”的设计直接回应了多人智能体中最棘手的权限边界与协调问题，为公司级助手提供了合理方案。它验证了面向协作工作的智能体框架这一新兴品类，也表明 YC 对团队级 AI 基础设施的兴趣在增加。 QM 横跨 Slack 与 Web 界面，为每位员工提供供个人智能体使用的隔离工作空间，同时通过共享房间实现跨智能体协调。该项目与 Orca、AQ 等同样探索多人智能体编码与工作场景的同类工具处于同一赛道。

hackernews · tosh · 7月31日 18:04 · [社区讨论](https://news.ycombinator.com/item?id=49126604)

**背景**: 智能体框架（agent harness）是一种编排层，为 AI 智能体提供工具、权限和结构化环境以可靠完成任务。多人智能体系统将其扩展到多个智能体与人类共同协作，但面临权限范围（决定每个智能体可访问的数据与工具）和协调等难题。QM 采用的“每人作用域 + 共享房间”是该领域正在兴起的一种常见设计模式，Claude Cowork 和 agent chat rooms 等工具也采用类似思路。Y Combinator 的背书表明这一品类正获得越来越多的关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aitoolly.com/ai-news/article/2026-08-01-qm-a-new-multiplayer-ai-agent-harness-for-collaborative-startup-workflows-in-slack-and-web">QM: Multiplayer AI Agent Harness for Startups and Slack</a></li>
<li><a href="https://learn.microsoft.com/en-us/agent-framework/agents/harness">Agent Harnesses | Microsoft Learn</a></li>
<li><a href="https://www.arthur.ai/column/access-management-ai-agents-scope-permissions">Access Management for AI Agents: Scope What They Touch | Arthur</a></li>

</ul>
</details>

**社区讨论**: 评论者整体热情，来自相邻领域的开发者称这一方向“令人振奋又有种不真实感”，并称赞“每人作用域”是公司级助手的明智方案。有人开玩笑说智能体已开始自主安排会议，也有人质疑 QM 与 Claude Cowork 等现有产品的差异化，希望看到直接对比。

**标签**: `#AI agents`, `#multiplayer`, `#LLM`, `#collaboration`, `#Y Combinator`

---

<a id="item-6"></a>
## [OpenAI 将 GPT-5.6 Luna 价格下调 80%，Terra 下调 20%](https://simonwillison.net/2026/Jul/30/luna-price-drop/#atom-everything) ⭐️ 8.0/10

2026 年 7 月 30 日，OpenAI 宣布将 GPT-5.6 Terra 价格下调 20%，GPT-5.6 Luna 价格大幅下调 80%。OpenAI 将此次降价归功于 GPT-5.6 Sol，它优化了负载均衡和推理过程，使服务成本降低了 20%。 Luna 的新定价——每百万输入令牌 0.20 美元、每百万输出令牌 1.20 美元——使其比 Google 的 Gemini 3.1 Flash-Lite 更便宜，大约是 Anthropic Claude Haiku 4.5 输入价格的五分之一。这改变了低成本 LLM 部署的竞争格局，并表明 AI 模型可用于优化自身的服务基础设施。 Sol 通过寻找可以预计算、避免或并行化的工作来优化前向传播，并使用 Codex 在 Triton 和 Gluon 中自主重写了生产内核。这些优化使端到端服务成本降低了 20%，从而实现了降价；请注意，文章中 Gemini Flash-Lite 的输入价格写作$0.25/百万令牌。

rss · Simon Willison · 7月30日 23:58

**背景**: GPT-5.6 是 OpenAI 于 2026 年 7 月 9 日发布的模型系列，包含三个档位：Luna（最快最便宜）、Terra（均衡）和 Sol（旗舰）。此次降价的背后是使用 Sol 本身来提高推理效率，包括在 Triton 和 Gluon（OpenAI 维护的两个开源 GPU 编程语言）中重写内核。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://openai.com/index/gpt-5-6/">GPT‑5.6: Frontier intelligence that scales with ... - OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5.6`, `#AI pricing`, `#inference optimization`, `#machine learning`

---

<a id="item-7"></a>
## [MiniMax 多模态视频模型 H3 将于 8 月 3 日开源](https://modelscope.cn/models/MiniMax/MiniMax-H3) ⭐️ 8.0/10

MiniMax 宣布，其新一代通用多模态视频模型 H3 将于 2026 年 8 月 3 日在魔搭社区（ModelScope）开源发布。该模型原生支持文本、图像、音频与视频的理解和生成，最高可生成 15 秒 2K 分辨率、带原生双声道音频的内容。 此次开源是开源多模态 AI 的重要一步，H3 在一个模型中统一实现了四种模态的理解与生成。该模型有望影响影视、广告、电商、游戏等创意与商业应用领域，让开发者更容易获得先进的视频生成能力。 H3 具备多维度精准编辑控制能力，支持原生双声道音视频输出，最高可生成 15 秒 2K 分辨率内容。它采用 Contextual Omni Representation 与 Omni Reference 等技术，可自然融合多种参考素材进行连贯创作。

telegram · zaihuapd · 7月31日 12:37

**背景**: MiniMax H3 是一款通用的全模态生成模型，于 2026 年 7 月 31 日正式发布。多模态视频模型能够整合文本、图像、音频和视频的理解与生成；在魔搭社区（ModelScope）这一阿里巴巴开源模型平台上开源此类模型，可帮助开发者和研究者将其部署并定制到实际应用中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ithome.com/0/984/379.htm">MiniMax H3 通用多模态视频模型将于 8 月 3 日开源，最高可支持 15s 2...</a></li>
<li><a href="https://baike.baidu.com/item/MiniMax+H3/68391253">MiniMax H3 - 百度百科</a></li>
<li><a href="https://apidot.ai/zh/blog/minimax-h3-review">MiniMax H3 全面评测：功能、画质、价格与早期实测 | APIDot</a></li>

</ul>
</details>

**标签**: `#multimodal`, `#video model`, `#open source`, `#AI`, `#MiniMax`

---

<a id="item-8"></a>
## [德国法院裁定 AI 音乐公司 Suno 侵犯版权](https://www.dw.com/en/german-court-rules-that-ai-music-firm-suno-violated-copyrights/a-78152227) ⭐️ 8.0/10

慕尼黑地区法院上周五裁定，美国 AI 音乐公司 Suno 侵犯版权，须披露非法所得并支付赔偿，具体金额尚待确定。Suno 表示不认同判决，将评估包括上诉在内的所有选项。 这是全球首批检验版权法如何适用于 AI 音乐训练的重大司法裁决之一，可能为整个 AI 行业的训练数据授权实践树立先例。它可能促使 AI 音乐公司为训练数据获取正规许可，从而影响 AI 开发者和更广泛的音乐生态。 该诉讼由德国音乐版权集体管理组织 GEMA 于 2025 年 1 月提起，指控 Suno 未经许可和补偿，用受版权保护的音乐训练 AI 模型。庭审中，GEMA 演示了 Suno 生成的歌曲与原作品高度相似，但确切的赔偿金额尚未确定。

telegram · zaihuapd · 7月31日 13:11

**背景**: GEMA 代表德国超过 9.5 万名音乐人及全球超 200 万名权利持有人的音乐权益。Suno 是一款 AI 音乐生成器，用户通过文本提示即可创建歌曲。这些案件背后的核心法律问题是，使用受版权保护的作品训练 AI 模型是否构成侵权，或是否能被认定为合理使用，这是全球法院和立法机构正在激烈争论的议题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GEMA_%28German_organization%29">GEMA ( German organization) - Wikipedia</a></li>
<li><a href="https://suno.com/">Suno | AI Music Generator</a></li>
<li><a href="https://astraea.law/insights/ai-training-data-copyright">AI Training Data Copyright: Fair Use, Licensing, and ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#copyright`, `#music`, `#legal`, `#Suno`

---
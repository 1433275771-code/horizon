---
layout: default
title: "Horizon Summary: 2026-08-16 (ZH)"
date: 2026-08-16
lang: zh
---

> 从 32 条内容中筛选出 8 条重要资讯。

---

1. [Anthropic 公布官方 Claude 系统提示词](#item-1) ⭐️ 8.0/10
2. [AI 模型正故意变笨以变得更聪明](#item-2) ⭐️ 8.0/10
3. [Cloudflare 在用户切换名称服务器时静默注入 Web Analytics 分析脚本](#item-3) ⭐️ 8.0/10
4. [Qwen 3.8 27B：令人惊艳的视觉大模型，但默认过度思考](#item-4) ⭐️ 8.0/10
5. [分析称 PJM 建模错误浪费 120 亿美元用户电费，且可能重蹈覆辙](#item-5) ⭐️ 8.0/10
6. [SSOG-Attention：基于可分离高斯和的次二次注意力机制](#item-6) ⭐️ 8.0/10
7. [重新审视 ECA：跨通道交互可能并非关键](#item-7) ⭐️ 8.0/10
8. [Anthropic 第二季营收暴涨 14 倍至逾 115 亿美元](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 公布官方 Claude 系统提示词](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic 已在官方文档中发布 Claude 模型在 claude.ai 和移动应用上使用的系统提示词，公开了塑造模型行为的隐藏指令。此次发布让人们前所未有地看到主流商用大语言模型的默认配置。 这一举措意义重大，因为它让开发者、研究人员和公众得以罕见地一窥领先 AI 模型通常隐藏的系统级指令，从而更深入地分析其行为和安全措施。它还为追踪模型行为随时间的演变提供了基准，这对 AI 部署中的信任与问责至关重要。 系统提示词记录在 Claude 平台发布说明中，包含当前日期、格式偏好和行为准则等实用元素。社区成员如 Simon Willison 已构建基于 git 的追踪工具，以比较不同模型版本之间的变化，例如从 Opus 4.8 到 Opus 5 的转变。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词是在对话开始前提供给大语言模型的初始指令，用于设定上下文、语气和后续所有回复的行为约束。这类提示词通常具有专有性，对最终用户隐藏，因此 Anthropic 公开发布是一项值得关注的透明化举措。已发布的提示词展示了 Anthropic 如何引导 Claude 处理各种边缘情况，例如核实对话中是否真的有图片，以及在用户处于危机状态时优先考虑其福祉。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/release-notes/system-prompts">System Prompts - Claude Platform Docs</a></li>
<li><a href="https://tactiq.io/learn/claude-system-prompt">Claude System Prompt Explained: What&#x27;s Inside and Why It Matters</a></li>
<li><a href="https://github.com/Piebald-AI/claude-code-system-prompts">GitHub - Piebald-AI/claude-code-system-prompts: All parts of Claude Code&#x27;s system prompt, 27 builtin tool descriptions, sub agent prompts (Plan/Explore/Task), utility prompts (CLAUDE.md, compact, statusline, magic docs, WebFetch, Bash cmd, security review, agent creation). Updated for each Claude Code version. · GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区评论中既有赞赏也有担忧。Simon Willison 分享了一个追踪系统提示词变化的 git 仓库，并特别提到了 Fable 5 和 Mythos 5 等有趣的添加内容。另有用户担心论坛正在删除对 AI 持批评态度的文章；还有人评论说，即使是像 Opus 4.8 这样的强大模型也需要系统提示词来执行基本常识，这引发了对模型究竟有多“智能”的疑问。

**标签**: `#AI`, `#Claude`, `#LLM`, `#System Prompts`, `#Transparency`

---

<a id="item-2"></a>
## [AI 模型正故意变笨以变得更聪明](https://w4g1.dev/blog/models-are-getting-dumber-on-purpose) ⭐️ 8.0/10

w4g1 的新博文认为，AI 模型正故意‘变笨’，将事实回忆外包给外部工具与检索系统，而不是把事实存进权重。文章引用 SimpleQA 等基准测试，指出即使 Gemini 2.5 Pro 这类顶级模型也会答错约一半事实性问题，并预测模型卡最终可能不再列出知识截止日期。 这标志着大语言模型架构的重大转向：从把越来越多事实塞进参数，转向工具增强推理与可插拔知识。若该方向实现，可减少幻觉、消除知识截止造成的过时问题，并让用户按需插拔领域知识模块，从而改变模型的训练、部署与模型卡说明方式。 文章引用 SimpleQA（一个禁止使用工具的事实回忆基准）说明‘金钱能买到的最好记忆’仍会答错一半问题，并设想未来模型卡不再列出知识截止日期，因为权重中的事实要数年才会过时。评论区补充说，Cactus 已发布一款仅 14 MB、主打工具调用的 LLM‘Needle’，而微软的 KBLaM 则将外部知识编码为键值向量，实现即插即用集成。

hackernews · hruvhwe · 8月16日 19:04 · [社区讨论](https://news.ycombinator.com/item?id=49322695)

**背景**: 大多数大语言模型在预训练阶段把知识隐式存储在参数中，因此存在固定的知识截止日期，并容易产生幻觉。检索增强生成（RAG）通过在推理时连接外部数据库，让模型获取最新事实，而不是凭记忆回忆。微软的 KBLaM 等‘可插拔知识库’方案则尝试把外部知识直接编码进注意力层，让领域知识可互换而无需重训。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Retrieval-augmented_generation">Retrieval-augmented generation - Wikipedia</a></li>
<li><a href="https://www.microsoft.com/en-us/research/blog/introducing-kblam-bringing-plug-and-play-external-knowledge-to-llms/">Introducing KBLaM: Bringing plug-and-play external knowledge to LLMs - Microsoft Research</a></li>
<li><a href="https://arxiv.org/abs/1909.01066">[1909.01066] Language Models as Knowledge Bases?</a></li>

</ul>
</details>

**社区讨论**: 评论区参与度高但观点不一。有人（如 kennywinker）认同可插拔知识库的构想，认为用户可自由组合不同领域模块；也有人（如 COAGULOPATH）批评文章疑似 AI 生成且数据过时，指出 SimpleQA 许久未更新、Gemini 2.5 Pro 已是 16 个月前的模型。pulkitsh1234 则提出更根本的质疑：当需要推理不可预测的人类行为时，推理与事实知识真的能分开吗？

**标签**: `#AI`, `#ML models`, `#tool use`, `#retrieval`, `#LLM trends`

---

<a id="item-3"></a>
## [Cloudflare 在用户切换名称服务器时静默注入 Web Analytics 分析脚本](https://news.ycombinator.com/item?id=49322107) ⭐️ 8.0/10

一位 Hacker News 用户报告称，在将名称服务器切换到 Cloudflare 以通过自定义子域名提供 R2 存储桶服务后，Cloudflare 静默地向其纯 HTML、无 JavaScript 的网站注入了 Web Analytics JavaScript 片段。用户必须去 Analytics 仪表盘手动禁用该片段，而不是主动选择开启。 Cloudflare 官方文档确认，对于经过代理的流量，Web Analytics 的自动设置默认处于开启状态，这意味着许多网站所有者可能在不知情的情况下将访问者数据发送给 Cloudflare。这引发了透明度和隐私方面的担忧，并影响到所有将 Cloudflare 用作代理的用户，尤其是那些被 R2 免出口流量费用吸引的新用户。 这种注入仅在流量经由 Cloudflare 代理（即橙色云朵开启）时发生；仅使用 DNS 的域名需要手动设置。被注入的脚本是来自 static.cloudflareinsights.com/beacon.min.js 的模块，带有完整性哈希和 data-cf-beacon 令牌，可以通过类似 script-src &\#x27;self&\#x27; 的内容安全策略（CSP）阻止，或在 Web Analytics 仪表盘中关闭。

hackernews · stagas · 8月16日 17:49

**背景**: Cloudflare 是一家内容分发网络和 DNS 提供商；当域名被代理时，Cloudflare 可以在其边缘节点处理 HTML 响应时对其进行修改。R2 是 Cloudflare 的对象存储服务，要通过自定义子域名提供 R2 存储桶的内容，通常需要该域名经过 Cloudflare 代理。Cloudflare Web Analytics 是一款免费分析产品，其自动设置通过向被代理的 HTML 页面注入一个 JavaScript“信标（beacon）”来实现。由于该注入默认开启，因此为 R2 或其他 Cloudflare 功能而切换名称服务器的用户可能并不会意识到脚本已被添加。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.cloudflare.com/web-analytics/faq/">FAQs · Cloudflare Web Analytics docs</a></li>
<li><a href="https://developers.cloudflare.com/web-analytics/get-started/">Enabling Cloudflare Web Analytics · Cloudflare Web Analytics docs</a></li>
<li><a href="https://developers.cloudflare.com/r2/">Overview · Cloudflare R 2 docs</a></li>

</ul>
</details>

**社区讨论**: 评论者建议使用 Content-Security-Policy 元标签来阻止外部注入的脚本，还有一位用户确认看到了带完整性属性的 beacon 脚本。其他人则询问该站点是使用了代理还是仅 DNS，并表示他们的 DNS-only 域名没有启用 Web Analytics。总体舆论对 Cloudflare 默认提供退出选项的做法持批评态度，不过 CSP 等解决方法也被认可。

**标签**: `#Cloudflare`, `#privacy`, `#web analytics`, `#nameservers`, `#security`

---

<a id="item-4"></a>
## [Qwen 3.8 27B：令人惊艳的视觉大模型，但默认过度思考](https://simonwillison.net/2026/Aug/16/qwen-38-27b/) ⭐️ 8.0/10

阿里巴巴 Qwen 实验室于周五发布了 Qwen 3.8 27B，这是一款采用 Apache 2.0 许可、拥有 270 亿参数的视觉大语言模型。该模型默认采用“xhigh”推理强度设置，导致生成一张鹈鹕骑自行车的 SVG 图像耗时 21 分钟、消耗 22,276 个推理令牌。 Qwen 3.8 27B 的 270 亿参数规模使其适合在笔记本电脑上实际部署，而其自称的基准测试结果显示其性能优于 Qwen 3.6 27B 和闭源的 Qwen 3.7-Plus。然而，默认的过高推理强度会显著拖慢响应速度，这凸显了实际使用者需要权衡的可用性问题。 该模型在 LM Studio 中以 17GB 的 Q4\_K\_M 量化版本提供，作者在 128GB M5 Max MacBook Pro 和 NVIDIA DGX Spark 上进行了测试。LM Studio 默认的 8,192 令牌上下文限制很快被模型的过度思考耗尽，但将上下文提升到 262,144 令牌的最大值后问题得以解决。

rss · Simon Willison · 8月16日 22:00

**背景**: 大语言模型通常采用思维链推理，即模型在生成最终答案之前先生成内部推理步骤。Qwen 3.8 27B 支持“reasoning\_effort”参数，提供从 low 到 xhigh 的选项来平衡深度和成本，但其 xhigh 默认值原本是为复杂任务设计的，而非日常提示。过度思考——即模型生成过多且往往不必要的推理——是推理型大语言模型中的一个已知问题，近期的研究已对此展开探讨。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2502.03373">[2502.03373] Demystifying Long Chain - of - Thought Reasoning in LLMs</a></li>
<li><a href="https://spectrum.ieee.org/reasoning-in-ai">Is Your AI Stuck in Its Own Head? Today&#x27;s Large Language Models Have a Problem with Overthinking</a></li>
<li><a href="https://medium.com/@lssmj2014/you-think-too-much-so-do-llms-the-overthinking-trap-in-reasoning-models-d0268d8b00f6">You Think Too Much — So Do LLMs: The Overthinking Trap in Reasoning Models | by Baozilla, Let&#x27;s go! | Medium</a></li>

</ul>
</details>

**标签**: `#LLM`, `#Qwen`, `#open-weights`, `#AI`, `#benchmarks`

---

<a id="item-5"></a>
## [分析称 PJM 建模错误浪费 120 亿美元用户电费，且可能重蹈覆辙](https://newsletter.semianalysis.com/p/12b-of-us-ratepayers-money-wasted) ⭐️ 8.0/10

SemiAnalysis 的一项调查报道称，PJM 容量市场中的建模错误浪费了美国纳税人 120 亿美元，并警告 PJM 正计划重蹈覆辙。 此事意义重大，因为 PJM 运营着美国最大的批发电市场，服务 6700 万客户，其容量市场决策直接影响电费账单。如果所指控的建模错误重演，可能在数据中心需求激增和电厂退役的背景下加剧电网可靠性挑战。 文章标题和摘要表明，&\#x27;错误的模型&\#x27;指的是用于预测需求和设定容量补贴的电网建模工具，而非 AI 模型。PJM 预计 2026 年需求将年增长 5%（2005-2020 年为零增长），主要来自新建数据中心，同时许多发电厂因环境或经济原因关闭，造成供应紧张。

rss · Semianalysis · 8月16日 22:27

**背景**: PJM 互联是一家区域输电组织（RTO），协调 13 个州和华盛顿特区的批发电，曾是世界最大的竞争性批发电市场，直到欧洲综合能源市场发展起来。在容量市场中，PJM 向发电商采购未来年份的供电承诺，定价部分依赖于预测需求的计算机模型。模型缺陷可能导致过度采购容量或定价错误，最终由用户承担。电网建模工具对清洁能源转型至关重要，但许多现有工具仍使用可追溯至数十年前的旧代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PJM_Interconnection">PJM Interconnection</a></li>
<li><a href="https://en.wikipedia.org/wiki/Electricity_capacity_market">Electricity capacity market</a></li>
<li><a href="https://blog.ucs.org/mark-specht/grid-modeling-overview-four-types-of-models-guiding-the-transition-to-clean-electricity/">Grid Modeling Overview: Four Types of Models Guiding the Transition...</a></li>

</ul>
</details>

**标签**: `#energy grid`, `#modeling`, `#infrastructure`, `#policy`, `#analysis`

---

<a id="item-6"></a>
## [SSOG-Attention：基于可分离高斯和的次二次注意力机制](https://www.reddit.com/r/MachineLearning/comments/1vpt6ay/ssogattention_sum_of_separable_gaussians_as_a/) ⭐️ 8.0/10

一种新的注意力机制 SSOG-Attention 取代了标准缩放点积注意力（SDPA），它为每个头学习少量可分离高斯原子，并根据查询向量进行几何引导，将复杂度从 O\(N²·d\) 降低到 O\(N·√N·d\)。作者报告称，该方法在 CIFAR-100 上优于 SDPA，在 ImageNet-1k 上性能相当，且收敛更快、内存占用更低，并已开源代码。 这解决了 Transformer 中标准注意力二次方扩展这一根本瓶颈，该瓶颈限制了序列长度和上下文规模。如果实证结果可靠，它有望为长序列模型（尤其是视觉和多模态应用）带来更高效的训练与推理。 该方法将高斯原子分解为可分离和，通过在维度间分配计算实现 O\(N·√N·d\) 的降复杂度。实验显示，在小数据集（CIFAR-100）上有明显优势，在较大数据集（ImageNet-1k）上性能相当且收敛更快，同时随规模增大速度和内存效率更优。作者说明部分代码和博客内容使用了 AI 辅助，但为其所有结论负责。

reddit · r/MachineLearning · /u/4rtemi5 · 8月16日 10:06

**背景**: 缩放点积注意力（SDPA）需要计算所有查询与键令牌之间的两两相似度分数，因此复杂度为 O\(N²·d\)，在长序列上变得不可行。次二次注意力方法旨在近似或替代完整注意力以提升可扩展性，例如稀疏注意力和基于核的近似。可分离高斯和是一种经典技术，通过少量可分解（可分离）分量来近似高维函数或核，常用于卷积和散射等问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2606.28184">A fast sum - of - Gaussians algorithm for the high-dimensional fractional...</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-sub-quadratic-sparse-attention-subq-ssa">What Is Sub - Quadratic Sparse Attention ? | MindStudio</a></li>

</ul>
</details>

**标签**: `#attention`, `#transformer efficiency`, `#machine learning`, `#sub-quadratic`, `#gaussian`

---

<a id="item-7"></a>
## [重新审视 ECA：跨通道交互可能并非关键](https://www.reddit.com/r/MachineLearning/comments/1vptaw9/revisiting_the_efficient_channel_attention_paper/) ⭐️ 8.0/10

Reddit 上一篇文章对高效通道注意力\(ECA\)论文提出批评，认为其对通道均值做一维卷积在概念上存在问题。基于象棋残局库的实验显示，卷积核大小为 1 的 ECA 与大小为 3 的 ECA 表现几乎相当，这动摇了“跨通道交互带来性能提升”这一核心论断。 ECA 是被广泛引用（引用超 1.2 万次）的计算机视觉注意力机制，因此对其概念基础的质疑具有广泛影响。实验结果表明，相比 Squeeze-and-Excitation 带来的提升可能来自避免降维，而非通道交互，这可能会影响未来通道注意力设计的研究方向。 作者在 6 子国际象棋残局库上使用无偏随机采样测试了多种门控变体。结果显示：ECA（k=3）准确率为 96.68%，ECA（k=1）为 96.61%，而不含任何跨通道交互的 PerChannelGate 达到 96.65%。

reddit · r/MachineLearning · /u/arkuto · 8月16日 10:13

**背景**: 高效通道注意力\(ECA\)是 Wang 等人在 2019 年提出的一种通道注意力模块，旨在改进 Squeeze-and-Excitation\(SE\)模块。SE 在全局平均池化后使用全连接层建模通道间依赖，而 ECA 改为使用一维卷积来捕获局部跨通道交互，同时避免降维。Reddit 帖子利用国际象棋残局库——一个具有完整真实标签的已解游戏——来评估架构设计选择，并指出通道维度缺乏卷积所依赖的空间局部性和平移不变性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1910.03151">[1910.03151] ECA -Net: Efficient Channel Attention for Deep...</a></li>
<li><a href="https://www.emergentmind.com/topics/efficient-channel-attention-eca-mechanisms">Efficient Channel Attention Mechanisms</a></li>
<li><a href="https://blog.paperspace.com/attention-mechanisms-in-computer-vision-ecanet/">ECA -Net in PyTorch and TensorFlow | Paperspace Blog</a></li>

</ul>
</details>

**标签**: `#deep learning`, `#attention mechanisms`, `#computer vision`, `#research critique`, `#ECA`

---

<a id="item-8"></a>
## [Anthropic 第二季营收暴涨 14 倍至逾 115 亿美元](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

Anthropic 第二季初步营收超过 115 亿美元，同比增长逾 14 倍，当季调整后营业利润转正。公司正筹备可能于今年秋季启动的大型 IPO。 这标志着领先 AI 实验室的重大商业里程碑，表明 AI 大规模变现正在快速实现。若成功上市，公众投资者将获得对最大 AI 初创公司之一的直接敞口，并进一步加剧与 OpenAI 的竞争。 这些数据为初步数据，仍可能调整：第二季营收对比去年同期为 7.87 亿美元，2026 年第一季为 47.3 亿美元。据报道，若今年秋季启动，这将是规模最大的 AI 公司 IPO 之一。

telegram · zaihuapd · 8月16日 07:26

**背景**: Anthropic 是大语言模型 Claude 系列的开发商，也是获得大型投资机构支持的领先 AI 初创公司。快速的营收增长反映了企业对 AI 助手和编程工具的强劲需求。IPO 将标志着这家已通过私募融资数十亿美元的公司迎来关键转变，也将检验公开市场对纯 AI 公司的兴趣。

**标签**: `#Anthropic`, `#AI`, `#Revenue`, `#IPO`, `#Business`

---
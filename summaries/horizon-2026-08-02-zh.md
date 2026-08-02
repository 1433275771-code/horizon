# Horizon 每日速递 - 2026-08-02

> 从 29 条内容中筛选出 4 条重要资讯。

---

1. [eBay 骚扰事件致 5600 万美元赔偿及监禁](#item-1) ⭐️ 8.0/10
2. [微软牵头公开信捍卫开放权重 AI 模型](#item-2) ⭐️ 8.0/10
3. [LLM 上下文退化：研究总结与实用缓解习惯](#item-3) ⭐️ 8.0/10
4. [AI 芯片每 9 个月翻番，2028 年底全球将达 2 亿颗](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [eBay 骚扰事件致 5600 万美元赔偿及监禁](https://www.ft.com/content/06ec1b03-d4af-40cf-b12a-4ba5a410f6d2) ⭐️ 8.0/10

eBay 针对批评者 David 和 Ina Steiner 的骚扰运动已导致 5600 万美元赔偿，以及前安全主管的监禁判决。前高级总监 Jim Baugh 获刑 57 个月，前高级经理 Brian Gilbert 被判处已服刑期并罚款 2 万美元。 此案凸显了企业安全团队可能被用作对付普通个人的武器，引发对问责和权力滥用的严重担忧。这也向科技公司发出信号：此类行为将带来严重的法律和财务后果。 包括前警监在内的七名 eBay 安全团队成员参与了此次骚扰行动。判决各不相同：Jim Baugh 获刑 57 个月，Brian Gilbert 被判处已服刑期、一年监督释放及 2 万美元罚款，其他高管也被判监禁。

hackernews · JumpCrisscross · 8月2日 19:19 · [社区讨论](https://news.ycombinator.com/item?id=49147435)

**背景**: David 和 Ina Steiner 经营着一份批评 eBay 的通讯刊物，引起了公司的不满。作为回应，eBay 安全团队策划了一场骚扰和恐吓这对夫妇的行动，包括发送威胁信息和监视。该案件由联邦检察官揭露，最终导致定罪和 5600 万美元的里程碑式和解。

**社区讨论**: 评论者对这一骚扰行为仅限于一对夫妇表示怀疑，质疑 eBay 是否对其它批评者也采取了类似行动。有人分享了报道此案的播客系列，还有人详细列出了判决结果，并呼吁对涉案的前警监进行更广泛的调查。

**标签**: `#cybersecurity`, `#corporate ethics`, `#legal`, `#harassment`, `#eBay`

---

<a id="item-2"></a>
## [微软牵头公开信捍卫开放权重 AI 模型](https://simonwillison.net/2026/Aug/2/open-letters/#atom-everything) ⭐️ 8.0/10

2026 年 7 月 24 日，微软牵头发布公开信《开放权重与美国 AI 领导力》，共有包括英伟达、亚马逊、Y Combinator 和后来加入的 OpenAI 在内的 235 家 AI 相关公司签署，反对政府对开放权重模型的限制。三天后 Anthropic 发布自身立场，7 月 28 日再有 1324 名前沿 AI 公司员工签署《Pacing the Frontier》，呼吁审慎把控自动化 AI 开发步伐。 这波公开信标志着 AI 产业大规模动员以影响监管走向，试图对抗以安全为由限制开放权重模型的提案。其结果将影响先进 AI 的开放性、中美竞争格局，以及模型蒸馏和自动化 AI 研究的治理方式。 微软牵头的公开信特别支持模型蒸馏，认为政策制定者不应将合法的模型开发技术与盗用混为一谈。Anthropic 拒绝签署该信，其 CEO Dario Amodei 呼吁打击工业规模的蒸馏操作，同时表示 Anthropic 从未主张禁止开放权重模型。

rss · Simon Willison · 8月2日 04:16

**背景**: 开放权重模型是指将核心训练参数公开发布、供任何人下载的 AI 模型，这让技术更易获取，但不一定符合完整开源定义。随着各国政府考虑以安全为由施加限制，这场争论日益激烈：支持者认为开放权重有助于透明和分布式监督，批评者则担心被威权政权或恶意行为者滥用。近期这些公开信反映了 AI 社区在创新、竞争与安全之间如何平衡的紧张关系。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights : not quite what you’ve been told – Open Source Initiative</a></li>
<li><a href="https://www.nytimes.com/2026/07/28/technology/open-weight-ai.html">What Is Open-Weights A.I.? - The New York Times</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#open weights`, `#AI regulation`, `#Microsoft`, `#open source`

---

<a id="item-3"></a>
## [LLM 上下文退化：研究总结与实用缓解习惯](https://www.reddit.com/r/MachineLearning/comments/1vdsgcj/context_degradation_in_llms_what_the_papers/) ⭐️ 8.0/10

r/MachineLearning 上的一篇帖子综合了关于大语言模型上下文退化的近期研究，并提出了在长分析会话中缓解质量下降的实用习惯。 随着模型不断宣传更长的上下文窗口，从业者发现输出质量在达到上限之前就已下降；该帖将研究结论与可落地的工作流相结合，对从事长文档分析或智能体推理的人都有参考价值。 该帖的主要贡献在于综合了现有研究结论——包括“lost in the middle”现象和长上下文基准上的性能退化——并将其转化为个人化的工作习惯。它没有提出新模型或新数据集，而是连接了研究与日常实践。

reddit · r/MachineLearning · /u/usernamehere93 · 8月2日 20:20

**背景**: 大语言模型在有限的上下文窗口内运行，长对话或长文档可能会出现上下文退化，即连贯性和可用性逐渐下降。“lost in the middle”现象表明，模型对上下文开头和结尾信息的利用往往好于中间部分。LongBench、RULER 以及 Artificial Analysis Long Context Reasoning 等基准试图衡量这些效应，结果通常显示性能会随输入长度增加而下降。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jameshoward.us/2024/11/26/context-degradation-syndrome-when-large-language-models-lose-the-plot">Context Degradation Syndrome: When Large Language Models ...</a></li>
<li><a href="https://www.emergentmind.com/topics/context-degradation-in-large-language-models">Context Degradation in LLMs</a></li>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-long-context-reasoning">Artificial Analysis Long Context Reasoning Benchmark Leaderboard | Artificial Analysis</a></li>

</ul>
</details>

**标签**: `#LLM`, `#context length`, `#machine learning`, `#practical tips`

---

<a id="item-4"></a>
## [AI 芯片每 9 个月翻番，2028 年底全球将达 2 亿颗](https://www.nytimes.com/interactive/2026/07/29/technology/ai-chips-data-center-boom.html) ⭐️ 8.0/10

据 Epoch AI 估算，全球 AI 芯片数量目前约 2000 万颗，每 9 个月翻一番，到 2028 年底将达约 2 亿颗。IDC 预测 2029 年全球 AI 基础设施投资将突破 1 万亿美元，而去年为 3180 亿美元。 这一前所未有的基础设施扩建由“规模定律”驱动，正在重塑全球算力格局，美国控制着约 80% 的 AI 算力。但大规模建设也引发对电价上涨、环境问题以及类似历史上基建狂热带来泡沫破裂的担忧。 仅 Google 一家的 AI 芯片数量据信是中国所有公司的四倍，这正推动中国加速自研半导体和 AI 基础设施建设。经济学家警告当前支出可能超过盈利，而扩建已导致电价上涨和环境争议。

telegram · zaihuapd · 8月2日 01:01

**背景**: “规模定律”（Scaling Laws）是 AI 中的经验观察，即模型性能会随着算力增加而可预测地提升，这促使科技公司不断扩建数据中心。Epoch AI 是成立于 2022 年的非营利研究机构，通过历史趋势分析研究 AI 发展轨迹，本文引用了其预测数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://epoch.ai/">Epoch AI</a></li>
<li><a href="https://baoyu.ai/blog/state-of-ai-in-2026-lex-fridman-podcast">栏目对话和访谈：Sebastian Raschka 和 Nathan Lambert 在 Lex...</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#infrastructure`, `#scaling laws`, `#data centers`, `#AI investment`

---


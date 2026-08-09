# Horizon 每日速递 - 2026-08-09

> 从 33 条内容中筛选出 6 条重要资讯。

---

1. [基因组语言模型生成可存活的噬菌体基因组](#item-1) ⭐️ 9.0/10
2. [开发者对应用被拒的道歉文被指抄袭并误导 John Gruber](#item-2) ⭐️ 8.0/10
3. [AI 可穿戴设备记录一切：反监控对策的兴起](#item-3) ⭐️ 8.0/10
4. [全球最大单体 AI 算力设施在内蒙古乌兰察布投产](#item-4) ⭐️ 8.0/10
5. [马斯克公布 SpaceX 月球工厂计划：机器人生产 AI 卫星](#item-5) ⭐️ 8.0/10
6. [MiniMax H3 团队 AMA：将开源 2K DiT 模型与稀疏注意力](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [基因组语言模型生成可存活的噬菌体基因组](https://www.reddit.com/r/MachineLearning/comments/1vjj4pr/r_generative_design_of_novel_bacteriophages_with/) ⭐️ 9.0/10

研究人员使用基因组语言模型 Evo 1 和 Evo 2，以裂解性噬菌体 ΦX174 为模板设计了完整噬菌体基因组，并通过实验确认了 16 个可存活的噬菌体。这是首次证明生成式语言模型能够在全基因组规模上产生功能性序列。 这项工作表明，通用基因组语言模型不仅能预测，还能生成完整、有功能的基因组，为合成生物学和噬菌体疗法开辟了新途径。同时证明 AI 设计的生物体可以具有显著的进化新颖性，这意味着生物系统工程方式的范式转变。 模型以ΦX174（一种感染大肠杆菌的小型单链 DNA 病毒）为设计模板，生成了具有真实遗传结构和理想宿主特性的全基因组序列。所得的 16 个可存活噬菌体表现出显著的进化新颖性，突显了 Evo 2 等基因组基础模型（基于 9 万亿碱基对训练）的生成能力。

reddit · r/MachineLearning · /u/moschles · 8月9日 07:11

**背景**: 基因组语言模型（gLMs）是在 DNA 和 RNA 序列上训练的大型语言模型，将基因组视为一种生物学文本，其语法编码了调控相互作用。Evo 2 是一个前沿的基因组基础模型，能够以单核苷酸分辨率预测功能特性并生成序列，上下文长度可达 100 万碱基对。噬菌体ΦX174 是一种历史上重要且非常小的病毒感染大肠杆菌，是测试全基因组设计的理想模板。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nature.com/articles/s41586-026-10176-5">Genome modelling and design across all domains of life with Evo 2 | Nature</a></li>
<li><a href="https://arcinstitute.org/tools/evo">Evo 2: DNA Foundation Model | Arc Institute</a></li>
<li><a href="https://en.wikipedia.org/wiki/Phi_X_174">Phi X 174 - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI for biology`, `#genome language models`, `#synthetic biology`, `#Evo 2`, `#bacteriophage design`

---

<a id="item-2"></a>
## [开发者对应用被拒的道歉文被指抄袭并误导 John Gruber](https://blog.terrygodier.com/2026/08/09/mea-culpa-dark-hours.html) ⭐️ 8.0/10

一位开发者的占星应用被 App Store 拒绝后，发布了一篇题为《Mea Culpa – Dark Hours》的文章，但 Hacker News 评论者指控他用自己的应用替换成了开源天文应用 Dark Hours 的副本，甚至连名字都照搬。文章还被指没有为误导知名苹果博主 John Gruber 而道歉。 这起争议凸显了与 AI 生成代码、开源署名以及开发者社区中公开道歉可信度相关的伦理问题。它也引发了对苹果 App Store 审核流程如何被有影响力的科技评论者讨论的质疑。 社区指出，原始 Dark Hours 应用可在 darkhours.app 获取，而 Gruber 据称在了解情况后在 Daring Fireball 上发布了撤回文章。评论者还指出，这篇道歉文没有承认向 Gruber 编造了有关苹果审核流程的不实说法，并怀疑开发者将复制现有项目的责任推给了 AI（Claude）。

hackernews · satvikpendem · 8月9日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=49231154)

**背景**: 苹果 App Store 有严格的审核流程，因占星内容等原因被拒绝的应用，有时会在重新提交前进行大幅修改。像 Dark Hours 这样的开源项目虽然可以在其许可证下合法复用，但在未署名的情况下完整复制整个项目，通常被视为抄袭，即使复制行为是由 AI 编程助手完成的。

**社区讨论**: Hacker News 评论者大多持怀疑态度，有人说他们“根本不信”有关 AI 的借口。还有人批评该文章没有向 John Gruber 道歉，一位评论者称这篇道歉文是“有限坦白”（limited hangout），即一种只披露部分真相的危机公关策略。

**标签**: `#AI ethics`, `#plagiarism`, `#App Store`, `#open source`, `#community controversy`

---

<a id="item-3"></a>
## [AI 可穿戴设备记录一切：反监控对策的兴起](https://www.theatlantic.com/technology/2026/05/ai-wearable-surveillance-countermeasures/687203/) ⭐️ 8.0/10

《大西洋月刊》于 2026 年 5 月发表文章，探讨 AI 可穿戴设备如何实现对日常生活的无孔不入的记录，并介绍了对抗性服装、干扰人脸识别的迷彩图案以及屏蔽信号的穿戴设计等应对措施，帮助个人抵抗无处不在的监控。 随着智能眼镜等 AI 可穿戴设备的普及，这篇文章揭示了一场日益严重的隐私危机，以及新兴的反监控装备市场。它还引发了关于企业权力的讨论，即政府是否应监管那些在未经真正同意的情况下通过记录人们获利的企业。 文章具体讨论了能破坏人脸识别算法的对抗性穿戴设备、受一战‘眩惑迷彩’启发的技术，以及人眼不可见的红外干扰措施。文中提供了存档链接供读者阅读，相关讨论还提及芝加哥大学早期‘干扰器’研究项目作为前身。

hackernews · ike\_usawa · 8月9日 11:30 · [社区讨论](https://news.ycombinator.com/item?id=49230477)

**背景**: 生活记录（lifelogging）是指通过可穿戴技术持续记录个人生活的做法，最早可追溯到 2003 年 DARPA 的 LifeLog 项目。‘反向监控’（sousveillance）一词描述的是普通公民而非权威机构‘自下而上’的记录行为，随着摄像头和传感器缩小并融入日常穿戴设备，这一行为变得更加可行。作为回应，反监控服装与装备应运而生，利用图案、材料和信号来干扰机器视觉并阻止追踪。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lifelog">Lifelog - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Sousveillance">Sousveillance - Wikipedia</a></li>
<li><a href="https://theydidntask.com/blog/anti-ai-fashion-adversarial-wearables">Anti-Surveillance Clothing: 7 Real Options (and Their Limits) in 2026</a></li>
<li><a href="https://weburbanist.com/2016/11/28/how-to-be-invisible-15-anti-surveillance-designs-installations/">How to Be Invisible: 15 Anti-Surveillance Gadgets &amp; Wearables | Urbanist</a></li>

</ul>
</details>

**社区讨论**: 评论区普遍表达了对企业监控的强烈不满，有人呼吁建立‘企业与国家的分离’，也有人指出奥巴马多年前就在推介监视资本主义。多位评论者提到人们自愿使用带有监控功能的设备和应用，暗示对缺乏集体反抗的无奈；还有评论者分享了芝加哥大学早期反监控研究的链接。

**标签**: `#surveillance`, `#AI`, `#privacy`, `#wearables`, `#society`

---

<a id="item-4"></a>
## [全球最大单体 AI 算力设施在内蒙古乌兰察布投产](https://www.globaltimes.cn/page/202608/1367666.shtml) ⭐️ 8.0/10

2026 年 8 月 6 日，远景科技集团宣布“远景乌兰察布星河基地”正式投产。该基地是全球最大的单体 AI 算力设施，建筑面积 12 万平方米，支持百万 GPU 并行计算。 这一里程碑极大扩展了中国 AI 算力规模，并以 2GW 的规划容量和面向 Token 产出的优化设计，提升了全球 AI 数据中心的规模基准。它还强化了“东数西算”战略，为紧邻北京的绿色大型 AI 集群提供了可复制的模式。 该基地绿电占比超过 80%，到北京的数据传输时延为 4.2 毫秒，电价较京津冀地区低约 50%。它是远景“戈壁使命”计划的首个旗舰项目，旨在为国产算力集群提供可复制的方案。

telegram · zaihuapd · 8月9日 05:06

**背景**: 乌兰察布是中国“东数西算”工程的八大国家级枢纽节点之一，该工程将算力任务引导至可再生能源丰富的西部地区。如今的 AI 数据中心日益以 Token 吞吐量——即生成 AI 模型 Token 的速度——来衡量，而不仅仅看 GPU 数量。“戈壁使命”是远景科技集团在沙漠和草原地区建设绿色大规模 AI 基础设施的计划；远景是一家总部位于江苏的绿色科技企业，专注于智能风电、储能和零碳解决方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://threadreaderapp.com/thread/2079595760207925390.html">Thread by @rydcunningham on Thread Reader App – Thread Reader...</a></li>
<li><a href="https://www.andela.com/publication/beyond-gpus-how-token-economics-are-reshaping-the-modern-data-center">Beyond GPUs: How token economics are reshaping the modern data ...</a></li>
<li><a href="https://www.envision-group.com/cn/">远景科技集团 Envision Group</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data center`, `#GPU computing`, `#green energy`, `#China`

---

<a id="item-5"></a>
## [马斯克公布 SpaceX 月球工厂计划：机器人生产 AI 卫星](https://finance.yahoo.com/technology/articles/pure-insanity-elon-musk-details-173635969.html) ⭐️ 8.0/10

在 SpaceX 首次公开财报电话会议上，埃隆·马斯克公布了一项在月球建立自动化工厂的计划。机器人将从月球土壤中提取矿物，生产 AI 计算卫星，并利用电磁质量驱动器将其发射入轨。 这一提议可能将太空制造从地球运载转变为月球本地生产，降低发射成本，并为轨道上的大规模 AI 基础设施提供可能。它也凸显了机器人、AI 与太空探索日益融合的趋势，不过马斯克的时间表历来较为乐观。 月球环境极为严苛，月尘具有磨损性，昼夜各持续 14 天。SpaceX 前副总裁 Jim Cantrell 称该计划“纯属疯狂”，但认为马斯克有能力实现；公司当季营收 78 亿美元，但太空部门因 Starship 研发录得 2.05 亿美元亏损。

telegram · zaihuapd · 8月9日 05:37

**背景**: 质量驱动器（mass driver）是一种拟议中的非火箭发射系统，利用直线电机或电磁线圈将有效载荷加速到高速。原位资源利用（ISRU）是在目的地天体（如月球风化层或水冰）就地取材，而非从地球携带来。这些概念支撑了在月球建立工厂的想法：提取本地资源、制造硬件，并免去地球重型物流将其发射入轨。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mass_driver">Mass driver</a></li>
<li><a href="https://www.arborialabs.com/applications/macro_scale/in_situ_resource_utilization">In - Situ Resource Utilization ( ISRU ) – Arboria Labs</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#AI`, `#Space Manufacturing`, `#Robotics`, `#Lunar Base`

---

<a id="item-6"></a>
## [MiniMax H3 团队 AMA：将开源 2K DiT 模型与稀疏注意力](https://www.reddit.com/r/StableDiffusion/s/fjM3d7AEV8) ⭐️ 8.0/10

在 r/StableDiffusion 的 Reddit AMA 中，MiniMax H3 团队宣布计划开源一个 2K 再生模型（专用潜空间 DiT，而非普通超分模型）以及稀疏注意力参考实现。他们还在考虑推出 4/8 步低步数版本，并从 H3 模型谱系衍生出一款独立图像生成模型。 这标志着领先的视频生成团队在开源方面的重大推进，有望让高分辨率视频生成和高效注意力技术惠及更广泛的社区。稀疏注意力实现有望在不产生可感知画质损失的情况下降低计算成本并提升质量，使研究人员和开发者受益。 团队尚未公布 H3-Regenerate-2K 模型的具体发布日期。他们承认社区反馈的 Ref2VA 画质退化和纹理细节模糊问题，并表示已着手改进。

telegram · zaihuapd · 8月9日 08:28

**背景**: DiT（扩散 Transformer）是一种扩散模型架构，用基于潜空间补丁的 Vision Transformer 替代常用的 U-Net 主干网络，具有更好的可扩展性。稀疏注意力是一种优化技术，只对有意义的 token 子集计算注意力，而不是所有 token 对，从而降低标准注意力 O\(N²\) 的复杂度。MiniMax H3 是一个开放权重的全模态生成模型，可联合处理文本、图像、视频和音频。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2212.09748">[2212.09748] Scalable Diffusion Models with Transformers</a></li>
<li><a href="https://deepfa.ir/en/blog/sparse-attention-efficient-text-processing-language-models">Sparse Attention: Smart Architecture for Efficient Processing in Language Models</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>

</ul>
</details>

**标签**: `#video generation`, `#open-source`, `#sparse attention`, `#MiniMax`, `#AI research`

---


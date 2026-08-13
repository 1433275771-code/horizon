---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 34 条内容中筛选出 10 条重要资讯。

---

1. [DRAM 意面化：逆向地址加扰以解锁隐藏内存](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Pro 0813 已通过 API 发布，开放权重上线 Hugging Face](#item-2) ⭐️ 9.0/10
3. [Gemini 3.7 Flash](#item-3) ⭐️ 8.0/10
4. [OpenAI 与 Cerebras 推出 GPT-5.6 Sol Ultrafast，推理速度提升近 7 倍](#item-4) ⭐️ 8.0/10
5. [DeepSeek 发布开源 Harness 开发者预览版](#item-5) ⭐️ 8.0/10
6. [《选择无聊技术》：创新代币理念的持久价值](#item-6) ⭐️ 8.0/10
7. [特朗普签署备忘录，允许私企开展政府背书的海外网络攻击](#item-7) ⭐️ 8.0/10
8. [DeepMind 推手语转文字模型 SL2T，首次落地 Pixel 11](#item-8) ⭐️ 8.0/10
9. [长鑫存储超越腾讯，成中国市值最高公司](#item-9) ⭐️ 8.0/10
10. [OpenAI 预览 Ultrafast 模式，GPT-5.6 Sol 提速 14 倍](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DRAM 意面化：逆向地址加扰以解锁隐藏内存](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

Christopher Domas 的项目 skitter-creek-bath-salts 展示了如何使用 z3 求解器逆向 DRAM 地址加扰，将一致的物理地址转换为加扰后的“意面化”视图。这使拥有 ring-0 权限的攻击者能够访问通常受保护的内存区域，如 AMD Jaguar（AMD16h）系统中的 PSP 私有内存、SMRAM 和 C6 空闲状态。 这项研究打破了硬件级内存隔离，证明 DRAM 加扰并非安全边界，而是一个可绕过的混淆层。它可能削弱 Xbox、PlayStation 等游戏机或任何依赖内存加扰向 CPU 隐藏固件的平台，使单纯的 ring-0 入侵升级为对平台的完全控制。 求解出的变换被描述为“罗塞塔石碑”，可将一致内存视图中的任意目标地址映射到意面化视图中的别名，从而绕过平台围栏和安全检查。README 指出，Zen 3 的内存控制器寄存器基地址有所不同，因此新一代 CPU 可能不受影响，但仍需进一步研究。

hackernews · matt\_d · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**背景**: DRAM 地址加扰是内存控制器使用的一种技术，它会将物理地址在通道、层级、bank 和行之间打乱，以提升性能和散热均匀性。这种映射通常作为安全措施保密，但研究人员已证明可通过侧信道技术和形式化求解器对其进行逆向。项目名称借用“意面化”（天体在极端引力下被拉伸）作为扭曲内存视图的比喻。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/xoreaxeaxeax/skitter-creek-bath-salts">GitHub - xoreaxeaxeax/skitter-creek-bath-salts: Unlocking _everything_ on the CPU with DRAM scrambling · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Memory_scrambling">Memory controller - Wikipedia</a></li>
<li><a href="https://arxiv.org/pdf/2004.02354">DRAMDig: A Knowledge-assisted Tool to Uncover DRAM Address Mapping</a></li>

</ul>
</details>

**社区讨论**: 评论者对 Christopher Domas 即将在 Black Hat 上发表的演讲表现出极大热情，并提到他此前在逆向工程和硬件后门方面的工作。一些人对早期计算机简单易懂的 DRAM 表示怀念，另一些人则担心这对 Xbox 和 PlayStation 安全团队的影响。除了 AMD Jaguar 之外，哪些较新的 CPU 家族可能受到影响仍是疑问。

**标签**: `#DRAM`, `#hardware security`, `#reverse engineering`, `#memory hacking`, `#exploitation`

---

<a id="item-2"></a>
## [DeepSeek V4 Pro 0813 已通过 API 发布，开放权重上线 Hugging Face](https://simonwillison.net/2026/Aug/12/deepseek-v4-pro-0813/) ⭐️ 9.0/10

DeepSeek 最新的 Pro 模型 DeepSeek V4 Pro 0813 现已通过 OpenRouter 等渠道以 API 方式提供。随后其开放权重已在 Hugging Face 上发布，共 1.7 万亿参数，大小约 893 GB。 DeepSeek 再次发布大规模开放权重模型，为开发者和研究者提供了比肩闭源商业 API 的前沿选择，可能加剧价格竞争并加速本地部署。1.7 万亿参数的权重可公开下载，也进一步壮大了前沿规模下的开放权重生态。 该模型增强了 Agent 能力，并原生支持 Responses API 格式以适配 Codex；V4-Pro 和 V4-Flash 的思考模式新增 low、high、max 三档。API 将于 2026 年 8 月 17 日实行峰谷定价，闲时价格仅为高峰时段的一半；Hugging Face 上的权重为 893 GB、1.7 万亿参数。

rss · Simon Willison · 8月12日 23:59

**背景**: 开放权重指将训练好的神经网络数值参数公之于众，用户可检查、微调并在本地运行模型，即使未公开完整训练数据和代码，也提升了透明度。OpenRouter 是一个统一的 API 网关，开发者可通过单一接口访问多家厂商的数百个大语言模型，因此常成为新模型的首发渠道。参数是神经网络中通过训练学到的权重和偏置；1.7 万亿的参数量属于超大模型，使该模型处于当代大语言模型的前沿规模。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://promptengineering.org/llm-open-source-vs-open-weights-vs-restricted-weights/">Openness in Language Models: Open Source vs Open Weights vs...</a></li>
<li><a href="https://www.codecademy.com/article/what-is-openrouter">What is OpenRouter ? A Guide with Practical Examples | Codecademy</a></li>
<li><a href="https://news.ycombinator.com/item?id=37804839">Ask HN: GPT-4 has 1.7T parameters. What&#x27;s a parameter? | Hacker News</a></li>

</ul>
</details>

**标签**: `#AI`, `#DeepSeek`, `#machine-learning`, `#open-weights`, `#model-release`

---

<a id="item-3"></a>
## [Gemini 3.7 Flash](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 8.0/10

谷歌发布了 Gemini 3.7 Flash，这是一款具备强大视觉性能且定价优惠的新 AI 模型。

hackernews · thisisauserid · 8月13日 17:23 · [社区讨论](https://news.ycombinator.com/item?id=49289112)

**标签**: `#Gemini`, `#Google`, `#AI`, `#LLM`, `#Model Release`

---

<a id="item-4"></a>
## [OpenAI 与 Cerebras 推出 GPT-5.6 Sol Ultrafast，推理速度提升近 7 倍](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

OpenAI 与 Cerebras 宣布推出 GPT-5.6 Sol Ultrafast 模式，该模式在 11 小时 11 分钟内回答了全部 2500 道 HLE 问题，而 Claude Fable 5 需要 78 小时 27 分钟——以相近的准确度实现了近 7 倍的加速。根据 Artificial Analysis 报告的输出速度，该模式的运行速度比 Fable 5 快 11 倍，比 Fast 模式下的 Opus 4.8 快 5 倍。 此次合作表明，在晶圆级硬件上实现超快速 LLM 推理是可行的，可能降低实时 AI 应用的延迟和成本。同时，它也引发了行业范围内关于推理速度是否以牺牲推理质量为代价的争论，这可能影响未来 AI 模型的部署与优化方式。 Cerebras 和 OpenAI 的公告均未明确说明 Ultrafast 模式产生的结果与常规 GPT-5.6 Sol 完全相同，因此两者性能是否完全一致尚未得到确认。Ultrafast 模式也未公布定价信息，这可能意味着它面向企业级用户，或两家公司正在评估市场需求后再确定价格。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: Cerebras Systems 开发了全球最大的 AI 处理器——晶圆级引擎（WSE），其中 WSE-3 包含 4 万亿个晶体管、90 万个 AI 优化核心、44GB 片上 SRAM 以及每秒 21 PB 的内存带宽。传统的 LLM 推理依赖 GPU 集群，而 Cerebras 的晶圆级架构提供了一种截然不同的方案，能够大幅加速 token 生成。此次与 OpenAI 的合作旨在探索定制芯片如何将前沿模型的推理速度推向极限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://www.cerebras.ai/chip">Product - Chip - Cerebras</a></li>
<li><a href="https://introl.com/blog/cerebras-wafer-scale-engine-cs3-alternative-ai-architecture-guide-2025">Cerebras Wafer-Scale Engine | Introl Blog</a></li>

</ul>
</details>

**社区讨论**: Hacker News 评论者对 OpenAI 与 Cerebras 的合作表示兴奋，一些人强调速度有助于 LLM 进行迭代思考并提升推理质量。然而，也有人持怀疑态度：他们指出公告未明确说明 Ultrafast 模式与原版模型质量一致，并认为缺失定价细节可能意味着该服务价格过高或仍处于探索阶段。

**标签**: `#AI`, `#LLM`, `#Inference`, `#OpenAI`, `#Cerebras`

---

<a id="item-5"></a>
## [DeepSeek 发布开源 Harness 开发者预览版](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek Harness（dsh）的开发者预览版，这是一个基于 Cordis 插件系统的开源 agent harness，采用 MIT 许可证，源码已在 GitHub 上提供。该预览版引入了可追踪的追加式会话日志，以及“万物皆插件”的架构。 Agent harness 基础设施对于生产级 LLM agent 正变得至关重要，而 DeepSeek 以开源方式提供具备完整可追踪性和插件系统的工具，可能会影响更广泛的开发者生态。这也促使其他 AI 实验室在各自的 agent 工具中提供类似的透明度。 该 harness 由 Cordis v4 驱动，支持热重载以及在进程不重启的情况下动态启用或停用插件，并且可以回滚插件产生的副作用。会话日志为追加写入，记录系统提示词、推理过程、工具调用、子代理调度和上下文注入；Trajectory 视图支持在同一事件流上进行恢复、分叉、搜索和重放。

hackernews · bjin · 8月13日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49285244)

**背景**: Agent harness 是围绕大语言模型的软件基础设施，负责管理工具调用、记忆、状态持久化、执行环境和反馈循环，使模型能够执行任务，而不仅仅是对提示做出响应。DeepSeek Harness 采用“万物皆插件”的架构，并构建在 Cordis 之上；Cordis 是一套插件系统，最初用于 Koishi 等项目，支持插件的热加载和卸载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">GitHub - deepseek -ai/ deepseek - harness : DeepSeek Harness ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agent_harness">Agent harness - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 一位作者确认这是采用 MIT 许可证的早期开发者预览版，并表示虽有粗糙之处但欢迎反馈。评论者称赞完整可追踪性是“杀手级”功能，相比美国模型模糊化的追踪记录优势明显；也有人讨论了底层的 Cordis v4 论文，并对“万物皆插件”的设计表达了审美疲劳。

**标签**: `#AI`, `#developer-tools`, `#open-source`, `#agent-harness`, `#plugin-system`

---

<a id="item-6"></a>
## [《选择无聊技术》：创新代币理念的持久价值](https://mcfunley.com/choose-boring-technology) ⭐️ 8.0/10

Dan McKinley 于 2015 年发表的《选择无聊技术》一文被重新推荐，并获得高分评价，被视为关于务实技术选择的经典之作。文章主张公司应默认采用成熟、无趣的技术，只在新技术能带来真正竞争优势时，才花费有限的&\#x27;创新代币&\#x27;。 这篇文章为工程管理者提供了一个容易记住的框架，用来抵制追逐热门技术和频繁重写的冲动。&\#x27;创新代币&\#x27;的比喻已成为解释架构决策中&\#x27;稳定性&\#x27;与&\#x27;新颖性&\#x27;之间权衡的常用说法。 McKinley 提出，一家公司在很长一段时间内大致只有三枚创新代币，每选择一项新技术就要花掉一枚。他的观点源自 Etsy 的工作经验：刻意选择 MySQL 和 PHP 等&\#x27;无聊&\#x27;技术，既支撑了快速产品开发，又避免了运维复杂度失控。

hackernews · tosh · 8月13日 17:48 · [社区讨论](https://news.ycombinator.com/item?id=49289512)

**背景**: &\#x27;无聊技术&\#x27;并不意味着过时技术，而是指像 PostgreSQL 这样成熟、可预测、文档完善、行为稳定的工具。&\#x27;创新代币&\#x27;这一概念经由 McKinley 的文章普及，提醒团队每引入一个新组件都会带来运维和认知成本，因此必须谨慎地分配&\#x27;创新&\#x27;额度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lessannoyingbusiness.com/post/innovation-tokens">Innovation Tokens - When to break from the status quo</a></li>
<li><a href="https://xebia.com/blog/how-innovation-tokens-can-change-your-life/">How Innovation Tokens Can Change Your Life | Xebia</a></li>
<li><a href="https://www.peal.dev/blog/boring-technology-principle-why-we-pick-proven-tools">The Boring Technology Principle : Why We Reach for... — peal.dev</a></li>

</ul>
</details>

**社区讨论**: 评论区整体高度认可这篇文章，有评论者称&\#x27;创新代币&\#x27;是自己作为产品经理和工程领导遇到过的最实用概念之一。也有人补充例外情况：当团队已经具备某项技术的内部专长时，这个选择即便不&\#x27;无聊&\#x27;也可能是正确的；在 AI Agent 时代，或许应该把创新代币全部投给 Agent，同时让周边技术保持无聊。另有一条评论对文章观点提出反对意见，但内容已被截断。

**标签**: `#technology strategy`, `#engineering culture`, `#software architecture`, `#innovation tokens`, `#pragmatism`

---

<a id="item-7"></a>
## [特朗普签署备忘录，允许私企开展政府背书的海外网络攻击](https://www.bloomberg.com/news/articles/2026-08-13/trump-enlists-private-sector-to-boost-cyber-offensive-arsenal) ⭐️ 8.0/10

美国总统特朗普签署备忘录，授权受联邦政府直接控制与监督的私营企业在海外开展监控和网络攻击，以打击针对美国人的外国网络化跨国犯罪组织。 这标志着私营企业进一步参与国家支持的进攻性网络行动，模糊了企业与政府行为之间的界限。它可能重塑美国进行网络防御的方式，并影响全球法律界与科技界。 国土安全部（DHS）将负责运行该项目，并与司法部（DOJ）协调监督。参与企业须维持至少 100 万美元的保证金或托管款，如不遵守合同约定将被没收。

telegram · zaihuapd · 8月13日 05:10

**背景**: 总统备忘录是一种无需国会批准即可发布的行政指令。这份备忘录让私营网络安全企业参与传统上由 NSA（国家安全局）和网络司令部等政府机构专属的进攻性行动。100 万美元保证金作为合规的财务担保。批评者可能会质疑私营实体在海外开展监控和攻击的法律依据与问责机制。

**标签**: `#cybersecurity`, `#surveillance`, `#US policy`, `#offensive cyber operations`, `#private sector`

---

<a id="item-8"></a>
## [DeepMind 推手语转文字模型 SL2T，首次落地 Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 8.0/10

谷歌 DeepMind 发布大规模多语言手语转文字模型 SL2T，已率先在 Pixel 11 的 Gboard 和实时字幕（Live Transcribe）中支持美国手语转英语，后续将扩展到更多设备和语言。 这是手语 AI 模型首次直接进入消费级产品，有望显著改善聋人和听障人士的沟通体验。同时表明在设备端以保护隐私的方式实现手语翻译已经成为现实。 SL2T 使用超过 10 万小时、50 多种手语的数据训练，在 FLEURS-ASL 基准上零样本得分达 70 BLEURT，远超此前纪录。为保护隐私，它只处理手部和身体姿态关键点，不读取原始视频。

telegram · zaihuapd · 8月13日 08:55

**背景**: 手语翻译为文字通常需要大量带标注的视频数据。SL2T 采用隐私优先的思路：先从视频中估计手、身体和面部关键点，再直接基于这些坐标进行翻译，而不查看原始画面。FLEURS-ASL 是 FLEURS 语音基准向美国手语的扩展；BLEURT 是一个神经网络评估指标，通过将生成文本与参考答案比较来打分。所谓“零样本”指模型未在该基准上微调就能获得这一成绩。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/">Putting sign language AI into users’ hands — Google DeepMind</a></li>
<li><a href="https://arxiv.org/html/2408.13585">FLEURS - ASL : Including American Sign Language in Massively...</a></li>
<li><a href="https://github.com/google-research/bleurt">GitHub - google-research/ bleurt : BLEURT is a metric for Natural...</a></li>

</ul>
</details>

**标签**: `#DeepMind`, `#sign language`, `#translation`, `#accessibility`, `#AI model`

---

<a id="item-9"></a>
## [长鑫存储超越腾讯，成中国市值最高公司](https://www.bloomberg.com/news/articles/2026-08-13/cxmt-overtakes-tencent-to-become-most-valuable-chinese-company) ⭐️ 8.0/10

长鑫存储（CXMT）市值超过腾讯，成为中国市值最高的上市公司，市值约 5240 亿美元。该公司上月在科创板上市，首日暴涨 467%，此后股价继续上涨。 这标志着中国科技领域的一次重大格局转变：一家半导体存储器制造商的市值超越了长期位居首位的互联网巨头腾讯。这反映出在半导体自主可控和全球供应链不确定性的背景下，投资者对中国本土芯片企业的热情高涨。 长鑫存储的科创板 IPO 发行价为每股 8.66 元人民币。腾讯周四下跌 4.5%，今年以来累计下跌超过 26%，原因是该公司大幅加大了对人工智能领域的投入。

telegram · zaihuapd · 8月13日 10:10

**背景**: 长鑫存储（CXMT）是一家成立于 2016 年的中国半导体公司，总部位于安徽合肥，专注于 DRAM 存储芯片的设计与制造，产品用于手机、个人电脑、平板电脑和服务器。该公司目前是中国最大的 DRAM 厂商，也是全球第四大 DRAM 制造商。DRAM 是一种易失性内存，用于临时存储数据，几乎所有计算设备都需要使用它。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ChangXin_Memory_Technologies">ChangXin Memory Technologies</a></li>
<li><a href="https://www.cxmt.com/en/">About cxmt - cxmt</a></li>
<li><a href="https://www.binance.com/en/square/post/344907979167714">#changxintechsetsipopriceatcny8.66 AI Hardware Boom</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#market-cap`, `#China tech`, `#CXMT`, `#Tencent`

---

<a id="item-10"></a>
## [OpenAI 预览 Ultrafast 模式，GPT-5.6 Sol 提速 14 倍](https://openai.com/index/previewing-ultrafast/) ⭐️ 8.0/10

OpenAI 预览了面向 GPT-5.6 Sol 的 Ultrafast 模式，相比标准处理最多可提速 14 倍，在 OpenAI API 上每秒输出可达 750 个 token。该服务由 Cerebras 提供支持，目前仅向少数客户限量开放。 这一提速可能让 OpenAI 的旗舰模型在故障响应、金融研究、客服和电商等对时延敏感的场景中变得切实可用。同时，这也表明 Cerebras 的晶圆级硬件正成为高吞吐推理场景中 GPU 的有力替代方案。 Ultrafast 模式目前是限量预览，OpenAI 表示将随算力扩充逐步扩大访问。其最高吞吐量为每秒 750 个 token，这一水平在标准基础设施上此前难以企及。

telegram · zaihuapd · 8月13日 17:04

**背景**: Cerebras 是一家总部位于美国的 AI 基础设施公司，其晶圆级引擎专为快速 AI 处理而设计，宣称比 GPU 更大、更快。GPT-5.6 Sol 是 OpenAI 的旗舰模型，拥有 105 万 token 的上下文窗口，在编程和智能体工作流方面表现出色。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cerebras.ai/">Cerebras is the go-to platform for fast and effortless AI training.</a></li>
<li><a href="https://www.edenai.co/providers/cerebras">Cerebras API: Models, Pricing &amp; Speed</a></li>
<li><a href="https://openrouter-web.vercel.app/openai/gpt-5.6-sol">GPT - 5 . 6 Sol - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5`, `#AI performance`, `#Cerebras`, `#API`

---
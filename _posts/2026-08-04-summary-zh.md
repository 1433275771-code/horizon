---
layout: default
title: "Horizon Summary: 2026-08-04 (ZH)"
date: 2026-08-04
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [Keyv 及相关 npm 包在活跃的 Shai-Hulud 供应链攻击中遭到入侵](#item-1) ⭐️ 9.0/10
2. [谷歌为 Anthropic 搭建 2000 亿美元华尔街融资机器](#item-2) ⭐️ 9.0/10
3. [为多样化肤色定制的色彩空间与算法](#item-3) ⭐️ 8.0/10
4. [DeepSeek V4 Flash 在单块 AMD MI300X 上运行](#item-4) ⭐️ 8.0/10
5. [联邦快递邮件酷似钓鱼，侵蚀信任助长诈骗](#item-5) ⭐️ 8.0/10
6. [Oxide Computer 完成 4.45 亿美元 D 轮融资](#item-6) ⭐️ 8.0/10
7. [Xbox 宕机导致光盘游戏无法游玩，数字所有权争议再起](#item-7) ⭐️ 8.0/10
8. [PipeNetwork 推出 MiniMax-H3 的 MLX 移植版，让 Apple Silicon 也能生成视频](#item-8) ⭐️ 8.0/10
9. [我国发布首部 L3/L4 自动驾驶强制性国标](#item-9) ⭐️ 8.0/10
10. [白宫开源 AI 监管急转弯，硅谷立场分裂](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Keyv 及相关 npm 包在活跃的 Shai-Hulud 供应链攻击中遭到入侵](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 9.0/10

一种名为 Shai-Hulud 的自复制蠕虫正在积极入侵 Keyv npm 包及其相关依赖，同时攻击 npm 生态系统中数百个其他包。该攻击仍在持续，已引发研究人员和政府机构的紧急安全警告。 此次攻击针对 Keyv 等被广泛使用的开源包，Keyv 有数百个下游依赖项目，因此入侵可能波及无数应用程序。这凸显了 npm 依赖链的系统性脆弱性，以及改进供应链安全实践的紧迫性。 该蠕虫已入侵超过 500 个包，通过 pre-install 钩子和自动化凭证窃取进行传播。攻击还利用被攻陷的维护者账户发布恶意更新，这使得在没有行为分析的情况下难以检测。

hackernews · cimi\_ · 8月4日 11:01 · [社区讨论](https://news.ycombinator.com/item?id=49166874)

**背景**: npm 注册表是 JavaScript 和 Node.js 的默认包管理器，针对它的供应链攻击正变得越来越普遍。Shai-Hulud 是一种自我传播的蠕虫，通过入侵包来窃取凭证并传播恶意代码，这标志着从传统一次性载荷攻击的重大演变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://unit42.paloaltonetworks.com/npm-supply-chain-attack/">&quot;Shai-Hulud&quot; Worm Compromises npm Ecosystem in Supply Chain Attack (Updated November 26)</a></li>
<li><a href="https://www.cisa.gov/news-events/alerts/2025/09/23/widespread-supply-chain-compromise-impacting-npm-ecosystem">Widespread Supply Chain Compromise Impacting npm Ecosystem | CISA</a></li>
<li><a href="https://www.trendmicro.com/en_us/research/25/i/npm-supply-chain-attack.html">What We Know About the NPM Supply Chain Attack | Trend Micro (US)</a></li>

</ul>
</details>

**社区讨论**: 社区成员就缓解措施展开辩论，有人提出了一个名为 Packj 的工具，通过静态和动态分析来检测入侵指标。其他人建议使用开发容器进行隔离，呼吁暂停使用 pre-install 钩子，并对脆弱的依赖系统表示不满，还有人质疑为何 GitHub 不能自动阻止攻击者的数据外传仓库。

**标签**: `#security`, `#supply-chain attack`, `#npm`, `#open-source`, `#dependency management`

---

<a id="item-2"></a>
## [谷歌为 Anthropic 搭建 2000 亿美元华尔街融资机器](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 9.0/10

谷歌悄然搭建了约 2000 亿美元的基础设施融资架构，向 Anthropic 交付超过 1500 亿美元的 AI 芯片，参与方包括博通、阿波罗、黑石、摩根士丹利及多家加密矿企。2026 年 6 月，特殊目的载体 Compute SPV 完成首批交易，购入约 350 亿美元硬件，约合 1 吉瓦算力、100 万颗 TPU。 这是有史以来规模最大的基础设施融资安排之一，可能重塑 AI 算力的融资方式，将数千亿美元的硬件从企业资产负债表中剥离。这种风险共担模式可能成为其他缺乏信用评级的 AI 公司效仿的模板。 合同总额约 2000 亿美元，约八成与芯片直接挂钩。与传统贷款不同，该结构类似项目融资：谷歌为数据中心提供担保，博通购买并协助融资芯片，阿波罗和黑石购买硬件后回租给 Anthropic。

telegram · zaihuapd · 8月4日 10:52

**背景**: Anthropic 没有信用评级，因此贷款方需要风险缓释措施。该融资通过特殊目的载体（SPV）购买芯片及相关设备，再将算力租赁给 AI 公司；贷款方以长期客户承诺为基础为资产提供融资。这种&\#x27;厂商融资&\#x27;模式借鉴了波音和 GE 推销飞机与发动机的做法，让各方都不必把数百亿美元 AI 硬件压在自家资产负债表上。分析师还指出，AI 领域存在&\#x27;循环融资&\#x27;现象，即芯片制造商和云服务商投资 AI 初创公司，而这些公司又用资金购买它们的产品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techtimes.com/articles/318207/20260611/anthropic-ai-safety-warning-meets-35b-compute-deal-silicon-valley-cannot-slow-alone.htm">Anthropic AI Safety Warning Meets $35B Compute Deal: Silicon Valley...</a></li>
<li><a href="https://finance.biggo.com/news/cc3ceaa8-e838-4501-b4c0-13b9fcba9232">Google Orchestrates $200 Billion AI Chip Financing Network in Landmark Infrastructure Deal — BigGo Finance</a></li>
<li><a href="https://blockeden.xyz/blog/2026/03/06/ai-circular-financing-loop-vendor-financing/">The Great AI Circular Financing Loop: When Vendors Fund Their Own Customers - BlockEden.xyz</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#Google`, `#Anthropic`, `#financing`, `#cloud computing`

---

<a id="item-3"></a>
## [为多样化肤色定制的色彩空间与算法](https://toneyalexander.github.io/inclusive-color-space/) ⭐️ 8.0/10

开发者发布了一个交互式网页，介绍一种简单算法和自定义色彩空间，用于在数字艺术和游戏开发中程序化生成多样化且合理的肤色。该项目包含取色器、演示以及详细的数学原理说明。 肤色选择通常很困难，而 RGB 等色彩空间对此并不直观。这种方法有望让更具包容性的角色创建变得更容易，并激发更多关于肤色感知色彩工具的研究。 作者承认方法论“有点不稳”，并列出了未来工作方向，表明当前空间是一个“足够好”的近似而非最终模型。实现基于 RGB 色彩空间，使用函数拟合和基于方程的变换。

hackernews · automatoney · 8月4日 15:16 · [社区讨论](https://news.ycombinator.com/item?id=49170165)

**背景**: 色彩空间用数值定义颜色的表示方式；RGB 很常用，但它在感知上并不均匀，也不适合表示肤色。该项目通过分析 RGB 中看起来像合理人类肤色的颜色范围，构建了一个简化的肤色色彩空间，并提供相应公式和演示。其目标是覆盖最广泛、包容的合理（但简化）肤色范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://toneyalexander.github.io/inclusive-color-space/">What Colors Are We? Constructing A Color Space For Skin Tones</a></li>

</ul>
</details>

**社区讨论**: 评论者反应积极，称赞演示效果以及将函数拟合到肤色数据上的想法。有人指出其形状与在 Oklab 中绘制的粉底色号数据一致，也有人提到了 Pantone Skin Tones 等参考，并观察到部分生成颜色略显绿、蓝或紫。

**标签**: `#color-science`, `#procedural-generation`, `#digital-art`, `#color-space`, `#skin-tones`

---

<a id="item-4"></a>
## [DeepSeek V4 Flash 在单块 AMD MI300X 上运行](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

GitHub 上的一个项目展示了在单块 AMD MI300X GPU 上运行 DeepSeek V4 Flash，速度约为每秒 150 token，并保留模型的完整原始权重。实现方式是将原本 1M token 的上下文窗口缩减为 256k token。 这是一项重要的硬件优化成果，因为它表明参数量达 284B 的 MoE 模型（激活参数 13B）可以在单块加速卡上高效运行，从而降低本地或成本敏感场景的部署门槛。同时它也凸显了 AMD MI300X 的大容量 HBM 和带宽在大型模型推理方面的竞争力，对 Nvidia 的主导地位构成挑战。 该项目保留模型的完整原始权重（MXFP4），而不是额外量化，主要折中是上下文长度从 1M token 降到 256k token。MI300X 是 OAM 模块，通常以 8 卡服务器整机形式销售，而非单张 PCIe 卡；项目的“先前工作”部分还引用了 2xMI300X 的相关实现。

hackernews · zhoutong · 8月4日 10:00 · [社区讨论](https://news.ycombinator.com/item?id=49166386)

**背景**: DeepSeek V4 Flash 是 DeepSeek V4 系列的预览版，属于混合专家（MoE）模型，总参数 284B，激活参数 13B，设计用于在 1M token 的上下文窗口内高效推理。AMD MI300X 是数据中心 GPU，配备 192GB HBM3 显存，与 Nvidia 的数据中心加速器竞争；在单块这类 GPU 上运行大型 MoE 模型，需要仔细管理内存和上下文。Ollama 和 Hugging Face 等工具现已收录 DeepSeek V4 Flash，这有助于它在本地进行实验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://ollama.com/library/deepseek-v4-flash">deepseek - v 4 - flash</a></li>
<li><a href="https://en.wikipedia.org/wiki/Amd_MI300X">Amd MI300X</a></li>

</ul>
</details>

**社区讨论**: 评论区总体上肯定了这一工作，但也提出了一些实际注意事项：MI300X 不能单独购买（通常装在约 25 万欧元的 8 卡整机中），并且“先前工作”部分遗漏了 DwarfStar，后者据称能用更少内存运行同一模型。还有人认为，256k 上下文的取舍相当合理，与 Codex 等模型相当，并且 DeepSeek V4 Flash 也应能塞进未来基于 PCIe、配备 144GB 的 MI350P 中。

**标签**: `#DeepSeek`, `#AMD MI300X`, `#LLM inference`, `#quantization`, `#hardware`

---

<a id="item-5"></a>
## [联邦快递邮件酷似钓鱼，侵蚀信任助长诈骗](https://www.troyhunt.com/thanks-fedex-this-is-why-we-keep-getting-phished/) ⭐️ 8.0/10

安全研究员 Troy Hunt 发文指出，联邦快递等正规公司会发送酷似钓鱼邮件的通知，例如带有 PDF 附件的报关通知竟来自个人发件人。这类做法让真实邮件与诈骗信息的界限变得模糊。 当可信品牌模仿诈骗邮件的模式发送邮件时，用户辨别钓鱼邮件与真实信息的能力会被削弱。这会让真正的钓鱼攻击更容易得手，也使安全培训的效果大打折扣。 评论区举出实例：联邦快递报关单由“某人”以 PDF 附件发送，谷歌存储告警使用了短域名 c.gle，美国国税局在电话语音系统中使用了商用文本转语音技术。这说明攻击者无需高级技巧，就能轻松模仿同样的外观和语气。

hackernews · stymaar · 8月4日 21:09 · [社区讨论](https://news.ycombinator.com/item?id=49175192)

**背景**: 网络钓鱼是一种社会工程攻击，攻击者将欺诈信息伪装成正常通信，以窃取账号密码或数据。SPF、DKIM、DMARC 等邮件认证标准可帮助收件服务器验证邮件是否真的来自其声明的域名，BIMI 则允许品牌在受支持的邮件客户端中显示经过验证的标识。然而，这些保护只有在企业始终遵守安全的发信规范时才有用；当正规发信方的行为与钓鱼者相似时，用户就无法再依赖熟悉的外观线索来判断真伪。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cloudflare.com/learning/email-security/dmarc-dkim-spf/">What are DMARC, DKIM, and SPF?</a></li>
<li><a href="https://en.wikipedia.org/wiki/Brand_Indicators_for_Message_Identification">Brand Indicators for Message Identification - Wikipedia</a></li>
<li><a href="https://bimigroup.org/">Home - BIMI Group</a></li>

</ul>
</details>

**社区讨论**: 评论者大多赞同作者，并分享了各自经历：有人收到过看起来像骗局的真实联邦快递报关单，有人质疑 Google 的短链接域名 c.gle 是否合法，还有人指出国税局电话系统以及泛滥的廉价通用顶级域名也在造成混乱。总体情绪是对正规机构不但没有让通信更易验证、反而加剧用户困惑表示沮丧。

**标签**: `#phishing`, `#security`, `#email`, `#cybersecurity`, `#FedEx`

---

<a id="item-6"></a>
## [Oxide Computer 完成 4.45 亿美元 D 轮融资](https://www.sec.gov/Archives/edgar/data/1795071/000179507126000002/xslFormDX01/primary_doc.xml) ⭐️ 8.0/10

根据最近提交的 SEC Form D 文件，Oxide Computer 已完成 4.45 亿美元的 D 轮融资。这是该公司迄今最大的一轮融资，此前在 2026 年早些时候曾完成 2 亿美元的 C 轮融资。 这轮巨额融资表明投资者对 Oxide 挑战传统云基础设施、押注云原生硬件的使命充满信心。这笔资金可能帮助公司扩大生产和销售，为企业客户提供超大规模云服务之外的新选择。 该 SEC Form D 文件属于 Regulation D 豁免发行通知，表格本身不披露估值或详细的投资人信息。评论者引述 Oxide 的融资历史为 2023 年 4400 万美元 A 轮、2025 年 1 亿美元 B 轮、2026 年 2 亿美元 C 轮，而本轮 4.45 亿美元 D 轮是一个明显跃升。

hackernews · depr · 8月4日 20:13 · [社区讨论](https://news.ycombinator.com/item?id=49174407)

**背景**: Oxide Computer 是一家专注于云原生硬件的初创公司，旨在重新思考企业采购和运营云基础设施的方式。Form D 是向美国 SEC 提交的 Regulation D 豁免证券发行通知，通过 SEC 的 EDGAR 电子系统申报。云原生方式通常利用容器化的微服务，使应用能够在不同环境中运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sec.gov/resources-small-businesses/capital-raising-building-blocks/what-form-d">What is Form D? - SEC.gov</a></li>
<li><a href="https://en.wikipedia.org/wiki/Form_D">Form D - Wikipedia</a></li>
<li><a href="https://aws.amazon.com/what-is/cloud-native/">What is Cloud Native? - Cloud Native Architecture Explained - AWS</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体正面：用户为这一消息欢呼，并称赞 Jessie Frazelle 的参与，有人说她做的项目都值得信任。不过，一位工程副总裁表示，他们去年提交了销售咨询但从未收到回复，尽管他们每年在 AWS 上花费约 90 万美元。还有人质疑 Oxide 是否真的向客户发货，因为他们没有看到实际部署案例。

**标签**: `#funding`, `#hardware`, `#cloud-computing`, `#infrastructure`, `#oxide-computer`

---

<a id="item-7"></a>
## [Xbox 宕机导致光盘游戏无法游玩，数字所有权争议再起](https://birchtree.me/blog/xbox-goes-down-you-cant-play-games-you-own-on-disc/) ⭐️ 8.0/10

一次大规模 Xbox 服务中断导致用户无法游玩自己拥有的实体光盘游戏，原因是微软的服务器端许可证验证不可用。微软已承认该问题，并表示将更改许可验证系统，确保光盘游戏在服务器中断或离线时不会被封锁。 这一事件表明，即使是实体光盘游戏也与 DRM 和在线基础设施紧密捆绑，削弱了“真正拥有”的意义。它强化了玩家应获得更强权利（访问、保存和转售所购软件）的论点。 微软承认光盘游戏需要经过许可证验证，但表示这类验证不应在服务器故障或离线状态下阻止游戏访问。该公司正在准备修复，并表示将在这次被广泛报道的中断事件后更改许可验证系统。

hackernews · surprisetalk · 8月4日 12:01 · [社区讨论](https://news.ycombinator.com/item?id=49167448)

**背景**: “始终在线”DRM 要求消费者在连接服务器后才能使用产品，通常用于验证许可证。微软一直在 Xbox 平台上大力推动数字发行，如今就连光盘版游戏也依赖在线许可证检查。这种做法长期以来备受争议，因为它引入了单点故障，并让正版玩家依赖服务器可用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Always-online_DRM">Always-online DRM</a></li>
<li><a href="https://ixbt.games/en/news/2026/07/30/425735-xbox-izmenit-sistemu-licenzii-posle-skandala-s-nedostupnymi-igrami.html">Xbox to Change Licensing System After Inaccessible Games Scandal</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对现代游戏脆弱性的不满，并将其与 GameCube、PS3 等旧主机作对比——那些平台上游戏可离线运行并支持局域网联机。他们认为真正的问题在于“所有权”而非实体版与数字版之分，并呼吁赋予玩家保留、备份、转售和传承游戏的权利。还有人批评 Xbox 即使在《士官长合集》等游戏中也要强制在线登录。

**标签**: `#Xbox`, `#DRM`, `#digital-ownership`, `#gaming`, `#outage`

---

<a id="item-8"></a>
## [PipeNetwork 推出 MiniMax-H3 的 MLX 移植版，让 Apple Silicon 也能生成视频](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

Simon Willison 展示了 PipeNetwork/minimax-h3-mlx——这是 MiniMax 全能模态模型 MiniMax-H3 的 MLX 移植版，并在他的 M5 Max MacBook Pro 上成功运行。他用一段文本提示生成了约 15 秒的视频片段，模型下载约 115 GB，生成耗时不到 45 分钟。 这使一个前沿的开放权重全能模态视频模型能够在普通 Apple 硬件上实际运行，减少对云端 GPU 集群的依赖。它也凸显了 MLX 生态系统的成长，使其成为在 Apple Silicon 上本地运行大型生成模型的一条可行路径。 该 MLX 移植版使用 MiniMax-H3 的 8-bit 量化版本，并与原模型的 FL2VA 组件搭配使用。Willison 指出，由于他没有参考 MiniMax 的视频提示词撰写指南，生成的音频听起来像杂乱语音；该指南包含控制音频输出的建议。

rss · Simon Willison · 8月4日 19:10

**背景**: MiniMax-H3 是一个通用的全能模态生成系统，可接受文本、图像、音频和视频输入，并一次性生成长达 15 秒、带有原生音频的视频片段。MLX 是苹果推出的开源数组框架，专为在 Apple silicon 上进行机器学习而设计，利用其统一内存架构。该项目将 MiniMax-H3 移植到 MLX，使模型能够在 Apple 硬件上本地运行，而无需依赖远程服务器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple ...</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between ...</a></li>
<li><a href="https://fal.ai/minimax-h3">MiniMax H3 - Open-Weights General-Purpose Multimodal Video ...</a></li>

</ul>
</details>

**标签**: `#MLX`, `#MiniMax-H3`, `#video generation`, `#Apple Silicon`, `#open source`

---

<a id="item-9"></a>
## [我国发布首部 L3/L4 自动驾驶强制性国标](https://wap.miit.gov.cn/jgsj/zbys/qcgy/art/2026/art_a1d2072374884287b67048a77560014e.html) ⭐️ 8.0/10

2026 年 7 月 30 日，工业和信息化部发布《智能网联汽车 自动驾驶系统安全要求》（GB 44721—2026），这是我国首部针对 L3、L4 级自动驾驶系统的强制性国家标准，拟于 2027 年 7 月 1 日起正式实施。 该标准将自动驾驶安全要求从推荐性转为强制性，为所有进入中国市场的 L3/L4 车辆设定了必须达到的最低安全门槛。这将深刻影响汽车制造商、供应商以及自动驾驶技术公司的研发与上市审批流程，重塑全球最大汽车市场中的高级别自动驾驶格局。 标准适用于搭载 L3 级和/或 L4 级系统的 M 类（载客）和 N 类（载货）车辆，但不包括自动泊车系统。该标准是对 2024 年推荐性国标的系统性升级，从企业全生命周期安全保障、系统动态驾驶能力、人机交互与用户告知、多维度检验检测四个维度构建要求体系，并要求 L3 系统具备驾驶人接管能力监测功能。

telegram · zaihuapd · 8月4日 13:06

**背景**: 中国国家标准分为强制性标准（GB，不带 T）和推荐性标准（GB/T）两类，强制性标准必须依法执行，推荐性标准则属于自愿采用。L3 级（有条件自动驾驶）和 L4 级（高度自动驾驶）是 SAE 定义的高级别自动驾驶等级，系统在大多数情况下承担驾驶任务，但特定场景下仍可能需要人类驾驶人接管。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://www.ce.cn/xwzx/gnsz/gdxw/202608/t20260804_3128645.shtml">ce.cn/xwzx/gnsz/gdxw/202608/t20260804_3128645.shtml</a></li>
<li><a href="https://www.autohome.com.cn/news/202608/1316205.html">autohome.com.cn/news/202608/1316205.html</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/695754743">一文看懂规范标准的强制性标准和推荐性标准 - 知乎</a></li>

</ul>
</details>

**标签**: `#autonomous driving`, `#regulation`, `#national standard`, `#China`, `#safety`

---

<a id="item-10"></a>
## [白宫开源 AI 监管急转弯，硅谷立场分裂](https://www.nytimes.com/2026/08/04/technology/ai-washington-regulation-whiplash.html) ⭐️ 8.0/10

特朗普政府一度考虑对中国开源 AI 实施制裁、贸易黑名单甚至禁止美企合作，但在硅谷强烈反对后转向要求模型发布前接受网络安全审查的新框架。白宫于 2026 年 8 月 4 日召集科技公司商议该方案，导火索是中国开源模型 Kimi 部分性能比肩 OpenAI 顶级模型。 这一政策急转弯将影响美国 AI 生态的开放程度，并重塑与中国开源模型的全球竞争格局。它也暴露了美国科技巨头之间的重大分歧：OpenAI 与 Anthropic 以国家安全为由推动限制，而英伟达、Meta 等则力挺开放生态。 新框架拟在模型公开发布前进行网络安全审查，这与早前考虑制裁、贸易黑名单的强硬方案形成鲜明对比。黄仁勋上月首次在 X 平台发帖为开源辩护，并参与组建了拥有逾 230 家成员的安全联盟。

telegram · zaihuapd · 8月4日 15:22

**背景**: Kimi 是月之暗面（Moonshot AI）开发的一系列大语言模型；该公司由杨植麟等清华校友于 2023 年 3 月创立，是中国“AI 六小龙”之一。其最新模型（如 Kimi K3）据报道在部分基准测试中可与美国顶尖模型匹敌，加剧了美国围绕开源 AI 的政策争论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28chatbot%29">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Yang_Zhilin">Yang Zhilin - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI政策`, `#开源AI`, `#中美竞争`, `#监管`, `#人工智能`

---
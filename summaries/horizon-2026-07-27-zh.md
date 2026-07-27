# Horizon 每日速递 - 2026-07-27

> 从 33 条内容中筛选出 15 条重要资讯。

---

1. [vLLM v0.26.0：支持 Inkling 模型、优化 DeepSeek-V4、fp32 lm\_head](#item-1) ⭐️ 9.0/10
2. [月之暗面发布 3T MoE 模型 Kimi-K3](#item-2) ⭐️ 9.0/10
3. [Fastjson2 远程代码执行漏洞曝光，尚无补丁](#item-3) ⭐️ 9.0/10
4. [PGSimCity：PostgreSQL 内部机制的 3D 交互可视化](#item-4) ⭐️ 8.0/10
5. [美国公民因在边境输入紧急擦除密码导致 GrapheneOS 手机被擦除而遭起诉](#item-5) ⭐️ 8.0/10
6. [证明自动化迈向实用：验证的 zstd 解码器](#item-6) ⭐️ 8.0/10
7. [数据导向设计 PDF 引发社区讨论](#item-7) ⭐️ 8.0/10
8. [欧盟提议浏览器级隐私设置消除 Cookie 横幅](#item-8) ⭐️ 8.0/10
9. [令牌中继市场推动 AI 欺诈与滥用](#item-9) ⭐️ 8.0/10
10. [小型 4B 开放权重模型在瑞典医学问答中媲美 o3](#item-10) ⭐️ 8.0/10
11. [Claude 共享链接遭搜索引擎索引泄露用户数据](#item-11) ⭐️ 8.0/10
12. [SpaceX 拒收未来猎鹰 9 号订单，全力押注星舰](#item-12) ⭐️ 8.0/10
13. [华为据报筹建月产 14 万片晶圆的 DRAM 工厂](#item-13) ⭐️ 8.0/10
14. [谷歌称 Gemini 4 为最雄心勃勃的预训练项目](#item-14) ⭐️ 8.0/10
15. [阿里推出千问办公 AI 平台，支持电脑操控](#item-15) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0：支持 Inkling 模型、优化 DeepSeek-V4、fp32 lm\_head](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 9.0/10

vLLM v0.26.0 正式发布，包含来自 212 位贡献者的 411 次提交。新版本新增了对 Inkling 模型家族的全面支持、针对 DeepSeek-V4 的重要性能优化（包括专用路由内核和 fused\_topk\_bias），以及通过新的 head\_dtype 选项实现的 fp32 lm\_head 支持。 此版本将 vLLM 的模型生态扩展至新兴的 Inkling 开放权重系列，并为广泛用于生产的 DeepSeek-V4 带来了显著的吞吐量提升。fp32 lm\_head 功能提高了那些需要在语言模型头部使用更高精度的模型的生成准确性。 Inkling 支持包括分片 CUDA 图、Hopper FA4 相对注意力、MTP=1 推测解码、LoRA 和 NVFP4 量化。DeepSeek-V4 优化包括路由内核带来的 2.94% 端到端 TPOT 提升以及 fused\_topk\_bias 的 1.5–2 倍加速。fp32 lm\_head 已扩展到 LoRA，并提供了 ROCm 快速路径。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理引擎，专为生产环境设计。Inkling 是 Thinking Machines Lab 推出的全新开放权重多模态模型系列，支持文本、图像和音频输入。Flash Attention 4 \(FA4\) 是一种针对 Hopper 架构（如 H100、H200）优化的 GPU 注意力计算内核。NVFP4 是随 NVIDIA Blackwell GPU 引入的 4 位浮点量化格式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/model-card/inkling/">Inkling Model Card - Thinking Machines Lab</a></li>
<li><a href="https://arxiv.org/html/2603.05451v1">FlashAttention-4: Algorithm and Kernel Pipelining Co-Design for Asymmetric Hardware Scaling</a></li>
<li><a href="https://build.nvidia.com/spark/nvfp4-quantization">NVFP4 Quantization | DGX Spark</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#DeepSeek`, `#performance optimization`, `#model serving`

---

<a id="item-2"></a>
## [月之暗面发布 3T MoE 模型 Kimi-K3](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 9.0/10

2026 年 7 月 27 日，月之暗面在 HuggingFace 开源了 Kimi-K3，这是一个 3 万亿参数的混合专家模型，采用原生 mxfp4 精度。这是首个开源 3T 级模型。 Kimi-K3 为开源模型树立了新的规模标杆，可能通过竞争降低推理成本（如 GLM-5.2 曾降价 45%）。同时也给 Meta 等巨头带来压力，迫使其推出更具竞争力的开源模型。 由于采用 mxfp4 格式，该模型托管约需 1.5 TB 显存，接近 8 块 NVIDIA B200 GPU 的极限（优化需 16 块）。这是一个数据中心级模型，不适合个人或小规模部署。

hackernews · nateb2022 · 7月27日 06:18 · [社区讨论](https://news.ycombinator.com/item?id=49065752)

**背景**: 混合专家（MoE）是一种将模型划分为多个专门子网络（专家）的架构，每次输入仅激活部分专家以提高效率。这使得 Kimi-K3 在保持 3T 稠密模型知识容量的同时，将推理成本控制在接近更小模型的水平。月之暗面声称 Kimi-K3 是全球首个开源 3 万亿参数级模型，于 2026 年 7 月 27 日发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://localaihandbook.com/resources/kimi-k3-open-model-local-ai/">Kimi K3: What the World&#x27;s First Open 3 - Trillion - Parameter Model ...</a></li>
<li><a href="https://officeforge.co/blog/kimi-k3-open-weight-frontier">Kimi K 3 : First Open 3 T-Class Model Arrives for AI Teams | OfficeForge</a></li>

</ul>
</details>

**社区讨论**: 社区成员关注模型的托管成本和显存需求，有用户估算需要 1.5 TB 显存，实际使用可能需要 16 块 B200。其他人讨论 Kimi-K3 带来的竞争可能进一步降低 API 价格，并引用 GLM-5.2 在 1.5 个月内降价 45% 的例子。还有人猜测模型何时能完全“去审查”以及可能带来的风险。

**标签**: `#LLM`, `#Model Release`, `#MoE`, `#HuggingFace`, `#AI Infrastructure`

---

<a id="item-3"></a>
## [Fastjson2 远程代码执行漏洞曝光，尚无补丁](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

7 月 27 日，长亭科技披露了 Fastjson2 的一个远程代码执行漏洞，影响 2.0.62 及以前所有版本，攻击者可通过恶意 JSON 数据绕过 AutoType 校验。项目维护者已确认该问题，但目前尚未发布官方补丁。 这一广泛使用的 Java JSON 库中的严重漏洞对无数应用构成重大风险，尤其是那些依赖默认 AutoType 设置的应用。由于尚无修复补丁，用户必须禁用 AutoType 或采取临时措施，这可能会破坏合法功能。 该漏洞类似于之前的 Fastjson 反序列化攻击，虽然完整漏洞细节和利用代码尚未公开，但被认为极易被利用。维护者关闭了相关拉取请求（PR \#7695）并未合入主分支，使得所有已发布版本均无补丁。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson2 是一款流行的 Java JSON 解析库，在阿里巴巴生态及更广泛的领域中被广泛使用。AutoType 是一个允许在反序列化过程中动态绑定类的特性，它一直是远程代码执行漏洞的常见攻击目标。早期 Fastjson 1.x 系列中的类似漏洞（如 CVE-2022-25845、CVE-2026-16723）已得到修复，但 Fastjson2 系列仍然存在漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jfrog.com/blog/cve-2022-25845-analyzing-the-fastjson-auto-type-bypass-rce-vulnerability/">CVE-2022-25845 - Fastjson RCE vulnerability analysis</a></li>
<li><a href="https://medium.com/@knownsec404team/fastjson-deserialization-vulnerability-history-5206714ceed1">Fastjson Deserialization Vulnerability History | by Knownsec 404 team | Medium</a></li>
<li><a href="https://github.com/alibaba/fastjson2/wiki/Security-Advisory:-Remote-Code-Execution-in-fastjson-1.2.68%E2%80%931.2.83">Security Advisory: Remote Code Execution in fastjson 1.2.68–1 ...</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#fastjson2`, `#rce`, `#java`

---

<a id="item-4"></a>
## [PGSimCity：PostgreSQL 内部机制的 3D 交互可视化](https://nikolays.github.io/PGSimCity/) ⭐️ 8.0/10

PGSimCity 是一个可探索的 3D 城市，以动画形式展示 PostgreSQL 的工作原理，包括查询解析、规划、执行以及缓冲池管理等过程。它已在 GitHub 上作为开源工具发布，用户可交互式探索数据库内部机制。 该工具让开发者和学生能够直观理解复杂的数据库内部机制，弥合了抽象架构图与实时系统行为之间的鸿沟。其交互式方法可能启发为 Kubernetes 或云计算等其他系统构建类似的教育可视化工具。 该可视化工具基于 Three.js 构建，直接在浏览器中运行，将 PostgreSQL 组件显示为建筑，进程显示为移动实体。目前包含引导式导览模式，但缺少自定义查询输入功能，这也是用户的常见需求。

hackernews · jonbaer · 7月27日 00:19 · [社区讨论](https://news.ycombinator.com/item?id=49063754)

**背景**: PostgreSQL 是一个关系型数据库，具有复杂的客户端-服务器架构，涉及解析器、规划器、执行器和共享缓冲池。理解这些内部机制对于性能调优和调试至关重要，但传统文档通常依赖静态图表。PGSimCity 以动态 3D 形式展示了这些组件的实际运行情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/NikolayS/PGSimCity">GitHub - NikolayS/PGSimCity: An explorable 3D city that shows how Postgres actually works · GitHub</a></li>
<li><a href="https://blog.algomaster.io/p/postgresql-internal-architecture">How PostgreSQL Works: Internal Architecture Explained</a></li>
<li><a href="https://www.postgresql.org/docs/current/overview.html">PostgreSQL: Documentation: 18: Chapter 51. Overview of ...</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极，用户称赞这种教学数据库内部机制的创新方法。但反馈指出，导览中视觉变化过快可能让人不知所措，许多用户希望有交互模式，可以输入自定义查询并观察逐步处理过程。部分评论者还担心模拟的准确性，因为它使用了“vibe-coding”技术快速构建。

**标签**: `#PostgreSQL`, `#visualization`, `#educational tool`, `#database internals`

---

<a id="item-5"></a>
## [美国公民因在边境输入紧急擦除密码导致 GrapheneOS 手机被擦除而遭起诉](https://www.techspot.com/news/113236-us-prosecutors-charge-atlanta-man-after-grapheneos-phone.html) ⭐️ 8.0/10

一名美国公民在机场被美国边境人员搜查时，因输入紧急擦除密码（duress PIN）导致其 GrapheneOS 手机自行擦除所有数据，随后被起诉。 此案突显了在边境使用紧急擦除密码的法律风险——销毁数据可能导致妨碍司法指控。它强调了隐私增强工具与政府入境口岸搜查权之间的紧张关系。 GrapheneOS 的紧急擦除密码功能会在输入时不可逆地擦除设备及所有已安装的 eSIM。据报道，被告在边境搜查期间使用了该功能，因此面临联邦妨碍司法或销毁证据的指控。

hackernews · eecc · 7月26日 22:21 · [社区讨论](https://news.ycombinator.com/item?id=49063022)

**背景**: GrapheneOS 是一个基于 Android 的开源安全强化移动操作系统，专注于隐私和安全。它提供了紧急擦除密码功能，在胁迫情况下输入该密码会立即擦除设备以保护数据。美国边境巡逻人员拥有广泛权力搜查电子设备，故意销毁证据可能被指控妨碍司法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS</a></li>
<li><a href="https://discuss.grapheneos.org/d/14722-using-duress-password-example">Using duress password example - GrapheneOS Discussion Forum</a></li>
<li><a href="https://www.androidauthority.com/grapheneos-duress-pin-3584795/">I use a duress PIN to protect my data — here’s how it works</a></li>

</ul>
</details>

**社区讨论**: 文章评论中讨论了威胁模型，有人指出边境人员权力巨大且法律中意图很重要。也有人认为用户选择使用紧急擦除功能时必须承担法律后果。建议采用类似 VeraCrypt 的隐藏卷方案，以避免在明面上触发擦除操作。

**标签**: `#GrapheneOS`, `#border search`, `#phone security`, `#privacy`, `#legal`

---

<a id="item-6"></a>
## [证明自动化迈向实用：验证的 zstd 解码器](https://www.imperialviolet.org/2026/07/26/zstd-lean.html) ⭐️ 8.0/10

Adam Langley（ImperialViolet）于 2026 年 7 月 26 日发表了一项实验，用 Lean 语言实现了一个完整的 Zstandard 解码器，并由多个大型语言模型在大约 20 分钟内生成了形式化证明。 这表明证明自动化可以大幅降低形式化验证的成本，可能使其在压缩解码器这类安全关键型软件中变得切实可行。 作者指出，传统形式化验证的成本大约是常规开发的 20 倍，而 LLM 辅助的证明生成显著降低了工作量。该实验使用了支持依赖类型的证明助手 Lean，并且证明覆盖了完整的 zstd 解码器。

hackernews · zdw · 7月26日 20:53 · [社区讨论](https://news.ycombinator.com/item?id=49062291)

**背景**: 形式化验证使用数学证明来确保软件正确性，但历史上对大多数项目来说成本过高。证明自动化旨在通过定理证明器以及最近的大语言模型来降低这一成本。Lean 是一个交互式定理证明器，可以编码复杂属性，其依赖类型系统允许直接在代码中表达和验证不变量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.remio.ai/post/lean-proof-automation-just-crossed-from-research-into-real-software">Lean Proof Automation Just Crossed From Research Into Real...</a></li>
<li><a href="https://elsolitario.org/en/2026/07/26/lean-llm-formal-proofs-zstd/">LLMs Test Code in Lean: How a zstd Decoder Was Verified</a></li>

</ul>
</details>

**社区讨论**: 评论者讨论了权衡：一些人指出了形式化验证的高成本（20 倍），并质疑 LLM 能否应对规模化；另一些人则对依赖类型的维护负担表示担忧。不过，也有乐观的看法认为，将定理证明器嵌入编程语言并结合 LLM，可以减少传统测试的需求。

**标签**: `#formal verification`, `#proof automation`, `#compression`, `#software reliability`, `#dependent types`

---

<a id="item-7"></a>
## [数据导向设计 PDF 引发社区讨论](https://www.gamedevs.org/uploads/introduction-to-data-oriented-design.pdf) ⭐️ 8.0/10

Mike Acton 关于面向性能关键软件的数据导向设计（DoD）的经典 PDF 演示在游戏开发社区重新受到关注。 DoD 是从面向对象编程的重要范式转变，专注于 CPU 缓存效率和数据布局，可显著提升游戏和实时系统的性能。 该 PDF 强调通过分析数据流和使用结构体数组（SoA）而非数组结构体（AoS）来设计算法。Mike Acton 还发布了一个用于数据导向编程的 LLM 技能。

hackernews · tosh · 7月26日 18:11 · [社区讨论](https://news.ycombinator.com/item?id=49060724)

**背景**: 数据导向设计（DoD）是一种以提高 CPU 缓存使用效率为目标的优化方法，常用于视频游戏开发。它优先考虑数据布局和变换而非抽象，与面向对象设计形成对比。主要示例是使用并行数组（SoA）来改善缓存局部性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Data-oriented_design">Data-oriented design</a></li>
<li><a href="https://www.dataorienteddesign.com/dodmain/">Richard Fabian - Data-oriented design</a></li>
<li><a href="https://github.com/dbartolini/data-oriented-design">GitHub - dbartolini/data-oriented-design: A curated list of data oriented design resources. · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论中情绪不一：有人称赞该方法能提升性能，也有人质疑其在需求不断变化的动态项目环境中的实用性。有评论提到 Mike Acton 发布了用于 DoD 的 LLM 技能。

**标签**: `#data-oriented design`, `#software engineering`, `#performance`, `#game development`

---

<a id="item-8"></a>
## [欧盟提议浏览器级隐私设置消除 Cookie 横幅](https://killthecookiebanner.eu/) ⭐️ 8.0/10

欧盟委员会提出了一项解决方案，通过让用户在浏览器中一次性设置隐私偏好，并自动将偏好传达给网站，从而消除 Cookie 横幅。 这可以显著减少用户困扰和同意疲劳，同时简化网站运营商的合规流程。这代表了从逐个网站同意到浏览器强制隐私信号的重大转变。 该提案基于现有标准，如全球隐私控制（GPC），该标准允许用户传达拒绝出售或共享数据的偏好。然而，网站自愿采纳带来了执行层面的问题。

hackernews · rapnie · 7月26日 11:53 · [社区讨论](https://news.ycombinator.com/item?id=49057175)

**背景**: Cookie 横幅在欧盟 ePrivacy 指令和 GDPR 要求网站对非必要 Cookie 获取知情同意后变得普遍。然而，许多横幅设计为引导用户接受跟踪，导致&\#x27;同意疲劳&\#x27;。浏览器级隐私偏好旨在通过启用单一、用户友好的信号来解决这个问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.w3.org/TR/gpc/">Global Privacy Control (GPC)</a></li>
<li><a href="https://globalprivacycontrol.org/">Global Privacy Control — Take Control Of Your Privacy</a></li>
<li><a href="https://secureprivacy.io/blog/sec-gpc-explained">sec-GPC Explained: The Future of Browser ... | Secure Privacy Blog</a></li>

</ul>
</details>

**社区讨论**: 社区成员反应不一：有人认为 Cookie 横幅不应构成知情同意，有人则称赞浏览器级方法绕过了操纵性设计。少数评论者建议，更好的技术默认设置，例如默认隔离第三方 Cookie，也可以解决问题。

**标签**: `#privacy`, `#cookie banners`, `#web standards`, `#EU legislation`, `#browser settings`

---

<a id="item-9"></a>
## [令牌中继市场推动 AI 欺诈与滥用](https://vectoral.com/blog/token-relay-market) ⭐️ 8.0/10

Matt Lenhard 的一项调查揭示了一个蓬勃发展的中继市场，通过盗用的 API 密钥、滥用的云免费额度以及订阅模式漏洞，转售商能够以远低于标准定价（常超过 90%折扣）提供 LLM 令牌。 这破坏了 AI/ML 令牌经济，损害了合法提供商，并创造了不公平的竞争环境，欺诈者借此获得竞争优势。同时也暴露了云服务和 AI 服务在账单和使用限制处理上的系统性漏洞。 转售商通常通过代理 API 运作，汇集来自多种来源的令牌，包括盗用凭证、欺诈性获取的 AWS/Azure 免费额度以及共享订阅账户。这种做法在中国尤为普遍，并针对 Claude 和 Codex 等服务。

hackernews · mlenhard · 7月26日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=49058993)

**背景**: LLM 提供商将令牌作为计量资源出售，通常提供免费层级或额度以吸引客户。然而，当实际市场清算价高于提供商标价时，这些系统便产生了套利机会——类似于活动的票务倒卖。欺诈者利用账单漏洞以近乎零成本获取令牌，然后转售获利。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.explainx.ai/blog/ai-token-black-market-claude-resellers-distillation-2026">AI Token Black Market: Claude Resellers at 70–93% Off (2026 ...</a></li>
<li><a href="https://simonwillison.net/2026/Jul/26/relay-market/">An Inside Look at the Relay Market Powering Token Resellers ...</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，这并非新鲜事——类似的转售市场在广告展示领域早已存在。他们强调了免费云额度（如 AWS）在助长欺诈中的作用，并指出订阅模式从根本上容易受到自动化和滥用。一些评论认为，核心问题在于定价远低于市场清算价，从而不可避免地产生套利。

**标签**: `#token resale`, `#fraud`, `#cloud credits`, `#AI tokens`, `#subscription models`

---

<a id="item-10"></a>
## [小型 4B 开放权重模型在瑞典医学问答中媲美 o3](https://www.reddit.com/r/MachineLearning/comments/1v71wds/openweight_4b_models_approach_o3level_medical/) ⭐️ 8.0/10

开放权重的 4B 参数模型（Gemma4-E4B 和 Qwen3.5-4B）在瑞典医学执照考试数据集 MedQA-SWE 上零样本准确率达到 77%，而启用推理后，Qwen3.5-4B 达到 87%，接近 o3 的 88%。 这表明，经过适当的后训练，小型开放权重模型可以在特定领域任务上与 GPT-4 和 o3 等前沿模型相媲美，凸显了在低资源语言中构建高效、可访问的医疗 AI 系统的潜力。 Qwen3.5-4B 模型尽管使用瑞典语提示，但推理过程使用英语；实验中采用了 S-GRPO 论文中的提前退出干预，以防止推理轨迹陷入无限循环。

reddit · r/MachineLearning · /u/AccomplishedCat4770 · 7月26日 11:58

**背景**: MedQA-SWE 是首个瑞典语开源多项选择临床问答数据集，源自外国医生申请瑞典行医执照的考试。监督微调（SFT）和启用推理等后训练技术可显著提升小型模型性能。S-GRPO 论文提出了一种提前退出方法，用于限制推理轨迹长度并防止过度思考。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aclanthology.org/2024.lrec-main.975/">MedQA-SWE - a Clinical Question &amp; Answer Dataset for Swedish</a></li>
<li><a href="https://arxiv.org/abs/2505.07686">S - GRPO : Early Exit via Reinforcement Learning in Reasoning Models</a></li>
<li><a href="https://huggingface.co/datasets/nicher92/medqa-swe">nicher92/medqa-swe · Datasets at Hugging Face</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#medical AI`, `#language models`, `#open-weight models`, `#Swedish`

---

<a id="item-11"></a>
## [Claude 共享链接遭搜索引擎索引泄露用户数据](https://search.brave.com/search?q=site%3Aclaude.ai%2Fshare&amp;amp;source=android) ⭐️ 8.0/10

Anthropic 的 Claude AI 共享对话链接正被 Google、Bing 和 Brave 等搜索引擎索引，导致 API 密钥、加密货币钱包和个人信息等敏感数据在用户不知情的情况下泄露。 这一隐私漏洞影响了数百万曾共享对话链接的 Claude 用户，可能泄露机密商业数据、财务凭证和个人身份信息，而 Anthropic 尚未推出修复方案。 共享 URL 缺少防止搜索引擎抓取的 &\#x27;noindex&\#x27; 标签，尽管谷歌已屏蔽了被索引的页面，但截至报道时 Brave 和 Bing 仍能在搜索结果中返回这些页面。

telegram · zaihuapd · 7月26日 11:16

**背景**: 搜索引擎使用爬虫来索引可公开访问的网页。当 Claude 用户共享对话链接时，这些 URL 变为公开状态，若未正确限制则可能被搜索引擎发现。大约一年前，ChatGPT 曾出现类似问题并迅速修复。用户可以在 Claude 设置中删除敏感共享对话，以降低风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thecybersecguru.com/news/claude-shared-chats-google-search-privacy/">Claude Shared Chats Indexed by Search Engines Raise Privacy ...</a></li>
<li><a href="https://www.digitalphablet.com/ai/claude-conversation-link-shared-google-indexes-it-exposing-user-chats/">Claude Conversation Link Shared, Google Indexes It, Exposing ...</a></li>
<li><a href="https://cyberpress.org/google-indexed-claude-share-links/">Google Indexed Claude Share Links Containing Sensitive User ...</a></li>

</ul>
</details>

**标签**: `#privacy`, `#security`, `#Claude`, `#AI`, `#data leak`

---

<a id="item-12"></a>
## [SpaceX 拒收未来猎鹰 9 号订单，全力押注星舰](https://www.bloomberg.com/news/articles/2026-07-23/spacex-is-turning-away-falcon-customers-in-major-bet-on-starship) ⭐️ 8.0/10

SpaceX 已开始拒绝卫星运营商在 2028 年后使用猎鹰 9 号火箭的专属发射请求，并不再接受其拼单项目的未来预订。公司还缩减了猎鹰系列部分非重复使用部件的生产，以加速向星舰的过渡。 如果星舰在 2028 年底前无法投入商业运营，这一战略转变可能导致发射能力缺口，影响众多依赖 SpaceX 进入轨道的太空公司。这标志着 SpaceX 全力押注星舰作为未来平台，用于扩展星链以及执行载人登月和火星任务，尽管近期遭遇延误且自 IPO 以来股价下跌了 25%。 SpaceX 可能仍会为美国国防部和 NASA 保留猎鹰 9 号任务，但 2028 年后的商业客户正被拒绝。星舰的首个外部建造商业卫星合同（Superbird-9）以及计划单次发射 Starlab 空间站的任务是其未来载荷的一部分。

telegram · zaihuapd · 7月26日 12:42

**背景**: 猎鹰 9 号是 SpaceX 的可重复使用主力火箭，通过其拼单项目主导了商业发射市场，提供频繁且实惠的轨道进入服务。星舰是一款完全可重复使用的下一代火箭，旨在携带大型载荷和机组人员前往深空，但尚未投入商业运营。SpaceX 为未来订单放弃猎鹰 9 号，反映了一场高风险赌注：星舰将在猎鹰 9 号生产线缩减前投入运营。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.spacex.com/rideshare">Smallsat Rideshare Program - SpaceX</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_Starship_launches">List of Starship launches - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Starship">SpaceX Starship - Wikipedia</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Starship`, `#Falcon 9`, `#Space Industry`, `#Launch Services`

---

<a id="item-13"></a>
## [华为据报筹建月产 14 万片晶圆的 DRAM 工厂](https://www.xda-developers.com/huawei-is-building-its-own-dram-fab-and-it-could-reshape-ram-prices-for-everyone/) ⭐️ 8.0/10

据报，华为正与深圳芯片企业昇维旭合作，在中国建设一座 12 英寸 DRAM 晶圆厂，规划月产能约 14 万片。华为已否认相关说法，但分析人士认为，此举旨在保障其昇腾 AI 芯片的内存供应，并减少对长鑫存储等外部供应商的依赖。 若项目属实，该工厂可能显著改变全球 DRAM 供应格局，有望缓解供应紧张，影响消费者和数据中心的内存价格。这也凸显了华为在制裁下推进半导体自给自足的战略决心，尤其是为其日益增长的 AI 芯片业务提供支撑。 该工厂规划为 12 英寸晶圆厂，这是先进 DRAM 生产的常见规格，但华为已公开否认参与该项目。即使立即开工建设，量产仍需数年时间，因此短期内对消费级 DRAM 价格的影响不大。

telegram · zaihuapd · 7月27日 03:17

**背景**: DRAM（动态随机存取存储器）是一种用于计算设备临时数据存储的半导体存储器。华为的昇腾 AI 芯片（如昇腾 950 系列）在 AI 推理和训练任务中需要高带宽内存。在美国制裁下，华为一直致力于开发关键组件的国内替代方案，建设专用 DRAM 工厂是保障其 AI 和服务器产品供应链的合理举措。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Huawei_Ascend_%28chip%29">Huawei Ascend (chip)</a></li>
<li><a href="https://www.tsmc.com/english/dedicatedFoundry/manufacturing/gigafab">GIGAFAB® Facilities - Taiwan Semiconductor Manufacturing ...</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#DRAM`, `#semiconductor`, `#AI chips`, `#supply chain`

---

<a id="item-14"></a>
## [谷歌称 Gemini 4 为最雄心勃勃的预训练项目](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 8.0/10

谷歌 CEO 桑达尔·皮查伊在 Alphabet 2026 年第二季度财报电话会议上宣布，下一代模型 Gemini 4 已投入训练，并称其为公司迄今为止最具雄心的预训练项目。该模型预计于 2026 年 11 月或 12 月发布。 这一公告表明谷歌继续大力投资前沿 AI，旨在保持对 OpenAI 和 Anthropic 等竞争对手的领先地位。Gemini 4 的发布可能在推理、编码和多模态能力上树立新标杆，影响依赖谷歌 AI 生态的开发者和企业。 皮查伊强调，谷歌将优先将算力分配给前沿 AGI 研发，以确保 Gemini 4 发布时仍处于领先地位。此外，Gemini 3.x Flash 系列将保持几乎每月一次的更新频率，重点提升智能编码等能力。

telegram · zaihuapd · 7月27日 04:06

**背景**: 像 Gemini 这样的大型语言模型通常在大规模数据集上进行预训练，以预测下一个词，然后针对特定任务进行微调。谷歌的 Gemini 系列于 2023 年 12 月推出，包括 Gemini Pro、Flash 和 Flash Lite 等模型，旨在平衡不同性能和成本。预训练是计算最密集的阶段，雄心勃勃的预训练项目意味着在数据、算力和算法创新上的巨大投入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Large_language_model">Large language model - Wikipedia</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3 .6 Flash — Google DeepMind</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#Gemini`, `#Large Language Model`, `#AGI`

---

<a id="item-15"></a>
## [阿里推出千问办公 AI 平台，支持电脑操控](https://qwenwork.cn/) ⭐️ 8.0/10

阿里巴巴上线了“千问办公”Beta 版，这是一个一站式 AI 办公平台，可通过自然语言生成和编辑文档、表格、PPT、网页、代码及多媒体内容，并能操控电脑跨应用执行点击、输入和数据提取等操作。 此次发布标志着阿里巴巴进入竞争激烈的 AI 办公领域，提供了一个集文档创建与桌面自动化于一体的综合工具，有望提升知识工作者和小企业的生产力。同时，它引入了明确的免费与付费定价模式，对微软 Copilot 或 WPS AI 等现有竞品构成挑战。 千问办公支持网页、Windows、macOS（14 以上系统）客户端，并已接入钉钉；付费套餐连续包月活动价 78 元起，每月提供 2000 积分，新用户限时获赠 2000 积分（有效期 90 天）。电脑操控功能可能截取屏幕内容或执行不可撤销操作，默认会在操作前征求用户确认。

telegram · zaihuapd · 7月27日 05:45

**背景**: 电脑操控（Computer Use）是指 AI 智能体模拟人类行为来控制桌面应用程序，例如点击按钮或输入文本。它是阿里巴巴更大的 AgentBay 生态系统的一部分，为开发者提供构建自动化工作流的工具。该功能使 AI 超越文本生成，直接像人类用户一样与软件交互。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ithome.com/0/981/982.htm">阿里千问办公官网现身，鸿蒙电脑 Beta 版同步上线 AppGallery 应用尝...</a></li>
<li><a href="https://help.aliyun.com/zh/agentbay/computeruse">Computer Use-无影 Agent 开发套件 AgentBay ... - 阿里云</a></li>

</ul>
</details>

**标签**: `#AI办公`, `#千问办公`, `#阿里巴巴`, `#自动办公`, `#电脑操控`

---


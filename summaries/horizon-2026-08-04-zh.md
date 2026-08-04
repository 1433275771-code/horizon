# Horizon 每日速递 - 2026-08-04

> 从 33 条内容中筛选出 11 条重要资讯。

---

1. [Qwen 发布 3.8-Max：2.4 万亿参数，首次开源 Max 级模型](#item-1) ⭐️ 9.0/10
2. [LLM 放大现有专长而非取代它](#item-2) ⭐️ 8.0/10
3. [OpenAI 列出十项 AI 驱动的数学与计算机科学进展](#item-3) ⭐️ 8.0/10
4. [开发者工具必须开源，以便 LLM 直接修改源码](#item-4) ⭐️ 8.0/10
5. [ComfyUI 首日支持 MiniMax H3：开放权重、原生音频与 2K 视频](#item-5) ⭐️ 8.0/10
6. [Andy Pavlo 加盟 ClickHouse，创立 ClickHouse Labs](#item-6) ⭐️ 8.0/10
7. [简街 Bonsai 让 OCaml 进入全栈 Web 开发](#item-7) ⭐️ 8.0/10
8. [Kimi K3 架构解析：压缩内存、跨层注意力与潜在专家路由](#item-8) ⭐️ 8.0/10
9. [DNA 设备漏洞威胁 30 年犯罪证据安全](#item-9) ⭐️ 8.0/10
10. [英伟达 170HX 矿卡破解解锁 80GB 显存 价格飙升](#item-10) ⭐️ 8.0/10
11. [苹果就 iCloud 后门要求起诉英国政府](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 发布 3.8-Max：2.4 万亿参数，首次开源 Max 级模型](https://qwen.ai/blog?id=qwen3.8) ⭐️ 9.0/10

通义千问发布了 Qwen 3.8-Max，这是一个总参数 2.4 万亿、活跃参数 950 亿的混合专家模型，并宣布将于下周开源权重——这是 Qwen 首次开源 Max 级别模型。 这标志着开源 AI 的一个重要里程碑：Qwen 最强模型将向社区开放。此举可能会显著推动围绕 MoE 架构和超大规模推理的研究与开发。 该模型基于 Qwen 3.5 架构，在编码、工作、研究和长周期任务方面表现出色。在编码测试中，它自主运行超过 10 天，并在 WWW2025 多模态对话意图识别竞赛中击败 526 支队伍中的 458 支；目前已在 QwenCloud 上提供 API 服务。

telegram · zaihuapd · 8月3日 02:31

**背景**: Qwen 3.8-Max 采用混合专家（MoE）架构，该架构通过每个 token 仅激活部分参数来扩展总参数规模，同时保持计算高效。在 MoE 模型中，总参数代表完整的知识容量，而活跃参数决定每次推理的计算成本。这种方法已成为前沿大语言模型的标准做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://medium.com/@csburakkilic/understanding-moe-architectures-the-difference-between-total-and-active-parameters-ad1d161fccaa">Understanding MoE Architectures: The Difference Between Total and Active Parameters | by Burak Kılıç | Medium</a></li>

</ul>
</details>

**标签**: `#AI`, `#Qwen`, `#open-source`, `#large language model`, `#model release`

---

<a id="item-2"></a>
## [LLM 放大现有专长而非取代它](https://www.seangoedecke.com/llms-reward-expertise/) ⭐️ 8.0/10

在文章《LLM 奖励专长》中，肖恩·格德克认为，大语言模型为领域专家带来不成比例的生产力提升，而对缺乏相关背景知识的新手帮助有限。 这挑战了“AI 将让专长大众化或降低个人专家价值”的流行叙事。它表明，组织和个人应注重培养深厚知识以最大化 LLM 的收益，同时 AI 可能拉大专家与新手之间的生产力差距。 文章的核心论点是：专家能够评估、质疑并引导 LLM 的输出，而新手缺乏这种能力。评论者还指出，在提示词中“表明专家身份”可以显著改变回答质量，并且把 LLM 当作大脑的延伸比当作替代品效果更好。

hackernews · MaxMussio · 8月3日 21:13 · [社区讨论](https://news.ycombinator.com/item?id=49161518)

**背景**: 大语言模型（LLM）是在海量文本数据上训练、能生成类人文本的 AI 系统。人们常假设这类工具最终会取代编程、写作或研究等领域的专家。这篇文章提出反驳，认为判断输出质量的能力——知道什么是正确、相关或优秀的——恰恰是领域专长的关键所在，因此 LLM 对于已具备专长的人相当于“力量倍增器”。

**社区讨论**: 社区反应总体上赞同文章论点，有人用“放大镜”比喻，强调 LLM 反映用户自身的专业水平和用心程度。一些评论者警告说，如果人们理所当然地认为 AI 总是有效，可能会导致一代领域专家流失；还有人指出，即使通用知识很强，亲自动手熟悉代码库仍然至关重要。

**标签**: `#LLMs`, `#expertise`, `#AI`, `#software engineering`, `#productivity`

---

<a id="item-3"></a>
## [OpenAI 列出十项 AI 驱动的数学与计算机科学进展](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 8.0/10

OpenAI 发布了一篇文章，列举了 AI 在数学和理论计算机科学领域推动的十项最新进展，展示了 AI 在证明和发现方面取得的具体成果。 这篇文章凸显了 AI 在数学研究中日益显著的实际影响——LLM 等工具正从新奇事物变成必备工具。它也引发了社区广泛讨论，即 AI 进展是否呈指数曲线增长，以及接下来哪些领域将被改变。 摘要未提供完整列表，但评论者指出其中包含高维球堆积和多色拉姆齐数等问题。这些进展与近期成果相关，例如 OpenAI 对单位距离猜想的证伪以及 Erdős 难题 1196 的解决。

hackernews · milkshakes · 8月3日 16:27 · [社区讨论](https://news.ycombinator.com/item?id=49157930)

**背景**: 自动定理证明（ATP）是利用计算机程序证明数学定理的子领域，其根源可追溯到计算机科学早期。Lean、Coq 等证明助手通过人机协作来开发形式化证明。如今，大型语言模型越来越多地被用来提出猜想和搜索证明，从而促成了长期难题的解决或猜想的证伪。因此，AI 正成为数学家的“半人马”伙伴，将机器搜索与人类洞察结合起来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automated_theorem_proving">Automated theorem proving</a></li>
<li><a href="https://en.wikipedia.org/wiki/Proof_assistant">Proof assistant - Wikipedia</a></li>
<li><a href="https://scitechdaily.com/ai-helps-crack-an-87-year-old-math-conjecture-with-one-tiny-formula/">AI Helps Crack an 87-Year-Old Math Conjecture With One Tiny Formula</a></li>

</ul>
</details>

**社区讨论**: 整体情绪热情而审慎：评论者指出，AI 能处理人类无法完成的繁琐、逐项检验的工作，但仍缺乏提出猜想的直觉。有人认为这是 y=2^x 的指数趋势，并追问哪些领域会抵抗这种变化；也有人指出 OpenAI 列表中具体问题令人惊讶地直观。

**标签**: `#AI`, `#mathematics`, `#theoretical computer science`, `#OpenAI`, `#research`

---

<a id="item-4"></a>
## [开发者工具必须开源，以便 LLM 直接修改源码](https://blog.exe.dev/devtools-must-be-open-source) ⭐️ 8.0/10

exe.dev 博客发表新文章，主张开发者工具必须开源，以便 LLM 能直接修改其源码，从而取消配置系统。这篇文章引发了社区的热烈讨论。 这一观点挑战了工具设计中的一个核心假设，提出让 AI 编程代理通过直接修改源码来取代配置系统。如果被采纳，可能会改变开发者工具的构建、维护和分叉方式，影响整个生态中的开发者和维护者。 文章提议设置一个夜间定时任务，拉取上游变更并将本地 AI 修改 rebase 到上游之上，同时检查软件是否仍能正常工作。社区评论者指出这种做法并不可靠，浪费资源，而且低估了下游分支的维护负担。

hackernews · bryanmikaelian · 8月3日 14:15 · [社区讨论](https://news.ycombinator.com/item?id=49156111)

**背景**: 文章认为，传统配置系统是因为用户无法轻松修改闭源工具行为而存在的折中方案。既然 LLM 能够阅读并修改源代码，让开发者工具开源就能让用户直接编辑程序，从而去掉配置层。这一想法延续了开源运动的理想，但在维护成本与效率方面面临现实疑问。

**社区讨论**: 评论者大体认同开发者工具应当开源，但对文中的激进结论持保留态度。simonw 指出 LLM 让开源初衷变得更为可行，而 kelnos 和 theamk 认为用 AI 重建替换配置既低效又不可靠；作为开发者工具维护者的 lalitmaganti 则警告称这一想法过于理想化，因为工程师只希望工具能正常运作。

**标签**: `#open-source`, `#devtools`, `#LLM`, `#software-engineering`

---

<a id="item-5"></a>
## [ComfyUI 首日支持 MiniMax H3：开放权重、原生音频与 2K 视频](https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui) ⭐️ 8.0/10

ComfyUI 宣布首日支持 MiniMax H3，这是一款新的开放权重多模态视频模型，可接受文本、图像、视频和音频输入，并生成原生立体声视频，最高支持 2K 分辨率和每段 15 秒。 此次发布让创作者能够立即在 ComfyUI 中本地运行下一代开放权重视频模型，并支持原生音频生成和 2K 输出。社区反响热烈，表明它可能对 AI 媒体生成工作流产生重大影响。 根据模型卡，该模型约 40% 的参数（调制权重）可以被剪枝并替换为查找表，从而将总内存从 123.6 GB 降至 42.5 GB，且质量无损。有用户报告称，在 RTX 4070 Ti Super 上生成 10 秒 480p 视频大约需要 10 分钟。

hackernews · vblanco · 8月3日 13:34 · [社区讨论](https://news.ycombinator.com/item?id=49155629)

**背景**: MiniMax H3 是一个开放权重的多模态视频模型系列，支持文字转视频、图像转视频以及帧间转换生成。ComfyUI 是一个流行的基于节点的 AI 图像和视频流水线构建界面。首日支持意味着 MiniMax H3 在发布当天就被原生集成到 ComfyUI 中，用户可以直接加载模型并在本地运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui">MiniMax H3 Day - 0 Support in ComfyUI : Open Weights, Native Audio...</a></li>
<li><a href="https://huggingface.co/Comfy-Org/MiniMax-H3">Comfy-Org/ MiniMax - H 3 · Hugging Face</a></li>
<li><a href="https://hailuoai.video/tools/minimax-h3">MiniMax H 3 Multimodal AI Video Model | Hailuo AI</a></li>

</ul>
</details>

**社区讨论**: 社区评论大体上热情洋溢，但也提出了技术问题。一位用户质疑剪枝 40% 的权重是否真的能做到“质量无损”，以及该做法能否应用于大语言模型。其他用户分享了性能体验，称赞整体质量，但同时提到在非寻常场景下仍存在瑕疵，以及部分片段仍有“AI 平滑”效果。

**标签**: `#ComfyUI`, `#MiniMax H3`, `#AI video generation`, `#Open weights`, `#Text-to-video`

---

<a id="item-6"></a>
## [Andy Pavlo 加盟 ClickHouse，创立 ClickHouse Labs](https://clickhouse.com/blog/andy-pavlo-joins-clickhouse) ⭐️ 8.0/10

著名数据库研究者 Andy Pavlo 以数据库研究副总裁的身份加入 ClickHouse，创立并领导新的研究部门 ClickHouse Labs。这一消息于 2026 年 8 月 3 日公布。 此举将学术数据库研究与工业实践连接起来，表明 ClickHouse 对长期研究的大手笔投入。它可能影响 OLAP 数据库架构的未来走向，并激励更多学术界与产业界的合作。 ClickHouse Labs 将由 Pavlo 领导，他以数据库系统方面的研究以及在卡内基梅隆大学广受欢迎的“数据库系统”课程而闻名。该部门将专注于数据库研究，并计划将学术成果融入 ClickHouse 的开源 OLAP 引擎。

hackernews · nikolay\_sivko · 8月3日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49156011)

**背景**: ClickHouse 是一个开源的列式数据库管理系统，专为大规模数据集的在线分析处理（OLAP）而设计。通过建立专门的研究实验室，ClickHouse 旨在探索新的数据库技术，并在竞争激烈的 OLAP 市场中保持领先地位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://clickhouse.com/blog/andy-pavlo-founding-clickhouse-labs">ClickHouse launches ClickHouse Labs with Andy Pavlo as VP of Database Research | ClickHouse</a></li>
<li><a href="https://www.businesswire.com/news/home/20260803890510/en/ClickHouse-Launches-ClickHouse-Labs-With-Andy-Pavlo-as-VP-of-Database-Research">ClickHouse Launches ClickHouse Labs With Andy Pavlo as VP of Database Research</a></li>
<li><a href="https://en.wikipedia.org/wiki/ClickHouse">ClickHouse - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对此消息表示欢迎，不少人希望 ClickHouse 能在政府资助减少的情况下为学术数据库研究提供资金。还有人猜测快速 OLAP 产品之间的融合趋势，一位评论者称赞 Pavlo 的 CMU 课程给自己带来的启发。

**标签**: `#ClickHouse`, `#database research`, `#Andy Pavlo`, `#OLAP`, `#industry news`

---

<a id="item-7"></a>
## [简街 Bonsai 让 OCaml 进入全栈 Web 开发](https://github.com/janestreet/bonsai) ⭐️ 8.0/10

简街（Jane Street）的 Bonsai 是一个用 OCaml 构建响应式 Web 应用的 UI 库，因能让前后端共享类型而备受社区关注。它目前已在 GitHub 上公开可用。 Bonsai 的重要性在于它让 OCaml 开发者可以用同一种语言和类型编写全栈应用，减少样板代码并提高类型安全。它也是来自大型金融科技公司的生产级 UI 框架，可能影响 OCaml 在 Web 开发领域的采用。 Bonsai 部分灵感来自 Elm，旨在用于在 Incremental 风格的框架（如 Incr\_dom 或 React）中构建可复用 UI 组件。在简街，它已被用来构建许多内部 Web 应用，包括与交易系统交互的工具。

hackernews · KolmogorovComp · 8月3日 08:29 · [社区讨论](https://news.ycombinator.com/item?id=49152842)

**背景**: Bonsai 是简街（Jane Street）开发的 OCaml 库，简街是一家以广泛使用 OCaml 闻名的量化交易公司。简街的许多内部系统以前只有终端界面，而 Bonsai 使现有类型化业务逻辑更容易移植到 Web。该库支持响应式编程，帮助开发者利用 OCaml 强大的类型系统构建动态 Web 应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/janestreet/bonsai">GitHub - janestreet / bonsai : A library for building dynamic webapps...</a></li>
<li><a href="https://en.mycoding.id/bonsai-janestreet-s-ui-library-57684.html">Bonsai : Janestreet &#x27;s Ui Library</a></li>
<li><a href="https://opam.ocaml.org/packages/bonsai/">opam - bonsai</a></li>

</ul>
</details>

**社区讨论**: 社区态度谨慎乐观。一些开发者询问除简街之外的生产环境实际采用情况，另一些人对前后端共享类型感到兴奋。还有讨论将 Bonsai 与 Melange 比较，也有人批评其默认外观不够美观，但性能得到认可。

**标签**: `#OCaml`, `#UI`, `#Jane Street`, `#Frontend`, `#Functional Programming`

---

<a id="item-8"></a>
## [Kimi K3 架构解析：压缩内存、跨层注意力与潜在专家路由](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

SemiAnalysis 发表了对 Kimi K3 的深度分析，重点关注其压缩内存、跨深度注意力、潜在专家路由及推理性能。文章详细阐述了这些架构组件与以往大型语言模型设计的差异。 Kimi K3 将压缩内存、跨层注意力和潜在专家路由相结合，有望显著提升长上下文处理能力和推理效率。这份来自知名来源的分析为 AI 研究者和系统工程师提供了对一款前沿生产模型的罕见技术剖析。 该架构使用了类似 Compressive Transformer 的压缩内存，将较早的激活压缩而非丢弃，从而扩展有效上下文长度。它还实现了跨模型深度的注意力（类似于注意力残差），并采用在低维潜在空间中做出专家选择决策的潜在专家路由。

rss · Semianalysis · 8月3日 19:42

**背景**: 压缩内存由 Compressive Transformer 提出，通过对本将被逐出的旧激活应用学习式压缩操作，扩展了模型可关注的上下文历史，从而能覆盖更长的序列。跨深度注意力（有时称为注意力残差）允许注意力头在读取当前层之外还读取前几层的表示，使信息不仅能沿 token 方向传递，还能沿网络深度方向流动。潜在专家路由（如 Mixture of Latent Experts，MoLE）将路由决策保持在低维潜在空间中，从而提升大规模混合专家模型中专家选择的效率与可扩展性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/1911.05507">COMPRESSIVE TRANSFORMERS FOR LONG-RANGE SEQUENCE MODELLING Jack W. Rae∗∗† ‡</a></li>
<li><a href="https://sebastianraschka.com/llm-architecture-gallery/attention-residuals/">Attention Residuals (AttnRes) | Sebastian Raschka, PhD</a></li>
<li><a href="https://www.emergentmind.com/topics/mixture-of-latent-experts-mole">Mixture of Latent Experts (MoLE)</a></li>

</ul>
</details>

**标签**: `#AI`, `#Model Architecture`, `#Inference`, `#Machine Learning`, `#Kimi K3`

---

<a id="item-9"></a>
## [DNA 设备漏洞威胁 30 年犯罪证据安全](https://www.wsj.com/tech/cybersecurity/security-flaw-placed-30-years-of-dna-evidence-at-risk-of-hacking-1932775a) ⭐️ 8.0/10

研究人员发现，美国多数犯罪实验室使用的 DNA 分析设备存在严重漏洞，可让攻击者不留痕迹地篡改 DNA 扫描数据。设备制造商赛默飞世尔已在 7 月承认该漏洞，并于上周五发布安全公告和加入数字签名的软件更新。 该漏洞可能让攻击者篡改自 1995 年以来的法医 DNA 证据，进而影响刑事调查和定罪案件。这也暴露出美国 200 多家犯罪实验室网络安全防护参差不齐、缺乏统一监管的问题。 研究人员借助 Anthropic 的 Claude 生成的代码，在约 45 分钟内成功篡改 DNA 扫描文件，且修改后的文件未触发常用分析软件的警报。赛默飞世尔表示尚未发现该漏洞被实际利用，并正与美国网络安全和基础设施安全局（CISA）合作。

telegram · zaihuapd · 8月3日 05:15

**背景**: 法医实验室使用 DNA 分析设备（如基因分析仪）从犯罪现场样本中生成 DNA 图谱，并产生由专门软件解读以供比对的數據文件。数字签名基于非对称加密技术，接收方可以验证文件在签名后是否被篡改。该漏洞影响设备处理数据文件的方式，使得在绕过实验室访问控制的情况下篡改成为可能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ip.net.coffee/claude/news/20260803b.html">美犯罪实验室 DNA 设 备 曝漏洞：30...</a></li>
<li><a href="https://aiplus.360.cn/cjwt/5305.html">数字签名：保证数据安全的关键技术 - 360亿方智能</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#DNA analysis`, `#forensics`, `#vulnerability`, `#Thermo Fisher`

---

<a id="item-10"></a>
## [英伟达 170HX 矿卡破解解锁 80GB 显存 价格飙升](https://finance.sina.com.cn/tech/roll/2026-08-03/doc-inikzqsf4659769.shtml) ⭐️ 8.0/10

亚利桑那州立大学的研究人员公开了破解英伟达 CMP 170HX 矿卡的方法，利用 Falcon 安全协处理器的栈溢出漏洞绕过 OTP 熔丝锁定。该破解最高可将显存解锁至 80GB，FP32 算力从 0.39 TFLOPS 暴增至 94 TFLOPS，导致二手价格飙升。 这一破解意义重大，因为它将一款受限严重的矿卡变成廉价 AI 算力选择，冲击英伟达的产品分级策略，影响平价 AI 硬件市场。同时，它也暴露了英伟达 GPU 保护机制的安全弱点。 CMP 170HX 采用与 A100 相同的 GA100 核心，但出厂限制为 4480 个 CUDA 核心和 8GB HBM2e，通过 OTP 熔丝锁定。该漏洞利用 Falcon 协处理器的 DMA 无界溢出劫持权限；社区测试显示，解锁卡可在 Windows 和 Linux 下运行 AI 图像生成及大语言模型推理，但长期稳定性和不同批次的解锁上限仍不确定。

telegram · zaihuapd · 8月3日 11:29

**背景**: CMP 170HX 是英伟达 2021 年发布的加密货币矿卡，基于阉割版 GA100 GPU，配备巨大散热片、无主动散热，原价约 5000 美元。英伟达通过 OTP 熔丝永久锁定计算、显存等硬件功能，GPU 内嵌的 Falcon 协处理器则用于防止错误编程。这些限制此前被认为不可逆转，因此此次破解格外引人注目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techpowerup.com/289310/nvidia-cmp-170hx-mining-card-tested-based-on-ga100-gpu-sku">NVIDIA CMP 170HX Mining Card Tested, Based on GA100 GPU SKU | TechPowerUp</a></li>
<li><a href="https://videocardz.com/newz/nvidia-cmp-170hx-mining-card-with-ga100-gpu-has-a-massive-heatspreader">NVIDIA CMP 170HX mining card with GA100 GPU has a massive heatspreader - VideoCardz.com</a></li>
<li><a href="https://download.nvidia.com/open-gpu-doc/Falcon-Security/1/Falcon-Security.html">NVIDIA Falcon Security</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体热烈，用户在实际系统上验证了解锁效果，并指出 AI 负载性价比大幅提升。也有人担忧长期可靠性、英伟达可能的反制措施，以及不同批次解锁成功率的差异。新闻中未包含官方评论。

**标签**: `#hardware`, `#security`, `#Nvidia`, `#AI computing`, `#exploit`

---

<a id="item-11"></a>
## [苹果就 iCloud 后门要求起诉英国政府](https://www.ft.com/content/2cc9c96a-0e5b-4c33-a95a-3d11072a145c?syn-25a6b1a6=1) ⭐️ 8.0/10

苹果已向英国调查权力法庭提起法律申诉，挑战政府的技术能力通知（TCN），该通知要求苹果开放英国用户加密 iCloud 云备份的访问权限。 此案检验了英国政府强制科技公司削弱加密的权力，对全球隐私、安全以及端到端加密的未来具有重大影响。裁决可能为民主国家政府如何在执法需求与用户隐私之间取得平衡开创先例。 苹果于 2025 年 2 月在英国下架了 iCloud 高级数据保护（端到端加密）功能，此前影响英美用户的旧要求被撤回，取而代之的是仅针对英国用户的新通知。Privacy International 和 Liberty 也对 TCN 提出了申诉，法庭已定于下月举行案件管理听证。

telegram · zaihuapd · 8月3日 15:40

**背景**: 技术能力通知（TCN）是英国《2016 年调查权力法》下的法律工具，允许内政大臣对运营商施加义务，协助拦截通信。调查权力法庭是英国审理公共机构监控投诉的法院。苹果的高级数据保护是 iCloud 的可选功能，采用端到端加密，因此连苹果本身也不掌握解密的密钥。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Technical_capability_notice">Technical capability notice</a></li>
<li><a href="https://en.wikipedia.org/wiki/Investigatory_Powers_Tribunal">Investigatory Powers Tribunal</a></li>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>

</ul>
</details>

**标签**: `#Apple`, `#encryption`, `#privacy`, `#UK law`, `#iCloud`

---


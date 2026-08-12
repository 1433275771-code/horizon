---
layout: default
title: "Horizon Summary: 2026-08-12 (ZH)"
date: 2026-08-12
lang: zh
---

> 从 38 条内容中筛选出 11 条重要资讯。

---

1. [DeepSeek V4 Pro 0813](#item-1) ⭐️ 8.0/10
2. [Tailscale 将数据库损坏追溯至 16 年历史的 SQLite WAL-Reset Bug](#item-2) ⭐️ 8.0/10
3. [Qwen 发布 Qwen3.8-2.4T-A95B，2.4T 参数 MoE 模型](#item-3) ⭐️ 8.0/10
4. [xAI 发布 Grok 4.6，性能比肩 GPT-5.6 并引发讨论](#item-4) ⭐️ 8.0/10
5. [为什么小 JPEG 在 Chrome 中看起来不同：缩放算法的怪癖](#item-5) ⭐️ 8.0/10
6. [uBlock Origin 放弃屏蔽 Facebook 广告](#item-6) ⭐️ 8.0/10
7. [AI 正在淘汰软件工程的中层阶级？](#item-7) ⭐️ 8.0/10
8. [车牌读取器搜索应需要搜查令](#item-8) ⭐️ 8.0/10
9. [数学家探讨 LLM 真正擅长何种数学](#item-9) ⭐️ 8.0/10
10. [Adam 的逐坐标更新破坏矩阵分解的隐式低秩偏置](#item-10) ⭐️ 8.0/10
11. [LTX 发布开源视频模型 LTX-2.5，单张 RTX 5090 可本地运行](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Pro 0813](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) ⭐️ 8.0/10

DeepSeek V4 Pro 0813 发布，引起社区高度关注，实际基准测试显示其以极低成本达到具有竞争力的性能。

hackernews · explosion-s · 8月12日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=49274600)

**标签**: `#AI`, `#DeepSeek`, `#LLM`, `#model-release`, `#benchmarks`

---

<a id="item-2"></a>
## [Tailscale 将数据库损坏追溯至 16 年历史的 SQLite WAL-Reset Bug](https://tailscale.com/blog/sqlite-wal-reset-bug) ⭐️ 8.0/10

Tailscale 将历时六个月的间歇性数据库损坏追溯到 SQLite 中一个已有 16 年历史的 WAL-Reset 数据竞争 Bug，并资助开发了一个开源 VFS shim 来帮助定位该问题，最终在 SQLite 3.51.3 中确认修复。调查过程中还发现了另一个独立的陈旧表达式索引 Bug。 这一事件意义重大，因为 SQLite 是全球部署最广泛的数据库之一，一个隐藏了 16 年的细微损坏 Bug 会对依赖 WAL 模式的开发者和应用产生广泛影响。同时，这也展现了企业资助针对性开源调试工具的价值，使整个 SQLite 生态受益。 WAL-Reset Bug 是一个数据竞争问题，只有在存在多个并发连接时才会触发，尽管 Tailscale 的设计采用单写入进程。该 Bug 是在一个用于记录和拦截文件系统操作的 VFS shim 帮助下定位的，调查过程中还发现了 SQLite 中另一个独立的陈旧表达式索引 Bug。

hackernews · ropbear · 8月12日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49272832)

**背景**: 预写日志（WAL）是数据库系统用于保证原子性和持久性的一种技术，它将更改先追加到日志中，再应用到主数据库文件。SQLite 的 VFS（虚拟文件系统）层抽象了操作系统接口，允许自定义 shim 拦截和调试文件操作。WAL-Reset Bug 涉及 SQLite 的检查点（checkpoint）过程，该过程将条目从临时 WAL 文件移动至主数据库文件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tailscale.com/blog/sqlite-wal-reset-bug">How Tailscale helped find the SQLite WAL-Reset bug</a></li>
<li><a href="https://antithesis.com/blog/2026/wal-reset-bug/">Breaking the WAL | Antithesis</a></li>
<li><a href="https://www.theregister.com/databases/2026/08/12/tailscale-says-deeply-buried-16-year-old-sqlite-bug-caused-last-years-outages/5287004">Tailscale says deeply buried 16-year-old SQLite bug caused ...</a></li>

</ul>
</details>

**社区讨论**: 评论者们称赞了这篇文章，并赞赏 Tailscale 资助开源调试工具以及与 SQLite 签订支持合同的做法。Simon Willison 特别提到 VFS shim 是企业资助特定调试工具的有趣案例，也有读者指出单写入设计起初让这个数据竞争问题显得出人意料。

**标签**: `#SQLite`, `#database`, `#debugging`, `#open-source`, `#Tailscale`

---

<a id="item-3"></a>
## [Qwen 发布 Qwen3.8-2.4T-A95B，2.4T 参数 MoE 模型](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) ⭐️ 8.0/10

Qwen 在 Hugging Face 上发布了 Qwen3.8-2.4T-A95B，这是一个混合专家（MoE）模型，总参数 2.4 万亿，激活参数 950 亿，提供 BF16 和 FP8 两种格式。模型原生上下文长度为 262,144 tokens，可扩展至 1,010,000 tokens。 这是一次重要的开源权重发布，可与 Kimi k3 和 DeepSeek V4 等专有模型抗衡，使研究人员和开发者能够在本地硬件上运行接近前沿水平的模型。它也加剧了开源 LLM 领域的竞争，尤其是在同一晚还有其他多个重要发布的情况下。 BF16 版本大小约为 4.9TB，而 FP8 和 1-bit 量化版本分别可缩减至约 2.4TB 和 397GB。许可证与 Kimi k3 类似，允许免费内部使用或年收入低于 5000 万美元的商业用途，超过该阈值则有限制；开源权重模型缺少 Qwen3.8-Max 的视觉输入、非思考模式和默认 1M 上下文等功能。

hackernews · Philpax · 8月12日 15:01 · [社区讨论](https://news.ycombinator.com/item?id=49273478)

**背景**: 混合专家（MoE）是一种机器学习架构，将模型划分为多个子网络（即“专家”），每个专家专注于输入数据的子集，从而在保持较低计算成本的同时显著提升性能。在 MoE 模型中，总参数指整个模型的大小，激活参数是每个 token 实际使用的子集；两者差距越大，说明推理效率越高。FP8 量化以 8 位浮点格式存储模型权重和激活值，相比 BF16 能大幅降低内存和推理成本，同时准确率损失很小。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/mixture-of-experts">What is mixture of experts? | IBM</a></li>
<li><a href="https://www.spheron.network/blog/fp8-quantization-inference-performance-hardware-explained/">What is FP8 Quantization? AI Inference Performance, Accuracy ...</a></li>
<li><a href="https://www.f22labs.com/blogs/active-vs-total-parameters-whats-the-difference/">Active vs Total Parameters: What’s the Difference?</a></li>

</ul>
</details>

**社区讨论**: 社区讨论指出该模型发布时体积较大，因为只提供了 BF16 和 FP8 格式，比 Kimi k3 更难部署，同时没有 QAT q4 量化版本，可能需要资源充足的机构自行量化。一些评论者对 1-bit 量化后仅 397GB（激活参数 95B）感到惊叹，认为这能将 Opus 4.5 级别性能带到消费级硬件上；另一些人则遗憾开源权重版缺少视觉和 1M 上下文支持。还有用户提到 DeepSeek V4-Pro 的基准分数几乎同期公布，进一步加剧了竞争态势。

**标签**: `#AI`, `#Machine Learning`, `#LLM`, `#Open Source`, `#MoE`

---

<a id="item-4"></a>
## [xAI 发布 Grok 4.6，性能比肩 GPT-5.6 并引发讨论](https://x.ai/news/grok-4-6) ⭐️ 8.0/10

xAI 发布了 Grok 4.6，这是一个前沿模型，在 Artificial Analysis Intelligence Index 上追平了 GPT-5.6 Sol，并在智能体编码和知识工作基准上取得前沿水平。该模型已通过 API 提供，支持可调推理能力和多模态输入。 此次发布加剧了前沿 AI 实验室之间的竞争，为开发者提供了一个比 GPT-5.6 和 Claude 更便宜、更快速的选择。然而，社区对默认系统提示和基准可信度的担忧，可能会影响人们对模型能力衡量和部署方式的信任。 一个值得注意的问题是，xAI 的 API 会自动添加默认系统提示，其中“不要提及这些指南”的说明可能覆盖用户提供的系统指令，导致模型拒绝讨论系统提示。基准声明依赖于包含九项基准的 Artificial Analysis Intelligence Index 综合评分，但一些研究者质疑快速提升是来自蒸馏还是基准作弊。

hackernews · iLuddite · 8月12日 15:32 · [社区讨论](https://news.ycombinator.com/item?id=49274027)

**背景**: 在大型语言模型中，系统提示（system prompt）是在对话开始前设定的一组初始指令，用于塑造模型的行为；API 提供商可能会在用户指令之上注入自己的默认提示。这一隐藏指令层很重要，因为它控制语气、安全规则，以及模型是否会讨论自身的指导原则。Grok 是 xAI 的模型系列，该公司在专用推理基础设施上投入巨大，使 Grok 成为快速且经济的前沿竞争者。新的 API 还支持可调推理努力、文本/图像混合输入和实时网络搜索，这与 Grok 4.6 和 4.7 的发布信息一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.ai/news/grok-4-6">Introducing Grok 4 . 6 | SpaceXAI</a></li>
<li><a href="https://dev.muapi.ai/grok-4">Grok 4 .7 &amp; Grok 4 . 6 API — xAI Multimodal Reasoning + Grok ... | Muapi</a></li>
<li><a href="https://dev.to/simplr_sh/mastering-system-prompts-for-llms-2d1d">Mastering System Prompts for LLMs - DEV Community System Prompts vs. User Prompts: The Missing Manual for ... How to Use System Prompts to Control LLM Behavior System Prompts: Guiding LLMs with Initial Instructions Safeguarding System Prompts for LLMs - arXiv.org</a></li>

</ul>
</details>

**社区讨论**: 评论呈现两极分化：一些人欢迎 Grok 4.6，认为它是价格更低、体验更简洁的真正竞争者；另一些人则质疑基准分数的突然跃升，认为可能涉及蒸馏或基准作弊。一条热度很高的讨论指出，API 的默认系统提示可能覆盖用户的系统指令并阻止讨论系统提示，一些人认为这存在透明度问题。

**标签**: `#AI`, `#Grok`, `#xAI`, `#LLM`, `#benchmark`

---

<a id="item-5"></a>
## [为什么小 JPEG 在 Chrome 中看起来不同：缩放算法的怪癖](https://guillaumetech.github.io/posts/jpg-scaling-chrome/) ⭐️ 8.0/10

这篇文章解释了 Chrome 渲染缩小后的 JPEG 时与其他浏览器不同的原因——它使用的缩放算法是低分辨率线性插值，会使图像变模糊并产生轻微向右偏移。作者建议使用尺寸合适的图像，而不是用 JPEG 来制作图标等小型图形。 不同浏览器的缩放行为会导致 UI 在不同浏览器中显示不一致，影响 Web 开发者、Electron 应用以及所有渲染小图像的场景。了解这些差异有助于开发者选择更合适的图像格式和分辨率，以确保渲染清晰且可预测。 Chrome 在缩小图像时使用低分辨率线性插值，这可能是为速度优化的，并且会轻微向右偏移。CSS 的 image-rendering 属性有时可以控制缩放算法，而 Firefox 正在开发低比例解压缩图像的功能（Bugzilla bug 2033250）以提高质量。

hackernews · gutechh · 8月12日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=49272549)

**背景**: 图像缩放是一种重采样，将高分辨率图像缩小到较小的尺寸需要使用合适的抗混叠滤波器以避免伪影。不同浏览器实现方式不同：Chrome 使用快速但模糊的线性插值，而 Firefox 结果更锐利但略带振铃伪影。JPEG 针对照片设计，会产生压缩伪影，因此不适合用于图标；通常更推荐使用支持 alpha 透明度的 PNG。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://entropymine.com/resamplescope/notes/browsers/">How web browsers resize images - entropymine.com</a></li>
<li><a href="https://stackoverflow.com/questions/37906602/blurry-downscaled-images-in-chrome">html - Blurry downscaled images in Chrome - Stack Overflow</a></li>
<li><a href="https://gehrcke.de/2014/11/css-crispy-downscaled-images/">CSS: Crispy downscaled images – Jan-Philip Gehrcke, PhD</a></li>

</ul>
</details>

**社区讨论**: 评论者证实该问题同样影响 PNG，并在 Chrome 升级到 Electron 版本时导致图标失真，迫使团队暂停发布。其他人同意使用尺寸合适的图像比格式更重要，并提到 Firefox 的低比例解压缩 bug，还指出 Firefox 和 Chrome 使用不同的缩放算法，在模糊和振铃之间有权衡。一位评论者补充说，CSS 的 image-rendering 属性有时可以控制算法，尤其是在高 DPI 显示器上。

**标签**: `#JPEG`, `#Chrome`, `#browser rendering`, `#image scaling`, `#web development`

---

<a id="item-6"></a>
## [uBlock Origin 放弃屏蔽 Facebook 广告](https://digitalescapetools.com/2026/08/ublock-origin-stops-chasing-facebook-ads.html) ⭐️ 8.0/10

uBlock Origin 已宣布将停止过滤 Facebook 上的广告，原因是该平台的反对抗手段日益复杂，使屏蔽变得不切实际。这一消息通过 Reddit 帖子发布并由 Neowin 报道，标志着该扩展长期致力于让 Facebook 无广告的努力告一段落。 这是广告拦截军备竞赛中的一次显著失利，因为 Facebook 是网络上最大的广告平台之一，而 uBlock Origin 是使用最广泛的广告拦截器之一。此举可能会影响其他拦截器，并推动用户转向包括基于 AI 的视觉广告检测在内的替代策略，同时也引发了对传统基于过滤的拦截方式局限性的质疑。 Facebook 一直在通过将“赞助商”一词拆分为逐字符 span 并使用 DOM 操作来混淆其广告标记，从而向广告拦截过滤器隐藏该标签。这使得可靠地检测和屏蔽广告的资源成本远超其价值，导致 uBlock Origin 团队放弃了针对 Facebook 的专用过滤器。

hackernews · Markoff · 8月12日 11:28 · [社区讨论](https://news.ycombinator.com/item?id=49270726)

**背景**: uBlock Origin 是一款免费的开源浏览器扩展，使用过滤列表来拦截广告、跟踪器和恶意内容，并以对 CPU 和内存占用低而著称。广告拦截器通常依赖静态规则来识别广告元素，但像 Facebook 这样的平台可以动态改变其 HTML 和 CSS 来规避这些规则，从而形成一场持续的军备竞赛。uBlock Origin 的官方描述称其为“广谱内容拦截器”而非单纯的广告拦截器，但在本次决定之前，Facebook 广告一直是其长期目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.dylanpaulus.com/posts/how-fb-avoids-adblockers">How Facebook Avoids Ad Blockers | Dylan Paulus</a></li>
<li><a href="https://ublockorigin.com/">uBlock Origin - Free, open-source ad blocker extension</a></li>
<li><a href="https://en.wikipedia.org/wiki/Ad_blocking">Ad blocking - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Reddit 帖子下的评论大多持支持态度，用户们认为继续屏蔽 Facebook 广告得不偿失。有人预测未来会出现一种通过视觉识别广告的计算机视觉模型，也有人质疑 Facebook 这种捉迷藏游戏的意义，指出安装广告拦截器的用户本来就不太可能点击广告。

**标签**: `#ad-blocking`, `#uBlock Origin`, `#Facebook`, `#privacy`, `#web`

---

<a id="item-7"></a>
## [AI 正在淘汰软件工程的中层阶级？](https://blog.florianherrengt.com/ai-removing-middle-class-software-engineering.html) ⭐️ 8.0/10

这篇博文认为，AI 编程工具正在淘汰中级软件工程岗位，让资深工程师直接生成代码，绕过了传统的交接流程。评论者争论这到底是放大了糟糕的工程实践，还是仅仅自动化了“StackOverflow 工程师”这一角色。 这很重要，因为它可能重塑软件工程领域的职业发展路径，影响整个行业的就业安全、技能培养和代码质量。它也引发了紧迫的问题：随着 AI 工具的普及，初级工程师将如何学习，以及哪些角色仍然具有价值。 博文强调，“糟糕的工程师”现在可以借助 AI 将糟糕的工程实践放大十倍并影响整个组织，一位评论者警告不要把批判性思维外包给 LLM。另一位评论者指出，资深工程师不再需要将思考提炼成 Jira 工单交给中级实现者，使得这种交接变得过时。

hackernews · florianherrengt · 8月12日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=49271994)

**背景**: 在传统企业软件开发中，资深工程师设计解决方案并将其拆分为工单，然后由中级工程师编写代码并在网上搜索答案来实现。现在 AI 助手可以直接完成大部分实现工作，这可能会压缩工程层级并缩减中间层。这样只剩下初级岗位用于学习、高级岗位用于监督，而中级岗位可能变得多余。

**社区讨论**: 评论者大体上认同这一论点，有人指出，对技术失去兴趣的老资历工程师现在可以大规模地交付糟糕的代码。另一个人反驳说，更好的工具可能只是拉平了竞争环境，就业上不会有净变化；还有人强烈建议永远不要将批判性思维委托给 AI 模型。

**标签**: `#AI`, `#software engineering`, `#future of work`, `#LLM`, `#career impact`

---

<a id="item-8"></a>
## [车牌读取器搜索应需要搜查令](https://andrewpwheeler.com/2026/08/12/license-plate-reader-searches-should-require-a-warrant/) ⭐️ 8.0/10

在 2026 年 8 月 12 日的一篇博文中，犯罪学家 Andrew Wheeler 主张，警方在未获搜查令的情况下使用自动车牌识别器构成大规模监控，应需司法批准。这篇文章在 Hacker News 上引发了关于隐私和警察问责制的大规模讨论。 自动车牌识别器在美国广泛部署，可记录每辆经过摄像头的车辆的时间、日期和位置，从而形成可搜索的个人行踪数据库。关于是否要求搜查令的辩论，对隐私权以及警方在公共场所进行监控的边界具有重大影响。 文章认为，车牌识别器数据的总量（不仅仅是黑名单匹配）使得无证搜索构成不合理的侵犯，而是否访问历史位置数据的决定应由中立法官做出。文章还指出，警察部门通常会保留车牌识别器记录数月或数年，这加剧了监控风险。

hackernews · apwheele · 8月12日 14:43 · [社区讨论](https://news.ycombinator.com/item?id=49273165)

**背景**: 自动车牌识别器利用摄像头和光学字符识别技术，在车辆经过时捕捉车牌号码以及时间和位置元数据。该系统可用于从收费到犯罪调查等多种用途，既可安装在固定杆上，也可安装在巡逻车上。由于它们记录每块车牌而不只是黑名单上的车牌，因此会生成庞大的车辆历史行踪数据库。法律争论的焦点在于，未经授权的长期追踪是否违反了合理的隐私预期。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sls.eff.org/technologies/automated-license-plate-readers-alprs">Automated License Plate Readers</a></li>
<li><a href="https://www.flocksafety.com/blog/how-an-automatic-license-plate-recognition-system-works">How an Automatic License Plate Recognition System Works</a></li>

</ul>
</details>

**社区讨论**: 评论者大多同意搜查令要求，但认为这还不够。有人指出，车牌识别器摄像头是通用、可重新编程的设备，可能被用于更广泛的监控；也有人认为，大规模数据收集本身应被禁止，而不仅仅是被监管。少数人提出技术解决方案，例如使用数字签名的轮换车牌号，使没有密钥就无法追踪。

**标签**: `#privacy`, `#surveillance`, `#law`, `#policy`, `#technology`

---

<a id="item-9"></a>
## [数学家探讨 LLM 真正擅长何种数学](https://gowers.wordpress.com/2026/08/12/what-sort-of-maths-are-llms-good-at/) ⭐️ 8.0/10

在一篇新博文中，著名数学家 Timothy Gowers 分析了大型语言模型擅长哪些类型的数学，指出测试时扩展和采样技术虽能让 LLM 发现例子与反例，但很少能产生真正具有人类风格的证明。他提出了一个关键的未来检验标准：AI 能否生成新颖、令人意外、且事后看来优美自然的证明。 由于 Gowers 是世界上最杰出的数学家之一，他的评估有助于校准人们对 AI 在数学研究中作用的预期。这一讨论也影响着研究者如何评价测试时扩展技术的价值，以及什么才算真正的 AI 数学成就。 该文强调朴素采样是早期 AI 数学成功的原始引擎，并援引 DeepMind 的 AlphaCode：它在 2022 年生成数百万个候选程序，超过了普通人类程序员。Gowers 提出，判断 AI 达到人类水平数学能力的关键标志，是它能否给出难以偶然发现、但事后看来优美自然的证明。

hackernews · ColinWright · 8月12日 10:04 · [社区讨论](https://news.ycombinator.com/item?id=49270022)

**背景**: 测试时扩展指在推理阶段投入更多算力来提升推理能力，例如让模型多次采样答案或更长时间地“思考”。采样通过 temperature、top-k、top-p、min-p 等参数控制生成文本的随机性与创造性；生成大量候选再从中筛选，正是 LLM 擅长某些数学任务的原因。Gowers 的这篇博文属于一场更广泛的讨论：计算机生成的证明是否应与人类证明享有同等地位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://createbytes.com/insights/test-time-scaling-vs-fine-tuning-llm">Test - Time Scaling vs Fine-Tuning: Master LLM Optimization 2026</a></li>
<li><a href="https://link.springer.com/article/10.1007/s11245-025-10164-w">How to Recognize Artificial Mathematical Intelligence in Theorem Proving | Topoi | Springer Nature Link</a></li>
<li><a href="https://www.thoughtworks.com/en-us/insights/blog/generative-ai/Min-p-sampling-for-LLMs">Min-p sampling for LLMs | Thoughtworks United States</a></li>

</ul>
</details>

**社区讨论**: 评论者大体上赞同 Gowers，并明确把他的观察与测试时扩展联系起来；有人指出 AlphaCode 的早期成功正源于大规模采样，远早于 ChatGPT。还有人补充了 AI 数学成就清单等参考资料，并提出开放问题——例如，编码智能体在并发代码上的困难是否会延续到时序逻辑领域。

**标签**: `#LLMs`, `#mathematics`, `#test-time scaling`, `#AI research`, `#proofs`

---

<a id="item-10"></a>
## [Adam 的逐坐标更新破坏矩阵分解的隐式低秩偏置](https://www.reddit.com/r/MachineLearning/comments/1vmjb3p/the_loss_does_not_see_the_basis_but_adam_does_r/) ⭐️ 8.0/10

一项由/u/EtherealGlyph 开展的新研究在匹配训练损失的欠定矩阵感知任务上测试了九种更新规则，发现 Adam、RMSProp、Lion、signum 和 Adafactor 会丢失 GD、共享标量 Adam、Muon 和 Shampoo 所保持的隐式低秩偏置。一个将 Adam 分母从逐坐标插值到共享标量的单参数族能单调地恢复该偏置，表明罪魁祸首是各向异性而非自适应性。 这为在低秩矩阵分解和深度线性网络中，为什么某些优化器比其他优化器泛化更好提供了机制层面的解释。这意味着优化器的选择会悄然改变隐式正则化，从而影响实际深度学习工作流中的模型质量。 理论部分仅涵盖无记忆更新规则，动量相关结论是实验性的。其他发现包括：Muon 在真正低秩目标上是精确的，但随着谱尾能量增加退化最快，并在约 4%谱尾能量处让位于 GD；作者发现对其自己优化器使用全局范数裁剪可将恢复误差从 0.347 降至 0.220。文中的注意事项是，高光谱数据上 43-44%的留出误差降低使用的是仅基于训练的学习率规则，该规则恰好让 Adam 在其自身网格上取得最差的学习率。

reddit · r/MachineLearning · /u/EtherealGlyph · 8月12日 16:39

**背景**: 该研究关注形如 W = UV^T 的因子化模型，其损失函数在因子做正交旋转\(U,V\) → \(UQ,VQ\)时保持不变。梯度下降尊重这种不变性，而 Adam 的逐坐标二阶矩缩放不尊重，导致其更新依赖于所选的基。隐式低秩偏置是指基于梯度的训练即使没有显式正则化，也倾向于收敛到低秩解，这在矩阵分解和深度线性网络中非常重要。Muon 和 Shampoo 等优化器采用结构化的预条件处理以保持旋转行为，研究将其与保持该偏置联系起来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1802.09568">[1802.09568] Shampoo: Preconditioned Stochastic Tensor Optimization</a></li>
<li><a href="https://github.com/KellerJordan/Muon">GitHub - KellerJordan/Muon: Muon is an optimizer for hidden ...</a></li>
<li><a href="https://cbmm.mit.edu/sites/default/files/publications/Implicit+Rank+Regularization.pdf">Noise and Implicit Low - Rank Bias</a></li>

</ul>
</details>

**标签**: `#optimization`, `#Adam`, `#matrix factorization`, `#low-rank`, `#deep learning`

---

<a id="item-11"></a>
## [LTX 发布开源视频模型 LTX-2.5，单张 RTX 5090 可本地运行](https://ltx.io/model/ltx-2-5) ⭐️ 8.0/10

LTX 发布了开源视频生成基础模型 LTX-2.5，权重、训练代码与推理管线全部开放。该模型可在单张 RTX 5090 上本地运行，年收入低于 1000 万美元的公司可免费商用。 此次发布大幅降低了高质量 AI 视频生成的门槛，让没有大型 GPU 集群的研究者和开发者也能使用。全开源的方式（包括训练代码）有望加速视频生成生态系统的创新与定制化。 LTX-2.5 支持文生视频与图生视频，改进了多镜头连贯性与提示词遵循能力。它采用新的扩散视频解码器和 Gemma 4 12B 文本编码器；在 98 个提示词的文生视频瑕疵评测中，LTX-2.5 Pro 在十款模型中排名第一。

telegram · zaihuapd · 8月12日 02:15

**背景**: LTX-2.5 是开源的视频生成基础模型，而视频生成领域通常使用扩散模型从文本或图像生成或编辑视频。由于权重和训练代码全部开放，用户可以在自有硬件上进行微调和运行。采用 Gemma 4 12B 文本编码器，体现了将强大的语言模型集成到多模态生成流程中、以提升语义理解的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ltx.io/model/ltx-2-5">LTX - 2 . 5 : LTX&#x27;s Latest AI Open-Source Foundation Model | LTX</a></li>
<li><a href="https://huggingface.co/google/gemma-4-12B">google/gemma-4-12B · Hugging Face</a></li>
<li><a href="https://lilianweng.github.io/posts/2024-04-12-diffusion-video/">Diffusion Models for Video Generation | Lil&#x27;Log</a></li>

</ul>
</details>

**标签**: `#video generation`, `#open-source`, `#AI`, `#diffusion model`, `#local inference`

---
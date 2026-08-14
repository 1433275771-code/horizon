# Horizon 每日速递 - 2026-08-14

> 从 35 条内容中筛选出 11 条重要资讯。

---

1. [GLM-5.3 发布引发关于涌现网络能力的辩论](#item-1) ⭐️ 9.0/10
2. [PostgreSQL 修复 to\_char 堆溢出高危漏洞，可执行任意代码](#item-2) ⭐️ 9.0/10
3. [Qwen 3.8 27B：新的本地推理模型广受好评](#item-3) ⭐️ 8.0/10
4. [为什么 Opus 5 用起来反而更别扭](#item-4) ⭐️ 8.0/10
5. [Firefox 成为最后一个支持 uBlock Origin 的主流浏览器](#item-5) ⭐️ 8.0/10
6. [无训练：将《毁灭战士》渲染器编译成 210 亿参数 Transformer](#item-6) ⭐️ 8.0/10
7. [Vivodyne 推出 AI 人体组织实验室，年测 300 万样本或终结动物测试](#item-7) ⭐️ 8.0/10
8. [小红书开源 dots3-note：280B MoE 仅激活 16B 参数](#item-8) ⭐️ 8.0/10
9. [美国法官下令谷歌一周内去除第三方应用商店安装障碍](#item-9) ⭐️ 8.0/10
10. [库克 9 月 1 日卸任苹果 CEO，约翰·特努斯接任](#item-10) ⭐️ 8.0/10
11. [苹果联手阿里自研中国专属 AI 模型，或成首个获批外企](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GLM-5.3 发布引发关于涌现网络能力的辩论](https://z.ai/blog/glm-5.3) ⭐️ 9.0/10

Z.ai 发布了最新旗舰模型 GLM-5.3，该模型基于 GLM-5.2 的基础模型并通过后训练改进而来，主打编程与长时程任务能力。官方称其在长时程任务能力上有大幅提升，并出现了发现零日漏洞、改编内核利用程序等涌现性网络能力。 此次发布意义重大，因为它将前沿编程模型推向自主安全研究领域，引发关于安全披露和双重用途风险的紧迫问题。同时，它也加剧了 AI 实验室之间的竞争，社区已开始将其与 Sol、Fable 等前沿模型进行比较。 GLM-5.3 与 GLM-5.2 使用相同的基础模型，所有能力提升都来自后训练，并支持 100 万 token 的上下文窗口。公司还运营着一个协调漏洞披露页面（cvd.z.ai），似乎在大规模扫描开源软件，其中许多高危/严重 CVE 仍处于保密期。

hackernews · pella · 8月14日 05:19 · [社区讨论](https://news.ycombinator.com/item?id=49294997)

**背景**: GLM（通用语言模型）是 Z.ai 开发的一系列开放权重大语言模型，首个模型于 2021 年发布，2023 年以 ChatGLM 聊天机器人形式推出。“涌现能力”是指大语言模型规模扩大时意外出现的能力，如高级推理或工具使用；自 2022 年一篇关键论文以来，这一话题一直存在争议。在此次事件中，开发者观察到 GLM-5.3 能够执行红队场景、内核利用改编等安全研究任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GLM_%28AI%29">GLM (AI) - Wikipedia</a></li>
<li><a href="https://openlm.ai/glm-5.2/">GLM-5.3 - openlm.ai</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.3">GLM-5.3 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体热烈但存在分歧：有用户报告称该模型在实际红队测试中表现出色并立即升级了订阅套餐，也有人对大规模漏洞扫描和负责任的披露方式提出伦理质疑。还有评论认为 GLM-5.3 仍略逊于 Sol、Fable 等顶级模型，并担心开放权重发布可能同时加速防御性与攻击性用途。

**标签**: `#AI`, `#LLM`, `#cybersecurity`, `#coding`, `#GLM`

---

<a id="item-2"></a>
## [PostgreSQL 修复 to\_char 堆溢出高危漏洞，可执行任意代码](https://www.postgresql.org/support/security/CVE-2026-14669/) ⭐️ 9.0/10

PostgreSQL 披露了高危漏洞 CVE-2026-14669，该漏洞存在于 to\_char\(timestamptz\) 函数处理超长 POSIX 时区缩写时，可导致堆缓冲区溢出。本地低权限数据库用户可利用该漏洞以 PostgreSQL 服务进程的操作系统权限执行任意代码。 该漏洞 CVSS 评分为 8.8，影响所有受支持的 PostgreSQL 分支（14 至 18），因此大多数生产环境都需要立即修补。成功利用可在数据库服务器上下文中执行代码，进而可能导致服务器被完全攻陷。 受影响版本包括 PostgreSQL 18.5、17.11、16.15、15.19 和 14.24 之前的版本。由于 18.5 因回归问题被撤回，18 系列用户应直接升级到 18.6；此次小版本更新无需转储数据库或运行 pg\_upgrade，只需替换程序文件并重启服务。

telegram · zaihuapd · 8月14日 14:35

**背景**: to\_char 是 PostgreSQL 的数据类型格式化函数，用于将时间戳、区间和数字转换为格式化字符串（PostgreSQL 文档）。堆缓冲区溢出是指程序写入超过堆内存分配边界的区域，攻击者可利用它执行任意代码或使系统崩溃（Automox）。PostgreSQL 的小版本更新通常只需安装新二进制文件并重启即可安全应用；而大版本升级才会使用 pg\_upgrade。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.postgresql.org/docs/current/functions-formatting.html">PostgreSQL: Documentation: 18: 9.8. Data Type Formatting Functions</a></li>
<li><a href="https://www.automox.com/blog/vulnerability-definition-heap-buffer">What is Heap Buffer Overflow Vulnerability? - Automox</a></li>
<li><a href="https://www.postgresql.org/docs/current/pgupgrade.html">PostgreSQL : Documentation: 18: pg _ upgrade</a></li>

</ul>
</details>

**标签**: `#security`, `#postgresql`, `#CVE`, `#vulnerability`, `#database`

---

<a id="item-3"></a>
## [Qwen 3.8 27B：新的本地推理模型广受好评](https://huggingface.co/Qwen/Qwen3.8-27B-FP8) ⭐️ 8.0/10

阿里巴巴 Qwen 团队在 Hugging Face 上发布了 FP8 量化版本地推理模型 Qwen 3.8 27B。社区用户报告其基准测试表现强劲、实际使用质量出色，使其成为近期最受关注的本地 LLM 发布之一。 该发布表明高质量推理模型可以在消费级笔记本上运行，降低了私有、离线 AI 的使用门槛。也说明开源权重模型继续推动本地模型领域的前沿发展。 该 27B 参数模型采用 FP8 量化来降低显存占用，可通过 Ollama 等工具运行，并支持多 token 预测（MTP）。不过用户也指出一些不完善之处，包括 Jinja 模板问题需要社区修复，以及显存效率低于同类模型。

hackernews · erdaltoprak · 8月14日 15:00 · [社区讨论](https://news.ycombinator.com/item?id=49299605)

**背景**: Qwen 是阿里云开发的开源权重大语言模型系列，最初于 2023 年 8 月发布，并在 Hugging Face 上提供。推理模型会在回答前生成逐步的思维链（chain-of-thought），从而提升复杂问题解决能力，但也会消耗更多算力。FP8 量化可减小模型体积和内存占用，使 27B 参数规模这类大模型更容易在本地运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/Qwen_language_model">Qwen (language model)</a></li>
<li><a href="https://huggingface.co/Qwen">Org profile for Qwen on Hugging Face, the AI community building the...</a></li>

</ul>
</details>

**社区讨论**: 评论总体积极，用户称赞该模型的推理能力和实际输出质量；simonw 称这是他见过能跑在笔记本上的模型中画得最好的鹈鹕。主要担忧集中在显存效率、在 Ollama 中无法完全关闭思考模式，以及推理痕迹中独特的笔记式风格——有人怀疑这种风格会影响多 token 预测的效果。社区还分享了针对 Jinja 模板问题的修复方案。

**标签**: `#LLM`, `#Qwen`, `#local AI`, `#model release`, `#reasoning`

---

<a id="item-4"></a>
## [为什么 Opus 5 用起来反而更别扭](https://mun-logadan.github.io/why-does-opus-5-feel-worse/) ⭐️ 8.0/10

一篇新博文指出，Anthropic 的 Claude Opus 5 虽然能力更强，但写作体验却更差，作者将其归因于以智能体为中心的 post-training（后训练）——优化目标是其他 AI 智能体而非人类读者。该文章在 Hacker News 上引发热议，获得 724 分和 659 条评论。 这标志着一个潜在转折点：前沿模型的后训练不再主要围绕人类交互来优化，即使用户能力在提升，日常使用体验也可能因此退化。随着 AI 智能体成为重要受众，产品设计者和开发者需要在智能体效率与人类可读性之间做出权衡。 批评者认为 Opus 5 的文字过于省略、抽象，充满『智能体腔调』；而 Anthropic 官方将 Opus 5 定位为面向长期多步骤任务的 agentic 编程模型。该模型最大的提升在于深度推理、长时程智能体任务和测试时计算扩展，这或许解释了其文风变化的原因。

hackernews · numeri · 8月14日 10:12 · [社区讨论](https://news.ycombinator.com/item?id=49296740)

**背景**: 后训练（post-training），也称为对齐（alignment），是将基础大语言模型变成有用助手的关键阶段，目的是教会模型以人类喜欢的方式进行对话。相比之下，以智能体为中心的后训练（agentic post-training）则优化模型自主完成多步骤任务的能力，过程中可能使用工具或将任务交给子智能体，因此简洁、面向机器的表达方式可能优先于面向人类的自然措辞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/claude-opus-5">Introducing Claude Opus 5 \ Anthropic</a></li>
<li><a href="https://pytorch.org/blog/a-primer-on-llm-post-training/">A Primer on LLM Post-Training – PyTorch</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/whats-new-opus-5">What&#x27;s new in Claude Opus 5 - Claude Platform Docs</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为 Opus 5 能力更强，但交互体验更差，抱怨它过于啰嗦、表达省略、在缺乏严格指令时会跑题。有用户表示在重度项目中感觉 OpenAI 的 Sol 模型『好用得太多』；还有人猜测后训练的目标受众已经不再是人类。

**标签**: `#AI`, `#LLM`, `#UX`, `#Anthropic`, `#agents`

---

<a id="item-5"></a>
## [Firefox 成为最后一个支持 uBlock Origin 的主流浏览器](https://www.pcworld.com/article/3212428/firefox-is-now-the-last-major-browser-that-still-supports-ublock-origin.html) ⭐️ 8.0/10

原版 uBlock Origin 扩展在 Chromium 内核浏览器迁移到 Manifest V3 后正在失去支持，Firefox 成为唯一仍能正常运行它的主流浏览器。Mozilla 继续允许旧版 Manifest V2 扩展以及 uBlock Origin 所依赖的 webRequest API。 这标志着浏览器生态的一次重大转变：Firefox 与 Chrome、Edge、Brave 等 Chromium 内核浏览器在广告拦截能力上出现了明显分化。依赖强力内容过滤功能以保护隐私和提升性能的用户，将不得不在改用 Firefox 或接受功能较弱、基于 MV3 的拦截器之间做出选择。 uBlock Origin 依赖 webRequest API 来实时拦截网络请求，而 Manifest V3 限制该 API，改用规则集有限的 declarativeNetRequest。兼容 MV3 的替代品 uBlock Origin Lite 使用这些受限 API，过滤能力较弱；此外，Firefox 还会在每次更新时人工审核 uBlock Origin 的代码。

hackernews · DemiGuru · 8月14日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49303202)

**背景**: 浏览器扩展是可以改变浏览器行为的微型程序，像 uBlock Origin 这样的广告拦截器通过在广告加载前拦截请求来工作。Google 推出 Manifest V3 作为 Chrome 扩展的新框架，声称能改善隐私、安全和性能，但它限制了扩展拦截内容的方式。Firefox 则保留了旧版 Manifest V2 的支持，使功能更强、更完整的原版 uBlock Origin 可以继续使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">UBlock Origin</a></li>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3">Extensions / Manifest V 3 | Chrome for Developers</a></li>
<li><a href="https://www.eff.org/deeplinks/2021/12/googles-manifest-v3-still-hurts-privacy-security-innovation">Google’s Manifest V 3 Still Hurts Privacy, Security, and Innovation</a></li>

</ul>
</details>

**社区讨论**: 评论者大多称赞 Firefox，并批评 Google 处理 Manifest V3 的方式，有人直言“支持 Firefox，去他的 Chrome”。一位用户指出 Firefox 会在更新时审核 uBlock Origin 的代码，另一位则说技术上仍可在 Chrome 中加载未打包的扩展，只是非常麻烦。还有一位开发者表示，正是因为 MV3 他们关闭了自己的 Chrome 扩展，因为现在只有 Firefox 还能屏蔽 Google 搜索广告。

**标签**: `#web-browsers`, `#ad-blocking`, `#privacy`, `#manifest-v3`, `#firefox`

---

<a id="item-6"></a>
## [无训练：将《毁灭战士》渲染器编译成 210 亿参数 Transformer](https://www.reddit.com/r/MachineLearning/comments/1voazhm/i_compiled_dooms_renderer_into_a_21bparameter/) ⭐️ 8.0/10

一位开发者通过将计算图直接编译为模型权重，把 id Software 的《毁灭战士》渲染器移植到了一个 210 亿参数的 Transformer 中，整个过程零训练。最终生成的 Hugging Face 检查点能以令牌化绘图命令的形式生成完整的 E1M1 画面，在 NVIDIA B200 上耗时略超过 40 分钟。 这表明 Transformer 权重无需训练即可编码完整的经典算法，为构建可解释、可验证的神经模型提供了新路径。它可能启发将任意程序编译为神经网络权重的工具，对模型透明度、安全性和 AI 基础设施具有深远意义。 每帧需要 3614 个令牌的提示词外加 53747 个生成令牌，输出是一系列像素绘图命令，由 43 行主机程序解析成经典的 E1M1 画面。该检查点可作为标准 Hugging Face transformers 模型加载，无需 trust\_remote\_code，且源码计算图、权重和主机代码均已公开。

reddit · r/MachineLearning · /u/notforrob · 8月14日 15:50

**背景**: Transformer 是一种通过注意力机制处理序列的神经网络，其权重通常需要在大规模数据集上训练得到。本项目使用了名为 Torchwright 的自定义编译器，将固定的计算图直接转换为 Transformer 权重，因此不涉及任何学习过程。《毁灭战士》渲染引擎是 1993 年经典的软件渲染器，在 CPU 上绘制游戏的 3D 世界，而这项工作将其输出重现为逐令牌生成任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ood.dev/posts/calculator/">A calculator, compiled into a transformer — Out of Distribution</a></li>
<li><a href="https://towardsdatascience.com/i-built-a-tiny-computer-inside-a-transformer/">I Built a Tiny Computer Inside a Transformer | Towards Data Science</a></li>
<li><a href="https://doomwiki.org/wiki/Doom_rendering_engine">Doom rendering engine - The Doom Wiki at DoomWiki.org</a></li>

</ul>
</details>

**标签**: `#transformer`, `#compiler`, `#Doom`, `#deep learning`, `#neural networks`

---

<a id="item-7"></a>
## [Vivodyne 推出 AI 人体组织实验室，年测 300 万样本或终结动物测试](https://www.fastcompany.com/91589344/the-worlds-largest-biological-datacenter-could-help-make-animal-testing-obsolete) ⭐️ 8.0/10

Vivodyne 近日推出了其称之为全球最大的人类生物数据中心：由 12 个机器人 HIVE 实验室组成的网络，每年可运行 310 万项活体人组织实验。这一年产能约为美国所有临床试验总和的两倍。 这可能通过提供基于人体、AI 驱动的平台来更好地预测药物安全性和有效性，从而使动物测试变得过时。目前约 90%的临床试验在通过动物测试后仍然失败，因此规模化的人体组织测试可能大幅提高药物研发的成功率。 每个 HIVE 实验室使用 AI 设计的实验，该系统的受控试验规模约为美国所有临床试验总和的两倍。然而，这种方法能否真正在监管审批中替代动物测试仍有待验证。

telegram · zaihuapd · 8月14日 01:48

**背景**: 长期以来，动物测试一直是临床前药物评估的标准，但动物模型往往无法准确反映人体生物学。类器官和其他实验室培养的人体组织正在成为替代方案，而将其与 AI 和机器人技术结合可实现大规模筛选。Vivodyne 源自宾夕法尼亚大学的生物工程研究。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://biobuzz.io/news/penn-born-vivodyne-launches-what-it-calls-the-worlds-largest-human-biological-datacenter/">Penn-Born Vivodyne Launches What It Calls the World&#x27;s Largest ...</a></li>
<li><a href="https://www.aol.com/articles/vivodyne-launches-world-largest-human-130000000.html">Vivodyne Launches the World’s Largest Human Biological ...</a></li>
<li><a href="https://www.frontiersin.org/journals/bioengineering-and-biotechnology/articles/10.3389/fbioe.2023.1190637/full">Frontiers | Patient-derived organoids as a platform for drug screening in metastatic colorectal cancer</a></li>

</ul>
</details>

**标签**: `#AI`, `#生物技术`, `#药物测试`, `#人体组织`, `#动物测试替代`

---

<a id="item-8"></a>
## [小红书开源 dots3-note：280B MoE 仅激活 16B 参数](https://x.com/dotsstudioai/status/2088083314855018521) ⭐️ 8.0/10

小红书 dots 实验室正式发布了 dots3-note preview，这是 dots3 系列首个开放权重的模型。该模型总参数达 280B，每次仅激活 16B 参数，支持 512K 上下文，并能处理文本、图片、视频和音频。 本次开源通过将大规模 MoE 基座与全新的强化学习方法（TEMPO）相结合，推动了高效开源大模型的前沿发展，专门面向长程智能体任务。同时发布的 VibeSearchBench 和 VibeLifeBench 两个真实场景基准，也为社区提供了评估主动搜索和生活管理智能体的标准化手段。 该模型每次推理仅激活 280B 总参数中的 16B，相比同等规模的稠密模型大大降低了推理成本。TEMPO 方法通过自批判和测试时价值估计来训练长程智能体；配套基准包含 200 个双语搜索任务和 200 个跨多周的生活管理任务。

telegram · zaihuapd · 8月14日 08:27

**背景**: 混合专家模型（MoE）会为每个 token 只路由到部分参数，从而在单次计算量较低的情况下获得很大的模型总容量。目前强化学习正越来越多地被用于让 LLM 智能体具备长程规划和工具使用能力。TEMPO 在这一思路中加入了自批判与测试时价值估计；而新基准则聚焦于用户意图模糊、任务跨越多周且世界异步变化的真实场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/VibeBench/VibeSearchBench">GitHub - VibeBench/VibeSearchBench: 🔍 The hardest search benchmark in the wild — vague, multi-turn, proactive. 200 long-horizon tasks with persona-driven progressive disclosure, scored by verifiable schema-free knowledge-graph evaluation. No vibes, just triplet F1.</a></li>
<li><a href="https://arxiv.org/abs/2605.27882">[2605.27882] VibeSearchBench: Benchmarking Long-horizon Proactive Search in the Wild</a></li>
<li><a href="https://arxiv.org/abs/2608.10875">VibeLifeBench: Can Your Life Agent Be Proactive and ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#Open-Source`, `#MoE`, `#Reinforcement Learning`, `#Multimodal`

---

<a id="item-9"></a>
## [美国法官下令谷歌一周内去除第三方应用商店安装障碍](https://www.androidauthority.com/google-play-store-remove-third-party-app-store-friction-3698697/) ⭐️ 8.0/10

美国地区法官 James Donato 下令谷歌删除 Play 商店中安装第三方安卓应用商店的多余步骤和警告弹窗。谷歌须在一周内完成修改，让第三方商店的安装像安装普通应用一样直接。 这项裁决通过消除刻意设置的、有利于 Play 商店的摩擦，直接重塑了安卓应用分发格局。作为 Epic 诉谷歌案的实质性反垄断救济措施，它可能降低 Epic 自家应用商店等竞争对手的门槛，并影响用户发现替代应用市场的方式。 该命令针对的是那些反竞争的“摩擦”设计，例如要求用户先点击多个“查看详情”界面后才会出现“安装”按钮。根据陪审团关于谷歌在安卓应用分发中构成非法垄断的裁定，谷歌必须在裁决生效后一周内完成整改。

telegram · zaihuapd · 8月14日 09:55

**背景**: 安卓系统允许“侧载”，即通过传输 APK 文件从官方 Google Play 商店之外安装应用。Google Play Protect 会扫描设备中的有害应用并警告用户潜在风险，但法院认定 Play 商店中的部分警告和多余步骤是蓄意设计，旨在阻止用户安装第三方应用商店。这一裁决源于 Epic 诉谷歌反垄断案，Epic Games 指控谷歌利用其市场力量扼杀应用分发和支付处理领域的竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sideloading">Sideloading - Wikipedia</a></li>
<li><a href="https://support.google.com/googleplay/answer/2812853?hl=en">Use Google Play Protect to help keep your apps safe &amp; your data private - Google Play Help</a></li>
<li><a href="https://developers.google.com/android/play-protect">Play Protect | Google for Developers</a></li>

</ul>
</details>

**标签**: `#antitrust`, `#Google Play`, `#Android`, `#regulation`, `#app distribution`

---

<a id="item-10"></a>
## [库克 9 月 1 日卸任苹果 CEO，约翰·特努斯接任](https://www.youtube.com/watch?v=ZBB8ut58SdY) ⭐️ 8.0/10

蒂姆·库克将于 9 月 1 日卸任苹果 CEO，约翰·特努斯将接任首席执行官。库克将继续担任执行董事长，并表示希望大家记住他善良、正直的一面。 此次领导层变动意义重大，因为苹果是全球最具影响力的科技公司之一。这一交接可能会影响苹果的战略方向、产品路线图和企业治理。 库克的卸任日期和继任者首次一同公布。卸任后，库克将留任执行董事长，以支持新的运营团队。

telegram · zaihuapd · 8月14日 11:00

**背景**: 蒂姆·库克自 2011 年接替史蒂夫·乔布斯以来一直担任苹果 CEO。执行董事长通常专注于董事会治理和战略监督，而非日常管理。约翰·特努斯是苹果高管，他的任命标志着公司领导层进入新阶段。

**标签**: `#Apple`, `#Tim Cook`, `#CEO`, `#leadership`, `#tech news`

---

<a id="item-11"></a>
## [苹果联手阿里自研中国专属 AI 模型，或成首个获批外企](https://www.reuters.com/business/retail-consumer/apple-trains-its-own-ai-model-china-market-with-alibabas-support-sources-say-2026-08-14/) ⭐️ 8.0/10

苹果已专门为中国市场训练了一款大语言模型，并获得了阿里巴巴的支持，且已于上月向中国网信办备案其生成式 AI 服务。这款自研模型预计将在未来数月内随 iOS 更新与 Apple Intelligence 一起在华上线，标志着苹果从依赖第三方模型转向自研策略。 若获批，苹果将成为首个获北京批准在华提供自有 AI 模型的外国公司，这是重要的监管里程碑。此举让苹果在其最重要的市场之一获得对 AI 体验的更大掌控，并可能影响全球科技公司应对中国严格 AI 监管的方式。 该模型专为中国市场训练，并借助了阿里巴巴的支持，相关生成式 AI 服务已向中国网信办备案。Apple Intelligence 预计在未来数月内随 iOS 更新在华推出，但目前尚未公布具体支持的设备和上线日期。

telegram · zaihuapd · 8月14日 14:47

**背景**: Apple Intelligence 是苹果在 2024 年 WWDC 上发布的一套 AI 功能，集成于 iOS 18、iPadOS 18 和 macOS Sequoia，包括写作工具、图像生成、通知摘要以及 ChatGPT 集成。在中国，生成式 AI 服务须在 2023 年 8 月生效的规定下于上线前向网信办备案，截至 2025 年 3 月已有 346 个服务完成备案。苹果此前在中国的 AI 服务依赖第三方模型，如今正转向自研模型，并借助本地合作伙伴的支持来满足监管要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence</a></li>
<li><a href="https://appinchina.co/blog/what-is-chinas-aigc-filing/">What is China’s AIGC Filing?</a></li>
<li><a href="http://english.scio.gov.cn/pressroom/2025-04/09/content_117814020.html">346 generative AI services filed with Cyberspace Administration of China | english.scio.gov.cn</a></li>

</ul>
</details>

**标签**: `#Apple`, `#AI`, `#China`, `#Alibaba`, `#Regulation`

---


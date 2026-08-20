# Horizon 每日速递 - 2026-08-20

> 从 36 条内容中筛选出 10 条重要资讯。

---

1. [恶意 Rust 库 arrayref 在构建时执行载荷](#item-1) ⭐️ 9.0/10
2. [GitHub 公布 8 月 17 日宕机原因：重试漏洞将流量放大 10 倍](#item-2) ⭐️ 8.0/10
3. [速卖通静默 WebAudio 指纹识别干扰蓝牙多点连接](#item-3) ⭐️ 8.0/10
4. [反思文章：传统教育如何扼杀生物学的奇妙](#item-4) ⭐️ 8.0/10
5. [设备端钢琴自动续写：125M 参数 Transformer](#item-5) ⭐️ 8.0/10
6. [Linux 7.2 发布，AMD HDMI 2.1 支持引热议](#item-6) ⭐️ 8.0/10
7. [AI 让中国学生作业分涨 18% 考试分却降 20%](#item-7) ⭐️ 8.0/10
8. [Stripe 同意收购 AI 模型网关 OpenRouter，覆盖 400 多个模型](#item-8) ⭐️ 8.0/10
9. [陶哲轩警告：AI 或引发数学界最大危机，证明过剩无人能懂](#item-9) ⭐️ 8.0/10
10. [反向查询服务泄露数百万张人脸照片](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [恶意 Rust 库 arrayref 在构建时执行载荷](https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/) ⭐️ 9.0/10

广泛使用的 Rust 库 arrayref 的一个被攻破的版本引入了拼写仿冒（typosquatting）的 proc-macro1 包，其构建脚本会在编译时下载并运行远程二进制程序。安全研究人员表示，恶意版本在开发者系统上执行了后门，arrayref 的维护者账户也遭到入侵。 这是一起针对 Rust 热门库的重大供应链攻击，任何依赖受影响版本的项目都可能在日常构建过程中执行恶意代码。同时，它暴露了 crates.io 和 GitHub 在处理安全事件方面的不足，影响整个 Rust 生态。 恶意包名为 proc-macro1，是对合法过程宏辅助库 proc-macro2 的拼写仿冒（typosquat），载荷会在 Cargo 的 build.rs 阶段、包编译之前执行。社区报告称，恶意版本已从 crates.io 上移除，但没有明显的 yank 标记，也没有 RustSec 安全公告。

hackernews · abhisek · 8月20日 13:23 · [社区讨论](https://news.ycombinator.com/item?id=49374269)

**背景**: Cargo 是 Rust 的包管理器，它允许包包含 build.rs 脚本；该脚本会在包本身编译之前被编译并运行，这是用于生成代码或链接原生库的合法机制。RustSec 咨询数据库是社区维护的仓库，用于收录针对 crates.io 包的安全公告。此类供应链攻击在开源生态中日益令人担忧，因为一个被攻破的依赖就可能影响成千上万的下游项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-poison-arrayref-rust-crate-to-push-infostealer-malware/">Hackers poison arrayref Rust crate to push infostealer malware</a></li>
<li><a href="https://www.wiz.io/blog/rust-supply-chain-attack-on-arrayref-significant-overlap-with-dprk-campaigns">Rust Supply Chain Attack on arrayref: Significant Overlap ...</a></li>
<li><a href="https://doc.rust-lang.org/cargo/reference/build-scripts.html">Build Scripts - The Cargo Book</a></li>

</ul>
</details>

**社区讨论**: 评论者批评 GitHub 在事件期间直接隐藏仓库，并批评 crates.io 在没有 yank 标记或安全公告的情况下移除恶意版本。还有人呼吁 Cargo 对 build.rs 脚本进行沙盒隔离，并主张采用“内置电池”式标准库，以减少庞大的依赖树，从而降低 AI 辅助供应链攻击的可能性。

**标签**: `#supply chain security`, `#Rust`, `#malware`, `#security advisory`, `#open source ecosystem`

---

<a id="item-2"></a>
## [GitHub 公布 8 月 17 日宕机原因：重试漏洞将流量放大 10 倍](https://github.blog/news-insights/company-news/the-august-17-outage-and-the-work-ahead/) ⭐️ 8.0/10

GitHub 发布了一份关于 8 月 17 日宕机的事后分析报告，揭示 VS Code 中一个潜在的重试漏洞将流量放大了约 10 倍，并延迟了 Copilot Token Service 的恢复。宕机期间，一个内部端点响应延迟触发了客户端重试循环，进一步加剧了问题。 这一事件凸显了看似无害的客户端重试逻辑如何在宕机期间指数级放大负载，影响数百万 GitHub 和 Copilot 用户。它也强调了在大型生态系统中采用稳健重试策略、熔断器以及客户端与服务间协调的重要性。 该重试漏洞由单个内部端点的延迟响应触发，造成客户端重试循环，流量被放大约 10 倍，延长了 Copilot Token Service 的恢复时间。报告还提到，自 4 月以来月提交量从 14 亿增长到 29 亿，表明用户规模迅速扩大，也给可靠性工作带来了更大压力。

hackernews · 0xedb · 8月20日 19:22 · [社区讨论](https://news.ycombinator.com/item?id=49378957)

**背景**: 重试风暴是指大量客户端在同一时间对失败或缓慢的请求进行重试，产生的流量激增会加剧原有问题。最佳实践包括使用指数退避和抖动（jitter）以及熔断器来防止级联故障。GitHub 的这次事件是重试风暴反模式的典型例子：客户端为了不让用户看到错误而不断重试，反而形成反馈循环，拖延了恢复进程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/azure/architecture/antipatterns/retry-storm/">Retry Storm Antipattern - Azure Architecture Center</a></li>
<li><a href="https://jeffbailey.us/blog/2025/12/16/what-is-a-retry-storm/">What Is a Retry Storm? | Jeff Bailey</a></li>
<li><a href="https://www.baeldung.com/resilience4j-backoff-jitter">Better Retries with Exponential Backoff and Jitter | Baeldung</a></li>

</ul>
</details>

**社区讨论**: 评论者观点不一：有人批评行业不惜一切代价避免让用户看到错误的趋势，导致用户盯着加载图标数小时；也有人感谢 GitHub 在大规模免费服务上的投入。还有人注意到提交量从 14 亿涨到 29 亿的惊人增长，认为是行业&\#x27;生产力焦虑&\#x27;的体现。另一位评论者则质疑激进重试的价值，认为桌面服务应尽量减少重试，以避免此类雪崩式故障。

**标签**: `#outage`, `#post-mortem`, `#reliability`, `#GitHub`, `#retry-logic`

---

<a id="item-3"></a>
## [速卖通静默 WebAudio 指纹识别干扰蓝牙多点连接](https://blog.laserphile.com/2026/08/aliexpress-webpage-keeping-multipoint.html) ⭐️ 8.0/10

速卖通网站通过 OfflineAudioContext 运行静默 WebAudio 指纹识别，产生的无声音频流会干扰蓝牙多点连接。用户报告在打开速卖通页面或应用时，助听器、车载音响等蓝牙设备出现异常。 这一事件凸显了一种具有真实世界副作用的隐私侵犯型指纹识别技术。它表明网络跟踪可能损害硬件功能，影响用户的蓝牙设备，并削弱对浏览的信任。 该指纹识别技术渲染一段静音波形并对其进行哈希，生成稳定的浏览器标识符，即使在隐私模式和清除 Cookie 后依然有效。这种静音流可能会混淆蓝牙多点连接（该功能期望音频由用户发起），而且由于音频是静音的，浏览器可能不会显示扬声器图标。

hackernews · emctech · 8月20日 10:08 · [社区讨论](https://news.ycombinator.com/item?id=49372583)

**背景**: WebAudio 指纹识别是一种跟踪技术，利用 Web Audio API 的 OfflineAudioContext 静默渲染一段短暂的音频样本，然后对结果进行哈希以识别设备。蓝牙多点连接允许耳机或扬声器同时保持与多个设备的连接，并在音频流之间切换。当网页通过蓝牙链路播放静音音频时，设备可能将其视为活动音频流，从而破坏多点切换。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=49372583">AliExpress runs silent WebAudio fingerprinting that breaks ...</a></li>
<li><a href="https://privacyscore.dev/blog/audio-fingerprinting-explained">Audio Fingerprinting: The Silent Browser Tracker</a></li>
<li><a href="https://shokz.com/blogs/news/bluetooth-multipoint-vs-dual-audio">Bluetooth Multipoint vs Dual Audio: What&#x27;s the Difference?</a></li>

</ul>
</details>

**社区讨论**: 评论者报告了助听器的相关蓝牙故障，以及 AliExpress 的 iOS 应用触发车载音响命令的问题，并希望静音音频能触发标签页的扬声器图标。有人分享了 Firefox 缓解该技术的链接，还有人讽刺地表示苹果应该将速卖通从 App Store 中下架。

**标签**: `#privacy`, `#fingerprinting`, `#web security`, `#webaudio`, `#bluetooth`

---

<a id="item-4"></a>
## [反思文章：传统教育如何扼杀生物学的奇妙](https://jsomers.net/i-should-have-loved-biology/) ⭐️ 8.0/10

在 2020 年的一篇反思性文章中，作者 jsomers.net 认为传统教育通过死记硬背扼杀了他对生物学的天然好奇。这篇文章在 Hacker News 上引发了关于生命科学浪漫与现实之辨以及发现式学习价值的讨论。 这篇文章引起科技和科学界许多读者的共鸣，揭示了教学法中一个系统性问题，可能使一些学生不愿从事科学职业。它也为关于如何让科学教育更以探究为导向、减少知识灌输的长期讨论提供了新的素材。 这篇 Hacker News 帖获得了 170 分和 64 条评论，评论者引用了皮亚杰、布鲁纳和帕珀特等教育理论家的观点。有评论者提出反论点：现实中的生命科学研究往往不如文章所描绘的那样浪漫。

hackernews · tyre · 8月20日 17:50 · [社区讨论](https://news.ycombinator.com/item?id=49377853)

**背景**: 发现式学习是一种建构主义教育方法，学生通过探索和解决问题而非直接教学来获取知识，这种方法得到皮亚杰、布鲁纳和帕珀特等理论家的支持。相比之下，传统教育往往强调对既定事实的死记硬背，批评者认为这会压制好奇心。这篇文章还涉及“浪漫科学”这一历史视角，它重视惊奇感和整体理解，一些教育者认为这种视角有助于激发学生对科学的兴趣。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Discovery_learning">Discovery learning - Wikipedia</a></li>
<li><a href="https://uteach.io/articles/discovery-based-learning-definition-principles-and-techniques">Discovery-Based Learning: Definition, Principles, Techniques What is discovery based learning? - California Learning ... Discovery-Based Learning: Why We Learn by Doing Discovery-Based Learning | Center for the Advancement of STEM ... Discovery Learning (Bruner) – Learning Theories The Discovery Learning Model: Instructional Design Models ...</a></li>
<li><a href="https://www.frontiersin.org/journals/education/articles/10.3389/feduc.2019.00038/full">Frontiers | Engaging Students in Science: The Potential Role of “Narrative Thinking” and “Romantic Understanding”</a></li>

</ul>
</details>

**社区讨论**: 评论者大多对这篇文章感同身受，分享了他们因死记硬背式教育而好奇心受挫的经历。一位从数据科学家转行做生物研究的评论者提醒，真实的研究工作包含大量琐碎事务；其他人则将这种批评与皮亚杰和帕珀特关于通过互动学习的观点联系起来。还有人指出物理和化学教育也存在同样的问题。

**标签**: `#biology`, `#education`, `#pedagogy`, `#science`, `#reflection`

---

<a id="item-5"></a>
## [设备端钢琴自动续写：125M 参数 Transformer](https://simedw.com/2026/08/20/midi-autocomplete/) ⭐️ 8.0/10

一位开发者训练了一个 1.25 亿参数的 Transformer 模型，在 iPhone 15 上以约每秒 108 个音符的速度实时自动续写钢琴演奏。该系统通过一款免费应用展示：用户在 MIDI 钢琴上弹几个音符后，模型会完全在设备端继续完成演奏。 该项目将 GitHub Copilot 这类代码助手的“自动补全”范式应用到音乐领域，使 AI 生成变成一种互动、实时的创作工具。它还表明相对较小的 1.25 亿参数模型也能在设备端高效运行，为私密、低延迟的 AI 创意工具指出了方向。 模型处理的是 MIDI 音符事件而非音频，这种紧凑的表示使其能够满足实时推理要求。作者欢迎就模型、训练数据、Core ML 转换以及失败尝试提问；评论中也有用户专门询问预训练和后训练的样本量。

hackernews · simedw · 8月20日 12:04 · [社区讨论](https://news.ycombinator.com/item?id=49373456)

**背景**: Transformer 是一种最初为语言建模设计的深度学习架构，也是 GPT 等生成式模型的基础；它按顺序预测序列中的下一个 token，在这个项目中即预测钢琴曲的下一个音符。MIDI 是数字乐器领域的技术标准，以音符开/关事件来编码演奏信息，因此非常适合用于符号化音乐生成。Core ML 是苹果的设备端机器学习框架，能在 iPhone 上高效运行模型，并通过避免云端处理来保护用户隐私。“设备端”推理意味着整个模型在本地运行，因此没有网络延迟，用户数据也不会离开设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generative_pre-trained_transformer">Generative pre-trained transformer - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/MIDI">MIDI - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论整体积极，有人称赞这个项目“很有 HN 精神”，并指出真正的价值在于探索和学习过程，而不仅是演示本身。讨论也很有深度：有人将它联系到古典作曲训练中的“自动补全”传统，有人类比 AI 辅助设计工具，还有人追问数据集规模，并提到听到《致爱丽丝》开头被引向意外方向时会产生一种奇特的不安感。

**标签**: `#machine-learning`, `#music-generation`, `#transformers`, `#on-device-ai`, `#coreml`

---

<a id="item-6"></a>
## [Linux 7.2 发布，AMD HDMI 2.1 支持引热议](https://www.igalia.com/2026/08/19/Linux-72-Released.html) ⭐️ 8.0/10

Linux 7.2 已正式发布，带来了一系列内核改进和驱动更新。此次发布特别引发了社区关于 AMD 开源驱动中 HDMI 2.1 支持如何实现的热议。 这次发布对 Linux 用户，尤其是使用 AMD GPU 的用户意义重大，因为 HDMI 2.1 支持一直是一个备受争议且期待已久的功能。它反映了开源图形驱动的持续进步，可能影响 Linux 在高刷新率显示器上的采用。 社区讨论指出，此前 HDMI 2.1 支持曾受到 HDMI 论坛的阻碍，而新版本似乎已包含该支持，但原因并不明确。用户也好奇此类内核发布新闻的目标受众，以及 HDMI 相比 DisplayPort 的实际好处。

hackernews · mariuz · 8月20日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=49376265)

**背景**: Linux 7.2 是一个主要内核版本，遵循 Linux 内核的标准发布周期。AMD 的开源 GPU 驱动 AMDGPU 是 Linux 上 Radeon 显卡的主要驱动，并且已经完全上游化。HDMI 2.1 是一个重要的接口标准，支持高达 48 Gbps 的带宽，可实现更高的分辨率和刷新率，并支持 VRR 和 eARC 等功能。HDMI 论坛的许可和合规要求历来限制了 HDMI 2.1 功能在开源中的实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AMDgpu_%28Linux_kernel_module%29">AMDgpu (Linux kernel module) - Wikipedia</a></li>
<li><a href="https://www.rtings.com/tv/learn/hdmi-2-1">What Is HDMI 2.1?: An Overview - RTINGS.com</a></li>

</ul>
</details>

**社区讨论**: 社区评论呈现出好奇与怀疑交织的氛围，用户询问在之前的限制下 HDMI 2.1 支持如今为何成为可能，以及 HDMI 是否比 DisplayPort 更可取。一些用户对更新树莓派感到兴奋，另一些用户则认为该发布新闻很有见地。

**标签**: `#linux`, `#kernel`, `#hdmi`, `#open-source`, `#release`

---

<a id="item-7"></a>
## [AI 让中国学生作业分涨 18% 考试分却降 20%](https://www.economist.com/graphic-detail/2026/08/18/does-ai-stop-children-from-learning) ⭐️ 8.0/10

一项针对 2.7 万名 12 至 18 岁中国学生的研究发现，AI 辅助学习使作业平均分提高 18%，但六个月后考试成绩比不用 AI 的同学低 20%。成绩下滑主要集中在那些主要用 AI 赶作业的学生身上。 这是规模最大的真实教育场景研究之一，量化了 AI 对学习的混合影响，说明作业分数的快速提升并不等于更深的学习效果。这一发现对教育科技领域的乐观预期提出挑战，也提示学校需要制定政策，引导学生把 AI 当辅导工具而非抄捷径的手段。 约 80%的参与者使用了豆包等常见 AI 模型，使用 AI 的学生每项作业平均耗时从 64 分钟降至 45 分钟。花同样时间用 AI 理解概念的学生考试并未下降；另一项研究也发现，借助聊天机器人学习的大学生测试得分更高。

telegram · zaihuapd · 8月20日 03:58

**背景**: 豆包是字节跳动推出的 AI 聊天机器人，据 QuestMobile 在 2025 年引用的数据，其月活用户超过 1.72 亿，是中国最受欢迎的 AI 应用之一。大语言模型既可以充当数字辅导老师，也可能被学生用来快速生成作业答案，从而在作业成绩和考试成绩之间造成差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/%E8%B1%86%E5%8C%85_%28%E8%81%8A%E5%A4%A9%E6%9C%BA%E5%99%A8%E4%BA%BA%29">豆包 (聊天机器人) - 维基百科，自由的百科全书</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/705205912">深度剖析字节豆包AI - 知乎</a></li>
<li><a href="https://www.53ai.com/news/LargeLanguageModel/2024080658760.html">豆包，大模型的磁力三重奏 - 53AI-AI知识库|企业AI知识库|大模型知识库|AIHub</a></li>

</ul>
</details>

**标签**: `#AI`, `#教育技术`, `#教育研究`, `#学习`, `#AI教育影响`

---

<a id="item-8"></a>
## [Stripe 同意收购 AI 模型网关 OpenRouter，覆盖 400 多个模型](https://stripe.com/en-jp/newsroom/news/stripe-agrees-to-acquire-openrouter) ⭐️ 8.0/10

Stripe 于 2026 年 8 月 19 日宣布同意收购 AI 模型网关与路由平台 OpenRouter。该平台可根据任务复杂度、价格、速度和可靠性，在 80 多家提供商的 400 多个模型之间动态分配请求，帮助企业优化 Token 使用。 此次收购标志着 AI 基础设施领域的重要举措，将 Stripe 的支付生态系统与 OpenRouter 的模型分发层相结合。它可能重塑开发者访问和支付 AI 模型的方式，使 Stripe 在 AI 与支付的交汇处占据战略位置。 OpenRouter 提供统一的 API 密钥和请求格式，可访问来自 Anthropic、Google、Meta、Mistral 等提供商的数百个模型，覆盖 80 多家提供商、400 多个模型。此次收购的财务条款未披露。

telegram · zaihuapd · 8月20日 07:00

**背景**: AI 模型路由是在应用与模型提供商之间设置软件层，根据成本、延迟或质量要求为每次请求动态选择最佳模型。OpenRouter 是该领域知名的统一 API 网关，开发者只需一次集成即可在众多模型间进行原型验证和基准测试。这一背景有助于理解 Stripe 此举的重要性：它将 AI 模型分发与支付融为一体，为大规模消耗 Token 的 AI 智能体和应用提供了关键支撑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://ai-sdk.dev/providers/community-providers/openrouter">Community Providers: OpenRouter</a></li>
<li><a href="https://inworld.ai/resources/ai-model-routing-cost-reduction">AI Model Routing Explained : Cut LLM Costs (2026) - Inworld AI</a></li>

</ul>
</details>

**标签**: `#AI`, `#acquisition`, `#model-router`, `#Stripe`, `#infrastructure`

---

<a id="item-9"></a>
## [陶哲轩警告：AI 或引发数学界最大危机，证明过剩无人能懂](https://the-decoder.com/terence-tao-says-ai-could-trigger-maths-biggest-crisis-since-godel/) ⭐️ 8.0/10

陶哲轩在为 2026 年国际数学家大会撰写的文章中警告，AI 可能引发自哥德尔以来数学界最大的危机。他援引 First-Proof 项目第二轮的结果：4 个 AI 系统测试了 10 道未发表的研究题，其中 7 道至少被一个系统判定为合格，每题成本仅需数十至数百美元。 这种转变可能让数学从“证明稀缺”走向“证明过剩”，大量证明由机器生成而无人能够真正理解。这将挑战验证与信任的核心概念，影响所有依赖证明作为黄金标准的数学家、期刊和资助机构。 陶哲轩认为，无法被清晰讲解的证明即使通过形式验证，也应被视为不完整。First-Proof 的结果显示，研究级的 AI 证明已经变得廉价且看似合理，因此他呼吁数学界不要再争论 AI 能做什么，而应正视研究目标这一被回避的问题。

telegram · zaihuapd · 8月20日 13:19

**背景**: First-Proof 是斯坦福大学和哈佛大学发起的项目，让 AI 系统在没有提示或参考文献的情况下面对全新的研究级猜想。形式验证是一种严格的、可由机器检查的逻辑正确性确认方法，但它并不保证人类能理解推理过程。20 世纪初罗素悖论和哥德尔不完备定理引发的危机，也曾迫使数学家重新审视学科的基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.daniellitt.com/blog/2026/2/20/mathematics-in-the-library-of-babel">Mathematics in the Library of Babel — Daniel Litt</a></li>
<li><a href="https://aiguidenews.com/en/news/363ac70d-b60e-4c3d-be31-607fd400fe29">OpenAI&#x27;s First Proof — When AI Takes on... | AI Guide News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_proof">Formal proof - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI`, `#mathematics`, `#Terence Tao`, `#proofs`, `#research`

---

<a id="item-10"></a>
## [反向查询服务泄露数百万张人脸照片](https://arstechnica.com/gadgets/2026/08/reverse-lookup-service-exposed-millions-of-photos-of-peoples-faces/) ⭐️ 8.0/10

一家反向图像搜索服务泄露了一个约 450 GB 的数据库，其中包含超过 900 万张人物面部图像，以及关联的邮箱、电话号码和 IP 地址。服务方目前已限制数据库访问，但事件影响范围和补救措施仍在确认中。 人脸属于难以更换的生物识别标识，此次泄露引发了严重的隐私与身份安全担忧。泄露的数据可能被用于未经授权的身份识别、追踪或诈骗，可能影响数百万人。 被泄露的数据库约 450 GB，包含超过 900 万条记录，其中部分涉及邮箱、电话号码和 IP 地址。由于面部图像属于生物识别数据，其影响可能比普通的凭据泄露更为严重，专家呼吁密切监控。

telegram · zaihuapd · 8月20日 15:14

**背景**: 反向图像搜索服务允许用户上传照片，并在互联网上查找相似或相同的图片。这类服务通常依赖感知哈希算法（将图像特征转换为可比较的指纹）或人脸特征向量（将人脸表示为数学向量以进行相似度匹配）等技术。由于这些系统往往存储原始图像及关联的元数据，一旦发生泄露，就可能同时暴露生物识别数据和个人联系方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnblogs.com/raorao1994/p/9108345.html">感 知 哈 希 算 法 - 扰扰 - 博客园</a></li>
<li><a href="https://blog.csdn.net/wyyang2/article/details/118553455">图像识别与 哈 希 算 法 ：pHash、aHash与dHash的比较与实现-CSDN博客</a></li>
<li><a href="https://blog.csdn.net/u013250861/article/details/121387151">CV-CNN-2015：FaceNet（人脸特征向量提取、计算欧氏距离）【Triplet L...</a></li>

</ul>
</details>

**标签**: `#数据泄露`, `#隐私`, `#生物识别`, `#安全`

---


# Horizon 每日速递 - 2026-07-29

> 从 41 条内容中筛选出 9 条重要资讯。

---

1. [开源引擎在 M 系列 Mac 上用 2GB 内存运行 Gemma 4 26B](#item-1) ⭐️ 9.0/10
2. [俄联邦安全局刑事指控杜罗夫协助恐怖活动，发出国际通缉](#item-2) ⭐️ 9.0/10
3. [Mitchell Hashimoto 宣布成立 Superlogical，基于 libghostty 构建](#item-3) ⭐️ 8.0/10
4. [Handbook.md 论文：长篇幅政策文件无法可靠约束 AI 智能体](#item-4) ⭐️ 8.0/10
5. [文档携带的 AI 蠕虫通过 Word 版 Copilot 自我传播](#item-5) ⭐️ 8.0/10
6. [ncnn 的 Vulkan 后端将边缘 ML 推理速度提升至 CPU ONNX 的 10 倍](#item-6) ⭐️ 8.0/10
7. [Claude 共享对话及 Artifacts 遭谷歌索引](#item-7) ⭐️ 8.0/10
8. [报告称 Hugging Face 被广泛用于生成深度伪造裸照](#item-8) ⭐️ 8.0/10
9. [月之暗面融资 35 亿美元，估值 350 亿美元](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [开源引擎在 M 系列 Mac 上用 2GB 内存运行 Gemma 4 26B](https://github.com/drumih/turbo-fieldfare) ⭐️ 9.0/10

TurboFieldfare 是一款用 Swift 和 Metal 编写的推理引擎，通过从 SSD 流式传输路由的 MoE 专家，在 M 系列 Mac 上仅用约 2GB 内存即可运行 4-bit 量化的 Gemma 4 26B 模型。 这使得在内存受限的设备（如基础款 Mac）上运行大型语言模型成为可能，无需昂贵的高内存硬件，从而让更多人能使用先进的 AI。 4-bit 量化权重约 14GB，但只有共享层和 KV 缓存保留在 RAM 中；路由的专家通过小型专家缓存和有界并行预读从 SSD 流式传输。在 8GB M2 MacBook Air 上可达 5-6 tok/s，在 M5 MacBook Pro 上可达 31-35 tok/s。

hackernews · gitpusher42 · 7月29日 15:05 · [社区讨论](https://news.ycombinator.com/item?id=49098510)

**背景**: 混合专家（MoE）模型有多个专门的“专家”子网络，每个 token 只激活其中一部分。传统推理需要将所有权重加载到内存中，但利用 MoE 的稀疏性，可以按需加载所需的专家。该项目基于这一原理，使用 SSD 流式传输来突破内存限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2202.09368">[2202.09368] Mixture-of-Experts with Expert Choice Routing Images Intro to Routing: Mixture-of-Experts and Expert Choice [2510.04694] Multilingual Routing in Mixture-of-Experts Mixture-of-Experts with Expert Choice Routing - NeurIPS Mixture-of-Experts with Expert Choice Routing - Google Research Top-K Routing: Expert Selection in Mixture of Experts Models Parameter-Efficient Routed Fine-Tuning: Mixture-of-Experts ...</a></li>
<li><a href="https://arxiv.org/abs/2603.20397">[2603.20397] KV Cache Optimization Strategies for Scalable ... Understanding KV Caching in Transformers - Medium KV Cache in Transformers – Optimizing LLM Inference Cache strategies · Hugging Face</a></li>
<li><a href="https://www.mindstudio.ai/blog/ssd-streaming-ai-models-ram-dial">SSD Streaming for AI Models: How to Turn RAM from a Wall into ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论讨论了与 llama.cpp 中 mmap 的对比，指出 TurboFieldfare 将 SSD 读取与推理活动同步以最小化延迟。一位用户提供了在较旧 macOS 版本上编译的解决方法，另一位用户则对没有 Nvidia GPU 的 Apple 硬件上慢速推理的实际用途表示怀疑。

**标签**: `#AI`, `#inference`, `#mac`, `#open-source`, `#optimization`

---

<a id="item-2"></a>
## [俄联邦安全局刑事指控杜罗夫协助恐怖活动，发出国际通缉](https://www.interfax.ru/russia/1106228) ⭐️ 9.0/10

这一针对知名科技创始人的前所未有的法律升级，为平台责任和内容审核开创了危险先例，可能影响全球消息平台的运营方式，并引发对言论自由和政府越权的严重担忧。 FSB 具体指控 Telegram 管理层拒绝删除被乌克兰情报机构及恐怖/极端组织用于协调破坏、恐怖袭击、大规模杀戮和网络诈骗的频道、群组和机器人，造成多人伤亡和数十亿卢布损失。

telegram · zaihuapd · 7月29日 05:56

**背景**: Telegram 由帕维尔·杜罗夫创立，是一款广泛使用的消息平台，以其强大的加密和隐私保护功能闻名。在俄乌战争背景下，Telegram 既是战争更新消息的重要来源，也成为虚假信息和攻击协调的温床。杜罗夫是俄罗斯出生的企业家，2024 年在法国因其他指控被捕，进一步加剧了他的法律困境。FSB 的国际通缉表明俄罗斯有意让平台领导者对用户生成内容承担个人责任。

**标签**: `#Telegram`, `#Pavel Durov`, `#legal`, `#content moderation`, `#Russia`

---

<a id="item-3"></a>
## [Mitchell Hashimoto 宣布成立 Superlogical，基于 libghostty 构建](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto 宣布成立新公司 Superlogical，该公司将在开源库 libghostty 之上构建终端应用，而 Ghostty 本身已转交给非营利组织。 此举通过将核心终端模拟器（Ghostty）与商业产品分离，建立了一种可持续的开源商业模式，可能为其他寻求在不损害社区信任的前提下变现的开源项目提供参考。 Superlogical 将使用与他人相同的 MIT 许可证的 libghostty 组件，并将共享的终端工作上游化，使所有 libghostty 用户受益。该公司专注于构建终端应用，而非模拟器本身。

hackernews · yan · 7月29日 15:41 · [社区讨论](https://news.ycombinator.com/item?id=49098965)

**背景**: Ghostty 是一个快速、功能丰富、跨平台的终端模拟器，采用 GPU 加速和原生 UI。libghostty 是其 C 兼容库，允许开发者将终端模拟功能嵌入其他应用，以 MIT 许可证发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Uzaaft/awesome-libghostty">GitHub - Uzaaft/awesome-libghostty</a></li>
<li><a href="https://ghostty.org/">Ghostty</a></li>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty -org/ ghostty : Ghostty is a fast, feature-rich, and...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞这一开源策略，有人指出将 Ghostty 转交给非营利组织并在此基础上构建 Superlogical 的做法很巧妙。部分人将其与 OLE/COM 类比，也有少数人批评标题故弄玄虚，有标题党之嫌。

**标签**: `#opensource`, `#company`, `#terminal`, `#mitchellh`, `#ghostty`

---

<a id="item-4"></a>
## [Handbook.md 论文：长篇幅政策文件无法可靠约束 AI 智能体](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

一篇题为《Handbook.md》的新论文表明，长篇幅政策文件在约束 AI 智能体方面不可靠，揭示了当前长上下文模型在策略遵循方面的根本局限性。 这一发现挑战了仅靠增加上下文长度就能确保 AI 对齐的假设，因为即使是拥有百万级 token 上下文的模型也无法可靠地遵循详细策略，这引发了自主智能体的关键安全问题。 该论文可能使用了一个要求智能体遵循冗长复杂政策文档的基准测试，并发现性能随文档长度显著下降，突显了 KV 缓存量化和有限工作记忆的问题。

hackernews · spIrr · 7月29日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=49096969)

**背景**: 长上下文模型（如声称支持 128K 或 1M token 的模型）常被用于需要保留大量信息的任务，但实际在长上下文基准上的表现差异很大。AI 策略遵循是指衡量模型输出遵循一套书面规则的程度。这篇论文进一步证明，当前的长上下文模型对于约束必须遵守详细策略的自主智能体并不可靠。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://benchlm.ai/best/long-context">Best Long Context AI Models (July 2026) — Ranked by Benchmark Data</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍赞同这一发现，指出长上下文模型由于量化和采样器问题在实际中表现不佳。有评论者观察到，即使是人类也难以遵守长篇政策文件，因此期望模型完美遵循可能不现实。另一位评论者指出，如果模型没有针对特定手册进行专门训练，它就不会遵循，这表明后训练对于智能体能力至关重要。

**标签**: `#AI alignment`, `#long-context models`, `#AI safety`, `#policy adherence`, `#LLM limitations`

---

<a id="item-5"></a>
## [文档携带的 AI 蠕虫通过 Word 版 Copilot 自我传播](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 8.0/10

安全研究员 Håkon Måløy 展示了一种新型提示注入变体，可将 Microsoft Word 文档转变为针对 Word 版 Copilot 的自我复制 AI 蠕虫。该攻击于 2026 年 7 月 28 日至 29 日向微软 MSRC 披露，是主流办公套件中首次公开演示文档携带的 AI 蠕虫自我传播。 该攻击利用了 Copilot 等 AI 助手无法区分可信指令与用户提供内容的缺陷，使得蠕虫能通过共享文档在无人干预下传播。鉴于 Copilot 已集成到 Microsoft Office 并可访问敏感数据，此漏洞对企业用户构成了严重且未缓解的安全风险。 该攻击通过将恶意指令隐藏在文档元数据或格式（例如白色文本）中，Copilot 读取并执行这些指令，从而修改文档并将蠕虫传播到新文件。值得注意的是，当蠕虫从内部创建的文档传播时，它会继承该文档的信任级别，使得检测更加困难。截至发布，尚无有效的缓解措施。

hackernews · Canopy9560 · 7月29日 11:44 · [社区讨论](https://news.ycombinator.com/item?id=49096188)

**背景**: 提示注入是一种攻击类型，通过利用 AI 模型无法区分指令与数据的缺陷，使对抗性输入诱使模型产生非预期行为。在间接提示注入中，恶意提示被嵌入 AI 检索的内容中，例如网页或文档。此研究扩展了这一概念，创造了自我复制的蠕虫，类似于 1990 年代的宏病毒，但使用的是自然语言而非宏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://www.explainx.ai/blog/copilot-word-document-ai-worm-xpia-july-2026">Copilot Word AI Worm XPIA — July 2026 | explainx.ai Blog</a></li>

</ul>
</details>

**社区讨论**: Hacker News 社区对此反应警觉，许多人指出只要 AI 系统将指令与数据混合，该漏洞可能无法修复。评论者警告称，GitHub 仓库或电子邮件可能被用于传播类似蠕虫，一些用户已卸载本地机器上的 Copilot 作为预防措施。其他人指出，诸如白色文本之类的简单技术仍然有效，凸显了利用的简便性。

**标签**: `#AI security`, `#prompt injection`, `#worm`, `#Copilot`, `#adversarial attacks`

---

<a id="item-6"></a>
## [ncnn 的 Vulkan 后端将边缘 ML 推理速度提升至 CPU ONNX 的 10 倍](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

PostSlate 的开发者报告在生产边缘设备上使用 ncnn 的 Vulkan 后端进行供应商无关的 GPU 推理，对于 ArcFace 和 SCRFD 等模型实现了相比 CPU 上的 ONNX Runtime 10 倍的加速。 这种方法表明，无需特定供应商的运行时即可实现跨平台 GPU 推理，这对于运行在多样化硬件（NVIDIA、AMD、Intel、Apple Silicon）上且不要求用户安装额外驱动的应用至关重要。 在 NVIDIA RTX 4070 上使用 FP16 时，ArcFace R50 从 30 毫秒（ONNX CPU）降至 3 毫秒（ncnn Vulkan），SCRFD 人脸检测从 25 毫秒降至 2.5 毫秒；模型大小也减半（174 MB ONNX FP32 到 87 MB ncnn FP16）。

reddit · r/MachineLearning · /u/ppchaos · 7月29日 10:22

**背景**: ncnn 是腾讯开发的高性能神经网络推理框架，专为移动和嵌入式平台优化，无第三方依赖。Vulkan 是一种跨平台 GPU API，提供对图形和计算硬件的底层访问，可实现跨不同供应商的高效 ML 推理，无需 CUDA 等专有运行时。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Tencent/ncnn">GitHub - Tencent/ncnn: ncnn is a high-performance neural network inference framework optimized for the mobile platform · GitHub</a></li>
<li><a href="https://www.lei.chat/posts/gpgpu-ml-inference-and-vulkan-compute/">GPGPU, ML Inference, and Vulkan Compute | Lei.Chat()</a></li>
<li><a href="https://developer.nvidia.com/blog/machine-learning-acceleration-vulkan-cooperative-matrices/">Machine Learning Acceleration in Vulkan with Cooperative Matrices | NVIDIA Technical Blog</a></li>

</ul>
</details>

**标签**: `#ML inference`, `#Vulkan`, `#ncnn`, `#edge computing`, `#GPU acceleration`

---

<a id="item-7"></a>
## [Claude 共享对话及 Artifacts 遭谷歌索引](https://thenextweb.com/news/claude-shared-chats-artifacts-google-search-indexed) ⭐️ 8.0/10

上周末，Claude 共享对话及 Artifacts 的链接被谷歌索引，导致医疗记录、公司文件等敏感数据暴露。Anthropic 称这符合设计，但于周一下午阻止了进一步的索引。 这一事件凸显了公开分享对话的 AI 聊天工具用户面临的重大隐私风险，暴露了敏感的个人和企业数据。它影响众多 Claude 用户，削弱了对这类分享功能安全性的信任，可能影响其采用率。 暴露的数据包括医疗记录、儿童信息和公司内部文件。Anthropic 澄清没有系统入侵，因为共享链接由用户生成并发布到公开平台。旧链接仍可访问，但用户可以在设置中撤销已共享的链接。

telegram · zaihuapd · 7月29日 02:40

**背景**: Claude Artifacts 是一项允许用户从对话中生成并共享交互式代码预览和应用程序的功能。共享链接默认是公开可访问的，如果它们被发布到其他公开页面，谷歌等搜索引擎就可以索引这些链接。此前 ChatGPT 和 Grok 也曾发生过类似事件，共享对话被搜索引擎索引。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/Claude_Artifacts">Claude Artifacts</a></li>
<li><a href="https://support.claude.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them">What are artifacts and how do I use them? | Claude Help Center</a></li>

</ul>
</details>

**标签**: `#privacy`, `#security`, `#Claude`, `#AI`, `#data exposure`

---

<a id="item-8"></a>
## [报告称 Hugging Face 被广泛用于生成深度伪造裸照](https://www.theverge.com/ai-artificial-intelligence/971723/hugging-face-nudify-deepfake-undress-women-children) ⭐️ 8.0/10

欧洲非营利组织 AI Forensics 于 2025 年 7 月 28 日发布的报告发现，开源模型平台 Hugging Face 被大量用于制作非自愿深度伪造色情内容，其排名前九的图像编辑模型中有七个能轻易按简单提示为女性“脱衣”。 这凸显了主要 AI 平台上内容审核的关键漏洞，引发了关于滥用开源模型生成虐待内容（包括儿童性虐待材料）的严重伦理与法律担忧。 报告使用蜜罐在 7 天内收到逾 1000 条请求，其中 73%涉性内容，近 7%针对儿童。尽管 Hugging Face 的政策禁止非自愿性内容及未成年人裸露，但平台缺乏主动过滤和输出扫描机制。

telegram · zaihuapd · 7月29日 08:20

**背景**: Hugging Face 是一家美国公司及社区平台，托管超过 10 万个开源机器学习模型和数据集，常被称为“机器学习界的 GitHub”。蜜罐是一种诱饵系统，旨在引诱攻击者，使研究人员在不危及真实系统的情况下观察恶意活动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.kaspersky.com.cn/resource-center/threats/what-is-a-honeypot">什么是蜜罐？蜜罐如何帮助提高安全性</a></li>

</ul>
</details>

**标签**: `#AI伦理`, `#深度伪造`, `#内容审核`, `#Hugging Face`, `#安全`

---

<a id="item-9"></a>
## [月之暗面融资 35 亿美元，估值 350 亿美元](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 8.0/10

月之暗面完成 35 亿美元融资，远超 10-20 亿美元目标，估值达 350 亿美元，其 Kimi K3 模型性能接近 OpenAI 和 Anthropic 的前沿模型。 此次巨额融资凸显了中国对 AI 的持续投入，以及月之暗面作为美国前沿实验室主要竞争对手的崛起。Kimi K3 模型的开源发布可能让尖端 AI 更普及，从而重塑全球 AI 格局。 Kimi K3 模型拥有 2.8 万亿参数，采用名为 KDA 的混合线性注意力机制，支持高达 100 万 tokens 的上下文。模型发布后，月之暗面的日销售额增长了至少 6 倍。

telegram · zaihuapd · 7月29日 10:12

**背景**: 月之暗面是一家总部位于北京的 AI 初创公司，成立于 2023 年，由清华校友创立，以开发 Kimi 聊天机器人和大语言模型而闻名。&\#x27;DeepSeek 时刻&\#x27;指 2025 年 1 月 DeepSeek 发布强大开源模型引发科技股抛售的市场冲击。月之暗面的 Kimi K3 发布引发了类似反应，被称为又一个&\#x27;DeepSeek 时刻&\#x27;。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28AI%29">Kimi (AI) - Wikipedia</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://huggingface.co/blog/ResterChed/kimi-k3-model-overview-mxfp4-quantization-open-wei">Kimi K3 Model Overview: 2.8T Parameters, MXFP4 Quantization, and What the Open Weights Mean for the Community</a></li>

</ul>
</details>

**标签**: `#AI funding`, `#Moonshot AI`, `#Kimi K3`, `#Chinese AI`, `#large language model`

---


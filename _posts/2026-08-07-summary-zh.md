---
layout: default
title: "Horizon Summary: 2026-08-07 (ZH)"
date: 2026-08-07
lang: zh
---

> 从 36 条内容中筛选出 12 条重要资讯。

---

1. [DeepSeek V4 Flash 0731 更新以速度和低成本赢得赞誉](#item-1) ⭐️ 8.0/10
2. [用 Rust 重写 Postgres：pgrust 让分析查询快 300 倍](#item-2) ⭐️ 8.0/10
3. [Cloudflare 推出 Kitesurf：基于 Blitz 的代理优先浏览器，运行于 V8 隔离环境](#item-3) ⭐️ 8.0/10
4. [据报道 2027 年内存产能已售罄，HBM 挤压供应](#item-4) ⭐️ 8.0/10
5. [站长反击爬虫一年：网站 99%流量是机器人](#item-5) ⭐️ 8.0/10
6. [法院责令 Meta 因损害儿童心理健康赔偿 5.67 亿美元](#item-6) ⭐️ 8.0/10
7. [SemiAnalysis：SpaceX 2027 年将建成 10GW AI 算力，微软成为最大承购方](#item-7) ⭐️ 8.0/10
8. [Gemini 遇阻，GCP 却趁势而上](#item-8) ⭐️ 8.0/10
9. [SEC 批准纳斯达克 23 小时交易制，12 月 6 日上线](#item-9) ⭐️ 8.0/10
10. [美国审查中国 AI 企业海外获取英伟达芯片渠道](#item-10) ⭐️ 8.0/10
11. [sub2api 曝 OAuth 高危漏洞，仅凭邮箱可接管账户](#item-11) ⭐️ 8.0/10
12. [OpenAI 称新模型 Astra 或达“关键”网络攻击能力，扩大安全测试](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Flash 0731 更新以速度和低成本赢得赞誉](https://arcprize.org/results/deepseek-v4-flash-0731) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek V4 Flash 的 07/31 更新版本。这是一个效率优化的混合专家（MoE）模型，总参数量 284B、激活参数 13B，支持 1M token 的上下文窗口。社区用户反馈，相比之前的 preview 版本，它在调试、数据分析和日常编程任务上表现有明显提升。 这次发布的意义在于：它把较强的实际能力与极低的成本结合在一起，让普通用户也能负担得起高强度的 LLM 使用。同时，它也说明高效的 MoE 架构加上良好的本地部署支持，能在速度和价格上与昂贵的云端 API 竞争。 该模型已上传到 Hugging Face，并可通过 Ollama 和 OpenRouter 使用；OpenRouter 上还列出了 API 价格和基准测试数据。在本地测试中，有用户在 2 块 RTX Pro 6000 Blackwell 上测得约 8k tok/s 的预填充速度和单流约 250 tok/s 的生成速度；另一名用户表示，开启 5–6 个活跃会话时，每天花费不足 5 美元。

hackernews · tosh · 8月7日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49214008)

**背景**: DeepSeek V4 Flash 是 DeepSeek V4 系列的预览版本，采用混合专家架构：虽然总参数有 284B，但每个 token 只激活 13B 参数，因此推理速度快、成本低。本地推理（local inference）指的是在自己的硬件或本地服务器上运行模型，而不是依赖云端处理，从而获得更低的成本和更高的可控性。0731 版本是一个与早期 preview 不同的更新快照，已被 Oh My Pi、OpenCode Go 等智能体工具采用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://grokipedia.com/page/Local_inference">Local inference</a></li>

</ul>
</details>

**社区讨论**: 讨论整体呈正面：用户称赞该模型的速度、性价比以及调试和文档分析方面的能力，有人称本地 token 吞吐速度是“杀手级特性”。不过，也有少数用户反馈会出现无限循环、不执行工具调用而浪费 token 的问题；讨论中还有一段与主题无关的关于 Claude 账号被封的插曲。

**标签**: `#deepseek`, `#ai`, `#llm`, `#model-release`, `#local-inference`

---

<a id="item-2"></a>
## [用 Rust 重写 Postgres：pgrust 让分析查询快 300 倍](https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/) ⭐️ 8.0/10

一个名为 pgrust 的 Postgres 查询引擎扩展用 Rust 重写了数据库核心，通过批处理、算子融合和 SIMD 指令，声称可将分析查询速度提升高达 300 倍。它与 PostgreSQL 18.3 磁盘兼容。 这一技术挑战了 Postgres 默认的逐行执行器，证明基于 Rust 的重写能为分析工作负载带来巨大加速。它可能推动 Postgres 生态采用向量化执行和自适应规划，惠及需要在 Postgres 上获得更快分析性能的开发者和用户。 作者强调正确性是第一优先级，通过形式化验证和差分模糊测试，已证明 1000 多个用户可见函数与 Postgres 逻辑完全一致。不过，pgrust 尚无稳定的扩展 ABI，现有 PostgreSQL 扩展无法在它上面使用。

hackernews · poly2it · 8月7日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=49208535)

**背景**: Postgres 是流行的开源关系型数据库，使用逐行的火山式查询引擎，处理复杂分析查询时可能较慢。pgrust 是一个用 Rust 重写 Postgres 核心的开源项目，旨在提升性能。批处理（向量化执行）一次处理多行数据，算子融合将多个算子合并以减少开销，SIMD（单指令多数据）允许一条 CPU 指令处理多个数据元素，这些都是现代分析数据库中的成熟技术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/malisper/pgrust">GitHub - malisper/ pgrust : Postgres rewritten in Rust , now faster than...</a></li>
<li><a href="https://dev.to/terminalchai/pgrust-the-open-source-project-rewriting-postgresql-in-rust-4860">pgrust : The Open-Source Project Rewriting PostgreSQL in Rust</a></li>
<li><a href="https://medium.com/@Srini_Data/what-is-simd-and-how-it-supercharges-modern-databases-3964ca7b5149">What Is SIMD and How It Supercharges Modern Databases | by SrinivasanSudharsanan | Medium</a></li>

</ul>
</details>

**社区讨论**: 评论区中，作者强调正确性是第一优先级，并提到对 1000 多个函数做了形式化验证和差分模糊测试。有读者质疑 pgrust 能否被广泛采用，因为用户更信任 Postgres 官方团队；也有读者对自适应规划表示期待。还有人询问 I/O 调度器和噪声邻居问题的处理。

**标签**: `#Postgres`, `#query-engine`, `#performance`, `#SIMD`, `#pgrust`

---

<a id="item-3"></a>
## [Cloudflare 推出 Kitesurf：基于 Blitz 的代理优先浏览器，运行于 V8 隔离环境](https://blog.cloudflare.com/kitesurf/) ⭐️ 8.0/10

Cloudflare 宣布推出 Kitesurf，这是一款专为 AI 代理设计的无状态网络浏览器，可运行在 Cloudflare Workers 的 V8 隔离环境中。Kitesurf 基于开源 Rust 浏览器引擎 Blitz 构建，目标是自动化、网页抓取、测试和内容生成。 Kitesurf 标志着向‘代理优先’基础设施迈出一步，让 AI 代理无需传统浏览器的开销即可大规模浏览网页。同时，它也引发疑问：Cloudflare 将如何让这个对代理友好的产品与现有的反机器人及安全服务协调一致。 与基于 Chromium 的浏览器不同，Kitesurf 基于 Blitz 构建，Blitz 是一个用 Rust 编写的模块化浏览器引擎，目前仍处于 alpha 阶段。该服务是无状态的，并运行在 Cloudflare 的全球 Workers 网络上；Cloudflare 表示 Kitesurf 的补丁将开源并回馈给 Blitz 上游。

hackernews · m3h · 8月7日 10:42 · [社区讨论](https://news.ycombinator.com/item?id=49208393)

**背景**: V8 隔离环境是 V8 JavaScript 引擎的独立实例，常用于 Cloudflare Workers 等无服务器平台，以在多租户场景下提供较强的隔离性。Blitz 是一个开源网络引擎，注重模块化、可嵌入性和 API 灵活性。代理优先浏览器是围绕 AI 代理的需求设计的，优先考虑程序化控制、无状态和可扩展性，而非面向人类的功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/kitesurf/">Introducing Kitesurf: The agent-first browser that runs in V8 isolates on Cloudflare Workers | Cloudflare Blog</a></li>
<li><a href="https://blitz.is/about">Blitz - About</a></li>
<li><a href="https://medium.com/@adityashete009/v8-isolates-for-serverless-functions-a-game-changer-0e8355cf7ac9">V8 isolates for Serverless Functions? A game changer | by Aditya Shete | Medium</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上感兴趣但保持谨慎。Blitz 的作者表示 Cloudflare 打算开源并向上游提交补丁，这一消息获得好评。一些用户对 Cloudflare 同时提供利于抓取的浏览器和反机器人保护表示担忧，另一些人则质疑消费级代理的实际使用场景。

**标签**: `#AI agents`, `#browser`, `#Cloudflare`, `#web scraping`, `#open source`

---

<a id="item-4"></a>
## [据报道 2027 年内存产能已售罄，HBM 挤压供应](https://www.ign.com/articles/ramageddon-continues-another-year-as-2027-memory-capacity-is-reportedly-sold-out) ⭐️ 8.0/10

内存行业报告称，2027 年的内存产能已被全部预订一空，原因是 HBM（高带宽内存）生产占据了不成比例的晶圆供应份额。这限制了包括 DDR5 在内的非 HBM DRAM 在 2027 年前的供应。 这一供应限制意义重大，因为它意味着 DDR5 内存的价格和可用性将在未来数年持续承压，影响 PC 装机者、数据中心和普通消费者。它也凸显了 AI 对 HBM 的需求正在重塑整个内存市场。 在相同技术节点下，HBM3E 生产相同比特数所需的晶圆供应大约是 DDR5 的三倍，因为 3D 堆叠和封装要求使 HBM 裸片更大。先进封装产能同样是一大瓶颈，而不仅仅是晶圆分配问题。

hackernews · inigyou · 8月7日 07:58 · [社区讨论](https://news.ycombinator.com/item?id=49207236)

**背景**: HBM（高带宽内存）是一种 3D 堆叠 DRAM 接口，用于 AI 加速器和高性能显卡，能够提供比标准内存高得多的带宽。它通过在中介层上堆叠 DRAM 裸片来制造，这使得每个 HBM 单元比同等容量的 DDR5 芯片占用更多晶圆面积。由于晶圆产能有限，内存厂商因 HBM 利润率更高而优先生产 HBM，从而限制了 DDR4、DDR5 等非 HBM DRAM 的产出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://blog.partstat.com/semiconductor-storage-hbm-market-shift/">Why High Bandwidth Memory Is Reshaping the Semiconductor Market</a></li>
<li><a href="https://oretonstorage.com/blog/as-hbm-demand-surges-with-ai-growth-ddr-supply-dynamics-are-shifting-we-analyze-wafer-allocation-packaging-bottlenecks-and-dram-pricing-implications">How HBM Production Is Constraining DDR Supply</a></li>

</ul>
</details>

**社区讨论**: 评论者对内存价格上涨表示不满，有人提到近期以高价购买 DDR4，以及零售商可能因涨价而取消订单。还有人讨论为嵌入式项目囤积内存，建议制定类似 USB 的通用内存条标准，并表达了对采用 AI 的犹豫，因为 AI 给内存和存储带来了巨大压力。

**标签**: `#hardware`, `#memory`, `#HBM`, `#supply-chain`, `#AI`

---

<a id="item-5"></a>
## [站长反击爬虫一年：网站 99%流量是机器人](https://patronview.com/news/99-percent-of-my-website-traffic-is-bots/) ⭐️ 8.0/10

一个拥有 150 万页面的网站站长报告称，其网站 99%的流量来自机器人和爬虫，并讲述了为期一年的对抗过程。某个月的账单飙升约 500%，主要与 Cloudflare D1 成本有关。 这一事件凸显了机器人流量给网站运营者带来的日益沉重的负担，既推高成本又扭曲数据统计。社区讨论还暴露出对 Cloudflare 等大公司掌控访问权限的担忧，以及 AI 爬虫无偿抓取网站价值的公平性问题。 该网站正常月账单约为 90 美元，但某次异常飙升月涨了约 500%，部分与 Cloudflare D1 成本有关。缓解手段包括 Anubis 等工作量证明系统；作者也承认自己的网站本身就抓取公开文档，并指出其中的讽刺意味。

hackernews · petercooper · 8月7日 14:51 · [社区讨论](https://news.ycombinator.com/item?id=49211386)

**背景**: 机器人和爬虫是自动访问网站并提取数据的程序，会消耗大量带宽并扭曲流量统计。许多站长借助 CDN 和 Cloudflare 等机器人管理服务过滤恶意流量，但这意味着把访问控制权交给第三方。Anubis 等工作量证明方案则通过要求客户端完成计算难题来验证真实浏览器，提供了另一种思路。

**社区讨论**: 评论者担忧开放网络和 Cloudflare 依赖；jwr 警告说，把访问决策外包给大公司会让用户被无声屏蔽且无处申诉。还有人分享了 Anubis 等工作量证明方案；一位用户称 Claude 搜索机器人 72 小时内抓取了约 20.5 万个页面却只带来 1 个推荐，感到吃亏。也有人建议站长放弃 D1、改做静态网站以节省开支。

**标签**: `#bots`, `#scraping`, `#cloudflare`, `#web performance`, `#security`

---

<a id="item-6"></a>
## [法院责令 Meta 因损害儿童心理健康赔偿 5.67 亿美元](https://www.theguardian.com/technology/2026/aug/06/new-mexico-court-meta) ⭐️ 8.0/10

2026 年 8 月 6 日，新墨西哥州法院裁定 Meta 支付 5.67 亿美元，以解决对儿童心理健康的伤害，并认定该公司违反了该州的公共妨害法。判决还要求 Meta 对未成年用户做出改变。 这项具有里程碑意义的裁决标志着社交媒体平台在青少年心理健康问题上承担的法律责任日益增加，可能会鼓励美国各地提起类似诉讼。它可能迫使主要平台重新设计面向未成年人的算法和安全功能，并对整个行业产生财务和监管影响。 该案依据新墨西哥州公共妨害法（NMSA 1978 § 30-8-1）提起，5.67 亿美元款项将用于青少年心理健康基金。社区评论者指出，对于一个仅有约 200 万人口的州来说，这笔金额相当巨大；同时也有报道提到更高的 9.42 亿美元总额。

hackernews · boplicity · 8月7日 00:06 · [社区讨论](https://news.ycombinator.com/item?id=49204352)

**背景**: 包括 Instagram 和 TikTok 在内的社交媒体平台因对年轻用户心理健康的影响（包括成瘾性设计和有害内容）而受到越来越多的审查。此案是美国各州针对科技公司提起的更广泛诉讼浪潮的一部分，这些诉讼指控科技公司违反了公共妨害法。新墨西哥州的裁决可能为法院如何处理州法律下的此类伤害开创先例，并可能影响未来的立法和平台政策。

**社区讨论**: 评论者普遍认为，对于人口稀少的新墨西哥州来说，这笔罚款意义重大，但也有人嘲笑这与 Meta 的全球收入相比只是“轻轻拍了一下手腕”。还有人指出了被违反的具体法律，并警告成瘾算法对年轻心灵的危害更大，同时对如果更多地方限制儿童使用社交媒体，该公司的未来收入表示担忧。

**标签**: `#Meta`, `#social media`, `#mental health`, `#legal ruling`, `#regulation`

---

<a id="item-7"></a>
## [SemiAnalysis：SpaceX 2027 年将建成 10GW AI 算力，微软成为最大承购方](https://newsletter.semianalysis.com/p/spacex-10gw-in-2027-why-its-real) ⭐️ 8.0/10

SemiAnalysis 的报告称，SpaceX 将在 2027 年前实际建成 10GW 的 AI 算力，并带来高达 3000 亿美元的年经常性收入，而微软的 Azure 将是最大的承购方。该报告将这一预测与每年每 GW 产生 1000 亿美元的 AI 推理经济相联系。 如果实现，SpaceX 将在 AI 基础设施领域占据主导地位，并使微软 Azure 实现三位数增长。这突显出 AI 算力竞赛的紧迫性，推理需求已超过当前供应商的供应能力。 这一预测假设推理收入达到每年每 GW1000 亿美元，并以微软 2026 年的&\#x27;10GW 觉醒&\#x27;为催化剂。文章强调了 SpaceX 独特的建设速度，但未具体说明实现该容量所采用的技术（如太阳能、储能或数据中心设计）。

rss · Semianalysis · 8月7日 20:08

**背景**: 承购方（offtaker）是能源或基础设施合同中的大型买家，通常长期承诺购买产出。微软一直在快速扩张自己的数据中心容量——其最大的园区通常运行在 500MW 至 1GW 之间——因此向 SpaceX 承诺 10GW 将是一个战略性的跨越。文章中提到的&\#x27;每 GW 每年 1000 亿美元推理收入&\#x27;反映了行业的新看法：AI 推理将成为主导的变现模式，每 GW 算力可产生巨额收入。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.genieai.co/en-us/define/offtaker">Offtaker definition and meaning | GenieAI</a></li>
<li><a href="https://www.techbuzz.ai/articles/softbank-bets-10b-on-france-with-3-1-gw-ai-data-center-push">SoftBank Bets $10B+ on France with 3.1 GW AI Data Center Push</a></li>
<li><a href="https://euroweeklytimes.com/technology/powering-the-future-ai-boom-creates-11000-datacenters-and-720bn-grid-bill/">Powering the Future: AI Boom Creates 11,000 Datacenters and...</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#AI infrastructure`, `#Energy`, `#Microsoft`, `#Semiconductor analysis`

---

<a id="item-8"></a>
## [Gemini 遇阻，GCP 却趁势而上](https://newsletter.semianalysis.com/p/gemini-is-cooked-but-gcp-is-cooking) ⭐️ 8.0/10

这篇 SemiAnalysis 通讯分析指出，谷歌的 Gemini AI 模型在 DeepMind 面临长期战略挫败，而谷歌云平台（GCP）却在短期内获得商业增长。分析强调，Alphabet 内部 DeepMind 的 AI 研究困境与 GCP 的云业务势头之间正出现日益明显的分化。 这一观点之所以重要，是因为它挑战了“谷歌 AI 未来完全取决于 Gemini 成败”的普遍假设，暗示 GCP 稳健的企业云增长可能成为更强劲的短期驱动因素。同时，它凸显了云基础设施需求正与前沿模型领先地位脱钩的趋势。 这篇文章的副标题为“为什么 DeepMind 的长期失败正是 GCP 的短期收益”，指出即使 Gemini 在基准测试中面临质疑，企业客户仍纷纷转向 GCP 使用其基础设施和 AI 服务。文章聚焦谷歌内部的组织动态，而非具体的模型基准或收入数据。

rss · Semianalysis · 8月7日 02:32

**背景**: Gemini 是谷歌 DeepMind 开发的多模态大语言模型系列，于 2023 年 12 月 6 日发布。谷歌云平台（GCP）是谷歌的云计算服务，为企业提供基础设施、存储和 AI 服务。DeepMind 是一家英美 AI 研究实验室，2014 年被谷歌收购，现为 Alphabet Inc.的子公司。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Gemini_%28language_model%29">Gemini (language model ) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Google_DeepMind">Google DeepMind - Wikipedia</a></li>
<li><a href="https://www.techtarget.com/searchcloudcomputing/definition/Google-Cloud-Platform">What is Google Cloud ? | Definition from TechTarget</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google`, `#GCP`, `#Cloud Computing`, `#Industry Analysis`

---

<a id="item-9"></a>
## [SEC 批准纳斯达克 23 小时交易制，12 月 6 日上线](https://finance.sina.com.cn/stock/bxjj/2026-08-07/doc-inimnkup0012339.shtml) ⭐️ 8.0/10

美国 SEC 已批准纳斯达克实施 23/5 交易制度，即每天 21:00 至次日 20:00 连续交易，仅留 1 小时（美东时间 20:00-21:00）进行系统维护。该制度将于 2026 年 12 月 6 日正式生效。 这标志着美国主要交易所首次实行完整的 23 小时交易制度，将从根本上改变市场基础设施与交易行为。该举措紧随 NYSE Arca 和 Cboe 的类似提案，将对交易所、券商、流动性提供商和投资者产生深远影响。 美东时间每天 20:00 至 21:00 将休市 1 小时，用于系统清算和数据处理。目前隔夜交易流动性较薄、价差较大；SEC 将于 9 月 17 日举办圆桌会议，讨论投资者保护等议题。

telegram · zaihuapd · 8月7日 10:03

**背景**: 长期以来，美股市场仅在工作日美东时间 9:30 至 16:00 进行常规交易，并有限定时间的盘前和盘后时段。近年来，散户投资者已通过 Blue Ocean ATS 等另类交易系统（ATS）获得隔夜交易渠道，Robinhood、嘉信理财等平台也提供延长时段服务。ATS 是受 SEC 监管的计算机化交易场所，用于撮合传统交易所之外的证券买卖订单。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tradinghours.com/markets/nasdaq">NASDAQ Market Hours &amp; Holidays 2026 - 2028 - TradingHours.com</a></li>
<li><a href="https://corporatefinanceinstitute.com/resources/equities/alternative-trading-system-ats/">Alternative Trading System ( ATS ) - Definition , Examples</a></li>
<li><a href="https://www.linkedin.com/pulse/235-trading-dismantling-manufactured-narrative-failure-gary-fischer-hface">23 / 5 Trading : Dismantling the Manufactured Narrative of Inevitable...</a></li>

</ul>
</details>

**标签**: `#SEC`, `#Nasdaq`, `#trading-hours`, `#market-infrastructure`, `#finance`

---

<a id="item-10"></a>
## [美国审查中国 AI 企业海外获取英伟达芯片渠道](https://www.bloomberg.com/news/articles/2026-08-07/us-reviews-china-s-offshore-access-to-nvidia-chips-after-ai-breakthroughs) ⭐️ 8.0/10

美国商务部工业与安全局（BIS）正在系统性地调查中国 AI 企业如何在海外获取并使用英伟达芯片，包括通过租用其他国家算力的远程云计算方式。这项审查是在月之暗面发布 Kimi K3 模型、以及一名白宫高官公开指控其非法获取芯片之后启动的。 此举可能重塑美国的出口管制和云计算监管规则，直接影响中国 AI 企业获取先进算力的方式。同时，它也加剧了中美科技竞争，并可能与反对进一步限制云端芯片访问的英伟达产生冲突。 据报道，BIS 正在整理两份国家名单：一份是涉嫌将受限芯片走私进入中国的黑市所在地，另一份是中国企业远程租用芯片的国家。美国众议院已通过一项两党法案，拟明确授权 BIS 限制此类云计算协议，预计会遭到英伟达反对；彭博社还报道称，阿里巴巴通过新加坡壳公司控制的实体，经正被美方调查的 Megaspeed 使用了位于马来西亚的英伟达芯片。

telegram · zaihuapd · 8月7日 11:18

**背景**: 美国长期以来限制向中国出口先进的英伟达芯片，但中国 AI 企业通过黑市和远程租用他国算力等方式寻求规避。Kimi K3 是月之暗面发布的旗舰开源权重大型语言模型，据称有 2.8 万亿参数，其性能逼近美国模型，使得这些规避渠道受到关注。远程访问芯片本身并不违法，因此新立法试图明确 BIS 对此类安排的管辖权。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3">moonshotai/ Kimi - K 3 · Hugging Face</a></li>
<li><a href="https://www.eigent.ai/blog/kimi-k3-open-weight-frontier-model">Kimi K 3 : Moonshot AI &#x27;s 2.8T Open-Weight Model</a></li>
<li><a href="https://modal.com/library/moonshot/kimi-k3">Kimi K 3 by Moonshot AI | Model Library | Modal</a></li>

</ul>
</details>

**标签**: `#AI`, `#semiconductors`, `#export-controls`, `#China`, `#US-policy`

---

<a id="item-11"></a>
## [sub2api 曝 OAuth 高危漏洞，仅凭邮箱可接管账户](https://github.com/Wei-Shaw/sub2api/issues/5350) ⭐️ 8.0/10

sub2api v0.1.171 及之前版本存在一个 CVSS 8.8 的严重 OAuth 账户接管漏洞。攻击者仅需知道受害者的注册邮箱，无需密码、验证码或任何用户交互，就能将自己的 OAuth 身份绑定到受害者账户。 该漏洞使攻击者能够完全控制受害者的 API 密钥、账单余额和订阅配额，可能导致数据窃取和经济损失。由于 sub2api 是用于统一多个 AI 订阅的开源代理，受影响用户范围较广，应立即更新修复。 该缺陷位于 pending session（待处理会话）流程中，existingUser 分支在绑定 OAuth 身份前未校验用户密码或验证码。此后，攻击者的每次 OAuth 登录都会解析为受害者账户，从而实现持久的账户接管。

telegram · zaihuapd · 8月7日 14:59

**背景**: sub2api 是一个托管在 GitHub 上的开源 AI API 代理，用于统一 Claude、OpenAI、Gemini 和 Antigravity 的订阅。OAuth 是一种广泛使用的授权协议，允许用户在不共享密码的情况下向第三方授予资源访问权限。在此漏洞中，会话绑定步骤缺少凭证校验，使攻击者能够将自己的 OAuth 身份关联到其他用户的账户，从而导致完全接管账户。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/Sub2API">Sub2API</a></li>
<li><a href="https://www.sub2api.com/">Sub 2 API - AI API Gateway</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#OAuth`, `#account-takeover`, `#sub2api`

---

<a id="item-12"></a>
## [OpenAI 称新模型 Astra 或达“关键”网络攻击能力，扩大安全测试](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/) ⭐️ 8.0/10

OpenAI 于 2026 年 8 月 7 日披露，其即将推出的 Astra 模型在内部评估中显示出代理编码与网络安全方面的重大进展，初步结果强到无法排除达到“关键”网络能力阈值的可能性。公司已暂停不符合强化安全要求的 Astra 相关内部活动，并将与政府机构和 AI 安全组织合作开展第三方测试。 此事意义重大，因为这是 OpenAI 首次公开警示其前沿模型可能接近“关键”自主网络攻击能力阈值，对发布节奏、AI 监管和全球网络安全风险都有重要影响。若该能力成为现实，模型将能在无人干预的情况下发现并利用加固真实系统中的零日漏洞。 根据 OpenAI 的预备框架，“关键”网络安全阈值意味着模型可在无需人工干预的情况下，自主发现并利用多种加固真实关键系统中所有严重级别的功能性零日漏洞，或仅凭高层目标规划并执行端到端的新型网络攻击。此前 GPT-5.6-Sol 等模型在同一评估中仅被评为“高”；OpenAI 正在实施隔离测试环境、加密增强、通用监控等管控措施。

telegram · zaihuapd · 8月7日 16:44

**背景**: OpenAI 的预备框架是一套安全与治理流程，通过定义“高”“关键”等能力阈值来指导部署决策。代理编码指 AI 系统在最少人工干预下自主规划、编写、测试和修改代码，而 AI 红队测试是一种在攻击者利用之前发现 AI 系统漏洞的结构化对抗性测试过程。这一新闻反映出前沿实验室在发布强大模型前进行更严格安全评估并引入外部测试的行业趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/">Responding to the next frontier of critical cyber capabilities | OpenAI</a></li>
<li><a href="https://openai.com/index/updating-our-preparedness-framework/">Our updated Preparedness Framework | OpenAI</a></li>
<li><a href="https://cloud.google.com/discover/what-is-agentic-coding">What is agentic coding? How it works and use cases | Google Cloud</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#OpenAI`, `#Cybersecurity`, `#Frontier models`, `#AI regulation`

---
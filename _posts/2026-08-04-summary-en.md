---
layout: default
title: "Horizon Summary: 2026-08-04 (EN)"
date: 2026-08-04
lang: en
---

> From 38 items, 10 important content pieces were selected

---

1. [Keyv and related npm packages compromised in active Shai-Hulud supply chain attack](#item-1) ⭐️ 9.0/10
2. [Google Builds $200B Wall Street Financing Machine for Anthropic](#item-2) ⭐️ 9.0/10
3. [Custom Color Space and Algorithm for Diverse Skin Tones](#item-3) ⭐️ 8.0/10
4. [DeepSeek V4 Flash Runs on a Single AMD MI300X](#item-4) ⭐️ 8.0/10
5. [FedEx Phishing-Like Emails Show Why Users Keep Falling for Scams](#item-5) ⭐️ 8.0/10
6. [Oxide Computer Raises $445M in Series D Funding Round](#item-6) ⭐️ 8.0/10
7. [Xbox Outage Blocks Disc Games, Reigniting Digital Ownership Debate](#item-7) ⭐️ 8.0/10
8. [PipeNetwork&\#x27;s MLX Port Brings MiniMax-H3 Video Generation to Apple Silicon](#item-8) ⭐️ 8.0/10
9. [China Issues First Mandatory National Standard for L3/L4 Autonomous Driving](#item-9) ⭐️ 8.0/10
10. [White House Reverses on Open-Source AI Rules, Splitting Silicon Valley](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Keyv and related npm packages compromised in active Shai-Hulud supply chain attack](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 9.0/10

A self-replicating worm named Shai-Hulud is actively compromising the Keyv npm package and its related dependencies, along with hundreds of other packages in the npm ecosystem. The attack is ongoing and has triggered urgent security warnings from researchers and government agencies. This attack targets widely used open-source packages like Keyv, which has hundreds of downstream dependents, meaning the compromise could cascade across countless applications. It underscores the systemic fragility of the npm dependency chain and the urgent need for better supply-chain security practices. Over 500 packages have been compromised by the worm, which spreads via pre-install hooks and automated credential harvesting. The attack also leverages compromised maintainer accounts to publish malicious updates, making detection difficult without behavioral analysis.

hackernews · cimi\_ · Aug 4, 11:01 · [Discussion](https://news.ycombinator.com/item?id=49166874)

**Background**: The npm registry is the default package manager for JavaScript and Node.js, and supply chain attacks against it are becoming increasingly common. Shai-Hulud is a self-propagating worm that compromises packages to steal credentials and spread malicious code, representing a significant evolution from traditional single-use payload attacks.

<details><summary>References</summary>
<ul>
<li><a href="https://unit42.paloaltonetworks.com/npm-supply-chain-attack/">&quot;Shai-Hulud&quot; Worm Compromises npm Ecosystem in Supply Chain Attack (Updated November 26)</a></li>
<li><a href="https://www.cisa.gov/news-events/alerts/2025/09/23/widespread-supply-chain-compromise-impacting-npm-ecosystem">Widespread Supply Chain Compromise Impacting npm Ecosystem | CISA</a></li>
<li><a href="https://www.trendmicro.com/en_us/research/25/i/npm-supply-chain-attack.html">What We Know About the NPM Supply Chain Attack | Trend Micro (US)</a></li>

</ul>
</details>

**Discussion**: Community members debated mitigations, with one proposing a tool called Packj that uses static and dynamic analysis to detect indicators of compromise. Others suggested using devcontainers for isolation, called for a moratorium on pre-install hooks, and expressed frustration over the fragile dependency system, while another questioned why GitHub couldn&\#x27;t automatically block the attacker&\#x27;s exfiltration repositories.

**Tags**: `#security`, `#supply-chain attack`, `#npm`, `#open-source`, `#dependency management`

---

<a id="item-2"></a>
## [Google Builds $200B Wall Street Financing Machine for Anthropic](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 9.0/10

Google has quietly assembled a roughly $200 billion infrastructure financing structure to deliver over $150 billion in AI chips to Anthropic, with Broadcom, Apollo, Blackstone, Morgan Stanley, and crypto miners as participants. In June 2026, the special-purpose vehicle Compute SPV completed its first deals, buying about $35 billion in hardware — around 1 gigawatt of compute and 1 million TPUs. This is one of the largest infrastructure financing arrangements ever built, and it could reshape how AI compute is funded by moving hundreds of billions in hardware off corporate balance sheets. The risk-sharing model may become a template for other AI companies lacking credit ratings. Total contracts are worth roughly $200 billion, with about 80% directly tied to chips. Unlike a traditional loan, the structure resembles project financing: Google guarantees data centers, Broadcom buys and helps finance chips, while Apollo and Blackstone purchase hardware and lease it back to Anthropic.

telegram · zaihuapd · Aug 4, 10:52

**Background**: Anthropic has no credit rating, so lenders need risk mitigation. The financing uses a special-purpose vehicle \(SPV\) that buys chips and related equipment, then leases computing capacity to the AI company; lenders finance the assets against long-term customer commitments. This &\#x27;vendor financing&\#x27; model, borrowed from Boeing and GE&\#x27;s practice of marketing aircraft and engines, lets parties avoid putting hundreds of billions in AI hardware on their own balance sheets. Analysts have also flagged &\#x27;circular financing&\#x27; in AI, where chipmakers and cloud providers invest in startups that use the funds to buy their products.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techtimes.com/articles/318207/20260611/anthropic-ai-safety-warning-meets-35b-compute-deal-silicon-valley-cannot-slow-alone.htm">Anthropic AI Safety Warning Meets $35B Compute Deal: Silicon Valley...</a></li>
<li><a href="https://finance.biggo.com/news/cc3ceaa8-e838-4501-b4c0-13b9fcba9232">Google Orchestrates $200 Billion AI Chip Financing Network in Landmark Infrastructure Deal — BigGo Finance</a></li>
<li><a href="https://blockeden.xyz/blog/2026/03/06/ai-circular-financing-loop-vendor-financing/">The Great AI Circular Financing Loop: When Vendors Fund Their Own Customers - BlockEden.xyz</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#Google`, `#Anthropic`, `#financing`, `#cloud computing`

---

<a id="item-3"></a>
## [Custom Color Space and Algorithm for Diverse Skin Tones](https://toneyalexander.github.io/inclusive-color-space/) ⭐️ 8.0/10

The developer released an interactive web page introducing a simple algorithm and a custom color space for procedurally generating diverse, plausible skin tones for digital art and game development. The project includes a color picker, demos, and detailed explanations of the math. Skin tone selection is often difficult and color spaces like RGB are not intuitive for this task. This approach could make inclusive character creation easier and spark further work on skin-tone-aware color tools. The author notes the methodology is &\#x27;a bit shaky&\#x27; and outlines future work, suggesting the current space is a good-enough approximation rather than a definitive model. The implementation uses function fitting and equation-based transforms on top of the RGB color space.

hackernews · automatoney · Aug 4, 15:16 · [Discussion](https://news.ycombinator.com/item?id=49170165)

**Background**: A color space defines how colors are represented numerically; RGB is common but not perceptually uniform or well-suited for skin tones. This project constructs a simplified skin-tone color space by analyzing a range of RGB colors that look like plausible human skin, and provides equations and demos. The goal is to cover the broadest inclusive range of plausible but simplified skin tones.

<details><summary>References</summary>
<ul>
<li><a href="https://toneyalexander.github.io/inclusive-color-space/">What Colors Are We? Constructing A Color Space For Skin Tones</a></li>

</ul>
</details>

**Discussion**: Commenters reacted positively, praising the presentation and the idea of fitting functions to skin-tone data. Some noted the shape matches data from makeup shades plotted in Oklab, while others pointed out references like Pantone Skin Tones and observed that some generated colors appear slightly green, blue, or purple.

**Tags**: `#color-science`, `#procedural-generation`, `#digital-art`, `#color-space`, `#skin-tones`

---

<a id="item-4"></a>
## [DeepSeek V4 Flash Runs on a Single AMD MI300X](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

A GitHub project demonstrates running DeepSeek V4 Flash on a single AMD MI300X GPU at roughly 150 tokens per second while preserving the model&\#x27;s full intended weights. It achieves this by trading the original 1M-token context window for a 256k-token one. This is a significant hardware optimization because it shows that a 284B-parameter MoE model \(with 13B active parameters\) can run efficiently on a single accelerator, lowering the hardware barrier for local or cost-sensitive deployment. It also highlights AMD MI300X&\#x27;s large HBM capacity and bandwidth as a competitive option for large-model inference, challenging Nvidia&\#x27;s dominance. The project preserves the model&\#x27;s full intended weights \(MXFP4\) rather than applying additional quantization, with the main tradeoff being context length, reduced from 1M to 256k tokens. The MI300X is an OAM module typically sold in 8-GPU server boxes, not as a standalone PCIe card, and a related 2xMI300X implementation is referenced in the project&\#x27;s prior-art section.

hackernews · zhoutong · Aug 4, 10:00 · [Discussion](https://news.ycombinator.com/item?id=49166386)

**Background**: DeepSeek V4 Flash is a preview of the DeepSeek V4 series: a Mixture-of-Experts model with 284B total parameters and 13B activated, designed for efficient reasoning across a 1M-token context window. AMD MI300X is a data-center GPU with 192GB of HBM3 memory, positioned against Nvidia&\#x27;s data-center accelerators; running large MoE models on a single such GPU requires careful memory and context management. Utilities like Ollama and Hugging Face now list DeepSeek V4 Flash, which helps make it accessible for local experiments.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://ollama.com/library/deepseek-v4-flash">deepseek - v 4 - flash</a></li>
<li><a href="https://en.wikipedia.org/wiki/Amd_MI300X">Amd MI300X</a></li>

</ul>
</details>

**Discussion**: Commenters generally praised the work but raised practical caveats: a single MI300X cannot be bought as a standalone card \(it ships in ~€250K 8-GPU racks\), and the prior-art section misses DwarfStar, which reportedly runs the same model in less memory. Others noted that the 256k context loss is a reasonable tradeoff, comparable to models like Codex, and that DeepSeek V4 Flash should also fit into the 144GB of the future PCIe-based MI350P.

**Tags**: `#DeepSeek`, `#AMD MI300X`, `#LLM inference`, `#quantization`, `#hardware`

---

<a id="item-5"></a>
## [FedEx Phishing-Like Emails Show Why Users Keep Falling for Scams](https://www.troyhunt.com/thanks-fedex-this-is-why-we-keep-getting-phished/) ⭐️ 8.0/10

Security researcher Troy Hunt published a post explaining how legitimate companies like FedEx send emails that mimic phishing patterns, such as customs notices with PDF attachments from individual senders. These practices blur the line between genuine correspondence and scam messages. When trusted brands model their emails on scam-like patterns, users&\#x27; ability to distinguish phishing from legitimate messages is eroded. This makes real phishing attacks more effective and undermines years of security awareness training. Commenters cited concrete examples: a FedEx customs notice sent by &quot;some guy&quot; with a PDF, a Google storage alert using the shortened domain c.gle, and the IRS using commercially available text-to-speech in phone trees. These cases show that attackers can easily replicate the same look and feel without needing advanced techniques.

hackernews · stymaar · Aug 4, 21:09 · [Discussion](https://news.ycombinator.com/item?id=49175192)

**Background**: Phishing is a form of social engineering where attackers disguise fraudulent messages as legitimate communications to steal credentials or data. Email authentication standards such as SPF, DKIM, and DMARC help receiving servers verify that a message genuinely comes from the declared domain, while BIMI allows brands to display verified logos in supported email clients. However, these protections only help if companies consistently follow secure sending practices; when legitimate senders behave like phishers, users cannot rely on familiar cues.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cloudflare.com/learning/email-security/dmarc-dkim-spf/">What are DMARC, DKIM, and SPF?</a></li>
<li><a href="https://en.wikipedia.org/wiki/Brand_Indicators_for_Message_Identification">Brand Indicators for Message Identification - Wikipedia</a></li>
<li><a href="https://bimigroup.org/">Home - BIMI Group</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed with the author, sharing their own examples: one person reported a genuine FedEx customs notice that looked like a scam, another questioned the legitimacy of Google&\#x27;s c.gle link, and others pointed to IRS phone systems and the proliferation of cheap generic top-level domains. The overall sentiment was frustration that legitimate organizations add to the confusion instead of making their communications easier to verify.

**Tags**: `#phishing`, `#security`, `#email`, `#cybersecurity`, `#FedEx`

---

<a id="item-6"></a>
## [Oxide Computer Raises $445M in Series D Funding Round](https://www.sec.gov/Archives/edgar/data/1795071/000179507126000002/xslFormDX01/primary_doc.xml) ⭐️ 8.0/10

Oxide Computer has raised $445 million in a Series D round, according to a recent SEC Form D filing. This marks the company&\#x27;s largest funding round to date, following a $200 million Series C reported earlier in 2026. This substantial round signals strong investor confidence in Oxide&\#x27;s mission to challenge conventional cloud infrastructure with cloud-native hardware. The funding could help the company scale production and sales, giving enterprises a new alternative to dominant hyperscaler clouds. The SEC Form D filing indicates a Regulation D exempt offering, and the form itself does not disclose valuation or detailed investor information. Commenters cite Oxide&\#x27;s prior fundraising history as a $44 million Series A in 2023, a $100 million Series B in 2025, and a $200 million Series C in 2026, making the $445 million Series D a significant step up.

hackernews · depr · Aug 4, 20:13 · [Discussion](https://news.ycombinator.com/item?id=49174407)

**Background**: Oxide Computer is a startup focused on cloud-native hardware, aiming to rethink how companies purchase and operate cloud infrastructure. Form D is a notice filed with the U.S. SEC for exempt securities offerings under Regulation D, and it is submitted through the SEC&\#x27;s EDGAR electronic system. The cloud-native approach typically uses containerized microservices so applications can run across different environments.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sec.gov/resources-small-businesses/capital-raising-building-blocks/what-form-d">What is Form D? - SEC.gov</a></li>
<li><a href="https://en.wikipedia.org/wiki/Form_D">Form D - Wikipedia</a></li>
<li><a href="https://aws.amazon.com/what-is/cloud-native/">What is Cloud Native? - Cloud Native Architecture Explained - AWS</a></li>

</ul>
</details>

**Discussion**: Community sentiment is largely positive: users cheered the news and praised Jessie Frazelle&\#x27;s involvement, with one saying they trust anything she works on. However, an engineering VP said their sales inquiry was never acknowledged despite spending about $900,000 per year on AWS. Another commenter questioned whether Oxide actually ships hardware to customers, since they have not seen real deployments.

**Tags**: `#funding`, `#hardware`, `#cloud-computing`, `#infrastructure`, `#oxide-computer`

---

<a id="item-7"></a>
## [Xbox Outage Blocks Disc Games, Reigniting Digital Ownership Debate](https://birchtree.me/blog/xbox-goes-down-you-cant-play-games-you-own-on-disc/) ⭐️ 8.0/10

A major Xbox outage prevented users from playing games they own on physical discs, because Microsoft&\#x27;s server-side license verification was unreachable. Microsoft has acknowledged the problem and said it will change its licensing system so disc games are not blocked during server outages or offline play. This incident demonstrates that even physical game discs are entangled with DRM and online infrastructure, undercutting the idea of true ownership. It strengthens arguments that gamers should receive stronger rights to access, preserve, and resell the software they buy. Microsoft acknowledged that disc-based games undergo license verification, but said such verification should not prevent access during server issues or offline. The company is preparing a fix and says it will change the licensing system after the widely reported outage.

hackernews · surprisetalk · Aug 4, 12:01 · [Discussion](https://news.ycombinator.com/item?id=49167448)

**Background**: Always-online DRM requires consumers to maintain a connection to a server before they can use a product, often to verify licenses. Microsoft has pushed digital distribution heavily for Xbox, and even disc-based games now rely on online license checks. This practice has long been controversial because it introduces a single point of failure and forces legitimate owners to depend on server availability.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Always-online_DRM">Always-online DRM</a></li>
<li><a href="https://ixbt.games/en/news/2026/07/30/425735-xbox-izmenit-sistemu-licenzii-posle-skandala-s-nedostupnymi-igrami.html">Xbox to Change Licensing System After Inaccessible Games Scandal</a></li>

</ul>
</details>

**Discussion**: Commenters expressed frustration at the fragility of modern gaming, contrasting it with older consoles like the GameCube and PS3 where games worked offline and via LAN. They argued the real issue is ownership, not physical versus digital, and called for rights to keep, back up, resell, and pass on games. Some also criticized Xbox&\#x27;s online login requirements even in titles such as the Master Chief Collection.

**Tags**: `#Xbox`, `#DRM`, `#digital-ownership`, `#gaming`, `#outage`

---

<a id="item-8"></a>
## [PipeNetwork&\#x27;s MLX Port Brings MiniMax-H3 Video Generation to Apple Silicon](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

Simon Willison demonstrates PipeNetwork/minimax-h3-mlx, an MLX port of MiniMax&\#x27;s omni-modal MiniMax-H3 model, running on his M5 Max MacBook Pro. He generated a 15-second video clip from a text prompt, with model downloads around 115 GB and generation taking under 45 minutes. This makes a frontier open-weights omni-modal video model practical on commodity Apple hardware, reducing reliance on cloud GPU clusters. It also highlights MLX&\#x27;s growing ecosystem as a viable path for running large generative models locally on Apple Silicon. The MLX port uses an 8-bit quantized version of MiniMax-H3 and pairs it with the FL2VA component from the original model. Willison notes the generated audio was speech-like garbage because he did not follow MiniMax&\#x27;s video prompting guide, which contains guidance for controlling audio output.

rss · Simon Willison · Aug 4, 19:10

**Background**: MiniMax-H3 is a general-purpose omni-modal generative system that accepts text, images, audio, and video, and can generate up to 15-second video clips with native audio in a single pass. MLX is Apple&\#x27;s open-source array framework designed for machine learning on Apple silicon, taking advantage of its unified memory architecture. This project ports MiniMax-H3 to MLX, enabling the model to run locally on Apple hardware rather than on remote servers.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple ...</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between ...</a></li>
<li><a href="https://fal.ai/minimax-h3">MiniMax H3 - Open-Weights General-Purpose Multimodal Video ...</a></li>

</ul>
</details>

**Tags**: `#MLX`, `#MiniMax-H3`, `#video generation`, `#Apple Silicon`, `#open source`

---

<a id="item-9"></a>
## [China Issues First Mandatory National Standard for L3/L4 Autonomous Driving](https://wap.miit.gov.cn/jgsj/zbys/qcgy/art/2026/art_a1d2072374884287b67048a77560014e.html) ⭐️ 8.0/10

On July 30, 2026, China&\#x27;s Ministry of Industry and Information Technology \(MIIT\) published GB 44721—2026, &\#x27;Safety Requirements for Autonomous Driving Systems of Intelligent Connected Vehicles&\#x27; — the country&\#x27;s first mandatory national standard for L3 and L4 autonomous driving. The standard will take effect on July 1, 2027. This transforms autonomous-driving safety rules from voluntary recommendations into legal requirements, setting a minimum safety bar that all L3/L4 vehicles must meet to enter the Chinese market. It will reshape the development and approval process for automakers, suppliers, and technology companies building higher-level autonomous driving systems in the world&\#x27;s largest auto market. The standard applies to M-class \(passenger\) and N-class \(truck\) vehicles equipped with L3 or L4 systems, but excludes automatic parking systems. It upgrades a 2024 recommended standard into a mandatory one, covering four dimensions: enterprise life-cycle safety assurance, dynamic driving capability, human-machine interaction and user notification, and multi-dimensional inspection and testing; L3 systems must also have driver takeover capability monitoring.

telegram · zaihuapd · Aug 4, 13:06

**Background**: In China, national standards come in two types: mandatory standards \(GB, no &\#x27;T&\#x27;\) and recommended standards \(GB/T\). Mandatory standards must be followed by law, while recommended ones are voluntary. L3 \(conditional\) and L4 \(highly automated\) driving are the two highest levels of autonomous driving defined by SAE, where the system handles most driving tasks but may still require a human driver to intervene in certain situations.

<details><summary>References</summary>
<ul>
<li><a href="http://www.ce.cn/xwzx/gnsz/gdxw/202608/t20260804_3128645.shtml">ce.cn/xwzx/gnsz/gdxw/202608/t20260804_3128645.shtml</a></li>
<li><a href="https://www.autohome.com.cn/news/202608/1316205.html">autohome.com.cn/news/202608/1316205.html</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/695754743">一文看懂规范标准的强制性标准和推荐性标准 - 知乎</a></li>

</ul>
</details>

**Tags**: `#autonomous driving`, `#regulation`, `#national standard`, `#China`, `#safety`

---

<a id="item-10"></a>
## [White House Reverses on Open-Source AI Rules, Splitting Silicon Valley](https://www.nytimes.com/2026/08/04/technology/ai-washington-regulation-whiplash.html) ⭐️ 8.0/10

The Trump administration, after considering sanctions and trade blacklists against Chinese open-source AI, shifted to a framework requiring pre-release cybersecurity review of AI models. On August 4, 2026, the White House invited tech companies to discuss the new rules, citing competition from China&\#x27;s Kimi model. This policy whiplash will shape the openness of the U.S. AI ecosystem and affect global competition with China&\#x27;s open-source models. It also exposes a major rift among U.S. tech giants, with OpenAI and Anthropic pushing for restrictions while Nvidia, Meta, and others defend open ecosystems. The proposed framework would review models for cybersecurity risks before public release, a significant shift from earlier proposals of sanctions and trade blacklists. Jensen Huang posted on X for the first time last month to defend open source and helped form a security alliance with over 230 members.

telegram · zaihuapd · Aug 4, 15:22

**Background**: Kimi is a series of large language models developed by Moonshot AI, a Chinese AI startup founded in March 2023 by Tsinghua alumni including Yang Zhilin. Moonshot AI is one of China&\#x27;s six &\#x27;AI Tigers,&\#x27; and its latest models, such as Kimi K3, are reported to rival top U.S. models in some benchmarks, intensifying U.S. policy debates about open-source AI.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28chatbot%29">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Yang_Zhilin">Yang Zhilin - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI政策`, `#开源AI`, `#中美竞争`, `#监管`, `#人工智能`

---
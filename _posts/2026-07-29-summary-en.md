---
layout: default
title: "Horizon Summary: 2026-07-29 (EN)"
date: 2026-07-29
lang: en
---

> From 41 items, 9 important content pieces were selected

---

1. [Open-source engine runs Gemma 4 26B in 2GB RAM on M-series Mac](#item-1) ⭐️ 9.0/10
2. [Russian FSB charges Telegram founder Durov with aiding terrorism, issues international warrant](#item-2) ⭐️ 9.0/10
3. [Mitchell Hashimoto launches Superlogical, builds on libghostty](#item-3) ⭐️ 8.0/10
4. [Handbook.md Paper: Long Policy Documents Fail to Govern AI Agents](#item-4) ⭐️ 8.0/10
5. [Document-borne AI worms self-propagate via Copilot for Word](#item-5) ⭐️ 8.0/10
6. [ncnn Vulkan Backend Boosts Edge ML Inference 10x Over CPU ONNX](#item-6) ⭐️ 8.0/10
7. [Claude Shared Chats and Artifacts Indexed by Google](#item-7) ⭐️ 8.0/10
8. [Hugging Face Widely Used for Non-Consensual Deepfake Nudes, Report Says](#item-8) ⭐️ 8.0/10
9. [Moonshot AI Raises $3.5B at $35B Valuation on Kimi K3](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Open-source engine runs Gemma 4 26B in 2GB RAM on M-series Mac](https://github.com/drumih/turbo-fieldfare) ⭐️ 9.0/10

TurboFieldfare, a Swift and Metal inference engine, streams routed MoE experts from SSD to run the 4-bit quantized Gemma 4 26B model on M-series Macs using only about 2GB of RAM. This enables running large language models on memory-constrained devices like base-model Macs, democratizing access to advanced AI without requiring expensive high-RAM hardware. The 4-bit quantized weights are ~14GB, but only the shared layers and KV cache stay in RAM; routed experts are streamed from SSD using a small expert cache and bounded parallel pread. It achieves 5-6 tok/s on an 8GB M2 MacBook Air and 31-35 tok/s on an M5 MacBook Pro.

hackernews · gitpusher42 · Jul 29, 15:05 · [Discussion](https://news.ycombinator.com/item?id=49098510)

**Background**: Mixture-of-Experts \(MoE\) models have multiple specialized &\#x27;expert&\#x27; sub-networks, and only a subset is activated per token. Traditional inference requires loading all weights into memory, but by exploiting MoE&\#x27;s sparsity, only the needed experts are loaded on demand. This project builds on that principle, using SSD streaming to overcome RAM limitations.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2202.09368">[2202.09368] Mixture-of-Experts with Expert Choice Routing Images Intro to Routing: Mixture-of-Experts and Expert Choice [2510.04694] Multilingual Routing in Mixture-of-Experts Mixture-of-Experts with Expert Choice Routing - NeurIPS Mixture-of-Experts with Expert Choice Routing - Google Research Top-K Routing: Expert Selection in Mixture of Experts Models Parameter-Efficient Routed Fine-Tuning: Mixture-of-Experts ...</a></li>
<li><a href="https://arxiv.org/abs/2603.20397">[2603.20397] KV Cache Optimization Strategies for Scalable ... Understanding KV Caching in Transformers - Medium KV Cache in Transformers – Optimizing LLM Inference Cache strategies · Hugging Face</a></li>
<li><a href="https://www.mindstudio.ai/blog/ssd-streaming-ai-models-ram-dial">SSD Streaming for AI Models: How to Turn RAM from a Wall into ...</a></li>

</ul>
</details>

**Discussion**: Community comments discuss comparisons to mmap in llama.cpp, noting that TurboFieldfare synchronizes SSD reads with inference activity to minimize latency. A user provided a workaround for compiling on older macOS versions, and another expressed skepticism about the practical usefulness of slow inference on Apple hardware without Nvidia GPUs.

**Tags**: `#AI`, `#inference`, `#mac`, `#open-source`, `#optimization`

---

<a id="item-2"></a>
## [Russian FSB charges Telegram founder Durov with aiding terrorism, issues international warrant](https://www.interfax.ru/russia/1106228) ⭐️ 9.0/10

On July 29, the Russian Federal Security Service \(FSB\) announced criminal charges against Telegram founder Pavel Durov under Article 205.1.1.1 of the Criminal Code for aiding terrorism, and placed him on an international wanted list for failing to remove content used to coordinate attacks in Russia. This unprecedented legal escalation against a major tech founder sets a dangerous precedent for platform liability and content moderation, potentially impacting how messaging platforms operate globally and raising serious concerns about free speech and government overreach. The FSB specifically accused Telegram&\#x27;s management of refusing to delete channels, groups, and bots used by Ukrainian intelligence and terrorist/extremist organizations to coordinate sabotage, terrorist attacks, mass killings, and cyber fraud, resulting in numerous casualties and billions of rubles in damages.

telegram · zaihuapd · Jul 29, 05:56

**Background**: Telegram, founded by Pavel Durov, is a widely used messaging platform known for its strong encryption and privacy features. In the context of the Russia-Ukraine war, Telegram has become a key source of war updates but also a breeding ground for misinformation and coordination of attacks. Durov, a Russian-born entrepreneur, was arrested in France in 2024 on separate charges, adding to his legal troubles. The FSB&\#x27;s international warrant signals Russia&\#x27;s intent to hold platform leaders personally accountable for user-generated content.

**Tags**: `#Telegram`, `#Pavel Durov`, `#legal`, `#content moderation`, `#Russia`

---

<a id="item-3"></a>
## [Mitchell Hashimoto launches Superlogical, builds on libghostty](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto announced a new company called Superlogical, which will build terminal applications on top of the open source libghostty library, while keeping Ghostty itself transferred to a non-profit. This move establishes a sustainable open source business model by separating the core terminal emulator \(Ghostty\) from commercial products, which could serve as a template for other open source projects seeking to monetize without compromising community trust. Superlogical will consume the same MIT-licensed libghostty components available to everyone else, and will upstream shared terminal work so all libghostty consumers benefit. The company focuses on building terminal applications rather than the emulator itself.

hackernews · yan · Jul 29, 15:41 · [Discussion](https://news.ycombinator.com/item?id=49098965)

**Background**: Ghostty is a fast, feature-rich, cross-platform terminal emulator that uses GPU acceleration and native UI. libghostty is its C-compatible library that allows developers to embed terminal emulation functionality into other applications, released under the MIT license.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Uzaaft/awesome-libghostty">GitHub - Uzaaft/awesome-libghostty</a></li>
<li><a href="https://ghostty.org/">Ghostty</a></li>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty -org/ ghostty : Ghostty is a fast, feature-rich, and...</a></li>

</ul>
</details>

**Discussion**: Commenters largely praised the open source strategy, with one noting the cleverness of transferring Ghostty to a non-profit and building Superlogical on that foundation. Some drew parallels to OLE/COM, while a few criticized the enigmatic title as clickbait.

**Tags**: `#opensource`, `#company`, `#terminal`, `#mitchellh`, `#ghostty`

---

<a id="item-4"></a>
## [Handbook.md Paper: Long Policy Documents Fail to Govern AI Agents](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

A new paper titled &\#x27;Handbook.md&\#x27; demonstrates that long policy documents are unreliable for governing AI agents, revealing fundamental limitations of current long-context models in policy adherence. This finding challenges the assumption that increasing context length alone can ensure AI alignment, as even models with millions of tokens of context fail to reliably follow detailed policies, raising critical safety concerns for autonomous agents. The paper likely uses a benchmark that requires agents to adhere to long, complex policy documents, and finds that performance degrades significantly with document length, highlighting issues with KV-cache quantization and limited working memory.

hackernews · spIrr · Jul 29, 13:01 · [Discussion](https://news.ycombinator.com/item?id=49096969)

**Background**: Long-context models, such as those claiming 128K or 1M token support, are often used for tasks requiring retention of extensive information. However, actual performance on long-context benchmarks varies widely. Policy adherence in AI refers to measuring how well a model&\#x27;s outputs follow a set of written rules. This paper adds evidence that current long-context models are not reliable for governing autonomous agents that must follow detailed policies.

<details><summary>References</summary>
<ul>
<li><a href="https://benchlm.ai/best/long-context">Best Long Context AI Models (July 2026) — Ranked by Benchmark Data</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agree with the findings, noting that long context models often perform poorly in practice due to quantization and sampler issues. One commenter observed that even humans struggle with long policy documents, so expecting perfect adherence from models may be unrealistic. Another pointed out that if a model isn&\#x27;t specifically trained on a handbook, it won&\#x27;t follow it, suggesting that post-training is critical for agentic capabilities.

**Tags**: `#AI alignment`, `#long-context models`, `#AI safety`, `#policy adherence`, `#LLM limitations`

---

<a id="item-5"></a>
## [Document-borne AI worms self-propagate via Copilot for Word](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 8.0/10

Security researcher Håkon Måløy demonstrated a novel prompt injection variant that turns Microsoft Word documents into self-replicating AI worms targeting Copilot for Word. The attack, disclosed to Microsoft MSRC on July 28-29, 2026, marks one of the first public demonstrations of document-borne AI-worm self-propagation in a mainstream productivity suite. This attack exploits the inability of AI assistants like Copilot to distinguish between trusted instructions and user-provided content, enabling worms to spread through shared documents without human intervention. Given Copilot&\#x27;s integration into Microsoft Office and its access to sensitive data, this vulnerability poses a serious, unmitigated security risk for enterprise users. The attack works by hiding malicious instructions in document metadata or formatting \(e.g., white text\), which Copilot reads and executes, causing it to alter documents and propagate the worm to new files. Notably, when the worm spreads from an internally created document, it inherits the trust level of that document, making it harder to detect. As of publication, no robust mitigation exists.

hackernews · Canopy9560 · Jul 29, 11:44 · [Discussion](https://news.ycombinator.com/item?id=49096188)

**Background**: Prompt injection is a type of attack where adversarial inputs trick AI models into unintended behavior by exploiting the model&\#x27;s inability to separate instructions from data. In indirect prompt injection, malicious prompts are embedded in content that the AI retrieves, such as web pages or documents. This research extends the concept to create self-replicating worms, reminiscent of macro viruses from the 1990s but using natural language instead of macros.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://www.explainx.ai/blog/copilot-word-document-ai-worm-xpia-july-2026">Copilot Word AI Worm XPIA — July 2026 | explainx.ai Blog</a></li>

</ul>
</details>

**Discussion**: The Hacker News community reacted with alarm, with many noting that the vulnerability is likely unfixable as long as AI systems mix instructions with data. Commenters warned of scenarios where GitHub repositories or emails could be used to propagate similar worms, and some users have already uninstalled Copilot from local machines as a precaution. Others pointed out that simple techniques like white text still work, highlighting the ease of exploitation.

**Tags**: `#AI security`, `#prompt injection`, `#worm`, `#Copilot`, `#adversarial attacks`

---

<a id="item-6"></a>
## [ncnn Vulkan Backend Boosts Edge ML Inference 10x Over CPU ONNX](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

The developer of PostSlate reports using ncnn&\#x27;s Vulkan backend for vendor-agnostic GPU inference on production edge devices, achieving a 10x speedup over CPU-based ONNX Runtime for models like ArcFace and SCRFD. This approach demonstrates that cross-platform GPU inference is feasible without vendor-specific runtimes, which is critical for applications running on diverse hardware \(NVIDIA, AMD, Intel, Apple Silicon\) without requiring users to install additional drivers. On an NVIDIA RTX 4070 with FP16, ArcFace R50 dropped from 30 ms \(ONNX CPU\) to 3 ms \(ncnn Vulkan\), and SCRFD face detection from 25 ms to 2.5 ms; model size also halved \(174 MB ONNX FP32 to 87 MB ncnn FP16\).

reddit · r/MachineLearning · /u/ppchaos · Jul 29, 10:22

**Background**: ncnn is a high-performance neural network inference framework developed by Tencent, optimized for mobile and embedded platforms with no third-party dependencies. Vulkan is a cross-platform GPU API that provides low-level access to graphics and compute hardware, enabling efficient ML inference across different vendors without proprietary runtimes like CUDA.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Tencent/ncnn">GitHub - Tencent/ncnn: ncnn is a high-performance neural network inference framework optimized for the mobile platform · GitHub</a></li>
<li><a href="https://www.lei.chat/posts/gpgpu-ml-inference-and-vulkan-compute/">GPGPU, ML Inference, and Vulkan Compute | Lei.Chat()</a></li>
<li><a href="https://developer.nvidia.com/blog/machine-learning-acceleration-vulkan-cooperative-matrices/">Machine Learning Acceleration in Vulkan with Cooperative Matrices | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Tags**: `#ML inference`, `#Vulkan`, `#ncnn`, `#edge computing`, `#GPU acceleration`

---

<a id="item-7"></a>
## [Claude Shared Chats and Artifacts Indexed by Google](https://thenextweb.com/news/claude-shared-chats-artifacts-google-search-indexed) ⭐️ 8.0/10

Over the weekend, shared Claude conversation and Artifacts links were indexed by Google, exposing sensitive data such as medical records and company files. Anthropic stated the indexing was by design but later blocked further indexing on Monday afternoon. This incident highlights significant privacy risks for users of AI chat tools who share conversations publicly, as it exposes sensitive personal and corporate data. It affects many Claude users and erodes trust in the security of such sharing features, potentially impacting adoption. The exposed data included medical records, children&\#x27;s information, and internal company documents. Anthropic clarified that no system breach occurred, as shared links are generated by users and were published on public platforms. Old links remain accessible, but users can revoke them in their settings.

telegram · zaihuapd · Jul 29, 02:40

**Background**: Claude Artifacts is a feature that allows users to generate and share interactive code previews and applications from conversations. Shared links are publicly accessible by default, and if they are linked from other public pages, search engines like Google can index them. Similar incidents have occurred with ChatGPT and Grok, where shared conversations were indexed by search engines.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/Claude_Artifacts">Claude Artifacts</a></li>
<li><a href="https://support.claude.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them">What are artifacts and how do I use them? | Claude Help Center</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#security`, `#Claude`, `#AI`, `#data exposure`

---

<a id="item-8"></a>
## [Hugging Face Widely Used for Non-Consensual Deepfake Nudes, Report Says](https://www.theverge.com/ai-artificial-intelligence/971723/hugging-face-nudify-deepfake-undress-women-children) ⭐️ 8.0/10

A report by European nonprofit AI Forensics, released on July 28, 2025, found that the open-source model hub Hugging Face is being extensively used to generate non-consensual deepfake pornography, with seven out of nine top image-editing models capable of undressing women with simple prompts. This highlights a critical gap in content moderation on major AI platforms, raising serious ethical and legal concerns about the misuse of open-source models for generating abusive content, including child sexual abuse material \(CSAM\). The report used a honeypot that received over 1,000 requests in seven days, with 73% involving sexual content and nearly 7% targeting children. Despite Hugging Face&\#x27;s policy banning non-consensual intimate content and child nudity, the platform lacks proactive filtering and output scanning mechanisms.

telegram · zaihuapd · Jul 29, 08:20

**Background**: Hugging Face is an American company and community platform hosting over 100,000 open-source machine learning models and datasets, often called the &\#x27;GitHub for ML&\#x27;. A honeypot is a decoy system designed to lure attackers, allowing researchers to observe malicious activity without risking real systems.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.kaspersky.com.cn/resource-center/threats/what-is-a-honeypot">什么是蜜罐？蜜罐如何帮助提高安全性</a></li>

</ul>
</details>

**Tags**: `#AI伦理`, `#深度伪造`, `#内容审核`, `#Hugging Face`, `#安全`

---

<a id="item-9"></a>
## [Moonshot AI Raises $3.5B at $35B Valuation on Kimi K3](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 8.0/10

Moonshot AI completed a $3.5 billion funding round, surpassing its $1-2 billion target, valuing the company at $35 billion, driven by the success of its Kimi K3 model which rivals frontier models from OpenAI and Anthropic. This massive fundraising highlights China&\#x27;s sustained investment in AI and Moonshot AI&\#x27;s emergence as a major competitor to US frontier labs. The open-source release of Kimi K3 could democratize access to state-of-the-art AI, potentially reshaping the global AI landscape. The Kimi K3 model has 2.8 trillion parameters, uses a novel hybrid linear attention mechanism called Kimi Delta Attention \(KDA\), and supports up to 1 million tokens of context. After the model&\#x27;s release, Moonshot AI&\#x27;s daily sales grew at least sixfold.

telegram · zaihuapd · Jul 29, 10:12

**Background**: Moonshot AI is a Beijing-based AI startup founded in 2023 by Tsinghua alumni, known for developing the Kimi chatbot and large language models. The term &\#x27;DeepSeek moment&\#x27; refers to a market shock in January 2025 when DeepSeek released a powerful open-source model, causing tech stock sell-offs. Moonshot AI&\#x27;s Kimi K3 release triggered a similar reaction, being called another &\#x27;DeepSeek moment.&\#x27;

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28AI%29">Kimi (AI) - Wikipedia</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://huggingface.co/blog/ResterChed/kimi-k3-model-overview-mxfp4-quantization-open-wei">Kimi K3 Model Overview: 2.8T Parameters, MXFP4 Quantization, and What the Open Weights Mean for the Community</a></li>

</ul>
</details>

**Tags**: `#AI funding`, `#Moonshot AI`, `#Kimi K3`, `#Chinese AI`, `#large language model`

---
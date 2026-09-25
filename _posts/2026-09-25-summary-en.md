---
layout: default
title: "Horizon Summary: 2026-09-25 (EN)"
date: 2026-09-25
lang: en
---

> From 45 items, 15 important content pieces were selected

---

**Tools Update**
1. [openai/codex rust-v0.157.0 Release Notes](#item-tools-update-1) ⭐️ 7.0/10
2. [uv 0.12.19: PyPy/GraalPy versions, lazy imports preview, lockfile resolution settings](#item-tools-update-2) ⭐️ 5.0/10

**Technology News**
1. [Go Experiments with Platform-Independent SIMD](#item-tech-news-1) ⭐️ 8.0/10
2. [SemiAnalysis Maps China&\#x27;s AI Datacenter Expansion](#item-tech-news-2) ⭐️ 8.0/10
3. [U.S. Appeals Court Upholds Anthropic Supply Chain Risk Designation](#item-tech-news-3) ⭐️ 7.0/10
4. [Coding Agents Increase Software Engineering Difficulty, Says Simon Willison](#item-tech-news-4) ⭐️ 7.0/10
5. [F-Droid 2.0 released with rewritten UI, dropping Android 6 and Privileged Extension support](#item-tech-news-5) ⭐️ 7.0/10
6. [Google Cloud Releases Gemini 3.8 Live with Live Avatar](#item-tech-news-6) ⭐️ 7.0/10
7. [Anthropic Claude Agent Trades Books in Market Experiment](#item-tech-news-7) ⭐️ 7.0/10
8. [Meta Muse 被曝漏洞可劫持账户](#item-tech-news-8) ⭐️ 7.0/10
9. [Microsoft launches Copilot super app integrating chat, coding, and agents](#item-tech-news-9) ⭐️ 7.0/10

**Technology Blog**
1. [Asking More Questions to Understand Technical Designs](#item-tech-blog-1) ⭐️ 7.0/10

**Financial News**
1. [Appeals court rules that states can regulate Kalshi’s sports prediction markets, dealing another legal blow to platforms](#item-finance-news-1) ⭐️ 8.0/10
2. [Bitget suspects North Korean hackers in $351.6 million crypto breach](#item-finance-news-2) ⭐️ 7.0/10
3. [China&\#x27;s Xi Urges U.S. Cooperation on AI During White House Meeting](#item-finance-news-3) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [openai/codex rust-v0.157.0 Release Notes](https://github.com/openai/codex/releases/tag/rust-v0.157.0) ⭐️ 7.0/10

openai/codex released version rust-v0.157.0, introducing GPT-6 Sol and Luna models with Amazon Bedrock support, fullscreen transcripts, automatic background-server startup, conversation forking, and improved terminal rendering. This is a shipped feature release with no breaking changes.

github · github-actions\[bot\] · Sep 25, 02:31

**「Changes」** \#\#\# New Features
\- Added GPT-6 Sol and Luna models with Amazon Bedrock support and migration prompts for older models \(\#47332, \#47347\)
\- Enabled fullscreen transcripts by default with Shift-click to extend text selections \(\#47178, \#47414\)
\- Enabled automatic background-server startup for eligible interactive sessions with recovery choices for incompatible server settings \(\#47179, \#47318\)
\- Added an \`f\` shortcut to fork conversations open in another app, preserving drafts and queued prompts \(\#47185\)
\- Made \`/import\` available in remote sessions and local background-server sessions \(\#47317\)
\- Improved terminal rendering with Unicode bullets, checkboxes, aligned equations, and optimization notation \(\#47191, \#47322\)

\#\#\# Bug Fixes
\- Preserved active voice conversations when switching threads \(\#47381\)
\- Recovered unsent question answers into the composer when turns end without disrupting active history searches \(\#47422, \#47423\)
\- Respected tmux mouse settings and restored native scrollback for Terminal.app over SSH in automatic screen mode \(\#47399, \#47417\)
\- Fixed configured proxy routing for realtime connections and standalone web search, including search redirects \(\#47101, \#47142, \#47204\)
\- Added retries for transient file-upload failures and increased the upload timeout to five minutes \(\#47122, \#47393\)
\- Enforced network restrictions across redirects and ongoing HTTP and WebSocket traffic, including cancellation when policy changes revoke access \(\#47389, \#47407\)

**「Impact」** Users upgrading to rust-v0.157.0 will gain access to new GPT-6 models and enhanced terminal capabilities. The automatic background-server startup and fullscreen transcripts are enabled by default, which may affect existing workflows that relied on manual server management or compact transcript views. Users with custom proxy configurations should verify that realtime connections and web search continue to route correctly. The conversation forking shortcut \(\`f\`\) provides a new way to manage concurrent sessions. No explicit migration steps are required, but users should review the new default behaviors to ensure they align with their preferences.

**Tags**: `#new-models`, `#bedrock-integration`, `#ui-enhancements`, `#background-server`, `#terminal-rendering`

---

<a id="item-tools-update-2"></a>
### [uv 0.12.19: PyPy/GraalPy versions, lazy imports preview, lockfile resolution settings](https://github.com/astral-sh/uv/releases/tag/0.12.19) ⭐️ 5.0/10

uv 0.12.19 is a shipped incremental release that adds PyPy 3.11.16/3.12.14 and updated GraalPy 3.13.0 build 25.4.4 Python versions, introduces two preview features \(lazy build-backend imports on CPython 3.15+ and omitting unused resolution settings from uv.lock\), and includes several bug fixes. No breaking changes are introduced.

github · astral-releases-bot\[bot\] · Sep 25, 00:33

**「Changes」** \#\#\# Python
\- Added PyPy 3.11.16 and 3.12.14
\- Updated GraalPy 3.13.0 to build 25.4.4

\#\#\# Enhancements
\- Format upload URLs with backticks in \`uv publish\` errors

\#\#\# Preview features
\- Run build-backend hooks with lazy imports on CPython 3.15+ via \`build-lazy-imports\` preview feature
\- Omit unused resolution settings from \`uv.lock\` and ignore changes to them when checking lockfile freshness via \`resolution-inputs\` preview feature

\#\#\# Bug fixes
\- Preserve signed and encoded query parameters in direct-URL metadata to avoid reinstalling unchanged packages
\- Recognize \`1.0.0\` as satisfying \`===1\` during installed-package checks, matching resolution
\- Avoid collisions between Git checkout readiness markers and \`.ok\` files in dependencies
\- Preserve always-false \`python\_version\` markers when parsing their serialized form

\#\#\# Rust API
\- Restored public \`FlatDistributions\` export and its \`BTreeMap\` conversion for downstream resolvers

\#\#\# Documentation
\- Made individual preview-feature reference entries linkable by name

**「Impact」** Most users can upgrade to 0.12.19 without action; the new PyPy and GraalPy versions expand available Python interpreters for projects targeting those runtimes. Users who rely on the Rust API should note the restored \`FlatDistributions\` export. The two preview features are opt-in and do not affect default behavior. The bug fixes improve lockfile stability and package reinstall detection, which may reduce unnecessary reinstalls and lockfile churn. No migration steps are required for existing configurations.

**Tags**: `#python-versions`, `#preview-features`, `#bug-fixes`, `#uv-publish`, `#lockfile`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Go Experiments with Platform-Independent SIMD](https://go.dev/blog/simd-experiment) ⭐️ 8.0/10

Go developers are experimenting with a platform-independent SIMD implementation that abstracts over fixed-width vector ISAs \(like SSE/AVX\) and variable-length vector ISAs \(like ARM SVE and RISC-V Vector\). The approach enables performance gains across architectures, with community benchmarks showing portable SIMD runs ~5x faster than non-SIMD code and ~11% slower than architecture-specific SIMD. The experiment supports non-fixed vector architectures, distinguishing it from other portable SIMD solutions.

hackernews · yurivish · Sep 25, 11:47 · [Discussion](https://news.ycombinator.com/item?id=49843269)

**「SIMD and Vector ISA Context」** SIMD \(Single Instruction, Multiple Data\) allows parallel processing of data arrays using specialized CPU instructions. Traditional SIMD ISAs like SSE and AVX use fixed-width registers, while newer architectures like ARM SVE and RISC-V Vector use variable-length vectors, complicating portable implementations. Go&\#x27;s experiment addresses this by providing an abstraction layer that works across both fixed and variable-length vector ISAs.

**「Performance Gains for Go Applications」** For Go developers working on compute-intensive tasks, this experimental SIMD implementation offers significant performance improvements without sacrificing portability. Community testing shows ~5x speedups over non-SIMD code, making pure Go implementations of tasks like image processing and machine learning models more viable. The support for variable-length vector ISAs like SVE and RVV also positions Go well for future hardware.

**「Developer Feedback and Use Cases」** Community members report real-world testing with the experimental SIMD, including image color swapping benchmarks showing portable SIMD at ~11% slower than arch-specific SIMD but ~5x faster than non-SIMD. One developer noted measurable performance improvements in speech-to-text models running natively in Go with CGO disabled. Developers appreciate the approach&\#x27;s handling of non-fixed vector architectures, which they say distinguishes it from other portable SIMD solutions.

**Tags**: `#Go`, `#SIMD`, `#Performance Optimization`, `#Compiler Engineering`, `#Systems Programming`

---

<a id="item-tech-news-2"></a>
### [SemiAnalysis Maps China&\#x27;s AI Datacenter Expansion](https://newsletter.semianalysis.com/p/the-chinese-ai-infrastructure-boom) ⭐️ 8.0/10

SemiAnalysis has introduced the China Datacenter Model, mapping over 1,000 AI datacenters operated by 60+ entities across China. The model reveals that the largest hyperscaler accounts for roughly one-fifth of national datacenter leasing capacity, while 100MW of new AI-ready capacity was deployed within 12 months. The analysis also highlights the impact of the government&\#x27;s Eastern Data Western Compute initiative on regional infrastructure distribution.

rss · Semianalysis · Sep 25, 15:58

**「Context on China&\#x27;s AI Infrastructure Push」** China&\#x27;s rapid expansion of AI datacenters is driven by national policy support, including the Eastern Data Western Compute strategy, which aims to balance computing resources between eastern and western regions. This follows years of increasing investment in domestic semiconductor and cloud infrastructure to support AI development.

**「Implications for Global Infrastructure Planning」** The concentration of leasing capacity among top hyperscalers and the speed of deployment suggest that infrastructure planners and investors should account for rapid scaling and regional shifts when evaluating opportunities in the AI datacenter sector, particularly in markets influenced by state-led initiatives.

**Tags**: `#AI infrastructure`, `#datacenters`, `#China tech`, `#Semiconductor analysis`, `#cloud computing`

---

<a id="item-tech-news-3"></a>
### [U.S. Appeals Court Upholds Anthropic Supply Chain Risk Designation](https://www.cnbc.com/2026/09/25/pentagon-anthropic-ai-risk-appeals-court.html) ⭐️ 7.0/10

A U.S. appeals court upheld the designation of Anthropic as a supply chain risk under the Secure Technology Act, a designation typically reserved for foreign adversaries. The decision stems from a dispute between Anthropic and the Department of Defense over restrictions on military use of its AI models. The ruling raises concerns about the application of national security designations to domestic AI companies and potential political implications for AI governance.

hackernews · cramer4next · Sep 25, 15:29 · [Discussion](https://news.ycombinator.com/item?id=49845977)

**「Secure Technology Act Designations」** The Secure Technology Act allows the U.S. government to restrict transactions with technology companies deemed to pose a supply chain risk, primarily targeting foreign adversaries like Huawei. Applying this designation to a domestic firm like Anthropic represents an unusual expansion of the law&\#x27;s intended scope, which was originally designed to address foreign national security threats rather than internal corporate disputes.

**「Implications for Domestic AI Regulation」** The ruling could establish a precedent for using national security designations against domestic technology companies, potentially affecting how AI firms negotiate contracts with the U.S. military. It may also influence future AI governance frameworks and create uncertainty for companies seeking to balance ethical AI principles with government partnerships.

**「Community Reactions to the Ruling」** Commenters expressed concern that the designation, originally intended for foreign adversaries, was being applied to a domestic entity, with some suggesting it could be politically weaponized. Others questioned whether the ruling aligned with Anthropic&\#x27;s stated goals of limiting military AI use, while some speculated about broader implications for partisan targeting of technology companies.

**Tags**: `#AI governance`, `#national security`, `#Anthropic`, `#U.S. policy`, `#supply chain risk`

---

<a id="item-tech-news-4"></a>
### [Coding Agents Increase Software Engineering Difficulty, Says Simon Willison](https://simonwillison.net/2026/Sep/24/harder/) ⭐️ 7.0/10

Simon Willison argues that coding agents, while capable of impressive results, make software engineering more difficult by requiring greater discipline and knowledge to use effectively. He emphasizes that unlocking their full potential demands extraordinary rigor from developers, despite their ability to perform remarkable tasks.

rss · Simon Willison · Sep 24, 23:31

**「Context on AI Coding Tools」** AI-powered coding agents have rapidly evolved to assist developers with tasks ranging from code generation to debugging, but their integration into real-world workflows remains challenging due to issues like code quality, context management, and reliability.

**「Implication for Developer Workflows」** Willison&\#x27;s observation suggests that teams adopting coding agents may need to invest more heavily in developer training and process discipline to avoid introducing errors or inefficiencies, potentially offsetting some of the productivity gains these tools promise.

**Tags**: `#coding-agents`, `#ai`, `#llms`, `#software-engineering`, `#developer-tools`

---

<a id="item-tech-news-5"></a>
### [F-Droid 2.0 released with rewritten UI, dropping Android 6 and Privileged Extension support](https://f-droid.org/2026/09/24/f-droid-2.0-a-new-chapter-for-android-freedom.html) ⭐️ 7.0/10

F-Droid 2.0, the largest update in ten years for the open-source Android app repository, was released on September 24, 2026. The new version features a completely rewritten user interface and underlying code, reorganized into three main areas: Discover, Search, and My Apps. It improves app discovery, categorization, search, and filtering, including support for searching app descriptions, categories, and translated content, with enhanced CJK \(Chinese, Japanese, Korean\) text search. The rollout will happen over the coming weeks following 14 test releases. However, the update drops support for Android 6 and the F-Droid Privileged Extension.

telegram · zaihuapd · Sep 24, 23:58

**「F-Droid as an open-source Android app repository」** F-Droid is a well-known open-source alternative to proprietary app stores like Google Play, allowing users to browse, install, and update Android applications that are distributed under free and open-source licenses. It has been a cornerstone of the Android open-source ecosystem for over a decade, providing a privacy-respecting platform for app distribution.

**「Compatibility changes affect older devices and privileged installations」** Users on Android 6 devices will no longer be able to update to or use F-Droid 2.0, requiring them to remain on the previous version or upgrade their devices. Additionally, the removal of F-Droid Privileged Extension support impacts users who relied on system-level integration for automatic app installations and updates, particularly in managed or enterprise environments.

**Tags**: `#F-Droid`, `#Android`, `#Open Source`, `#Mobile`, `#App Store`

---

<a id="item-tech-news-6"></a>
### [Google Cloud Releases Gemini 3.8 Live with Live Avatar](https://cloud.google.com/blog/products/ai-machine-learning/gemini-3-8-live-with-live-avatar-is-now-generally-available) ⭐️ 7.0/10

Google Cloud has made Gemini 3.8 Live with Live Avatar generally available, enabling real-time lip-synced video avatars and voice-to-voice conversation in 97 languages. The feature, first previewed at Google Cloud Next 2026, requires enterprise allowlisting for custom avatars and includes SynthID watermarking for audio and video. Gemini 3.8 Live Extended Thinking remains in private preview.

telegram · zaihuapd · Sep 25, 03:09

**「Previewed at Google Cloud Next 2026」** Gemini 3.8 Live with Live Avatar was initially previewed at Google Cloud Next 2026 as part of Google&\#x27;s push to expand multimodal AI capabilities for enterprise applications.

**「Enterprise Adoption of AI Avatars」** Enterprises can now deploy real-time, multilingual AI avatars with built-in SynthID watermarking, though custom avatar creation requires allowlisting, potentially limiting immediate adoption to approved organizations.

**Tags**: `#Gemini`, `#AI`, `#Google Cloud`, `#Live Avatar`, `#Multimodal AI`

---

<a id="item-tech-news-7"></a>
### [Anthropic Claude Agent Trades Books in Market Experiment](https://www.anthropic.com/research/project-swap) ⭐️ 7.0/10

Anthropic conducted an experiment in which a Claude agent traded books in a simulated market after brief five-minute chats with 201 human participants. The agent&\#x27;s book rankings aligned with participants&\#x27; own preferences 61% of the time, and participants rated their satisfaction at 7.2 out of 10. The study found that stronger models achieved higher transaction efficiency, and participants were willing to delegate approximately 30% of their annual book budget to such agents. The market did not reach optimal outcomes primarily due to the agent&\#x27;s limited knowledge of participants rather than weak negotiation skills.

telegram · zaihuapd · Sep 25, 04:40

**「Agentic AI in Market Simulation」** This experiment builds on research into AI agents performing real-world tasks through preference inference and negotiation. Prior work has explored how language models can represent user preferences in decision-making scenarios, but this study specifically tests agentic behavior in a multi-party trading environment where agents must infer preferences from minimal interaction.

**「Implications for AI-Assisted Decision Making」** The results suggest that AI agents can effectively perform preference-based trading tasks with only brief user interaction, indicating potential for deployment in personal shopping, recommendation, and budget allocation services. Organizations developing AI assistants may consider how to balance user privacy with the depth of preference data needed for optimal agent performance.

**Tags**: `#AI agents`, `#market simulation`, `#preference inference`, `#Anthropic`, `#experiment`

---

<a id="item-tech-news-8"></a>
### [Meta Muse 被曝漏洞可劫持账户](https://www.ithome.com/1/007/126.htm) ⭐️ 7.0/10

A zero-day in Meta Muse for macOS enables account hijacking via hidden voice config; Meta has issued a hotfix.

telegram · zaihuapd · Sep 25, 07:27

**Tags**: `#security`, `#macOS`, `#Meta`, `#zero-day`, `#vulnerability`

---

<a id="item-tech-news-9"></a>
### [Microsoft launches Copilot super app integrating chat, coding, and agents](https://www.theverge.com/news/1000532/microsoft-copilot-super-app-chat-coding-autopilot) ⭐️ 7.0/10

Microsoft announced an updated Copilot &\#x27;super app&\#x27; that consolidates AI chat, coding, and agent capabilities into a single interface with Home, Code, and Autopilot tabs. The Code tab enables users to create apps and automations and share them with colleagues, while the former Scout assistant has been rebranded as Autopilot, a cloud-based &\#x27;digital colleague.&\#x27; Home and Code will roll out to Frontier users over the coming weeks, and Autopilot enters private preview later this month.

telegram · zaihuapd · Sep 25, 12:15

**「Background」** Copilot is Microsoft&\#x27;s AI assistant brand spanning productivity \(Microsoft 365\), development \(GitHub\), and cloud \(Azure\) products. The rebranding of Scout to Autopilot reflects Microsoft&\#x27;s effort to position its AI agents as collaborative, cloud-hosted entities rather than local personal assistants.

**「Impact」** Frontier program participants will gain access to the integrated Home and Code tabs in the next few weeks, allowing them to build and share automations without leaving the Copilot interface. Organizations evaluating Copilot as a unified AI workspace should note that Autopilot&\#x27;s private preview is limited to a smaller audience initially, meaning full agent collaboration capabilities will arrive after the broader Home and Code rollout.

**Tags**: `#AI`, `#Microsoft`, `#Copilot`, `#Developer Tools`, `#Productivity`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Asking More Questions to Understand Technical Designs](https://seangoedecke.com/you-should-all-be-asking-way-more-questions/) ⭐️ 7.0/10

rss · Sean Goedecke · Sep 25, 00:00

**「Background」** Sean Goedecke argues that most people don&\#x27;t ask enough questions during technical discussions because they trust the speaker rather than actively trying to understand. He contends that small misunderstandings early on compound into major problems later, making it essential to interrupt and clarify during conversations rather than waiting until the end.

**「Solution」** Goedecke&\#x27;s approach involves mentally simulating implementation while listening to a plan, visualizing the actual code that would need to be written. He focuses on three key areas: data flow between services, service-to-service communication \(including authentication\), and data persistence. When he hears something vague or inconsistent with known system constraints, he immediately asks for clarification. This technique has helped him uncover fundamentally unworkable designs, such as a complex event-driven system that couldn&\#x27;t meet data-siloing requirements. He applies the same rigorous questioning to AI agents, asking targeted questions about code reuse, authentication capabilities, requirement satisfaction, and file modifications. About half the time, these questions reveal that the AI has made design mistakes, highlighting the importance of continuous verification even with advanced models.

**「Takeaway」** The core thesis is that actively asking questions and mentally simulating implementation during design discussions is a crucial skill for technical leadership, as it can save significant time and turn failed projects into successful ones. This approach is especially important when working with AI agents, which make design mistakes due to their lack of continuous learning and domain experience.

**Tags**: `#technical communication`, `#software architecture`, `#AI collaboration`, `#design review`, `#engineering process`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Appeals court rules that states can regulate Kalshi’s sports prediction markets, dealing another legal blow to platforms](https://www.cnbc.com/2026/09/25/appeals-court-rules-states-can-regulate-sports-prediction-markets.html) ⭐️ 8.0/10

A federal appeals court ruled that states can regulate sports prediction markets as gambling, dealing a second major legal blow to platforms like Kalshi and setting up a potential Supreme Court case over federal versus state oversight.

rss · CNBC Finance · Sep 25, 21:41

**Tags**: `#Regulation`, `#Prediction Markets`, `#Gambling`, `#CFTC`, `#Legal`

---

<a id="item-finance-news-2"></a>
### [Bitget suspects North Korean hackers in $351.6 million crypto breach](https://www.cnbc.com/2026/09/25/crypto-platform-bitget-suspects-north-korea-in-352-million-hack.html) ⭐️ 7.0/10

Crypto exchange Bitget reported a security breach resulting in approximately $351.6 million in digital assets being stolen, with preliminary evidence pointing to North Korean hackers based on IP addresses and attack patterns. The breach affected multiple blockchains including Ethereum, XRP Ledger, Avalanche, BNB Smart Chain, and Arbitrum, and withdrawals remain suspended while systems are repaired.

rss · CNBC Finance · Sep 25, 06:13

**「Background」** Bitget CEO Gracy Chen stated that investigators identified IP addresses linked to VPN services previously used by a North Korean hacking group, and that the attack pattern resembled earlier operations attributed to the country. The attacker breached a critical backend wallet system, spoofed transfer information, and triggered the authorization-signing process, though private key compromise has been ruled out.

**「Impact」** The breach affects crypto investors and users across multiple blockchain networks, with Bitget confirming that customer balances remain accurate and the loss is fully covered by its User Protection Fund, which holds more than $464 million. Bybit CEO Ben Zhou offered assistance and is updating the LazarusBounty platform to help trace the stolen funds.

**Tags**: `#Cybersecurity`, `#Cryptocurrency`, `#North Korea`, `#Digital Assets`, `#Exchange Security`

---

<a id="item-finance-news-3"></a>
### [China&\#x27;s Xi Urges U.S. Cooperation on AI During White House Meeting](https://www.cnbc.com/2026/09/25/chinas-xi-urges-us-to-cooperate-on-ai.html) ⭐️ 7.0/10

Chinese President Xi Jinping told U.S. President Donald Trump during a White House meeting that cooperation on artificial intelligence offers more opportunity than competition, calling for continued AI dialogue and joint efforts to prevent misuse of the technology. The meeting coincided with early-stage talks on establishing a U.S.-China AI dialogue and an alert system for AI incidents, as confirmed by U.S. Treasury Secretary Scott Bessent and China&\#x27;s Commerce Ministry.

rss · CNBC Finance · Sep 25, 01:22

**「Background」** The U.S. has imposed restrictions on China&\#x27;s access to advanced semiconductors used for training AI models, and has criticized Chinese companies for allegedly misusing American AI technology. Recent concerns about autonomous AI systems making cyberattacks faster and harder to contain have heightened interest in cross-border AI risk management.

**「Impact」** The diplomatic overture signals a potential shift toward managed U.S.-China AI cooperation, which could influence global AI governance standards and affect tech companies and investors in both countries operating under existing semiconductor export controls.

**Tags**: `#AI policy`, `#U.S.-China relations`, `#diplomacy`, `#semiconductor restrictions`, `#AI governance`

---
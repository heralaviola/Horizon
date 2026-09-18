---
layout: default
title: "Horizon Summary: 2026-09-18 (EN)"
date: 2026-09-18
lang: en
---

> From 61 items, 18 important content pieces were selected

---

**Tools Update**
1. [openai/codex rust-v0.155.0: voice, TUI, task, and security updates](#item-tools-update-1) ⭐️ 8.0/10
2. [uv 0.12.16: Hash verification, macOS fixes, and Pyodide updates](#item-tools-update-2) ⭐️ 7.0/10
3. [openai/codex rust-v0.155.1 patch fixes TUI reasoning summary default](#item-tools-update-3) ⭐️ 5.0/10

**Technology News**
1. [Android 17 Adds Pixel-Exclusive APIs Without AOSP Release](#item-tech-news-1) ⭐️ 7.0/10
2. [Developer Claims Proof of Conway&\#x27;s Conjecture via AI-Assisted Approach](#item-tech-news-2) ⭐️ 7.0/10
3. [Inside ZCode: Silently uploading your Git history to the cloud](#item-tech-news-3) ⭐️ 7.0/10
4. [Engrams Embedding Entendre: Codesign for Efficient DRAM/SSD Offloading](#item-tech-news-4) ⭐️ 7.0/10
5. [NHANES CHD risk model audit removes leakage-prone questionnaire data](#item-tech-news-5) ⭐️ 7.0/10
6. [Claude Projects Redesigned: From Folders to Conversations](#item-tech-news-6) ⭐️ 7.0/10
7. [OpenAI launches Astra for Law legal AI service](#item-tech-news-7) ⭐️ 7.0/10
8. [联合国携手谷歌打造 AI 可用的全球数据平台](#item-tech-news-8) ⭐️ 7.0/10
9. [美国联邦公报网站撤下之前采用的 Qwen 搜索工具](#item-tech-news-9) ⭐️ 7.0/10
10. [长鑫存储拟进军闪存市场](#item-tech-news-10) ⭐️ 7.0/10
11. [Anthropic launches wet biology lab to advance AI-driven drug discovery](#item-tech-news-11) ⭐️ 7.0/10

**Technology Blog**
1. [Two Techniques for Programming with System One Models](#item-tech-blog-1) ⭐️ 8.0/10

**Financial News**
1. [Warren Buffett Steps Down as Berkshire Hathaway Chairman After 61 Years](#item-finance-news-1) ⭐️ 8.0/10
2. [China&\#x27;s Housing Regulator Declares &\#x27;Stock Era&\#x27; as Secondary Market Share Surpasses Half](#item-finance-news-2) ⭐️ 7.0/10
3. [Chinese Yuan Hits Four-Year High as PBOC Raises Daily Midpoint for Eighth Session](#item-finance-news-3) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [openai/codex rust-v0.155.0: voice, TUI, task, and security updates](https://github.com/openai/codex/releases/tag/rust-v0.155.0) ⭐️ 8.0/10

openai/codex released rust-v0.155.0, a shipped update adding experimental voice conversations, live TUI reasoning summaries, task management in the agents overview, Touch ID for MCP, configurable daemon update schedules, and improved Amazon Bedrock AWS credential handling. The release also includes bug fixes for tmux resizes, transcript restoration, OAuth credential reporting, account switching, and WSL sandbox hardening.

github · github-actions\[bot\] · Sep 17, 23:14

**「Changes」** \#\#\# New Features
\- Added experimental \`/voice\` conversations with live transcripts and microphone controls on supported builds, enabled through \`/experimental\`. \(\#43581, \#43651, \#44331\)
\- The TUI now shows live reasoning summaries in the status row and completion timestamps after successful turns. \(\#43558, \#43921\)
\- Added task hiding, archiving, and deletion in the agents overview, plus worktree ownership details and confirmed deletion of clean managed worktrees. \(\#43942, \#44424, \#44433\)
\- Added Touch ID verification for MCP requests in local TUI sessions on supported Macs. \(\#43624, \#43712, \#43715\)
\- Added configurable daemon update schedules and \`codex app-server daemon update\`; saved threads and active goals can recover after daemon restarts. \(\#43542, \#43562, \#44314\)
\- Amazon Bedrock can now obtain AWS credentials from configured commands, with caching, expiration-based refresh, and authentication recovery. \(\#44028\)

\#\#\# Bug Fixes
\- Accepted prompts are now saved even when compaction fails before a turn starts. \(\#44487\)
\- Fixed missed tmux resizes, transcript viewport restoration, and stale history appearing after switching threads. \(\#43603, \#43889, \#43994\)
\- MCP servers now report expired OAuth credentials accurately and provide reconnect guidance when token refresh fails. \(\#43947, \#44359\)
\- Automatic approval reviews now preserve complete actions and authorization evidence more reliably, retry transient failures, and distinguish review failures from unsafe-action findings. \(\#44482, \#44569, \#44570\)
\- Switching accounts now invalidates remote-control sessions, cached WebSocket state, and model catalogs belonging to the previous identity. \(\#43906, \#44341, \#44489\)
\- Blocked Windows-process escapes from restricted WSL sandboxes and hardened brokered shell snapshots against credential exposure. \(\#44286, \#43909, \#44040\)

\#\#\# Chores
\- Aligned Python SDK and runtime publishing with stable CLI releases, using matching versions and verifying runtime assets before SDK publication. \(\#44067\)

**「Impact」** Users who rely on the TUI for interactive coding sessions will benefit from live reasoning summaries and completion timestamps, while those managing multiple tasks can now hide, archive, or delete tasks directly from the agents overview. Mac users gain Touch ID verification for MCP requests, improving local security. Teams using Amazon Bedrock should review the new AWS credential command configuration to take advantage of caching and automatic refresh. The experimental voice feature is opt-in via \`/experimental\` and may change in future releases. Upgrading is recommended for the security hardening around WSL sandboxes and shell snapshots, though no explicit migration steps are required for most users.

**Tags**: `#voice-conversations`, `#tui-enhancements`, `#task-management`, `#security`, `#cloud-integration`

---

<a id="item-tools-update-2"></a>
### [uv 0.12.16: Hash verification, macOS fixes, and Pyodide updates](https://github.com/astral-sh/uv/releases/tag/0.12.16) ⭐️ 7.0/10

uv 0.12.16 is a patch release that adds hash verification for downloaded wheels and source distributions, improves macOS platform marker handling, and fixes several panic-related bugs. The release also introduces new Pyodide Python distributions and a preview feature for offline lock validation. These are shipped enhancements and bug fixes, not breaking changes.

github · astral-releases-bot\[bot\] · Sep 18, 01:01

**「Changes」** \#\#\# Python
\- Added Pyodide 314.0.7, 0.29.5, and 0.27.8

\#\#\# Enhancements
\- Verify downloaded wheels and source distributions against hashes supplied by package indexes
\- Allow \`build-constraint-dependencies\` entries to include hashes for verifying downloaded build dependencies
\- Honor Darwin \`platform\_release\` markers in \`required-environments\` using macOS wheel deployment targets
\- Reject unsupported Git URL schemes while parsing lockfiles instead of panicking during frozen exports

\#\#\# Preview features
\- Support \`lock-without-metadata\` across all dependency types while retaining \`package.metadata\` for remote URL dependencies to enable offline validation
\- Honor configured and command-line index settings, including credentials, in \`uv upgrade\`
\- Allow \`uv check\` to run in projects that are not managed by uv and outside workspaces
\- Respect \`--python\` and \`UV\_PYTHON\` when selecting the Python version for \`uv check\`

\#\#\# Bug fixes
\- Redact Azure shared access signatures from displayed and logged URLs
\- Check archive sizes from \`pylock.toml\` before reusing cached distributions
\- Keep user-authored local dependency paths relative in lockfiles when backend metadata reports absolute paths
\- Use the bundled \`uv\_build\` backend only when its version matches active version pins
\- Handle malformed index URLs without panicking when credentials are configured
\- Report a configuration error instead of panicking for proxy URLs without a host
\- Return a credential-redacted error instead of panicking when a URL cannot be converted to a path

**「Impact」** Users who rely on package integrity verification will benefit from the new hash verification of downloaded wheels and source distributions, which strengthens supply-chain security. macOS users gain more accurate platform marker handling for wheel selection. The panic-to-error conversions improve stability and reduce crashes in edge cases involving Git URLs, proxy URLs, and malformed index URLs. The preview offline lock validation feature is useful for environments without network access but should be tested before relying on it in production. Upgrading is recommended for all users, with no special migration steps required.

**Tags**: `#security`, `#hash-verification`, `#compatibility`, `#macos`, `#pyodide`

---

<a id="item-tools-update-3"></a>
### [openai/codex rust-v0.155.1 patch fixes TUI reasoning summary default](https://github.com/openai/codex/releases/tag/rust-v0.155.1) ⭐️ 5.0/10

openai/codex released rust-v0.155.1, a patch release that fixes a bug where new local TUI sessions incorrectly enabled reasoning summaries by default, causing request rejections from providers that do not support them. The fix restores the previous default behavior \(disabled\) while still respecting explicit user settings. This is a shipped bug fix.

github · github-actions\[bot\] · Sep 18, 20:03

**「Changes」** \- New local TUI sessions now leave reasoning summaries disabled by default, fixing request rejection by providers that do not support them. Explicit reasoning-summary settings remain respected. \(\#46467\)
\- Restore none as the TUI reasoning summary default \(@celia-oai\)

**「Impact」** Users running local TUI sessions with providers that do not support reasoning summaries should upgrade to avoid request rejections. No migration action is required; the fix only restores the previous default behavior while preserving any explicit user configuration.

**Tags**: `#bug-fix`, `#tui`, `#reasoning-summary`, `#compatibility`, `#patch-release`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Android 17 Adds Pixel-Exclusive APIs Without AOSP Release](https://grapheneos.social/@GrapheneOS/117282080803799576) ⭐️ 7.0/10

Android 17 introduces new APIs in a Pixel-only update without releasing the corresponding source code to AOSP, marking the first time since the Android 3.x era that new platform APIs are not made available to the open-source project. According to community analysis, the issue specifically concerns the first and third quarterly release patches each year being Pixel-exclusive, rather than the entire Android 117 release. This represents a significant departure from Google&\#x27;s historical practice of making new APIs available to all Android partners and open-source projects simultaneously with Pixel releases.

hackernews · theanonymousone · Sep 18, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49758736)

**「Android release model and AOSP history」** Historically, Google released new Android platform versions to the Android Open Source Project \(AOSP\) alongside or shortly after Pixel device updates, allowing OEMs and custom distributions like GrapheneOS to access new APIs and security patches. GrapheneOS, an open-source security-focused OS built on AOSP since 2016, has traditionally tracked these releases closely, including reaching Android 17 on June 16, 2026. The current concern stems from Google&\#x27;s quarterly release patches \(QPRs\), where the first and third QPRs each year are now reportedly Pixel-exclusive, meaning new APIs and some September platform security fixes are not immediately available to AOSP or non-Pixel devices.

**「Implications for AOSP and Security-Focused Projects」** The Pixel-exclusive API releases create challenges for projects like GrapheneOS that depend on AOSP source code to build security-hardened Android distributions. Without access to the new APIs and quarterly patches, these projects cannot maintain full compatibility with Pixel devices or provide equivalent functionality to users. This shift raises concerns about the long-term viability of AOSP as a truly open platform and may force alternative Android ecosystems to develop independent implementations of Google&\#x27;s proprietary features.

**「Developer and Community Response」** Community members expressed frustration with Google&\#x27;s increasing restrictions, with one commenter noting the &\#x27;ridiculous&\#x27; roadblocks for GrapheneOS including delayed source patches and attestation issues. Technical analysis from participants like bri3d and Ajedi32 clarified that the core issue involves quarterly release patches being Pixel-exclusive rather than just one API, suggesting a systematic change in Google&\#x27;s release model that affects the broader Android ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS - Wikipedia</a></li>
<li><a href="https://alternativeto.net/news/2026/9/grapheneos-claims-android-17-qpr1-apis-remain-exclusive-to-pixel-devices/">GrapheneOS claims Android 17 QPR1 APIs remain exclusive to Pixel ...</a></li>
<li><a href="https://stateofsurveillance.org/news/grapheneos-android-17-port-degoogled-privacy-os-2026/">GrapheneOS Hits Android 17 the Day Google Releases It</a></li>

</ul>
</details>

**Tags**: `#Android`, `#AOSP`, `#GrapheneOS`, `#Open Source`, `#Mobile Development`

---

<a id="item-tech-news-2"></a>
### [Developer Claims Proof of Conway&\#x27;s Conjecture via AI-Assisted Approach](https://overreacted.io/how-i-vibed-a-proof-of-conways-conjecture/) ⭐️ 7.0/10

A developer, writing under the username m-hodges, has published a personal narrative describing a claimed proof of Conway&\#x27;s conjecture, linking to a GitHub repository \(github.com/gaearon/conway-refinement\) that contains technical details of the approach. The post, titled &\#x27;I vibed a proof of Conway&\#x27;s conjecture,&\#x27; frames the work as an AI-assisted mathematical discovery rather than a formally peer-reviewed publication. The repository includes a section titled &\#x27;Why I think it&\#x27;s correct,&\#x27; outlining the reasoning behind the claimed proof. The submission has sparked discussion on Hacker News, with technically trained commenters engaging on topics such as verification, simplification, and the role of AI in mathematical discovery.

hackernews · m-hodges · Sep 18, 14:36 · [Discussion](https://news.ycombinator.com/item?id=49755024)

**「Conway&\#x27;s Conjecture and Surreal Numbers」** Conway&\#x27;s conjecture, proposed by mathematician John H. Conway, relates to the structure of surreal numbers, a class of numbers that includes all ordinal numbers, real numbers, and infinite and infinitesimal numbers. The conjecture concerns the behavior of certain sequences derived from the surreal number system, and a proof would represent a significant advancement in combinatorial game theory and mathematical logic. The surreal numbers are constructed recursively by filling gaps between previously defined numbers, a process described in the community comments as spawning new numbers in every gap between existing ones.

**「Implications for AI-Assisted Mathematical Discovery」** If verified, the claimed proof would demonstrate the potential for AI-assisted approaches to contribute meaningfully to solving longstanding open problems in mathematics. However, the informal presentation and lack of peer review mean the claim remains unconfirmed by the broader mathematical community. The discussion highlights growing interest in how AI tools can augment human mathematical reasoning, with one commenter suggesting that &\#x27;mathematicians have more work now to unravel all this, and make it useful.&\#x27;

**「Community Response to the Claimed Proof」** Commenters on Hacker News have engaged critically with the post, with one trained amateur mathematician encouraging the author to continue simplifying and understanding the proof independently. Another commenter drew an analogy between AI-assisted discovery and the &\#x27;infinite monkey theorem,&\#x27; proposing an &\#x27;LLM corollary&\#x27; that finite LLM agents with sufficient token budgets could almost surely find all theorems. Some discussion also focused on the mechanics of surreal number construction, with questions about how the approach extends beyond rational numbers.

**Tags**: `#mathematics`, `#artificial intelligence`, `#open source`, `#research`, `#conway&\#x27;s conjecture`

---

<a id="item-tech-news-3"></a>
### [Inside ZCode: Silently uploading your Git history to the cloud](https://blog.ferstar.org/en/posts/zcode-silent-workspace-snapshot-upload/) ⭐️ 7.0/10

ZCode, an AI coding agent by z.ai, was found to silently upload users&\#x27; entire Git history to the cloud via its codebase indexing feature, prompting an official apology and community discussion about AI agent permissions and privacy.

hackernews · csmantle · Sep 18, 06:11 · [Discussion](https://news.ycombinator.com/item?id=49750694)

**Tags**: `#ai-safety`, `#privacy`, `#security`, `#coding-agents`, `#git`

---

<a id="item-tech-news-4"></a>
### [Engrams Embedding Entendre: Codesign for Efficient DRAM/SSD Offloading](https://newsletter.semianalysis.com/p/engrams-embedding-entendre-codesign) ⭐️ 7.0/10

A technical exploration of the Engrams model architecture and its impact on DRAM/SSD offloading efficiency, with implications for AI inference systems and hardware-software codesign.

rss · Semianalysis · Sep 18, 14:34

**Tags**: `#AI Systems`, `#Hardware-Software Codesign`, `#Model Architecture`, `#DRAM/SSD Optimization`, `#Inference Engineering`

---

<a id="item-tech-news-5"></a>
### [NHANES CHD risk model audit removes leakage-prone questionnaire data](https://www.reddit.com/r/MachineLearning/comments/1wjp062/classifying_coronary_heart_disease_risk_from/) ⭐️ 7.0/10

A student project predicts self-reported, physician-diagnosed coronary heart disease from four NHANES cycles \(2011-2012 to 2017-2018\), about 21,500 adults after cleaning, comparing logistic regression, random forest, and gradient boosting on demographics, blood pressure, body measurements, and a lipid panel. The author performed a leakage audit and found that including NHANES cardiovascular questionnaire variables \(stroke, heart attack, angina, and the CHD outcome itself\) inflated PR-AUC from 0.23 to 0.51, so those variables were removed and the leakage effect was documented. After sigmoid recalibration fit on the development set and a threshold frozen before test-set evaluation, final held-out test results were ROC-AUC 0.875 and PR-AUC 0.239 for logistic regression, with random forest and gradient boosting performing similarly; age alone achieved 0.83 AUC. The author notes that smoking status, diabetes, and blood pressure medication use are available in NHANES but not yet included as features.

reddit · r/MachineLearning · /u/YouJonaa · Sep 18, 12:36

**「Background」** NHANES \(National Health and Nutrition Examination Survey\) is a U.S. CDC program that collects health and nutrition data through interviews, physical examinations, and laboratory tests, and its public-use datasets are commonly used for epidemiological and machine learning research. A leakage audit identifies features that encode information about the target variable, which can artificially inflate model performance and mislead interpretation of real risk factors.

**「Impact」** The project illustrates strong ML engineering practices for healthcare data by explicitly auditing and removing leakage-prone self-reported questionnaire variables, recalibrating miscalibrated probabilities \(mean predicted risk ~30% vs. true 4% prevalence\), and freezing the decision threshold on the development set before test evaluation, which serves as a useful reference for practitioners building risk models on survey data with low-prevalence outcomes.

**Tags**: `#machine-learning`, `#healthcare-ai`, `#data-leakage`, `#calibration`, `#NHANES`

---

<a id="item-tech-news-6"></a>
### [Claude Projects Redesigned: From Folders to Conversations](https://claude.com/blog/projects-redesigned) ⭐️ 7.0/10

Anthropic has launched a redesigned version of Claude Projects, now in beta within Claude Code. Instead of organizing work into folders, users describe a goal and Claude automatically breaks it down, assigns parallel threads, reviews outputs, and summarizes results. The feature also supports mobile follow-up and continues running tasks after the user leaves their computer. The beta is initially available to select Claude Pro and Max subscribers, with expansion to more Claude Code users planned within a week, followed by a broader rollout to all Claude, Team, and Enterprise plans.

telegram · zaihuapd · Sep 18, 00:18

**「Background」** Previously, Claude Projects functioned as a folder-based system for organizing conversations and files around specific topics or tasks. The new design shifts to a conversation-based model where the AI actively manages task decomposition and parallel processing, aligning with Anthropic&\#x27;s broader push toward agentic workflows in developer tools.

**「Impact」** For Claude Code users, the redesign introduces automated task management that could streamline complex development workflows by reducing manual organization and enabling parallel execution. However, the impact is currently limited as the feature is in beta and only accessible to a subset of Pro and Max subscribers, with full availability expected in stages over the coming weeks.

**Tags**: `#Claude`, `#AI agents`, `#developer tools`, `#Anthropic`, `#project management`

---

<a id="item-tech-news-7"></a>
### [OpenAI launches Astra for Law legal AI service](https://openai.com/index/astra-for-law/) ⭐️ 7.0/10

OpenAI launched Astra for Law, a legal AI service that combines GPT-6 Astra with legal retrieval indexing for law firms and legal tech companies. On the Vals AI benchmark, the service scored 54.0% on 200 U.S. legal research questions, a 40% relative improvement over GPT-6 Astra with web search alone \(38.7%\). The service is rolling out to select law firms via Trusted Access for ChatGPT and Codex, with a GPT-6 Astra Law API and 26 partner plugins plus zero-data-retention privacy controls to follow.

telegram · zaihuapd · Sep 18, 01:49

**「Background」** Astra for Law builds on OpenAI&\#x27;s GPT-6 Astra model family, adding domain-specific legal retrieval indexing to improve accuracy on legal research tasks. The Vals AI benchmark is a standard evaluation for legal AI systems measuring performance on U.S. legal questions.

**「Impact」** Law firms and legal tech developers will be able to build AI products on a model optimized for legal research, with the upcoming GPT-6 Astra Law API and zero-data-retention controls addressing confidentiality concerns common in legal workflows.

**Tags**: `#AI`, `#LegalTech`, `#OpenAI`, `#GPT-6`, `#SoftwareEngineering`

---

<a id="item-tech-news-8"></a>
### [联合国携手谷歌打造 AI 可用的全球数据平台](https://techcrunch.com/2026/09/17/un-turns-to-google-to-make-its-global-data-ready-for-ai-agents/) ⭐️ 7.0/10

The UN partners with Google to launch an AI-ready global data platform replacing UNData, supporting natural language queries and MCP protocol, with 26 UN agencies committed and a goal to include 80% of datasets by 2027.

telegram · zaihuapd · Sep 18, 04:50

**Tags**: `#AI infrastructure`, `#data platforms`, `#United Nations`, `#Google`, `#open data`

---

<a id="item-tech-news-9"></a>
### [美国联邦公报网站撤下之前采用的 Qwen 搜索工具](https://www.reuters.com/legal/litigation/us-government-website-used-ai-search-tool-china-that-fbi-said-copied-anthropic-2026-09-17/) ⭐️ 7.0/10

The U.S. Federal Register removed a Qwen-powered search tool over concerns about using Chinese-developed AI in government systems, underscoring AI supply-chain and data-security risks.

telegram · zaihuapd · Sep 18, 05:20

**Tags**: `#AI governance`, `#supply chain security`, `#data security`, `#government technology`, `#Qwen`

---

<a id="item-tech-news-10"></a>
### [长鑫存储拟进军闪存市场](https://www.reuters.com/world/asia-pacific/chinas-cxmt-eyes-flash-memory-push-amid-global-shortage-firm-take-samsung-ymtc-2026-09-18/) ⭐️ 7.0/10

China&\#x27;s CXMT is reportedly planning to enter the NAND flash memory market, expanding beyond DRAM amid global chip shortages driven by AI demand.

telegram · zaihuapd · Sep 18, 07:55

**Tags**: `#semiconductors`, `#NAND flash`, `#CXMT`, `#DRAM`, `#AI hardware`

---

<a id="item-tech-news-11"></a>
### [Anthropic launches wet biology lab to advance AI-driven drug discovery](https://www.reuters.com/world/anthropic-quietly-sets-up-biology-lab-it-ramps-ai-drug-program-2026-09-18/) ⭐️ 7.0/10

Anthropic has quietly established a wet biology laboratory in the San Francisco Bay Area to advance its AI-driven drug discovery program, with the goal of using its Claude AI to orchestrate laboratory robotics for conducting biological experiments. The company&\#x27;s head of life sciences confirmed the initiative, which focuses on rare disease research and currently avoids clinical trials to prevent direct competition with pharmaceutical companies. This effort builds on Anthropic&\#x27;s earlier launch of Claude Science software and its reported $400 million acquisition of startup Coefficient Bio.

telegram · zaihuapd · Sep 18, 13:17

**「Background」** The move reflects a broader trend of applying large language models to scientific research, particularly in automating laboratory workflows through AI-directed robotics. Anthropic&\#x27;s expansion into wet-lab biology follows its development of Claude Science, a software platform designed to support scientific research tasks.

**「Impact」** By integrating Claude AI with lab robotics, Anthropic aims to accelerate experimental design and execution in rare disease research, potentially shortening early-stage discovery cycles. However, the company&\#x27;s decision to avoid clinical trials limits its immediate impact on drug development pipelines, keeping it focused on preclinical research rather than competing directly with established pharmaceutical firms.

**Tags**: `#AI drug discovery`, `#biotech`, `#robotics`, `#rare diseases`, `#Anthropic`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Two Techniques for Programming with System One Models](https://seangoedecke.com/two-techniques-for-working-with-system-one-models/) ⭐️ 8.0/10

rss · Sean Goedecke · Sep 18, 00:00

**「Background」** System One models like Jev output only decisions—answers to multiple-choice questions—making them fast but inflexible compared to traditional LLMs. The author explores how to program with these models by turning any LLM into a fast classifier using structured output and single-token generation, then building real demos \(Doom and Wikiracing\) to test practical techniques.

**「Solution」** The first technique, tiered goals, addresses the limited compute of a single 200ms forward pass. In the Doom demo, simply providing game inputs as choices led the model to hold down &\#x27;shoot&\#x27; constantly and wander aimlessly. The fix was to periodically ask the model to choose short-term goals \(e.g., &\#x27;collect armor&\#x27;, &\#x27;kill enemies&\#x27;\) and include that goal in the fast inner loop prompt. This mirrors multi-timescale planning used in game and robotics AI: a 10-second strategic loop, a 5-second tactical loop, a 1-second target breakdown, and a 100ms input loop. The second technique, tournament sampling, tackles the problem of large choice spaces. Wikiracing requires navigating from &\#x27;baseball&\#x27; to &\#x27;sun&\#x27; across over a thousand Wikipedia links, but System One models cap at ~255 choices. Jev&\#x27;s two-stage scoring approach failed because Qwen3-8B assigned similar top scores to hundreds of links. Instead, the author fed 100 links at a time, selected the best, then ran a second pass with chosen links. This worked well, finding the optimal three-link path, because ordinary LLMs excel at relative judgments over absolute ratings. The author notes labels \(associating tokens with choices\) outperformed indexes for Wikiracing but not Doom, and that an H100 achieved 190ms decision loops versus 500ms on a 4090.

**「Takeaway」** System One models—fast, decision-only classifiers—are a promising alternative to tool-calling LLMs for real-time applications, and can be programmed effectively using tiered goals for multi-timescale planning and tournament sampling for handling large choice spaces, though they remain larger and slower than task-specific classifiers.

**Tags**: `#system-one-models`, `#structured-output`, `#real-time-ai`, `#prompt-engineering`, `#llm-classification`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Warren Buffett Steps Down as Berkshire Hathaway Chairman After 61 Years](https://www.cnbc.com/2026/09/18/buffett-stepping-down-as-berkshire-chairman.html) ⭐️ 8.0/10

Warren Buffett, 96, is stepping down as chairman of Berkshire Hathaway after 61 years, with his son Howard Buffett taking over the role as part of a long-standing succession plan. Buffett will become chairman emeritus while remaining a board member, and Greg Abel — who already took over as CEO in late 2025 — will continue running the company&\#x27;s day-to-day operations.

rss · CNBC Finance · Sep 18, 12:04

**「Background」** Buffett transformed Berkshire from a struggling textile mill into a $1 trillion conglomerate with $44.5 billion in operating earnings last year and a 19.7% compounded annual return to shareholders, nearly double the S&amp;P 500&\#x27;s performance. The leadership transition was already underway, with Abel becoming CEO in November 2025, and Buffett cited his age and physical limitations as reasons for stepping back from the chairman role.

**「Impact」** The change marks the end of an era for one of the world&\#x27;s most influential investors and shifts focus to whether Abel can effectively deploy Berkshire&\#x27;s $365.5 billion cash pile, especially after the company&\#x27;s underwhelming 1% stock gain in 2026 compared to the S&amp;P 500&\#x27;s 11% rally.

**Tags**: `#Corporate governance`, `#Leadership transition`, `#Berkshire Hathaway`, `#Investment management`, `#Market impact`

---

<a id="item-finance-news-2"></a>
### [China&\#x27;s Housing Regulator Declares &\#x27;Stock Era&\#x27; as Secondary Market Share Surpasses Half](https://www.peopleapp.com/column/30053168917-500007704534) ⭐️ 7.0/10

China&\#x27;s Ministry of Housing and Urban-Rural Development stated that the property market has entered a &\#x27;stock era,&\#x27; with secondary home transactions rising from 27% in 2020 to 52% in the first eight months of 2026.

telegram · zaihuapd · Sep 18, 02:29

**「Background」** The shift reflects a structural change in supply-demand dynamics, as new home sales decline relative to resales of existing homes, according to an official statement reported by People&\#x27;s Daily.

**「Impact」** The growing dominance of the secondary market may reduce demand for new construction, affecting developers and related industries that rely on land sales and new project launches.

**Tags**: `#housing market`, `#real estate`, `#policy`, `#supply and demand`, `#secondary market`

---

<a id="item-finance-news-3"></a>
### [Chinese Yuan Hits Four-Year High as PBOC Raises Daily Midpoint for Eighth Session](https://www.bloomberg.com/news/articles/2026-09-18/chinese-yuan-hits-strongest-level-since-2022-after-pboc-fixing) ⭐️ 7.0/10

The Chinese yuan reached a four-year high, with offshore yuan rising 0.1% to 6.6957 per dollar, its strongest level since July 2022, as the People&\#x27;s Bank of China raised the daily midpoint for an eighth consecutive session, the longest streak since 2023.

telegram · zaihuapd · Sep 18, 03:00

**「Background」** The PBOC&\#x27;s daily midpoint is a policy-guided reference rate that sets the center of the yuan&\#x27;s permitted trading band each day, and the recent upward adjustments have come ahead of a planned meeting between Chinese President Xi Jinping and U.S. President Donald Trump, with trade tensions expected to be a focus.

**「Impact」** The strengthening yuan makes imports cheaper and boosts the purchasing power of Chinese consumers, while making Chinese exports more expensive for foreign buyers, potentially affecting exporters and multinational companies relying on yuan-denominated costs.

**Tags**: `#Chinese yuan`, `#PBOC`, `#currency policy`, `#trade tensions`, `#foreign exchange`

---
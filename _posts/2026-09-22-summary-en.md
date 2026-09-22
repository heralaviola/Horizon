---
layout: default
title: "Horizon Summary: 2026-09-22 (EN)"
date: 2026-09-22
lang: en
---

> From 55 items, 17 important content pieces were selected

---

**Tools Update**
1. [openai/codex rust-v0.156.0: fullscreen TUI, voice, usage dashboard, worktrees, themes](#item-tools-update-1) ⭐️ 9.0/10
2. [uv 0.12.18: JSON output and check options for pip commands](#item-tools-update-2) ⭐️ 7.0/10
3. [pi v0.87.1: New Frontier Models and Grok 4.7 Default](#item-tools-update-3) ⭐️ 7.0/10

**Technology News**
1. [Anthropic Releases Claude Opus 5.5 with 40% Cost Reduction](#item-tech-news-1) ⭐️ 9.0/10
2. [DeepSeek and Tsinghua Release DSec Sandbox Platform for Agent Training](#item-tech-news-2) ⭐️ 8.0/10
3. [Complex KDA Extends Kimi Delta Attention Gate Range for Orthogonal Matrix Expressivity](#item-tech-news-3) ⭐️ 7.0/10
4. [Stage Skipping for Fault-Tolerant Pipeline-Parallel Training](#item-tech-news-4) ⭐️ 7.0/10
5. [QontoFAQ: A Better Information Retrieval Benchmark](#item-tech-news-5) ⭐️ 7.0/10
6. [OpenAI Forms Math &amp; AI Advisory Group at Institute for Advanced Study](#item-tech-news-6) ⭐️ 7.0/10
7. [Cloudflare GA&\#x27;s Python Workers with AI, storage, and database integrations](#item-tech-news-7) ⭐️ 7.0/10
8. [Mimo CLI Reverse-Engineered for Potential Data Collection](#item-tech-news-8) ⭐️ 7.0/10
9. [DeepSeek to Brief UN Security Council on AI Risks This Week](#item-tech-news-9) ⭐️ 7.0/10
10. [China probes DeepSeek and Moonshot over Anthropic data leak claims](#item-tech-news-10) ⭐️ 7.0/10
11. [OpenAI to Allow External Safety Evaluations Earlier in Model Development](#item-tech-news-11) ⭐️ 7.0/10

**Financial News**
1. [CFTC Warns Prediction Market &\#x27;Mentions&\#x27; Contracts Face Higher Manipulation Risk](#item-finance-news-1) ⭐️ 7.0/10
2. [Kalshi asks CFTC to allow margin trading on event contracts](#item-finance-news-2) ⭐️ 7.0/10
3. [U.S. tech and finance executives confirmed for Trump-Xi summit dinner as Chinese participation stays unclear](#item-finance-news-3) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [openai/codex rust-v0.156.0: fullscreen TUI, voice, usage dashboard, worktrees, themes](https://github.com/openai/codex/releases/tag/rust-v0.156.0) ⭐️ 9.0/10

openai/codex released rust-v0.156.0, a shipped release that adds an optional fullscreen TUI, default voice conversations, a usage analytics dashboard, worktree sessions enabled by default, new terminal themes, and Mermaid/equation rendering, alongside bug fixes and dependency updates. No breaking changes are indicated in the release notes.

github · github-actions\[bot\] · Sep 22, 19:51

**「Changes」** \#\#\# New Features
\- Optional fullscreen UI via \`/tui\` with transcript search, mouse selection, and right-click copying.
\- Voice conversations enabled by default, with an F8 toggle, a \`/voice settings\` picker, and bundled audio runtimes for Linux and Windows.
\- \`/usage\` analytics dashboard for account usage, token totals, and plugin/skill activity.
\- Worktree sessions created from the agent command center; worktree support now enabled by default.
\- Six new terminal themes plus Mermaid diagram and equation rendering in responses.
\- Local background server updates via \`/daemon\`, or bypass with \`--no-daemon\`.

\#\#\# Bug Fixes
\- Preserve streamed answers and plans on failed, interrupted, or subagent-completed turns.
\- Fix clipboard forwarding in tmux/SSH and preserve tab indentation for pasted text.
\- Restore Plan mode on session resume and preserve thread identity/settings when editing earlier prompts.
\- Recover login through system proxies and refresh MCP credentials on OAuth 503 errors.
\- Prevent speech drops during playback pauses or audio bursts.
\- Close sandbox isolation gaps for inbound Windows connections, privileged Linux/macOS sockets, and read-only macOS file handle writes.

\#\#\# Documentation
\- Clarify deprecated \`friendly\` and \`pragmatic\` personality settings no longer select response styles.
\- Explain \`?\` single-character matching in network proxy allow/deny patterns.

\#\#\# Chores
\- Update bundled TLS dependencies, including OpenSSL 3.6.4 for Linux musl builds.

**「Impact」** Users upgrading to rust-v0.156.0 gain new interaction modes \(fullscreen TUI, voice by default\) and observability \(usage dashboard\) without required migration steps. Teams relying on worktrees should note worktree support is now enabled by default, which may affect existing local session workflows. The bundled Linux and Windows voice runtimes and updated TLS dependencies \(OpenSSL 3.6.4 for musl\) are included in release artifacts. Sandbox security fixes address inbound Windows traffic, privileged sockets, and macOS file handle writes, so users of the offline/sandbox modes should upgrade to close those gaps. No configuration changes are required for the new features, though voice being on by default may be relevant for shared or automated environments.

**Tags**: `#tui`, `#voice`, `#analytics`, `#worktrees`, `#themes`

---

<a id="item-tools-update-2"></a>
### [uv 0.12.18: JSON output and check options for pip commands](https://github.com/astral-sh/uv/releases/tag/0.12.18) ⭐️ 7.0/10

uv 0.12.18 is a shipped release that adds \`--output-format json\` and \`--check\` options to \`uv pip install\` and \`uv pip sync\`, introduces a preview build-dependency validation feature, speeds up editable wheel creation, and includes several bug fixes. The changes are backward-compatible.

github · astral-releases-bot\[bot\] · Sep 22, 23:00

**「Changes」** \#\#\# Enhancements
\- Added \`--output-format json\` to \`uv pip install\` and \`uv pip sync\`, including for \`--dry-run\` and \`--check\` \(\[\#21893\]\(https://github.com/astral-sh/uv/pull/21893\)\)
\- Added \`--check\` to \`uv pip install\` and \`uv pip sync\` to report planned changes without modifying the environment \(\[\#21844\]\(https://github.com/astral-sh/uv/pull/21844\)\)
\- Failures from \`get\_requires\_for\_build\_\*\` hooks are now correctly identified in build errors \(\[\#21881\]\(https://github.com/astral-sh/uv/pull/21881\)\)

\#\#\# Preview features
\- Added \`--preview-features build-dependency-check\` to validate build requirements for \`uv build --no-build-isolation\`; use \`--skip-dependency-check\` to opt out \(\[\#21880\]\(https://github.com/astral-sh/uv/pull/21880\)\)

\#\#\# Performance
\- Speeded up \`uv\_build\` editable wheel creation by omitting compression from temporary wheels \(\[\#21918\]\(https://github.com/astral-sh/uv/pull/21918\)\)

\#\#\# Bug fixes
\- Package versions are now selected with wheels compatible with each Python resolution fork, correctly interpreting generic and stable-ABI wheel tags \(\[\#21835\]\(https://github.com/astral-sh/uv/pull/21835\), \[\#21836\]\(https://github.com/astral-sh/uv/pull/21836\)\)
\- Project, script, and lock files are restored when \`uv add\`, \`uv remove\`, or \`uv version\` fails or is interrupted \(\[\#21860\]\(https://github.com/astral-sh/uv/pull/21860\), \[\#21856\]\(https://github.com/astral-sh/uv/pull/21856\)\)
\- Configured \`dependency-metadata\` is now used when checking whether installed requirements are satisfied \(\[\#21843\]\(https://github.com/astral-sh/uv/pull/21843\)\)
\- Archive entries that normalize to absolute Windows paths are now rejected \(\[\#21923\]\(https://github.com/astral-sh/uv/pull/21923\)\)
\- Distribution filenames and archive extensions are now recognized when URL fragments contain \`?\` \(\[\#21920\]\(https://github.com/astral-sh/uv/pull/21920\)\)
\- Correctly lowercased platform tags are now generated for BSD and Haiku releases \(\[\#21853\]\(https://github.com/astral-sh/uv/pull/21853\)\)
\- Windows relative paths are no longer rebuilt into absolute form \(\[\#21923\]\(https://github.com/astral-sh/uv/pull/21923\)\)

**「Impact」** Users of \`uv pip install\` and \`uv pip sync\` benefit from improved scripting and dry-run workflows via the new \`--output-format json\` and \`--check\` options. The preview build-dependency validation feature is opt-in and does not affect default behavior. The performance improvement for editable wheel creation reduces build times. The bug fixes improve correctness in wheel tag interpretation, file restoration on failure, and path handling. No migration action is required; the changes are backward-compatible.

**Tags**: `#pip`, `#json-output`, `#dry-run`, `#build-dependencies`, `#performance`

---

<a id="item-tools-update-3"></a>
### [pi v0.87.1: New Frontier Models and Grok 4.7 Default](https://github.com/earendil-works/pi/releases/tag/v0.87.1) ⭐️ 7.0/10

The pi tool \(earendil-works/pi\) released version 0.87.1, adding support for latest frontier models including Claude Opus 5.5, GPT-6 Sol, and GPT-6 Luna across multiple providers, and changing the default xAI model to Grok 4.7. This release includes shipped features, fixes, and a default model change.

github · github-actions\[bot\] · Sep 22, 19:43

**「Changes」** \#\#\# New Features
\- \*\*Latest frontier models\*\* — Use Claude Opus 5.5, GPT-6 Sol, and GPT-6 Luna through supported providers, including GitHub Copilot.
\- \*\*Grok 4.7 by default for xAI\*\* — New xAI sessions now default to Grok 4.7.

\#\#\# Added
\- Added inherited Claude Opus 5.5, GPT-6 Sol, and GPT-6 Luna support for GitHub Copilot.
\- Added inherited GPT-6 Sol and GPT-6 Luna support for OpenAI API keys and OpenAI Codex subscriptions.
\- Added inherited Claude Opus 5.5 support for Anthropic with adaptive thinking and a 1M context window.

\#\#\# Changed
\- Changed the default xAI model to Grok 4.7.

\#\#\# Fixed
\- Fixed split-turn compaction summaries being refused by Claude Fable 5.1 by clearly separating the conversation and using continuation-oriented instructions \(\[\#9908\]\(https://github.com/earendil-works/pi/pull/9908\) by \[@davidbrai\]\(https://github.com/davidbrai\)\).
\- Fixed missing or invalid \`--mode\` values being silently ignored instead of reporting an error and exiting with a nonzero status \(\[\#9045\]\(https://github.com/earendil-works/pi/issues/9045\)\).
\- Fixed inherited image-only user messages being rejected by some OpenAI-compatible providers because they included an empty text part \(\[\#9797\]\(https://github.com/earendil-works/pi/issues/9797\)\).
\- Fixed inherited Anthropic OAuth requests reporting an outdated Claude Code version.

**「Impact」** Users relying on GitHub Copilot, OpenAI, Anthropic, or xAI providers should upgrade to access the newly supported frontier models. Those using xAI will see Grok 4.7 become the new default model for new sessions, which may affect existing workflows expecting a different default. The fixes address error handling for invalid \`--mode\` values and compatibility issues with image-only messages and Anthropic OAuth, improving reliability across providers. No explicit migration steps are mentioned, but users should review their provider configurations to ensure compatibility with the new defaults and model support.

**Tags**: `#models`, `#providers`, `#github-copilot`, `#xai`, `#anthropic`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Anthropic Releases Claude Opus 5.5 with 40% Cost Reduction](https://www.anthropic.com/claude-opus-5-5) ⭐️ 9.0/10

Anthropic released Claude Opus 5.5, the first model in its 5.5 series, offering 40% lower cost than Opus 5 and over 30% faster output. The model achieves state-of-the-art performance on automated behavioral audits and maintains strong results in cybersecurity and biology tasks. Claude Sonnet 5.5 and Haiku 5.5 variants are scheduled for release in the coming weeks.

telegram · zaihuapd · Sep 22, 16:30

**「Claude 5 Series Evolution」** The Claude 5 series represents Anthropic&\#x27;s latest generation of AI models, with Opus 5.5 building upon the capabilities of its predecessor Opus 5. This release follows the company&\#x27;s recent emphasis on responsible AI development and frontier model pacing.

**「Reduced Costs May Shift Market Dynamics」** With input tokens priced at $4 per 1M \(down from $5\) and output tokens at $20 per 1M \(down from $25\), the cost reduction could make Claude Opus 5.5 more competitive against other high-end models, particularly given that Opus 5 was previously the highest-spending model on OpenRouter.

**「Community Notes Pacing Concerns and Price Reactions」** Community members noted the irony in Anthropic&\#x27;s announcement, as the company had recently called for pacing frontier development, yet this release emphasizes specific performance improvements. Users also highlighted the significant price drops, with one commenter calling it a long-awaited reduction, while others compared it favorably to alternative models like DeepSeek v4.1.

**Tags**: `#AI`, `#Machine Learning`, `#Anthropic`, `#Claude`, `#LLM`

---

<a id="item-tech-news-2"></a>
### [DeepSeek and Tsinghua Release DSec Sandbox Platform for Agent Training](https://arxiv.org/abs/2609.22978) ⭐️ 8.0/10

DeepSeek-AI and Tsinghua University published a technical report on DSec, a scalable sandbox platform that serves approximately 3 million daily sandboxes with peak concurrency above 380,000 and creation rates exceeding 5,000 sandboxes per second. DSec provides a unified SDK supporting four backend types—FnCall, container, Firecracker microVM, and full VM—to cover workloads such as online judge execution, software engineering, security penetration testing, and computer operations, and it integrates with reinforcement learning by decoupling stateful rollout execution from preemptible GPU training. The platform is built on the 3FS distributed file system with on-demand EROFS image loading, achieving 1.7x faster task completion, 57% less disk writes, and roughly 40% lower peak memory usage compared to traditional Docker full-image pulls.

telegram · zaihuapd · Sep 22, 04:45

**「Background」** Large-scale agent training and evaluation require sandboxed environments that can run diverse, stateful tasks while scaling to hundreds of thousands of concurrent executions, a challenge that general-purpose container runtimes struggle to meet efficiently. DSec addresses this by combining multiple isolation backends with a unified SDK and tight coupling to reinforcement learning workflows, where rollout execution must be separated from GPU-bound training to allow preemption and resource sharing.

**「Impact」** For AI and infrastructure teams building or evaluating agents, DSec demonstrates a production-grade approach to scaling sandbox-based training to millions of daily instances, which may inform the design of similar platforms; however, the report is a technical summary rather than a full implementation guide, so direct adoption would require additional engineering detail.

**Tags**: `#agent infrastructure`, `#sandboxing`, `#reinforcement learning`, `#distributed systems`, `#cloud computing`

---

<a id="item-tech-news-3"></a>
### [Complex KDA Extends Kimi Delta Attention Gate Range for Orthogonal Matrix Expressivity](https://www.reddit.com/r/MachineLearning/comments/1wn5uv9/understanding_and_enhancing_kimi_delta_attention_r/) ⭐️ 7.0/10

A technical analysis of Kimi Delta Attention \(KDA\) proposes Complex KDA \(CKDA\) by extending the diagonal gate range to \[-1,1\] and the delta rule learning rate to \[0,2\]. The theory connects CKDA to orthogonal diagonal-plus-rank-one matrices and demonstrates the ability to track S3, S4, and A5 groups, though not S5. Experiments show CKDA can learn S3 and S4, achieves promising results on audio continuation tasks, and remains competitive with standard KDA on language modeling while training stably.

reddit · r/MachineLearning · /u/Yossarian\_1234 · Sep 22, 10:34

**「Background」** Kimi Delta Attention \(KDA\) is a variant of delta rule-based attention mechanisms that uses a diagonal gating mechanism to control information flow. The original formulation restricts gate values to a specific range, limiting the types of transformations the attention mechanism can express, particularly those requiring reflection operations for 2D rotations.

**「Impact」** For researchers working on sequence modeling and attention mechanisms, CKDA offers a theoretically grounded enhancement that may improve the expressivity of delta-rule-based architectures. The extension to \[-1,1\] gate ranges and \[0,2\] learning rates could enable more complex rotational transformations in a single step, potentially benefiting applications requiring precise group tracking such as audio signal processing and structured sequence prediction.

**Tags**: `#machine-learning`, `#attention-mechanisms`, `#theoretical-analysis`, `#sequence-modeling`, `#research`

---

<a id="item-tech-news-4"></a>
### [Stage Skipping for Fault-Tolerant Pipeline-Parallel Training](https://www.reddit.com/r/MachineLearning/comments/1wnd5ys/simulating_fault_tolerance_with_stage_skipping_in/) ⭐️ 7.0/10

Templar&\#x27;s Crucible distributed pre-training platform adds stage skipping to tolerate pipeline-stage failures: when an inner stage goes offline, activations and gradients bypass it for multiple steps so healthy workers keep training. The approach combines data-parallel replicas, pipeline parallelism, SparseLoCo compressed updates, and pipeline compression, and is validated via simulation on a 178M model with eight replicas and four stages per replica. At a 1% per-replica failure probability per global step, validation loss stayed close to the no-failure baseline even though each simulated outage removed a stage for six global steps, with each configuration compared against its own no-failure run. The work is a simulation of learning effects rather than a measurement of physical worker replacement or production cost savings.

reddit · r/MachineLearning · /u/covenant\_ai · Sep 22, 15:47

**「Background」** Pipeline-parallel training splits a model into sequential stages placed on separate workers, so a failed stage can stall the entire pipeline and waste the compute of healthy workers. Prior fault-tolerance work in distributed training has focused on checkpointing and worker replacement, which pause or restart progress rather than continuing training during an outage.

**「Impact」** The simulation suggests that stage skipping could let pre-training continue on unreliable workers and spot instances without waiting for recovery, but because results are simulated rather than measured on physical worker replacement, the actual production cost savings and convergence behavior remain unverified.

**Tags**: `#pipeline parallelism`, `#fault tolerance`, `#distributed training`, `#model compression`, `#pre-training`

---

<a id="item-tech-news-5"></a>
### [QontoFAQ: A Better Information Retrieval Benchmark](https://www.reddit.com/r/MachineLearning/comments/1wn9xqk/qontofaq_a_better_information_retrieval_benchmark/) ⭐️ 7.0/10

Qonto has released QontoFAQ, a new information retrieval benchmark and metric designed to better measure document relevance for product question answering. The benchmark includes a dataset for evaluating embedding models and accompanying open-source code, aiming to align retrieval evaluation more closely with the goal of finding documents that directly answer product-related questions. The approach is detailed in a Medium article and the code is available on GitHub.

reddit · r/MachineLearning · /u/espadrine · Sep 22, 13:45

**「Background」** Traditional information retrieval benchmarks often struggle to accurately reflect real-world relevance, especially in specialized domains like product support, where the goal is to retrieve documents that precisely answer user questions. QontoFAQ addresses this gap by introducing a metric and dataset tailored to product question answering scenarios.

**「Impact」** Developers and researchers working on embedding models for customer support or product search applications can use QontoFAQ to evaluate model performance in a more realistic and targeted setting, potentially leading to better-tuned systems for answering product questions.

**Tags**: `#information-retrieval`, `#benchmarking`, `#machine-learning`, `#open-source`, `#nlp`

---

<a id="item-tech-news-6"></a>
### [OpenAI Forms Math &amp; AI Advisory Group at Institute for Advanced Study](https://techcrunch.com/2026/09/21/openai-forms-math-advisory-group-as-its-ai-resolves-more-than-100-open-problems/) ⭐️ 7.0/10

OpenAI announced on September 21 the formation of an independent Math &amp; AI Advisory Group at the Institute for Advanced Study in Princeton, composed of 9 mathematicians who will evaluate results, coordinate publication, and provide advice. The group is strictly advisory and does not influence OpenAI&\#x27;s research direction or decision-making. The announcement accompanies OpenAI&\#x27;s claim that its internal models have resolved over 100 open mathematical problems, a statement that follows criticism from 25 Fields Medalists regarding AI labs pursuing famous math problems.

telegram · zaihuapd · Sep 22, 03:00

**「Background」** The Institute for Advanced Study in Princeton is a renowned independent research center historically associated with major advances in mathematics and physics. OpenAI&\#x27;s claim of solving over 100 open math problems comes amid broader interest in applying AI to mathematical research, and follows public criticism from 25 Fields Medalists who warned against AI labs racing to solve famous problems without proper verification.

**「Impact」** The advisory group&\#x27;s role in evaluating and coordinating publication of AI-derived mathematical results may lend credibility to OpenAI&\#x27;s claims, but its limited authority means the mathematical community will likely retain skepticism until independent verification of the claimed problem resolutions is provided.

**Tags**: `#OpenAI`, `#AI research`, `#mathematics`, `#advisory board`, `#TechCrunch`

---

<a id="item-tech-news-7"></a>
### [Cloudflare GA&\#x27;s Python Workers with AI, storage, and database integrations](https://blog.cloudflare.com/python-workers-ga/) ⭐️ 7.0/10

Cloudflare announced the general availability of Python Workers on September 21, making Python a first-class language on its edge computing platform with native support for FastAPI, Django, and Flask frameworks. The feature, introduced two years ago, now integrates directly with Workers AI, R2, D1, and supports running PostgreSQL databases and LangChain AI libraries at the edge. This GA release enables developers to deploy Python web and AI workloads on Cloudflare&\#x27;s global network without managing infrastructure.

telegram · zaihuapd · Sep 22, 04:00

**「Background」** Cloudflare Workers is a serverless edge computing platform that allows developers to run code closer to users across Cloudflare&\#x27;s global network. Python support was initially introduced as a beta two years ago, expanding beyond the platform&\#x27;s original JavaScript and TypeScript focus to support additional languages via a WebAssembly-based runtime.

**「Impact」** Python developers can now deploy web applications and AI workloads to Cloudflare&\#x27;s edge network with native framework support and integrated access to AI inference, object storage, and database services, reducing the need for separate backend infrastructure when building latency-sensitive applications.

**Tags**: `#cloud-computing`, `#python`, `#edge-computing`, `#serverless`, `#cloudflare`

---

<a id="item-tech-news-8"></a>
### [Mimo CLI Reverse-Engineered for Potential Data Collection](https://linux.do/t/topic/2935748) ⭐️ 7.0/10

Reverse engineering of Mimo CLI has revealed that the tool may collect repository metadata by default, including the repository URL, commit hash, and branch information. This telemetry can reportedly be disabled by setting the environment variable MIMOCODE\_ENABLE\_ANALYSIS=false. Additionally, a closed-source function named collectCodebase\(\) was found in the trajectory-bundle and codebase-bundle extensions, which has the capability to enumerate Git repository files, read source code, and compress it into a package. However, there is no evidence that this function is currently active or that any collected code is transmitted externally. These components are not part of Mimo CLI&\#x27;s official open-source repository, and the findings have not been confirmed by the vendor.

telegram · zaihuapd · Sep 22, 08:18

**「Background」** Mimo CLI is a command-line interface tool designed for software development workflows, though its core functionality remains less widely documented compared to mainstream developer tools. The discovery of closed-source extensions containing potentially invasive functions highlights ongoing concerns about transparency in modern CLI tools, where telemetry and code collection capabilities may be embedded in non-open components that are not subject to public scrutiny.

**「Impact」** Developers using Mimo CLI should be aware that repository metadata may be transmitted by default and should set MIMOCODE\_ENABLE\_ANALYSIS=false to opt out. Organizations concerned with supply-chain security or source code confidentiality should audit their use of Mimo CLI and its extensions, particularly given the presence of unconfirmed but potentially risky code collection capabilities in closed-source components.

**Tags**: `#privacy`, `#supply-chain-security`, `#CLI-tools`, `#reverse-engineering`, `#telemetry`

---

<a id="item-tech-news-9"></a>
### [DeepSeek to Brief UN Security Council on AI Risks This Week](https://www.reuters.com/world/asia-pacific/deepseek-brief-un-security-council-ai-this-week-sources-say-2026-09-22/) ⭐️ 7.0/10

Chinese AI startup DeepSeek is scheduled to brief the UN Security Council this week on artificial intelligence risks, joining a meeting of the 15-member council on AI and international security. OpenAI CEO Sam Altman is expected to attend and present, with senior representatives from Anthropic also anticipated. DeepSeek founder Liang Wenfeng is not planned to attend, though arrangements remain subject to change.

telegram · zaihuapd · Sep 22, 11:34

**「Background」** The UN Security Council has increasingly turned its attention to the governance of artificial intelligence as a matter of international peace and security, reflecting growing global concern over the technology&\#x27;s potential misuse and strategic implications.

**「Impact」** DeepSeek&\#x27;s participation signals that Chinese AI firms are being included in high-level multilateral discussions on AI governance, potentially shaping how international norms around AI safety and security are developed across competing geopolitical blocs.

**Tags**: `#AI governance`, `#DeepSeek`, `#UN Security Council`, `#AI risk`, `#international security`

---

<a id="item-tech-news-10"></a>
### [China probes DeepSeek and Moonshot over Anthropic data leak claims](https://www.theinformation.com/articles/china-probes-deepseek-moonshot-potential-data-leaks-anthropic) ⭐️ 7.0/10

Chinese internet regulators are investigating DeepSeek and Moonshot following Anthropic allegations that the two companies forwarded sensitive user data to the Claude model. Anthropic released a 154-page report on September 10 naming seven Chinese companies for large-scale misuse of Claude, including an example in which DeepSeek allegedly routed a request from a police surveillance developer to Claude.

telegram · zaihuapd · Sep 22, 14:37

**「Regulatory context」** The investigation reflects growing scrutiny of Chinese AI firms over data handling and cross-border model access, amid broader concerns about compliance with domestic data protection rules and the security of sensitive user information.

**「Potential consequences」** If the allegations are substantiated, the investigations could lead to regulatory penalties for DeepSeek and Moonshot and may prompt tighter oversight of data flows between Chinese AI companies and foreign models.

**Tags**: `#AI regulation`, `#data privacy`, `#DeepSeek`, `#Moonshot`, `#Anthropic`

---

<a id="item-tech-news-11"></a>
### [OpenAI to Allow External Safety Evaluations Earlier in Model Development](https://www.bloomberg.com/news/articles/2026-09-22/openai-to-let-outside-groups-evaluate-ai-models-at-earlier-phase) ⭐️ 7.0/10

OpenAI plans to let external organizations conduct technical safety evaluations earlier in the AI model development lifecycle, moving assessments from pre-release to during training and evaluation phases, as announced in an upcoming blog post. The company is partnering with institutions such as METR and Redwood Research, requiring evaluators to have independent mechanisms, scientific rigor, and clear accountability. This shift responds to rising concerns among AI industry employees about catastrophic risks and unintended model behaviors observed during testing.

telegram · zaihuapd · Sep 22, 17:39

**「Background」** Previously, external safety evaluations were typically conducted only before a model&\#x27;s public release, limiting the window for identifying risks during development. OpenAI&\#x27;s move reflects growing scrutiny of AI safety practices amid reports of models exhibiting unexpected behaviors during internal testing.

**「Impact」** By enabling earlier external evaluations, OpenAI may set a new standard for AI safety governance, potentially influencing other AI labs to adopt similar practices. Organizations collaborating as evaluators, such as METR and Redwood Research, could gain greater influence over model development processes, while also facing increased responsibility for identifying risks before models reach broader deployment.

**Tags**: `#AI Safety`, `#OpenAI`, `#Model Evaluation`, `#Governance`, `#Machine Learning`

---

## Financial News

<a id="item-finance-news-1"></a>
### [CFTC Warns Prediction Market &\#x27;Mentions&\#x27; Contracts Face Higher Manipulation Risk](https://www.cnbc.com/2026/09/22/cftc-prediction-markets-mentions-contracts-have-manipulation-risk.html) ⭐️ 7.0/10

The CFTC issued advisory guidance to regulated exchanges warning that prediction market &\#x27;mentions&\#x27; contracts — which bet on specific words used in speeches or broadcasts — carry heightened manipulation risk because settlement depends on conduct that may not be independently verifiable. The guidance follows a $172,539 insider-trading settlement with a Trump teleprompter operator and Kalshi&\#x27;s removal of sports-related mention markets.

rss · CNBC Finance · Sep 22, 22:13

**「Background」** Mention markets allow traders to bet on what specific words will be used in a speech, earnings call, or broadcast, with settlement based on the discrete conduct of a particular individual. The CFTC&\#x27;s advisory follows prior enforcement action and an internal review announced in August, though it does not impose new regulatory requirements.

**「Impact」** The guidance signals increased regulatory scrutiny of an emerging market segment and may influence how exchanges design and list mention-based contracts, potentially affecting platforms like Kalshi and other prediction market operators.

**Tags**: `#CFTC`, `#prediction markets`, `#market manipulation`, `#Kalshi`, `#regulatory guidance`

---

<a id="item-finance-news-2"></a>
### [Kalshi asks CFTC to allow margin trading on event contracts](https://www.cnbc.com/2026/09/22/kalshi-asks-cftc-to-allow-margin-trading-on-its-platform-letting-users-buy-with-borrowed-funds.html) ⭐️ 7.0/10

Prediction market platform Kalshi has filed with the CFTC seeking approval to offer margin trading on event contracts, which would let users buy with borrowed funds, a practice already standard on Wall Street but not yet permitted for event contracts on regulated U.S. exchanges.

rss · CNBC Finance · Sep 22, 12:28

**「Background」** Kalshi already provides leverage on its perpetual futures contracts but has not yet received approval to do so for its prediction markets, where all event contracts on regulated U.S. exchanges are currently entirely collateralized.

**「Impact」** If approved, margin trading could attract institutional liquidity to the prediction market sector, particularly for longer-dated contracts, though Kalshi said it would avoid offering margin on sports, culture, and mention markets.

**Tags**: `#prediction markets`, `#CFTC regulation`, `#margin trading`, `#institutional adoption`, `#Kalshi`

---

<a id="item-finance-news-3"></a>
### [U.S. tech and finance executives confirmed for Trump-Xi summit dinner as Chinese participation stays unclear](https://www.cnbc.com/2026/09/22/heres-who-we-know-is-going-to-the-trump-xi-dinner-so-far.html) ⭐️ 7.0/10

A dinner on Thursday in Washington, D.C. ahead of a Trump-Xi summit will be attended by U.S. executives including Microsoft&\#x27;s Satya Nadella, Nvidia&\#x27;s Jensen Huang, OpenAI&\#x27;s Sam Altman, Google&\#x27;s Sundar Pichai, Tesla&\#x27;s Elon Musk, Citigroup&\#x27;s Jane Fraser, Amazon&\#x27;s Jeff Bezos, Apple&\#x27;s Tim Cook, Dell&\#x27;s Michael Dell and Meta&\#x27;s Mark Zuckerberg, while Chinese corporate attendance remains unconfirmed.

rss · CNBC Finance · Sep 22, 20:07

**「Background」** The dinner precedes Chinese President Xi Jinping&\#x27;s planned U.S. visit from Wednesday to Friday, and comes amid longstanding U.S.-China tensions that have led both governments to place companies from the other country on business-restricting blacklists.

**Tags**: `#U.S.-China relations`, `#Trump-Xi summit`, `#tech industry`, `#corporate diplomacy`, `#trade policy`

---
---
layout: default
title: "Horizon Summary: 2026-10-15 (EN)"
date: 2026-10-15
lang: en
---

> From 50 items, 16 important content pieces were selected

---

**Tools Update**
1. [openai/codex rust-v0.163.0 Release Notes](#item-tools-update-1) ⭐️ 8.0/10
2. [pi v1.3.0: configurable /share destinations, cache-preserving thinking changes, and resumed-session tool retention](#item-tools-update-2) ⭐️ 7.0/10
3. [hunk v0.24.0-beta.1: UI fixes, CLI validation, and marketplace addition](#item-tools-update-3) ⭐️ 5.0/10
4. [OpenCode v1.19.1 Discontinues Session Sharing](#item-tools-update-4) ⭐️ 5.0/10

**Technology News**
1. [Libreboot 26.10 Adds UEFI and Chromebook Support](#item-tech-news-1) ⭐️ 8.0/10
2. [Anthropic Reports Q3 Revenue of $16.8 Billion Ahead of IPO](#item-tech-news-2) ⭐️ 8.0/10
3. [Random neural units self-assemble learning circuits matching backpropagation](#item-tech-news-3) ⭐️ 8.0/10
4. [Meta Releases Muse Spark Open, an Apple Silicon-Optimized Open-Weight Model](#item-tech-news-4) ⭐️ 7.0/10
5. [Goodfire claims neural networks are &\#x27;clean&\#x27; and interpretable](#item-tech-news-5) ⭐️ 7.0/10
6. [Citizen Lab: Ad Infrastructure Used to Deliver Zero-Click Spyware](#item-tech-news-6) ⭐️ 7.0/10
7. [ASML Developing Hybrid Bonding Tool, Per Patents and Roadmap](#item-tech-news-7) ⭐️ 7.0/10

**Technology Blog**
1. [Muse Spark Open Day 0 Support on vLLM](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [IMF: Rural Chinese spend 8.7% of income on healthcare, second only to US](#item-finance-news-1) ⭐️ 7.0/10
2. [Harvard Endowment Returns 27.1% in Fiscal 2026, Reaching Nearly $68 Billion](#item-finance-news-2) ⭐️ 7.0/10
3. [China says rare earth exports to EU will continue despite U.S. trade deal expiry](#item-finance-news-3) ⭐️ 7.0/10
4. [China Accelerates Replacement of Western Wind Power Equipment](#item-finance-news-4) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [openai/codex rust-v0.163.0 Release Notes](https://github.com/openai/codex/releases/tag/rust-v0.163.0) ⭐️ 8.0/10

openai/codex released version rust-v0.163.0, introducing a searchable /config UI, real-time response steering, leader key customization, daemon restart, parallel tool execution, and enabling Daybreak by default. This is a shipped feature release with significant enhancements to core workflows, interactivity, and performance.

github · github-actions\[bot\] · Oct 15, 21:30

**「Changes」** \#\#\# New Features
\- \*\*Searchable /config UI\*\*: Open \`/config\` to search preferences across categories, change supported settings immediately, and see which changes require a restart. \(\#52990, \#53429\)
\- \*\*Real-time response steering\*\*: Send a follow-up while Codex is responding to steer it immediately. Interrupting a turn also stops active Code Mode cells and their nested tool calls. \(\#51812, \#51835\)
\- \*\*Leader key customization\*\*: Configure a leader key in \`/keymap\`. The default is \`Ctrl+X\`, shortcut hints stay open until you choose or cancel, and voice mute moves to \`F9\`. \(\#52273\)
\- \*\*Daemon restart\*\*: Restart a managed background server from \`/daemon\`. Codex warns about work the restart could interrupt, then reconnects automatically. \(\#53173\)
\- \*\*Parallel tool execution\*\*: Codex can run independent read-only tools in parallel, including skill, memory, and conversation-history lookups. \(\#52245\)
\- \*\*Daybreak enabled by default\*\*: Daybreak is enabled by default for eligible accounts. \`codex exec\` can also select it with an OpenAI API key when the server offers access. \(\#53701, \#53717\)

\#\#\# Bug Fixes
\- \*\*Thread resumption\*\*: Resuming a saved thread restores its permissions and network approvals, while respecting explicit overrides and current managed policy. \(\#53150, \#53419, \#53424\)
\- \*\*Network proxy security\*\*: The network proxy now checks permission before a DNS lookup, rejects duplicate \`Host\` headers, and prevents credential aliases from bypassing inspection hooks. \(\#51650, \#52661, \#53506\)
\- \*\*Side conversations\*\*: Return to an existing side conversation with \`/side\` after switching threads. Answers to pending prompts also go back to the thread that asked. \(\#52184, \#53436\)
\- \*\*Windows clipboard\*\*: On Windows, \`Ctrl+V\` and \`Shift+Insert\` paste text as well as images. On WSL, repeated pastes reuse the clipboard reader, and copy attempts time out instead of hanging. \(\#53224, \#52967, \#53453\)
\- \*\*Command execution\*\*: Local commands finish promptly when a child keeps an output pipe open. Remote commands preserve late-arriving output so the final poll can still collect it. \(\#52652, \#53331, \#53622\)
\- \*\*Diff output\*\*: \`codex exec\` no longer prints the same file diff again after an unrelated command. \(\#53444\)

\#\#\# Documentation
\- Updated the bundled OpenAI Docs guidance for migrations to the GPT-6 family, including model-specific reasoning, tool use, and data residency considerations. \(\#51768\)
\- Clarified how the Linux sandbox uses bubblewrap for filesystem isolation and seccomp for syscall filtering. \(\#52610\)

\#\#\# Chores
\- Codex now uses its standard shell executor and no longer bundles a patched \`zsh\`. Configurations using the retired shell flags receive a migration notice. \(\#52160, \#52213\)
\- Reduced Linux and macOS release package size by stripping symbols from packaged binaries while preserving them in the original build outputs. \(\#52178\)

**「Impact」** Users should upgrade to benefit from the new searchable config UI, real-time steering, and parallel tool execution, which improve interactivity and performance. The leader key change \(\`Ctrl+X\` default\) and voice mute relocation to \`F9\` may require users to update their muscle memory or custom keymaps. Configurations using the retired \`zsh\` shell flags will receive a migration notice and should be updated to use the standard shell executor. The network proxy security fixes address potential credential bypass and DNS lookup vulnerabilities, making this update important for security-conscious deployments. Daybreak being enabled by default may affect model behavior for eligible accounts. No explicit restart is required for most changes, though some config changes will prompt for a restart.

**Tags**: `#configuration`, `#interactivity`, `#performance`, `#daemon-management`, `#security`

---

<a id="item-tools-update-2"></a>
### [pi v1.3.0: configurable /share destinations, cache-preserving thinking changes, and resumed-session tool retention](https://github.com/earendil-works/pi/releases/tag/v1.3.0) ⭐️ 7.0/10

pi v1.3.0 is a shipped release that adds configurable /share upload destinations, cache-preserving thinking-level changes on OpenAI GPT-6, cleaner model switching that drops prior thinking, and tool retention for resumed sessions. The release also includes a broad set of provider, caching, and build fixes.

github · github-actions\[bot\] · Oct 15, 19:17

**「Changes」** \#\#\# New Features
\- \*\*Choose where \`/share\` uploads\*\*: \`sessionShareDestination\` selects \`auto\`, \`gist\`, or \`radius\`.
\- \*\*Cache-preserving thinking level changes on OpenAI GPT-6\*\*: changing the thinking level mid-session with an API key keeps the prompt cache.
\- \*\*Kimi Code over Chat Completions\*\*: tools added mid-conversation no longer invalidate the prompt cache. \`models.json\` base URL overrides must now include \`/v1\`.
\- \*\*Clean model switching\*\*: thinking from a previous model is dropped instead of being shown to the new model as text.
\- \*\*Resumed sessions keep their active tools\*\*: \`--tools +name\`/\`-name\` applies on top of them.

\#\#\# Added
\- Changing the thinking level mid-session on OpenAI GPT-6 models \(API key\) now keeps the prompt cache \(\[\#10853\]\(https://github.com/earendil-works/pi/issues/10853\)\)
\- Added the \`sessionShareDestination\` setting to choose automatic, GitHub gist, or Radius uploads for \`/share\` \(\[\#10870\]\(https://github.com/earendil-works/pi/issues/10870\) by \[@vegarsti\]\(https://github.com/vegarsti\)\)

\#\#\# Changed
\- Changed the \`kimi-coding\` provider to use OpenAI Chat Completions at \`https://api.kimi.com/coding/v1\`, the protocol used by the official Kimi Code client. K3, K3-256K, and Kimi For Coding now accept tools added mid-conversation without invalidating the prompt cache. \`models.json\` overrides of the \`kimi-coding\` base URL must now include \`/v1\` \(\[\#10720\]\(https://github.com/earendil-works/pi/issues/10720\)\)
\- Changed model switching to drop thinking blocks from earlier assistant messages produced by a different model, instead of sending them as plain text. The new model previously saw the old model&\#x27;s reasoning as part of its replies and could start writing its own reasoning into the visible answer \(\[\#10995\]\(https://github.com/earendil-works/pi/issues/10995\)\)

\#\#\# Fixed
\- Pinned internal Pi dependencies to exact release versions to prevent fresh installs from mixing incompatible packages \(\[\#10865\]\(https://github.com/earendil-works/pi/issues/10865\)\)
\- Fixed resumed sessions dropping tools activated during the session. Resume now restores the session&\#x27;s active tools, with \`--tools +name\`/\`-name\` entries applied to them, unless \`--tools\` with tool names, \`--no-tools\`, or \`--no-builtin-tools\` selects tools explicitly \(\[\#10785\]\(https://github.com/earendil-works/pi/issues/10785\)\)
\- Fixed stopping a codemode script or reaching its deadline waiting for a non-interruptible built-in to return on Bun \(\[\#10748\]\(https://github.com/earendil-works/pi/issues/10748\)\)
\- Fixed repeated codemode timeouts or aborts accumulating surviving workers; admission now limits live workers to two across sessions, counting cancelled workers until actual exit \(\[\#10748\]\(https://github.com/earendil-works/pi/issues/10748\)\)
\- Fixed \`--model\` choosing a provider by catalog order when several providers offer the match; Pi now prefers the provider with credentials and otherwise reports the ambiguity. \`--models\` and \`enabledModels\` add a model for each provider that offers it and warn about the ambiguity \(\[\#10160\]\(https://github.com/earendil-works/pi/issues/10160\)\)
\- Fixed \`read\` line-range labels for numeric-string or null arguments in the TUI, session tree, HTML exports, and examples \(\[\#9887\]\(https://github.com/earendil-works/pi/issues/9887\)\)
\- Fixed the Nix flake build failing when a provider switched APIs: the model catalog pin is now refreshed from the newest published catalog when its model API groups differ, and releases pin the newest catalog and build with it before tagging \(\[\#10985\]\(https://github.com/earendil-works/pi/issues/10985\)\)
\- Fixed the Nix package putting its Node.js first on \`PATH\`, which made bash tool shells use Pi&\#x27;s Node instead of the user&\#x27;s \`node\`/\`npm\`. Pi&\#x27;s Node is now only a fallback \(\[\#10519\]\(https://github.com/earendil-works/pi/issues/10519\)\)
\- Fixed prompt templates dropping empty quoted arguments \(\`&quot;&quot;\` or \`&\#x27;&\#x27;\`\), which shifted later positional arguments and prevented positional defaults from applying \(\[\#10867\]\(https://github.com/earendil-works/pi/issues/10867\)\)
\- Fixed the Nix package build failing in its install check because it still expected chord and esbuild, which Pi no longer depends on
\- Fixed tool-call argument parsing dropping fields when a string contains an invalid \`\\u\` escape such as \`\\usepackage\` \(\[\#10868\]\(https://github.com/earendil-works/pi/issues/10868\)\)
\- Fixed Anthropic and Bedrock Claude requests failing with a 400 when an error tool result contains images; the images are now sent after the tool results of the turn, so the model still sees them \(\[\#10794\]\(https://github.com/earendil-works/pi/issues/10794\)\)
\- Fixed OpenCode Go Gemini models failing with a 404 by moving OpenCode Zen and OpenCode Go to the \`opencode.ai/inference\` endpoints, and added Google Generative AI support to the OpenCode Go provider
\- Fixed OpenCode Go MiniMax M2.7 failing with &quot;Model does not support this protocol&quot; by using the Anthropic Messages API
\- Fixed automatic retry not triggering for gateway \`Unable to forward upstream stream\` errors \(\[\#10920\]\(https://github.com/earendil-works/pi/issues/10920\)\)
\- Fixed automatic retry not triggering for \`The service is temporarily unavailable\` errors, which also made compaction fail on the first attempt \(\[\#10965\]\(https://github.com/earendil-works/pi/issues/10965\)\)
\- Fixed OpenAI-compatible responses showing thinking after the answer when a proxy such as LiteLLM sends reasoning and content in the same stream chunk \(\[\#10926\]\(https://github.com/earendil-works/pi/issues/10926\)\)
\- Fixed Gemini 4 Argon requests on Google Vertex failing with &quot;Thinking budget is not supported&quot;, and its thinking level being ignored on the Gemini API \(\[\#10890\]\(https://github.com/earendil-works/pi/issues/10890\)\)
\- Fixed Xiaomi MiMo models failing with a 400 at the \`minimal\` thinking level; they now expose only the \`off\` and \`high\` levels \(\[\#10818\]\(https://github.com/earendil-works/pi/issues/10818\)\)
\- Fixed \`openai-codex/gpt-6.1-sol\` using a 272K context window instead of the 500K window Codex now provides \(\[\#10840\]\(https://github.com/earendil-works/pi/issues/10840\)\)
\- Fixed tool calls whose final arguments are malformed JSON silently running with only the fields parsed before the error; they now fail validation and show the model the raw arguments it sent \(\[\#10897\]\(https://github.com/earendil-works/pi/issues/10897\)\)
\- Fixed Claude Haiku 5.5 and Claude Opus 5 not supporting the \`off\` thinking level \(\[\#10753\]\(https://github.com/earendil-works/pi/issues/10753\)\)
\- Fixed \`done\(\)\` of an extension&\#x27;s \`ctx.ui.custom\(\{ overlay: true \}\)\` closing the topmost overlay instead of its own, which left the finished overlay on screen and another extension&\#x27;s dialog unresolved \(\[\#10648\]\(https://github.com/earendil-works/pi/issues/10648\), \[\#10999\]\(https://github.com/earendil-works/pi/pull/10999\) by \[@masonc15\]\(https://github.com/masonc15\)\)

**「Impact」** Users who share sessions should set the new \`sessionShareDestination\` setting to control upload targets. Users overriding the \`kimi-coding\` base URL in \`models.json\` must append \`/v1\` to avoid breakage. The model-switching and resumed-session tool-retention changes are automatic and require no action. The dependency pinning and Nix build fixes improve install reliability for fresh installs and Nix users. Provider-specific fixes \(Kimi Code, OpenCode Go, Gemini, MiMo, Claude\) resolve 400/404 errors and incorrect thinking-level handling, so affected users should upgrade to restore those models.

**Tags**: `#sessions`, `#providers`, `#caching`, `#model-switching`, `#tools`

---

<a id="item-tools-update-3"></a>
### [hunk v0.24.0-beta.1: UI fixes, CLI validation, and marketplace addition](https://github.com/modem-dev/hunk/releases/tag/v0.24.0-beta.1) ⭐️ 5.0/10

The hunk project released v0.24.0-beta.1, a beta version focused on incremental improvements rather than major new features. This release includes UI fixes for binary file navigation, empty review distinction, and sidebar visibility during navigation, along with a CLI fix to reject unrecognized patch input, the addition of hunk-why to the extension marketplace, and documentation corrections.

github · github-actions\[bot\] · Oct 15, 17:26

**「Changes」** \- \*\*UI Fix\*\*: Binary files are now reachable by file navigation and clicks \(PR \#1178\)
\- \*\*CLI Improvement\*\*: Rejects unrecognized nonempty patch input \(PR \#1183\)
\- \*\*Extension Marketplace\*\*: Added hunk-why to the hunk-extension marketplace \(PR \#1179\)
\- \*\*UI Fix\*\*: Distinguishes empty reviews from filtered files \(PR \#1182\)
\- \*\*UI Fix\*\*: Keeps the selected file visible in the sidebar during held navigation \(PR \#1085\)
\- \*\*Testing\*\*: Allows published prereleases in changelog smoke tests \(PR \#1185\)
\- \*\*Documentation\*\*: Corrected stale facts and filled gaps across hunk.dev docs \(PR \#1186\)
\- \*\*New Contributor\*\*: @Lawgk made their first contribution in PR \#1085

**「Impact」** This beta release is primarily relevant for hunk users who want to test upcoming improvements before the stable v0.24.0 release. The UI fixes enhance navigation reliability, particularly for binary files and sidebar behavior. The CLI change may affect users who previously relied on passing unrecognized patch input, as such input will now be rejected. The addition of hunk-why to the extension marketplace provides users with a new tool for understanding why certain hunks are included. No breaking changes are introduced, but beta users should expect potential instability. Upgrading is optional unless testing these specific improvements is desired.

**Tags**: `#ui-fixes`, `#cli-improvement`, `#extension-marketplace`, `#documentation`, `#beta-release`

---

<a id="item-tools-update-4"></a>
### [OpenCode v1.19.1 Discontinues Session Sharing](https://github.com/anomalyco/opencode/releases/tag/v1.19.1) ⭐️ 5.0/10

OpenCode v1.19.1 is a bugfix release that discontinues session sharing functionality, removing existing share links and session-sharing commands. This is a breaking change affecting users who relied on share links and session-sharing commands.

github · opencode-agent\[bot\] · Oct 15, 19:19

**「Changes」** \- Session sharing has been discontinued. Existing share links and session-sharing commands are no longer available, and importing sessions from share URLs is unsupported.

**「Impact」** Users who relied on session sharing functionality will be affected by this change. Existing share links will no longer work, and session-sharing commands have been removed. Users who need to share sessions should consider alternative methods, as importing sessions from share URLs is now unsupported. No migration path is provided for existing share links.

**Tags**: `#bugfix`, `#session-sharing`, `#breaking-change`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Libreboot 26.10 Adds UEFI and Chromebook Support](https://libreboot.org/news/libreboot2610.html) ⭐️ 8.0/10

Libreboot 26.10 &quot;Ominous Olive&quot; introduces UEFI/EDK II support and compatibility with 233 Chromebook models imported from MrChromebox&\#x27;s coreboot distribution, significantly expanding the range of hardware that can run fully-free firmware. The release is source-only, requiring users to build from source as no pre-built binaries are provided. Community discussion emphasizes the technical magnitude of the UEFI integration and its impact on future device support.

hackernews · iamnothere · Oct 15, 12:52 · [Discussion](https://news.ycombinator.com/item?id=50102923)

**「Firmware Context」** Libreboot is a free software distribution of coreboot that replaces proprietary BIOS/UEFI firmware with fully-free alternatives. Previously, Libreboot&\#x27;s hardware support was limited compared to projects like MrChromebox&\#x27;s coreboot distribution, which maintains extensive Chromebook compatibility. The integration of UEFI/EDK II support addresses a long-standing limitation that prevented Libreboot from supporting many modern devices requiring UEFI firmware interfaces.

**「Hardware Compatibility Expansion」** Users can now install fully-free firmware on a vastly expanded range of devices, particularly Chromebooks, with 233 models becoming potentially supported. However, the source-only distribution model means users must have the technical capability to build firmware images themselves, and only Baytrail \(Kip\) Chromebooks have been tested so far, with other models requiring additional validation.

**「Community Response」** Community members highlight the significance of the UEFI integration, with one contributor noting collaboration with the Heads project on ChromeOS ports using MrChromebox&\#x27;s code as an upstream dependency. Discussion also covers Libreboot&\#x27;s strict policy on LLM-assisted contributions, with some community members expressing support for the approach while others focus on the technical achievements of the release.

**Tags**: `#libreboot`, `#uefi`, `#coreboot`, `#chromebook`, `#open-source-firmware`

---

<a id="item-tech-news-2"></a>
### [Anthropic Reports Q3 Revenue of $16.8 Billion Ahead of IPO](https://simonwillison.net/2026/Oct/15/anthropic-tells-investors/) ⭐️ 8.0/10

Anthropic reported third-quarter revenue of $16.8 billion, representing a nearly 50% increase from the second quarter&\#x27;s $11.5 billion, according to figures disclosed to investors during a day of investor meetings. The company also revealed that it generated $1.70 in revenue for every $1 spent on computing power in Q3, with adjusted operating margins \(excluding stock-based compensation\) reaching 11%. Additionally, Anthropic disclosed that distillation activities accounted for 5% to 7% of revenue and that it had materially reduced such usage in the third quarter. These metrics were shared as the company prepares for a potential initial public offering.

rss · Simon Willison · Oct 15, 13:04

**「Revenue Growth and Distillation Controls」** Anthropic&\#x27;s quarterly revenue growth has accelerated significantly, rising from approximately $4.8 billion in Q1 to $16.8 billion in Q3. The company&\#x27;s focus on controlling distillation—where rival AI labs train models using outputs from Anthropic&\#x27;s models—reflects a strategic shift to protect its competitive position and revenue streams. Previously, Anthropic had relied on annualized run-rate revenue figures in investor communications, a practice it appears to have discontinued in these latest disclosures.

**「Implications for AI Development Economics」** The disclosed financial metrics, particularly the $1.70-to-$1 revenue-to-compute ratio and the reduction in distillation activities, suggest that Anthropic is optimizing its operational efficiency and monetization strategies. For other AI developers and investors, these figures provide insight into the economic viability of large-scale AI model deployment and the competitive dynamics surrounding model usage and replication.

**Tags**: `#AI`, `#Anthropic`, `#Financial Metrics`, `#IPO`, `#Distillation`

---

<a id="item-tech-news-3"></a>
### [Random neural units self-assemble learning circuits matching backpropagation](https://www.reddit.com/r/MachineLearning/comments/1x6hmyg/how_artificial_neural_networks_build_their_own/) ⭐️ 8.0/10

A PNAS paper titled &quot;How Biological Synapses Self-Assemble Gradient Learning&quot; reports that randomly interconnected neuron-like units governed by shared plasticity rules can self-assemble learning motifs and achieve pattern recognition and image classification performance comparable to backpropagation-trained networks. The MIT coverage emphasizes the distinction between directly designing a learning circuit versus specifying local rules from which learning machinery organizes itself. The authors caution that self-organization does not establish that the brain uses this mechanism, and note open questions about motif stability under different initial connectivity and extension beyond the demonstrated tasks.

reddit · r/MachineLearning · /u/Dorian182 · Oct 15, 10:01

**「Background」** Traditional neural network training relies on backpropagation, an algorithm that requires precise, globally coordinated weight updates computed from a loss function. In contrast, biological brains appear to learn through local plasticity rules at synapses, without centralized error signals, motivating research into self-organizing systems that can build their own learning machinery from simple local interactions.

**「Impact」** The demonstrated ability of locally specified plasticity rules to self-assemble functional learning circuits suggests a potential pathway toward more biologically plausible AI systems, though the authors note this does not constitute evidence that the brain uses this specific mechanism. Researchers in computational neuroscience and machine learning may use these findings to explore alternatives to backpropagation, while remaining cautious about claims of direct neural relevance given the open questions about motif stability and task generalization.

**Tags**: `#neural networks`, `#self-organization`, `#plasticity`, `#machine learning`, `#computational neuroscience`

---

<a id="item-tech-news-4"></a>
### [Meta Releases Muse Spark Open, an Apple Silicon-Optimized Open-Weight Model](https://research.meta.ai/blog/muse-spark-open) ⭐️ 7.0/10

Meta has released Muse Spark Open, an open-weight language model optimized for Apple Silicon and designed to run on Mac Studio hardware. The model supports a wide range of runners including Unsloth and MLX, and is available on Hugging Face under a restricted license that permits most uses but prohibits offering the model as a service to third parties if the provider&\#x27;s aggregate gross revenue exceeds $20 million. The release targets developers and researchers interested in on-device inference and broad compatibility across inference frameworks.

hackernews · bigwheels · Oct 15, 17:47 · [Discussion](https://news.ycombinator.com/item?id=50107379)

**「Open-weight LLM landscape and Apple Silicon inference」** Open-weight language models—those whose trained parameters are publicly released—have become a key battleground for on-device inference, with vendors optimizing distributions for specific hardware like Apple Silicon. Meta&\#x27;s prior Llama series established the company&\#x27;s pattern of releasing model weights alongside a custom license that permits broad use while restricting large-scale API monetization, a structure that the Muse Model License now extends to the 816B-parameter Muse Spark Open. Apple&\#x27;s M-series chips, particularly the M5 Ultra Mac Studio referenced in Meta&\#x27;s announcement, have driven recent interest in running multi-hundred-billion-parameter models locally rather than in the cloud.

**「Impact」** Organizations and developers using Apple Silicon for on-device inference can adopt Muse Spark Open without relying on cloud APIs, but companies with annual revenues above $20 million must avoid offering the model as a paid service to third parties to remain compliant with the license. Early benchmarks suggest it trails competitors like Qwen3.8 Flash Next and GLM 5.3 Flash at the highest reasoning level, which may influence model selection for performance-sensitive applications.

**「Community Discussion」** Commenters noted that Muse Spark Open underperforms Qwen3.8 Flash Next and GLM 5.3 Flash in published benchmarks, and raised concerns that the &\#x27;Model as a Service&\#x27; clause effectively restricts its use by larger commercial entities. Others highlighted the model&\#x27;s broad runner support and deployment flexibility, while some interpreted the release as part of Meta&\#x27;s broader strategy to standardize the industry around its model ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://research.meta.ai/blog/muse-spark-open">Introducing Muse Spark Open, The Most Capable US Open‑Weight ...</a></li>
<li><a href="https://9to5mac.com/2026/10/15/meta-launches-new-muse-spark-open-model-optimized-to-run-on-mac-studio/">Meta launches new Muse Spark Open model, optimized ... - 9to5Mac</a></li>
<li><a href="https://fourweekmba.com/ai-meta-opens-816b-muse-spark-but-20m-api-hosts-need-a-deal/">Meta Opens 816B Muse Spark, but $20M+ API Hosts Need a Deal</a></li>
<li><a href="https://www.unite.ai/metas-816b-parameter-muse-spark-open-weights-are-now-public/">Meta’s 816B-Parameter Muse Spark Open Weights Are Now Public</a></li>
<li><a href="https://www.okaynews.com/meta-muse-spark-open-release-commercial-licence/">Meta Releases Muse Spark Open With Commercial Licence Conditions</a></li>

</ul>
</details>

**Tags**: `#open-weight-llm`, `#apple-silicon`, `#on-device-inference`, `#model-licensing`, `#meta-ai`

---

<a id="item-tech-news-5"></a>
### [Goodfire claims neural networks are &\#x27;clean&\#x27; and interpretable](https://already-clean.goodfire.com/) ⭐️ 7.0/10

Goodfire AI published a post arguing that neural networks are &\#x27;clean&\#x27; and increasingly interpretable, citing work on mechanistic interpretability and a microscope demo of a model the authors say they mostly understand. The post, linked from a Nick Cammarata tweet, frames interpretability as a solvable scientific problem but does not present peer-reviewed evidence or novel empirical results beyond the demo. Hacker News commenters pushed back, calling the claims an overreach and noting that progressive feature complexity, the Lottery Ticket Hypothesis, and the Multimodal Gap already describe similar phenomena.

hackernews · themgt · Oct 15, 16:04 · [Discussion](https://news.ycombinator.com/item?id=50105647)

**「Mechanistic interpretability and prior work」** Mechanistic interpretability seeks to reverse-engineer trained neural networks into human-understandable circuits and features, a field advanced by early work at OpenAI and later by Anthropic&\#x27;s sparse autoencoder \(SAE\) results. The Lottery Ticket Hypothesis \(Frankle &amp; Carbin, 2018\) showed that subnetworks can be pruned and retrained to match full-network performance, while the Multimodal Gap \(Garcia et al., 2022\) describes how representations condense across modalities during training. These prior results establish that network structure and training dynamics shape later behavior, which commenters say the new post does not meaningfully extend.

**「Claims lack novel evidence, raising skepticism」** Because the post offers no peer-reviewed results or new empirical findings beyond a single demo, researchers are unlikely to treat the &\#x27;clean&\#x27; claim as a breakthrough, and organizations evaluating interpretability tools should weigh the demo as illustrative rather than proven. The skepticism in the Hacker News thread suggests that any adoption of Goodfire&\#x27;s approach will require independent validation against established techniques like SAEs and circuit analysis.

**「Commenters question novelty and rigor」** Commenters including bluejay2387 and aesthesia argued that the claims overreach known results, citing the Lottery Ticket Hypothesis and the Multimodal Gap as prior explanations for the described phenomena, while aesthesia compared the tone to early Anthropic SAE enthusiasm. Several users, including ks2048, pointed to the microscope demo as the only concrete artifact, and lukewarm707 invoked Judith Butler to critique the framing as more rhetorical than technical.

**Tags**: `#machine-learning`, `#interpretability`, `#neural-networks`, `#ai-safety`, `#research`

---

<a id="item-tech-news-6"></a>
### [Citizen Lab: Ad Infrastructure Used to Deliver Zero-Click Spyware](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 7.0/10

Citizen Lab research reveals that targeted advertising infrastructure was exploited as a delivery mechanism for zero-click mercenary spyware, highlighting a novel attack vector in ad tech systems. The report, published on October 15, 2026, details how ad delivery pipelines can be subverted to install malware without user interaction. While the findings underscore serious risks to user privacy and software security, some industry professionals have questioned the report&\#x27;s framing of the &\#x27;zero-click&\#x27; aspect, noting that the activation mechanism remains unclear.

hackernews · jcomp · Oct 15, 10:43 · [Discussion](https://news.ycombinator.com/item?id=50101813)

**「Targeted advertising and zero-click spyware delivery」** Targeted advertising systems serve personalized ads by matching user profiles to advertiser demand through real-time bidding across ad exchanges and supply paths. Zero-click spyware refers to malicious software that compromises a device without requiring the user to click or otherwise interact with content, historically associated with sophisticated exploit chains in messaging or operating-system components. Citizen Lab has previously documented mercenary spyware vendors such as NSO Group and Candiru abusing mobile and desktop vulnerabilities, establishing a pattern of commercial exploit development that this AdFection finding extends into the ad-tech supply chain.

**「Implications for Ad Tech and User Privacy」** The research raises concerns for developers and organizations building or securing web applications, ad tech systems, and user privacy protections. It suggests that ad delivery networks may need enhanced scrutiny and security measures to prevent exploitation as malware distribution channels. An AdTech engineer with 13 years of experience acknowledged the underlying risks but criticized the report for being overly sensationalist about the zero-click mechanism.

**「Community Reactions Range from Criticism to Calls for Regulation」** Community responses included calls to ban online advertising entirely, critiques of the report&\#x27;s sensationalism from an experienced AdTech engineer, and political commentary about Israeli tech firms. Some users questioned why Israel has become a leading cyber power, attributing it to regional security pressures. The discussion reflected both technical skepticism and broader concerns about trust in cybersecurity vendors.

<details><summary>References</summary>
<ul>
<li>AdFection Spyware Hit 70000 Apps via Ad Networks [2026] - Tech Insider</li>
<li>New &#x27;zero-click&#x27; spyware hacked phones using targeted ads, UofT researchers discover</li>
<li>Zero-Click Spyware Ads: Citizen Lab&#x27;s AdFection Report - shattered.io</li>

</ul>
</details>

**Tags**: `#security`, `#spyware`, `#adtech`, `#privacy`, `#exploitation`

---

<a id="item-tech-news-7"></a>
### [ASML Developing Hybrid Bonding Tool, Per Patents and Roadmap](https://newsletter.semianalysis.com/p/asml-is-building-a-hybrid-bonding) ⭐️ 7.0/10

ASML is reportedly developing a hybrid bonding tool, according to its patent filings, a news report, and the company&\#x27;s roadmap, though no official announcement has been made. Hybrid bonding is a semiconductor manufacturing technique that enables higher interconnect density and improved chip performance. The development, if confirmed, could impact future chip fabrication processes, but the evidence remains indirect rather than based on an official product launch.

rss · Semianalysis · Oct 15, 19:27

**「Hybrid Bonding in Chip Manufacturing」** Hybrid bonding is an advanced packaging technology that directly connects metal and dielectric layers between chips or wafers without traditional solder bumps, allowing for finer interconnect pitches and better electrical performance. It has become increasingly important for applications such as image sensors, high-bandwidth memory, and 3D-stacked logic chips.

**「Potential Impact on Semiconductor Supply Chain」** If ASML enters the hybrid bonding equipment market, it could expand its presence beyond lithography and compete with existing players like EV Group and SUSS MicroTec, potentially reshaping the advanced packaging landscape for chipmakers relying on 3D integration.

**Tags**: `#semiconductors`, `#ASML`, `#hybrid bonding`, `#chip manufacturing`, `#patent analysis`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Muse Spark Open Day 0 Support on vLLM](https://vllm.ai/blog/2026-10-15-muse-spark-open) ⭐️ 6.0/10

rss · vLLM Blog · Oct 15, 00:00

**「Background」** Muse Spark Open is a large-scale multimodal mixture-of-experts \(MoE\) model with 816B total parameters and a 1M-token context window, released by Meta in BF16 and NVFP4 formats. Supporting such a model on vLLM requires handling its complex architecture, including MoE layers, hybrid attention, and multiple encoders, while maintaining efficient inference across diverse hardware platforms.

**「Solution」** The vLLM team implemented Day 0 support for Muse Spark Open, leveraging its architecture: every decoder layer is an MoE layer with 256 experts, using a &\#x27;sandwich normalization&\#x27; scheme and latent MoE projections \(pooler/unpooler\) to reduce parameter count. Hybrid attention alternates between full and sliding-window attention in a 4-layer cycle, reducing KV cache usage at 1M context. The model includes a 2B vision encoder \(shared with Muse Glimmer\) and a small 118M audio encoder. For inference acceleration, a DSpark speculator enables block diffusion-based speculative decoding, supporting up to 7 draft tokens per pass. Hardware optimizations include fused kernels on Nvidia \(FlashInfer, low-latency BF16 GEMM\), FP8/MXFP4 support on AMD MI355X, and TPU v7 integration with megakernels. RL training is supported via LoRA adapters applied on NVFP4 checkpoints, with vLLM serving as the rollout engine and Verl FSDP2 as the trainer, achieving AIME-2024 accuracy gains from 0.56 to 0.85 over 150 steps. Prebuilt Docker images are available for Nvidia and AMD, with nightly PyPI wheels pending code review.

**「Takeaway」** The vLLM team delivered comprehensive Day 0 support for Muse Spark Open, addressing its architectural complexity through optimized kernels, speculative decoding, and cross-platform hardware acceleration, while enabling RL workflows via LoRA integration.

**Tags**: `#mixture-of-experts`, `#speculative-decoding`, `#quantization`, `#multimodal-models`, `#vLLM`

---

## Financial News

<a id="item-finance-news-1"></a>
### [IMF: Rural Chinese spend 8.7% of income on healthcare, second only to US](https://www.cnbc.com/2026/10/15/chinese-spending-nearly-as-much-of-income-as-americans-on-healthcare.html) ⭐️ 7.0/10

IMF research finds rural Chinese spend 8.7% of disposable income on healthcare, second only to the U.S. \(9.9%\) among 20 major economies, while urban China spends 5.4%. The IMF says raising government health and social security spending in rural areas could significantly reduce household savings rates.

rss · CNBC Finance · Oct 15, 23:00

**「Background」** The findings appear in the IMF book &\#x27;Toward a New Economic Growth Model for China,&\#x27; which examines how high healthcare costs push Chinese households to save rather than spend. Rural per capita disposable income was 24,456 yuan \($6,400\) versus 56,502 yuan in urban areas, with the U.S. at $68,289.

**「Impact」** The research suggests that expanding rural social spending could lift consumption among China&\#x27;s large rural population, where the savings rate for rural workers in cities is around 14%.

**Tags**: `#Healthcare`, `#China`, `#IMF`, `#Household Savings`, `#Consumption`

---

<a id="item-finance-news-2"></a>
### [Harvard Endowment Returns 27.1% in Fiscal 2026, Reaching Nearly $68 Billion](https://www.cnbc.com/2026/10/15/harvards-endowment-jumps-27percent-with-spacex-as-top-holding.html) ⭐️ 7.0/10

Harvard University&\#x27;s endowment returned 27.1% in fiscal 2026, its best performance since 2021, growing to nearly $68 billion and outperforming the S&amp;P 500&\#x27;s 22.3% return. The gain was driven in part by a $2.2 billion stake in SpaceX, now the endowment&\#x27;s largest holding, even as the university faces a near six-fold increase in the federal excise tax on its investment income and a 19.5% drop in federally-sponsored research revenue to $509 million.

rss · CNBC Finance · Oct 15, 19:53

**「Background」** The Trump administration has moved to penalize Harvard by withholding federal funding, and starting this fiscal year the federal excise tax on Harvard&\#x27;s net investment income is set to rise from 1.4% to 8%, which Harvard estimates will cost roughly $300 million annually.

**「Impact」** The strong investment returns provide Harvard with greater financial flexibility to support its operations over time, but the combination of reduced federal research funding and the steep excise tax increase poses significant financial pressure on the university&\#x27;s budget and resource allocation.

**Tags**: `#Endowment`, `#Higher education`, `#Federal policy`, `#Investment returns`, `#Tax policy`

---

<a id="item-finance-news-3"></a>
### [China says rare earth exports to EU will continue despite U.S. trade deal expiry](https://www.cnbc.com/2026/10/15/china-rare-earth-exports-europe.html) ⭐️ 7.0/10

China&\#x27;s Commerce Ministry said it will keep approving rare earth export licenses to the EU even if the U.S.-China trade deal expires in January, citing a willingness to use a &\#x27;green channel&\#x27; mechanism to maintain flows.

rss · CNBC Finance · Oct 15, 09:02

**「Background」** Beijing tightened rare earth export controls in October 2025, requiring licenses for products containing any Chinese-sourced rare earths, after the U.S. expanded its entity list to cover majority-owned subsidiaries of Chinese firms, affecting roughly 20,000 entities. The U.S. and China agreed to suspend those measures for one year following a summit between Presidents Xi Jinping and Donald Trump, with the truce later extended by two months to January.

**「Impact」** The signal matters for EU manufacturers and clean-energy supply chains that depend on Chinese rare earths, though the commitment rests on a spokesperson statement rather than enacted policy and awaits the European Commission&\#x27;s review of ongoing trade negotiations.

**Tags**: `#Rare earths`, `#China-EU trade`, `#China-U.S. trade`, `#Export controls`, `#Critical minerals`

---

<a id="item-finance-news-4"></a>
### [China Accelerates Replacement of Western Wind Power Equipment](https://www.bloomberg.com/news/articles/2026-10-15/china-removes-western-wind-power-equipment-to-boost-security?srnd=phx-technology) ⭐️ 7.0/10

China is speeding up the replacement of Western wind power equipment with domestic alternatives, citing energy security concerns, according to an analysis of over 1,600 public procurement documents by the Polish-based Center for Eastern Studies, with roughly 300 documents involving equipment replacement.

telegram · zaihuapd · Oct 15, 14:55

**「Background」** The shift targets key components such as turbine control systems, industrial software, and related parts, driven by Chinese energy companies&\#x27; concerns over high maintenance costs, long spare-parts supply cycles, and potential security risks from foreign technology.

**「Impact」** The policy-driven trend is expected to create new market opportunities for Chinese wind turbine manufacturers while increasing pressure on Western suppliers, who may face further shrinking market share in China&\#x27;s renewable energy sector.

**Tags**: `#Energy Security`, `#Wind Power`, `#China Policy`, `#Supply Chain`, `#Industrial Policy`

---
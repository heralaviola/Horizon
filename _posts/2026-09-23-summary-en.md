---
layout: default
title: "Horizon Summary: 2026-09-23 (EN)"
date: 2026-09-23
lang: en
---

> From 48 items, 10 important content pieces were selected

---

**Tools Update**
1. [Zed v1.22.0-pre: BYOK AI models, per-call overrides, and subagent compaction](#item-tools-update-1) ⭐️ 7.0/10
2. [Zed v1.21.0: Rendering, AI, and Language Server Improvements](#item-tools-update-2) ⭐️ 7.0/10
3. [openai/codex rust-v0.156.1 adds GPT-6 Sol and Luna models](#item-tools-update-3) ⭐️ 5.0/10

**Technology News**
1. [Google Releases Gemini 3.8 Text-to-Speech with Voice Replication](#item-tech-news-1) ⭐️ 7.0/10
2. [Simon Willison&\#x27;s Interactive Shadow Roots Learning Tool](#item-tech-news-2) ⭐️ 7.0/10
3. [Claude Opus 5.5, GPT-6 Sol and Luna released with price cuts](#item-tech-news-3) ⭐️ 7.0/10
4. [Qualcomm Unveils Snapdragon 8 Elite Extreme Gen 6 Platform](#item-tech-news-4) ⭐️ 7.0/10

**Financial News**
1. [Trump-Xi Summit: China&\#x27;s Self-Sufficiency Reshapes US-China Trade Dynamics](#item-finance-news-1) ⭐️ 7.0/10
2. [CFTC Warns Prediction Markets&\#x27; &\#x27;Mentions&\#x27; Contracts Face Higher Manipulation Risk](#item-finance-news-2) ⭐️ 7.0/10
3. [China Allegedly Tells Banks to Keep Vanke Overdue Loans Off Bad-Debt Books](#item-finance-news-3) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [Zed v1.22.0-pre: BYOK AI models, per-call overrides, and subagent compaction](https://github.com/zed-industries/zed/releases/tag/v1.22.0-pre) ⭐️ 7.0/10

Zed v1.22.0-pre is a pre-release that adds BYOK support for new AI models \(Claude Opus 5.5, GPT-6 Astra/Sol/Luna\), per-call model overrides in spawn\_agent, automatic subagent compaction, and dynamically fetched OpenCode models. These are shipped feature additions, though as a pre-release it may not be stable for production use.

github · zed-zippy\[bot\] · Sep 23, 16:21

**「Changes」** \#\#\# AI
\- Added BYOK support for GPT-6 Astra with an OpenAI API key. \(\[\#64420\]\(https://github.com/zed-industries/zed/pull/64420\)\)
\- Added BYOK support for GPT-6 Sol and GPT-6 Luna with an OpenAI API key. \(\[\#64628\]\(https://github.com/zed-industries/zed/pull/64628\)\)
\- Added BYOK support for Claude Opus 5.5 with an Anthropic API key. \(\[\#64627\]\(https://github.com/zed-industries/zed/pull/64627\)\)
\- Added an optional \`model\` parameter to \`spawn\_agent\` to choose a model for that spawn instead of using the configured subagent model or inheriting the parent model, with the active model shown in its card. \(\[\#64498\]\(https://github.com/zed-industries/zed/pull/64498\); thanks \[itsfuad\]\(https://github.com/itsfuad\)\)
\- Added Grok 4.7 to the SuperGrok and xAI providers and made it their recommended default. \(\[\#64567\]\(https://github.com/zed-industries/zed/pull/64567\); thanks \[raphaelluethy\]\(https://github.com/raphaelluethy\)\)
\- Added Z.ai GLM to the Mistral provider. \(\[\#63535\]\(https://github.com/zed-industries/zed/pull/63535\); thanks \[ummon-v\]\(https://github.com/ummon-v\)\)
\- Added the \`agent.threads\_sidebar.auto\_open\` setting to control whether opening a folder in an existing window also opens the Threads Sidebar. \(\[\#64259\]\(https://github.com/zed-industries/zed/pull/64259\), \[\#64395\]\(https://github.com/zed-industries/zed/pull/64395\); thanks \[jackhwalters\]\(https://github.com/jackhwalters\) and \[joshkent94\]\(https://github.com/joshkent94\)\)
\- Added support for \`&quot;...&quot;\` in \`edit\_predictions.disabled\_globs\` and \`edit\_predictions\_disabled\_in\` so settings can extend inherited edit prediction exclusions and scopes. \(\[\#64540\]\(https://github.com/zed-industries/zed/pull/64540\), \[\#64546\]\(https://github.com/zed-industries/zed/pull/64546\); thanks \[porada\]\(https://github.com/porada\)\)
\- Enabled compaction for subagents. \(\[\#64135\]\(https://github.com/zed-industries/zed/pull/64135\)\)
\- Improved OpenCode model availability by fetching the Zen and Go model list dynamically instead of relying on one bundled with Zed. \(\[\#64585\]\(https://github.com/zed-industries/zed/pull/64585\)\)
\- Improved Threads Sidebar sizing so changes to \`agent.threads\_sidebar.default\_width\` take effect even after manually resizing the sidebar. \(\[\#64395\]\(https://github.com/zed-industries/zed/pull/64395\); thanks \[joshkent94\]\(https://github.com/joshkent94\)\)

\#\#\# Git
\- Added a unified/split toggle to the diff view opened with \`zed --diff &lt;old&gt; &lt;new&gt;\`. \(\[\#64529\]\(https://github.com/zed-industries/zed/pull/64529\); thanks \[rn23thakur\]\(https://github.com/rn23thakur\)\)
\- Improved how quickly branch diffs show their first changes when a branch has drifted far from its base. \(\[\#62536\]\(https://github.com/zed-industries/zed/pull/62536\); thanks \[azeemshaik025\]\(https://github.com/azeemshaik025\)\)

\#\#\# Terminal
\- Added support for \`&quot;...&quot;\` in \`terminal.path\_hyperlink\_regexes\` to extend inherited regexes without repeating them. \(\[\#64552\]\(https://github.com/zed-industries/zed/pull/64552\); thanks \[porada\]\(https://github.com/porada\)\)

\#\#\# macOS
\- Added macOS three-finger Look Up and translation gestures for text in focused Markdown previews. \(\[\#59297\]\(https://github.com/zed-industries/zed/pull/59297\); thanks \[cppcoffee\]\(https://github.com/cppcoffee\)\)

\#\#\# Windows
\- Added \`MicaBackdrop\` and \`MicaAltBackdrop\` options for the \`background.appearance\` theme setting. \(\[\#48340\]\(https://github.com/zed-industries/zed/pull/48340\); thanks \[Marocco2\]\(https://github.com/Marocco2\)\)

\#\#\# Other
\- Added support for \`&quot;...&quot;\` in \`file\_scan\_inclusions\` and \`hidden\_files\` so project settings can extend inherited inclusion and hidden-file patterns. \(\[\#64440\]\(https://github.com/zed-industries/zed/pull/64440\), \[\#64484\]\(https://github.com/zed-industries/zed/pull/64484\); thanks \[porada\]\(https://github.com/porada\)\)
\- Added confirmation in the title bar when a manual update check found Zed was already up to date. \(\[\#64106\]\(https://github.com/zed-industries/zed/pull/64106\); thanks \[tahayvr\]\(https://github.com/tahayvr\)\)
\- Improved the pending keystrokes indicator with grouped bindings, a scrollable list, and support for chords without a timeout, such as shortcuts starting with \`cmd-k\`. \(\[\#64362\]\(https://github.com/zed-industries/zed/pull/64362\), \[\#64522\]\(https://github.com/zed-industries/zed/pull/64522\)\)

\#\#\# Bug Fixes
\- Fixed invalid file patterns discarding valid exclusion, hidden-file, read-only, and private-file rules or causing inclusion and file-type settings to panic. \(\[\#64525\]\(https://github.com/zed-industries/zed/pull/64525\); thanks \[porada\]\(https://github.com/porada\)\)
\- Fixed \`cmd-w\` \(macOS\) and \`ctrl-w\` \(Linux/Windows\) closing the active dock instead of the active pane item. \(\[\#64515\]\(https://github.com/zed-industries/zed/pull/64515\)\)
\- Fixed newly available ChatGPT subscription models not appearing in the model picker. \(\[\#64625\]\(https://github.com/zed-industries/zed/pull/64625\)\)
\- Fixed a crash when typing into an empty side of a merge conflict. \(\[\#64604\]\(https://github.com/zed-industries/zed/pull/64604\)\)
\- Fixed ligatures being disabled on Windows unless \`buffer\_font\_features\` was set. \(\[\#62338\]\(https://github.com/zed-industries/zed/pull/62338\); thanks \[interkelstar\]\(https://github.com/interkelstar\)\)
\- Fixed LSP completions without edit ranges ignoring the configured \`completions.lsp\_insert\_mode\`. \(\[\#64139\]\(https://github.com/zed-industries/zed/pull/64139\)\)
\- Fixed the Settings window opening with its header off-screen at high DPI scaling on Windows. \(\[\#62073\]\(https://github.com/zed-industries/zed/pull/62073\); thanks \[habisahmad\]\(https://github.com/habisahmad\)\)
\- Fixed the Git Panel unexpectedly switching repositories when viewing changes in multi-repository projects. \(\[\#58795\]\(https://github.com/zed-industries/zed/pull/58795\); thanks \[mengh04\]\(https://github.com/mengh04\)\)
\- Fixed importing VS Code \`files.exclude\` into \`file\_scan\_exclusions\`. \(\[\#64492\]\(https://github.com/zed-industries/zed/pull/64492\); thanks \[porada\]\(https://github.com/porada\)\)
\- Fixed &quot;Add to .git/info/exclude&quot; failing in secondary Git worktrees. \(\[\#63967\]\(https://github.com/zed-industries/zed/pull/63967\); thanks \[mateioprea\]\(https://github.com/mateioprea\)\)
\- Fixed terminals retaining about 2 MB of memory per command after the command finished. \(\[\#64405\]\(https://github.com/zed-industries/zed/pull/64405\); thanks \[EcutAtom336\]\(https://github.com/EcutAtom336\)\)
\- Fixed external-agent terminals completing prematurely or reporting the wrong exit status. \(\[\#64544\]\(https://github.com/zed-industries/zed/pull/64544\)\)
\- Fixed a memory leak when closing macOS windows with experimental accessibility enabled. \(\[\#64143\]\(https://github.com/zed-industries/zed/pull/64143\); thanks \[feigeCode\]\(https://github.com/feigeCode\)\)
\- Fixed the terminal grid losing its top alignment when growing on Windows. \(\[\#63699\]\(https://github.com/zed-industries/zed/pull/63699\); thanks \[39ali\]\(https://github.com/39ali\)\)
\- Fixed a crash on Linux \(X11\) when a window was redrawn immediately after GPU device recovery. \(\[\#64570\]\(https://github.com/zed-industries/zed/pull/64570\)\)
\- Fixed language servers not starting for files opened via UNC paths on Windows. \(\[\#56553\]\(https://github.com/zed-industries/zed/pull/56553\); thanks \[Joblen\]\(https://github.com/Joblen\)\)
\- Fixed PowerShell installed by Scoop not being detected when Scoop uses a custom installation directory. \(\[\#62473\]\(https://github.com/zed-industries/zed/pull/62473\); thanks \[jliu666\]\(https://github.com/jliu666\)\)
\- Fixed task worktree variables resolving to the wrong project when the global \`tasks.json\` file was focused, and paths containing spaces breaking Windows tasks. \(\[\#55727\]\(https://github.com/zed-industries/zed/pull/55727\); thanks \[di404\]\(https://github.com/di404\)\)

**「Impact」** Users leveraging AI agents in Zed will benefit most from this release, particularly those wanting to use their own API keys for newer models like Claude Opus 5.5 and GPT-6 variants. The per-call model override in spawn\_agent and automatic subagent compaction provide greater control over agent workflows. As a pre-release \(v1.22.0-pre\), it may contain instability and is not recommended for production use. The release notes appear incomplete \(cut off mid-sentence in the Bug Fixes section\), so users should expect potential additional changes in the final release.

**Tags**: `#AI`, `#BYOK`, `#model-override`, `#subagent`, `#pre-release`

---

<a id="item-tools-update-2"></a>
### [Zed v1.21.0: Rendering, AI, and Language Server Improvements](https://github.com/zed-industries/zed/releases/tag/v1.21.0) ⭐️ 7.0/10

Zed v1.21.0 is a shipped release that improves rendering performance in syntax-highlighted files and Markdown code blocks, adds a language server command picker, introduces an agent sleep-prevention setting, and expands BYOK AI model support to include Claude Opus 5.5 and GPT-6 variants.

github · zed-zippy\[bot\] · Sep 23, 15:42

**「Changes」** \#\#\# Features

\*\*AI\*\*
\- Added SuperGrok sign-in for Grok models in the Agent Panel.
\- Added \`agent.prevent\_idle\_sleep\` setting \(enabled by default\) to prevent idle system sleep during agent threads.
\- Added support for DeepSeek Flash 4.1.
\- Added \`agent.threads\_sidebar\_default\_width\` setting to configure Threads Sidebar width.
\- Added \`agent: rename selected thread\` action for renaming active Terminal Threads.
\- Added BYOK support for Claude Opus 5.5 \(Anthropic\).
\- Added BYOK support for GPT-6 Sol and Luna \(OpenAI\).
\- Added BYOK support for GPT-6 Astra \(OpenAI\).
\- Added Z.ai GLM to the Mistral provider.
\- Improved ACP compatibility and async task wakeup handling.

\*\*Git\*\*
\- Added Cut, Copy, and Paste context menu actions to the commit message editor.

\*\*Languages\*\*
\- Added a language server command picker and \`showDocument\` request support for opening files and URLs.
\- Added a prompt to install the Emmet extension for Emmet-supported languages.
\- Added support for running language-server actions from actionable inlay hints.
\- Improved rendering performance for Markdown code blocks in Agent Panel, hover popovers, and Markdown preview.
\- Improved development extension compilation by auto-replacing outdated WASI SDK installations.

\*\*Other\*\*
\- Added \`comment\_empty\_lines\` parameter to \`editor::ToggleComments\` for multiline selections.
\- Added \`editor.code\_lens.foreground\` for customizing CodeLens text independently.
\- Added support for \`&quot;...&quot;\` in \`read\_only\_files\` to extend inherited read-only patterns.
\- Added \`menu\` \(Linux/Windows\) and \`shift-f10\` \(all platforms\) shortcuts for Project Panel context menu.
\- Improved editor rendering performance in syntax-highlighted files, especially with minimap enabled.

\#\#\# Bug Fixes
\- Fixed folder highlight persistence after drag operations.
\- Fixed macOS traffic light animation when exiting fullscreen.
\- Fixed macOS window restoration opening on active Space instead of original Space.
\- Fixed auto-compaction thresholds for GitHub Copilot models with prompt limits below context window.
\- Fixed Inline Assistant fallback model selection when no default model configured.
\- Fixed macOS hover effects triggering in underlying Zed windows.
\- Fixed deleted files appearing outside file tree in Outline Panel during diff view.
\- Fixed crash during Python interpreter discovery with non-UTF-8 output.
\- Fixed crash when pasting in expanded deleted diff hunk in Helix mode.
\- Fixed Linux startup crash when XKB keyboard-definition files unavailable.
\- Fixed Anthropic credit exhaustion classification as malformed request instead of payment issue.
\- Fixed canceled external file drags on Linux Wayland remaining active.
\- Fixed development extension compilation on Windows ARM64.
\- Fixed development extension compilation with large Tree-sitter grammars.
\- Fixed data-retention consent checks for hosted counting and compaction requests.
\- Fixed diff statistics to use theme&\#x27;s version-control colors.
\- Fixed font suggestions listing unavailable fallback fonts and internal aliases.
\- Fixed intermittent &quot;database is locked&quot; errors when sharing database across Zed instances.
\- Fixed Ollama inability to access images returned by tool calls.
\- Fixed Python decorator syntax highlighting conflicting with matrix multiplication operator.

**「Impact」** This release benefits all Zed users, particularly those working with AI agents, language servers, and large syntax-highlighted files. The \`agent.prevent\_idle\_sleep\` setting is enabled by default, so users who prefer their system to sleep during agent operations should disable it in settings. No other migration actions are required. Users leveraging BYOK AI models can now access Claude Opus 5.5 and GPT-6 variants \(Sol, Luna, Astra\) with their existing API keys. The rendering performance improvements are especially noticeable for users with the minimap enabled or those frequently viewing Markdown content.

**Tags**: `#performance`, `#ai`, `#language-server`, `#settings`, `#rendering`

---

<a id="item-tools-update-3"></a>
### [openai/codex rust-v0.156.1 adds GPT-6 Sol and Luna models](https://github.com/openai/codex/releases/tag/rust-v0.156.1) ⭐️ 5.0/10

openai/codex released version rust-v0.156.1, a minor incremental update that adds GPT-6 Sol and GPT-6 Luna models to the model picker and updates the rate-limit switch prompt to recommend GPT-6 Luna. This is a non-breaking feature addition with limited user impact.

github · github-actions\[bot\] · Sep 23, 02:41

**「Changes」** \- Added GPT-6 Sol and GPT-6 Luna models to the model picker.
\- Updated the rate-limit switch prompt to recommend GPT-6 Luna.
\- Hotfix for 0.156.0 release.

**「Impact」** Users who want to try the new GPT-6 Sol or GPT-6 Luna models can now select them directly from the model picker. The rate-limit prompt now suggests GPT-6 Luna as the recommended model when switching due to rate limits. No migration or compatibility actions are required; this is a low-priority update for users who do not need the new models.

**Tags**: `#model-catalog`, `#ui-update`, `#incremental-feature`, `#minor-release`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Google Releases Gemini 3.8 Text-to-Speech with Voice Replication](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-text-to-speech/) ⭐️ 7.0/10

Google has released Gemini 3.8 text-to-speech, introducing voice replication from 30-second audio samples with built-in consent verification, SynthID watermarking, and C2PA credentials. The release targets AI/ML developers working with voice synthesis, though availability varies across Google&\#x27;s consumer, prosumer, and cloud platforms. Community discussion highlights both technical interest in the capabilities and concerns about inconsistent platform support.

hackernews · swolpers · Sep 23, 15:29 · [Discussion](https://news.ycombinator.com/item?id=49817615)

**「Voice Synthesis Evolution in AI Platforms」** Text-to-speech systems have evolved from basic speech generation to advanced voice cloning requiring minimal samples. Google&\#x27;s Gemini series has progressively incorporated multimodal capabilities, with this 3.8 release focusing specifically on voice synthesis enhancements and safety measures.

**「Platform Fragmentation Creates Developer Challenges」** Developers face inconsistent capabilities across Google&\#x27;s platforms, with features like voice replication potentially unavailable on certain tiers. Organizations that restrict consumer and prosumer access may find themselves limited to GCP offerings with different feature sets, complicating deployment strategies.

**「Developer Reactions Highlight Platform and Capability Concerns」** Community members note Google&\#x27;s lack of alignment across consumer, prosumer, and cloud platforms, with different availabilities and capabilities per tier. Some developers express interest in local alternatives like KeenLore using Gemma, while others appreciate Gemini 3.8&\#x27;s voice library and control options for creative projects.

**Tags**: `#text-to-speech`, `#voice-synthesis`, `#gemini`, `#ai-safety`, `#developer-tools`

---

<a id="item-tech-news-2"></a>
### [Simon Willison&\#x27;s Interactive Shadow Roots Learning Tool](https://simonwillison.net/2026/Sep/23/shadow-roots/) ⭐️ 7.0/10

Simon Willison has created an interactive educational tool that explains CSS shadow roots through live, editable examples. The tool, available at https://tools.simonwillison.net/shadow-roots, allows users to experiment with shadow DOM concepts in real-time. Built using Fable 5.1 Medium, the artifact provides hands-on understanding of how shadow roots encapsulate styles and markup in modern web development.

rss · Simon Willison · Sep 23, 16:37

**「Understanding Shadow Roots in Web Development」** Shadow roots are a core part of the Shadow DOM API, which enables encapsulation of CSS and JavaScript in web components. They allow developers to attach a hidden, separate DOM tree to an element, keeping its styling and behavior isolated from the main document. This encapsulation prevents style leakage and conflicts, making components more predictable and reusable.

**「Practical Learning for Frontend Developers」** Frontend developers working with web components or modern CSS architectures can use this tool to gain practical experience with shadow roots. The live examples help clarify how encapsulation works, which is essential for building maintainable component libraries and avoiding common styling pitfalls in large-scale applications.

**Tags**: `#css`, `#web-development`, `#frontend`, `#education`, `#tools`

---

<a id="item-tech-news-3"></a>
### [Claude Opus 5.5, GPT-6 Sol and Luna released with price cuts](https://simonwillison.net/2026/Sep/22/opus-and-sol-and-luna/) ⭐️ 7.0/10

Anthropic released Claude Opus 5.5, and OpenAI released GPT-6 Sol and GPT-6 Luna, with GPT-6 Sol and Luna priced at half the cost of their GPT-5.6 equivalents. GPT-6 Luna is now $0.10/M input and $0.50/M output, while GPT-6 Sol is $2/M input and $10/M output. Claude Opus 5.5 also received a 20% price cut to $4/M input and $20/M output, with cached input reads dropping 60%. The releases follow Grok 4.7 and MiMo v2.6 from the previous day, intensifying competition in the AI model market.

rss · Simon Willison · Sep 22, 23:46

**「Context of recent AI model releases」** The rapid succession of model releases—Grok 4.7 and MiMo v2.6 yesterday, followed by Claude Opus 5.5 and GPT-6 Sol/Luna today—reflects an accelerating pace of AI development. OpenAI&\#x27;s GPT-5.6 series had previously established pricing tiers that these new models are undercutting, with GPT-5.6 Luna having been noted for combining strong performance with low cost before GPT-6 Luna halved those prices.

**「Price reductions reshape API cost landscape」** Developers building applications on these APIs will see significant cost savings, particularly with GPT-6 Luna now among the cheapest models OpenAI has ever released at $0.10/M input. The 60% reduction in cached input pricing for Claude Opus 5.5 is especially impactful for agentic applications where most input tokens are processed at cached rates. However, Claude Opus 5.5 at max thinking level has been reported to hit output token limits and fail on simple prompts, suggesting potential reliability issues at higher reasoning settings.

**Tags**: `#AI`, `#Machine Learning`, `#Software Engineering`, `#Cloud APIs`, `#Pricing`

---

<a id="item-tech-news-4"></a>
### [Qualcomm Unveils Snapdragon 8 Elite Extreme Gen 6 Platform](https://www.qualcomm.com/smartphones/products/8-series/snapdragon-8-elite-extreme-gen-6-mobile-platform) ⭐️ 7.0/10

Qualcomm announced the Snapdragon 8 Elite Extreme Gen 6 mobile platform, targeting next-generation agentic AI workloads on smartphones. The platform features a 5 GHz Oryon CPU \(13% faster than its predecessor\), an Adreno GPU with 44% higher performance and 40% better efficiency, and a Hexagon NPU that is 35% faster. It supports 8K60 and 4K240 video capture, triple 64MP cameras, and includes the X105 5G modem with a peak downlink speed of 14.8 Gbps. While the announcement highlights significant hardware improvements, a note from Geek Street indicated that engineering prototype efficiency gains are modest compared to expectations for the retail A20 Pro version.

telegram · zaihuapd · Sep 23, 00:52

**「Background」** Qualcomm&\#x27;s previous flagship tier was the Snapdragon 8 Elite Gen 5 series, which established the Oryon CPU and Adreno GPU baseline that the new Extreme Gen 6 variant builds upon. The Gen 6 generation marks Qualcomm&\#x27;s first 2nm process node for mobile platforms, enabling the higher clock speeds and efficiency targets claimed for agentic AI workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://www.qualcomm.com/news/releases/2026/09/snapdragon-leads-the-agentic-ai-age-with-two-of-the-world-s-fast">Snapdragon Leads the Agentic AI Age with Two of ... - Qualcomm</a></li>
<li><a href="https://9to5google.com/2026/09/22/snapdragon-8-elite-gen-6/">Qualcomm announces the Snapdragon 8 Elite Gen 6 - 9to5Google</a></li>
<li><a href="https://wccftech.com/snapdragon-8-elite-extreme-gen-6-snapdragon-8-elite-gen-6-official/">Snapdragon 8 Elite Extreme Gen 6 &amp; Snapdragon 8 ... - Wccftech</a></li>

</ul>
</details>

**Tags**: `#Snapdragon 8 Elite Extreme Gen 6`, `#Qualcomm`, `#mobile AI`, `#Oryon CPU`, `#Hexagon NPU`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Trump-Xi Summit: China&\#x27;s Self-Sufficiency Reshapes US-China Trade Dynamics](https://www.cnbc.com/2026/09/23/trump-xi-meeting-why-chinas-self-sufficiency-changes-the-calculus.html) ⭐️ 7.0/10

Ahead of a Trump-Xi summit, China&\#x27;s push for self-sufficiency and entrenched role in global supply chains have reduced the threat to its domestic market from global trade developments, even as the U.S.-China trade deficit remains elevated. While tariffs have done little to dent America&\#x27;s appetite for Chinese goods, surging demand for AI-related parts has kept the deficit high, and China&\#x27;s real estate downturn has accelerated its global export expansion.

rss · CNBC Finance · Sep 23, 21:26

**「Background」** The U.S.-China trade deficit escalated tensions between the two nations in recent years, but China&\#x27;s efforts to build self-sufficiency have mitigated the impact of global trade volatility on its domestic market. The upcoming Trump-Xi meeting follows a trade truce reached last fall, with businesses hoping for an extension rather than new concessions.

**「Impact」** Chinese companies&\#x27; dominance in critical minerals and global supply chains, combined with their increasing competitiveness in product quality, is reshaping international trade dynamics and prompting the EU and U.S. to intensify scrutiny of China-origin exports.

**Tags**: `#China-US trade`, `#supply chain`, `#economic policy`, `#trade deficit`, `#AI and technology`

---

<a id="item-finance-news-2"></a>
### [CFTC Warns Prediction Markets&\#x27; &\#x27;Mentions&\#x27; Contracts Face Higher Manipulation Risk](https://www.cnbc.com/2026/09/22/cftc-prediction-markets-mentions-contracts-have-manipulation-risk.html) ⭐️ 7.0/10

The U.S. Commodity Futures Trading Commission \(CFTC\) advised regulated exchanges that prediction market &\#x27;mentions&\#x27; contracts — which bet on specific words used in speeches or broadcasts — carry a heightened risk of manipulation because their outcomes depend on discrete, hard-to-verify conduct. The guidance follows a $172,539 settlement with a Trump teleprompter operator for insider trading on such contracts and notes that platform Kalshi removed sports-related mention markets during an agency review.

rss · CNBC Finance · Sep 23, 00:58

**「Background」** Mentions contracts ask traders to predict exact words or phrases that will appear in a speech, earnings call, or broadcast, making settlement dependent on a single person&\#x27;s actions rather than publicly verifiable data. The CFTC&\#x27;s letter to designated contract markets outlines four factors exchanges should weigh — external obligations on the subject, potential pressure on their conduct, independent verifiability of the words used, and oversight measures — without creating new regulatory requirements.

**「Impact」** The guidance affects U.S.-regulated platforms like Kalshi, which must now engage with the CFTC during early contract design to address manipulation risks, while rivals such as Polymarket continue offering mention markets only on unregulated international exchanges.

**Tags**: `#CFTC`, `#prediction markets`, `#market manipulation`, `#Kalshi`, `#insider trading`

---

<a id="item-finance-news-3"></a>
### [China Allegedly Tells Banks to Keep Vanke Overdue Loans Off Bad-Debt Books](https://www.reuters.com/world/asia-pacific/china-asks-banks-keep-vanke-loans-off-bad-debt-books-sources-say-2026-09-22/) ⭐️ 7.0/10

Chinese financial regulators have told some large banks not to classify Vanke&\#x27;s overdue loans as bad debt and to extend repayment terms, according to unnamed sources, as a move to avert a developer default. The developer reported a record 886 million yuan loss in 2025 and a 149.5 million yuan net loss in the first half of the year.

telegram · zaihuapd · Sep 23, 03:12

**「Background」** The intervention targets larger banks and also asks them to temporarily suspend interest collection, marking one of Beijing&\#x27;s most direct efforts to prevent a major property developer from defaulting.

**「Impact」** The reported directive could delay recognition of potential losses at Chinese banks and signal continued official support for struggling property developers, affecting investor confidence in the sector&\#x27;s debt treatment.

**Tags**: `#Financial Regulation`, `#Real Estate`, `#Credit Policy`, `#China Markets`, `#Corporate Debt`

---
---
layout: default
title: "Horizon Summary: 2026-09-30 (EN)"
date: 2026-09-30
lang: en
---

> From 52 items, 22 important content pieces were selected

---

**Tools Update**
1. [Zed v1.22.0: BYOK GPT-6.1 Sol, Dynamic Subagent Model Selection, and Auto Compaction](#item-tools-update-1) ⭐️ 8.0/10
2. [Zed v1.23.1-pre: BYOK GPT-6.1 Sol, AI error handling, and JSONL table preview](#item-tools-update-2) ⭐️ 7.0/10
3. [Hunk v0.23.0: Search, Status Line, and Daemon Management](#item-tools-update-3) ⭐️ 7.0/10
4. [pi v0.99.2: MCP exposure, OAuth, and Anthropic federation](#item-tools-update-4) ⭐️ 7.0/10
5. [OpenCode v1.18.34 Patch Release: Session Headers and macOS Signing Fixes](#item-tools-update-5) ⭐️ 5.0/10

**Technology News**
1. [Google DeepMind Releases Gemini 4 Argon Model](#item-tech-news-1) ⭐️ 8.0/10
2. [Large Collaborative Survey of Modern NLP Tokenization Published](#item-tech-news-2) ⭐️ 8.0/10
3. [CO₂Jump: Training-Free Self-Correcting Sampler for Text-Image Consistency](#item-tech-news-3) ⭐️ 8.0/10
4. [DeepSeek open-sources Ascend platform AI components](#item-tech-news-4) ⭐️ 8.0/10
5. [Developer reverses MCP opposition, citing real-world macOS app use](#item-tech-news-5) ⭐️ 7.0/10
6. [Qwen3 Becomes Dominant Language Backbone in 100+ Audio Models](#item-tech-news-6) ⭐️ 7.0/10
7. [Multi-scan radar classification on RadarScenes via temporal accumulation](#item-tech-news-7) ⭐️ 7.0/10
8. [ORTUS AI open-sources RightWayUp 360-degree image rotation model](#item-tech-news-8) ⭐️ 7.0/10
9. [Cloudflare to become a public certificate authority](#item-tech-news-9) ⭐️ 7.0/10
10. [Kimi K3 Joins OpenAI Codex Enterprise Channel](#item-tech-news-10) ⭐️ 7.0/10
11. [Apple reportedly planning October 13 smart home launch](#item-tech-news-11) ⭐️ 7.0/10
12. [Bilibili open-sources Index-Translate multilingual translation model family](#item-tech-news-12) ⭐️ 7.0/10

**Financial News**
1. [China warns EU against trade restrictions amid October deadline](#item-finance-news-1) ⭐️ 8.0/10
2. [Fed&\#x27;s Kashkari: Inflation Still Too High Despite Cooler PCE Data](#item-finance-news-2) ⭐️ 7.0/10
3. [Trading Volume Scrutiny Hits Kalshi and Polymarket Ahead of Potential Listings](#item-finance-news-3) ⭐️ 7.0/10
4. [China Sets New IPO Hurdles for Humanoid Robot Startups](#item-finance-news-4) ⭐️ 7.0/10
5. [Myanmar&\#x27;s Myawaddy cyber-scam hub resurges with 9,300+ recruitment posts, expands to Africa and Americas](#item-finance-news-5) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [Zed v1.22.0: BYOK GPT-6.1 Sol, Dynamic Subagent Model Selection, and Auto Compaction](https://github.com/zed-industries/zed/releases/tag/v1.22.0) ⭐️ 8.0/10

Zed v1.22.0 is a shipped release focused on enhancing AI-assisted development workflows. The most significant changes include Bring-Your-Own-Key \(BYOK\) support for GPT-6.1 Sol, dynamic model selection for subagents via an optional \`model\` parameter in \`spawn\_agent\`, and automatic compaction for subagents. Additional improvements cover dynamic OpenCode model fetching, Git diff toggles, and various bug fixes. These changes are primarily additive and do not introduce breaking changes.

github · zed-zippy\[bot\] · Sep 30, 16:03

**「Changes」** \#\#\# AI
\- Added an optional \`model\` parameter to \`spawn\_agent\` to choose a model for that spawn instead of using the configured subagent model or inheriting the parent model, with the active model shown in its card. \(\[\#64498\]\(https://github.com/zed-industries/zed/pull/64498\); thanks \[itsfuad\]\(https://github.com/itsfuad\)\)
\- Added BYOK support for GPT-6.1 Sol with an OpenAI API key. \(\[\#64968\]\(https://github.com/zed-industries/zed/pull/64968\); thanks \[ktKongTong\]\(https://github.com/ktKongTong\)\)
\- Added Grok 4.7 to the SuperGrok and xAI providers and made it their recommended default. \(\[\#64567\]\(https://github.com/zed-industries/zed/pull/64567\); thanks \[raphaelluethy\]\(https://github.com/raphaelluethy\)\)
\- Added the \`agent.threads\_sidebar.auto\_open\` setting to control whether opening a folder in an existing window also opens the Threads Sidebar. \(\[\#64259\]\(https://github.com/zed-industries/zed/pull/64259\), \[\#64395\]\(https://github.com/zed-industries/zed/pull/64395\); thanks \[jackhwalters\]\(https://github.com/jackhwalters\) and \[joshkent94\]\(https://github.com/joshkent94\)\)
\- Added support for \`&quot;...&quot;\` in \`edit\_predictions.disabled\_globs\` and \`edit\_predictions\_disabled\_in\` so settings can extend inherited edit prediction exclusions and scopes. \(\[\#64540\]\(https://github.com/zed-industries/zed/pull/64540\), \[\#64546\]\(https://github.com/zed-industries/zed/pull/64546\); thanks \[porada\]\(https://github.com/porada\)\)
\- Enabled compaction for subagents. \(\[\#64135\]\(https://github.com/zed-industries/zed/pull/64135\)\)
\- Improved OpenCode model availability by fetching the Zen and Go model list dynamically instead of relying on one bundled with Zed. \(\[\#64585\]\(https://github.com/zed-industries/zed/pull/64585\)\)
\- Improved performance when resolving OpenCode models. \(\[\#64666\]\(https://github.com/zed-industries/zed/pull/64666\)\)
\- Improved Threads Sidebar sizing so changes to \`agent.threads\_sidebar.default\_width\` take effect even after manually resizing the sidebar. \(\[\#64395\]\(https://github.com/zed-industries/zed/pull/64395\); thanks \[joshkent94\]\(https://github.com/joshkent94\)\)
\- Hid deprecated OpenCode models. \(\[\#64666\]\(https://github.com/zed-industries/zed/pull/64666\)\)

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
\- Fixed ligatures being disabled on Windows unless \`buffer\_font\_features\` was set. \(\[\#62338\]\(https://github.com/zed-industries/zed/pull/62338\); thanks \[interkelstar\]\(https://github.com/interkelstar\)\)
\- Fixed LSP completions without edit ranges ignoring the configured \`completions.lsp\_insert\_mode\`. \(\[\#64139\]\(https://github.com/zed-industries/zed/pull/64139\)\)
\- Fixed the Settings window opening with its header off-screen at high DPI scaling on Windows. \(\[\#62073\]\(https://github.com/zed-industries/zed/pull/62073\); thanks \[habisahmad\]\(https://github.com/habisahmad\)\)
\- Fixed importing VS Code \`files.exclude\` into \`file\_scan\_exclusions\`. \(\[\#64492\]\(https://github.com/zed-industries/zed/pull/64492\); thanks \[porada\]\(https://github.com/porada\)\)
\- Fixed “Add to .git/info/exclude” failing in secondary Git worktrees. \(\[\#63967\]\(https://github.com/zed-industries/zed/pull/63967\); thanks \[mateioprea\]\(https://github.com/mateioprea\)\)
\- Fixed terminals retaining about 2 MB of memory per command after the command finished. \(\[\#64405\]\(https://github.com/zed-industries/zed/pull/64405\); thanks \[EcutAtom336\]\(https://github.com/EcutAtom336\)\)
\- Fixed external-agent terminals completing prematurely or reporting the wrong exit status. \(\[\#64544\]\(https://github.com/zed-industries/zed/pull/64544\)\)
\- Fixed a memory leak when closing macOS windows with experimental accessibility enabled. \(\[\#64143\]\(https://github.com/zed-industries/zed/pull/64143\); thanks \[feigeCode\]\(https://github.com/feigeCode\)\)
\- Fixed the terminal grid losing its top alignment when growing on Windows. \(\[\#63699\]\(https://github.com/zed-industries/zed/pull/63699\); thanks \[39ali\]\(https://github.com/39ali\)\)
\- Fixed a crash on Linux \(X11\) when a window was redrawn immediately after GPU device recovery. \(\[\#64570\]\(https://github.com/zed-industries/zed/pull/64570\)\)
\- Fixed language servers not starting for files opened via UNC paths on Windows. \(\[\#56553\]\(https://github.com/zed-industries/zed/pull/56553\); thanks \[Joblen\]\(https://github.com/Joblen\)\)
\- Fixed PowerShell installed by Scoop not being detected when Scoop uses a custom installation directory. \(\[\#62473\]\(https://github.com/zed-industries/zed/pull/62473\); thanks \[jliu666\]\(https://github.com/jliu666\)\)
\- Fixed task worktree variables resolving to the wrong project when the global \`tasks.json\` file was focused, and paths containing spaces breaking Windows tasks. \(\[\#55727\]\(https://github.com/zed-industries/zed/pull/55727\); thanks \[di404\]\(https://github.com/di404\)\)
\- Fixed adding the current line to an Agent thread when no text was selected using \`cmd-&gt;\` \(macOS\), \`ctrl-&gt;\` \(Linux\), or \`ctrl-shift-.\` \(Windows\). \(\[\#64589\]\(https://github.com/zed-industries/zed/pull/64589\)\)
\- Fixed a bug where the block cursor hid the character underneath until its animation completed. \(\[\#64521\]\(https://github.com/zed-industries/zed/pull/64521\); thanks \[linyisu\]\(https://github.com/linyisu\)\)
\- Fixed columnar selections landing in the wrong column around non-ASCII text, tabs, soft wraps, and collapsed content. \(\[\#63723\]\(https://github.com/zed-industries/zed/pull/63723\); thanks \[itsfuad\]\(https://github.com/itsfuad\)\)

**「Impact」** Users leveraging AI assistance in Zed will benefit most from this release, particularly those using subagents or wanting to use GPT-6.1 Sol with their own API key. The addition of dynamic model selection for subagents and automatic compaction improves workflow flexibility and efficiency. Developers using OpenCode integrations will see improved model availability and performance. The release also includes several bug fixes that enhance stability and usability across platforms, including memory leak fixes and improved terminal behavior. No breaking changes are introduced, so upgrading is recommended for all users to take advantage of the new features and fixes.

**Tags**: `#AI`, `#subagents`, `#model-selection`, `#BYOK`, `#OpenCode`

---

<a id="item-tools-update-2"></a>
### [Zed v1.23.1-pre: BYOK GPT-6.1 Sol, AI error handling, and JSONL table preview](https://github.com/zed-industries/zed/releases/tag/v1.23.1-pre) ⭐️ 7.0/10

Zed v1.23.1-pre is a pre-release that adds BYOK support for GPT-6.1 Sol via an OpenAI API key, improves AI error handling and retries, and enhances OpenCode model resolution performance. It also introduces JSONL/NDJSON tabular previews and various bug fixes. As a pre-release, it is not yet stable.

github · zed-zippy\[bot\] · Sep 30, 18:26

**「Changes」** \#\#\# Features

\- \*\*AI\*\*: Added BYOK support for GPT-6.1 Sol with an OpenAI API key.
\- \*\*AI\*\*: Added \`agent.max\_idle\_retained\_threads\` setting to control idle agent thread retention.
\- \*\*AI\*\*: Improved Google AI error messages and added automatic retries when a model is overloaded.
\- \*\*AI\*\*: Improved OpenCode model resolution performance and hid deprecated models.
\- \*\*AI\*\*: Improved plan updates from ACP agents, including panel refreshes after status changes.
\- \*\*AI\*\*: Improved Agent Panel error display when Zed sign-in expires.
\- \*\*AI\*\*: Improved visibility of keyboard-selected agent conversations in the Threads Sidebar.
\- \*\*Git\*\*: Added folder-specific context menu in the Git Panel&\#x27;s tree view.
\- \*\*Languages\*\*: Added JSONL and NDJSON support to the tabular data preview \(cmd-k v / ctrl-k v\).
\- \*\*Languages\*\*: Added extension installation suggestions for more languages when opening unsupported files.
\- \*\*Languages\*\*: Added support for rewrapping text in Typst files.
\- \*\*Remote Development\*\*: Added support for \`terminal.shell\` in remote sessions.
\- \*\*Other\*\*: Added \`alt-/\` to show bindings that can complete a pending multi-keystroke shortcut.
\- \*\*Other\*\*: Added \`soft\_wrap\_indent\` setting \(\`&quot;none&quot;\`, \`&quot;same&quot;\`, \`&quot;extra\_one&quot;\`, \`&quot;extra\_two&quot;\`\) for soft-wrapped continuation lines.
\- \*\*Other\*\*: Improved responsiveness when watching paths on slow or unresponsive filesystems.
\- \*\*Other\*\*: Improved \`editor: select next\` and \`editor: select previous\` to respect the buffer search whole-word option.

\#\#\# Bug Fixes

\- Fixed &quot;Rerun last debug scenario&quot; not running the last scheduled scenario.
\- Fixed a crash on Windows when reading a stored credential with no username.
\- Fixed a crash when pasting multiple selections at the end of a file in Vim mode.
\- Fixed a crash when typing the start of a multi-key binding at the end of a read-only file.
\- Fixed agent notifications showing a thread&\#x27;s original title after renaming.
\- Fixed commit details and diffs waiting behind an in-progress fetch, pull, or push.
\- Fixed external-agent sessions remaining loaded after conversation closure during loading.
\- Fixed images in Markdown table cells ignoring column alignment and vertical centering.
\- Fixed OpenAI model tool calls to MCP servers treating optional fields as required.
\- Fixed missing or outdated output in agent tool results.
\- Fixed search highlights in Markdown Preview hiding matched text with opaque highlight colors.
\- Fixed stale agent responses clearing newer prompts or showing earlier errors.
\- Fixed syntax highlighting for fenced code blocks with extra text after the language name.
\- Fixed pending keybindings list showing \`task: spawn\` instead of the task name.
\- Fixed Zed Cloud connection failing with \`UnknownIssuer\` behind corporate TLS-inspecting proxies.
\- ACP: Fixed partial tool-call display updates when content referenced an unavailable terminal.
\- Fixed inlay hints positioned past buffer end appearing on the last line.
\- Fixed a rare crash when hovering wrapped Markdown text on Linux.
\- Fixed breadcrumb highlighting outside excerpts.
\- Fixed centered layout not applying when a pane was zoomed in.
\- Fixed closing one LSP Logs view stopping streams used by another view or downstream client.
\- Fixed completion details lacking visual distinction from completion labels.
\- Fixed delayed selection of the first entry when opening a context menu.
\- Fixed entries folding when clicked in the Outline Panel.
\- Fixed Helix buffer picker opening in the wrong pane on \`space b\`.
\- Fixed hover flicker after dismissing native menus on macOS.
\- Fixed incorrect selected and hover colors for threads in the Threads Sidebar.

**「Impact」** This is a pre-release \(v1.23.1-pre\) and is not recommended for production use. Users who want to test new AI features, particularly BYOK support for GPT-6.1 Sol, can opt into the pre-release channel. No migration steps are required, but users should expect potential instability. The JSONL/NDJSON table preview and improved AI error handling are notable enhancements for developers working with structured data and AI agents.

**Tags**: `#AI`, `#BYOK`, `#OpenAI`, `#Google AI`, `#OpenCode`

---

<a id="item-tools-update-3"></a>
### [Hunk v0.23.0: Search, Status Line, and Daemon Management](https://github.com/modem-dev/hunk/releases/tag/v0.23.0) ⭐️ 7.0/10

Hunk v0.23.0 is a shipped release that adds slash-based search of diff content, a host-owned status line with inline prompts exposed to extensions, and daemon/client build skew visibility with restart capability. It also includes performance improvements for highlighting and test fixtures, plus UI fixes for opening help and menus without first-use suspension.

github · github-actions\[bot\] · Sep 30, 17:06

**「Changes」** \#\#\# Features
\- \*\*Search\*\*: \`/\` searches diff content via a bundled search extension \(PR \#1096\)
\- \*\*Status Line\*\*: Host-owned status line with inline prompts, exposed to extensions \(PR \#1095\)
\- \*\*Daemon Management\*\*: Make daemon/client build skew visible and resolvable with \`hunk daemon status/restart\` \(PR \#1099\)
\- \*\*Config\*\*: Make wheel scrolling configurable \(PR \#853\)
\- \*\*Extensions\*\*: Add host-owned file-view syntax highlighting \(PR \#1053\)
\- \*\*UI\*\*: Add support for line numbers in &quot;Open file in editor&quot; for Zed \(PR \#1073\)
\- \*\*Extensions Marketplace\*\*: Add \`hunk-triage\` to hunk-extension marketplace \(PR \#1113\)
\- \*\*Extensions Marketplace\*\*: Add \`hunk-starlark\` to extension marketplace \(PR \#1124\)
\- \*\*Theme\*\*: Add a default terminal theme that follows terminal colors \(PR \#1128\)
\- \*\*Extensions\*\*: Bundle GitHub review commands \(PR \#1129\)

\#\#\# Performance Improvements
\- \*\*Highlight\*\*: Load Shiki WASM bytes without base64 decoding \(PR \#1078\)
\- \*\*Test\*\*: Reduce fixture process overhead \(PR \#1092\)
\- \*\*Test \(PTY\)\*\*: Speed up integration synchronization \(PR \#1098\)

\#\#\# Fixes
\- \*\*UI\*\*: Open help and menus without first-use suspension \(PR \#1079\)
\- \*\*Test \(PTY\)\*\*: Synchronize inputs on committed screen state \(PR \#1083\)
\- \*\*Nix\*\*: Install \`hunkdiff\` alias so \`hunk patch\` works \(PR \#1108\)
\- \*\*Test\*\*: Compare install VM paths in one spelling so symlinked tmpdirs pass \(PR \#1120\)
\- \*\*CLI\*\*: Resolve bundled skills by proximity, not candidate order \(PR \#1116\)
\- \*\*UI\*\*: Register one terminal blur listener per diff pane \(PR \#1111\)
\- \*\*Nix\*\*: Use \`stdenv.hostPlatform.isLinux\` \(PR \#1101\)

\#\#\# Documentation
\- Publish v0.22.0 notes \(PR \#1087\)
\- Gate Homebrew availability claims \(PR \#1088\)

\#\#\# New Contributors
\- @seiichi1101 \(PR \#1073\)
\- @schickling-assistant \(PR \#1108\)
\- @shashank-100 \(PR \#1120\)
\- @speedsharmaai \(PR \#1111\)
\- @patrickhaahr \(PR \#1101\)
\- @dhh \(PR \#1128\)

**「Impact」** Users upgrading to v0.23.0 gain new workflows for searching diffs, viewing status information, and managing daemon/client version mismatches. The daemon skew visibility feature is particularly relevant for users running distributed or long-lived daemon processes, as it allows them to detect and resolve version mismatches via \`hunk daemon status\` and \`hunk daemon restart\`. No explicit migration steps are mentioned in the release notes, but users relying on custom status line configurations or extension integrations may need to adapt to the new host-owned status line API. The performance improvements for highlighting and test fixtures should result in faster startup and rendering times, especially for users working with large diffs or complex syntax highlighting.

**Tags**: `#search`, `#status-line`, `#daemon`, `#performance`, `#ui`

---

<a id="item-tools-update-4"></a>
### [pi v0.99.2: MCP exposure, OAuth, and Anthropic federation](https://github.com/earendil-works/pi/releases/tag/v0.99.2) ⭐️ 7.0/10

pi v0.99.2 is a shipped release that improves MCP server handling and adds OAuth and Anthropic workload identity federation authentication options. The default codemode exposure change reduces prompt clutter and improves tool discovery, while new authentication options expand compatibility with secured MCP servers. These are workflow enhancements rather than breaking changes.

github · github-actions\[bot\] · Sep 30, 19:30

**「Changes」** \#\#\# New Features
\- MCP servers with default \`codemode\` exposure no longer appear in the \`codemode\` description or block the first prompt; they appear in a short system prompt section and are discoverable via \`searchTools\(\)\` and \`describeNamespace\(\)\`.
\- Added \`oauth.clientName\` setting for MCP servers that only accept known OAuth clients.
\- Added \`&quot;auth&quot;: \{ &quot;provider&quot;: &quot;&lt;provider&gt;&quot; \}\` for HTTP MCP servers to authenticate with a provider&\#x27;s \`/login\` token as bearer token.
\- Added Anthropic workload identity federation from \`ANTHROPIC\_FEDERATION\_RULE\_ID\`, \`ANTHROPIC\_ORGANIZATION\_ID\`, and \`ANTHROPIC\_IDENTITY\_TOKEN\_FILE\` environment variables.
\- \`/reload\` now enables tools newly added to the \`defaultTools\` setting.

\#\#\# Added
\- Added \`description\` field for MCP servers \(\`pi mcp add --description\`\), shown in system prompt and used to rank tools in search.
\- Added \`describeNamespace\(name\)\` codemode helper returning namespace instructions and tool names.
\- Added \`oauth.clientName\` setting via \`pi mcp add --oauth-client-name\`.
\- Added provider-based authentication for HTTP MCP servers with token read on every request.
\- Added Anthropic workload identity federation support.
\- \`/reload\` now enables newly added \`defaultTools\` while preserving session overrides.

\#\#\# Changed
\- MCP servers with default \`codemode\` exposure no longer appear in \`codemode\` description; \`codemode-deferred\` is now an alias for \`codemode\`.
\- \`codemode\` description no longer includes deferred tools, tool counts, or MCP server instructions.
\- First prompt no longer waits for MCP servers without \`direct\` tools; they connect in background.

\#\#\# Fixed
\- Fixed new sessions intermittently ignoring saved default model or warning no models available for extension-registered native providers with stored credentials.
\- Fixed \`/mcp\` sign-in URL not being clickable when wrapping across lines.
\- Fixed codemode \`image\(\)\` accepting malformed base64 data or unsupported image types causing HTTP 400 errors.
\- Fixed codemode failing to start script worker from standalone Windows executable.
\- Fixed prompt submission slowing down with session length due to repeated model catalog lookups.
\- Fixed model lookups slowing down for providers with refreshed pi.dev catalog \(quadratic time merging\).
\- Fixed built-in tool renderer and minimal mode extension examples removing built-in tools&\#x27; summaries and guidelines.
\- Fixed context overflow detection for Z.AI CN endpoint \`Prompt exceeds max length\` errors.
\- Fixed Anthropic requests failing when tool schema uses keywords Anthropic strict tool use rejects.
\- Fixed provider retries firing immediately when \`Retry-After\` header contains unparseable date.
\- Fixed extension commands without string name or handler crashing pi.
\- Fixed collapsed codemode and MCP tool results filling screen with long single-line output.
\- Fixed \`codemode.mode: &quot;only&quot;\` listing \`read\`, \`bash\`, \`edit\`, and \`write\` in system prompt tool list.
\- Fixed codemode scripts calling wrong MCP tool when two tool names differ only in \`-\` and \`\_\`.

**「Impact」** Users of the pi coding agent who work with MCP servers will benefit from reduced prompt clutter and improved tool discovery through the new codemode exposure handling. Those using secured MCP servers can now leverage OAuth client name settings and provider-based authentication. Users relying on Anthropic services can take advantage of workload identity federation. The fixes address various performance issues, error handling, and edge cases that improve overall stability. No breaking changes are introduced, so upgrading should be straightforward for existing users.

**Tags**: `#mcp`, `#authentication`, `#oauth`, `#anthropic`, `#coding-agent`

---

<a id="item-tools-update-5"></a>
### [OpenCode v1.18.34 Patch Release: Session Headers and macOS Signing Fixes](https://github.com/anomalyco/opencode/releases/tag/v1.18.34) ⭐️ 5.0/10

OpenCode v1.18.34 is a patch release that fixes session identity headers sent with model requests and improves macOS binary signing for better reliability on macOS 27+. The release addresses authentication flow correctness and ensures CLI binaries run reliably on newer macOS versions.

github · opencode-agent\[bot\] · Sep 30, 22:39

**「Changes」** \#\#\# Bugfixes
\- Send namespaced session and parent-session identity headers with model requests.
\- Re-sign locally compiled macOS binaries so they run reliably on macOS 27+.
\- Sign macOS CLI release binaries with a Developer ID.

\#\#\# Community Contributions
\- @dc85: Corrected GPT 6.1 Sol cache pricing in documentation.
\- @metal-huang: Fixed plugin name extraction in /status dialog using path.sep.
\- @ryangamerdev: Ad-hoc re-sign darwin binaries after local compile.

**「Impact」** This release is recommended for all macOS users, particularly those on macOS 27+, to ensure reliable binary execution and proper code signing. Users running locally compiled binaries will benefit from the re-signing fix. The session identity header changes improve authentication flow correctness for model requests. No migration steps are required; users can upgrade directly to v1.18.34.

**Tags**: `#bugfix`, `#macos`, `#binary-signing`, `#session-management`, `#patch-release`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Google DeepMind Releases Gemini 4 Argon Model](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/) ⭐️ 8.0/10

Google DeepMind has released the Gemini 4 Argon model, described as a non-flash variant offering improved intelligence, performance, and price analysis compared to previous Gemini iterations. The model is currently being tested with early adopters, and Google states it will expand availability to developers, enterprises, and consumers once feedback on guardrails is gathered. Unlike prior Gemini releases, Argon is not immediately available to all subscribers, including those on the AI Ultra plan.

hackernews · bradleyg223 · Sep 30, 20:04 · [Discussion](https://news.ycombinator.com/item?id=49913571)

**「Gemini Model Line Evolution」** The Gemini family of models has evolved through several versions, with Gemini 3.8 Flash being a recent iteration noted for its utility in non-complex tasks. Google&\#x27;s approach has typically involved staggered rollouts, beginning with limited access before broader availability. The introduction of Argon represents a shift toward higher-capability non-flash models, following industry trends where providers balance performance gains with controlled deployment.

**「Access Limitations Affect Subscriber Value」** Subscribers to Google&\#x27;s AI Ultra plan may find diminished value as Argon is not yet accessible to them, despite being a premium tier. This mirrors similar strategies by competitors like Anthropic with Fable, though OpenAI provides broader access to Astra for Pro users. Organizations relying on Gemini for enterprise workloads will need to wait for expanded availability, potentially impacting adoption timelines.

**「Community Reacts to Access and Capabilities」** Hacker News users expressed mixed reactions, with some highlighting impressive technical capabilities demonstrated by earlier Gemini models, such as advanced debugging assistance. Others criticized the limited availability, questioning the value of premium subscriptions when new models are restricted to early testers. Discussion also touched on the broader AI landscape, noting increased competition and distributed innovation across cloud providers and startups.

**Tags**: `#AI`, `#Machine Learning`, `#Gemini`, `#Google DeepMind`, `#Model Release`

---

<a id="item-tech-news-2"></a>
### [Large Collaborative Survey of Modern NLP Tokenization Published](https://www.reddit.com/r/MachineLearning/comments/1wuccjf/tokenization_a_survey_for_modern_nlp_r/) ⭐️ 8.0/10

A collaborative survey of modern NLP tokenization has been published, authored by 32 researchers and covering algorithms, evaluations, multilinguality, encodings, theory, and adjacent topics such as constrained generation, token healing, and tokenizer security. The survey also discusses potential replacements for traditional tokenizers, including latent and visual tokenization approaches. The work is available as a preprint on AlphaXiv at https://www.alphaxiv.org/abs/2609.tokenization-survey-modern-nlp.

reddit · r/MachineLearning · /u/mcmcmcmcmcmcmcmcmc\_ · Sep 30, 18:13

**「Background」** Tokenization—the process of splitting text into subword units that language models consume—has become a foundational but historically understudied component of modern NLP pipelines, with choices in algorithm and vocabulary affecting model performance, multilingual coverage, and downstream behavior. Prior work has largely focused on individual tokenizer algorithms \(e.g., BPE, SentencePiece, Unigram\) or their empirical effects, rather than a unified treatment of the field. The referenced survey, hosted on alphaXiv, aims to fill that gap by consolidating research across algorithms, evaluation, multilinguality, theory, and adjacent topics such as token healing and tokenizer security.

<details><summary>References</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=49910852">Tokenization : A Survey for Modern NLP | Hacker News</a></li>
<li><a href="https://www.alphaxiv.org/">Explore | alphaXiv</a></li>
<li><a href="https://huggingface.co/spaces/Xenova/the-tokenizer-playground">The Tokenizer Playground - a Hugging Face Space by Xenova</a></li>

</ul>
</details>

**Tags**: `#nlp`, `#tokenization`, `#survey`, `#machine-learning`, `#language-models`

---

<a id="item-tech-news-3"></a>
### [CO₂Jump: Training-Free Self-Correcting Sampler for Text-Image Consistency](https://www.reddit.com/r/MachineLearning/comments/1wtyl5m/concurrent_image_understanding_and_generation/) ⭐️ 8.0/10

A NeurIPS 2026 paper from Google, Google DeepMind, and Stony Brook University introduces CO₂Jump, a training-free sampler that improves text-image consistency in joint generation. The method uses text confidence and cross-modal attention to guide image updates during sampling, and allows low-confidence tokens to be masked and regenerated so earlier decisions can be revised. It operates with one model forward pass per denoising step and requires no additional training. The authors evaluate on image editing, maze solving, and nonograms, and introduce three datasets: JEdit-1M, JMaze-200K, and JNono-200K. Across 8–512 sampling steps, CO₂Jump was the only compared sampler that improved monotonically on both editing quality and grounding.

reddit · r/MachineLearning · /u/Upstairs\_Theme2785 · Sep 30, 07:28

**「Background」** Joint text-to-image generation often produces outputs where the image and the accompanying text description are inconsistent, such as a model describing the correct solution to a maze while drawing a different path. This mismatch arises because generating both outputs in parallel does not inherently enforce alignment between modalities. Prior approaches typically rely on additional training or iterative refinement without explicit confidence-based correction during sampling.

**「Impact」** For developers and researchers working on multimodal text-to-image systems, CO₂Jump offers a training-free way to improve consistency between generated images and text without modifying the underlying model. Its self-correcting mechanism may be applicable to tasks where verifiable alignment between modalities is required, though the paper&\#x27;s evaluation is limited to puzzle-solving and image-editing benchmarks, so broader deployment remains unproven.

**Tags**: `#multimodal AI`, `#text-to-image generation`, `#sampling methods`, `#consistency`, `#self-correcting models`

---

<a id="item-tech-news-4"></a>
### [DeepSeek open-sources Ascend platform AI components](https://mp.weixin.qq.com/s/X41mKH4Ds-VXUAnK6M8Eww) ⭐️ 8.0/10

DeepSeek open-sourced foundational AI components for Huawei Ascend platforms on September 30, 2026, including TileLang compiler tooling, compute libraries, and distributed communication libraries as counterparts to its NVIDIA platform components. The release includes DeepGEMM Ascend, DeepEP Ascend, TileKernels, FlashMLA, and DeepSelect, with claimed performance near hardware limits and alignment with Huawei&\#x27;s 128-card supernode plans for Ascend 950. The specific performance claims are unverified by the supplied content.

telegram · zaihuapd · Sep 30, 03:09

**「Background」** DeepSeek previously developed and open-sourced similar foundational components for NVIDIA platforms, including TileLang, DeepGEMM, and DeepEP, which serve as the basis for this Ascend platform counterpart release.

**「Impact」** The release enables AI developers to build and optimize models on Huawei Ascend hardware using DeepSeek&\#x27;s toolchain, potentially improving portability between NVIDIA and Ascend ecosystems and supporting Huawei&\#x27;s 128-card supernode architecture for Ascend 950.

**Tags**: `#deepseek`, `#huawei-ascend`, `#open-source`, `#ai-infrastructure`, `#compiler`

---

<a id="item-tech-news-5"></a>
### [Developer reverses MCP opposition, citing real-world macOS app use](https://earendil.com/posts/you-said-no-mcp/) ⭐️ 7.0/10

A developer who previously opposed the Model Context Protocol \(MCP\) has publicly reversed their stance, citing community examples of MCP being used beyond coding tools. The post reflects on protocol design trade-offs including security, observability, and deployment, and acknowledges the value of changing strongly-held technical positions in public. While not announcing a new feature or product, the post documents a notable shift in perspective within the developer tooling community.

hackernews · yarapavan · Sep 30, 09:55 · [Discussion](https://news.ycombinator.com/item?id=49906637)

**「Background」** MCP \(Model Context Protocol\) was introduced as a standardized way for applications to expose context to large language models, initially gaining traction in coding assistants. Early criticism focused on concerns around security, performance, and protocol complexity. The protocol has since seen adoption in non-coding domains, including desktop applications, prompting reevaluation of its broader utility.

**「Impact」** The public reversal may encourage other developers and teams to reconsider MCP for integration in their own tools, particularly in non-coding contexts such as macOS app configuration. It also highlights the importance of revisiting technical decisions as real-world usage evolves, potentially accelerating MCP adoption in diverse application domains.

**「Community Discussion」** Community members shared examples of using MCP in macOS apps like rcmd, Clop, and Lunar for natural language configuration, supporting the post&\#x27;s argument about MCP&\#x27;s expanded utility. Some commenters noted that while MCP has flaws, its widespread compatibility and ease of use make it a practical choice, similar to established technologies like USB-C and HDMI.

**Tags**: `#MCP`, `#developer-tools`, `#protocol-design`, `#macOS`, `#community-discussion`

---

<a id="item-tech-news-6"></a>
### [Qwen3 Becomes Dominant Language Backbone in 100+ Audio Models](https://www.reddit.com/r/MachineLearning/comments/1wuctrt/qwenfamily_llms_are_quietly_becoming_the_backbone/) ⭐️ 7.0/10

A community-driven survey of 100+ audio models in audio.cpp found that Qwen-family LLMs are the most common language backbone, with 32 model families using Qwen architectures and 20 specifically using Qwen3. These models span speech synthesis, ASR, music generation, speech-to-speech, and audio/video tasks, indicating Qwen&\#x27;s broad adoption beyond text-to-speech applications.

reddit · r/MachineLearning · /u/Acceptable-Cycle4645 · Sep 30, 18:31

**「Qwen3 ASR family and audio.cpp ecosystem」** The Qwen3-ASR family, introduced in a January 2026 technical report, includes Qwen3-ASR-1.7B and Qwen3-ASR-0.6B models that support automatic speech recognition and language identification for 52 languages and dialects, building on the audio understanding capabilities of the Qwen3-Omni foundation model. A C++ implementation called qwen3-asr.cpp, released in February 2026, ports these models to the GGML tensor library with Metal GPU acceleration for Apple Silicon. These developments provide the technical foundation for the Qwen3-based audio models now being surveyed across the audio.cpp collection.

**「Implications for Audio Model Development」** The dominance of Qwen3 as a language backbone suggests practitioners building or selecting audio models should prioritize Qwen3-compatible pipelines, as it has become the de facto standard across diverse audio tasks. This trend may influence future model development toward Qwen-centric architectures.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/QwenLM/Qwen3-ASR">GitHub - QwenLM/Qwen3-ASR: Qwen3-ASR is an open-source series ...</a></li>
<li><a href="https://github.com/predict-woo/qwen3-asr.cpp">GitHub - predict-woo/qwen3-asr.cpp: Implementation of Qwen3 ...</a></li>
<li><a href="https://arxiv.org/pdf/2601.21337v1">Qwen3-ASR Technical Report - arXiv.org</a></li>

</ul>
</details>

**Tags**: `#audio-models`, `#qwen`, `#llm-architecture`, `#speech-synthesis`, `#asr`

---

<a id="item-tech-news-7"></a>
### [Multi-scan radar classification on RadarScenes via temporal accumulation](https://www.reddit.com/r/MachineLearning/comments/1wubuz7/multi_scan_radar_object_classification_on/) ⭐️ 7.0/10

A self-post describes extending a single-scan radar object classifier to a multi-scan approach on the RadarScenes dataset by accumulating observations over tracked object histories. Using a causal N=20 sliding-window buffer keyed on RadarScenes&\#x27; persistent track\_id, the method pools points across scans and fuses a causal GRU hidden state with an order-invariant pooled embedding, raising macro F1 from a 0.7370 single-scan baseline to 0.8897. The author reports that most of the gain \(+0.1243\) comes from observation accumulation via point pooling, with temporal ordering \(GRU\) adding a smaller +0.0282, and that end-to-end fine-tuning of the frozen per-scan encoder slightly hurt performance.

reddit · r/MachineLearning · /u/bruno\_pinto90 · Sep 30, 17:55

**「RadarScenes sparsity and temporal radar phenomena」** RadarScenes object instances average only about 2.9 radar points per scan, making single-scan classification sparse, and single scans cannot capture temporal characteristics such as RCS fluctuation and micro-Doppler from limb motion that vary continuously as an object moves. The approach builds on a prior single-scan DeepReflecs encoder \(Ulrich, Glaser &amp; Timm, RadarConf 2021\), a PointNet-style architecture with per-point shared weights.

**「Implication for radar-based perception systems」** For developers building radar-based perception systems, the results suggest that accumulating observations over tracked object histories yields larger accuracy gains than sophisticated sequence modeling, so prioritizing temporal point accumulation and a strong frozen per-scan encoder may be more effective than investing in complex temporal architectures.

**Tags**: `#radar`, `#object-classification`, `#multimodal-sensing`, `#point-cloud`, `#temporal-modeling`

---

<a id="item-tech-news-8"></a>
### [ORTUS AI open-sources RightWayUp 360-degree image rotation model](https://www.reddit.com/r/MachineLearning/comments/1wu6reb/opensourcing_rightwayup_a_360degree_image/) ⭐️ 7.0/10

ORTUS AI has open-sourced RightWayUp, a 360-degree image rotation detection model released under the Apache-2.0 license in six size variants from Pico \(browser-runnable\) to Max. The model estimates rotation angle from upright and abstains on ambiguous inputs such as sky, ground, or close-ups. On held-out test sets, RightWayUp Max achieved 93.0% accuracy within 10 degrees versus 88.4% for Woehrer 2026, and 98.8% on the Woehrer 2026 COCO-based benchmark versus 98.0%. The authors also report that saving COCO-based rotation benchmark images as JPEG q90 drops Woehrer 2026 from 98.0% to 30.2% accuracy, while their models remain stable, and that RightWayUp Max gets every image correct on RotBench. Code and weights are available on GitHub at https://github.com/ortusaitech/rightwayup with a full write-up at https://cheqit.ortusai.io/resources/rightwayup/.

reddit · r/MachineLearning · /u/wildtinkerer · Sep 30, 14:42

**「Image rotation detection context」** Image rotation detection determines how far an image is rotated from upright orientation, a practical need for video analytics where CCTV cameras may be installed upside-down or at an angle. Existing models often suffer from low accuracy and false positives on regular camera-like frames, and some lack permissive licensing, prompting ORTUS AI to train its own model.

**「Practical implications」** Practitioners working with CCTV orientation detection gain a permissively licensed, multi-size model that reportedly outperforms prior approaches on held-out data, with the smallest variant capable of running in a browser. The reported JPEG compression sensitivity of the Woehrer 2026 benchmark suggests evaluation methodology should be scrutinized, and the abstention mechanism may reduce false positives on ambiguous inputs.

**Tags**: `#computer-vision`, `#open-source`, `#model-release`, `#image-rotation`, `#machine-learning`

---

<a id="item-tech-news-9"></a>
### [Cloudflare to become a public certificate authority](https://blog.cloudflare.com/cloudflare-certificate-authority/) ⭐️ 7.0/10

Cloudflare announced plans to become a public certificate authority, having applied to join the Chrome, Apple, Microsoft, and Mozilla root certificate programs and signed an agreement to acquire a widely trusted root certificate from GlobalSign. The new CA will prioritize ACME automation for certificate issuance and renewal, and aims to begin issuing production-grade Merkle tree certificates \(MTC\) by the first quarter of 2027 to support a post-quantum internet. No certificates are being issued yet, as the initiative remains in its early stages.

telegram · zaihuapd · Sep 30, 06:26

**「Certificate authority and ACME context」** Public certificate authorities issue TLS/SSL certificates that browsers and operating systems trust to verify website identity, requiring inclusion in major root programs to be effective. The ACME protocol automates certificate issuance and renewal, popularized by Let&\#x27;s Encrypt, while post-quantum cryptography seeks to secure communications against future quantum computer attacks.

**「Potential effects on certificate automation and post-quantum adoption」** If Cloudflare completes its root program applications and begins issuing certificates, it could expand automated certificate provisioning options for its existing customer base and accelerate adoption of post-quantum Merkle tree certificates once they become available in 2027. Organizations relying on Cloudflare&\#x27;s services may benefit from integrated certificate management, though the post-quantum timeline remains several years out.

**Tags**: `#Cloudflare`, `#Certificate Authority`, `#ACME`, `#Post-Quantum Cryptography`, `#Internet Infrastructure`

---

<a id="item-tech-news-10"></a>
### [Kimi K3 Joins OpenAI Codex Enterprise Channel](https://36kr.com/newsflashes/4005691489112198) ⭐️ 7.0/10

Chinese AI infrastructure company Baseten announced that enterprise users can now invoke Kimi K3 within OpenAI&\#x27;s Codex programming tool, with usage fees billed directly against existing OpenAI procurement commitments. This makes Kimi K3 the first Chinese open-source model to enter OpenAI&\#x27;s enterprise paid settlement system, eliminating the need for additional vendor procurement processes.

telegram · zaihuapd · Sep 30, 11:23

**「OpenAI Codex Enterprise Channel」** OpenAI&\#x27;s Codex is a cloud-based coding assistant that provides API access to enterprise customers under procurement agreements. The enterprise channel allows organizations to consume AI services through existing billing and procurement workflows rather than setting up separate vendor relationships.

**「Simplified Enterprise Procurement for Chinese Models」** Enterprises using OpenAI&\#x27;s procurement framework can now access Kimi K3 without establishing a new vendor relationship or undergoing additional procurement approval, streamlining adoption of Chinese open-source models within existing AI workflows.

**Tags**: `#AI models`, `#enterprise AI`, `#open source`, `#model integration`, `#AI procurement`

---

<a id="item-tech-news-11"></a>
### [Apple reportedly planning October 13 smart home launch](https://www.bloomberg.com/news/articles/2026-09-30/apple-is-finally-ready-to-enter-its-next-big-category-the-smart-home) ⭐️ 7.0/10

According to unnamed sources cited by Bloomberg, Apple is planning to enter the smart home market on October 13 with a 6-inch display smart home hub \(codenamed J490\), an updated HomePod mini, a new Apple TV, and a next-generation Siri AI. The hub is said to use voice and face recognition to identify family members, display personalized content, and control connected devices. Apple has not confirmed the plans and declined to comment.

telegram · zaihuapd · Sep 30, 12:56

**「Apple&\#x27;s existing smart home efforts」** Apple has previously offered HomeKit software for controlling smart home devices and the HomePod line of smart speakers, but has not yet released a dedicated smart home hub with a display. The rumored J490 device would represent a more direct entry into the smart home hardware market.

**「Potential implications for developers and AI systems」** If launched, the rumored hub could require developers to adapt home automation apps and voice interface integrations for a new Apple platform with personalized recognition features, though the unconfirmed nature of the rumors means no immediate action is required.

**Tags**: `#smart-home`, `#apple`, `#ai-assistant`, `#siri`, `#iot`

---

<a id="item-tech-news-12"></a>
### [Bilibili open-sources Index-Translate multilingual translation model family](https://www.ithome.com/1/008/914.htm) ⭐️ 7.0/10

Bilibili&\#x27;s Index LLM team released Index-Translate, a Qwen3.5-based multilingual translation model family with 2B, 9B, and 35B-A3B \(preview\) parameter sizes, supporting 150 languages. The model weights are available on Hugging Face and ModelScope, and the model supports controllable translation features including terminology, formatting, and long document translation, as well as speech and syllable-level controllable translation.

telegram · zaihuapd · Sep 30, 14:08

**「Background」** Multilingual translation models built on top of large language models like Qwen3.5 typically extend base language capabilities with instruction-following for translation-specific tasks such as terminology control and format preservation. Bilibili&\#x27;s Index LLM team has previously developed language models for Chinese and multilingual applications.

**「Impact」** Developers and researchers working on translation and multilingual AI systems can immediately access the 2B and 9B model weights for experimentation and deployment, though the largest 35B-A3B model remains in preview status without full evaluation details.

**Tags**: `#machine translation`, `#open source`, `#multilingual models`, `#Qwen`, `#AI research`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China warns EU against trade restrictions amid October deadline](https://www.cnbc.com/2026/09/30/china-warns-europe-increases-trade-pressure.html) ⭐️ 8.0/10

China&\#x27;s commerce ministry warned it will respond firmly if the European Union imposes restrictions on Chinese businesses, as the EU considers &\#x27;301&\#x27;-style tools to reduce its record trade deficit with Beijing by an October deadline. The ministry said such actions would seriously undermine mutual trust and disrupt ongoing trade negotiations.

rss · CNBC Finance · Sep 30, 03:39

**「Background」** The EU and China have been holding trade talks this summer, with EU Trade Commissioner Maroš Šefčovič warning that Beijing must deliver concrete results by October or face harsher measures. European officials are reportedly finalizing a joint paper urging the European Commission to develop a tool that could cut China off from the European market within 24 hours, mirroring the U.S. Section 301 tariff approach.

**「Impact」** The escalating rhetoric threatens the EU-China trading relationship, worth nearly $1 trillion annually, and could disrupt global supply chains if either side follows through on proposed restrictions or retaliation.

**Tags**: `#trade policy`, `#China-EU relations`, `#tariffs`, `#diplomacy`, `#trade deficit`

---

<a id="item-finance-news-2"></a>
### [Fed&\#x27;s Kashkari: Inflation Still Too High Despite Cooler PCE Data](https://www.cnbc.com/2026/09/30/watch-minneapolis-fed-president-neel-kashkari.html) ⭐️ 7.0/10

Minneapolis Fed President Neel Kashkari said inflation remains too high even after the August core personal consumption expenditures \(PCE\) price index came in at 3% annually, below economists&\#x27; forecasts, and reiterated that the Fed&\#x27;s recent first rate hike in three years may be followed by further increases.

rss · CNBC Finance · Sep 30, 22:21

**「Background」** The August core PCE, the Fed&\#x27;s preferred inflation gauge, fell to 3% year-over-year, below the 3.1% median forecast in a Bloomberg survey, while the Federal Reserve raised interest rates earlier this month for the first time since 2022.

**「Impact」** Kashkari&\#x27;s stance signals that despite moderating price data, the Fed is likely to maintain a restrictive monetary policy path, keeping borrowing costs elevated for consumers and businesses.

**Tags**: `#Federal Reserve`, `#Inflation`, `#Monetary Policy`, `#PCE Price Index`, `#Interest Rates`

---

<a id="item-finance-news-3"></a>
### [Trading Volume Scrutiny Hits Kalshi and Polymarket Ahead of Potential Listings](https://www.cnbc.com/2026/09/30/kalshi-polymarket-trading-volume-scrutiny.html) ⭐️ 7.0/10

Industry observers are questioning whether trading volumes on prediction market platforms Kalshi and Polymarket are inflated, as both companies approach multibillion-dollar valuations and potential public listings. On Sept. 20, nearly half of the dollar volume on Kalshi&\#x27;s ether perpetual contracts came from trades sized between $5,495 and $5,505, while Polymarket&\#x27;s international exchange shows unusually high activity on low-probability contracts, prompting concerns about potential wash trading. Both companies deny any wrongdoing, and the CFTC is reportedly examining Kalshi&\#x27;s ether perpetual trades.

rss · CNBC Finance · Sep 30, 21:09

**「Background」** Prediction markets like Kalshi and Polymarket allow users to trade on the outcome of events, and they have experienced rapid growth, with Polymarket raising at over $20 billion and Kalshi reportedly targeting a $40 billion valuation. Trading volume is a key metric used to justify these valuations, especially as both platforms explore public listings as early as next year.

**「Impact」** If the volume figures are found to be inflated, it could undermine the valuations of Kalshi and Polymarket and affect retail investors who may rely on these metrics when evaluating potential public offerings.

**Tags**: `#Market Integrity`, `#Prediction Markets`, `#Regulatory Scrutiny`, `#Trading Volume`, `#CFTC`

---

<a id="item-finance-news-4"></a>
### [China Sets New IPO Hurdles for Humanoid Robot Startups](https://www.cnbc.com/2026/09/29/china-criteria-humanoid-robot-ipos.html) ⭐️ 7.0/10

China&\#x27;s securities regulator \(CSRC\) has introduced three new IPO criteria for humanoid robot startups — sustainable revenue and commercial orders, narrowing losses with a three-year forecast, and core technology such as robotic brains or hands — potentially disqualifying most of the over 100 companies in the sector from public markets. At least two dozen humanoid-related companies have filed to list in Hong Kong, but few, if any, are expected to meet the new standards.

rss · CNBC Finance · Sep 30, 02:50

**「Background」** The move reflects a cooling in one of the market&\#x27;s hottest sectors, following a surge in investment to $6.95 billion in the second quarter of 2025 and high-profile IPO performances like Unitree&\#x27;s 460% debut gain followed by a near-50% decline.

**「Impact」** The stricter criteria could significantly limit access to public funding for humanoid robot startups, affecting investor appetite and potentially slowing the rapid expansion of China&\#x27;s &\#x27;embodied AI&\#x27; sector.

**Tags**: `#regulatory policy`, `#IPO market`, `#artificial intelligence`, `#humanoid robotics`, `#China finance`

---

<a id="item-finance-news-5"></a>
### [Myanmar&\#x27;s Myawaddy cyber-scam hub resurges with 9,300+ recruitment posts, expands to Africa and Americas](https://mp.weixin.qq.com/s?src=11%C3%97tamp=1790752911&amp;amp;ver=6997&amp;amp;signature=tJVcZ9ZsBUYu0OreujDtX6vVvtS9Ctt465wAlnvsjXgICkCoMtYMDSnHK2jhiUr-3E5MMGed-D*wfCME4QB1ZZfz4l*X25ezIhEUqThiPJvQNTBZPjNwAUtZ8fxehWFr&amp;amp;new=1) ⭐️ 7.0/10

Myanmar&\#x27;s Myawaddy cyber-scam operations have resurged, with over 9,300 recruitment postings advertising &quot;high-salary cross-border jobs&quot; and approximately 83.7% of scams targeting U.S. victims, according to a report citing satellite imagery showing the Thitkate site developing from empty land in June to a built-up area by August.

telegram · zaihuapd · Sep 30, 12:10

**「Background」** The Myawaddy compound was previously dismantled in a joint Chinese-Myanmar crackdown last year, which local sources say was timed to coincide with an ASEAN summit; under pressure, criminal groups had already spread from northern Myanmar to Madagascar, Egypt, the Pacific islands, the Middle East, and Central America.

**「Impact」** The geographic expansion into multiple low-regulation jurisdictions and focus on U.S. victims signals a broad cross-border financial fraud threat, though direct effects on financial markets remain indirect.

**Tags**: `#cybercrime`, `#cross-border crime`, `#Myanmar`, `#financial fraud`, `#satellite surveillance`

---
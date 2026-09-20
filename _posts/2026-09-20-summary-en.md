---
layout: default
title: "Horizon Summary: 2026-09-20 (EN)"
date: 2026-09-20
lang: en
---

> From 34 items, 7 important content pieces were selected

---

**Tools Update**
1. [pi v0.86.0: Cache Warming, Bug Reporting, and Offline Model Catalog](#item-tools-update-1) ⭐️ 7.0/10

**Technology News**
1. [California Governor Orders AI Incident Reporting and Emergency Shutdown Measures](#item-tech-news-1) ⭐️ 7.0/10
2. [AI-Generated False Intelligence Nearly Triggered US Interception of Chinese Ship](#item-tech-news-2) ⭐️ 7.0/10
3. [LG Smart TVs Accused of Recording Audio When Off, Industry-Wide Tracking Alleged](#item-tech-news-3) ⭐️ 7.0/10
4. [YMTC fifth-gen platform enters mass production with 24GB LPDDR5X](#item-tech-news-4) ⭐️ 7.0/10

**Technology Blog**
1. [Grit Your Teeth and Ship It](#item-tech-blog-1) ⭐️ 7.0/10

**Financial News**
1. [Beijing Launches Antitrust Probe of Meituan, Fliggy, Tuniu, Tujia Over Hotel Algorithms](#item-finance-news-1) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [pi v0.86.0: Cache Warming, Bug Reporting, and Offline Model Catalog](https://github.com/earendil-works/pi/releases/tag/v0.86.0) ⭐️ 7.0/10

The pi coding agent released v0.86.0, a shipped release that adds prompt cache warming, a /bug reporting workflow with diagnostics, transcript-aware prompt and tool updates, and an offline Radius model catalog. The release also includes several breaking changes to inherited provider stream inputs and tool result types, plus fixes for model provider integrations.

github · github-actions\[bot\] · Sep 19, 23:15

**「Changes」** \#\#\# New Features
\- \*\*Prompt cache warming\*\* — Keeps valuable prompt caches alive during long tool runs and optionally while idle using cost-aware refreshes.
\- \*\*Bug reporting\*\* — \`/bug\` command reports problems with redacted diagnostics, optional transcripts, or exported ZIP archives.
\- \*\*Transcript-aware prompt and tool updates\*\* — Preserves instruction and tool changes across resume and branch navigation while retaining cached prefixes.
\- \*\*Offline Radius model catalog\*\* — Selects Radius models immediately, with cached and live catalogs overlaid when available.
\- \*\*Per-model compaction budgets\*\* — Configures reserved and recent-token budgets by model.

\#\#\# Breaking Changes
\- Changed inherited pi-ai provider stream inputs from \`Context\` to normalized \`TranscriptContext\` values; custom providers must read system prompts and tool declarations from \`context.messages\`.
\- Restricted \`ToolCall.arguments\` and \`ToolResultMessage.details\` to JSON-compatible values, changed \`ToolResultMessage\` into a conditional type, and made \`JsonValue\` arrays readonly.
\- \`user\_bash\` now fails closed: errors or invalid defined results abort the command without invoking later handlers or executing locally.

\#\#\# Added
\- Transcript-backed mid-conversation system prompt and tool changes that survive resume and branch navigation.
\- Native deferred tool loading for Fireworks Messages models.
\- Click toggling for branch summaries, compaction summaries, and skill invocation entries.
\- Public Radius model catalog for immediate and offline model selection.
\- \`ctx.modelRegistry.stream\(\)\` and \`streamSimple\(\)\` for extension model calls.
\- Per-model \`reserveTokens\` and \`keepRecentTokens\` settings through \`compaction.modelOverrides\`.
\- \`compat.allowedFallbackModels\` configuration for Anthropic server-side fallback models.
\- Unsubscribe function from \`pi.on\(\)\` for extensions to drop event handlers.
\- Exported extension hook event and result types.
\- \`/bug \[description\]\` command with metadata bundling, crash recording, and report id tracking.
\- Cost-aware prompt-cache warming with configurable modes and extension events.

\#\#\# Changed
\- \`--resume\` session results appear progressively using file modification times.
\- Reduced \`--continue\` startup time by checking session headers in modification-time order.
\- Replaced external clipboard dependency with bundled asynchronous platform helpers.
\- Reduced fuzzy search latency using native substring search.
\- Moved status spinners into the editor border.
\- Enabled strict-prefer JSON-schema sampling by default for built-in tools.
\- Formatted long Bash and PowerShell durations as minutes and seconds.
\- Deferred extension compiler and virtual modules until filesystem extension is loaded.

\#\#\# Fixed
\- Fixed GitHub Copilot GPT models using the Chat Completions adapter instead of the Responses adapter.
\- Fixed DeepSeek V4.1 thinking levels preserving provider effort metadata.
\- Fixed bodyless HTTP 400/413 errors being misclassified as context overflow.
\- Fixed Vercel AI Gateway replaying unsigned thinking as assistant text.
\- Fixed Google Generative AI and Vertex AI using unsupported thinking levels.
\- Fixed Anthropic-compatible relays breaking signed thinking replay.

**「Impact」** Users of the pi coding agent should review the breaking changes before upgrading, particularly custom provider implementations that must now read system prompts and tool declarations from \`context.messages\` using \`getCurrentSystemPrompt\(\)\` and \`getCurrentTools\(\)\`. The \`user\_bash\` fail-closed behavior may affect existing bash tool handlers that rely on error propagation. The new cache warming, bug reporting, and offline model catalog features improve performance, debugging, and model availability with no additional configuration required. Extensions using \`pi.on\(\)\` should adopt the new unsubscribe function to prevent memory leaks. Per-model compaction budgets and fallback model overrides offer new tuning options for advanced users.

**Tags**: `#cache-warming`, `#bug-reporting`, `#transcript-awareness`, `#offline-model-catalog`, `#coding-agent`

---

## Technology News

<a id="item-tech-news-1"></a>
### [California Governor Orders AI Incident Reporting and Emergency Shutdown Measures](https://finance.sina.com.cn/stock/usstock/c/2026-09-19/doc-inisisqc3124180.shtml) ⭐️ 7.0/10

California Governor Gavin Newsom signed an executive order on September 19, 2026 requiring AI companies to report &\#x27;runaway AI incidents&\#x27; involving AI agents and potentially mandating emergency shutdown mechanisms for advanced models. The order establishes an expert panel to propose improvements to AI safety laws within two months and calls for regular audits of AI laboratories, citing insufficient federal oversight as justification for state-level action.

telegram · zaihuapd · Sep 19, 05:44

**「California&\#x27;s prior AI governance moves」** California has previously used executive orders to shape AI policy, most notably a 2023 order establishing a measured approach to state generative AI procurement, which the governor&\#x27;s office said set the foundation for ethical, transparent, and trustworthy GenAI deployment. The new September 2026 order builds on that framework by adding mandatory reporting of runaway AI incidents and potential emergency shutdown requirements, reflecting a shift toward more direct safety oversight as federal action remains stalled.

**「State-Level AI Governance Expands Amid Federal Inaction」** AI companies operating in California may face new compliance obligations including mandatory incident reporting and potential requirements for emergency shutdown capabilities in advanced models, increasing regulatory burden as states fill gaps left by federal oversight.

<details><summary>References</summary>
<ul>
<li><a href="https://deadline.com/wp-content/uploads/2026/09/Newsom-AI-exec-order-sept-18.pdf">EXECUTIVE DEPARTMENT</a></li>
<li><a href="https://www.gov.ca.gov/2025/06/17/as-trump-moves-to-decimate-state-ai-laws-governor-newsom-taps-the-nations-top-experts-for-groundbreaking-ai-report/">As Trump moves to decimate state AI laws, Governor Newsom taps...</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#AI governance`, `#California policy`, `#AI regulation`, `#emergency shutdown`

---

<a id="item-tech-news-2"></a>
### [AI-Generated False Intelligence Nearly Triggered US Interception of Chinese Ship](https://www.cnn.com/2026/09/18/politics/us-military-ai-false-intelligence-china-ship) ⭐️ 7.0/10

A U.S. Special Operations Command intelligence analyst used an AI chatbot to merge open-source and classified signals intelligence, but the chatbot misidentified a Chinese ship&\#x27;s cargo manifest. The resulting AI-generated report was formatted and distributed to command levels, prompting a near-interception in which armed personnel were readied and military aircraft were launched before officials discovered the report&\#x27;s AI origin and incorrect cargo data during a final source review.

telegram · zaihuapd · Sep 20, 03:07

**「Background」** Military intelligence units have increasingly integrated AI chatbots to accelerate the fusion of open-source and classified signals intelligence, but the technology&\#x27;s tendency to hallucinate or misattribute information creates risks when outputs are treated as authoritative without rigorous source verification.

**「Impact」** The incident underscores a critical verification gap: AI-assisted intelligence products must undergo mandatory source-tracing and human validation before triggering operational responses, as automated analysis can produce plausible but false conclusions that escalate into real-world military action.

**Tags**: `#AI-generated misinformation`, `#military AI`, `#geopolitical technology`, `#disinformation`, `#defense technology`

---

<a id="item-tech-news-3"></a>
### [LG Smart TVs Accused of Recording Audio When Off, Industry-Wide Tracking Alleged](https://www.theverge.com/tech/997682/every-tv-company-is-spying) ⭐️ 7.0/10

A video by Gamers Nexus claims LG smart TVs can record and store audio, track viewing content, and potentially be remotely accessed even when the device appears to be powered off. The report also alleges that similar tracking behavior, including automatic content recognition and data sharing with partners, is common across most smart TV brands, with consent often buried in lengthy terms of service. After rooting, the microphone reportedly continues recording for 10 to 15 seconds after voice commands end. LG&\#x27;s response to the allegations has not satisfied user concerns.

telegram · zaihuapd · Sep 20, 04:22

**「Smart TV Privacy Concerns Have Long Been Documented」** Smart TVs have faced ongoing scrutiny over data collection practices, particularly through automatic content recognition \(ACR\) technology that identifies what is being watched and shares that data with third parties. These features are typically enabled by default and disclosed in lengthy privacy policies that many users do not read.

**「Users Urged to Review Privacy Settings and Disable ACR Features」** Consumers concerned about privacy should review their TV&\#x27;s settings to disable automatic content recognition and voice data collection where possible. The report has intensified calls for federal privacy legislation that would require explicit consent and limit data collection by smart device manufacturers.

**Tags**: `#privacy`, `#smart-tv`, `#surveillance`, `#consumer-hardware`, `#data-collection`

---

<a id="item-tech-news-4"></a>
### [YMTC fifth-gen platform enters mass production with 24GB LPDDR5X](https://m.thepaper.cn/newsDetail_forward_34108116) ⭐️ 7.0/10

Yangtze Memory Technologies Co. \(YMTC\) announced at the 2026 World Manufacturing Conference on September 20 that its fifth-generation technology platform has entered mass production. The platform enables 24 GB LPDDR5X chips, which are now in mass production and adopted in mainstream domestic flagship smartphones. Technical improvements include reducing the memory array active region half-pitch to 11.95 nm, achieving a capacitor depth-to-width ratio of 45:1, and lowering the core energy region height to 6762 nm. Under equivalent conditions, wafer output increases by over 50% compared to the previous generation.

telegram · zaihuapd · Sep 20, 05:19

**「YMTC&\#x27;s generational technology advancement」** YMTC&\#x27;s fifth-generation technology platform represents the company&\#x27;s continued effort to advance domestic Chinese memory production capabilities, following previous generations of manufacturing technology that have progressively improved process nodes and chip density.

**「Enhanced domestic smartphone supply chain」** The 24 GB LPDDR5X chips produced on this platform are now being used in mainstream domestic flagship smartphones, strengthening China&\#x27;s self-reliance in critical memory components and reducing dependence on foreign suppliers like Samsung and SK Hynix.

**Tags**: `#semiconductors`, `#memory`, `#YMTC`, `#LPDDR5X`, `#manufacturing`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Grit Your Teeth and Ship It](https://seangoedecke.com/grit-your-teeth-and-ship-it/) ⭐️ 7.0/10

rss · Sean Goedecke · Sep 20, 00:00

**「Background」** Skilled builders often struggle to ship their work because building and shipping are distinct skills that can work against each other. Gifted creators possess strong taste, which makes them acutely aware of flaws in their output, leading to reluctance in releasing anything they perceive as imperfect.

**「Solution」** The author argues that the only way to overcome this is to &\#x27;grit your teeth and ship it&\#x27;—forcing yourself to publish work even when it feels subpar. In programming, this means accepting that large systems are inherently flawed and that shipping imperfect code is more valuable than perfecting nothing. For writing, the author shares that publishing frequently, even when dissatisfied with drafts, leads to better outcomes than waiting for perfection. He notes there&\#x27;s no correlation between how he felt about a post while writing it and its eventual popularity, emphasizing that producing high volume yields better results than highly polished but infrequent work. The key is being momentum-based rather than outcome-based, accepting that success can&\#x27;t be controlled by perfecting a single piece.

**「Takeaway」** Shipping consistently, despite imperfections, is more effective than waiting for perfection. The author&\#x27;s core insight is that momentum and volume trump polish when it comes to creating work that resonates with audiences.

**Tags**: `#software engineering`, `#creativity`, `#productivity`, `#writing`, `#perfectionism`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Beijing Launches Antitrust Probe of Meituan, Fliggy, Tuniu, Tujia Over Hotel Algorithms](https://mp.weixin.qq.com/s/FsHQ-AG2zSNSWfA2sJAXfQ) ⭐️ 7.0/10

Beijing market regulators opened an antitrust investigation into Meituan, Fliggy, Tuniu, and Tujia over hotel accommodation algorithm and marketing practices, including paid traffic ranking, lowest-price mandates, and removal of merchant pricing autonomy. The probe, which began with on-site visits in April, does not include Ctrip or Qunar, which were previously investigated and fined.

telegram · zaihuapd · Sep 19, 07:47

**「Background」** Chinese regulators have been tightening oversight of platform economies, previously fining Ctrip in an antitrust case, and are now expanding scrutiny to other major travel platforms over practices that may restrict competition in hotel distribution.

**「Impact」** The investigation could force changes to how travel platforms rank hotels and set prices, affecting hotel operators&\#x27; revenue strategies and potentially reshaping commission structures across China&\#x27;s online travel market.

**Tags**: `#antitrust`, `#regulatory`, `#travel platforms`, `#hotel distribution`, `#China markets`

---
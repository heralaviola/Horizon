---
layout: default
title: "Horizon Summary: 2026-10-05 (EN)"
date: 2026-10-05
lang: en
---

> From 41 items, 12 important content pieces were selected

---

**Tools Update**
1. [earendil-works/pi released v1.0.3](#item-tools-update-1) ⭐️ 7.0/10
2. [pi v1.0.4: wildcard tool patterns, --no-mcp flag, and codemode image persistence](#item-tools-update-2) ⭐️ 6.0/10
3. [openai/codex released rust-v0.160.1](#item-tools-update-3) ⭐️ 5.0/10

**Technology News**
1. [Sona: one transformer replaced our 15+ candidate generators, pre-ranker and ranker in an A/B test \[R\]](#item-tech-news-1) ⭐️ 8.0/10
2. [Reflection releases Beam, a 501B open-weight sparse MoE model](#item-tech-news-2) ⭐️ 7.0/10
3. [Apple&\#x27;s AI Agent Privacy Tensions Surface in Hacker News Debate](#item-tech-news-3) ⭐️ 7.0/10
4. [Qualcomm licenses Huawei LogicFolding chip patents in broad deal](#item-tech-news-4) ⭐️ 7.0/10
5. [U.S.-China AI performance gap narrows to 3% after DeepSeek V4.1 Flash](#item-tech-news-5) ⭐️ 7.0/10
6. [Quad9 Defies French DNS Blocking Order, Faces €580K Daily Fines](#item-tech-news-6) ⭐️ 7.0/10

**Financial News**
1. [Cocoa Prices Climb to $5,670/Ton on El Niño and Climate Fears](#item-finance-news-1) ⭐️ 7.0/10
2. [Brazilian stocks jump as Bolsonaro now seen as heavy favorite to win presidency](#item-finance-news-2) ⭐️ 7.0/10
3. [Brazilian Stocks Rally on Election Result; PTC Surges on $22 Billion Acquisition](#item-finance-news-3) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [earendil-works/pi released v1.0.3](https://github.com/earendil-works/pi/releases/tag/v1.0.3) ⭐️ 7.0/10

v1.0.3 adds Azure Foundry Chat Completions support and image file saving, plus a breaking rename of the Azure provider requiring config updates.

github · github-actions\[bot\] · Oct 5, 08:38

**Tags**: `#breaking-change`, `#azure`, `#image-generation`, `#provider-rename`, `#codemode`

---

<a id="item-tools-update-2"></a>
### [pi v1.0.4: wildcard tool patterns, --no-mcp flag, and codemode image persistence](https://github.com/earendil-works/pi/releases/tag/v1.0.4) ⭐️ 6.0/10

The pi coding agent released v1.0.4, adding wildcard patterns for --tools/--exclude-tools, a --no-mcp flag to disable MCP support per run, and image persistence in codemode. The release also includes several fixes for syntax highlighting, MCP OAuth sign-in, and tool loadout behavior. These are incremental, non-breaking enhancements and fixes.

github · github-actions\[bot\] · Oct 5, 22:03

**「Changes」** \#\#\# New Features
\- \*\*Tool patterns and \`--no-mcp\`\*\*: \`--tools\` and \`--exclude-tools\` now accept \`\*\` wildcard patterns \(e.g., \`--tools read,codemode,&\#x27;mcp\_\_radius\_\_\*&\#x27;\`\). \`--tools\` keeps MCP tools unless an entry starts with \`mcp\_\_\`, and \`--no-mcp\` disables MCP support for a single run.
\- \*\*Codemode persists images\*\*: \`tools.read\(\)\` on an image file now returns an image block that \`image\(\)\` can display.

\#\#\# Added
\- Added \`\*\` patterns to \`--tools\` and \`--exclude-tools\`.
\- Added \`--no-mcp\` flag to disable built-in MCP support per run.

\#\#\# Fixed
\- Fixed syntax highlighting losing colors after the first line of multiline strings and comments in fenced code blocks \(\[\#10143\]\(https://github.com/earendil-works/pi/issues/10143\)\).
\- Fixed codemode scripts not receiving images from \`read\`: \`tools.read\(\)\` now resolves to an image block for image files \(\[\#10251\]\(https://github.com/earendil-works/pi/issues/10251\)\).
\- Fixed MCP OAuth sign-in failing with \`invalid\_redirect\_uri\` on servers with OpenID Connect client registration \(e.g., \`mcp.modem.dev\`\); pi now registers as a native client \(\[\#10493\]\(https://github.com/earendil-works/pi/issues/10493\)\).
\- Fixed \`--tools\` removing MCP tools, which left \`pi --tools codemode\` without any MCP servers; \`--tools\` now keeps MCP tools unless an entry starts with \`mcp\_\_\`.
\- Fixed MCP session shutdown returning while a server was still connecting, leaving its transport open until the server responded or timed out \(\[\#10249\]\(https://github.com/earendil-works/pi/issues/10249\)\).
\- Fixed system prompt rules and skills hint naming tools hidden by \`prepareLoadout\`; hidden tools are now excluded from rules, and \`ToolLoadout\` gains \`getPromptGuidelines\(\)\` \(\[\#10343\]\(https://github.com/earendil-works/pi/issues/10343\)\).
\- Fixed Bedrock requests failing with \`The pending stream has been canceled\` after a stalled HTTP/2 connection not being retried automatically \(\[\#10379\]\(https://github.com/earendil-works/pi/issues/10379\)\).
\- Fixed codemode scripts that patch built-ins \(e.g., \`Array.prototype.toJSON = ...\`\) crashing pi; built-ins are now frozen before the script runs \(\[\#10444\]\(https://github.com/earendil-works/pi/issues/10444\)\).

**「Impact」** Users managing multiple MCP servers or tool configurations will benefit from the new wildcard patterns and \`--no-mcp\` flag, which simplify per-run tool selection. Codemode users working with image files gain improved image handling. The fixes address several edge cases in MCP authentication, syntax highlighting, and tool loadout behavior. No breaking changes or migration steps are required; users can upgrade directly to v1.0.4.

**Tags**: `#cli`, `#mcp`, `#tools`, `#codemode`, `#images`

---

<a id="item-tools-update-3"></a>
### [openai/codex released rust-v0.160.1](https://github.com/openai/codex/releases/tag/rust-v0.160.1) ⭐️ 5.0/10

Bug fix preserving Windows environment variables when launching remote stdio MCP servers with explicitly configured remote environment variables.

github · github-actions\[bot\] · Oct 5, 18:29

**Tags**: `#bug-fix`, `#mcp`, `#windows-compatibility`, `#environment-variables`, `#remote-execution`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Sona: one transformer replaced our 15+ candidate generators, pre-ranker and ranker in an A/B test \[R\]](https://www.reddit.com/r/MachineLearning/comments/1wy4qxm/sona_one_transformer_replaced_our_15_candidate/) ⭐️ 8.0/10

Yandex Music&\#x27;s Sona is a single transformer that replaces 15+ candidate generators and ranking stages in production, using a History Compression technique to halve inference cost.

reddit · r/MachineLearning · /u/SettingAccording8986 · Oct 5, 10:07

**Tags**: `#recommender-systems`, `#transformers`, `#machine-learning`, `#production-ai`, `#ab-testing`

---

<a id="item-tech-news-2"></a>
### [Reflection releases Beam, a 501B open-weight sparse MoE model](https://reflection.ai/blog/introducing-beam) ⭐️ 7.0/10

Reflection has released Beam, a 501 billion parameter open-weight sparse Mixture-of-Experts \(MoE\) model optimized for coding, reasoning, and agentic workloads. The model uses 23 billion active parameters during inference and was pretrained on 23.8 trillion tokens from web and proprietary licensed datasets, with additional reinforcement learning \(RL\) applied for capability enhancement. Reflection claims Beam matches or outperforms comparable open base models, citing a 95.5% accuracy on a geography generalization task versus 92.5% for Opus 5. The model is positioned as a successor to Reflection&\#x27;s earlier work and enters a competitive open-weight landscape alongside models like DeepSeek V4.1 Flash.

hackernews · Philpax · Oct 5, 19:16 · [Discussion](https://news.ycombinator.com/item?id=49969183)

**「Sparse MoE models and open-weight competition」** Sparse Mixture-of-Experts models activate only a subset of parameters per token, enabling large total parameter counts with manageable compute costs during inference. The open-weight model space has seen rapid advancement from both Western and Chinese labs, with DeepSeek&\#x27;s V4.1 Flash \(552B total parameters\) representing a recent high-water mark for freely available models. Reflection&\#x27;s earlier models established a baseline for open-weight reasoning performance, and Beam represents an architectural shift toward sparser, more efficient inference.

**「Limited immediate impact due to missing technical details」** While Beam adds to the open-weight model ecosystem, its practical impact for developers and researchers is constrained by the lack of detailed architecture documentation, training methodology, or reproducible evaluation results. Community commentary highlights both interest in additional open models and skepticism about Western model performance relative to smaller Chinese alternatives. Organizations evaluating open-weight models for production use will need to independently verify Beam&\#x27;s claimed capabilities before adoption.

**「Community compares Beam to DeepSeek V4.1 Flash」** Commenters noted key specification differences between Beam and DeepSeek V4.1 Flash, including Beam&\#x27;s higher active parameter count \(23B vs 8B prefill\) but lower pretraining token count \(23.8T vs 45T\). Some users expressed concern that Western open-weight models remain behind Chinese counterparts despite larger parameter counts, while others welcomed the addition to the open model landscape. One commenter highlighted a demo showing Beam achieving 95.5% on a geography generalization task, though the evaluation methodology was not independently verified.

**Tags**: `#open-weight-models`, `#mixture-of-experts`, `#language-modeling`, `#coding-assistants`, `#benchmarking`

---

<a id="item-tech-news-3"></a>
### [Apple&\#x27;s AI Agent Privacy Tensions Surface in Hacker News Debate](https://stratechery.com/2026/apple-and-a-hackers-future/) ⭐️ 7.0/10

A Hacker News discussion \(185 points, 173 comments\) examines Apple&\#x27;s strategic challenge in balancing user privacy with AI agent capabilities, sparked by concerns over Meta&\#x27;s Muse AI accessing user data without explicit permission. The debate centers on Apple&\#x27;s full-disk access permissions and whether the company&\#x27;s privacy-first approach may limit AI agent functionality, with some users suggesting they might consider alternatives like Meta&\#x27;s platforms for better AI integration. The discussion reflects broader industry tensions between security defaults and the capabilities required for advanced AI agents.

hackernews · maguay · Oct 5, 10:05 · [Discussion](https://news.ycombinator.com/item?id=49962857)

**「Privacy vs. AI Agent Access Tension」** The tension between operating system security models and AI agent capabilities has become a central issue as companies develop general-purpose AI assistants that require access to personal data and system functions. Apple&\#x27;s historically strict permission model, including full-disk access controls, was designed to protect user privacy but may conflict with the data access requirements of sophisticated AI agents.

**「Developer and User Platform Choices at Stake」** The ongoing debate suggests that Apple&\#x27;s approach to AI integration could influence user loyalty and platform choices, with some technically savvy users expressing willingness to switch to platforms that offer more permissive AI agent capabilities. This represents a potential challenge for Apple&\#x27;s ecosystem strategy as AI becomes a more central computing paradigm.

**「Community Divided on Security vs. Convenience」** Commenters are split between those who view Apple&\#x27;s privacy protections as essential safeguards against companies like Meta, and those who argue that overly restrictive permissions limit the utility of AI agents. Some users defend Apple&\#x27;s approach as protecting users from themselves, while others see it as hindering innovation in AI-native computing environments.

**Tags**: `#Apple`, `#AI agents`, `#privacy`, `#security`, `#platform strategy`

---

<a id="item-tech-news-4"></a>
### [Qualcomm licenses Huawei LogicFolding chip patents in broad deal](https://www.bloomberg.com/news/articles/2026-10-05/qualcomm-licenses-patents-on-huawei-s-logicfolding-chip-tech) ⭐️ 7.0/10

Qualcomm and Huawei have signed a multi-year, broad patent cross-license agreement covering 5G, computing, artificial intelligence, and networking technologies, under which Qualcomm will also license patents related to Huawei&\#x27;s LogicFolding multi-layer chip architecture. The deal, announced by Huawei on October 5, 2026, includes Qualcomm purchasing some of Huawei&\#x27;s U.S. patents and is expected to close after regulatory approval, bringing the total expected value of Huawei&\#x27;s patent licensing agreements to over $6.9 billion since 2021. LogicFolding is described as a multi-layer wafer signal routing technique that can reduce heat and signal distance by moving signals through layer space rather than across the chip.

hackernews · 0xedb · Oct 5, 07:46 · [Discussion](https://news.ycombinator.com/item?id=49961861)

**「LogicFolding and U.S.-China tech tensions」** LogicFolding refers to a chip design approach using multiple stacked wafer layers to route signals vertically, a technique that community commenters note appears intuitive in retrospect but was pioneered by Huawei. The agreement comes amid ongoing U.S.-China semiconductor tensions, with Huawei having been added to the U.S. Entity List in 2019, restricting its access to U.S. technology and components.

**「Regulatory and competitive implications」** The deal raises questions about how Qualcomm, a U.S. company, can enter into patent agreements with Huawei while it remains on the Entity List, potentially drawing scrutiny from U.S. regulators. It may also prompt responses from other telecom equipment vendors such as Ericsson, particularly given the cross-license scope covering 5G and AI technologies.

**「Community reactions to LogicFolding and geopolitics」** Commenters expressed mixed views: some praised LogicFolding as a clever technique that reduces heat despite multiple layers, while others questioned the geopolitical implications of a U.S. firm partnering with a sanctioned Chinese company. One commenter noted the irony of the U.S. once emphasizing the criticality of leading the 5G race, now seeing technology shared through licensing deals.

**Tags**: `#semiconductors`, `#patents`, `#hardware`, `#chip-design`, `#Qualcomm`

---

<a id="item-tech-news-5"></a>
### [U.S.-China AI performance gap narrows to 3% after DeepSeek V4.1 Flash](https://www.bloomberg.com/news/articles/2026-10-04/us-lead-in-ai-over-china-narrows-after-deepseek-gains-bi-says) ⭐️ 7.0/10

Bloomberg industry research reports that the U.S. AI performance advantage over China has narrowed to 3% following DeepSeek&\#x27;s V4.1 Flash release, down from about 9% in May and 15% at the start of the year. The report attributes the improvement to Chinese technical accumulation and optimization for domestic hardware, and notes that DeepSeek V4.1 Flash ranked 6th globally on LiveBench in September, though Chinese models still account for only 3 of the top 15. The narrowing gap also raises questions about the effectiveness of U.S. technology export controls.

telegram · zaihuapd · Oct 5, 07:32

**「Background」** The comparison is based on LiveBench, a benchmark suite that evaluates AI model performance across tasks such as coding, mathematics, and language understanding, and is commonly used to track relative progress between leading AI labs. The report tracks a clear trend over time, with the U.S. lead shrinking from roughly 15% at the start of 2026 to 3% after DeepSeek&\#x27;s September update.

**「Impact」** The narrowing performance gap suggests that U.S. export restrictions on advanced semiconductors and AI hardware may be having diminishing returns, as Chinese developers optimize models for locally available chips. This could influence ongoing policy debates about the scope and enforcement of technology controls, and may prompt renewed scrutiny of how effectively such measures slow China&\#x27;s AI advancement.

**Tags**: `#AI`, `#machine learning`, `#benchmarks`, `#geopolitics`, `#DeepSeek`

---

<a id="item-tech-news-6"></a>
### [Quad9 Defies French DNS Blocking Order, Faces €580K Daily Fines](https://torrentfreak.com/dns-resolver-quad9-rejects-french-piracy-blocks-weighs-exit-as-bein-seeks-up-to-e580k-a-day/) ⭐️ 7.0/10

Swiss non-profit DNS provider Quad9 has refused to comply with a French court order requiring it to block access to 58 sports piracy domains requested by beIN Sports. The company faces potential daily fines of up to €580,000 \(€10,000 per domain\) while arguing that its non-logging architecture makes geographically targeted blocking technically infeasible. Quad9 stated it has never blocked any domain and can either implement global blocks or exit the French market entirely. The case follows France&\#x27;s July passage of a law allowing real-time automatic blacklisting of domains, which Quad9 criticized as &\#x27;reckless and dangerous.&\#x27; A Paris court heard arguments last Thursday and is expected to rule within three weeks.

telegram · zaihuapd · Oct 5, 08:05

**「DNS blocking and non-logging resolvers」** DNS-based content blocking works by returning non-routable or filtered responses for targeted domain names, a technique commonly used by ISPs and governments to restrict access to alleged copyright-infringing sites. Quad9 operates as a privacy-focused recursive DNS resolver that does not log client IP addresses or query data, which it argues prevents it from applying geographically targeted blocks without either global filtering or withdrawing service from the requesting jurisdiction. This technical stance has previously drawn regulatory attention, as seen in Russia&\#x27;s 2022 blocking of Quad9&\#x27;s 9.9.9.9 and 149.112.112.112 addresses by the federal service for supervision of communications \(РКН\).

**「Implications for Privacy-Focused DNS Services」** The case tests the limits of geographically targeted DNS blocking on privacy-focused resolvers that do not collect user data, potentially forcing such services to choose between compliance and maintaining their privacy principles. A ruling requiring targeted blocks could set a precedent affecting other non-logging DNS providers operating across multiple jurisdictions.

<details><summary>References</summary>
<ul>
<li><a href="https://otvet.mail.ru/question/270379040">У меня резко перестал dns сервер dns , quad 9 , net - nikita_fedin_238</a></li>

</ul>
</details>

**Tags**: `#DNS`, `#Internet Governance`, `#Privacy`, `#Copyright`, `#Legal`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Cocoa Prices Climb to $5,670/Ton on El Niño and Climate Fears](https://www.cnbc.com/2026/10/05/cocoa-prices-are-climbing-again-heres-why-this-time-is-different.html) ⭐️ 7.0/10

Cocoa futures closed at $5,670 per metric ton on Friday, up from recent declines, as traders brace for supply risks from an emerging El Niño and erratic weather in West Africa, the world&\#x27;s top cocoa-growing region. Goldman Sachs warned that this year&\#x27;s growing season mirrors conditions that preceded the 2023-24 cocoa crisis, when prices surged to a record $12,565 per ton.

rss · CNBC Finance · Oct 5, 18:02

**「Background」** Cocoa is highly sensitive to rainfall and temperature shifts, and West Africa accounts for roughly two-thirds of global production. After the 2024 price spike, chocolate makers like Lindt, Hershey, and Nestlé adjusted by raising prices, shrinking packages, and reformulating products, but they remain exposed to further cost pressures.

**「Impact」** Chocolate manufacturers face renewed cost pressures just weeks before Halloween, a peak demand period, with Lindt cutting its 2026 sales-growth forecast and Nestlé reporting a 20-basis-point drop in gross margin due to higher cocoa costs.

**Tags**: `#commodities`, `#cocoa`, `#El Niño`, `#supply chain`, `#chocolate makers`

---

<a id="item-finance-news-2"></a>
### [Brazilian stocks jump as Bolsonaro now seen as heavy favorite to win presidency](https://www.cnbc.com/2026/10/05/brazilian-stocks-jump-bolsonaro-now-heavy-favorite-to-win-presidency.html) ⭐️ 7.0/10

Brazilian stocks and bank shares surged after first-round election results shifted prediction market odds sharply toward Flávio Bolsonaro, whose fiscal discipline platform is favored by investors ahead of the Oct. 25 runoff.

rss · CNBC Finance · Oct 5, 20:41

**Tags**: `#Brazilian stocks`, `#presidential election`, `#prediction markets`, `#fiscal policy`, `#emerging markets`

---

<a id="item-finance-news-3"></a>
### [Brazilian Stocks Rally on Election Result; PTC Surges on $22 Billion Acquisition](https://www.cnbc.com/2026/10/05/stocks-making-the-biggest-moves-premarket-dkng-itub-ptc.html) ⭐️ 7.0/10

Brazilian stocks rallied after right-wing candidate Flavio Bolsonaro edged out incumbent Luiz Inacio Lula Da Silva by about 2 percentage points in Sunday&\#x27;s election, with the iShares MSCI Brazil ETF \(EWZ\) up 12% and U.S.-listed shares of Itau Unibanco and Banco Bradesco rising more than 13% each. Separately, software company PTC surged 36% after agreeing to be acquired by Schneider Electric for $205 per share, valuing the company at more than $22 billion, with the deal expected to close by the third quarter of 2027.

rss · CNBC Finance · Oct 5, 12:01

**「Background」** The Brazilian election result boosted market sentiment toward the country&\#x27;s financial sector, while the PTC acquisition represents one of the largest software deals in recent years, reflecting Schneider Electric&\#x27;s push to expand its industrial software capabilities.

**「Impact」** The election-driven rally lifted emerging market investors&\#x27; confidence in Brazilian equities, while PTC shareholders gained significantly from the premium acquisition offer, and Schneider Electric positioned itself for broader automation and software integration.

**Tags**: `#Brazilian election`, `#PTC acquisition`, `#premarket stocks`, `#emerging markets`, `#corporate acquisitions`

---
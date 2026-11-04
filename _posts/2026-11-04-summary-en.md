---
layout: default
title: "Horizon Summary: 2026-11-04 (EN)"
date: 2026-11-04
lang: en
---

> From 41 items, 10 important content pieces were selected

---

**Technology News**

1. [Safari 27.3 adds Adaptive Dark Mode](#item-tech-news-1) ⭐️ 7.0/10
2. [The Internals of PostgreSQL resurfaces on Hacker News](#item-tech-news-2) ⭐️ 7.0/10
3. [Developers report silent Postman AI installs and API data sharing](#item-tech-news-3) ⭐️ 7.0/10
4. [Namespace post on running Macs for Apple builds](#item-tech-news-4) ⭐️ 7.0/10
5. [Astra claims of improving Qwen called misleading](#item-tech-news-5) ⭐️ 7.0/10
6. [Aircraft noise in videos can reveal location](#item-tech-news-6) ⭐️ 7.0/10
7. [SemiAnalysis: SpaceX 2027 Datacenter Estimate Raised to About 13GW](#item-tech-news-7) ⭐️ 7.0/10
8. [Putin orders private data centers to reserve 10% capacity](#item-tech-news-8) ⭐️ 7.0/10
9. [NVIDIA reportedly caps Chinese data-center business at 49%](#item-tech-news-9) ⭐️ 7.0/10

**Financial News**

1. [South Korea announces 4.7 trillion won for a sovereign AI model](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>

### [Safari 27.3 adds Adaptive Dark Mode](https://webkit.org/blog/18541/introducing-adaptive-dark-mode/) ⭐️ 7.0/10

Safari 27.3 adds Adaptive Dark Mode, which can automatically darken websites that lack a native dark theme while respecting developer color-scheme preferences and opt-outs. WebKit announced the capability; the supplied account does not include an independent measurement of how sites are restyled. The change extends existing dark-mode techniques rather than introducing a new platform primitive.

hackernews · paddingtone · Nov 3, 21:39 · [Discussion](https://news.ycombinator.com/item?id=50358562)

**「Earlier dark-mode support」** According to WebKit, Safari 12.1 became the first browser to support dark mode on the web in spring 2019. Dark mode is widely used—WebKit says almost 40% of web page loads come from users in dark mode—but not every website provides its own dark version.

**「What it means」** Users who prefer dark mode may see light-only sites restyled automatically, while developers who do not want that treatment can opt out through color-scheme preferences such as color-scheme: light only.

**「Discussion」** Commenters who use dark mode welcomed the feature and said Safari’s respect for color-scheme: light only limits unwanted restyling, while one reader with astigmatism asked for the opposite conversion from dark sites to light. Others pointed to the existing CSS light-dark\(\) function and to the Dark Reader extension, which they say has offered customizable adaptive dark and light modes for years.

<details><summary>References</summary>
<ul>
<li><a href="https://webkit.org/blog/18541/introducing-adaptive-dark-mode/">Introducing Adaptive Dark Mode | WebKit</a></li>

</ul>
</details>

**Tags**: `#safari`, `#webkit`, `#css`, `#dark-mode`, `#web-platform`

---

<a id="item-tech-news-2"></a>

### [The Internals of PostgreSQL resurfaces on Hacker News](https://www.interdb.jp/pg/index.html) ⭐️ 7.0/10

Hacker News is again discussing The Internals of PostgreSQL, a long-standing guide at interdb.jp to PostgreSQL storage, MVCC, concurrency, and related mechanisms. The thread is a resurfacing of existing reference material, not a new PostgreSQL release or an independently measured result. A comment lists earlier discussions of the same guide in January 2019, January and February 2022, and March 2025.

hackernews · ibobev · Nov 3, 21:51 · [Discussion](https://news.ycombinator.com/item?id=50358702)

**「Background」** Hironobu Suzuki&\#x27;s The Internals of PostgreSQL, hosted at InterDB, is a reference for database administrators and system developers that explains how each PostgreSQL subsystem works and how those parts fit together. The same page is not new to Hacker News: earlier threads appeared in January 2019, January and February 2022, and March 2025.

**「Impact」** Readers using the guide while moving to PostgreSQL 18 should not treat its full-text search chapter as current without checking the release notes: one commenter reports that FTS now uses the cluster&\#x27;s default collation provider instead of always libc, so ICU or the builtin PG\_UNICODE\_FAST provider can change FTS and pg\_trgm behavior, and that the release notes say to reindex those indexes after pg\_upgrade.

**「Discussion」** gopalv says a Jepsen report on particledb renewed interest in PostgreSQL&\#x27;s SSI implementation and recommends jumping to the HOT update section, then zHeap and TOAST notes. getbrew argues that chapter has the most practical payoff—HOT applies only when no indexed column changes and the new tuple fits on the same page, so an index on a frequently updated column such as status or updated\_at disables it—and suggests a fillfactor around 80-90 plus comparing n\_tup\_hot\_upd with n\_tup\_upd in pg\_stat\_user\_tables; jon128 separately says the guide does not cover newer MVCC work such as OrioleDB.

<details><summary>References</summary>
<ul>
<li><a href="https://www.interdb.jp/pg/">Hironobu SUZUKI @ InterDB</a></li>
<li><a href="https://freecomputerbooks.com/The-Internals-of-PostgreSQL.html">The Internals of PostgreSQL - for Database Administrators and ...</a></li>

</ul>
</details>

**Tags**: `#PostgreSQL`, `#database internals`, `#MVCC`, `#systems`, `#open source`

---

<a id="item-tech-news-3"></a>

### [Developers report silent Postman AI installs and API data sharing](https://github.com/postmanlabs/postman-app-support/issues/14370) ⭐️ 7.0/10

Developers report that the Postman API client silently installs AI plugins and attempts to share detailed API request data, including secrets, in a GitHub support issue discussed on Hacker News. Commenters say logging covers query parameters and the resolved values of template variables such as \{\{some\_secret\}\}, and that blocking the logging endpoint stops the app from working properly. A healthcare worker said their cyber team decertified Postman and the group switched to Bruno. These are user reports rather than an independent measurement or a confirmed statement from Postman; the supplied item does not include the vendor&\#x27;s response.

hackernews · sidgarimella · Nov 3, 17:22 · [Discussion](https://news.ycombinator.com/item?id=50354960)

**「Background」** Codex and Claude Code can load third-party plugins and open remote MCP \(Model Context Protocol\) connections that add tools and startup instructions to a coding session. Those integrations can include a startup hook and a trust record that marks the hook as approved to run when the agent launches.

**「For API teams」** Teams cannot contain the reported logging by blocking Postman&\#x27;s endpoint: one developer said that breaks the app, and a healthcare cyber team has already decertified Postman, with staff moving to Bruno overnight. Migrating teams should retest scripts that use Postman&\#x27;s pm.\* helpers, because Bruno&\#x27;s scripting API differs and heavy Postman-specific syntax may need edits, and Bruno&\#x27;s migration guide advises deleting the Postman account afterward in an attempt to remove cloud-stored requests, responses, and secrets.

**「Community discussion」** Commenters describe resolved template secrets being sent to Postman and say disabling that logging breaks the app; one healthcare worker reported an internal cyber decertification and an overnight move to Bruno, while another concluded Postman is not HIPAA-compliant. Others call the product bloated after large funding and say they switched to Bruno so request definitions can live in git, though these are individual reports rather than a measured consensus.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/postmanlabs/postman-app-support/issues/14370">[SEVERE] Desktop auto-installs Codex/Claude plugins ... - GitHub</a></li>
<li><a href="https://aiweekly.co/alerts/postman-desktop-silently-installs-plugins-into-codex-claude-code">Postman Desktop Silently Installs Plugins Into Codex, Claude ...</a></li>
<li><a href="https://blog.usebruno.com/postman-to-bruno-migration-guide">Postman to Bruno Migration Guide</a></li>
<li><a href="https://tech-insider.org/api-testing-tools-postman-vs-bruno-vs-insomnia-vs-hoppscotch-2026/">API Testing Tools 2026: Postman vs Bruno vs Insomnia</a></li>

</ul>
</details>

**Tags**: `#postman`, `#api-tools`, `#data-privacy`, `#developer-security`, `#ai-features`

---

<a id="item-tech-news-4"></a>

### [Namespace post on running Macs for Apple builds](https://namespace.so/blog/mac-at-any-scale) ⭐️ 7.0/10

Namespace published “Mac at any scale,” a company blog post about operating Macs for customers who build and test Apple-platform apps. A commenter quotes the post as saying that many customers build and test iOS apps and that those apps cannot be built without a Mac. That is a vendor claim: the article body is not included here, so fleet size, hardware, availability, and procedures are not independently confirmed. The surrounding discussion treats Apple CI and code-signing limits as the constraints being worked around, not as a measured benchmark.

hackernews · anner\_ · Nov 3, 14:53 · [Discussion](https://news.ycombinator.com/item?id=50352758)

**「Why CI needs Macs」** Apple&\#x27;s supported toolchain for building and signing iOS and macOS apps runs on macOS, so continuous integration for those apps is organized around Apple hardware rather than ordinary Linux VMs. Namespace&\#x27;s macOS compute documentation, dated September 22, 2026, says those instances use Apple M4 Pro or M5 Max processors, and an August 25, 2026 write-up of a Namespace rack video described MacBooks being installed as CI servers, a choice viewers questioned in favor of Mac minis.

**「Impact」** Teams that accept Namespace’s stated requirement still need Mac capacity for iOS builds rather than an ordinary Linux CI host, and they must handle Apple’s certificate and signing workflow. A commenter’s personal cross-compiler is not shown here to remove that constraint for typical customer builds.

**「Community discussion」** Commenters disagree on whether a Mac is required: shepherdjerred rejects the quoted claim and describes a personal Linux-hosted cross-compiler used for a few iOS and macOS apps, while kccqzy and borschtplease read the post as evidence that teams are paying to work around Apple bugs, Xcode Cloud, and certificate signing involving plists and p8 files. Those are opinions, not confirmed details of Namespace’s fleet; kccqzy also speculates that buyers would pay a premium for a rack-style Mac because data-center operations are expensive.

<details><summary>References</summary>
<ul>
<li><a href="https://namespace.so/docs/architecture/compute/macos">macOS - Namespace Documentation</a></li>
<li><a href="https://www.explainx.ai/blog/namespace-macbooks-server-racks-can-you-use-august-2026">MacBooks as Servers? Namespace Rack Video (2026) | explainx ...</a></li>

</ul>
</details>

**Tags**: `#macOS`, `#iOS`, `#CI/CD`, `#infrastructure`, `#Apple`

---

<a id="item-tech-news-5"></a>

### [Astra claims of improving Qwen called misleading](https://honnibal.dev/blog/astra-read-write-misleading) ⭐️ 7.0/10

A blog post by syllogism argues that claims Astra can read and write weights to improve Qwen overstate a narrower fix for reasoning loops. The piece is a critique of existing claims, not a newly shipped model or an independently measured result. This item does not include the original Astra write-up or quantitative before-and-after scores.

hackernews · syllogism · Nov 3, 12:21 · [Discussion](https://news.ycombinator.com/item?id=50351111)

**「Weights versus steering」** The claim under criticism said Astra improved Qwen by reading and writing the model&\#x27;s weights. That framing mixed two setups, and the critique states that the experiments that read raw weights and the ones that fix Qwen use completely different techniques. Discussion of the Qwen result centers on reasoning loops, in which the model assigns too low a probability to the &lt;/think&gt; token that should close its thinking trace, a failure commenters say can be reduced by adding a steering vector.

**「How to read the score」** Practitioners citing Astra&\#x27;s author-run MATH-500 rise from 7.9% to 48.1% on Qwen3.5-0.8B should not treat that delta as improved mathematical ability. Reports of the same tests attribute the gain to an edit of about 0.016% of the weights that targeted reasoning loops already noted on Qwen&\#x27;s model card, so the figure does not support adopting weight-space editing as a general replacement for training.

**「Discussion」** A mechanistic-interpretability researcher agreed the original claim was oversold, saying it does not make Qwen better at math and only reduces reasoning loops—where the model assigns too low a probability to the token that closes reasoning—using simple steering that adds a vector. Another commenter said that limitation was already explained later in the original post, so only its title and brief misled, while others called the approach similar to earlier published techniques or said they were still struck that a model appeared able to modify weights at all.

<details><summary>References</summary>
<ul>
<li><a href="https://honnibal.dev/blog/astra-read-write-misleading">The &#x27; Astra can read and write weights to improve Qwen &#x27; post is...</a></li>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights: MATH-500 7.9% to 48.1% ...</a></li>
<li><a href="https://elsolitario.org/en/2026/11/02/mit-csail-astra-edits-0-016-of-qwen3-weights/">Weight-Space Programming: How Astra Edits Weights</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#mechanistic-interpretability`, `#llms`, `#research-critique`, `#qwen`

---

<a id="item-tech-news-6"></a>

### [Aircraft noise in videos can reveal location](https://simonwillison.net/2026/Nov/3/a-sound-that-leaks-your-exact-location/) ⭐️ 7.0/10

Simon Willison highlights a YouTube OSINT demonstration by Colsto in which nearly imperceptible aircraft noise in a video soundtrack is used to infer where the recording was made. The method extracts Doppler curves from passing planes and matches them to public ADS-B flight data using speed, distance, and the gaps between flights. Willison presents this as Colsto’s demonstrated technique, found via Lobste.rs, rather than as a shipped product or an independently measured result; the claim of an exact location comes from that demo.

rss · Simon Willison · Nov 3, 05:32

**「Background」** Aircraft with ADS-B periodically broadcast their position and velocity, and those broadcasts are widely collected into public flight tracks. Separately, the Doppler effect makes a passing plane&\#x27;s engine or propeller tone rise in pitch as it approaches a microphone and fall as it recedes; how quickly that curve changes depends on the recording point&\#x27;s distance and geometry relative to the flight path. Those two long-standing facts are what make ambient aircraft noise a potential location clue.

**「Impact」** People who publish outdoor video can have a recording site inferred from ambient aircraft audio alone, even when the picture contains no landmarks, because the soundtrack can be correlated with public flight tracks.

**Tags**: `#privacy`, `#osint`, `#geolocation`, `#signal-processing`, `#security`

---

<a id="item-tech-news-7"></a>

### [SemiAnalysis: SpaceX 2027 Datacenter Estimate Raised to About 13GW](https://newsletter.semianalysis.com/p/elon-is-doing-it-again-spacex-will) ⭐️ 7.0/10

SemiAnalysis says SpaceX has revised its 2027 datacenter capacity estimate from 10GW to about 13GW, and reports that 3.6GW is already under construction at existing and new sites. The firm says it has identified more than 9GW of capacity and contends this would be the largest datacenter build by any one company in that timeframe, roughly matching all of Google&\#x27;s datacenter capacity from 1999 to 2026 in about 1.5 years. Those figures, including an earlier SemiAnalysis claim that a 10GW plan could support more than $300 billion in annual recurring revenue, come from its datacenter and energy models rather than an independently verified result in this excerpt. The analysts also say power they attribute to Elon Musk&\#x27;s management exceeds 8GW but is still below the more than 9GW of datacenter power they expect online, with supply often identified while construction is already underway.

rss · Semianalysis · Nov 3, 20:44

**「Capacity baseline」** SemiAnalysis tracks AI datacenter scale as critical IT power—the electricity available to run accelerators—in its Datacenter Industry Model, which is the basis for the gigawatt figures in this update. The firm says that just two months earlier it had argued a SpaceX plan for 10 GW in 2027 was feasible; separately, Tom&\#x27;s Hardware, citing SemiAnalysis, reported that xAI&\#x27;s earlier Colossus site used about 200,000 GPUs and roughly 250 MW, with an aim of reaching gigawatt scale by mid-2026.

**「Power still limits usable supply」** AI compute buyers should not treat SpaceX’s revised ~13GW 2027 estimate as available capacity. SemiAnalysis reports that power is often identified only after construction starts, and that power under Elon’s management—more than 8GW—still trails the more than 9GW of datacenter power it expects to come online. For organizations already buying this compute, including Google, which CNBC reported agreed in June to pay SpaceX $920 million a month for 32 months of xAI capacity, delays in securing power would hold back usable supply even where buildings are underway.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/openais-gargantuan-data-center-is-even-bigger-than-elon-musks-xai-colossus-worlds-largest-300-mw-ai-data-center-in-texas-could-reach-record-1-gigawatt-scale-by-next-year">OpenAI&#x27;s gargantuan data center is even bigger than Elon Musk&#x27;s xAI ...</a></li>
<li><a href="https://semianalysis.com/datacenter-industry-model/">Datacenter Industry Model: AI Datacenter Capacity... | SemiAnalysis</a></li>
<li><a href="https://www.cnbc.com/2026/06/05/google-to-pay-spacex-920-million-a-month-for-xai-compute-capacity.html">Google to pay SpaceX $920 million a month for xAI compute ...</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#datacenters`, `#SpaceX`, `#cloud computing`, `#compute capacity`

---

<a id="item-tech-news-8"></a>

### [Putin orders private data centers to reserve 10% capacity](https://www.reuters.com/technology/putin-orders-private-data-centres-set-aside-10-capacity-support-it-2026-11-02/) ⭐️ 7.0/10

Russian President Vladimir Putin has signed a decree requiring non-state data centers in Russia to reserve 10% of their floor space and computing capacity so the government can use it, when needed, to keep domestic IT infrastructure and information resources running. The Ministry of Digital Development must inventory available private data-center space and compute nationwide, and a special commission will be able to require operators to grant access to the reserved resources within 24 hours of notice. With approval from the Federal Security Service \(FSB\), the government may also temporarily use data-center resources located outside Russia. The decree establishes a reservation and requisition framework; the report does not say that any capacity has already been called up.

telegram · zaihuapd · Nov 3, 10:58

**「Background」** Data centers provide the physical premises and computing capacity used to run information systems and information resources. When those facilities are not state-owned, they remain under private operators unless a legal order creates a standing right for the government to call on part of that capacity.

**「Impact」** Operators of non-state data centers in Russia must reserve 10% of premises and computing capacity for government use, and customers on that share can be displaced within 24 hours after a new commission orders access. The Digital Development Ministry will inventory private capacity nationwide, and resources at data centers outside Russia can also be used temporarily if the FSB approves.

**Tags**: `#data-centers`, `#infrastructure-policy`, `#compute`, `#russia`, `#technology-industry`

---

<a id="item-tech-news-9"></a>

### [NVIDIA reportedly caps Chinese data-center business at 49%](https://www.tomshardware.com/tech-industry/data-centers/nvidia-tells-data-center-operators-to-limit-business-from-chinese-customers-with-new-global-restrictions-report-claims-allegedly-restricted-to-49-percent-of-the-total-ensuring-51-percent-are-non-chinese-outfits) ⭐️ 7.0/10

According to a Financial Times report carried by Tom&\#x27;s Hardware, NVIDIA has told data-center operators worldwide to keep business from Chinese companies at no more than 49 percent, so at least 51 percent comes from non-Chinese customers. The reported limit applies only to new and future contracts and does not change leases already signed. It was described as having been conveyed verbally by sales and regional teams, with no formal document identified. NVIDIA was reported as saying that U.S. chips underpin U.S. model and application companies in global competition, and that current U.S. policy encourages cloud providers to accept business from anywhere on U.S. infrastructure.

telegram · zaihuapd · Nov 3, 16:19

**「Background」** The reported request concerns data-center operators that sell computing capacity to customers, including through leases that the account says would remain in force if already signed. In that account, Nvidia ties the instruction to current US policy, describing American chips as the basis for US model and application companies competing globally and saying cloud providers are encouraged to accept customers from anywhere when the work runs on US infrastructure.

**「Impact」** Operators negotiating new data-center contracts may need to track Chinese-company share and stay at or below the reported 49 percent ceiling, while customers on leases already signed are not described as affected. Because the instruction is reported only as a verbal sales directive, its enforceability and exact scope are not independently confirmed.

**Tags**: `#NVIDIA`, `#data centers`, `#China`, `#AI infrastructure`, `#export controls`

---

## Financial News

<a id="item-finance-news-1"></a>

### [South Korea announces 4.7 trillion won for a sovereign AI model](https://mp.weixin.qq.com/s/EldaEmYwi1eXuqkR2il-2A) ⭐️ 7.0/10

South Korean President Lee Jae-myung announced a 4.7 trillion won allocation to develop a sovereign AI model, a nationally controlled system the government aims to make world-leading, according to Cailian. The plan is included in South Korea’s proposed 2027 budget, which the report calls the country’s largest ever and which would raise total government spending 12.8% to 820.9 trillion won.

telegram · zaihuapd · Nov 4, 03:07

**「Background」** President Lee Jae Myung included the allocation in a proposed 2027 budget he presented to parliament, aiming to build a sovereign AI model—an AI system South Korea develops and controls itself instead of depending on foreign companies.

<details><summary>References</summary>
<ul>
<li><a href="https://www.straitstimes.com/asia/east-asia/south-korea-to-double-spending-on-ai-and-chips-in-2027">South Korea to double spending on AI and chips in 2027</a></li>

</ul>
</details>

**Tags**: `#South Korea`, `#AI policy`, `#government budget`, `#semiconductors`, `#fiscal policy`

---
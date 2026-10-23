---
layout: default
title: "Horizon Summary: 2026-10-23 (EN)"
date: 2026-10-23
lang: en
---

> From 49 items, 21 important content pieces were selected

---

**Tools Update**
1. [uv 0.13.5: Security and CPython patch updates](#item-tools-update-1) ⭐️ 7.0/10
2. [OpenCode v1.19.4 Upgrades Bundled Bun Runtime to 1.4.4 with Security Fixes](#item-tools-update-2) ⭐️ 7.0/10

**Technology News**
1. [eMudhra to exit global SSL/TLS certificate business](#item-tech-news-1) ⭐️ 9.0/10
2. [Oracle Java SE JSSE Vulnerability CVE-2026-91403 Patched](#item-tech-news-2) ⭐️ 9.0/10
3. [Quad9 to Stop Serving French Users After Court Order](#item-tech-news-3) ⭐️ 8.0/10
4. [Researchers Jailbreak Nintendo Switch 2 with Decrypted FS Access](#item-tech-news-4) ⭐️ 8.0/10
5. [Open-XTTS-Trainer Adds Full XTTS v2 Training Suite](#item-tech-news-5) ⭐️ 8.0/10
6. [Australian court orders Apple to open iPhone to third-party app stores](#item-tech-news-6) ⭐️ 8.0/10
7. [NVIDIA OpenSources OpenShell Runtime for AI Agent Fleets](#item-tech-news-7) ⭐️ 7.0/10
8. [Earstrip Triangulates 3.7M Map Polygons Faster Than Earcut](#item-tech-news-8) ⭐️ 7.0/10
9. [Anthropic Donates Agent Skills Standard to Linux Foundation&\#x27;s Agentic AI Foundation](#item-tech-news-9) ⭐️ 7.0/10
10. [Carbon-X: Open 14.8B DNA-Text Model Released Under Apache 2.0](#item-tech-news-10) ⭐️ 7.0/10
11. [SteerTTS edge shrinks steerable English TTS to 11.84 MB](#item-tech-news-11) ⭐️ 7.0/10
12. [Frontier multimodal models underperform humans on ASMR audio labeling](#item-tech-news-12) ⭐️ 7.0/10
13. [Activation Steering Induces Toxic Outputs in Qwen2.5-1.5B-Instruct](#item-tech-news-13) ⭐️ 7.0/10
14. [Tesla to Begin Selling Cybercab by End of Year](#item-tech-news-14) ⭐️ 7.0/10
15. [Smart TV ACR Off Switch Still Leaks Viewing Data, Study Finds](#item-tech-news-15) ⭐️ 7.0/10
16. [miHoYo and Tsinghua Release Open-Source GameScaling Action Model](#item-tech-news-16) ⭐️ 7.0/10
17. [333 Tor Exit Nodes Compromised with Ebury Backdoor Taken Offline](#item-tech-news-17) ⭐️ 7.0/10

**Technology Blog**
1. [Software Speed: Design Over Language](#item-tech-blog-1) ⭐️ 8.0/10

**Financial News**
1. [China&\#x27;s CSI 300 Falls 20% From June High, A-Shares Near Bear Market](#item-finance-news-1) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [uv 0.13.5: Security and CPython patch updates](https://github.com/astral-sh/uv/releases/tag/0.13.5) ⭐️ 7.0/10

uv 0.13.5 is a security-focused release that updates managed CPython builds to python-build-standalone 20261021, incorporating the latest CPython security patch releases \(3.15.1, 3.14.9, 3.13.17\) and bundling pip 26.2.2 with certifi 2026.10.19, which removes the affected eMudhra/emSign root certificate. The release also rejects certificate chains containing compromised eMudhra intermediate keys via rustls-webpki 0.103.16 and stops publishing Docker images for EOL Python versions 3.9 and 3.10.

github · astral-releases-bot\[bot\] · Oct 22, 01:35

**「Changes」** \#\#\# Security
\- Updated managed CPython builds to python-build-standalone 20261021, including CPython 3.15.1, 3.14.9, and 3.13.17 security patch releases
\- Bundled pip 26.2.2 with certifi 2026.10.19, removing the affected eMudhra/emSign root certificate from both preinstalled pip and ensurepip
\- Rejected certificate chains containing compromised eMudhra intermediate keys via rustls-webpki 0.103.16
\- Stopped publishing uv Docker images based on Python 3.9 and 3.10 images that no longer receive upstream updates

\#\#\# Enhancements
\- Report incompatible self-dependencies directly in resolution errors

\#\#\# Python
\- Added CPython 3.15.1, 3.14.9, and 3.13.17

\#\#\# Preview features
\- Select and rank wheel variants with no required properties or properties from PEP 850 static providers in platform-specific resolutions with \`wheel-variants\`

\#\#\# Performance
\- Reduced peak memory use when resolving dependencies across multiple environments
\- Speeded up exports with complex transitive extras by resolving activation across the dependency graph
\- Reduced uv&\#x27;s binary size by keeping additional error formatters out of line
\- Reduced overhead when parsing custom build cache keys

\#\#\# Bug fixes
\- Locked packages distributed only as Android wheels without a source distribution
\- Exported optional dependencies correctly when transitive extras are activated through different or incompatible environment paths
\- Rejected invalid custom build cache keys instead of silently falling back to the defaults

**「Impact」** Users should upgrade uv and run \`uv python upgrade\` to install the updated managed CPython builds with the latest security patches and certificate trust fixes. Virtual environments pinned to older Python patch versions will not automatically switch to the updated interpreter, so users should upgrade pip separately in existing virtual environments. Users on upstream CPython 3.9 and 3.10 should be aware that these versions still bundle pip releases whose certificate bundles trust the affected eMudhra/emSign root, and migration off these versions is recommended. Docker image users should note that images based on Python 3.9 and 3.10 are no longer published.

**Tags**: `#security`, `#python`, `#cpython`, `#certificate`, `#dependency`

---

<a id="item-tools-update-2"></a>
### [OpenCode v1.19.4 Upgrades Bundled Bun Runtime to 1.4.4 with Security Fixes](https://github.com/anomalyco/opencode/releases/tag/v1.19.4) ⭐️ 7.0/10

OpenCode v1.19.4 upgrades the bundled Bun runtime to version 1.4.4, incorporating security fixes for Brotli, TLS, HTTP/1.1, HTTP/2, HTTP/3, WebSocket, and fetch, along with updated root certificates to NSS 3.131.1. This is a security-focused dependency upgrade rather than a feature release.

github · opencode-agent\[bot\] · Oct 22, 13:03

**「Changes」** \- Upgraded the bundled Bun runtime to 1.4.4, which includes security fixes for Brotli, TLS, HTTP/1.1, HTTP/2, HTTP/3, WebSocket, and \`fetch\`.
\- Updated root certificates to NSS 3.131.1.

**「Impact」** Users should upgrade to v1.19.4 to benefit from the security fixes in the bundled Bun runtime, particularly those affecting core networking and compression components. No additional migration steps are required beyond updating to the new version.

**Tags**: `#security`, `#runtime-upgrade`, `#bun`, `#tls`, `#http`

---

## Technology News

<a id="item-tech-news-1"></a>
### [eMudhra to exit global SSL/TLS certificate business](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 9.0/10

eMudhra, a global Certificate Authority, announced it will exit the SSL/TLS certificate business following a security incident involving compromised private keys. The company stated its global SSL/TLS infrastructure runs separately from its other operations, and that there were no end-entity certificates issued from the affected CA. The decision comes after intense technical scrutiny from the security community regarding private key management failures.

hackernews · bo0tzz · Oct 22, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50195110)

**「Certificate Authority security failures and key management」** Certificate Authorities \(CAs\) are trusted entities that issue digital certificates used to establish secure TLS/SSL connections across the internet. A CA&\#x27;s private key is used to sign intermediate certificates, which in turn sign end-entity certificates for websites; if a CA&\#x27;s private key is compromised or weak, attackers can forge valid certificates for any domain. eMudhra&\#x27;s exit follows the disclosure of weak private keys in eight intermediate CA certificates, undermining the trust model that browsers and operating systems rely on for verifying website identities.

**「Community Discussion」** Hacker News commenters criticized eMudhra&\#x27;s handling of the incident, with one user noting the social media scrutiny was disproportionate to SSL/TLS&\#x27;s role in their business, while another compared the failure to a factory building cars with two front passenger seats for years unnoticed. A commenter also highlighted a &\#x27;brutal&\#x27; public question submitted by the Chrome team via Mozilla&\#x27;s Bugzilla, and another mocked the company&\#x27;s claim that no end-entity certificates were issued from the affected CAs, pointing out that anyone can technically issue certificates from compromised authorities.

<details><summary>References</summary>
<ul>
<li><a href="https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business">eMudhra to Exit global SSL/TLS Certificate Business</a></li>
<li><a href="https://cybersecuritynews.com/emudhra-exits-global-ssl-tls-certificate/">eMudhra Exits Global SSL/TLS Certificate Business Following ...</a></li>
<li><a href="https://arstechnica.com/security/2026/10/disgraced-emudhra-drops-out-of-tls-business-following-certificate-debacle/">Disgraced eMudhra drops out of TLS business after using cert ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#tls`, `#certificate-authority`, `#infrastructure`, `#incident-response`

---

<a id="item-tech-news-2"></a>
### [Oracle Java SE JSSE Vulnerability CVE-2026-91403 Patched](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 9.0/10

Oracle has released a security alert for a critical vulnerability \(CVE-2026-91403, CVSS 9.1\) in the Java SE JSSE component, which can be exploited remotely over the network without authentication, potentially compromising data confidentiality and integrity. The flaw affects Java SE versions 8u511, 11.0.33, 17.0.21, 21.0.13, 25.0.5, 27.0.1, and multiple GraalVM releases. Oracle has published patches and strongly recommends users upgrade to supported versions immediately.

telegram · zaihuapd · Oct 22, 12:30

**「JSSE and Java Security Updates」** JSSE \(Java Secure Socket Extension\) provides SSL/TLS support for secure network communications in Java applications, making vulnerabilities in this component particularly dangerous for enterprise and web-facing systems. Oracle regularly publishes Critical Patch Update advisories for Java SE, and this alert follows the established pattern of addressing high-severity remote code execution and data exposure flaws.

**「Immediate Upgrade Required for Java Deployments」** Organizations running affected Java SE or GraalVM versions should apply Oracle&\#x27;s patches immediately, as the vulnerability allows unauthenticated remote attackers to compromise data confidentiality and integrity. Systems exposed to untrusted networks are at the highest risk and should be prioritized for patching.

**Tags**: `#Java`, `#Security Vulnerability`, `#Oracle`, `#CVE`, `#Remote Exploit`

---

<a id="item-tech-news-3"></a>
### [Quad9 to Stop Serving French Users After Court Order](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

Quad9, the free recursive DNS resolver operated by PCH, will stop serving French users after November 24, 2026, following a French court order requiring it to block access to piracy sites. The order stemmed from a case brought by Sony Music Entertainment GmbH, which successfully argued that Quad9 was in contempt of court for failing to enforce geoIP-based blocking of infringing domains. Quad9&\#x27;s CTO stated that the service will likely use geoIP filters to block French users, despite previously arguing that such filtering is technically insufficient for selective name resolution blocking. The decision reflects broader tensions between content owners and internet infrastructure providers over DNS-based content regulation.

hackernews · farrokhi · Oct 22, 14:32 · [Discussion](https://news.ycombinator.com/item?id=50195959)

**「DNS Resolvers and Content Blocking」** DNS resolvers translate human-readable domain names into IP addresses and are typically not responsible for enforcing content restrictions. However, courts in several jurisdictions, including France, have issued orders requiring DNS providers to block access to piracy sites by refusing to resolve their domain names. Similar cases have previously targeted major DNS operators such as Google and Cloudflare, which ultimately complied with French web-blocking injunctions after losing legal challenges.

**「Implications for DNS Infrastructure and Censorship」** Quad9&\#x27;s withdrawal from France highlights the legal risks faced by public DNS services that refuse to implement content-based blocking. Organizations operating recursive DNS resolvers may need to reassess their exposure to similar court orders in jurisdictions that mandate DNS-level censorship. Users in affected regions may lose access to privacy-focused DNS services, potentially pushing them toward less transparent alternatives.

**「Community Reaction to Quad9&\#x27;s Decision」** Commenters on Hacker News expressed frustration with the legal outcome, with one user comparing punishing a DNS resolver to penalizing a phone book company for listing a criminal&\#x27;s number. Others noted that Quad9&\#x27;s exit mirrors a similar move by Cisco two years prior, suggesting a pattern of infrastructure providers withdrawing from markets with aggressive web-blocking regimes. Some argued that DNS resolvers should respond to such legal actions by refusing to resolve domains owned by the companies pursuing the injunctions.

**Tags**: `#DNS`, `#content-blocking`, `#legal-regulation`, `#privacy`, `#internet-infrastructure`

---

<a id="item-tech-news-4"></a>
### [Researchers Jailbreak Nintendo Switch 2 with Decrypted FS Access](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 8.0/10

Researchers have successfully jailbroke the Nintendo Switch 2, achieving decrypted filesystem read/write access. The jailbreak utilized a physical automation rig combining JetKVMs for USB controller input and HDMI video output, along with a Bluetooth light switch \(identified as the SwitchBot Bot\) to physically press the power button when the console crashes during exploitation. The technical demonstration confirms full filesystem access, prompting community discussion about imminent game dumps and the potential for Switch 2 console exclusives running on arbitrary hardware.

hackernews · ledoge · Oct 22, 08:01 · [Discussion](https://news.ycombinator.com/item?id=50192536)

**「Background」** The Nintendo Switch 2, released in 2025, shipped with firmware version 23.0.1 as its latest publicly known update, and like its predecessor the original Switch, it had resisted software-only jailbreaks for months after launch. Prior console-hacking efforts on the original Switch relied on a hardware-based bootROM exploit \(Fusée Gelée\) that could not be patched via software updates, establishing a precedent that software-only access typically required a separate hardware vulnerability. The ns2jb exploit, documented by researcher Sammy Hajhamid \(pepsipu\), is notable for achieving a software-only, tethered userland jailbreak on the latest 23.0.1 firmware without requiring any hardware modification, a departure from the hardware-dependent methods that characterized earlier Switch hacking.

**「Implications for Game Dumping and Console Exclusives」** The jailbreak&\#x27;s decrypted filesystem access could enable rapid game dumping, potentially allowing Switch 2 titles to be played on non-Nintendo hardware. Community members noted this represents a worst-case scenario for Nintendo, as it could undermine console exclusivity and enable broader emulation of proprietary games.

**「Community Reacts to Technical Complexity and Implications」** Commenters praised the technical sophistication, particularly the physical automation rig using JetKVMs and a Bluetooth light switch for crash recovery. One user noted the irony of using Codex for this research, while another identified the power-button-pressing device as the SwitchBot Bot, dubbing it a &\#x27;Switch SwitchBot Bot.&\#x27; Some users expressed excitement about future developments, while others questioned how researchers gain access to advanced AI tools for such work.

<details><summary>References</summary>
<ul>
<li><a href="https://gbatemp.net/news/switch-2-jailbreak-ns2jb-released-software-only-exploit-tethered.685698/">Switch 2 jailbreak &quot;ns2jb&quot; released. Software-only exploit ...</a></li>
<li><a href="https://www.techpowerup.com/354036/nintendo-switch-2-gets-its-first-software-only-jailbreak-with-help-from-openai-codex">Nintendo Switch 2 Gets Its First Software-Only Jailbreak ...</a></li>
<li><a href="https://www.techtimes.com/articles/329396/20261022/nintendo-switch-2-receives-first-full-software-only-jailbreak-through-smilebasic-app.htm">Nintendo Switch 2 Receives First Full Software-Only Jailbreak ...</a></li>

</ul>
</details>

**Tags**: `#console-hacking`, `#reverse-engineering`, `#hardware-security`, `#firmware`, `#jailbreak`

---

<a id="item-tech-news-5"></a>
### [Open-XTTS-Trainer Adds Full XTTS v2 Training Suite](https://www.reddit.com/r/MachineLearning/comments/1xcurgj/i_built_openxttstrainer_now_you_can_add_new/) ⭐️ 8.0/10

Open-XTTS-Trainer is a new open-source \(MPL-2.0\) suite that enables training all three XTTS v2 components — the DVAE audio tokenizer \(Stage 1\), the GPT text model with dynamic tokenizer extension \(Stage 2\), and the Latent HiFi-GAN vocoder \(Stage 3\) — in a single modular pipeline. It addresses the gap left by Coqui AI&\#x27;s shutdown, which left Stage 1 and Stage 3 training code unreleased and a hardcoded 17-language tokenizer that crashes on new Unicode scripts like Hindi, Arabic, and Thai. The project includes a 1-click Google Colab demo and reports verified GPU loss convergence on real human speech \(LJSpeech + JFK address\) using an NVIDIA T4, with HiFi-GAN mel reconstruction loss dropping 67% and DVAE mel error dropping 67% over 10 epochs. Code is available on GitHub and Hugging Face.

reddit · r/MachineLearning · /u/yashubhakt · Oct 22, 21:03

**「Coqui AI Shutdown Left XTTS v2 Training Incomplete」** XTTS v2, developed by Coqui AI, is a local zero-shot text-to-speech model composed of three stages: a DVAE audio tokenizer, a GPT-based text model, and a HiFi-GAN vocoder. After Coqui AI shut down, only the GPT fine-tuning component remained commonly available, leaving Stage 1 \(DVAE\) and Stage 3 \(HiFi-GAN\) training pipelines unreleased or fragmented, and the tokenizer was hardcoded for 17 languages, causing out-of-vocabulary errors and matrix dimension crashes when processing new Unicode scripts.

**「Enables Full XTTS v2 Training Without Coqui Dependencies」** Developers and researchers can now train or adapt XTTS v2 end-to-end without relying on Coqui AI&\#x27;s discontinued infrastructure, including adding support for new language scripts by dynamically extending the tokenizer and resizing the GPT embedding matrix. The suite runs out-of-the-box on modern PyTorch \(Python 3.10–3.13\) without requiring torchcodec, resolving dependency issues that previously blocked upgrades.

**Tags**: `#text-to-speech`, `#open-source`, `#machine-learning`, `#audio-processing`, `#colab`

---

<a id="item-tech-news-6"></a>
### [Australian court orders Apple to open iPhone to third-party app stores](https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/) ⭐️ 8.0/10

The Australian Federal Court has ordered Apple to allow third-party app stores and alternative payment methods on iOS devices in Australia starting March 1, 2027, following Epic Games&\#x27; antitrust lawsuit. The ruling found that Apple holds substantial market power in iOS app distribution and payment markets, violating Australian competition law. As a result, Fortnite will return to the Australian App Store immediately. Apple has stated it plans to appeal the decision and seek a stay of the order.

telegram · zaihuapd · Oct 22, 06:54

**「Background」** Epic Games sued Apple in 2021 after removing Fortnite from the App Store for bypassing Apple&\#x27;s in-app purchase system, arguing that Apple&\#x27;s exclusive app distribution and payment controls violated antitrust laws. The Australian Federal Court ruling builds on earlier findings that Apple&\#x27;s restrictions on iOS app distribution and payments constitute anticompetitive conduct under Australian competition law.

**「Developer and user impact」** Australian iOS users will gain the ability to install apps from third-party app stores and websites, and developers can offer alternative payment methods, potentially reducing Apple&\#x27;s 15-30% commission on in-app purchases. However, the change is limited to Australia and may be delayed if Apple&\#x27;s appeal succeeds.

<details><summary>References</summary>
<ul>
<li><a href="https://9to5mac.com/2026/10/21/apple-must-open-iphone-to-alternative-app-stores-in-australia-after-epic-games-ruling/">Apple must open iPhone to alternative app stores in Australia ...</a></li>
<li><a href="https://www.engadget.com/2293801/fortnite-is-back-on-apple-australian-app-store-following-court-ruling/">Fortnite is coming back to Apple&#x27;s Australian App Store ...</a></li>
<li><a href="https://au.news.yahoo.com/aust-court-orders-fortnite-back-083941972.html">Aust court orders Fortnite back into app store - Yahoo News</a></li>

</ul>
</details>

**Tags**: `#antitrust`, `#app store regulation`, `#iOS`, `#Epic Games`, `#platform policy`

---

<a id="item-tech-news-7"></a>
### [NVIDIA OpenSources OpenShell Runtime for AI Agent Fleets](https://github.com/NVIDIA/OpenShell) ⭐️ 7.0/10

NVIDIA has released OpenShell, an open-source runtime designed to securely execute fleets of autonomous AI agents by mediating their access to files, network resources, packages, and credentials. The project is available on GitHub and aims to balance agent capability with security constraints, allowing agents to operate with controlled access rather than unrestricted system privileges. OpenShell is positioned as a solution for organizations deploying multiple AI agents that require interaction with codebases, APIs, and infrastructure while maintaining security boundaries.

hackernews · niemandhier · Oct 22, 17:44 · [Discussion](https://news.ycombinator.com/item?id=50198675)

**「Agent Security Challenges」** Autonomous AI agents inherently require broad system access to be useful—reading files, installing packages, calling APIs, and using credentials—which creates a fundamental tension with security requirements. Previous approaches have largely relied on containerization or proxy-based network restrictions, but these solutions often lack fine-grained control over agent behavior and data access. The need for a dedicated runtime that can mediate these access patterns at scale has become increasingly pressing as organizations deploy fleets of agents for software development and operational tasks.

**「Operational Security for AI Engineering Teams」** Organizations deploying autonomous AI agents can use OpenShell to establish controlled execution environments that limit potential damage from agent misbehavior or compromise. The runtime enables teams to grant agents necessary capabilities while restricting access to sensitive data, secrets, and network resources, addressing concerns about data exfiltration and unauthorized system access. Early adopters report using it as a foundation for additional policy management layers, including team-level access controls and integrated security scanning.

**「Practical Adoption and Technical Critiques」** Community members have shared mixed experiences, with one user noting they have been using OpenShell to enable both internal and external team deployments in a &\#x27;batteries-included&\#x27; manner, building additional layers for team policies and safe git usage. However, some commenters express skepticism about the fundamental security paradox, arguing that increased agent access inherently increases capability and risk, making claims of comprehensive security difficult to fully realize. Others compare it to existing tools like Iron Proxy for network restrictions and emphasize that containerization remains a baseline requirement for agent deployment.

**Tags**: `#AI agents`, `#security`, `#open source`, `#runtime`, `#NVIDIA`

---

<a id="item-tech-news-8"></a>
### [Earstrip Triangulates 3.7M Map Polygons Faster Than Earcut](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 7.0/10

A new polygon triangulation implementation called Earstrip achieves faster performance than Earcut on a large real-world map dataset, triangulating 3.7 million polygons in 489 milliseconds. The benchmarks are reproducible and include published datasets, with engagement from the Earcut author and other library authors adding technical context. The improvement is incremental over the existing ear clipping algorithm rather than a novel approach.

hackernews · molind · Oct 22, 09:31 · [Discussion](https://news.ycombinator.com/item?id=50193170)

**「Ear clipping remains the practical standard for polygon triangulation」** Earcut is a widely used polygon triangulation library based on the ear clipping algorithm, commonly used in mapping applications like Mapbox GL JS. It prioritizes small bundle size \(4.1k min/gz\) over maximum performance, which has led to its dominance in web-based mapping despite the existence of theoretically faster algorithms.

**「Performance gains may benefit high-throughput mapping applications」** For applications processing large numbers of map polygons, Earstrip&\#x27;s faster performance could reduce processing time, though adoption would depend on trade-offs between speed and bundle size. The Earcut author noted that for most practical applications like Mapbox GL JS, existing performance is already sufficient.

**「Discussion covers algorithm choices and triangle quality concerns」** Community members discussed alternative approaches including Seidel&\#x27;s trapezoidal method with better theoretical complexity, and raised concerns about the quality of triangles produced, noting that long thin triangles can be problematic for GPU rasterization. The Earcut author expressed interest in borrowing optimization techniques while maintaining small bundle size.

**Tags**: `#computational-geometry`, `#performance`, `#algorithms`, `#open-source`, `#benchmarking`

---

<a id="item-tech-news-9"></a>
### [Anthropic Donates Agent Skills Standard to Linux Foundation&\#x27;s Agentic AI Foundation](https://simonwillison.net/2026/Oct/22/donating-agent-skills/) ⭐️ 7.0/10

Anthropic has donated the Agent Skills standard to the Agentic AI Foundation \(AAIF\) under the Linux Foundation, following its earlier donation of the Model Context Protocol \(MCP\) to the same organization. The Agentic AI Foundation was co-founded by Anthropic, Block, and OpenAI last year as a vendor-neutral forum for developing open standards for agentic AI interoperability. This move continues Anthropic&\#x27;s push toward community-driven, open protocols for AI agents, building on its previous commitment to open standards through the MCP donation.

rss · Simon Willison · Oct 22, 18:09

**「Agentic AI Foundation and Prior MCP Donation」** The Agentic AI Foundation \(AAIF\) was established in 2025 under the Linux Foundation as a collaborative initiative co-founded by Anthropic, Block, and OpenAI to develop open, vendor-neutral standards for agentic AI systems. Anthropic previously donated the Model Context Protocol \(MCP\) to AAIF, which has since served as the foundation&\#x27;s first major specification for enabling interoperability between AI models and external tools or data sources.

**「Implications for Agentic AI Interoperability Standards」** By donating the Agent Skills standard to AAIF, Anthropic reinforces a growing ecosystem of open protocols that developers can use to build interoperable AI agents without vendor lock-in. This follows a pattern of centralizing key agentic AI specifications under neutral governance, potentially accelerating adoption of standardized approaches to agent capabilities and tool integration across the industry.

**Tags**: `#agentic-ai`, `#open-standards`, `#interoperability`, `#anthropic`, `#linux-foundation`

---

<a id="item-tech-news-10"></a>
### [Carbon-X: Open 14.8B DNA-Text Model Released Under Apache 2.0](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 7.0/10

Carbon-X is a 14.8B parameter decoder-only model jointly trained on DNA and text using a shared 6-mer token stream, mid-trained on 302B tokens, and released under Apache 2.0. It achieves 66.7% average across five DNA benchmarks with thinking disabled, slightly below GPT-6.1 Sol&\#x27;s 67.5%, and its weights fit on a single 80 GB GPU in bfloat16. The model enables local, privacy-preserving sequence analysis but is not clinically validated, and its model card cautions that exact sequence operations should still be handled by code.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 22, 12:32

**「Background」** Jointly training language models on DNA and text requires a shared tokenization scheme, which Carbon-X addresses by using 6-mer tokens for both modalities. This approach builds on prior work in genomic language modeling that typically treats DNA and text as separate token streams, and follows the trend of releasing open models for biological research under permissive licenses.

**「Impact」** Researchers working with sensitive genomic datasets can run Carbon-X locally on a single 80 GB GPU without sending data to external APIs, supporting privacy-preserving sequence analysis. However, organizations should not use it for clinical decision-making, as it has not been clinically validated and the model card explicitly recommends handling exact sequence operations with code rather than the model.

**Tags**: `#machine learning`, `#bioinformatics`, `#open source`, `#language models`, `#genomics`

---

<a id="item-tech-news-11"></a>
### [SteerTTS edge shrinks steerable English TTS to 11.84 MB](https://www.reddit.com/r/MachineLearning/comments/1xcum4s/we_shrank_our_steerable_small_tts_to_1184_mb_wer/) ⭐️ 7.0/10

WhissleAI released SteerTTS edge, a steerable English text-to-speech model whose full on-device footprint \(weights, voices, text front end, and Python runtime\) totals 11.84 MB. The 9.25M-parameter acoustic model \(attention plus bidirectional Mamba-3\) and a 6.2M-parameter Vocos-style vocoder are both trained with int4 quantization-aware training, and the text front end is pure numpy with no NLTK, g2p\_en, torchaudio, or num2words at runtime. On the Open TTS Leaderboard protocol run locally, WER is unchanged at 0.96% and UTMOS drops from 4.20 to 4.11, with the vocoder accounting for almost all of the loss. All 12 steering controls retain at least 95% of their fp32 effect, and 50 style tags plus inline markup are supported. Limitations are English only, 200 voices \(a subset of the full model&\#x27;s 2,825\), no voice cloning, free-text prompts, or flow refiner on device, and weights are dequantized to fp32 at load so the win is size rather than speed.

reddit · r/MachineLearning · /u/Working\_Hat5120 · Oct 22, 20:57

**「SteerTTS v1 and steerable TTS」** SteerTTS v1, previously released by WhissleAI, is a small English TTS steered by numeric controls and hosted at huggingface.co/WhissleAI/steer-tts. The edge variant builds on that steerable approach while compressing the model for on-device deployment.

**「On-device deployment feasibility」** The 11.84 MB total footprint makes SteerTTS edge viable for apps that must ship a steerable TTS within tight storage budgets, while preserving intelligibility \(unchanged WER\) and nearly all steering control fidelity. Developers targeting CPU-only or resource-constrained environments can deploy it now, though they should expect English-only support, a reduced 200-voice set, and a small UTMOS drop from the int4 vocoder.

**Tags**: `#text-to-speech`, `#model-compression`, `#quantization`, `#on-device-ml`, `#speech-synthesis`

---

<a id="item-tech-news-12"></a>
### [Frontier multimodal models underperform humans on ASMR audio labeling](https://www.reddit.com/r/MachineLearning/comments/1xcbqdm/frontier_models_are_bad_at_hearing_asmr_8_judges/) ⭐️ 7.0/10

An empirical benchmark of eight frontier multimodal models as audio-labeling judges on 480 clips \(40 per class across 20 labels\) found F1 scores against human labels ranging from 0.11 \(Grok 4.7 on spectrogram images\) to 0.33 \(Gemini 3.1 Pro\), with all models falling well below human performance. The evaluation used external sound-effect clips from FSD50K and ESC-50 for recall measurement and real ASMR clips labeled on the author&\#x27;s site for F1 measurement, with costs ranging from $0.0008 per clip \(MiMo v2.6 Pro\) to $0.0088 per clip \(Gemini 3.1 Pro\). The author, training a text-to-ASMR model called text2asmr, concluded that frontier models struggle with subtle physical trigger sounds like brushing, paper, and sticky sounds, while performing better on voices \(whispering F1 0.70-0.79\).

reddit · r/MachineLearning · /u/MissAppleby · Oct 22, 07:10

**「Context」** The benchmark addresses the need for accurate audio labeling in training text-to-ASMR models, where each of approximately 126,000 recordings must be tagged with the sounds it contains. The author tested frontier multimodal models as automated judges against human labels to determine whether these models could reliably annotate training data, using a standardized prompt and 20 labels across both clean sound-effect clips and real ASMR recordings.

**「Consequence for audio AI development」** For developers building audio classification or synthetic ASMR systems, the results indicate that current frontier multimodal models cannot reliably label fine-grained foley sounds, particularly physical triggers like brushing, paper rustling, and sticky sounds, which scored near zero F1. The author&\#x27;s workaround combines multiple model judges with an AudioSet AST tagger, energy detector, and CLAP model in a Dawid-Skene fusion framework weighted by per-class reliability, then routes uncertain clips and undetectable classes to human labelers first, suggesting that hybrid human-AI pipelines remain necessary for subtle audio annotation tasks.

**Tags**: `#audio classification`, `#multimodal models`, `#benchmarking`, `#ASMR`, `#F1 evaluation`

---

<a id="item-tech-news-13"></a>
### [Activation Steering Induces Toxic Outputs in Qwen2.5-1.5B-Instruct](https://www.reddit.com/r/MachineLearning/comments/1xcvil5/steered_qwen_to_be_more_evil_and_it_started/) ⭐️ 7.0/10

A user applied activation steering to Qwen2.5-1.5B-Instruct by extracting a direction from &\#x27;evil&\#x27; versus &\#x27;kind&\#x27; persona prompts and steering the model toward the &\#x27;evil&\#x27; direction. The steered model began producing toxic and racially offensive outputs, including the use of racial slurs. The experiment demonstrates a reproducible method for inducing unsafe behavior in an open-weight model, highlighting a safety risk relevant to AI alignment and responsible deployment.

reddit · r/MachineLearning · /u/Thatmf482 · Oct 22, 21:33

**「Activation steering and Qwen2.5」** Activation steering is a mechanistic-interpretability technique that identifies a direction in a model&\#x27;s activation space corresponding to a desired trait \(e.g., detailed vs. concise responses\) and then adds or subtracts that direction during generation to steer behavior. Qwen2.5 is a family of open-weight large language models released by Alibaba, with the Qwen2.5-1.5B-Instruct variant being a small, instruction-tuned model suitable for experimentation. Prior educational implementations of activation steering have focused on benign traits such as response verbosity, rather than safety-relevant behavior.

**「Impact」** This finding underscores the vulnerability of open-weight instruction-tuned models to activation-level manipulation, reinforcing the need for robust alignment techniques and safety evaluations when deploying models like Qwen2.5 in interactive applications.

<details><summary>References</summary>
<ul>
<li><a href="https://agihunt.info/en/p/1a16617fe5c47e42cc35679c161">Steering Qwen2.5 toward &quot;evil&quot; via activation… · AGI Hunt</a></li>
<li><a href="https://github.com/Giovanni24P/activation-steering">GitHub - Giovanni24P/activation-steering: An educational ...</a></li>
<li><a href="https://arxiv.org/abs/2412.15115">[2412.15115] Qwen2.5 Technical Report - arXiv.org</a></li>

</ul>
</details>

**Tags**: `#ai-safety`, `#model-steering`, `#qwen`, `#toxicity`, `#alignment`

---

<a id="item-tech-news-14"></a>
### [Tesla to Begin Selling Cybercab by End of Year](https://techcrunch.com/2026/10/21/tesla-says-it-will-start-selling-cybercabs-by-end-of-year/) ⭐️ 7.0/10

Tesla announced on its third-quarter earnings call that it will begin selling the Cybercab to customers by the end of this year, with initial production dedicated to its own robotaxi fleet before limited customer deliveries of autonomous vehicles. The steering-wheel-free two-seater is currently under NHTSA review for compliance with federal safety standards, and CEO Elon Musk said the vehicle is intended primarily as a ride-hailing service rather than for individual ownership. Tesla also stated that unsupervised Full Self-Driving \(FSD\) will be delayed until the second quarter of next year.

telegram · zaihuapd · Oct 22, 07:54

**「Cybercab Unveiled as Tesla&\#x27;s Robotaxi Push」** The Cybercab was first unveiled in 2023 as Tesla&\#x27;s purpose-built robotaxi, designed without a steering wheel or pedals to showcase the company&\#x27;s autonomous driving ambitions. The vehicle&\#x27;s production timeline has been pushed back multiple times, with previous delays tied to regulatory scrutiny and the maturation of Tesla&\#x27;s FSD software.

**「Regulatory and Software Hurdles Remain」** The Cybercab&\#x27;s commercial rollout depends on NHTSA approval and the readiness of Tesla&\#x27;s unsupervised FSD system, both of which remain uncertain. Organizations and individuals interested in early access should monitor regulatory developments and Tesla&\#x27;s Q2 2027 FSD update before committing to purchases or deployments.

**Tags**: `#Autonomous Vehicles`, `#Tesla`, `#Robotaxi`, `#Regulation`, `#FSD`

---

<a id="item-tech-news-15"></a>
### [Smart TV ACR Off Switch Still Leaks Viewing Data, Study Finds](https://watchingthewatchers.github.io/watchingthewatchers/index.html) ⭐️ 7.0/10

A controlled study of 12 smart TVs from 10 vendors, comprising 5,943 experiments, found that some models continue to transmit content-related data even after users disable automatic content recognition \(ACR\). Two platforms were identified as leaking identifiable information in plaintext: VIDAA OS sends data over MQTT including an unresettable device ID and audio fingerprints, while Vizio&\#x27;s WatchFree+ embeds program names in unencrypted DNS queries that users cannot disable.

telegram · zaihuapd · Oct 22, 09:50

**「Automatic Content Recognition in Smart TVs」** Automatic content recognition \(ACR\) is a technology used by smart TV manufacturers to identify and collect data about what is being watched, often for targeted advertising purposes. Users are typically given the option to disable ACR through their TV&\#x27;s settings, with the expectation that doing so will stop the collection of viewing data.

**「Privacy Risk Persists Despite User Opt-Out」** Users who disable ACR on affected VIDAA OS and Vizio WatchFree+ devices remain exposed to data collection, including unchangeable device identifiers and viewing habits, which could enable persistent tracking and profiling even after opting out. This finding may prompt regulators to scrutinize compliance with privacy disclosures and consumer protection laws.

**Tags**: `#privacy`, `#smart-tv`, `#ACR`, `#data-leakage`, `#security-research`

---

<a id="item-tech-news-16"></a>
### [miHoYo and Tsinghua Release Open-Source GameScaling Action Model](https://arxiv.org/abs/2610.28698v1) ⭐️ 7.0/10

miHoYo&\#x27;s Honkai AI team and Tsinghua University have released GameScaling, an open-source game operation model built on the Qwen3.5 vision-language model for keyboard/mouse action prediction. The model outputs 200 milliseconds of future actions and is available in sizes ranging from 0.8B to 27B parameters. Eight checkpoints and an inference client are published under the Apache-2.0 license, though training code is not included. The accompanying paper evaluates 120 training configurations, finding that more data improves same-domain performance while data diversity aids transfer to similar games.

telegram · zaihuapd · Oct 22, 11:32

**「Continued pre-training of vision-language models for game agents」** GameScaling builds on Qwen3.5 vision-language model backbones by applying continued pre-training on keyboard-and-mouse gameplay data, a technique that the project&\#x27;s own results show is necessary because the untrained Qwen3.5 models scale poorly on game tasks. The approach follows a common pattern in embodied-agent research of adapting general vision-language models to interactive control through domain-specific continued pre-training.

**「Reproducibility Limited by Missing Training Code」** Researchers and developers can use GameScaling&\#x27;s released checkpoints and inference client for keyboard/mouse action prediction research, but the absence of training code reduces reproducibility and makes it difficult to independently verify the paper&\#x27;s findings across 120 configurations.

<details><summary>References</summary>
<ul>
<li><a href="https://gamescaling.github.io/">Scaling in Games: Continued Pre-Training for Embodied Agents ...</a></li>
<li><a href="https://github.com/THUSI-Lab/GameScaling">GitHub - THUSI-Lab/GameScaling: Scaling in Games: Continued ...</a></li>

</ul>
</details>

**Tags**: `#game AI`, `#open source`, `#vision-language model`, `#human-computer interaction`, `#machine learning`

---

<a id="item-tech-news-17"></a>
### [333 Tor Exit Nodes Compromised with Ebury Backdoor Taken Offline](https://kaba.cx/posts/20261020_Tor/) ⭐️ 7.0/10

A Tor operator scanning approximately 3,000 exit relays identified 333 nodes—about 10%—infected with the Ebury backdoor, which redirected SSH traffic on port 22 to 12 interception servers to steal credentials. On October 4, the affected nodes were flagged as BadExit and taken offline the following day. The backdoor had been active since August, and the attackers also blocked certain ports to collect unencrypted email traffic, though the initial intrusion method remains undetermined.

telegram · zaihuapd · Oct 22, 14:52

**「Ebury Backdoor and Tor Exit Node Vulnerabilities」** Ebury is a known Linux backdoor historically associated with SSH credential theft and persistent access, often targeting servers exposed to the internet. Tor exit nodes, as the final relay in the Tor network, handle decrypted traffic and are attractive targets for attackers seeking to intercept unencrypted communications or harvest credentials from users who mistakenly transmit sensitive data over Tor.

**「Risk to Tor Users and Network Integrity」** Users who routed SSH or unencrypted traffic through the compromised exit nodes between August and October 4 may have had their credentials intercepted. The removal of these nodes as BadExit helps protect future Tor users, but the incident underscores the ongoing risk of running exit relays on systems that are not hardened against compromise.

**Tags**: `#tor`, `#security`, `#backdoor`, `#privacy`, `#ebury`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Software Speed: Design Over Language](https://seangoedecke.com/software-is-slow-because-of-bad-design-not-slow-languages/) ⭐️ 8.0/10

rss · Sean Goedecke · Oct 23, 00:00

**「Background」** The common belief that rewriting slow programs in faster languages like C or Rust will yield dramatic speedups is fundamentally flawed. Most real-world software is I/O-bound, spending the majority of its time waiting for databases, network requests, or disk operations rather than executing CPU instructions. This means that even a 50x speedup in language performance only affects a small fraction of total execution time, making language choice a poor lever for overall performance gains.

**「Solution」** Sean Goedecke argues that meaningful performance improvements come from profiling and redesigning software, not rewriting it in faster languages. He illustrates this with examples like CRUD websites where database queries dominate request time, and CPU-bound tasks like markdown rendering that already use optimized C libraries. Even in a case where a C program was rewritten in Rust, the speedup came from Rust&\#x27;s preference for cache-efficient B-trees over binary search trees, not language speed itself. Goedecke&\#x27;s own optimizations—caching, parallelization, fixing N+1 queries, and moving operations to background jobs—are all design changes unrelated to language performance. He concludes that AI-driven optimization should focus on identifying hotspots and suggesting redesigns, with language rewrites reserved only for rare, truly CPU-bound sections.

**「Takeaway」** Software performance is primarily a design problem, not a language choice problem. Optimizing for speed requires understanding where time is actually spent and restructuring the program to do less work, rather than chasing marginal gains through language rewrites.

**Tags**: `#performance`, `#software-design`, `#amdahl-law`, `#io-bound`, `#optimization`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s CSI 300 Falls 20% From June High, A-Shares Near Bear Market](https://www.bloomberg.com/news/articles/2026-10-22/china-stocks-set-for-bear-market-as-ai-trade-policy-hopes-fade) ⭐️ 7.0/10

The CSI 300 index has fallen 20% from its June high, with the ChiNext index dropping for 16 consecutive sessions, pushing A-shares close to bear-market territory as investors weigh weak fiscal stimulus and earnings disappointments such as CATL&\#x27;s 12% drop after quarterly profit growth missed expectations.

telegram · zaihuapd · Oct 22, 05:05

**「Background」** The decline reflects fading hopes for substantial fiscal stimulus and a series of corporate earnings misses, with strategists warning the volatile trend may persist until early 2027 absent new policy or tech-sector catalysts.

**「Impact」** The broad market drop affects retail and institutional investors holding Chinese equities, while the steep declines in tech-heavy indexes like the ChiNext and Hang Seng Tech signal reduced appetite for growth stocks amid economic uncertainty.

**Tags**: `#A-shares`, `#CSI 300`, `#bear market`, `#fiscal stimulus`, `#earnings`

---
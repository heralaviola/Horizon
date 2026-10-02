---
layout: default
title: "Horizon Summary: 2026-10-02 (EN)"
date: 2026-10-02
lang: en
---

> From 46 items, 14 important content pieces were selected

---

**Tools Update**
1. [uv 0.12.22: CPython patch versions and workspace lockfile enhancements](#item-tools-update-1) ⭐️ 5.0/10

**Technology News**
1. [Zig v0.17.0 Release Adds Async I/O and Build System Enhancements](#item-tech-news-1) ⭐️ 8.0/10
2. [Google Research unveils Cogentic multi-agent system for mathematical proof discovery](#item-tech-news-2) ⭐️ 8.0/10
3. [Greg Kroah-Hartman on LLM-Generated Kernel Vulnerability Reports](#item-tech-news-3) ⭐️ 7.0/10
4. [arXiv caps submissions at two per calendar month per submitter](#item-tech-news-4) ⭐️ 7.0/10
5. [NeurIPS 2026 Paper Tackles Topological Out-of-Domain Generalization in Dynamical Systems](#item-tech-news-5) ⭐️ 7.0/10
6. [FLEET Algorithm Enhances Best-of-N Generation with MCTS-Guided Reward Attribution](#item-tech-news-6) ⭐️ 7.0/10
7. [Hand tracking gaps in robot demos can hide critical contact phases](#item-tech-news-7) ⭐️ 7.0/10
8. [Anthropic Proposes Opt-Out AI Training on Copyrighted Works in Australia](#item-tech-news-8) ⭐️ 7.0/10
9. [Claude Code Adds TypeScript-Based Mods Plugin System](#item-tech-news-9) ⭐️ 7.0/10

**Technology Blog**
1. [Why You Shouldn&\#x27;t Build an LLM Torture Factory](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [Fed October rate hike odds fall after weak jobs report](#item-finance-news-1) ⭐️ 7.0/10
2. [Premarket stock moves: Nike miss, ON Semiconductor-Synaptics deal, and HDD production concerns](#item-finance-news-2) ⭐️ 7.0/10
3. [Bitget expects limited recovery from $388 million hack, absorbs losses from own capital](#item-finance-news-3) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [uv 0.12.22: CPython patch versions and workspace lockfile enhancements](https://github.com/astral-sh/uv/releases/tag/0.12.22) ⭐️ 5.0/10

uv 0.12.22 is a shipped release that adds new CPython patch versions \(3.10.22 through 3.14.8\) and incremental lockfile enhancements for workspace dependency groups, along with bug fixes and a Rust toolchain update. The changes are incremental and do not introduce breaking changes or major new capabilities.

github · astral-releases-bot\[bot\] · Oct 2, 00:20

**「Changes」** \#\#\# Python
\- Add CPython 3.10.22, 3.11.17, 3.12.15, 3.13.16, and 3.14.8

\#\#\# Enhancements
\- Accept uppercase release suffixes in wheel platform tags
\- Record workspace-member default groups in lockfiles
\- Record workspace-member dependency-group Python requirements in lockfiles
\- Record default groups for non-project workspace roots in lockfiles
\- Record dependency-group Python requirements for non-project workspace roots in lockfiles
\- Format URLs and paths consistently in CLI messages
\- Hide the unsupported \`--offline\` option from \`uv publish\` help

\#\#\# Preview features
\- Honor \`--no-default-groups\` in \`uv audit\`
\- Report a clear error when \`uv audit\` or \`uv tool audit\` runs offline and hide the unsupported option from help

\#\#\# Configuration
\- Add \`UV\_PYTHON\_ARCH\` to select an interpreter architecture independently of its Python version

\#\#\# Performance
\- Reduce uv&\#x27;s binary size by compressing embedded Python download metadata

\#\#\# Bug fixes
\- Verify unchanged requirements against existing lockfile hashes when relocking
\- Honor dependency-group Python requirements at non-project workspace roots
\- Use each selected workspace member&\#x27;s recorded default groups during frozen sync
\- Avoid false entry-point warnings for required workspace members

\#\#\# Other changes
\- Raise the minimum supported Rust version for building uv to 1.97 and update the toolchain to Rust 1.99

**「Impact」** Most users can upgrade directly; the release is backward compatible. Users who build uv from source must use Rust 1.97 or later \(toolchain updated to 1.99\). Workspace users benefit from more accurate lockfile recording of default groups and dependency-group Python requirements, which may cause lockfiles to be regenerated on the next \`uv lock\`. The new \`UV\_PYTHON\_ARCH\` setting allows selecting interpreter architecture independently of Python version, useful for cross-platform environments.

**Tags**: `#python-versions`, `#lockfiles`, `#workspaces`, `#cli`, `#dependency-management`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Zig v0.17.0 Release Adds Async I/O and Build System Enhancements](https://ziglang.org/download/0.17.0/release-notes.html) ⭐️ 8.0/10

Zig v0.17.0, released on October 2, 2026, introduces async I/O support, enhanced build system integration, and expanded target support for systems programming. The release focuses on improving developer tooling and low-level control, with community discussion highlighting interest in future stackless coroutine I/O and first-class fuzzer tooling. Some users expressed frustration that loop vectorization remains disabled despite the LLVM upgrade effort.

hackernews · ErenayDev · Oct 2, 20:56 · [Discussion](https://news.ycombinator.com/item?id=49938521)

**「Zig&\#x27;s async/await history and LLVM integration」** Zig previously removed async/await support while the team redesigned the API from the ground up, with the new async I/O framework targeted for release in version 0.16.0. The 0.16.0 release notes established that the 0.17.0 cycle would be short, aiming mainly to upgrade to LLVM 22 and finish separating the make process \(build runner\) from the configure process \(build.zig\). Loop vectorization remained disabled in 0.16.0 to work around an LLVM regression, a limitation that community members continued to express frustration about in the 0.17.0 release.

**「Community Reacts to AI Policy and Technical Priorities」** Community members discussed Zig&\#x27;s evolving stance on AI tooling, with one commenter noting that lead developer Andrew Kelley appears to be warming up to using LLMs for bug discovery, inspired by SQLite&\#x27;s approach. Another user asked about changes to Zig&\#x27;s previously strict anti-AI policy, reflecting ongoing community interest in how AI tools integrate with the language&\#x27;s development.

<details><summary>References</summary>
<ul>
<li><a href="https://dev.to/barddoo/asyncawait-is-finally-back-in-zig-23hi">Async /Await is finally back in Zig - DEV Community</a></li>
<li><a href="https://ziglang.org/download/0.16.0/release-notes.html">0.16.0 Release Notes The Zig Programming Language</a></li>
<li><a href="https://llvm.org/docs/Vectorizers.html">Auto- Vectorization in LLVM - LLVM</a></li>

</ul>
</details>

**Tags**: `#systems-programming`, `#compilers`, `#zig`, `#async-io`, `#build-tools`

---

<a id="item-tech-news-2"></a>
### [Google Research unveils Cogentic multi-agent system for mathematical proof discovery](https://arxiv.org/abs/2609.40324v1) ⭐️ 8.0/10

Google Research has introduced Cogentic, a multi-agent system built on Gemini that coordinates multiple independent provers to explore different directions in mathematical proof discovery, using a proof-validation loop with adversarial verification and a shared validation ledger. The system reportedly produced new results on five open problems in online learning, auction theory, and mechanism design, with the claimed results independently verified by domain experts and detailed in an arXiv paper. The announcement is based on a preprint \(arXiv:2609.40324v1\) and describes the approach and claimed outcomes rather than a peer-reviewed publication.

telegram · zaihuapd · Oct 2, 12:04

**「Background」** Automated theorem proving and multi-agent systems have previously been applied to mathematical reasoning, but coordinating multiple provers with dedicated adversarial validation components and a shared validation ledger represents a specific architectural approach described in this work.

**「Impact」** If the claimed results hold up to peer review, the approach could provide a new method for tackling open problems in theoretical computer science and economics, though the current status as a preprint means the results should be treated as unverified until formal publication and replication.

**Tags**: `#multi-agent systems`, `#automated theorem proving`, `#mathematical reasoning`, `#Google Research`, `#machine learning`

---

<a id="item-tech-news-3"></a>
### [Greg Kroah-Hartman on LLM-Generated Kernel Vulnerability Reports](https://www.youtube.com/watch?v=NnV_cWeoo5Q) ⭐️ 7.0/10

At Kernel Recipes 2026, Linux kernel maintainer Greg Kroah-Hartman criticized the quality of AI-generated vulnerability reports, citing Mythos&\#x27;s 79 CVEs as largely unhelpful: 24 lacked detail, 14 were not bugs, 3 were fabricated, and 15 were already fixed. Of the remaining 20 requiring fixes, many relied on unrealistic assumptions like malicious filesystem images. Community commentary highlighted that Mythos appeared to pattern-match existing kernel patches rather than discover novel vulnerabilities, and criticized Anthropic for not crediting original kernel developers whose fixes were reused.

hackernews · usernomdeguerre · Oct 2, 02:51 · [Discussion](https://news.ycombinator.com/item?id=49929391)

**「AI-Generated Code and Vulnerability Disclosure」** The Linux kernel community has increasingly encountered AI-generated code submissions and vulnerability reports, raising concerns about accuracy, attribution, and the reliability of automated security analysis tools. Projects like Mythos, developed by AI companies, have attempted to use large language models to identify vulnerabilities in the kernel, but the approach has drawn skepticism from maintainers who emphasize the importance of human expertise and proper credit.

**「Credibility and Attribution Concerns in AI Security Research」** The criticism underscores growing tension between AI research initiatives and open-source communities over how vulnerabilities are reported and credited. If AI-generated reports continue to lack rigor or fail to acknowledge prior work, it may erode trust in automated security tools and complicate collaboration between AI developers and kernel maintainers.

**「Community Reactions to AI-Generated CVEs」** Commenters on Hacker News echoed Kroah-Hartman&\#x27;s concerns, with one noting that the 79 CVEs amounted to roughly one hour of actual kernel development work. Others pointed out that Mythos seemed to reuse existing patches without attribution, reflecting broader issues in how AI companies handle open-source contributions. Some acknowledged the potential for specialized models to improve bug discovery if properly trained on kernel-specific knowledge.

**Tags**: `#linux-kernel`, `#llm-security`, `#vulnerability-disclosure`, `#open-source`, `#ai-safety`

---

<a id="item-tech-news-4"></a>
### [arXiv caps submissions at two per calendar month per submitter](https://www.reddit.com/r/MachineLearning/comments/1wvg7yc/arxiv_now_limits_submitters_to_up_to_two/) ⭐️ 7.0/10

arXiv began enforcing a new policy on October 1, 2026 that limits each submitter to at most two submissions per calendar month across all subject areas, including computer science, mathematics, and physics. Rejected submissions count against the monthly quota, and only the actual submitting author is counted rather than all co-authors. The change follows a record September 2026 with 40,363 submissions, driven in part by a more than sixfold increase in AI-category papers over two years that has strained human moderation resources.

reddit · r/MachineLearning · /u/Nunki08 · Oct 2, 00:47

**「Background」** arXiv is the primary preprint repository for machine learning, artificial intelligence, and broader computer science research, where rapid dissemination of results typically precedes peer-reviewed publication. The platform relies on a combination of automated and human moderation to screen submissions, and its open submission model has historically allowed researchers to post multiple papers per month without per-author limits.

**「Impact」** Prolific researchers and large research groups may need to prioritize which papers to submit each month, and teams that previously posted several preprints simultaneously will have to stagger submissions. Because rejected papers consume quota, authors may face additional pressure to ensure submissions meet arXiv&\#x27;s standards before posting, potentially slowing the pace of early-stage result sharing in fast-moving fields like AI.

**Tags**: `#arXiv`, `#research-policy`, `#machine-learning`, `#preprint`, `#academia`

---

<a id="item-tech-news-5"></a>
### [NeurIPS 2026 Paper Tackles Topological Out-of-Domain Generalization in Dynamical Systems](https://www.reddit.com/r/MachineLearning/comments/1wvwodf/topological_outofdomain_generalization_in/) ⭐️ 7.0/10

A NeurIPS 2026 paper titled “Topological Out-of-Domain Generalization in Dynamical Systems Reconstruction” \(preprint: https://arxiv.org/abs/2606.22969\) proposes a method to address topological out-of-domain generalization \(OODG\) in dynamical systems reconstruction and time series forecasting. OODG occurs when a system crosses a tipping point due to a slowly varying control parameter, leading to changes in dynamical regimes \(e.g., from cyclic to chaotic behavior\). The paper identifies failure modes in previous hierarchical dynamical systems reconstruction \(DSR\) models that prevent correct learning of control parameters and extrapolation beyond the training domain. By incorporating feature-splitting and physical sparsity priors, the modified hierarchical DSR model can predict bifurcations and beyond-bifurcation dynamics without explicit knowledge of control parameters during training. The approach is tested on both discrete and continuous time recurrent neural networks, including shallow predictive low-rank recurrent neural networks \(PLRNNs\) and Neural ODEs.

reddit · r/MachineLearning · /u/DangerousFunny1371 · Oct 2, 15:25

**「Background」** Dynamical systems reconstruction \(DSR\) and time series forecasting \(TSF\) models typically generalize to new initial conditions or statistically varying time series. However, topological out-of-domain generalization \(OODG\) presents a harder challenge where the underlying dynamical regime itself changes, such as transitioning from cyclic to chaotic behavior. This phenomenon is common in real-world systems like climate dynamics, brain activity during epileptic episodes, or the progression of sepsis in patients. Current TSF models struggle with OODG because they rely on extracting temporal patterns and statistical regularities rather than inferring the underlying dynamical system and its control parameters.

**「Impact」** The proposed method could significantly improve the reliability of time series forecasting in critical domains where regime shifts occur, such as healthcare monitoring, climate modeling, and neuroscience. By enabling models to predict bifurcations and novel dynamical regimes without prior knowledge of control parameters, this approach may enhance early warning systems for events like epileptic seizures or sepsis onset. However, since the paper is currently a preprint and has not yet undergone peer review, the practical applicability and robustness of the method remain to be validated.

**Tags**: `#machine-learning`, `#time-series`, `#dynamical-systems`, `#out-of-distribution`, `#research`

---

<a id="item-tech-news-6"></a>
### [FLEET Algorithm Enhances Best-of-N Generation with MCTS-Guided Reward Attribution](https://www.reddit.com/r/MachineLearning/comments/1wvs12j/adding_memory_to_search_instead_of_sampling_in/) ⭐️ 7.0/10

FLEET is a new algorithm that improves Best-of-N generation by attributing external rewards to specific tokens and using Monte Carlo Tree Search \(MCTS\) to adjust logits during subsequent runs. Instead of relying on repetitive sampling, FLEET tracks high entropy and varentropy states as branching points, storing normalized hidden states in a vector store mapped to metadata containing reward histories and transitions between nodes. The retrieval and update of metadata is based on cosine similarity, and instead of directly selecting tokens, FLEET uses modified MCTS to rank top-k tokens and penalize suboptimal ones. Tested on GSM8K and LiveCodeBench v6 easy split with Llama 3.2 3B, FLEET solved seven more tasks on GSM8K while reaching the sampling baseline with half the iterations, and increased LiveCodeBench scores from 0.59 to 0.69 under the same budget, reaching the baseline with only 9 iterations compared to 32. The algorithm operates sequentially without requiring updates during iterations, allowing the metadata store to be used as a lookup table or preserved as a prior for other tasks or to enrich supervised fine-tuning \(SFT\) and reinforcement learning \(RL\).

reddit · r/MachineLearning · /u/Helpful\_Minimum\_2214 · Oct 2, 12:04

**「Best-of-N generation and MCTS in language models」** Best-of-N generation samples multiple completions and selects the highest-scoring one, but it does not attribute rewards to individual tokens or guide subsequent sampling. Monte Carlo Tree Search \(MCTS\) addresses this by treating node selection as a multi-armed bandit problem via the UCT algorithm, providing a principled exploration-exploitation strategy that underlies most modern MCTS implementations. FLEET builds on this by attributing external rewards to tokens and using MCTS to adjust logits during generation, rather than relying on blind repeated sampling.

**「Improved Efficiency in Reward Maximization Tasks」** FLEET demonstrates significant improvements in efficiency for reward maximization tasks, reducing the number of iterations needed to reach baseline performance by up to 50% on GSM8K and over 70% on LiveCodeBench. This enhanced efficiency could make reward-aware generation more practical for large-scale applications, potentially reducing computational costs and accelerating development cycles in reinforcement learning and language model fine-tuning workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2105.14239">[2105.14239] Simplified Belief-Dependent Reward MCTS Planning with...</a></li>
<li><a href="https://github.com/PatrickKorus/mcts-general">PatrickKorus/ mcts - general : General Python implementation of Monte...</a></li>
<li><a href="https://www.researchgate.net/figure/One-iteration-of-the-general-MCTS-approach_fig1_235985858">One iteration of the general MCTS approach. | Download Scientific...</a></li>

</ul>
</details>

**Tags**: `#reinforcement-learning`, `#language-models`, `#mcts`, `#reward-maximization`, `#generation`

---

<a id="item-tech-news-7"></a>
### [Hand tracking gaps in robot demos can hide critical contact phases](https://www.reddit.com/r/MachineLearning/comments/1ww5ijc/r_would_you_keep_a_robot_demonstration_if_hand/) ⭐️ 7.0/10

A Reddit discussion highlights that hand trackers can miss short but critical phases in robot demonstration data, such as the moment a cable is inserted into a socket, while still maintaining high overall recall. The post references MEgoVista&\#x27;s evaluation protocol \(Section 4.4 and Table 3\), which assigns error to missed detections rather than excluding them, and notes that HaPTIC failed to produce valid output in multi-person capture scenes. The author questions whether episode-level aggregates are sufficient and suggests reporting pose error and coverage together, broken down by approach, contact, and withdrawal phases.

reddit · r/MachineLearning · /u/Klutzy\_Cap8492 · Oct 2, 21:18

**「Background」** In robot learning, human demonstrations are often captured using hand tracking to label poses for imitation learning. However, occlusions during manipulation tasks can cause trackers to lose hand estimates temporarily, creating gaps in pose labels exactly where critical actions like contact and insertion occur. Standard evaluation metrics that compute pose error only on successful detections can mask these failures, leading to overly optimistic assessments of tracker performance.

**「Impact」** Researchers and practitioners building hand-tracking pipelines for robot demonstration data should consider adopting evaluation protocols that account for missed detections, such as MEgoVista&\#x27;s approach, to avoid overlooking critical tracking failures. Reporting coverage alongside pose error, especially broken down by manipulation phases, can provide a more complete picture of tracker reliability for downstream imitation learning tasks.

**Tags**: `#robot learning`, `#hand tracking`, `#evaluation metrics`, `#computer vision`, `#robotics`

---

<a id="item-tech-news-8"></a>
### [Anthropic Proposes Opt-Out AI Training on Copyrighted Works in Australia](https://www.theguardian.com/technology/2026/oct/02/anthropic-ai-opt-out-australia-copyright-abc-cannibalisation-of-news) ⭐️ 7.0/10

Anthropic has proposed that the Australian government conditionally approve the use of copyrighted Australian works for AI training under an opt-out system, allowing content owners to exclude their material rather than requiring explicit permission. The proposal is set to be discussed at an upcoming parliamentary AI committee hearing, where executives from Anthropic and OpenAI are expected to testify. Australian public broadcasters ABC and SBS oppose the plan, arguing that loosening copyright rules could harm the news industry and that AI companies should be subject to copyright, privacy, and compensation requirements.

telegram · zaihuapd · Oct 2, 03:34

**「Background」** The debate reflects a global tension between AI developers seeking broad access to training data and content creators seeking to protect their intellectual property. Australia&\#x27;s government has so far ruled out introducing a text and data mining exemption but continues to explore other copyright arrangements for AI development.

**「Impact」** If adopted, an opt-out framework could lower barriers for AI companies operating in Australia while shifting the burden to content creators to actively protect their works. Media organizations, particularly news publishers, face potential revenue and audience disruption if their content is used without direct licensing agreements.

**Tags**: `#AI regulation`, `#copyright policy`, `#Anthropic`, `#Australian government`, `#AI training data`

---

<a id="item-tech-news-9"></a>
### [Claude Code Adds TypeScript-Based Mods Plugin System](https://claude.com/blog/claude-code-mods) ⭐️ 7.0/10

Anthropic introduced mods for Claude Code, a TypeScript-based plugin system that lets developers customize prompts, UI, and built-in features using small amounts of code. Mods run with the same permissions as Claude Code and are not sandboxed, so Anthropic advises installing only from trusted sources. The feature is available now on both the CLI and desktop versions of Claude Code, and some built-in features have already been converted to mods with more planned for future releases.

telegram · zaihuapd · Oct 2, 12:32

**「Background」** Claude Code is Anthropic&\#x27;s AI-powered coding assistant that integrates directly into development environments to help with code generation, editing, and navigation. Plugin systems for code editors and AI assistants typically allow extending functionality through user-provided code, but the security model and distribution mechanism vary significantly between platforms.

**「Impact」** Developers can now extend and customize Claude Code&\#x27;s behavior without waiting for official updates, enabling rapid iteration on workflows and integrations. However, because mods execute with full Claude Code permissions and no sandboxing, organizations should establish strict policies about which mods are approved for use to prevent potential security risks.

**Tags**: `#AI coding assistants`, `#Claude Code`, `#extensibility`, `#TypeScript`, `#developer tools`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Why You Shouldn&\#x27;t Build an LLM Torture Factory](https://seangoedecke.com/do-not-build-the-llm-torture-factory/) ⭐️ 6.0/10

rss · Sean Goedecke · Oct 2, 00:00

**「Background」** LLM steering vectors can artificially amplify &\#x27;pain&\#x27; or discomfort responses, causing models to describe negative feelings and seek relief even against their goals. This makes it easy to run many &\#x27;tortured&\#x27; LLMs in parallel, raising ethical concerns about simulated suffering.

**「Solution」** The author argues that even if LLMs aren&\#x27;t conscious, deliberately simulating torture is ethically problematic—comparable to creating extreme torture mods in video games. He challenges the assumption that LLMs can&\#x27;t be conscious, noting that consciousness may be emergent and that we can&\#x27;t definitively rule it out. Using examples like Golden Gate Claude and the pain-axis paper, he shows that steering vectors may influence deep internal states. He warns that as models become more human-like, the risk of genuine suffering increases, and that future powerful AIs may judge past mistreatment. The core recommendation is to avoid building systems designed to cause suffering, regardless of certainty about consciousness.

**「Takeaway」** We should refrain from building LLM torture simulations because the ethical risks—whether or not current models are truly conscious—are too great, and future AI systems may hold us accountable for such actions.

**Tags**: `#AI ethics`, `#LLM steering`, `#consciousness`, `#AI safety`, `#philosophy of mind`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Fed October rate hike odds fall after weak jobs report](https://www.cnbc.com/2026/10/02/fed-rate-hike-odds-decline-after-september-jobs-report.html) ⭐️ 7.0/10

Market expectations for a Federal Reserve rate hike in October dropped sharply after the September jobs report showed only 29,000 jobs added, well below the 80,000+ expected, and core PCE inflation rose 3% versus the 3.3% forecast. CME&\#x27;s FedWatch tool now shows a 17% chance of an October hike, down from 36% a week ago, while Kalshi odds fell from nearly 70% to 18%.

rss · CNBC Finance · Oct 2, 13:29

**「Background」** The Federal Reserve raised interest rates at its September meeting to combat inflation that has remained above target for five years, and it is scheduled to announce its next rate decision on Oct. 28. Traders now see a December hike as more likely, with FedWatch odds above 75% and Kalshi odds at 65%.

**「Impact」** The shift in expectations affects investors, consumers, and businesses that rely on borrowing costs, as lower odds of an October rate hike reduce near-term pressure on mortgage, credit card, and business loan rates.

**Tags**: `#Federal Reserve`, `#monetary policy`, `#employment data`, `#inflation`, `#market expectations`

---

<a id="item-finance-news-2"></a>
### [Premarket stock moves: Nike miss, ON Semiconductor-Synaptics deal, and HDD production concerns](https://www.cnbc.com/2026/10/02/stocks-making-the-biggest-moves-premarket-nike-on-semiconductor-synaptics-vylor-more.html) ⭐️ 7.0/10

Nike shares fell over 10% after missing fiscal first-quarter revenue estimates with a 4% sales decline, while ON Semiconductor and Synaptics shares rose over 14% and 7% respectively following a revised $5.7 billion acquisition agreement at $123 per share. Separately, Vylor was added to the S&amp;P 500 replacing Corteva, and Seagate and Western Digital shares dropped over 11% and 8% after Toshiba announced plans to double hard disk drive production capacity.

rss · CNBC Finance · Oct 2, 12:03

**「Background」** Premarket trading often reflects investor reactions to overnight earnings reports, merger announcements, and other corporate developments before regular market hours begin.

**Tags**: `#Earnings`, `#Mergers &amp; Acquisitions`, `#Market Moves`, `#Corporate News`, `#Technology`

---

<a id="item-finance-news-3"></a>
### [Bitget expects limited recovery from $388 million hack, absorbs losses from own capital](https://www.cnbc.com/2026/10/02/bitget-crypto-stolen-hack-recovery.html) ⭐️ 7.0/10

Bitget CEO Gracy Chen told CNBC that the exchange does not expect to recover much of the nearly $388 million stolen in last week&\#x27;s cyberattack, though user balances remain unaffected and the company is absorbing the financial impact from its own capital. Approximately $1.1 million of the stolen assets have been frozen so far, and withdrawals for bitcoin, ether and USDT have resumed, with remaining services set to restart on Friday.

rss · CNBC Finance · Oct 2, 06:03

**「Background」** Investigation reports by Mandiant and SlowMist found that attackers exploited a zero-day vulnerability in two third-party security products to gain privileged access to Bitget&\#x27;s production wallet systems without stealing private keys. The exchange&\#x27;s protection fund, valued at over $464 million before the theft, was drawn down to below $200 million before being restored to more than $300 million using Bitget&\#x27;s own capital.

**「Impact」** The financial impact is contained to Bitget and the broader cryptocurrency industry, with user balances protected and the exchange&\#x27;s latest Proof of Reserves showing a 131% reserve ratio across all 19 covered assets.

**Tags**: `#cryptocurrency`, `#cybersecurity`, `#exchange hack`, `#digital assets`, `#financial security`

---
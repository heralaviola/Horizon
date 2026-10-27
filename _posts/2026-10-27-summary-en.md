---
layout: default
title: "Horizon Summary: 2026-10-27 (EN)"
date: 2026-10-27
lang: en
---

> From 45 items, 9 important content pieces were selected

---

**Tools Update**
1. [uv 0.13.6: Enhancements, New Python Versions, and Preview Features](#item-tools-update-1) ⭐️ 5.0/10

**Technology News**
1. [Preprint Claims Disproof of Exponential Time Hypothesis](#item-tech-news-1) ⭐️ 9.0/10
2. [Anthropic S-1 Reveals $114B+ Cloud Commitments and Revenue Growth Strategy](#item-tech-news-2) ⭐️ 9.0/10
3. [Deepity: C++/CUDA predictive coding library beats JAX and ngc-learn on MNIST](#item-tech-news-3) ⭐️ 7.0/10
4. [PBT doesn&\#x27;t speed up grokking but can escape dead zones](#item-tech-news-4) ⭐️ 7.0/10
5. [Northwestern Traps Single Positron for Months in Quantum Cyclotron](#item-tech-news-5) ⭐️ 7.0/10
6. [Apple unveils new iPad mini with A20 Pro chip and 8.5-inch OLED display](#item-tech-news-6) ⭐️ 7.0/10
7. [Anthropic IPO filing reveals 5-7% revenue from policy-violating users](#item-tech-news-7) ⭐️ 7.0/10

**Financial News**
1. [Anthropic files for Nasdaq IPO under ticker ANT](#item-finance-news-1) ⭐️ 8.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [uv 0.13.6: Enhancements, New Python Versions, and Preview Features](https://github.com/astral-sh/uv/releases/tag/0.13.6) ⭐️ 5.0/10

uv 0.13.6 is a minor release that adds enhancements to recursion depth handling and project initialization guidance, introduces new CPython versions \(3.11.18, 3.12.16, 3.13.18, 3.14.10, 3.15.2\), and includes preview features for wheel variant selection and workspace metadata. The release also delivers performance improvements and bug fixes, with no breaking changes.

github · astral-releases-bot\[bot\] · Oct 27, 00:47

**「Changes」** \#\#\# Enhancements
\- Accept an empty \`UV\_RUN\_RECURSION\_DEPTH\` as zero and report invalid values consistently \(\[\#22814\]\(https://github.com/astral-sh/uv/pull/22814\)\)
\- Explain how to add project metadata when \`uv init\` finds a \`pyproject.toml\` without a \`\[project\]\` table \(\[\#22916\]\(https://github.com/astral-sh/uv/pull/22916\)\)

\#\#\# Python
\- Add CPython 3.11.18, 3.12.16, 3.13.18, 3.14.10, and 3.15.2 \(\[\#22938\]\(https://github.com/astral-sh/uv/pull/22938\)\)

\#\#\# Preview Features
\- Detect NVIDIA GPU capabilities when selecting compatible wheel variants with \`wheel-variants\` \(\[\#22690\]\(https://github.com/astral-sh/uv/pull/22690\)\)
\- Nest each module&\#x27;s owners in an object in \`uv workspace metadata\` output \(\[\#22638\]\(https://github.com/astral-sh/uv/pull/22638\)\)
\- Report the unsupported properties required by an incompatible wheel variant \(\[\#22719\]\(https://github.com/astral-sh/uv/pull/22719\)\)

\#\#\# Performance
\- Reduce peak memory use when resolving large workspaces \(\[\#22860\]\(https://github.com/astral-sh/uv/pull/22860\), \[\#22863\]\(https://github.com/astral-sh/uv/pull/22863\), \[\#22864\]\(https://github.com/astral-sh/uv/pull/22864\), \[\#22866\]\(https://github.com/astral-sh/uv/pull/22866\), \[\#22870\]\(https://github.com/astral-sh/uv/pull/22870\)\)
\- Reduce peak memory use when locking or upgrading large projects \(\[\#22833\]\(https://github.com/astral-sh/uv/pull/22833\), \[\#22834\]\(https://github.com/astral-sh/uv/pull/22834\)\)
\- Speed up redirected output from \`uv export\` and \`uv pip compile\` \(\[\#22840\]\(https://github.com/astral-sh/uv/pull/22840\)\)
\- Reuse cached or active environments when running PEP 723 scripts without dependencies \(\[\#21458\]\(https://github.com/astral-sh/uv/pull/21458\)\)
\- Reduce parsing overhead for build dependency and build backend settings \(\[\#22848\]\(https://github.com/astral-sh/uv/pull/22848\), \[\#22871\]\(https://github.com/astral-sh/uv/pull/22871\), \[\#22879\]\(https://github.com/astral-sh/uv/pull/22879\), \[\#22884\]\(https://github.com/astral-sh/uv/pull/22884\)\)
\- Reduce parsing overhead for project sources and workspace references \(\[\#22880\]\(https://github.com/astral-sh/uv/pull/22880\), \[\#22883\]\(https://github.com/astral-sh/uv/pull/22883\)\)
\- Reduce parsing overhead for cache, exclusion, cutoff, and preview settings \(\[\#22876\]\(https://github.com/astral-sh/uv/pull/22876\), \[\#22877\]\(https://github.com/astral-sh/uv/pull/22877\), \[\#22878\]\(https://github.com/astral-sh/uv/pull/22878\), \[\#22887\]\(https://github.com/astral-sh/uv/pull/22887\)\)
\- Reduce PyPI metadata parsing overhead \(\[\#22874\]\(https://github.com/astral-sh/uv/pull/22874\), \[\#22875\]\(https://github.com/astral-sh/uv/pull/22875\)\)
\- Speed up parsing tool receipt requirements \(\[\#22885\]\(https://github.com/astral-sh/uv/pull/22885\)\)

\#\#\# Bug Fixes
\- Prevent \`uv run --active --script\` and \`uv sync --active --script\` from deleting non-virtual-environment directories \(\[\#21464\]\(https://github.com/astral-sh/uv/pull/21464\)\)
\- Use \`AMD64\` for \`platform\_machine\` when resolving for x86-64 Windows \(\[\#22935\]\(https://github.com/astral-sh/uv/pull/22935\)\)
\- Preserve free-threaded and other non-default variants in \`uv python upgrade\` \(\[\#22836\]\(https://github.com/astral-sh/uv/pull/22836\)\)
\- Allow \`uv init --no-package\` and \`uv init --script\` when \`UV\_INIT\_BUILD\_BACKEND\` is set \(\[\#22907\]\(https://github.com/astral-sh/uv/pull/22907\)\)
\- Prevent panics when rendering containment markers with local versions \(\[\#22815\]\(https://github.com/astral-sh/uv/pull/22815\)\)

\#\#\# Documentation
\- Update the Docker guide and reproduction examples to use uv 0.13.5 \(\[\#22867\]\(https://github.com/astral-sh/uv/pull/22867\)\)

**「Impact」** This release is low-risk and suitable for most users to upgrade without action. Users working with large workspaces or projects will benefit from reduced memory usage and faster parsing during resolution, locking, and export operations. Those using preview features should note the new NVIDIA GPU detection for wheel variants and the updated \`uv workspace metadata\` output format. The addition of new CPython versions allows users to target the latest patch releases. No breaking changes or migration steps are required.

**Tags**: `#enhancements`, `#python-versions`, `#preview-features`, `#performance`

---

## Technology News

<a id="item-tech-news-1"></a>
### [Preprint Claims Disproof of Exponential Time Hypothesis](https://github.com/openai/math/blob/main/preprints/The-Exponential-Time-Hypothesis-is-False-October-25-2026/paper.pdf) ⭐️ 9.0/10

A preprint hosted on OpenAI&\#x27;s GitHub repository claims to disprove the Exponential Time Hypothesis \(ETH\), a central conjecture in computational complexity theory that posits certain NP-complete problems cannot be solved in subexponential time. The paper, dated October 25, 2026, asserts that 3SAT can be solved in time 2^o\(n\), where n is the number of variables, which would contradict ETH. However, the authors explicitly note that this does not imply NP admits subexponential-time algorithms in general, since 2^o\(n\) bounds do not transfer under standard polynomial-time reductions. The claim remains unverified and has not undergone peer review, drawing significant attention and skepticism from the theoretical computer science community.

hackernews · vok · Oct 26, 21:59 · [Discussion](https://news.ycombinator.com/item?id=50251661)

**「Background: The Exponential Time Hypothesis」** The Exponential Time Hypothesis \(ETH\) is a foundational conjecture in computational complexity theory stating that 3-SAT cannot be solved in subexponential time, specifically that there is no algorithm solving 3-SAT in time 2^o\(n\) where n is the number of variables. ETH is widely used to establish conditional lower bounds for numerous computational problems, meaning that disproving it would invalidate many hardness results across fields including algorithm design, cryptography, and hardness of approximation. A related conjecture, the Strong Exponential Time Hypothesis \(SETH\), has been used to prove that self-attention mechanisms in neural networks inherently require quadratic time complexity in input length, as established in a 2022 paper that showed sub-quadratic self-attention would contradict SETH.

**「Impact」** If verified, the result would undermine a foundational assumption used to prove conditional lower bounds for hundreds of problems in complexity theory, algorithm design, and hardness of approximation, potentially reshaping research directions in theoretical computer science. However, due to the lack of peer review and the extraordinary nature of the claim, practitioners and researchers are advised to treat it as speculative until independently confirmed.

**「Community Discussion」** Commenters on Hacker News expressed cautious interest, with some noting the rarity of complexity class separations and others questioning whether the technique could yield practical improvements in SAT solving or implications for models like self-attention, whose quadratic lower bounds were previously tied to SETH. Several emphasized the need for rigorous verification before accepting the result.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/openai/math/blob/main/preprints/The-Exponential-Time-Hypothesis-is-False-October-25-2026/paper.pdf">math / preprints /The- Exponential - Time - Hypothesis -is...</a></li>
<li><a href="https://arxiv.org/abs/2209.04881">[2209.04881] On The Computational Complexity of Self-Attention On The Computational Complexity of Self-Attention arXiv:2209.04881v1 [cs.LG] 11 Sep 2022 On The Computational Complexity of Self-Attention | alphaXiv On The Computational Complexity of Self-Attention Self-Attention: Complexity Analysis On The Computational Complexity of Self-Attention</a></li>

</ul>
</details>

**Tags**: `#computational-complexity`, `#algorithms`, `#theoretical-computer-science`, `#eth`, `#sat-solving`

---

<a id="item-tech-news-2"></a>
### [Anthropic S-1 Reveals $114B+ Cloud Commitments and Revenue Growth Strategy](https://www.sec.gov/Archives/edgar/data/2130357/000162828026067168/anthropicpbc-sx1.htm) ⭐️ 9.0/10

Anthropic&\#x27;s S-1 filing reveals over $114 billion in committed cloud contracts, including $114 billion to Google Cloud, $110 billion to AWS, $161 billion to Broadcom, and $120 billion to SpaceX. The filing indicates the company generated $50 billion in revenue and aims to scale to $500 billion, with community analysis suggesting much of recent growth stems from AI coding adoption, particularly Claude Code. The document also highlights dependencies on major cloud providers and potential risks from open-source models, especially those developed by Chinese labs.

hackernews · SiNTEx · Oct 26, 13:04 · [Discussion](https://news.ycombinator.com/item?id=50242939)

**「Anthropic&\#x27;s S-1 IPO Filing」** Anthropic filed a preliminary S-1 registration statement with the SEC to prepare for an initial public offering, marking the first time the AI company has publicly disclosed detailed financial and operational information. The filing reveals massive long-term cloud and infrastructure commitments totaling over $500 billion across providers including Google, Amazon, Microsoft, and Broadcom, alongside revenue figures and risk factors such as dependence on third-party compute capacity and competition from open-source models. This disclosure provides rare visibility into the economics and capital intensity of frontier AI development.

**「Financial Strategy Hinges on Sustained AI Demand and Infrastructure Scaling」** Anthropic&\#x27;s aggressive cloud commitments signal a high-stakes bet on continued AI demand, particularly in enterprise coding applications. If adoption rates slow, the company&\#x27;s substantial fixed-cost infrastructure investments could strain profitability. The reliance on a small number of cloud providers also introduces supply chain and pricing risks, while open-source alternatives pose a competitive threat to long-term revenue growth.

**「Community Questions Demand Sustainability and Open-Source Risks」** Commenters on Hacker News expressed skepticism about the sustainability of Anthropic&\#x27;s growth projections, noting that rapid AI coding adoption may not continue at current rates. Some highlighted the company&\#x27;s strong Q2 performance and efficient compute payback periods, while others pointed to open-source models, particularly from Chinese labs, as an underappreciated risk to Anthropic&\#x27;s business model.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.yahoo.com/technology/ai/articles/anthropic-1-518-billion-commitment-165731037.html?fr=sycsrp_catchall">Anthropic’s S-1 Is Here. The $518 Billion Commitment Is the ...</a></li>
<li><a href="https://www.theinformation.com/articles/anthropics-s-1-takeaways-giant-compute-commitments-complex-lock-ups">Anthropic’s S-1 Takeaways: From Giant Compute Commitments to ...</a></li>
<li><a href="https://www.cnbc.com/2026/10/26/anthropic-ipo-live-updates-ai-s-1-filing.html">Anthropic IPO live updates: AI lab&#x27;s S-1 filing - CNBC</a></li>

</ul>
</details>

**Tags**: `#AI`, `#business`, `#cloud`, `#open-source`, `#infrastructure`

---

<a id="item-tech-news-3"></a>
### [Deepity: C++/CUDA predictive coding library beats JAX and ngc-learn on MNIST](https://www.reddit.com/r/MachineLearning/comments/1xg6sqa/deepity_a_handtuned_ccuda_predictive_coding/) ⭐️ 7.0/10

Deepity, a from-scratch C++20 predictive coding library with hand-tuned AVX2/AVX-512 SIMD kernels, OpenBLAS/MKL integration, and a CUDA backend \(cuBLAS + CUTLASS\), has been released as alpha 0.1.0a3 with Python bindings via nanobind \(pip install pydeepity\). On a matched 784-512-512-10 sigmoid network \(T=20 settling steps, batch 250, 100 epochs, AdamW\) on a 12th Gen i7-12700H laptop CPU, Deepity reached 98.21% accuracy in 487.5s, compared to jpc \(JAX\) at 97.55% in 531.4s and ngc-learn at 98% in 1707.7s, with a reference PyTorch backprop run at 97.51% in 627.8s. The CPU path is mature and benchmarked, while the CUDA backend builds and runs but is still being optimized for large-scale training and lacks validated CUDA-vs-CPU numbers.

reddit · r/MachineLearning · /u/Important-Home4431 · Oct 26, 19:34

**「Predictive coding as a backpropagation alternative」** Predictive coding networks \(PCNs\) differ from backpropagation by having each layer maintain a local belief about its state and compare it against a top-down prediction from the layer above, training via alternating &\#x27;settling&\#x27; \(local error reduction\) and weight updates that only use each layer&\#x27;s own error, avoiding the need for weight transposes or a stored backward graph. Deepity implements several PCN variants including classic settling, Direct Kolen-Pollack feedback, and a configurable &\#x27;kitchen sink&\#x27; network with optional µPC scaling, residual connections, incremental PC, error-based PC, and momentum settling.

**「Performance claims await independent validation」** Deepity&\#x27;s reported ~675-690 GFLOPS/s sustained performance and MNIST accuracy wins over JAX and ngc-learn are based on a single-machine CPU benchmark with raw logs in the repository, but as alpha software with no published paper or broader evaluation, the results require independent reproduction before being considered a proven improvement over established frameworks. The library may be valuable for researchers exploring predictive coding systems, but its CUDA backend is not yet ready for large-scale training and convolution uses im2col+cuBLAS rather than cuDNN.

**Tags**: `#predictive coding`, `#C++`, `#CUDA`, `#machine learning libraries`, `#benchmarks`

---

<a id="item-tech-news-4"></a>
### [PBT doesn&\#x27;t speed up grokking but can escape dead zones](https://www.reddit.com/r/MachineLearning/comments/1xfqhfc/pbt_doesnt_make_grokking_faster_but_it_can_escape/) ⭐️ 7.0/10

An empirical study of Population Based Training \(PBT\) on the modular addition grokking benchmark \(mod 97, 35% train split, small MLP, 20 members, 20k steps\) finds that PBT does not accelerate grokking compared to a fixed hyperparameter grid. The best fixed cell reached 95% validation accuracy in 317 ± 29 steps, while PBT took 2667 ± 2244 steps across all seeds, with the grid&\#x27;s corner already containing the optimal setting. However, when starting from a hyperparameter dead zone \(lr 1e-4 to 1e-3, wd 0.01 to 0.08\) where no fixed setting groks, fast PBT \(perturbing every 100 steps with ×0.5/×2\) escaped in 3/3 runs at about 6850 steps, versus 0/3 for both fixed settings and slow PBT. The winning PBT trajectory follows a reproducible path: learning rate drops to the floor, weight decay climbs to the ceiling, then learning rate rises. Ablations show a random donor still escapes \(later\), no-selection causes the population to lose grokking after achieving it, and replaying the winning lr/wd schedule without PBT on fresh inits reaches 95% in 55/60 cases, indicating the schedule—not weight copying—drives the result. The author concludes PBT is a rescue tool for bad hyperparameter ranges rather than a speed-up, with caveats of one task, one model, one split, and 3-10 seeds per test.

reddit · r/MachineLearning · /u/Virtual-Message-9739 · Oct 26, 07:48

**「Background」** Grokking refers to a phenomenon in neural network training where a model transitions from memorizing training data to generalizing, often marked by a sudden drop in validation loss after prolonged overfitting. Population Based Training \(PBT\) is a hyperparameter optimization method that maintains a population of models and periodically replaces poorly performing members with mutated versions of better-performing ones, allowing hyperparameters to adapt during training rather than being fixed at the start.

**「Impact」** For researchers and practitioners using PBT for hyperparameter optimization, this study suggests that PBT should not be expected to speed up training on tasks where good fixed hyperparameters are already known, but it can serve as a fallback mechanism to escape poorly chosen hyperparameter ranges where fixed settings fail entirely. The finding that the winning lr/wd schedule—not weight copying—drives the result implies that the adaptive schedule discovered by PBT is the key benefit, which may inform the design of learning rate and weight decay schedulers for similar tasks.

**Tags**: `#grokking`, `#population-based training`, `#hyperparameter optimization`, `#modular addition`, `#empirical ML`

---

<a id="item-tech-news-5"></a>
### [Northwestern Traps Single Positron for Months in Quantum Cyclotron](https://www.wired.com/story/scientists-trapped-an-antimatter-particle-for-months-to-study-its-secrets/) ⭐️ 7.0/10

Northwestern University researchers led by Gerald Gabrielse trapped a single positron in a quantum cyclotron for months at near-absolute-zero temperatures in a vacuum, using electromagnetic fields to confine the antimatter particle without destroying it and enabling repeated measurements. The apparatus is expected to improve antimatter measurement precision by roughly 30x, according to the American Physical Society. No unexpected differences between the positron and electron have been observed so far, but any future detection of differing magnetic field responses would require rewriting the laws governing matter-antimatter behavior.

telegram · zaihuapd · Oct 26, 06:06

**「Antimatter trapping and quantum cyclotrons」** Positron trapping in Penning-trap-like devices has long been a goal of antimatter physics, but earlier experiments typically held particles for seconds to minutes before loss or annihilation limited precision. The Northwestern team&\#x27;s advance lies in combining electromagnetic confinement with quantum control, creating a single-positron quantum cyclotron whose energy levels can be observed and manipulated like an artificial atom, enabling repeated, non-destructive measurements over months. This builds on decades of antimatter-trapping work, including CERN&\#x27;s ALPHA and GBAR experiments that trap antihydrogen, but extends precision measurement techniques to a single positron rather than composite antimatter atoms.

<details><summary>References</summary>
<ul>
<li><a href="https://www.eurekalert.org/news-releases/1147987">Scientists trap and tame a single particle of antimatter for months</a></li>
<li><a href="https://www.zmescience.com/science/news-science/positron-trapped-for-months/">Physicists Trapped a Single Antimatter Particle for Months .</a></li>
<li><a href="https://www.wired.com/story/scientists-trapped-an-antimatter-particle-for-months-to-study-its-secrets/">Scientists Trapped an Antimatter Particle for Months to... | WIRED</a></li>

</ul>
</details>

**Tags**: `#antimatter`, `#precision measurement`, `#quantum cyclotron`, `#fundamental physics`, `#particle trapping`

---

<a id="item-tech-news-6"></a>
### [Apple unveils new iPad mini with A20 Pro chip and 8.5-inch OLED display](https://www.apple.com/newsroom/2026/10/apple-gives-ipad-mini-its-biggest-update-ever/) ⭐️ 7.0/10

Apple announced a redesigned iPad mini featuring an 8.5-inch OLED display with 1200-nit peak brightness, the A20 Pro chip, and IP-rated water and dust resistance, with a body thickness of 5.4mm. The device is available in midnight and starlight colors, with the 128GB model starting at ¥5,499. Pre-orders begin on October 29 at 1:10 AM, with sales starting November 6.

telegram · zaihuapd · Oct 26, 13:05

**「iPad mini generational update」** The iPad mini line was last significantly updated in 2021 with the sixth-generation model, which introduced USB-C and a larger display but retained an LCD panel and the A15 Bionic chip. This new model represents the most substantial redesign of the mini form factor to date.

**「Performance and display upgrade for compact tablet users」** Users upgrading from older iPad mini models will see major improvements in display quality and performance, with the OLED panel offering better contrast and the A20 Pro chip providing faster processing for tasks like photo editing, gaming, and multitasking. The addition of water and dust resistance also makes the device more durable for on-the-go use.

**Tags**: `#hardware`, `#mobile-computing`, `#apple`, `#chipsets`

---

<a id="item-tech-news-7"></a>
### [Anthropic IPO filing reveals 5-7% revenue from policy-violating users](https://www.reuters.com/technology/artificial-intelligence/why-anthropic-is-turning-away-some-users-2026-10-22/) ⭐️ 7.0/10

Anthropic&\#x27;s IPO filing disclosed that revenue from users violating its usage policies or terms of service accounted for 5% to 7% of the company&\#x27;s total revenue in the first nine months of the year. The company has cut off access for some paid accounts, alleging that certain accounts linked to Chinese AI labs used the service to extract Claude outputs for training their own models, constituting unauthorized model distillation that raises intellectual property and national security concerns. Anthropic stated that enhanced defenses implemented in the third quarter significantly reduced this revenue, lowering distillation extraction by 90% to 99%, while proactively forgoing substantial income and paid traffic worth trillions of tokens and banning tens of thousands of related accounts.

telegram · zaihuapd · Oct 26, 16:43

**「Model distillation and AI governance context」** Model distillation refers to the practice of using outputs from a large language model to train a smaller, more efficient model, which can raise intellectual property and competitive concerns when done without authorization. Anthropic&\#x27;s policy enforcement actions reflect broader industry efforts to prevent misuse of AI services for competitive model development, particularly involving cross-border entities.

**「Revenue reduction and policy enforcement implications」** By forgoing 5% to 7% of its revenue and banning tens of thousands of accounts, Anthropic demonstrates a willingness to sacrifice short-term income to protect its intellectual property and comply with potential national security regulations, which may influence how other AI companies approach user monitoring and policy enforcement.

**Tags**: `#AI governance`, `#Anthropic`, `#model distillation`, `#IP law`, `#AI regulation`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Anthropic files for Nasdaq IPO under ticker ANT](https://www.cnbc.com/2026/10/26/anthropic-ipo-live-updates-ai-s-1-filing.html) ⭐️ 8.0/10

Anthropic has filed for a Nasdaq initial public offering under the ticker symbol ANT, with Morgan Stanley and Goldman Sachs leading the deal and a target listing in mid-November. The draft prospectus shows first-half revenue of $16.3 billion, up from $1.1 billion a year earlier, alongside a net loss of $80.7 billion that is largely driven by $72 billion in convertible debt and other financing instruments rather than core operations.

telegram · zaihuapd · Oct 26, 13:21

**「Background」** The filing marks a major capital-markets milestone for one of the leading artificial-intelligence companies, which has grown rapidly on the back of its Claude chatbot models.

**「Impact」** The offering, if completed, would give public-market investors a direct way to trade shares in a top-tier AI developer and could pressure other AI startups to pursue similar listings.

**Tags**: `#IPO`, `#Anthropic`, `#AI`, `#Nasdaq`, `#Financial Results`

---
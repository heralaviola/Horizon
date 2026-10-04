---
layout: default
title: "Horizon Summary: 2026-10-04 (EN)"
date: 2026-10-04
lang: en
---

> From 30 items, 10 important content pieces were selected

---

**Tools Update**
1. [pi v1.0.2: per-thinking-level sampling overrides](#item-tools-update-1) ⭐️ 5.0/10

**Technology News**
1. [DynaBase: Minimal One-Parameter Architecture for Zero-Shot Dynamical System Reconstruction](#item-tech-news-1) ⭐️ 8.0/10
2. [US White House Launches AI Task Force to Assess Risks Within 120 Days](#item-tech-news-2) ⭐️ 8.0/10
3. [Default Hard Budget Caps for Pay-Per-Use APIs](#item-tech-news-3) ⭐️ 7.0/10
4. [ARC-AGI-3 Kaggle leaderboard scores jump from 7% to 56%](#item-tech-news-4) ⭐️ 7.0/10
5. [Mirror-Suit Robot Dataset for CV Specular Reflection Benchmarking](#item-tech-news-5) ⭐️ 7.0/10
6. [Tianjin University unveils 3-gram non-invasive brain-computer interface](#item-tech-news-6) ⭐️ 7.0/10
7. [Google Releases VeriHarness Long-Task Verification Framework](#item-tech-news-7) ⭐️ 7.0/10

**Financial News**
1. [Sports Betting Becomes Norm for Gen Z, Raising Financial and Mental Health Concerns](#item-finance-news-1) ⭐️ 7.0/10
2. [China cracks down on fake &\#x27;transparent kitchen&\#x27; takeout vendors after CCTV exposé](#item-finance-news-2) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [pi v1.0.2: per-thinking-level sampling overrides](https://github.com/earendil-works/pi/releases/tag/v1.0.2) ⭐️ 5.0/10

The pi project released v1.0.2, adding a new \`samplingParamsByThinkingLevel\` field to \`models.json\` that lets users set per-thinking-level sampling parameters \(such as \`temperature\` and \`top\_p\`\) for OpenAI-compatible APIs. This is a shipped, non-breaking incremental feature enhancement to model configuration and sampling control.

github · github-actions\[bot\] · Oct 4, 00:56

**「Changes」** \- Added \`samplingParamsByThinkingLevel\` to \`models.json\` for per-thinking-level sampling parameter overrides \(e.g., \`temperature\`, \`top\_p\`\) on OpenAI-compatible APIs. See \[Configure sampling by thinking level\]\(https://github.com/earendil-works/pi/blob/v1.0.2/packages/coding-agent/docs/models.md\#configure-sampling-by-thinking-level\) \(\[\#9776\]\(https://github.com/earendil-works/pi/pull/9776\) by \[@mrexodia\]\(https://github.com/mrexodia\)\).

**「Impact」** This release is relevant to users of pi who leverage thinking levels on OpenAI-compatible APIs and want finer control over sampling parameters per thinking level. Upgrading is straightforward and requires no migration steps, since the new field is additive and optional. Users who do not use thinking levels or OpenAI-compatible APIs are unaffected.

**Tags**: `#sampling`, `#model-configuration`, `#openai-compatible`, `#thinking-levels`, `#incremental-feature`

---

## Technology News

<a id="item-tech-news-1"></a>
### [DynaBase: Minimal One-Parameter Architecture for Zero-Shot Dynamical System Reconstruction](https://www.reddit.com/r/MachineLearning/comments/1wxex8n/a_minimal_interpretable_architecture_for_zeroshot/) ⭐️ 8.0/10

A NeurIPS 2026 paper presents DynaBase, a minimal and interpretable architecture for zero-shot reconstruction of dynamical systems using a single-parameter piecewise affine map and a context selector. The piecewise affine map uses only one parameter α to control local contraction or divergence rates, while the context selector chooses the closest data point from the provided context signal to the current state of the map. With these two mechanisms, DynaBase can reproduce major dynamical regimes including fixed points \(α&lt;1\), limit cycles \(α=1\), and chaotic attractors \(α&gt;1\). The authors claim that this simple context-driven 1-parameter map outperforms most major time series and dynamical system foundation models, as well as custom-trained models, in both long-term statistics and short-term predictions, even in zero-shot mode. Training is described as extremely cheap, achievable either analytically in one step via linear regression on forward predictions or through 1-parameter grid search directly on reconstruction objectives.

reddit · r/MachineLearning · /u/DangerousFunny1371 · Oct 4, 12:49

**「Background」** Reconstructing dynamical systems from data is a long-standing problem in time-series modeling, where foundation models are typically large and opaque. Prior work has used piecewise affine maps and context-based selection to approximate system behavior, but these approaches often require many parameters or fail to preserve the correct dynamical regime. The arXiv preprint \(2607.14937\) and its HTML version \(tool-1-1, tool-1-2\) establish that DynaBase reduces this to a single-parameter piecewise affine map combined with a context selector, claiming zero-shot reproduction of fixed points, limit cycles, and chaotic attractors.

**「Implications for dynamical systems modeling」** DynaBase&\#x27;s claimed zero-shot performance against established time series foundation models like TimesFM and custom-trained models, if validated, would offer researchers a far simpler and more interpretable alternative for reconstructing dynamical systems without task-specific training. Its single-parameter design and one-step analytical training could lower the barrier for applying foundation-model techniques to scientific modeling, though the claims remain unverified beyond the preprint and Reddit summary.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2607.14937">A Minimal Interpretable Architecture for Zero-Shot Reconstruction of...</a></li>
<li><a href="https://www.alphaxiv.org/overview/2607.14937">A Minimal Interpretable Architecture for Zero-Shot Reconstruction of...</a></li>
<li><a href="https://github.com/google-research/timesfm">google-research/timesfm: TimesFM ( Time Series Foundation Model )...</a></li>

</ul>
</details>

**Tags**: `#dynamical systems`, `#zero-shot learning`, `#interpretable ML`, `#NeurIPS`, `#piecewise affine map`

---

<a id="item-tech-news-2"></a>
### [US White House Launches AI Task Force to Assess Risks Within 120 Days](https://www.wsj.com/tech/ai/new-ai-task-force-to-report-on-risks-of-technology-after-public-and-industry-concerns-b6308bef) ⭐️ 8.0/10

The White House has established a new AI task force called the &\#x27;Super Intelligence Force,&\#x27; led by National Intelligence Director Jay Clayton, to evaluate the risks posed by artificial intelligence and determine the federal government&\#x27;s responsibilities regarding the technology. The task force is required to deliver a risk assessment report within 120 days. Despite rising concerns about AI safety, the Trump administration has declined to introduce new regulations, instead favoring a voluntary framework that includes external security audits and stronger internal controls, while prioritizing maintaining a competitive edge over China in AI development.

telegram · zaihuapd · Oct 4, 02:37

**「Background」** The formation of the task force follows growing public and industry concerns about the rapid advancement and potential risks of artificial intelligence, particularly in areas such as data privacy, national security, and autonomous decision-making. The White House&\#x27;s approach reflects a balance between fostering innovation and addressing oversight, consistent with prior U.S. strategies that emphasize voluntary compliance over mandatory regulation.

**「Impact」** The task force&\#x27;s 120-day mandate may influence how U.S. AI companies operate, particularly those involved in high-risk applications, as the resulting report could shape future regulatory expectations. Organizations in the AI sector should monitor the findings closely, as they may affect compliance strategies and federal contracting opportunities, especially in defense and intelligence-related domains.

**Tags**: `#AI governance`, `#U.S. policy`, `#risk assessment`, `#White House`, `#technology regulation`

---

<a id="item-tech-news-3"></a>
### [Default Hard Budget Caps for Pay-Per-Use APIs](https://simonwillison.net/2026/Oct/3/default-hard-budget-caps/) ⭐️ 7.0/10

Simon Willison argues that pay-by-usage services and APIs should implement default hard budget caps, which automatically cut off service after a specified monthly spend, rather than relying on soft caps that only send warning emails. He emphasizes that autonomous coding agents and personal agents increase the risk of runaway costs from paid API calls, and that users should be able to opt out of these protections only through explicit, prominent action. Willison notes that AWS recently launched spending limits that pause projects when limits are reached, and Google Cloud introduced Spend Caps in July, suggesting this is becoming an industry trend.

rss · Simon Willison · Oct 3, 23:34

**「Rise of Autonomous Coding Agents」** The increasing adoption of autonomous coding agents and personal agents has lowered the barrier to deploying applications that interact with paid APIs, hosted services, and cloud infrastructure. These agents can generate and execute code that incurs costs for storage, compute, and API usage, often without continuous human oversight, creating new operational risks around unexpected billing.

**「Reduced Risk of Unexpected Cloud Bills」** Implementing default hard budget caps would protect developers and organizations from surprise bills caused by autonomous agents or misconfigured services, particularly on platforms like AWS where users have historically feared runaway costs. This safeguard would make cloud services safer for personal projects and reduce the financial risk associated with deploying agent-driven applications.

**Tags**: `#AI agents`, `#API economics`, `#software engineering`, `#cost control`, `#developer tools`

---

<a id="item-tech-news-4"></a>
### [ARC-AGI-3 Kaggle leaderboard scores jump from 7% to 56%](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/) ⭐️ 7.0/10

A Reddit post reports that top ARC-AGI-3 scores on Kaggle rose from 7% to 56% over the past 30 days, based on a leaderboard graphic. The post claims that small local models usable by Kagglers, running in a harness, have begun matching or exceeding average human performance on a benchmark designed to test human-like reasoning. No model names, versions, or methodology were provided, and the leaderboard image was described as slightly out-of-date.

reddit · r/MachineLearning · /u/we\_are\_mammals · Oct 4, 10:24 · [Discussion](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/)

**「ARC-AGI benchmark context」** ARC-AGI \(Abstraction and Reasoning Corpus\) is a benchmark created to evaluate human-like reasoning and generalization in AI systems, with the original version intended to be difficult for models while solvable by humans. ARC-AGI-3 is a later iteration of the benchmark, and Kaggle competitions restrict participants to smaller, locally runnable models rather than large cloud-based systems.

**「Benchmark progress signals reasoning gains」** If verified, the reported score increase would suggest that smaller, locally deployable models can achieve human-level performance on a reasoning benchmark previously thought to require larger systems, which could influence how organizations evaluate model capabilities and choose deployment strategies.

**Tags**: `#machine-learning`, `#benchmarks`, `#ARC-AGI`, `#Kaggle`, `#model-evaluation`

---

<a id="item-tech-news-5"></a>
### [Mirror-Suit Robot Dataset for CV Specular Reflection Benchmarking](https://www.reddit.com/r/MachineLearning/comments/1wx7jg6/here_are_some_pictures_of_a_robot_costume_wearing/) ⭐️ 7.0/10

A 425-image dataset of a robot costume wearing a faceted mirror suit has been released to benchmark computer vision and depth-estimation models against extreme specular reflections. The archive includes 100% proprietary uncompressed Camera-Master RAW files, high-resolution JPEGs, and SHA-256 forensic manifests, captured in high-contrast outdoor environments to trigger bounding-box dropouts and segmentation failures. The dataset was submitted by /u/5500kelvin on Reddit and is positioned as a stress-test resource rather than a peer-reviewed publication.

reddit · r/MachineLearning · /u/5500kelvin · Oct 4, 05:21

**「Specular Reflection Challenges in Computer Vision」** Specular reflections pose a known challenge for computer vision systems, as glossy or mirrored surfaces can cause severe degradation in object detection, segmentation, and depth estimation by creating false edges, occlusions, and textureless regions. This dataset targets that under-served edge case with a purpose-built mirror suit designed to maximize geometric reflections and glare under real-world lighting conditions.

**「Benchmarking Robustness in Spatial AI」** The dataset provides a standardized benchmark for evaluating the robustness of CV and depth-estimation models in scenarios involving extreme mirror-like reflections, which are common in robotics, autonomous systems, and industrial inspection. Its inclusion of forensic manifests and uncompressed RAW files supports reproducible research and high-fidelity model testing.

**Tags**: `#computer vision`, `#dataset`, `#depth estimation`, `#specular reflection`, `#benchmarking`

---

<a id="item-tech-news-6"></a>
### [Tianjin University unveils 3-gram non-invasive brain-computer interface](https://news.tju.edu.cn/info/1005/615029.htm) ⭐️ 7.0/10

Tianjin University&\#x27;s Brain-Computer Interaction and Human-Machine Fusion Haohan Laboratory announced the &quot;Divine Work·Sumeru·Brain Cube,&quot; a non-invasive brain-computer interface system weighing 3 grams and measuring 2 cubic centimeters, which the university claims is the world&\#x27;s smallest and lightest non-invasive BCI system. The device integrates EEG electrodes, circuits, a battery, and wireless transmission into a form factor small enough to be concealed among hair strands, targeting applications in medical, consumer, education, and special operations safety management. The announcement comes from a brief university news release with limited technical detail, so the broader significance and real-world impact remain unverified.

telegram · zaihuapd · Oct 4, 03:24

**「Non-invasive BCI miniaturization context」** Non-invasive brain-computer interfaces have historically relied on bulky EEG headsets that require conductive gel and large electrode arrays, limiting their use outside clinical or laboratory settings. Recent efforts have focused on integrating electrodes, circuitry, battery, and wireless transmission into a single compact unit that can be worn discreetly among the hair, as described in reporting of the Tianjin University system. The Shengong Xumi Brain Cube, announced by the university&\#x27;s Haihe Laboratory of Brain-Computer Interaction and Human-Machine Integration together with Shengong Diting \(Tianjin\) Technology, represents the latest step in this trend toward miniaturized, wearable EEG devices.

<details><summary>References</summary>
<ul>
<li><a href="https://insidebci.com/news/2026-10-04-tianjin-university-shengong-xumi-brain-cube-3-gram-non-invasive-bci-worker-safety/">Tianjin University releases a 3-gram brain-signal recorder ...</a></li>
<li><a href="https://neurotech.com/news/2026-10-04-tianjin-university-unveils-a-3-gram-non-invasive-bci-that-di">Tianjin University Unveils a 3-Gram Non-Invasive BCI That ...</a></li>
<li><a href="https://x.com/thePandaily/article/2106643345829245153">Tianjin University Lab Unveils 3-Gram Non-Invasive Brain ...</a></li>

</ul>
</details>

**Tags**: `#brain-computer interface`, `#biomedical engineering`, `#wearable technology`, `#hardware`, `#research`

---

<a id="item-tech-news-7"></a>
### [Google Releases VeriHarness Long-Task Verification Framework](https://arxiv.org/abs/2610.00972v1) ⭐️ 7.0/10

Google has released VeriHarness, a framework for verifying long-horizon tasks by using the same model that generated candidate results to perform verification. The model checks environmental evidence for divergent claims, actively challenges consensus claims, and then selects, revises, or rebuilds the final output. On five long-task benchmarks and two models, VeriHarness achieved the highest selection scores, improving average results by 6.2 points for Gemini 3.5 Flash and 6.4 points for Claude Opus 4.8, and the team has released approximately 26,000 rollouts.

telegram · zaihuapd · Oct 4, 13:32

**「Background」** Long-horizon task verification is a key challenge in AI reasoning, where models must maintain consistency and factual accuracy across extended multi-step processes. Prior approaches often relied on separate verification models or human feedback, making self-verification by the same generative model a notable methodological shift.

**「Impact」** For developers and researchers working on long-context or agentic AI systems, VeriHarness offers a reproducible method to improve output reliability without changing the underlying model architecture, though adoption depends on integration with existing pipelines and benchmark compatibility.

**Tags**: `#AI`, `#machine learning`, `#Google`, `#framework`, `#verification`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Sports Betting Becomes Norm for Gen Z, Raising Financial and Mental Health Concerns](https://www.cnbc.com/2026/10/04/gen-z-sports-betting-financial-and-mental-health-risks.html) ⭐️ 7.0/10

A survey by Betterment found that 66% of Gen Z investors participate in sports betting, while the Bank of America Institute reported that Gen Z accounted for nearly 50% of all online betting activity during the 2026 FIFA World Cup. Financial and mental health experts warn that treating sports betting as an investment poses significant risks, including lower savings and increased likelihood of harmful gambling behaviors.

rss · CNBC Finance · Oct 4, 12:57

**「Background」** Sports betting expanded rapidly after the 2018 U.S. Supreme Court ruling that allowed states to legalize sportsbooks, now available in 30 states. The rise of prediction markets offering sports-related event contracts in early 2025 further broadened access, including to users under 21, blurring the line between gambling and investing.

**「Impact」** Experts say the normalization of sports betting among Gen Z is linked to reduced savings and potential mental health issues, particularly among college students, prompting calls for campus counseling services to address gambling-related harm.

**Tags**: `#sports betting`, `#Gen Z`, `#financial health`, `#mental health`, `#consumer behavior`

---

<a id="item-finance-news-2"></a>
### [China cracks down on fake &\#x27;transparent kitchen&\#x27; takeout vendors after CCTV exposé](https://content-static.cctvnews.cctv.com/snow-book/index.html?toc_style_id=feeds_default&amp;amp;t=1791107500811&amp;amp;item_id=17605095036155712436&amp;amp;channelId=1119) ⭐️ 7.0/10

A CCTV investigation found that 14 of 15 takeout vendors labeled as &\#x27;transparent kitchen&\#x27; in Changsha, Wuhan and Lijiang failed to show key food prep areas on camera, with 6 falsely claiming dine-in status and some showing rodent and sanitation issues, prompting the State Administration for Market Regulation to launch investigations and suspend businesses in multiple provinces.

telegram · zaihuapd · Oct 4, 10:38

**「Background」** The &\#x27;transparent kitchen&\#x27; label is a Chinese food-safety initiative requiring vendors to livestream or record their cooking and prep areas to build consumer trust, but the investigation revealed widespread non-compliance across the takeout sector.

**「Impact」** The crackdown affects millions of takeout consumers and delivery platforms, as regulators conduct industry-wide food-safety remediation that could lead to stricter oversight and temporary service disruptions for affected vendors.

**Tags**: `#Food Safety`, `#Regulatory Enforcement`, `#E-commerce`, `#Consumer Protection`, `#China`

---
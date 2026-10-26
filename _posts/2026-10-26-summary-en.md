---
layout: default
title: "Horizon Summary: 2026-10-26 (EN)"
date: 2026-10-26
lang: en
---

> From 29 items, 6 important content pieces were selected

---

**Technology News**
1. [Brotli decoder flaw CVE-2026-111497 hits Python and Node.js HTTP stacks](#item-tech-news-1) ⭐️ 8.0/10
2. [10-year-old Inception v3 CNN beats frontier LLMs on skin cancer diagnosis](#item-tech-news-2) ⭐️ 7.0/10
3. [Nanbeige releases Nanbeige4.3-33B, an Apache 2.0 teacher model for smaller agents \[N\]](#item-tech-news-3) ⭐️ 7.0/10
4. [Tesla to Add In-House AI Maps in FSD v15](#item-tech-news-4) ⭐️ 7.0/10
5. [GEEKCON Shanghai Drone Challenge Suspended After Manufacturer Alarm](#item-tech-news-5) ⭐️ 7.0/10

**Financial News**
1. [China&\#x27;s 2025 population falls by 3.39 million to 1.4049 billion](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Brotli decoder flaw CVE-2026-111497 hits Python and Node.js HTTP stacks](https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) ⭐️ 8.0/10

A high-severity flaw in Google&\#x27;s Brotli decoder, CVE-2026-111497 \(CVSS 4.0 score 9.2\), affects Brotli versions 1.0.3 through 1.2.0 and enables unauthenticated remote attackers to trigger memory corruption, data leaks, crashes, or potential arbitrary code execution via crafted compressed streams. The issue, initially disclosed as Node2Shell and later called HTTP2Shell, extends to Python and Node.js HTTP components. Patches are available: Brotli 1.2.1, brotlicffi 1.2.1.0, and Node.js 22.23.4, 24.22.1, and 26.12.1. OpenAI reported the vulnerability in February 2026.

telegram · zaihuapd · Oct 25, 02:42

**「Brotli in HTTP compression」** Brotli is a lossless compression algorithm widely used for HTTP content encoding, supported by browsers and server-side libraries including Python&\#x27;s Brotli package and Node.js&\#x27;s built-in zlib/brotli support. Prior security disclosures in compression libraries, such as past zlib and gzip vulnerabilities, have shown how malformed compressed streams can lead to memory-safety issues in decoders.

**「Upgrade required for affected stacks」** Organizations running Python services using Brotli or brotlicffi, and Node.js deployments on the 22.x, 24.x, or 26.x release lines, should upgrade immediately to the patched versions to prevent remote code execution and denial-of-service attacks. Because the vulnerability is exploitable via unauthenticated HTTP requests, any internet-facing service relying on Brotli decompression is at risk until patched.

**Tags**: `#security`, `#vulnerability`, `#Brotli`, `#Python`, `#Node.js`

---

<a id="item-tech-news-2"></a>
### [10-year-old Inception v3 CNN beats frontier LLMs on skin cancer diagnosis](https://lynchlab.net/llm-skin-cancer) ⭐️ 7.0/10

A fine-tuned 10-year-old Inception v3 CNN, trained on 68,011 ISIC dermoscopic and clinical images on a single H100 GPU, outperformed two frontier LLMs on skin cancer diagnosis across 200 held-out test lesions. The test lesions and all images of the same lesions or patients were removed from training, validation, and threshold selection, making this a clean out-of-sample comparison. The result illustrates that general-purpose LLMs are not well-suited for specialized medical imaging tasks where a smaller, domain-specific model can be more accurate.

hackernews · sungam · Oct 25, 17:15 · [Discussion](https://news.ycombinator.com/item?id=50233779)

**「Background」** Convolutional neural networks \(CNNs\) like Inception v3, introduced in 2014, were designed specifically for image classification and became the standard architecture for medical imaging tasks before the rise of large language models. The ISIC Archive is a widely used public dataset of dermoscopic and clinical skin lesion images for training and evaluating skin cancer detection models. Frontier LLMs, while powerful for text and multimodal reasoning, are not architecturally optimized for fine-grained visual classification in specialized domains like dermatology.

**「Impact」** For developers and researchers building medical AI systems, this comparison suggests that selecting an architecture matched to the task \(e.g., a CNN for image classification\) is more important than using a general-purpose multimodal LLM, and that smaller, well-tuned domain-specific models can outperform much larger general models while requiring fewer computational resources.

**「Community Discussion」** Commenters on Hacker News largely agreed that the result was unsurprising, with one noting that specialized architectures like a 30-million-parameter KataGo network can be superhuman at Go while frontier LLMs are not, and another pointing out that people previously defended LLM development by citing potential medical applications like cancer diagnosis. One commenter emphasized that for any application at scale, a dedicated classifier using the right architecture is more accurate than a general-purpose LLM.

**Tags**: `#machine-learning`, `#computer-vision`, `#medical-imaging`, `#model-comparison`, `#healthcare-ai`

---

<a id="item-tech-news-3"></a>
### [Nanbeige releases Nanbeige4.3-33B, an Apache 2.0 teacher model for smaller agents \[N\]](https://www.reddit.com/r/MachineLearning/comments/1xf6x35/nanbeige_releases_nanbeige4333b_an_apache_20/) ⭐️ 7.0/10

Nanbeige releases Nanbeige4.3-33B, a 33B Apache 2.0 teacher model with a 512K context window, reporting strong Terminal-Bench scores but mixed results on SWE-Bench Pro.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 25, 16:32

**Tags**: `#language-models`, `#open-source`, `#benchmarks`, `#agent-models`, `#apache-2.0`

---

<a id="item-tech-news-4"></a>
### [Tesla to Add In-House AI Maps in FSD v15](https://www.digitaltoday.co.kr/en/view/118497/tesla-to-build-in-house-maps-and-navigation-to-address-fsd-limits) ⭐️ 7.0/10

Tesla is developing an in-house AI-based map and navigation system that will debut in FSD v15, initially covering trip start and end phases before expanding to navigation and parking in the following months. The system uses fleet-collected road data to improve speed limit recognition, parking, and route selection, and supports voice commands and personalized route preferences. This shift addresses known limitations in FSD, particularly in speed limit recognition, parking, and route selection, as highlighted by shareholders.

telegram · zaihuapd · Oct 25, 10:57

**「Tesla&\#x27;s Previous Stance on Maps」** Tesla previously stated that autonomous driving should not rely on maps, favoring a vision-based approach using real-time camera data. This new in-house mapping effort represents a notable departure from that earlier position.

**「Improved FSD Capabilities Expected」** FSD v15 users can expect better speed limit recognition, parking assistance, and route selection once the AI map system is fully rolled out, though the feature will be introduced gradually over several months.

**Tags**: `#Tesla FSD`, `#AI mapping`, `#autonomous driving`, `#navigation systems`, `#software updates`

---

<a id="item-tech-news-5"></a>
### [GEEKCON Shanghai Drone Challenge Suspended After Manufacturer Alarm](https://tech.ifeng.com/c/8xSZe56UAz6) ⭐️ 7.0/10

A drone security challenge at GEEKCON Shanghai, which required participants to bypass GPS no-fly restrictions and seize control of a drone, reportedly triggered an alarm at a major drone manufacturer, leading to personnel being detained and the event being temporarily suspended. The incident occurred on the night of October 24, 2026, during the closing of the security-focused gathering. The challenge&\#x27;s technical nature has reignited discussions about the boundaries of responsible security disclosure and vendor cooperation.

telegram · zaihuapd · Oct 25, 13:29

**「Drone security challenges and GPS no-fly bypass」** GEEKCON is an annual security conference held each October 24, sponsored by major Chinese tech companies including Huawei, Tencent Security, and Ant Group. Drone security challenges at such events typically involve testing GPS spoofing and control-takeover techniques, which are also relevant to real-world concerns such as state-sponsored GPS jamming and spoofing, as seen in recent incidents like the September 2025 drone incursion over Poland where Russia was reported to be jamming satellite signals.

**「Raises Questions on Security Research Boundaries」** The suspension highlights ongoing tensions between white-hat security researchers and vendors, particularly in sensitive domains like drone technology where control takeover and GPS spoofing can have real-world safety implications. With long-time sponsors like Huawei, Tencent Security, and Ant Group involved, the incident may influence how future security challenges are vetted and coordinated with manufacturers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=xWAAaYdLkoE">Australia Supercharges Poland&#x27;s Drone Defense! - YouTube</a></li>
<li><a href="https://www.aethovpn.com/en/blog/security-and-privacy/gps-spoofing">GPS Spoofing : False Signals, Warning Signs, and Safety | AethoVPN</a></li>

</ul>
</details>

**Tags**: `#security research`, `#drone security`, `#GPS spoofing`, `#responsible disclosure`, `#GEEKCON`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s 2025 population falls by 3.39 million to 1.4049 billion](https://weibo.com/1796087453/5357878513767954) ⭐️ 7.0/10

China&\#x27;s total population fell by 3.39 million in 2025 to 1.4049 billion at year-end, according to the 2026 China Statistical Yearbook, bringing the population close to the 1.4 billion threshold; the country recorded 7.92 million births with a birth rate of 5.63 per 1,000 people and a natural growth rate of -2.41 per 1,000.

telegram · zaihuapd · Oct 25, 12:02

**「Background」** The decline reflects a continuing demographic trend driven by low birth rates, with 2025 data showing nine provinces exceeding a 7 per 1,000 birth rate and seven provinces recording positive natural growth, mostly in western and southern regions, while Heilongjiang, Jilin, and Liaoning reported the lowest birth rates.

**Tags**: `#Demographics`, `#China`, `#Economic data`, `#Population`, `#Policy`

---
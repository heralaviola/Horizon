---
layout: default
title: "Horizon Summary: 2026-10-24 (EN)"
date: 2026-10-24
lang: en
---

> From 39 items, 12 important content pieces were selected

---

**Tools Update**
1. [openai/codex rust-v0.164.0: presets, inline config, image previews, enterprise MCP auth](#item-tools-update-1) ⭐️ 8.0/10

**Technology News**
1. [iPhone Jailbreak Demonstrates Deep System Access](#item-tech-news-1) ⭐️ 8.0/10
2. [Kimi K3.1-Pro: 10T Open-Weight Model Released](#item-tech-news-2) ⭐️ 8.0/10
3. [Amazon Trainium Chips Expand to AI Training with Native PyTorch Support](#item-tech-news-3) ⭐️ 7.0/10
4. [Swarm Imitation Proven Equivalent to Single-Agent RL in Bandits](#item-tech-news-4) ⭐️ 7.0/10
5. [I just came across Next-Concept Modeling and the idea is fascinating\[R\]](#item-tech-news-5) ⭐️ 7.0/10
6. [LLM Memory: The Forgetting Problem Beyond Recall](#item-tech-news-6) ⭐️ 7.0/10
7. [High-Recall Coronary Stenosis Detection: Annotation and Evaluation Challenges](#item-tech-news-7) ⭐️ 7.0/10
8. [China&\#x27;s State Council issues AI employment mitigation policy](#item-tech-news-8) ⭐️ 7.0/10
9. [PHP Foundation Advises Disabling Upload Progress to Mitigate CVE-2026-115560 RCE](#item-tech-news-9) ⭐️ 7.0/10

**Financial News**
1. [Domestic AI model service prices double to 13.46 yuan after two-year price war](#item-finance-news-1) ⭐️ 7.0/10
2. [EU ends anti-dumping duties on Chinese solar glass](#item-finance-news-2) ⭐️ 7.0/10

---

## Tools Update

<a id="item-tools-update-1"></a>
### [openai/codex rust-v0.164.0: presets, inline config, image previews, enterprise MCP auth](https://github.com/openai/codex/releases/tag/rust-v0.164.0) ⭐️ 8.0/10

openai/codex released rust-v0.164.0, a shipped release that adds reusable prompt/slash-command presets, inline model and permissions configuration, image previews in the transcript, enterprise MCP authentication, credential masking for remote sessions, and an enabled-by-default Amazon Bedrock setup wizard, alongside several bug fixes. The changes are additive and improve configuration, authentication, and terminal UX without apparent breaking changes.

github · github-actions\[bot\] · Oct 23, 04:48

**「Changes」** \#\#\# New Features
\- Save reusable prompts and slash commands in ten numbered \`/presets\` slots, with a keyboard menu for quick access. \(\#54380, \#54381\)
\- Set model, reasoning effort, speed, and permission profiles directly with inline \`/model\` and \`/permissions\` arguments. \(\#54378, \#54383\)
\- Preview viewed and generated images in the fullscreen transcript on terminals supporting Kitty or Sixel graphics. \(\#54216\)
\- Authenticate enterprise MCP connections using eligible Codex account grants or dedicated sign-in, including OAuth clients requiring secrets. \(\#55334, \#55859, \#56001\)
\- Mask credentials during supported remote Bash commands and Zsh snapshot sessions, including credentials from custom providers. \(\#54309, \#54432, \#56049\)
\- The Amazon Bedrock setup wizard is now enabled by default, with API key entry grouped alongside other AWS sign-in methods when credentials are detected. \(\#56033, \#56023\)

\#\#\# Bug Fixes
\- Failed compaction no longer leaves partial summaries in conversation history, and background compaction failures fall back without panicking. \(\#53932, \#55581\)
\- Resuming sessions now finds compressed histories and restores saved thread settings instead of replacing them with global defaults. \(\#54008, \#55923\)
\- Windows HTTPS and WebSocket connections now handle proxy authentication challenges using the signed-in user&\#x27;s Negotiate or NTLM credentials. \(\#55994, \#56000\)
\- CLI configuration overrides are preserved when \`-c\` or \`--config\` appears at multiple subcommand levels. \(\#56022\)
\- Queued prompts now wait for pending permission selections to resolve before continuing. \(\#55682\)
\- Hardened sandbox checks for case-variant metadata paths on macOS and replaceable symlinks used to locate executables. \(\#54273, \#55384\)

\#\#\# Chores
\- Reduced disk usage by pruning unused installations, cleaning abandoned marketplace checkouts, and bounding daemon logs. \(\#53827, \#55149, \#55689, \#55690, \#55856\)
\- Updated the embedded JavaScript runtime with safety checks for optimized \`Array.sort\` operations. \(\#54519\)

**「Impact」** Users who rely on prompt reuse, model switching, or enterprise MCP integrations should review the new \`/presets\`, inline \`/model\` and \`/permissions\` arguments, and the enterprise MCP authentication flow. Teams using remote Bash or Zsh snapshot sessions benefit from credential masking, and AWS users will see the Bedrock wizard enabled by default. The compaction and session-resume fixes improve reliability when resuming conversations. No migration steps are described, but the breadth of new auth and config options may warrant a quick review before upgrading.

**Tags**: `#presets`, `#model-configuration`, `#image-preview`, `#mcp-authentication`, `#credential-masking`

---

## Technology News

<a id="item-tech-news-1"></a>
### [iPhone Jailbreak Demonstrates Deep System Access](https://blog.calif.io/p/iphone) ⭐️ 8.0/10

A team successfully jailbroke an iPhone, demonstrating deep system-level access to the device. The jailbreak enables users to bypass Apple&\#x27;s restrictions and gain root access to the operating system, allowing for extensive customization and control over the hardware. The demonstration has sparked technical discussion about mobile security, Apple&\#x27;s countermeasures, and the implications for platform control. The Hacker News discussion reflects strong community interest, with 741 points and 499 comments debating the security ramifications and practical usability of jailbroken devices.

hackernews · pavel\_lishin · Oct 23, 16:21 · [Discussion](https://news.ycombinator.com/item?id=50211474)

**「Jailbreaking and iPhone Security Context」** Jailbreaking an iPhone involves bypassing Apple&\#x27;s software restrictions to gain root-level access, allowing users to modify the operating system and install unauthorized software. This practice has been a persistent challenge for Apple, which regularly patches vulnerabilities exploited by jailbreak tools and may detect jailbroken devices to restrict access to services like iCloud and iMessage. The referenced blog post comes from Calif, a security engineering firm known for red teaming work with major AI companies, suggesting the jailbreak demonstration may be part of broader security research efforts.

**「Community Reactions to Jailbreak」** Community members expressed mixed feelings about the jailbreak. Some users lamented the limitations imposed by Apple&\#x27;s ecosystem, noting that even with a jailbreak, Apple can detect modifications and restrict access to services like iCloud and iMessage, effectively turning the iPhone into an iPod touch. Others raised concerns about accessibility, suggesting that security research opportunities are limited to a select group with access to specific device models. A few users questioned the real-world effectiveness of Apple&\#x27;s Lockdown Mode against such exploits, while others expressed interest in gaining root access to their own devices.

<details><summary>References</summary>
<ul>
<li><a href="https://calif.io/">Calif | Hackers gonna hack</a></li>

</ul>
</details>

**Tags**: `#iPhone`, `#jailbreak`, `#security`, `#reverse engineering`, `#mobile`

---

<a id="item-tech-news-2"></a>
### [Kimi K3.1-Pro: 10T Open-Weight Model Released](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

Kimi has released K3.1-Pro, a 10 trillion parameter open-weight model supporting 1 million token context, available now via Kimi, Work, Code, and API. The model shows improved performance in programming \(Terminal-Bench 4.0 score of 65.7%\), 3D creation \(BenchCAD score of 92.7%\), and financial research, with a Highspeed variant offering 2-3x faster inference. Full model weights are planned for release by November 4, 2026, though current availability is limited to API access.

telegram · zaihuapd · Oct 23, 17:14

**「Open-Weight LLM Context」** Open-weight large language models allow public access to trained parameters, enabling local deployment and modification. K3.1-Pro builds on the K3 model series with expanded training scale, positioning itself as Moonshot&\#x27;s strongest open-weight offering to date.

**「Performance and Pricing Impact」** K3.1-Pro is priced at $2.00/million tokens for input and $10/million for output, matching GPT-6.1 Sol and undercutting Claude Opus 5.5. The Highspeed variant costs twice as much but offers 2-3x faster inference, providing developers with a trade-off between speed and cost. Independent verification of the reported benchmarks is not yet available.

**Tags**: `#large language models`, `#open weights`, `#programming`, `#3D modeling`, `#benchmarks`

---

<a id="item-tech-news-3"></a>
### [Amazon Trainium Chips Expand to AI Training with Native PyTorch Support](https://newsletter.semianalysis.com/p/amazons-trainium-takes-a-strike-at) ⭐️ 7.0/10

Amazon&\#x27;s Trainium chips, previously optimized for inference workloads, are now being positioned as viable for AI training tasks as well. The report highlights native PyTorch integration, enabling developers to use familiar frameworks without extensive code modifications. Additional tooling such as TorchTitan and a &\#x27;GPU Impossible Profiler&\#x27; are mentioned as part of Amazon&\#x27;s effort to improve developer experience and performance optimization on Trainium hardware. However, the source material lacks detailed benchmarks or concrete performance data to substantiate claims of competitiveness against established training accelerators.

rss · Semianalysis · Oct 23, 19:06

**「Trainium Chips and AWS AI Infrastructure」** Amazon&\#x27;s Trainium chips are custom silicon developed by AWS for machine learning workloads, designed to offer an alternative to GPU-based solutions from vendors like NVIDIA. Initially focused on inference, AWS has been expanding their capabilities to support training workloads, aligning with broader industry trends toward custom AI accelerators. Native PyTorch support reflects AWS&\#x27;s strategy to reduce friction for developers migrating or deploying models on its cloud infrastructure.

**「Implications for AI Development on AWS」** Organizations using AWS may find Trainium chips increasingly attractive for both training and inference, potentially reducing reliance on GPU instances. However, without published performance comparisons or real-world deployment data, it remains unclear how Trainium stacks up against dominant GPU platforms in large-scale training scenarios. Developers should monitor upcoming releases for benchmark details before making infrastructure decisions.

**Tags**: `#AI Hardware`, `#Machine Learning`, `#Amazon Web Services`, `#PyTorch`, `#Chip Architecture`

---

<a id="item-tech-news-4"></a>
### [Swarm Imitation Proven Equivalent to Single-Agent RL in Bandits](https://www.reddit.com/r/MachineLearning/comments/1xdhf7r/r_the_hive_mind_is_a_single_reinforcement/) ⭐️ 7.0/10

A Reddit post announces a proof that collective decision-making via local imitation in swarms is mathematically equivalent to single-agent reinforcement learning \(RL\) in a multi-armed bandit setting. The work introduces Maynard-Cross Learning \(MCL\), a macroscopic update rule where N individuals act as N parallel environment rollouts with an effective per-sample step size of alpha = 1/N. The equivalence is derived by treating the population distribution over options as the policy of a single macro-agent and applying evolutionary replicator dynamics to bridge individual-level imitation and group-level policy updates. The paper is available on arXiv \(2410.17517\) with code and a project page, though the Reddit post provides only a truncated explanation without full proofs or empirical validation.

reddit · r/MachineLearning · /u/mistlab · Oct 23, 15:37

**「Background」** Multi-armed bandit problems model sequential decision-making where an agent selects actions to maximize cumulative reward, with Cross Learning being a known bandit algorithm. Swarm intelligence, exemplified by honey bee waggle dances, involves simple individuals following local imitation rules to achieve collective decisions, previously studied through evolutionary game theory and replicator dynamics.

**「Impact」** The equivalence provides a formal mechanism explaining how hive-mind intelligence emerges from non-learning individuals, offering new tools for analyzing imitative dynamics in social and economic systems and for designing decentralized swarm robotics algorithms. Researchers in collective intelligence and RL may use MCL to bridge biological models with machine learning frameworks.

**Tags**: `#reinforcement learning`, `#swarm intelligence`, `#multi-armed bandits`, `#collective decision-making`, `#mathematical equivalence`

---

<a id="item-tech-news-5"></a>
### [I just came across Next-Concept Modeling and the idea is fascinating\[R\]](https://www.reddit.com/r/MachineLearning/comments/1xd7bsu/i_just_came_across_nextconcept_modeling_and_the/) ⭐️ 7.0/10

A Reddit post highlights Next-Concept Modeling, a hierarchical discrete-code text-generation method that reportedly achieves up to 31x faster generation than diffusion language model baselines, linking to the arXiv paper for technical details.

reddit · r/MachineLearning · /u/PanelReader · Oct 23, 07:24

**Tags**: `#next-concept-modeling`, `#text-generation`, `#vq-vae`, `#diffusion-models`, `#language-model-efficiency`

---

<a id="item-tech-news-6"></a>
### [LLM Memory: The Forgetting Problem Beyond Recall](https://www.reddit.com/r/MachineLearning/comments/1xdpek9/are_we_solving_llm_memory_by_remembering_more/) ⭐️ 7.0/10

A Reddit discussion post raises concerns that current LLM memory approaches prioritize recall over forgetting or updating outdated information. The post highlights scenarios where conflicting data persists in long-context models, citing architectures like DeltaNet and BDH \(Dragon Hatchling\) as potential solutions. It questions whether the real issue lies in memory storage and update mechanisms or in how models reason over contradictory information, and calls for benchmarks that test memory updating rather than just retrieval.

reddit · r/MachineLearning · /u/Prestigious-Tip6030 · Oct 23, 20:39

**「Background: LLM Memory Architectures and Forgetting」** Long-context models and retrieval-augmented generation \(RAG\) systems can retain vast amounts of information, but they lack mechanisms to selectively forget or update outdated facts, causing conflicts when new information contradicts prior knowledge. Recent memory-augmented architectures have attempted to address this: DeltaNet applies the delta learning rule to write only prediction-error-based corrections rather than accumulating redundant copies, while BDH \(Dragon Hatchling\) uses Hebbian-style synaptic plasticity to adjust connections based on concept activation. Concurrently, the research community has begun developing benchmarks such as AgentMemoryBench and BEMULA that explicitly measure forgetting, knowledge conflict resolution, and memory mutation across sessions, reflecting growing recognition that effective memory management requires not just recall but also controlled forgetting.

**「Implications for Memory-Augmented Systems」** If unresolved, the inability to effectively forget or update outdated information could lead to persistent errors in applications like coding agents or RAG-based systems, where stale data may override newer, correct information. This underscores the need for evaluation frameworks that measure a model&\#x27;s ability to revise its knowledge in light of new evidence.

<details><summary>References</summary>
<ul>
<li><a href="https://vivekgupta.ai/llm-visualizer/visualization/DeltaNet.html">DeltaNet | LLM Improvement Visualizer</a></li>
<li><a href="https://neelmishra.github.io/blog/dl/architectures/transformers/variants/delta-net.html">DeltaNet: Write the Error, Not Another Copy | Neel Mishra</a></li>
<li><a href="https://d2l.smola.org/chapter_recurrent-modern/deltanet.html">12.5 DeltaNet and Corrective Memory Updates – Dive into Deep ...</a></li>
<li><a href="https://pathway.com/research/bdh-explainer">BDH Architecture Explained: Pathway’s Dragon Hatchling</a></li>
<li><a href="https://github.com/pathwaycom/bdh/">GitHub - pathwaycom/bdh: BDH (Dragon Hatchling ...</a></li>
<li><a href="https://arxiv.org/abs/2509.26507">The Dragon Hatchling: The Missing Link between the ...</a></li>
<li><a href="https://arxiv.org/abs/2605.09608">[2605.09608] Geometry Conflict: Explaining and Controlling ... From Recall to Forgetting: Benchmarking Long-Term Memory for ... LOKA: Conflict-Aware LLM Knowledge Update with Adaptive ... CAN AGENTS FORGET WHEN ASKED? A BENCH MARK FOR MEMORY ... Benchmarking Continual Agent Memory for Online Learning ... BENCHMARKING CONTINUAL AGENT MEMORY FOR ONLINE LEARNING ... MemoryAgentBench: LLM Memory Benchmark</a></li>
<li><a href="https://aclanthology.org/2026.findings-acl.1337.pdf">From Recall to Forgetting: Benchmarking Long-Term Memory for ...</a></li>
<li><a href="https://aclanthology.org/2026.acl-long.760.pdf">LOKA: Conflict-Aware LLM Knowledge Update with Adaptive ...</a></li>

</ul>
</details>

**Tags**: `#llm-memory`, `#long-context-models`, `#neural-architectures`, `#rag`, `#ai-systems`

---

<a id="item-tech-news-7"></a>
### [High-Recall Coronary Stenosis Detection: Annotation and Evaluation Challenges](https://www.reddit.com/r/MachineLearning/comments/1xdkcav/stenosis_detection_in_coronary_angiograms_need/) ⭐️ 7.0/10

A machine learning practitioner is developing a system to detect coronary artery stenosis in x-ray angiograms with high recall, accepting false positives as long as they remain manageable. They previously applied YOLO to in-house datasets, achieving acceptable in-domain performance but poor cross-dataset generalization, largely due to inconsistent annotation formats—fixed-size boxes around points versus lesion-fitted boxes. Their planned approach combines vessel centerline radius profiling to flag narrowing, followed by a candidate-filtering network, and they are seeking validation of this method or alternatives. The primary concern is evaluation, since doctor-provided labels do not mark every narrowing, making recall estimates overly optimistic.

reddit · r/MachineLearning · /u/Future-Structure-296 · Oct 23, 17:25

**「Coronary Angiogram Analysis and Annotation Variability」** Coronary angiography uses x-ray imaging to visualize blood vessels, where stenosis appears as vessel narrowing that requires precise localization and measurement. Annotation inconsistency across datasets is a known issue in medical imaging, where different institutions or annotators may use varying bounding box conventions, affecting model training and evaluation. The ARCADE dataset is one of the few publicly available annotated coronary angiogram datasets, though it may not capture the full diversity of clinical cases.

**「Evaluation Against Incomplete Ground Truth Remains an Open Challenge」** For practitioners building similar systems, the key takeaway is that cross-dataset generalization can fail not due to model limitations but due to annotation format mismatches, requiring careful preprocessing and standardization. Additionally, computing honest recall metrics against incomplete medical ground truth remains an unresolved problem, suggesting that alternative evaluation strategies such as lesion-level sensitivity analysis or synthetic lesion insertion may be necessary for reliable assessment.

**Tags**: `#medical imaging`, `#object detection`, `#YOLO`, `#evaluation`, `#annotation`

---

<a id="item-tech-news-8"></a>
### [China&\#x27;s State Council issues AI employment mitigation policy](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 7.0/10

China&\#x27;s State Council General Office has issued the &quot;Guiding Opinions on Adapting to AI Development to Promote Employment-Friendly Development,&quot; which directs AI deployment to prioritize labor-scarce and high-risk jobs while carefully controlling its application in labor-intensive industries. The policy encourages enterprises to establish unemployment buffer periods, notify affected workers in advance, and provide retraining and job-transition support to mitigate AI-driven employment displacement.

telegram · zaihuapd · Oct 23, 12:54

**「Context of AI and employment concerns」** Governments worldwide have grappled with balancing AI advancement against potential job displacement, with various countries exploring regulatory frameworks to address workforce impacts. This directive represents China&\#x27;s formal policy response to those concerns at the national level.

**「Implications for AI deployment and workforce」** The policy may influence how AI companies approach market entry in China, potentially favoring applications in sectors with labor shortages while requiring additional compliance measures for workforce transition in labor-intensive industries. Organizations deploying AI systems may need to implement notification procedures and retraining programs for affected employees.

**Tags**: `#AI policy`, `#employment`, `#government regulation`, `#AI ethics`, `#labor market`

---

<a id="item-tech-news-9"></a>
### [PHP Foundation Advises Disabling Upload Progress to Mitigate CVE-2026-115560 RCE](https://x.com/ThePHPF/status/2113580383875019242) ⭐️ 7.0/10

The PHP Foundation has recommended that developers disable the session.upload\_progress.enabled setting by setting it to 0 until the next PHP version is released, in order to mitigate CVE-2026-115560, a remote code execution vulnerability. The vulnerability affects only applications that switch the non-default serialize\_handler to &\#x27;php&\#x27; at runtime. This guidance follows a similar prior recommendation related to CVE-2026-109619.

telegram · zaihuapd · Oct 23, 13:46

**「Vulnerability Context」** The vulnerability involves PHP&\#x27;s session upload progress feature, which tracks file upload status via session data. When combined with a non-default serialize\_handler set to &\#x27;php&\#x27; at runtime, this feature can be exploited to achieve remote code execution. The PHP Foundation previously issued comparable mitigation advice for CVE-2026-109619, indicating a recurring pattern in this component.

**「Affected Applications」** PHP applications that dynamically switch the serialize\_handler to &\#x27;php&\#x27; during runtime are at risk of remote code execution. Developers running such configurations should immediately disable session.upload\_progress.enabled as a temporary mitigation until a patched PHP version becomes available.

**Tags**: `#PHP`, `#security`, `#vulnerability`, `#remote code execution`, `#CVE`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Domestic AI model service prices double to 13.46 yuan after two-year price war](https://mp.weixin.qq.com/s/JcsPrHgEkeseGBHAJ7s9mA) ⭐️ 7.0/10

A China Academy of Information and Communications Technology \(CAICT\) report shows the average normalized price of domestic large-model services rose from 6.8 yuan in the second half of 2025 to 13.46 yuan, roughly doubling after two years of price cuts.

telegram · zaihuapd · Oct 23, 06:05

**「Background」** The CAICT Artificial Intelligence Institute released the 2026 Large Model Token Service Performance Monitoring Report on October 23, documenting the shift from a prolonged domestic price war to higher, more consolidated pricing.

**「Impact」** Higher domestic model prices may increase operating costs for Chinese AI service providers and developers, even as they remain well below the roughly 117.8 yuan average for overseas models.

**Tags**: `#Artificial Intelligence`, `#Technology`, `#Market Pricing`, `#China`, `#Industry Report`

---

<a id="item-finance-news-2"></a>
### [EU ends anti-dumping duties on Chinese solar glass](https://www.163.com/dy/article/L9R94K6105484D40.html) ⭐️ 7.0/10

The European Commission repealed anti-dumping and anti-subsidy tariffs on Chinese solar glass, ending duties that had reached 84.2% and applying retroactively from 22 October 2026, with tariffs paid since 22 July 2025 eligible for refund without interest.

telegram · zaihuapd · Oct 23, 06:54

**「Background」** The duties were imposed to counter what the EU judged to be unfair pricing and subsidies, but the European Commission said the measure is no longer needed because there are no longer any active EU solar-glass producers and Chinese imports now account for only about 3% of the EU market, down from 30.5% during the original investigation.

**「Impact」** The repeal removes a major cost barrier for Chinese solar-glass exporters to the EU, though the immediate market effect is limited given China&\#x27;s small current import share and the absence of domestic EU producers to protect.

**Tags**: `#trade policy`, `#EU-China relations`, `#solar energy`, `#tariffs`, `#anti-dumping duties`

---
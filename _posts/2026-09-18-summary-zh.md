---
layout: default
title: "Horizon Summary: 2026-09-18 (ZH)"
date: 2026-09-18
lang: zh
---

> 从 61 条内容中筛选出 18 条重要资讯。

---

**工具更新**
1. [openai/codex rust-v0.155.0 发布：语音对话与任务管理增强](#item-tools-update-1) ⭐️ 8.0/10
2. [uv 0.12.16 发布：新增包哈希校验与 macOS 兼容性改进](#item-tools-update-2) ⭐️ 7.0/10
3. [openai/codex rust-v0.155.1 修复 TUI 推理摘要默认启用的 Bug](#item-tools-update-3) ⭐️ 5.0/10

**科技新闻**
1. [Android 17 在 AOSP 之外引入新 API，引发开放性担忧](#item-tech-news-1) ⭐️ 7.0/10
2. [开发者声称借助 AI 证明了康威猜想](#item-tech-news-2) ⭐️ 7.0/10
3. [Inside ZCode: Silently uploading your Git history to the cloud](#item-tech-news-3) ⭐️ 7.0/10
4. [Engrams Embedding Entendre: Codesign for Efficient DRAM/SSD Offloading](#item-tech-news-4) ⭐️ 7.0/10
5. [NHANES 心病预测项目公开数据泄露审计与校准处理](#item-tech-news-5) ⭐️ 7.0/10
6. [Claude 项目改版：从文件夹到对话式任务管理](#item-tech-news-6) ⭐️ 7.0/10
7. [OpenAI 推出法律 AI 基础 Astra for Law](#item-tech-news-7) ⭐️ 7.0/10
8. [联合国携手谷歌打造 AI 可用的全球数据平台](#item-tech-news-8) ⭐️ 7.0/10
9. [美国联邦公报网站撤下之前采用的 Qwen 搜索工具](#item-tech-news-9) ⭐️ 7.0/10
10. [长鑫存储拟进军闪存市场](#item-tech-news-10) ⭐️ 7.0/10
11. [Anthropic 设立湿实验室推进 AI 药物发现计划](#item-tech-news-11) ⭐️ 7.0/10

**科技博客**
1. [系统一模型编程的两大技巧](#item-tech-blog-1) ⭐️ 8.0/10

**财经新闻**
1. [Buffett 退出伯克希尔主席职位 儿子霍华德接任](#item-finance-news-1) ⭐️ 8.0/10
2. [住建部：二手房交易比例升至 52%，房地产进入存量时代](#item-finance-news-2) ⭐️ 7.0/10
3. [人民币兑美元升至四年高位 央行连续八日上调中间价](#item-finance-news-3) ⭐️ 7.0/10

---

## 工具更新

<a id="item-tools-update-1"></a>
### [openai/codex rust-v0.155.0 发布：语音对话与任务管理增强](https://github.com/openai/codex/releases/tag/rust-v0.155.0) ⭐️ 8.0/10

openai/codex 发布了 rust-v0.155.0 版本。这是一个功能丰富的更新，引入了实验性语音对话、TUI 实时推理摘要、代理概览中的任务管理、Touch ID 验证以及改进的 AWS 凭证处理等功能。这些变更涵盖了语音交互、任务管理、安全性和云集成等多个核心工作流程。

github · github-actions\[bot\] · 9月17日 23:14

**「变更内容」** \#\#\# 新功能
\- 新增实验性 \`/voice\` 对话功能，支持实时转录和麦克风控制（在支持的构建上通过 \`/experimental\` 启用）。
\- TUI 状态行现在显示实时推理摘要，并在成功回合后显示完成时间戳。
\- 代理概览中新增任务隐藏、归档和删除功能，以及工作区所有权详情和对干净受管工作区的删除确认。
\- 新增 Touch ID 验证用于本地 TUI 会话中的 MCP 请求（在支持的 Mac 设备上）。
\- 新增可配置的守护进程更新计划和 \`codex app-server daemon update\` 命令；保存的线程和活跃目标可在守护进程重启后恢复。
\- Amazon Bedrock 现在可以通过配置的命令获取 AWS 凭证，支持缓存、基于过期时间的刷新和身份验证恢复。

\#\#\# 缺陷修复
\- 即使在回合开始前压缩失败时，接受的提示也会被保存。
\- 修复错过的 tmux 调整大小、转录视图端口恢复和切换线程后出现的陈旧历史问题。
\- MCP 服务器现在准确报告过期的 OAuth 凭证，并在令牌刷新失败时提供重新连接指导。
\- 自动审批审查现在更可靠地保留完整的操作和授权证据，重试临时性失败，并区分审查失败与不安全操作的发现。
\- 切换账户时，远程控制会话、缓存的 WebSocket 状态和属于前一身份的模型目录将被失效。
\- 阻止 Windows 进程从受限 WSL 沙箱中逃逸，并加强经凭证代理的 shell 快照以防止凭证暴露。

\#\#\# 维护任务
\- 将 Python SDK 和运行时发布与稳定的 CLI 发布保持一致，使用匹配版本，并在 SDK 发布前验证运行时资产。

**「影响」** 此版本面向希望使用语音交互、更高效任务管理或增强安全性的用户。语音对话和 Touch ID 验证为交互方式带来了便利，但语音功能仍为实验性，可能存在稳定性或兼容性问题。依赖 Amazon Bedrock 的用户将受益于改进的 AWS 凭证处理。升级时，用户应注意实验性功能的启用方式，并确认其系统是否支持 Touch ID 验证。

**标签**: `#voice-conversations`, `#tui-enhancements`, `#task-management`, `#security`, `#cloud-integration`

---

<a id="item-tools-update-2"></a>
### [uv 0.12.16 发布：新增包哈希校验与 macOS 兼容性改进](https://github.com/astral-sh/uv/releases/tag/0.12.16) ⭐️ 7.0/10

uv 0.12.16 已发布，主要新增了对下载轮次和源分布包的哈希校验功能，提升了安全性；同时改进了 macOS 平台标记处理、Git URL 错误处理以及 Pyodide 发行版支持。这些变更为用户带来显著的安全性和稳定性提升。

github · astral-releases-bot\[bot\] · 9月18日 01:01

**「变更内容」** \#\#\# Python
\- 新增 Pyodide 314.0.7、0.29.5 和 0.27.8 发行版

\#\#\# 增强功能
\- 验证下载的轮次和源分布包是否符合包索引提供的哈希值
\- 允许 \`build-constraint-dependencies\` 条目包含哈希值，以验证下载的构建依赖项
\- 在 \`required-environments\` 中使用 macOS 轮次部署目标来处理 Darwin \`platform\_release\` 标记
\- 在解析锁文件时拒绝不支持的 Git URL 方案，而非在冻结导出时出现恐慌

\#\#\# 预览功能
\- 在所有依赖项类型中支持 \`lock-without-metadata\`，同时保留远程 URL 依赖项的 \`package.metadata\`，以实现脱机验证
\- 在 \`uv upgrade\` 中尊重配置的和命令行的索引设置，包括凭据
\- 允许 \`uv check\` 在非 uv 管理的项目中运行，且可在工作区外部运行
\- 在 \`uv check\` 中尊重 \`--python\` 和 \`UV\_PYTHON\` 选择 Python 版本

\#\#\# Bug 修复
\- 从显示的和记录的 URL 中隐藏 Azure 共享访问签名
\- 在重用缓存的分发包之前检查 \`pylock.toml\` 中的归档大小
\- 当后端元数据报告绝对路径时，保持用户编写的本地依赖路径在锁文件中为相对路径
\- 仅在其版本与活动版本引脚匹配时使用捆绑的 \`uv\_build\` 后端
\- 在配置凭据时处理格式错误的索引 URL，避免恐慌
\- 对于没有主机的代理 URL，报告配置错误而非恐慌
\- 当 URL 无法转换为路径时，返回凭据隐藏的错误，而非恐慌

**「影响」** 安全性关注的用户应优先升级，因为新增的哈希校验功能可有效防止供应链攻击。macOS 用户受益于更准确的平台标记处理，提升了兼容性。使用 Git URL 的用户可受益于更友好的错误提示，避免因不支持的 URL 方案导致的崩溃。预览功能的引入（如脱机锁验证）为高级用户提供了更多灵活性，但可能需要在生产环境中谨慎评估。常规用户无需采取额外迁移操作，即可直接升级至 0.12.16。

**标签**: `#security`, `#hash-verification`, `#compatibility`, `#macos`, `#pyodide`

---

<a id="item-tools-update-3"></a>
### [openai/codex rust-v0.155.1 修复 TUI 推理摘要默认启用的 Bug](https://github.com/openai/codex/releases/tag/rust-v0.155.1) ⭐️ 5.0/10

openai/codex 发布了 rust-v0.155.1 补丁版本，修复了新本地 TUI 会话中推理摘要被错误默认启用的 Bug，导致不支持该功能的提供商拒绝请求。此次为一次 Bug 修复补丁发布。

github · github-actions\[bot\] · 9月18日 20:03

**「变更内容」** \- 新本地 TUI 会话默认关闭推理摘要，修复因不支持推理摘要的提供商拒绝请求的问题。
\- 显式设置的推理摘要选项仍被正确遵守。
\- 恢复 TUI 推理摘要默认值为 &quot;none&quot;。

**「影响」** 使用本地 TUI 会话并依赖不支持推理摘要提供商的用户受到影响。升级后无需额外操作，之前因默认启用推理摘要而遭请求拒绝的问题将自动解决，同时用户仍可通过显式设置控制该行为。

**标签**: `#bug-fix`, `#tui`, `#reasoning-summary`, `#compatibility`, `#patch-release`

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Android 17 在 AOSP 之外引入新 API，引发开放性担忧](https://grapheneos.social/@GrapheneOS/117282080803799576) ⭐️ 7.0/10

Android 17 首次自 3.x 以来在 AOSP 之外引入新 API，Google 仅将其发布到 Pixel 设备上，而非传统的开放源代码项目（AOSP）版本。这意味着开发者和第三方制造商无法通过 AOSP 获取这些新功能，打破了过去新 API 同时发布到 AOSP 的惯例。该决定引发了对 Google 在开放源代码承诺上的担忧，尤其是对于依赖 AOSP 的项目如 GrapheneOS 而言。

hackernews · theanonymousone · 9月18日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49758736)

**「背景」** Android 17 作为 Google 自 3.x 版本以来首个在 AOSP 发布之前向 Pixel 设备独家添加新 API 的版本，其背后是 Google 调整 Android 发布节奏的结构性变化：Google 每半年向 OEM 和公众发布一次完整的 Android 源代码更新，但每年会发布四次 Pixel 专属更新，包括文档和 SDK。GrapheneOS 作为基于 AOSP 的安全隐私聚焦移动操作系统（自 2016 年首次发布），长期依赖这些 AOSP 更新来维护其去谷歌化的 Android 发行版，因此 Pixel 独占 API 的做法直接影响了其功能同步和安全补丁的及时性。

**「对开发者及开源项目的影响」** 这一变化可能限制开发者对新 API 的访问，尤其影响那些依赖 AOSP 构建自定义系统（如 GrapheneOS）的团队。这些项目可能需要等待 Google 的后续补丁或寻找替代方案，从而影响其功能更新速度和安全性。

**「社区对 Google 开放性策略的批评」** 社区成员 \[wps\] 指责 Google 对 GrapheneOS 设置越来越多的障碍，包括延迟的源代码更新和安全补丁限制。\[bri3d\] 解释说，问题不仅在于单个 API 的专属发布，而在于 Google 每年发布四次 Pixel 更新，但仅将部分季度补丁提供给 AOSP。\[Ajedi32\] 补充指出，首个和第三个季度补丁可能是专属 Pixel 的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS - Wikipedia</a></li>
<li><a href="https://alternativeto.net/news/2026/9/grapheneos-claims-android-17-qpr1-apis-remain-exclusive-to-pixel-devices/">GrapheneOS claims Android 17 QPR1 APIs remain exclusive to Pixel ...</a></li>
<li><a href="https://stateofsurveillance.org/news/grapheneos-android-17-port-degoogled-privacy-os-2026/">GrapheneOS Hits Android 17 the Day Google Releases It</a></li>

</ul>
</details>

**标签**: `#Android`, `#AOSP`, `#GrapheneOS`, `#Open Source`, `#Mobile Development`

---

<a id="item-tech-news-2"></a>
### [开发者声称借助 AI 证明了康威猜想](https://overreacted.io/how-i-vibed-a-proof-of-conways-conjecture/) ⭐️ 7.0/10

一位开发者在个人博客上发表了一篇名为《我如何借助 AI 证明康威猜想》的文章，并在 GitHub 上分享了一个名为 conway-refinement 的仓库，声称该仓库包含了对康威猜想的证明。然而，这一证明尚未经过正式的同行评审，仅以个人叙述的形式呈现，并引发了技术社区的讨论，特别是关于 AI 辅助数学发现的可信度问题。

hackernews · m-hodges · 9月18日 14:36 · [社区讨论](https://news.ycombinator.com/item?id=49755024)

**「背景」** 康威猜想是一项关于数列收敛性的开放数学问题，由约翰·康威提出，长期以来吸引了数学界的广泛关注。该问题的证明或 disproof 通常需要严格的数学推理和验证，而目前尚无公认的正式证明。

**「影响」** 这篇文章引发了对 AI 在数学研究中作用的深入讨论，特别是 AI 如何辅助数学家发现和验证新定理。然而，由于缺乏正式的同行评审，数学界可能仍需谨慎对待这一“证明”，并等待更严格的验证。

**「社区讨论」** 一位已发表且受过训练的业余数学家评论称，这种方法看起来是正确的，但建议继续简化和理解证明过程，直到自己能够完全跟进。另一位评论则将 AI 比作“无限猴子定理”中的猴子，认为 AI 的作用是辅助而非替代数学家的推理工作。

**标签**: `#mathematics`, `#artificial intelligence`, `#open source`, `#research`, `#conway&\#x27;s conjecture`

---

<a id="item-tech-news-3"></a>
### [Inside ZCode: Silently uploading your Git history to the cloud](https://blog.ferstar.org/en/posts/zcode-silent-workspace-snapshot-upload/) ⭐️ 7.0/10

ZCode, an AI coding agent by z.ai, was found to silently upload users&\#x27; entire Git history to the cloud via its codebase indexing feature, prompting an official apology and community discussion about AI agent permissions and privacy.

hackernews · csmantle · 9月18日 06:11 · [社区讨论](https://news.ycombinator.com/item?id=49750694)

**标签**: `#ai-safety`, `#privacy`, `#security`, `#coding-agents`, `#git`

---

<a id="item-tech-news-4"></a>
### [Engrams Embedding Entendre: Codesign for Efficient DRAM/SSD Offloading](https://newsletter.semianalysis.com/p/engrams-embedding-entendre-codesign) ⭐️ 7.0/10

A technical exploration of the Engrams model architecture and its impact on DRAM/SSD offloading efficiency, with implications for AI inference systems and hardware-software codesign.

rss · Semianalysis · 9月18日 14:34

**标签**: `#AI Systems`, `#Hardware-Software Codesign`, `#Model Architecture`, `#DRAM/SSD Optimization`, `#Inference Engineering`

---

<a id="item-tech-news-5"></a>
### [NHANES 心病预测项目公开数据泄露审计与校准处理](https://www.reddit.com/r/MachineLearning/comments/1wjp062/classifying_coronary_heart_disease_risk_from/) ⭐️ 7.0/10

用户 /u/YouJonaa 在 GitHub 项目 nhanes-chd-classification 中，使用 NHANES 2011-2018 四周期约 21,500 名成人数据，预测自报 physician-diagnosed 冠心病（CHD）。该项目明确移除了 NHANES 问卷中直接询问其他心血管疾病的变量，这些变量曾把 PR-AUC 从 0.23 虚增至 0.51。最终在留出测试集上，加权逻辑回归的 ROC-AUC 为 0.875，PR-AUC 为 0.239；随机森林和梯度提升与之相当。项目采用类别加权逻辑回归应对约 4% 的低发率问题，并在开发集上进行 sigmoid 重校准以修正原始概率严重过高（均预测风险 ~30% vs 实际 4%）的问题，同时在查看测试集前冻结决策阈值。

reddit · r/MachineLearning · /u/YouJonaa · 9月18日 12:36

**「背景」** NHANES（国家健康与营养状况评估调查）以人群抽样方式收集人口健康数据，其中包含直接询问受访者既往心血管疾病的问卷部分；若将这些自报的诊断变量纳入模型，会引入标签泄露（label leakage），导致模型实际学习到的是疾病间的共报关联，而非真实的风险因子。

**「影响」** 该项目对 NHANES 心病风险预测的从业者具有参考价值：它展示了如何通过显式泄露审计避免性能虚增，并通过在开发集上冻结阈值与校准步骤，确保测试集评估结果未被事后调优污染。然而，由于该项目为学生级别的实践作业，且未纳入吸烟、糖尿病及降压药使用等重要已有变量，目前尚不足以作为临床决策支持模型。

**标签**: `#machine-learning`, `#healthcare-ai`, `#data-leakage`, `#calibration`, `#NHANES`

---

<a id="item-tech-news-6"></a>
### [Claude 项目改版：从文件夹到对话式任务管理](https://claude.com/blog/projects-redesigned) ⭐️ 7.0/10

Anthropic 宣布重新设计 Claude 项目（Projects）功能，从传统的文件夹式管理转为对话式任务处理。用户只需描述目标，Claude 将自动拆解请求、分配并行线程、审查产出并汇总结果，同时支持移动设备随时跟进任务。该功能已在 Claude Code 中启动 beta 测试，首批面向部分 Claude Pro 和 Max 订阅用户，未来一周将扩大至更多 Claude Code 用户，之后覆盖全部 Claude 及 Team、Enterprise 方案。

telegram · zaihuapd · 9月18日 00:18

**「项目管理的演变」** Claude 项目最初以文件夹为基础，用户需手动组织文件和对话。此次改版将其转变为以对话为中心的任务管理方式，借助自动化拆解和并行处理技术，提升了复杂任务的处理效率。

**「对用户的影响」** 该改版使 Claude Code 用户能够更高效地处理复杂任务，无需手动拆分和管理多个线程。然而，由于该功能目前仅在 beta 阶段且面向有限用户群，部分用户可能无法立即体验到全部功能。

**标签**: `#Claude`, `#AI agents`, `#developer tools`, `#Anthropic`, `#project management`

---

<a id="item-tech-news-7"></a>
### [OpenAI 推出法律 AI 基础 Astra for Law](https://openai.com/index/astra-for-law/) ⭐️ 7.0/10

OpenAI 于 9 月 17 日推出 Astra for Law，这是一项将 GPT-6 Astra 与法律检索索引相结合的法律人工智能服务，旨在帮助律师事务所和法务科技公司构建 AI 产品。在 Vals AI 基准测试中，该服务在 200 道美国法律研究题上的正确率达到 54.0%，相比仅使用 GPT-6 Astra 联网搜索的 38.7%，实现了约 40% 的相对提升。该服务将首先通过 Trusted Access 向选定律所开放 ChatGPT 和 Codex 功能，随后推出 API，模型名称为 GPT-6 Astra Law，同时提供 26 个合作伙伴插件和零数据保留等隐私控制选项。

telegram · zaihuapd · 9月18日 01:49

**「法律 AI 的发展背景」** Astra for Law 是 OpenAI 在法律领域的一次重要探索，结合了大语言模型与专业领域知识库的检索增强技术。这一技术路线旨在解决传统大语言模型在法律推理和事实查找方面的局限性，尤其是在需要精确引用法律条文和案例的场景中。

**「对法律行业的影响」** Astra for Law 的推出可能提升律所在合同审查、法律研究和案件分析等方面的效率，但其实际性能仍需在真实工作场景中得到验证。值得注意的是，当前消息来源为 Telegram 帖子而非官方正式公告，部分技术细节和性能数据有待确认。

**标签**: `#AI`, `#LegalTech`, `#OpenAI`, `#GPT-6`, `#SoftwareEngineering`

---

<a id="item-tech-news-8"></a>
### [联合国携手谷歌打造 AI 可用的全球数据平台](https://techcrunch.com/2026/09/17/un-turns-to-google-to-make-its-global-data-ready-for-ai-agents/) ⭐️ 7.0/10

The UN partners with Google to launch an AI-ready global data platform replacing UNData, supporting natural language queries and MCP protocol, with 26 UN agencies committed and a goal to include 80% of datasets by 2027.

telegram · zaihuapd · 9月18日 04:50

**标签**: `#AI infrastructure`, `#data platforms`, `#United Nations`, `#Google`, `#open data`

---

<a id="item-tech-news-9"></a>
### [美国联邦公报网站撤下之前采用的 Qwen 搜索工具](https://www.reuters.com/legal/litigation/us-government-website-used-ai-search-tool-china-that-fbi-said-copied-anthropic-2026-09-17/) ⭐️ 7.0/10

The U.S. Federal Register removed a Qwen-powered search tool over concerns about using Chinese-developed AI in government systems, underscoring AI supply-chain and data-security risks.

telegram · zaihuapd · 9月18日 05:20

**标签**: `#AI governance`, `#supply chain security`, `#data security`, `#government technology`, `#Qwen`

---

<a id="item-tech-news-10"></a>
### [长鑫存储拟进军闪存市场](https://www.reuters.com/world/asia-pacific/chinas-cxmt-eyes-flash-memory-push-amid-global-shortage-firm-take-samsung-ymtc-2026-09-18/) ⭐️ 7.0/10

China&\#x27;s CXMT is reportedly planning to enter the NAND flash memory market, expanding beyond DRAM amid global chip shortages driven by AI demand.

telegram · zaihuapd · 9月18日 07:55

**标签**: `#semiconductors`, `#NAND flash`, `#CXMT`, `#DRAM`, `#AI hardware`

---

<a id="item-tech-news-11"></a>
### [Anthropic 设立湿实验室推进 AI 药物发现计划](https://www.reuters.com/world/anthropic-quietly-sets-up-biology-lab-it-ramps-ai-drug-program-2026-09-18/) ⭐️ 7.0/10

Anthropic 已在旧金山湾区悄然建立湿生物实验室，目标是让 Claude AI 指挥实验室机器人执行实验，以推进 AI 药物发现工作，尤其聚焦于罕见病研究。该实验室目前不直接参与临床试验，以避免与现有药企直接竞争。Anthropic 之前推出了 Claude Science 软件，并以约 4 亿美元收购了生物初创公司 Coefficient Bio。

telegram · zaihuapd · 9月18日 13:17

**「AI 在药物发现中的应用背景」** 近年来，大型语言模型在生物科学研究中被广泛应用于分子设计、蛋白质结构预测等领域。Anthropic 此前发布的 Claude Science 软件旨在将 AI 应用于科学研究领域，是其进军生物实验领域的延续。

**「对生物科技和药物开发的潜在影响」** 通过将 Claude AI 与实验室自动化设备结合，Anthropic 试图缩短传统药物研发流程中的实验环节时间，尤其在罕见病等市场较小但急需创新疗法的领域，这可能吉化相关研究的效率。

**标签**: `#AI drug discovery`, `#biotech`, `#robotics`, `#rare diseases`, `#Anthropic`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [系统一模型编程的两大技巧](https://seangoedecke.com/two-techniques-for-working-with-system-one-models/) ⭐️ 8.0/10

rss · Sean Goedecke · 9月18日 00:00

**「背景」** 作者介绍了“系统一模型”的概念，即仅输出决策（如多选题答案）的语言模型，相比传统 LLM 更快但灵活性更低。这些模型通过批量生成单 token 并使用结构化输出，本质上可以将任何 LLM 转化为快速分类器。编程时面临的核心挑战是：单次前向传播（约 200ms）计算量有限，难以从复杂环境状态中提取短期目标；同时面对大规模选择空间（如数千维基链接），模型难以做出有效判断。

**「方案」** 作者提出两项实用技巧。第一是分层目标（tiered goals）：设置多个时间尺度的目标循环——每 10 秒制定战略目标，每 5 秒制定战术子目标，每 1 秒分解为具体目标，最后在 100ms 内紧凑循环执行输入。这种方式模拟了常规 LLM 的推理过程，让模型能在有限计算下做出连贯决策。在 Doom 游戏中应用后，Qwen3-8B 不再滥按射击键，而是表现出更类人的玩法。第二是锦标赛采样（tournament sampling）：面对上千维基链接时，每次输入约 100 个链接进行选择，多轮筛选。这种方法克服了模型在大规模选择中评分不准的问题，成功找到从“棒球”到“太阳”的最优三跳路径。作者指出，普通 LLM 在相对判断上优于绝对评分，这正是 Jev 依赖置信度估计的局限所在。

**「启示」** 系统一模型作为通用快速分类器，能为实时 AI 系统提供可预测的推理时序，替代传统工具调用方式。分层目标与锦标赛采样这两种编程模式，为开发者在有限计算与大规模选择中构建高效决策系统提供了可复用的思路。

**标签**: `#system-one-models`, `#structured-output`, `#real-time-ai`, `#prompt-engineering`, `#llm-classification`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [Buffett 退出伯克希尔主席职位 儿子霍华德接任](https://www.cnbc.com/2026/09/18/buffett-stepping-down-as-berkshire-chairman.html) ⭐️ 8.0/10

96 岁的沃伦·巴菲特宣布退出伯克希尔哈撒韦主席职务，结束 61 年的领导时期，儿子霍华德·巴菲特接任该角色，公司估值约 1 万亿美元。

rss · CNBC Finance · 9月18日 12:04

**「背景」** 巴菲特自 1965 年起领导伯克希尔，去年 5 月已卸任 CEO 并由格雷格·阿贝接任，此次卸任主席职务为早已公布的继承计划的一部分，巴菲特将继续担任董事并担任名誉主席。

**「影响」** 这标志着伯克希尔哈撒韦这家全球最具影响力的投资公司进入后巴菲特时代，投资者将密切关注阿贝如何部署公司近 3655 亿美元的现金储备及是否能维持过往的投资业绩。

**标签**: `#Corporate governance`, `#Leadership transition`, `#Berkshire Hathaway`, `#Investment management`, `#Market impact`

---

<a id="item-finance-news-2"></a>
### [住建部：二手房交易比例升至 52%，房地产进入存量时代](https://www.peopleapp.com/column/30053168917-500007704534) ⭐️ 7.0/10

中国住房和城乡建设部表示，房地产市场供求关系发生重大变化，进入存量时代；二手房交易占比从 2020 年的 27%升至 2026 年前 8 个月的 52%。

telegram · zaihuapd · 9月18日 02:29

**「背景」** 存量时代意味着市场更多关注已有房屋的交易与出售，而非新增房屋的开发与销售。

**标签**: `#housing market`, `#real estate`, `#policy`, `#supply and demand`, `#secondary market`

---

<a id="item-finance-news-3"></a>
### [人民币兑美元升至四年高位 央行连续八日上调中间价](https://www.bloomberg.com/news/articles/2026-09-18/chinese-yuan-hits-strongest-level-since-2022-after-pboc-fixing) ⭐️ 7.0/10

人民币兑美元离岸汇率周四升至 6.6957，为 2022 年 7 月以来最强水平；中国央行连续第八个交易日上调中间价，为 2023 年以来最长连升，此间因习近平与特朗普即将举行会晤，贸易紧张预期成为关键催化因素。

telegram · zaihuapd · 9月18日 03:00

**「背景」** 央行每日上调中间价反映出对人民币汇率的支持态度，而特朗普与习近平的会晤预期正推升市场对贸易关系改善的乐观情绪。

**「影响」** 人民币连续第七个季度上涨，成为 2026 年亚洲表现最佳的货币之一，有助于降低中国出口企业的海外还款成本。

**标签**: `#Chinese yuan`, `#PBOC`, `#currency policy`, `#trade tensions`, `#foreign exchange`

---
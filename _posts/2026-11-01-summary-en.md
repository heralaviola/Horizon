---
layout: default
title: "Horizon Summary: 2026-11-01 (EN)"
date: 2026-11-01
lang: en
---

> From 29 items, 6 important content pieces were selected

---

**Technology News**

1. [Jepsen finds routine transactional failures in ParticleDB 1.1.4](#item-tech-news-1) ⭐️ 8.0/10
2. [Linux TCP use-after-free CVE-2026-98432 scored CVSS 9.8](#item-tech-news-2) ⭐️ 8.0/10
3. [OpenAI patched ChatGPT preview bug that enabled account takeover](#item-tech-news-3) ⭐️ 8.0/10
4. [HackerTube: a YouTube-style view of HN-recommended videos](#item-tech-news-4) ⭐️ 7.0/10

**Technology Blog**

1. [Fast and Slow Paths to Interesting Work](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**

1. [HKT agrees to halt US telecom services by 2027](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>

### [Jepsen finds routine transactional failures in ParticleDB 1.1.4](https://jepsen.io/analyses/particledb-1.1.4) ⭐️ 8.0/10

Jepsen&\#x27;s analysis of ParticleDB 1.1.4 reports that the database, despite claims of Postgres compatibility, routinely violated basic transactional guarantees. Testers observed lost committed writes, internal consistency violations, aborted reads \(G1a\), intermediate reads \(G1b\), and lost updates \(P4\); in an append workload, successfully appended values routinely disappeared from later reads of the same key. The write-up presents 96 issues, from crashes, deadlocks, and data loss to undeletable partially invisible rows, WHERE 4 = 5, dropped tables reappearing in distorted forms, confused columns, and strings turning into integers, and says a home-page claim of a TLA+ proof could not be assessed because no specification was available and it is unclear what, if anything, was proven of the system as built. Jepsen recommends that users halt further deployment, migrate to other databases as soon as possible, and consider checking or rebuilding database state from more reliable sources if available.

hackernews · aphyr · Oct 31, 13:39 · [Discussion](https://news.ycombinator.com/item?id=50316100)

**「Background」** Jepsen analyses check whether databases actually uphold the consistency guarantees they advertise. ParticleDB 1.1.4 claimed to be Postgres-compatible and to offer Snapshot Isolation with its occ-v3 and zero-copy-occ transaction modes, Serializability with serializable-ssi, and Strong Serializability with table-2pl.

**「Impact」** Users of ParticleDB should halt further deployment and migrate to another database as soon as possible, and should check or rebuild stored state from more reliable sources if those exist, because committed writes can disappear and claimed Postgres-compatible transactions do not hold. Jepsen’s tests of versions 1.1.4 through 1.1.18.11.rc-22 found full-ACID claims premature, so moving only to another release in that range is not a demonstrated fix.

**「Community discussion」** One commenter contrasted software that is correct by construction, where failures are generally local bugs, with software that is incorrect by construction and only appears to work through luck and workarounds, adding that AI can be effective at finding places to insert those workarounds. Another, quoting the advice to stop deploying ParticleDB, guessed that the errors came from vibecoding a database, which is an opinion the thread does not establish as fact.

<details><summary>References</summary>
<ul>
<li><a href="https://jepsen.io/analyses/particledb-1.1.4">Jepsen : ParticleDB 1 . 1 . 4</a></li>
<li><a href="https://jepsen.io/analyses/particledb-1.1.4">Jepsen: ParticleDB 1.1.4</a></li>

</ul>
</details>

**Tags**: `#distributed-systems`, `#databases`, `#jepsen`, `#transactional-consistency`, `#software-correctness`

---

<a id="item-tech-news-2"></a>

### [Linux TCP use-after-free CVE-2026-98432 scored CVSS 9.8](https://atlasum.net/blog/cve-2026-98432-linux-ipv4-tcp-uaf) ⭐️ 8.0/10

Hacker News is discussing CVE-2026-98432, a reported Linux kernel IPv4 TCP use-after-free given a CVSS score of 9.8. Commenters say it is a generic use-after-free rather than an MPTCP-only bug, and that a successful exploit requires multiple CPU cores to process packets carrying IP options. They also say exploitation over the internet is unlikely because most ISP routers drop packets with IP options, and that dropping those packets locally helps but is not a complete mitigation, according to Red Hat.

hackernews · oger · Oct 31, 19:16 · [Discussion](https://news.ycombinator.com/item?id=50319143)

**「Background」** A use-after-free is a memory bug in which code keeps using an object after that memory has been released. Red Hat describes CVE-2026-98432 as that class of race in the Linux kernel’s IPv4 TCP connection-request path, which a remote, unauthenticated attacker could trigger; AWS says the handshake-path issue affects kernel versions 4.4 and later when crafted IPv4 TCP packets reach an affected listener.

**「Who remains exposed」** Multi-core Linux servers on Ubuntu and RHEL remain exposed because those distributions have not yet shipped a fixed kernel. Dropping packets that carry IP options reduces risk but is not a complete mitigation, while single-core hosts and systems that pin packet processing to one core are not affected; exploitation over typical internet paths is considered unlikely where ISP routers already discard IP-options packets.

**「Community discussion」** Commenters report that Ubuntu and Red Hat security pages still show no patches and question why those server-focused distributions have not shipped a fix. Another argues that AWS customers using services such as Web Application Firewall, Application Load Balancer, Classic Load Balancer, TLS listeners on Network Load Balancer, CloudFront, or API Gateway are less directly exposed when they do not receive untrusted TCP connections themselves, while a separate comment notes that BSD, macOS, and Windows are not affected.

<details><summary>References</summary>
<ul>
<li><a href="https://aws.amazon.com/security/security-bulletins/2026-160-aws/">CVE-2026-98432 - Linux kernel IPv4 TCP use-after-free ...</a></li>
<li><a href="https://access.redhat.com/security/vulnerabilities/RHSB-2026-016">RHSB-2026-016 Use-after-free - kernel IPv4 (CVE-2026-98432 ...</a></li>
<li><a href="https://atlasum.net/blog/cve-2026-98432-linux-ipv4-tcp-uaf">Linux &#x27;s October 2026 TCP Use-After-Free: CVE - 2026 - 98432 — Atlas</a></li>

</ul>
</details>

**Tags**: `#linux-kernel`, `#security`, `#cve`, `#tcp`, `#vulnerability`

---

<a id="item-tech-news-3"></a>

### [OpenAI patched ChatGPT preview bug that enabled account takeover](https://simonwillison.net/2026/Oct/31/how-we-took-over-chatgpt-accounts/) ⭐️ 8.0/10

Parameter Labs reported a sandbox escape in ChatGPT HTML previews, the sandboxed iframes used for interactive custom HTML and previously called Canvas. A malicious ChatGPT share link, if opened by another signed-in user, could access that user&\#x27;s private data or take actions on their behalf. OpenAI closed the issue and paid a $5,000 bug bounty, which Simon Willison, summarizing the report, called low for a vulnerability this serious.

rss · Simon Willison · Oct 31, 23:15

**「Background」** ChatGPT&\#x27;s HTML preview feature, previously called Canvas, turns a code block into a small webpage and displays it in a sandboxed iframe on a different web address so arbitrary code cannot reach OpenAI APIs or private user data. Graph support in the parent page uses MathLive, a web component for editing and displaying typeset math formulas that includes a virtual keyboard the parent page can open via postMessage.

**「Share-link exposure」** Before the fix, a signed-in ChatGPT user who opened a malicious share link could have private data read through ChatGPT APIs and actions taken on their account. Parameter Labs reports that OpenAI has fixed the issue; the Preview sandbox itself held, and the gap was a separate main-page component that accepted instructions from it.

**「Community discussion」** On Hacker News, commenters called the $5,000 bounty too small for an account-takeover bug and worried it could discourage future reports; one noted the attack required the victim to open a link and said OpenAI had confirmed both frontends rejected the reported messages and resolved the issue. Another reader said the underlying writeup was hard to follow and did not clearly separate how the defenses were meant to work from how they were bypassed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.parameter.ai/labs/we-found-a-gap-at-openai">Do the Math : How We Took Over ChatGPT Accounts - Parameter</a></li>
<li><a href="https://mathlive.io/mathfield/">Introduction · MathLive</a></li>
<li><a href="https://www.parameter.ai/labs/we-found-a-gap-at-openai">Do the Math: How We Took Over ChatGPT Accounts - Parameter</a></li>

</ul>
</details>

**Tags**: `#chatgpt`, `#security`, `#sandbox-escape`, `#account-takeover`, `#web-security`

---

<a id="item-tech-news-4"></a>

### [HackerTube: a YouTube-style view of HN-recommended videos](https://karpathy.bearblog.dev/hacker-tube/) ⭐️ 7.0/10

Andrej Karpathy published HackerTube at hackertube.org, a YouTube-style interface for browsing videos recommended in Hacker News comments. The catalog covers 6,454 videos drawn from 39,834 comments since 2007. It is a browsing layer over those existing links, not a new recommendation model or an independently measured ranking result.

hackernews · karpathy · Oct 31, 19:56 · [Discussion](https://news.ycombinator.com/item?id=50319510)

**「Background」** Since 2007, Hacker News comment threads have included reader recommendations of videos alongside ordinary link discussion. HackerTube is a browsing interface over that existing comment record, not a new video host or a separately trained recommender.

**「Discussion」** Several commenters argued that recommendations from people they trust are more appealing than engagement-optimized feeds: phtrivier compared the site to a subscriptions tab, murm said browsing felt less like being baited into traps, and zmmmmm said interest-matched feeds often fail people looking for something new. mrshu also pointed to a later process note in which Karpathy described building the site by directing Claude Code—Opus 5.5 on medium effort—rather than writing code or running commands himself.

**Tags**: `#content-curation`, `#recommendation-systems`, `#hacker-news`, `#youtube`, `#karpathy`

---

## Technology Blog

<a id="item-tech-blog-1"></a>

### [Fast and Slow Paths to Interesting Work](https://seangoedecke.com/how-to-get-assigned-interesting-work/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 1, 00:00

**「Background」** Engineers tell Sean Goedecke they stay sidelined while one trusted colleague keeps the visible work, even after a manager agrees someone else should lead. He treats that gap as incentives, not as a breakdown of a formal round-robin assignment.

**「Solution」** He argues managers will keep giving high-profile work to a known shipper, because failure there damages their own standing fastest, and manager tenures of only a couple of years—mainly his observation, not a strong source—make that vicious cycle rational even as colleagues get less experienced. The slow ratchet is shipping small, visible, low-risk work, then only slightly riskier tasks, while avoiding mistakes that mark you unreliable, so incentives already align instead of fairness or career-development arguments; months or years of that can still be erased by failure, a manager&\#x27;s exit, or a change in the work. Faster routes, which he calls dangerous, are a skip-level directing the assignment and shifting blame, side projects needing no assignment, or peers on a healthy team who judge quality faster than results-focused managers and vouch for you—with catches of detected lobbying that sends skip-level trust back to the slow path, wasted time and annoyance, and teams that miss or undermine strong engineers.

**「Takeaway」** Goedecke concludes that being left off interesting work is an incentive problem, not a personal slight, and that companies are supposed to make money rather than be fair. Pleading that in one-on-ones is weaker than making the assignment look like it already serves the manager.

**Tags**: `#engineering careers`, `#tech management`, `#workplace incentives`, `#reputation`, `#project assignment`

---

## Financial News

<a id="item-finance-news-1"></a>

### [HKT agrees to halt US telecom services by 2027](https://www.cnbc.com/2026/10/31/hong-kong-telecom-firm-agrees-to-halt-us-operations-under-pressure.html) ⭐️ 7.0/10

Hong Kong telecom firm HKT agreed under pressure from the US Federal Communications Commission to file a shutdown application within 30 days and stop telecom services to and in the United States by September 1, 2027, ending a case the FCC opened in October 2025 to revoke its operating authorization over national security and alleged links to China Unicom.

telegram · zaihuapd · Oct 31, 10:22

**「Background」** In October 2025, the US Federal Communications Commission \(FCC\), which authorizes telecom operators, opened a case to revoke HKT&\#x27;s US operating authorization over national-security concerns and links to China Unicom; it has previously barred China Mobile, China Telecom and China Unicom from providing international telecom services to the United States, citing broad national-security concerns.

<details><summary>References</summary>
<ul>
<li><a href="https://telecom.economictimes.indiatimes.com/news/industry/hong-kong-telecom-company-agrees-to-halt-us-operations-under-pressure/135384212">HKT Telecom: HKT Halts US Operations Amid FCC Pressure Over National ...</a></li>

</ul>
</details>

**Tags**: `#HKT`, `#FCC`, `#telecom regulation`, `#national security`, `#market exit`

---
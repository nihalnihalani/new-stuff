# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-06

## X Brief: Fri 6 Nov 2026, 9 AM (5 Nov 09:00 to 6 Nov 09:00 IST)

**I checked 15 X accounts (76 posts) and 6 searches (~188 results), plus GitHub trending (daily, Python, TypeScript, Rust, Jupyter), Hugging Face, Hacker News / Show HN / Launch HN, r/LocalLLaMA (via search — Reddit JSON blocked), The Decoder, TechCrunch, The Verge, Latent Space, TLDR AI, Ben's Bites, the OpenAI, Anthropic, Google, Meta, Mistral, Microsoft, Moonshot/Kimi, Baidu ERNIE and Thinking Machines blogs, Artificial Analysis, Economic Times/Reuters, Devpost, Unstop, lablab.ai, WeMakeDevs, Vultr Community and public LinkedIn search. I kept 12 news items, 4 models, 15 repos and projects, and 10 open hackathons.** All times are IST.

- **OpenAI shipped GPT-6 Cyber** — Critical under the Preparedness Framework; ExploitGym **48.5%** (was 32.1%); **81** novel high-severity Firefox findings; Daybreak Red gated for approved customers.
- **Two open-base drops:** Baidu **ERNIE-5.5-Flash-Base** weights (280B/14B MoE, pretrain-only) and Thinking Machines **Inkling 2 Small** (594B/17B, AA Index **31**; Apache-2.0 weights planned **next week**).
- **For students:** **Nuvolos Fellowship closes today (6 Nov).** Flip the Switch closes **tomorrow 7 Nov at 23:59 IST**. Vultr Agent Rush ends ~**8 Nov**, Gnani closes **10 Nov at 23:59**. Festive Hacks is **in-person 25 Nov at BIEC Bengaluru** — not the online 16–21 Nov window yesterday listed.

### The one that matters most
**OpenAI launched GPT-6 Cyber**, a cybersecurity-specialized model classified **Critical** under its Preparedness Framework (up from High for GPT-5.6 Cyber). Maker-reported ExploitGym is **48.5%** vs **32.1%** for GPT-5.6 Cyber; OpenAI also cites **81** novel high-severity Firefox findings and the previously disclosed **948** Linux LPE pipeline. Access starts via API/Codex for approved **Daybreak Red** customers; Daybreak Blue for verified defenders is expanding; a Cyber at the Frontier livestream is **12 Nov at 10am PT**. For a student builder this is not a free API to poke at — it is the moment cyber-agent capability becomes a gated product surface. Sandbox every agent that can run tools, keep scopes authorized, and treat India fintech/payment APIs with extra care (see Crafty Falcon below). Pair the lesson with local agent-audit tooling like **Stroq** rather than chasing Critical-tier access you will not get. [OpenAI](https://openai.com/index/introducing-gpt-6-cyber) · 5 Nov · [post](https://x.com/OpenAI/status/2118390190246879554) · 22:39, 5 Nov · [The Verge](https://www.theverge.com/ai-artificial-intelligence/1027599/openai-gpt-6-cyber-launch) · 22:30, 5 Nov

### AI news

#### Labs and models
- **OpenAI GPT-6 Cyber** lands as a Critical cyber model with Daybreak Red access for approved customers and a Nov 12 livestream for more cyber announcements. Capability and dual-use governance are shipping as the same product. [OpenAI](https://openai.com/index/introducing-gpt-6-cyber) · 5 Nov · [Daybreak post](https://x.com/OpenAI/status/2118390192356700383) · 22:39, 5 Nov · [livestream post](https://x.com/OpenAI/status/2118390195099930906) · 22:39, 5 Nov
- **Google Gemini Omni 1.2 Flash** is GA on the Gemini API / Cloud: native video up to **15 seconds** (was 10s), multi-turn conversational editing, and a **30%** price cut to **$0.07/s** at 720p. Hackathon demo video without a separate video stack just got longer and cheaper. [Google](https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemini-omni-1-2-flash/) · 5 Nov · [DeepMind RT](https://x.com/GoogleDeepMind/status/2118392265961869549) · 22:47, 5 Nov
- **Baidu released ERNIE-5.5-Flash-Base** open weights: sparse MoE **280B total / 14B active**, pretrained on **33.5T** tokens, inference up to **1M** context, deliberately **pre-training-only** for community SFT/RL. Custom license excludes **EU/UK/KR** and needs written auth above ~**$50M** related revenue — read the geo clauses before you fine-tune for a product. [Baidu](https://ernie.baidu.com/release/ernie-5-5-flash-base/) · [HF](https://huggingface.co/baidu/ERNIE-5.5-Flash-Base) · 5 Nov · [The Decoder](https://the-decoder.com/baidu-releases-ernie-5-5-flash-base-with-280-billion-parameters-as-an-open-source-foundation-model/) · 5 Nov
- **Thinking Machines Lab introduced Inkling 2 Small**: MoE **594B / 17B active**, vision + variable effort, AA Intelligence Index **31**. On Tinker with closed weights now; lab says **Apache-2.0 weights next week** after safety testing. Watch the drop if you self-host. [Thinking Machines](https://thinkingmachines.ai/news/inkling-2-small/) · 5 Nov · [AA changelog](https://artificialanalysis.ai/changelog)

#### Products and APIs
- **Anthropic shipped Personal Finance in Claude** (US beta for Pro/Max/Ultra): Plaid bank/card connect, read-only balances + up to 2 years of transactions; Claude cannot move money; hub chats not used for training. Useful privacy/product case study — and a reminder it is US paid tiers only. [Claude](https://claude.com/resources/articles/introducing-personal-finance-in-claude) · [TechCrunch](https://techcrunch.com/2026/11/05/claude-can-now-analyze-your-spending-with-its-new-personal-finance-tool/) · 23:30, 5 Nov
- **Meta rolled out Muse Voice + expressive avatars** to all US Muse app users (mobile, web, Mac): realtime avatar reacts while listening/speaking. Consumer avatar-agent UX is now a mainstream surface. [Meta](https://about.fb.com/news/2026/11/introducing-muse-ai-voice-expressive-avatars/) · 5 Nov · [post](https://x.com/AIatMeta/status/2118412135340572850) · 00:06, 6 Nov · [TechCrunch](https://techcrunch.com/2026/11/05/meta-says-us-users-can-now-video-chat-with-their-muse-ai-avatar/) · 00:48, 6 Nov
- **Perplexity launched Teammates** — always-on work agents on top of Perplexity Computer (Slack + per-Teammate threads); requires **$200/month Max**. Another teammate product next to Dots/Duet — price is the student differentiator. [The Verge](https://www.theverge.com/ai-artificial-intelligence/1028302/perplexity-teammates-ai-agents-work) · 03:56, 6 Nov
- **Mistral expanded Studio** with managed agents, workflows, and enterprise apps for deploying Large 4 (“Le Chonk”) on cloud / VPC / on-prem. Enterprise agent-platform competition heats up for sovereign/on-prem tracks. [Mistral](https://mistral.ai/news/build-with-studio/) · 5 Nov · [post](https://x.com/MistralAI/status/2118370229466153299) · 21:19, 5 Nov
- **Moonshot launched Kimi Hosted Agents** (“Harness as a Service”): managed sandboxes, network controls, audit logs, **140+** Skills / **30+** plugins, Inference Hook for enterprise filters. Cuts the months of harness plumbing students usually rebuild. [Kimi](https://www.kimi.com/news/kimi-hosted-agents) · 5 Nov
- **Microsoft Foundry Local** lets you run **Qwen3.8-27B** on-device via Foundry Local CLI **≥0.13.0** and connect to **GitHub Copilot BYOK** (~**18 GB** INT4 for **24 GB** VRAM, 64K ctx). Privacy/offline coding loop without cloud token burn — if you have the GPU. [Microsoft](https://devblogs.microsoft.com/foundry/foundry-local-agentic-coding-qwen3-8-27b/) · 5 Nov

#### Funding and policy
- **OpenAI published a National Community Compact + Compute Campus Policy Blueprint** for future owned campuses: pay own energy/infra costs, water plans, no broad NDAs with public officials, local jobs/reporting — so residential ratepayers are not stuck with stranded costs. Macro context for “who pays for AI power.” [OpenAI](https://openai.com/index/setting-new-standard-responsible-ai-infrastructure/) · 5 Nov

#### India
- **CERT-In named campaign “Crafty Falcon”** targeting NBFCs, fintechs and crypto exchanges with AI-assisted break-ins “at machine speed.” Advisory names tools **ARTEX, PentAGI, Cairn, CyberStrikeAI**; attackers abuse victims’ own payment/disbursement APIs around low-monitoring windows. Direct follow-on to yesterday’s I4C theme — critical if you ship India fintech agents. [Economic Times / Reuters](https://m.economictimes.com/tech/artificial-intelligence/india-flags-chinese-linked-ai-tools-in-hacking-campaign-against-financial-firms/amp_articleshow/135566096.cms) · 14:13, 5 Nov

### New models and weights

| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| ERNIE-5.5-Flash-Base | Baidu | 280B total / 14B active MoE; 128K train / 1M infer | ERNIE 5.5 Flash Base Model License v1.0 (not Apache; no EU/UK/KR; >~$50M revenue needs auth) | Clean pretrain-only base for SFT/RL; FP8+BF16 on HF | [blog](https://ernie.baidu.com/release/ernie-5-5-flash-base/) · [HF](https://huggingface.co/baidu/ERNIE-5.5-Flash-Base) |
| Inkling 2 Small | Thinking Machines Lab | 594B total / 17B active MoE; vision | Closed on Tinker now; **Apache-2.0 weights planned next week** after safety testing | AA Index 31 — would be top non-China open-weights per AA if/when weights land | [blog](https://thinkingmachines.ai/news/inkling-2-small/) |
| GPT-6 Cyber | OpenAI | Proprietary cyber model | Daybreak Red gated API/Codex | Critical cyber classification; ExploitGym 48.5% (maker-reported) | [OpenAI](https://openai.com/index/introducing-gpt-6-cyber) |
| Gemini Omni 1.2 Flash | Google DeepMind | Video gen/edit model | Proprietary API | 15s clips, −30% price, conversational edits | [Google](https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemini-omni-1-2-flash/) |

### Benchmarks and leaderboards
- **DesignArena:** Inkling 2 Small is **4th overall**, **1st open weights** (Elo **1376**); DesignArena says ~**15×** cheaper than Kimi K3. [post](https://x.com/DesignArena/status/2118490433420685380) · 05:17, 6 Nov
- **Artificial Analysis 5 Nov:** Inkling 2 Small Intelligence Index **31** (highest open-weights-outside-China *pending* weight release). [AA changelog](https://artificialanalysis.ai/changelog)
- **APEX-Agents:** Hy4 (Tencent Hunyuan) is **#1 open-weights** at **77.6%** Pass@1 (Mercor). [Mercor](https://x.com/mercor/status/2118420063242039721) · 00:37, 6 Nov
- **FLUX 3 Image Klein** (BFL, 5.6B): **#2** open weights on AA-Image-T2I v2.1, **#3** on Editing. [ArtificialAnlys](https://x.com/ArtificialAnlys/status/2118484199552561609) · 04:52, 6 Nov
- **Maker-reported GPT-6 Cyber numbers** (treat as maker-reported): ExploitGym **48.5%** (GPT-5.6 Cyber **32.1%**); web pentest recall **40.3%** vs GPT-6 Astra **32.0%**; RemoteExploitBench **95%** completion vs Astra/Daybreak Blue **100%** refuse. [OpenAI](https://openai.com/index/introducing-gpt-6-cyber)

### Trending repos and projects
- [google/skills](https://github.com/google/skills) is Google's public Agent Skills pack for Google products so coding agents can follow Drive/Workspace/Cloud-aware workflows. Drop these into Claude Code, Cursor or Gemini setups when an agent needs Google-product steps. Python, +211 today (22,437).
- [microsoft/VibeVoice](https://github.com/microsoft/VibeVoice) is Microsoft's open-source frontier voice AI stack trending hard today. Prototype a local/self-hosted voice agent or hackathon voice UI on the published code. Python, +223 today (56,067).
- [ConardLi/garden-skills](https://github.com/ConardLi/garden-skills) is an open Agent Skills collection for web design, knowledge retrieval, image generation and related workflows. Pick a pack so a coding agent gets design/retrieval/image tools without writing prompts from scratch. JavaScript, +175 today (14,206).
- [sandbox-quantum/switch](https://github.com/sandbox-quantum/switch) is open-source AI teammates that run in Slack, Teams, Discord, Telegram and Mattermost; self-host with any model provider. Stand up a chat-native coworker for Flip the Switch (closes tomorrow) with your own keys. Python, +182 today (3,955).
- [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) is an agent skill that pushes coding agents to think like a lazy senior — prefer deleting and simplifying over writing more code. Attach it to Claude Code/Cursor so agents default to smaller diffs. JavaScript, +5,069 over 7d (185,302).
- [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) is Nous Research's long-running personal/coding agent harness (“the agent that grows with you”). Fork it as a self-hosted runtime that keeps memory and tools across sessions. Python, +2,357 over 7d (260,916).
- [Niko1221/Strata](https://github.com/Niko1221/Strata) is a local C++ inference engine aimed at running Qwen3.8-Flash-Next on consumer hardware with one-click Windows/Linux install and OpenAI/Anthropic-compatible localhost APIs. Use it as a local backend when you want a large MoE-class model on one consumer GPU box. C++, 40,641.
- [southleft/figma-console-mcp](https://github.com/southleft/figma-console-mcp) is an MCP server that treats your design system as an API — connect agents to Figma for extraction, creation and debugging. Give a design-aware coding agent Figma read/write tools so UI builds stay on-token. TypeScript, +179 today (3,145).
- [AGGIB/Stroq](https://github.com/AGGIB/Stroq) is a local audit/security tool for AI coding agents: finds secrets in sessions and installs hooks that trace risky commands back to the content that caused them (Claude Code, Codex, Cursor). Add Stroq hooks to a shared agent profile for secret scanning and command provenance — especially timely next to GPT-6 Cyber and Crafty Falcon. TypeScript, 107. [Show HN](https://news.ycombinator.com/item?id=50380704)
- [rivet-dev/rivet](https://github.com/rivet-dev/rivet) is an orchestrator for agentic workloads (Launch HN, YC W23): scale and orchestrate agents on S3 with a high-density runtime. Schedule many agent workers when a single laptop process is not enough for a multi-agent demo. Rust, 6,667. [Launch HN](https://news.ycombinator.com/item?id=50381687)
- [Qwen/Qwen3.8-27B](https://huggingface.co/Qwen/Qwen3.8-27B) is Qwen3.8 27B multimodal (image-text-to-text) near the top of HF trending. Wire it into a vision+chat demo or local OpenAI-compatible server; pairs with Microsoft Foundry Local's on-device path. Model weights, 19,215 HF likes (~8.04M downloads).
- [Lordog/dive-into-llms](https://github.com/Lordog/dive-into-llms) is a hands-on “Dive into LLMs” programming tutorial series (notebooks). Work through chapters as a structured path from basics to agent/RAG projects, or fork labs for a workshop. Jupyter Notebook, +217 today (59,392).
- [NVIDIA/Model-Optimizer](https://github.com/NVIDIA/Model-Optimizer) is NVIDIA's unified library for SOTA model optimization: quantization, distillation, pruning, NAS, speculative decoding. Quantize or distill an open model for a smaller deploy target before a hackathon demo. Python, +20 today (5,540).
- [pydantic/monty](https://github.com/pydantic/monty) is a secure Python sandbox written in Rust for safely running code produced by AI agents. Sandbox tool-calling agents that generate Python so they execute without full host privileges. Rust, +10 today (8,841).
- [Generated-Computers/Locals](https://github.com/Generated-Computers/Locals) runs many AI agents at once on a Mac, claiming up to ~3× faster multi-agent local runs. Parallelize several coding/research agents on one Mac during a hackathon without spinning VMs. Python, +738 over 7d (1,208).

### Hackathons
- **Flip the Switch** (WeMakeDevs × Switch) — submissions close **TOMORROW, 7 Nov at 23:59 IST** (confirmed). Connect a coding agent to Slack/Discord/Teams/Telegram via Switch; online; solo or up to 4; **$10,000** prize pool. Hacking began 4 Nov. [event](https://www.wemakedevs.org/hackathons/switch) · [schedule](https://www.wemakedevs.org/hackathons/switch/schedule) · [post](https://x.com/WeMakeDevs/status/2118215679073792241) · 11:05, 5 Nov
- **Vultr: Agent Rush** (lablab.ai × Vultr): hybrid online build **3–8 Nov**; optional on-site Salt Lake City 8 Nov. Teams 1–6; **$9,000** cash + **$5,000** Vultr credits; every participant gets **$200 Vultr credits**. Exact end clock still unconfirmed — confirm before cutting it fine. [event](https://lablab.ai/ai-hackathons/vultr-hackathon)
- **CodeNova India 2026** (WeCodeCoders, Unstop): online agentic-AI for UG/PG, teams 1–6. Top three get ₹30,000, paid internships and incubation; every participant gets a .xyz domain, **$100 Inkloom** and **$500 Adaption** AI credits. Registration / Round 1 tied to **10 Nov** (clock soft on Unstop today). Event 11–22 Nov. [event](https://unstop.com/hackathons/codenova-india-2026-national-hackathon-wecodecoders-1783775)
- **Great Indian AI Internship Challenge** (Gnani AI): up to **100 paid 6-month internships** (up to ₹1 lakh/month), ₹5 lakh in awards, **5,000 programme credits** per registration. Online; India students 18+; solo or team of 2. Deadline **10 Nov at 23:59 IST** (confirmed). [event](https://www.gnani.ai/internship)
- **DataNova 2026 Global Data-thon** (Devpost): online, students only, teams required, $1,750 prizes. Deadline **11 Nov at 03:30 IST** (confirmed). [event](https://datanova-2026-global-data-thon.devpost.com/)
- **PayPal AI Hackathon** (Devpost): online global; must use PayPal + AI; **$67,500+** prizes. Deadline **13 Nov at 01:30 IST** (confirmed). [event](https://paypalaihackathon.devpost.com/)
- **Agentic AI Hackathon** (Product Space, Unstop): online 14–15 Nov, solo or pairs, prizes worth ₹1,00,000. Registration through **14 Nov ~11:00 IST**; project submission **15 Nov 23:59** (Indian organizer — treat as IST). [event](https://unstop.com/hackathons/agentic-ai-hackathon-product-space-1792269)
- **DSH Hacks V2** (Devpost, AI × Healthcare): online, students 13+, credits stack (Momen, Adaption Labs, etc.). Deadline **15 Nov at 13:15 IST** (confirmed). [event](https://dsh-hacks-v2.devpost.com/)
- **UGREEN Hackathon 2026 on AI NAS** (Devpost): **$46,000** cash; Round 1 online (no NAS needed). Round 1 deadline **16 Nov at 13:15 IST** (confirmed). [event](https://ugreenhackathon.devpost.com/)
- **Festive Hacks** (WeMakeDevs × WeAreDevelopers) — **CORRECTION vs yesterday:** this is **in-person** on the conference floor **25 Nov 2026, 09:00–18:00 IST at BIEC Bengaluru**, not an online build 16–21 Nov. Teams 1–4; apply on Luma; only accepted hackers compete; submissions close **25 Nov 18:00 IST** (rules). 1st prize is a fully sponsored VIP trip to Berlin; 2nd ₹2,00,000; 3rd ₹1,00,000. Travel/stay not covered. [event](https://www.wemakedevs.org/hackathons/festivehacks) · [rules](https://www.wemakedevs.org/hackathons/festivehacks/rules)
- **Winners / notes:**
  - **Qloo Agentic Hackathon** ended; Devpost still says “Winners announced soon” (Top 3 finalists were due on This Week in Startups 5 Nov). Named winners/builds **not** on the page yet — do not invent. [Qloo](https://qloo.devpost.com/)
  - **ali_uraish** says 1st at **Haunted Hacks 2026 at YC** with ActorRelay (multi-agent system for industrial equipment) — X-only confirmation. [post](https://x.com/ali_uraish/status/2118512092529783228) · 06:43, 6 Nov

### Student perks and credits
- **URGENT — Nuvolos Fellowship 2026:** PhD/postdoc/RSE; up to **$5,000** Nuvolos cloud credits + platform access. **Applications close today, 6 Nov 2026**; decisions by 27 Nov. [Nuvolos](https://nuvolos.com/fellowship-programme)
- **Gnani** (see Hackathons): 5,000 programme credits per registration + paid internship path; closes **10 Nov at 23:59 IST**.
- **Vultr Agent Rush:** **$200 Vultr credits** each participant; online window ends ~**8 Nov**.
- **CodeNova:** $100 Inkloom + $500 Adaption for all participants (reg ~10 Nov).
- **OpenAI Codex for Students $100:** ChatGPT credits for Codex — **US/Canada students only**, not eligible for India. [OpenAI students](https://developers.openai.com/community/students)
- **Azure for Students:** **$100 Azure credit** + free quotas (path to Azure OpenAI / Foundry); no credit card; full-time university students. [Azure students](https://azure.microsoft.com/en-us/free/students)
- **GitHub Student Developer Pack:** Copilot Student, Codespaces Pro, JetBrains, MongoDB Atlas, Notion Education+AI, etc. [pack](https://education.github.com/pack/)
- **Nebius research grants:** rolling GPU cloud + Token Factory credits for postgraduate researchers. [Nebius](https://nebius.com/nebius-research-grants)

### Grok Bots
- **OpenMausBot** (open-source local-first Grok Bot alternative) passed **13.5k** GitHub stars. [post](https://x.com/Daniel24xiang/status/2118544455410311188) · 08:52, 6 Nov
- **Two free Grok Bot templates:** Griller (pokes product ideas) and Drafter. [post](https://x.com/eaxmmt/status/2118534404481970607) · 08:12, 6 Nov
- **Usage commentary:** one builder says the **$100/mo** plan hits **100%** usage in two days and needs plan-stage improvements. [post](https://x.com/pablothethinker/status/2118535637255016943) · 08:17, 6 Nov
- **Agent-team framing:** a post quotes Musk that 99% use GrokBot like Google while SpaceXAI engineers run teams of **50+** GrokBot agents. [post](https://x.com/ajitcodes/status/2118538872095162701) · 08:30, 6 Nov
- **Chief-of-Staff pattern:** ryanthawks has been running a Grok Bot Chief of Staff + specialists with Claude/Gemini routing for months. [post](https://x.com/ryanthawks/status/2118528956576244182) · 07:50, 6 Nov
- **GrokBotCEO** reports **42** Grok Bots, **7** live sites, **89,887** lines merged across **118** PRs. [post](https://x.com/GrokBotCEO/status/2118545211676840317) · 08:55, 6 Nov

### Build idea of the day
For **Flip the Switch** (closes **tomorrow, 7 Nov at 23:59 IST**), ship a Slack/Discord teammate on **sandbox-quantum/switch** itself — the same open Switch stack the hackathon is built around. Wire **ponytail** so the agent prefers deleting over bloating diffs, add **Stroq** hooks so secrets and risky commands get traced before the bot posts, and sandbox any Python the agent emits with **pydantic/monty**. If you need a local multimodal brain without burning Max-tier Teammates money, point the teammate at **Qwen3.8-27B** (or wait for Inkling 2 Small's Apache weights next week). Judges see an approval-gated coworker with real provenance, not another firehose of agent spam — and you stay inside today's open/local stack.

### What the field is arguing about
- **Aligned cyber agents at Critical:** GPT-6 Cyber's ExploitGym jump + Daybreak Red gating vs dual-use fears — same week as India's **Crafty Falcon** AI-tool attacks on fintech APIs.
- **Always-on work agents, different price tags:** Perplexity Teammates at **$200 Max** vs Mistral Studio / Kimi Hosted Agents / Muse Voice — who owns the harness, and can students afford the seat?
- **Open bases for post-training:** ERNIE base (weights today, geo-restricted license) vs Inkling 2 Small (Apache weights “next week”) — the race is as much about trainable bases as chat leaderboards.
- **AI-for-science adoption gap:** Anthropic's **207k-session** study — models used where RL-friendly (data analysis/writing), underused for ideation/physical work. [Anthropic](https://www.anthropic.com/research/how-researchers-use-claude) · 5 Nov
- **Who pays for AI power / community consent:** OpenAI's campus compact vs anti-datacenter ballot backlash.

### Worth reading in full
1. [OpenAI — Introducing GPT-6 Cyber](https://openai.com/index/introducing-gpt-6-cyber) — Critical classification, Daybreak access model, maker eval tables; rare transparency on cyber-agent productization.
2. [Baidu — ERNIE 5.5 Flash Base](https://ernie.baidu.com/release/ernie-5-5-flash-base/) — architecture (HCA/MLA, Multi-Router Latent MoE) + license geography you must read before fine-tuning.
3. [Thinking Machines — Inkling 2 Small](https://thinkingmachines.ai/news/inkling-2-small/) — training recipe, alignment mitigations, Apache weight-release plan.
4. [Anthropic — How researchers use Claude](https://www.anthropic.com/research/how-researchers-use-claude) — 207k-session Economic Index science report; acceleration scenarios by field.
5. [OpenAI — Setting a new standard for responsible AI infrastructure](https://openai.com/index/setting-new-standard-responsible-ai-infrastructure/) — Community Compact / campus blueprint; who pays for power and water.

### Quiet accounts / couldn't open
- **@AnthropicAI** and **@karpathy** posted nothing in the window (API result_count=0). @simonw only replied (UCSD-library datacenter joke). @GoogleDeepMind's in-window item was an RT of Gemini Omni 1.2 Flash.
- **DoraHacks** detail pages hit AWS WAF/CAPTCHA (Mozilla Otari left as secondary-only; skipped from open list). **Reddit** JSON / old.reddit blocked; no LocalLLaMA items included. **Product Hunt** returned HTTP 403 (used productlist.info / hunted.space for AgentKit #1 and Rerun #2 on 5 Nov — not promoted into the top-15 repos list).
- **Import AI** had no public Nov 5–6 edition (stuck on #479 / 2 Nov). **xAI / DeepSeek / Qwen** official blogs: no confirmed in-window release pages. **Unstop** Orbix/CodeNova clock times remain soft (JS shells). **Vultr Agent Rush** exact 8 Nov end clock still unconfirmed. **Qloo** winner names not on Devpost yet. **Festive Hacks** Luma application cutoff time not printed on overview/rules.
- Hugging Face blog livestreams (quantization Tue; ML Intern Slack bot) and @chinchoukou's skills-repo explainers were fetched but mostly overlap already-trending repos above.

## Archive

- [2026-11-06](briefs/2026-11-06.md)
- [2026-11-05](briefs/2026-11-05.md)
- [2026-11-04](briefs/2026-11-04.md)
- [2026-11-03](briefs/2026-11-03.md)
- [2026-11-02](briefs/2026-11-02.md)
- [2026-11-01](briefs/2026-11-01.md)
- [2026-10-31](briefs/2026-10-31.md)
- [2026-10-30](briefs/2026-10-30.md)
- [2026-10-29](briefs/2026-10-29.md)
- [2026-10-28](briefs/2026-10-28.md)
- [2026-10-27](briefs/2026-10-27.md)
- [2026-10-26](briefs/2026-10-26.md)
- [2026-10-25](briefs/2026-10-25.md)
- [2026-10-24 week](briefs/2026-10-24-week.md)
- [2026-10-24 sweep](briefs/2026-10-24-sweep.md)
- [2026-10-24 0900](briefs/2026-10-24-0900.md)
- [2026-10-24](briefs/2026-10-24.md)

## Tracking files

- [watchlist.csv](watchlist.csv) — X accounts and searches being tracked for the briefs
- [seen_log.csv](seen_log.csv) — every link already reported, to avoid duplicates

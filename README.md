# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-07

## X Brief: Sat 7 Nov 2026, 9 AM (6 Nov 09:00 to 7 Nov 09:00 IST)

**I checked 15 X accounts (49 posts) and 6 searches (~214 results), plus GitHub trending (daily, weekly, Python, TypeScript, Rust, Go, Jupyter), Hugging Face trending/papers, Hacker News / Show HN, Product Hunt (via StartupCorners Nov 6 digest — PH homepage thin), The Verge, TechCrunch, WIRED, The Register, Business Insider, Artificial Analysis not rechecked for a new Inkling move, OpenAI / Anthropic / Meta / Mistral / DeepMind posts and blogs, Devpost, Unstop/WeCodeCoders, lablab/Vultr Community, WeMakeDevs, Homingo, and public LinkedIn only as secondary search. Reddit LocalLLaMA/ML JSON stayed 403.** Kept 10 news items, 2 models, 15 repos/projects, and 10 open hackathons. All times are IST.

- **Nous released Arete-27B** — Apache-2.0 open weights on Qwen3.8-27B; propaganda rate **22% → ~1%** on their 803-prompt eval, Hermes Bench flat (~65.6%).
- **Anthropic published “components of agent memory”** (notes, dreaming, wikis, injected headers) — the how-to companion to yesterday’s science-usage study.
- **Flip the Switch closes TODAY at 23:59 IST.** Graph Hacks + Wispr winners are out. Toggle Wars (Flagsmith) opens **26–29 Nov**.

### The one that matters most
**Nous Research shipped Arete-27B**: Qwen3.8-27B post-trained (~53M tokens of SFT, no RL) so CCP-framed answers drop from **22% to ~1%** on their open Propaganda_Eval, with Hermes Bench **65.60%** vs base **65.77%** (noise). Weights, eval, and training data are public under **Apache-2.0**. For a student builder this is the cleanest “take the strongest local Chinese base, change the values layer, keep agentic capability” recipe of the week — and it pairs with yesterday’s Foundry Local / Qwen3.8-27B on-device path. Read the blog before you fine-tune: they chose Inkling as teacher, froze the vision encoder, and warn this is a root-cause nudge, not a claim they fixed every correlated failure mode. [blog](https://nousresearch.com/arete) · [HF](https://huggingface.co/NousResearch/Arete-27B) · [post](https://x.com/NousResearch/status/2118822925445050435) · 03:18, 7 Nov

### AI news

#### Labs and models
- **Arete-27B (Nous)** lands as open-weight post-training on Qwen3.8-27B for Western-aligned framing; eval + data shipped with the weights. Optionality on values without waiting for a US lab’s 27B base. [blog](https://nousresearch.com/arete) · [HF](https://huggingface.co/NousResearch/Arete-27B) · [post](https://x.com/NousResearch/status/2118822925445050435) · 03:18, 7 Nov
- **Anthropic — components of agent memory:** notes, salience, sleep-time “dreaming,” wiki representations, and a small injected MEMORY.md-style header. Dense harness design notes for anyone building persistent agents. [Anthropic](https://www.anthropic.com/research/components-of-agent-memory) · [post](https://x.com/AnthropicAI/status/2118814753154064501) · 02:46, 7 Nov
- **OpenAI BioBasicsBench** (with Ligo): 100 wet-lab analysis tasks; maker-reported GPT-6 Astra **66.7%** vs GPT-5.6 Sol **43.8%** at xhigh. Shows where multimodal science agents still over-conclude from messy gels/plates. [OpenAI](https://openai.com/index/measuring-how-ai-agents-handle-wet-lab-science/) · [post](https://x.com/OpenAI/status/2118782708767965238) · 00:38, 7 Nov
- **Meta specialized Muse / Meta AI models** (Wonder-trained) ship Active Memory + Active Focus; Meta cites PSI Index **47%** (was 38%). Agent memory is now a consumer product surface, not only a research blog. [Meta Research](https://research.meta.ai/blog/specialized-models-for-muse-and-metaai) · [post](https://x.com/AIatMeta/status/2118768974779634084) · 23:44, 6 Nov
- **DeepMind** shared research on AI agents stress-testing encryption (legacy 1024-bit RSA weaknesses found with human guidance; modern 2048-bit not claimed broken by these exploits). Agents-for-science signal next to OpenAI’s cyber week. [post](https://x.com/GoogleDeepMind/status/2118755418675765656) · 22:50, 6 Nov
- **Mistral Voxtral 3 end-of-turn detection** — knowing when the user finished speaking, not just ASR. Practical voice-agent building block. [post](https://x.com/MistralAI/status/2118744719870066936) · 22:08, 6 Nov

#### Products and APIs
- **Meta Muse Spaces:** describe a tracker/planner/game/hub; Muse builds it; connected apps can refresh in the background. UX pattern to study even if Muse isn’t your India daily driver. [Meta](https://about.fb.com/news/2026/11/introducing-spaces-customize-muse-app/) · [The Verge](https://www.theverge.com/tech/1028871/meta-muse-ai-spaces) · [TechCrunch](https://techcrunch.com/2026/11/06/meta-introduces-spaces-a-new-way-to-collaborate-with-your-muse-agent/) · 6 Nov
- **OpenAI × Hacktron** partnership expands Daybreak Red access for joint vuln research on OpenAI systems — continuation of the GPT-6 Cyber / Daybreak week, not a public student API. [OpenAI](https://openai.com/index/partnering-with-hacktron/) · 6 Nov

#### Funding and business
- **OpenAI reportedly ~$11B so far at $1.25T** (Bloomberg via TechCrunch); round may total ~$20B, below earlier ~$30B / $1.4T talk. Capital is still huge; targets are being marked down. [TechCrunch](https://techcrunch.com/2026/11/06/openai-reportedly-raises-an-additional-11-billion-at-a-1-25-trillion-valuation/) · ~04:23, 7 Nov
- **Ramp AI Index:** token spend grew only ~**1.5%** Aug–Sep after a **42%** July jump, while usage kept rising — price cuts capping lab ARPU as Anthropic IPO talk continues. [TechCrunch](https://techcrunch.com/2026/11/06/ramp-data-shows-ai-spending-stalling-just-as-anthropic-nears-its-ipo/) · ~21:24, 6 Nov
- **Thinking Machines Lab** nears a reported **~$5B Accel-led** round at ~**$40B** (Business Insider) — watch whether Inkling 2 Small’s promised Apache weights still land next week. [Business Insider](https://www.businessinsider.com/thinking-machines-lab-is-closing-5-billion-new-round-2026-11) · 6 Nov

#### Policy / dual-use
- **WIRED / Vals Cyber Offense:** Daybreak ~**81%** task completion vs DeepSeek open ~**73%**, at roughly **$2–3** vs **$17–46** token cost. Gating closed cyber models alone does not stop capability spread. [WIRED](https://www.wired.com/story/free-chinese-ai-models-are-getting-scary-good-at-hacking/) · 6 Nov
- **Bank of England:** firms estimate only ~**0.5%** cumulative AI productivity over three years — macro cold water next to the fundraising headlines. [The Register](https://www.theregister.com/ai-and-ml/2026/11/06/bank-of-england-pours-cold-water-on-ai-productivity-boom/5308059) · 6 Nov

#### India
- No fresh IndiaAI / Sarvam / Krutrim launch confirmed inside this 24h window (Ai2India digest items were Nov 3–4). Hackathon winners below are the India-builder signal today.

### New models and weights

| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Arete-27B | Nous Research | 27B (from Qwen3.8-27B); 64k train ctx | Apache-2.0 | SFT (~53M tokens) cuts propaganda rate 22%→~1%; Hermes Bench flat; weights+eval+data public | [blog](https://nousresearch.com/arete) · [HF](https://huggingface.co/NousResearch/Arete-27B) |
| Muse / Meta AI specialized (Wonder-trained) | Meta | undisclosed | proprietary product | Active Memory + Active Focus; PSI Index 47% (was 38%) | [Meta Research](https://research.meta.ai/blog/specialized-models-for-muse-and-metaai) |

### Benchmarks and leaderboards
- **BioBasicsBench** (OpenAI × Ligo): Astra **66.7%** vs Sol **43.8%** mean reward at xhigh (maker-reported). [OpenAI](https://openai.com/index/measuring-how-ai-agents-handle-wet-lab-science/)
- **Vals Cyber Offense** (via WIRED): Daybreak ~**81%** / DeepSeek open ~**73%**; open runs much cheaper. [WIRED](https://www.wired.com/story/free-chinese-ai-models-are-getting-scary-good-at-hacking/)
- **Arete Propaganda_Eval:** base Qwen3.8-27B any-propaganda **22%** → Arete **~0.9–1%**; fact mean **2.32 → 2.98**/5. [Nous](https://nousresearch.com/arete)
- **Muse PSI Index:** **47%** (was 38%) per Meta. [Meta](https://research.meta.ai/blog/specialized-models-for-muse-and-metaai)
- **Hermes Bench / Terminal-Bench-2.1** (maker-reported for Arete): Hermes **65.60%** vs **65.77%**; Terminal-Bench-2.1 **70%** vs **67%** (Nous does not claim credit for the Terminal bump). [Nous](https://nousresearch.com/arete)

### Trending repos and projects
- [NVIDIA/auto-ontology](https://github.com/NVIDIA/auto-ontology) is #1 on GitHub trending: a Python framework that builds semantic/graph reasoning layers over enterprise metadata for LLM agents. Use it when a hackathon agent needs a real knowledge graph instead of raw dumps. Python; +2,015 today on trending pages (~9.1k★). [chinchoukou](https://x.com/chinchoukou/status/2118629516893716939) · 14:30, 6 Nov
- [cloudflare/security-audit-skill](https://github.com/cloudflare/security-audit-skill) is a coding-agent skill for multi-phase security audits with independently verified, machine-readable findings. Drop it next to Stroq-style hooks when your agent can run tools. +2,524 / 24h (62,745★ per @trending_repos). [post](https://x.com/trending_repos/status/2118676886750666861) · 17:38, 6 Nov
- [morluto/rea](https://github.com/morluto/rea) is agent reverse-engineering from app behavior down toward native binaries. Build RE assistants that map closed apps/protocols with coding agents. TypeScript; +24,060 / 7d (~438k★ per whatstrending.ai).
- [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) is DeepSeek’s “everything is a plugin” agent harness. Ship custom tools/skills as plugins on that runtime. TypeScript; 275,033★ (GitHub API).
- [elder-plinius/T3MP3ST](https://github.com/elder-plinius/T3MP3ST) is an autonomous multi-agent red-teaming / offensive-security meta-harness — useful for agent security evals, not as an exploit guide. TypeScript; +242 today (6,953★).
- [meta/astryx](https://github.com/meta/astryx) is an open, customizable, agent-ready design system so coding agents share one UI contract. TypeScript; +198 today (14,059★).
- [lobehub/lobehub](https://github.com/lobehub/lobehub) runs super-agents inside the chats your team already uses. Prototype workplace agents without a full custom harness. TypeScript; +209 today (84,255★).
- [pipeshub-ai/pipeshub-ai](https://github.com/pipeshub-ai/pipeshub-ai) is an open permission-aware context layer for agents over Slack/Drive/Jira/GitHub/M365 (50+ connectors). Build enterprise RAG that respects ACLs. Python; +64 today (4,029★).
- [multica-ai/multica](https://github.com/multica-ai/multica) is a self-hostable humans+agents team workspace. Go; +130 today (55,176★).
- [infiniflow/ragflow](https://github.com/infiniflow/ragflow) is agent-native RAG / context infrastructure. Drop-in retrieval for document Q&A or multi-agent context. Go; +86 today (93,703★).
- [FareedKhan-dev/all-agentic-architectures](https://github.com/FareedKhan-dev/all-agentic-architectures) packs 35 production agent patterns (Reflexion, LATS, GraphRAG, MemGPT, Voyager, …) as a runnable textbook. Jupyter; +10 today (4,689★).
- [gepa-ai/gepa](https://github.com/gepa-ai/gepa) does reflective optimization for prompts/code — auto-improve loops that critique and rewrite. Jupyter; +25 today (7,320★).
- [snap-stanford/memorilla](https://github.com/snap-stanford/memorilla) is latent semantic memory for LLMs (compressed long-term memory for agents/RAG). 298★; on HN front page (~92 pts).
- [zalando-incubator/agentic-identity-broker](https://github.com/zalando-incubator/agentic-identity-broker) is an OAuth2 delegation/consent broker so agent tools get least-privilege API access. 53★; Show HN.
- [mainplane-ai/mainplane](https://github.com/mainplane-ai/mainplane) is an always-on control-plane agent with WireGuard workers so laptop sleep doesn’t kill the agent. Go; 802★; Show HN.

Also moving hard (already seen / yesterday list — star callouts only): microsoft/VibeVoice +1,004 today; vercel-labs/agent-browser +622; stablyai/orca +1,155. HF trending notables: [moonshotai/Kimi-K3.1-Pro](https://huggingface.co/moonshotai/Kimi-K3.1-Pro), [ricursiveAI/Ripple-65B-Preview](https://huggingface.co/ricursiveAI/Ripple-65B-Preview). OSS releases in window: llama.cpp **b12179**, transformers **v5.22.2**, Unsloth **v0.1.916-beta**, Google Gen AI SDK **v3.0.0**, CrewAI **1.15.36**.

### Hackathons
- **Flip the Switch** (WeMakeDevs × Switch) — submissions close **TODAY, 7 Nov at 23:59 IST** (confirmed). Online; solo or up to 4; connect coding agents to Slack/Teams/Discord via Switch; **$10,000** prize pool. [event](https://www.wemakedevs.org/hackathons/switch) · [post](https://x.com/WeMakeDevs/status/2118567394268598770) · 10:23, 6 Nov
- **Vultr: Agent Rush** (lablab.ai × Vultr): hybrid online build **3–8 Nov**; optional on-site Salt Lake City 8 Nov. Teams 1–6; **$9,000** cash + **$5,000** Vultr credits; every participant gets **$200 Vultr credits**. Exact end clock still soft — confirm before cutting it fine. [event](https://community.vultr.com/e/vultr-agent-rush-hackathon)
- **CodeNova India 2026** (We Code Coders): online agentic AI for UG/PG, teams 1–6; top three share ₹30,000 + internships/incubation. Registration through **10 Nov ~12:30 IST** (confirmed on organiser page). [event](https://wecodecoders.in/events/codenova-india)
- **Great Indian AI Internship Challenge** (Gnani): up to **100 paid internships**, ₹5 lakh awards, **5,000 programme credits** per registration. Deadline **10 Nov** (final). [register](https://www.gnani.ai/great-indian-ai-internship-registration-form)
- **DataNova 2026 Global Data-thon** (Devpost): online, students only, teams required, $1,750 prizes. Deadline **11 Nov at 03:30 IST** (confirmed). [event](https://datanova-2026-global-data-thon.devpost.com/)
- **PayPal AI Hackathon** (Devpost): online global; must use PayPal + AI; **$67,500+** prizes. Deadline **13 Nov at 01:30 IST** (confirmed). [event](https://paypalaihackathon.devpost.com/)
- **DSH Hacks V2** (Devpost, AI × Healthcare): online, students 13+, credits stack. Deadline **15 Nov at 13:15 IST** (confirmed). [event](https://dsh-hacks-v2.devpost.com/)
- **Agentic AI Hackathon** (Product Space): online 14–15 Nov; prizes ₹50,000 cash (page headline). Project submission **15 Nov 23:59 IST** (confirmed). [event](https://theproductspace.in/events/agentic-hackathon)
- **Homingo Hack Days** (Edition 01): India students/early-career; reg closes **15 Nov 23:59 IST**; kickoff 21 Nov; submit 4–6 Dec; ₹5,000 winner. [FAQ](https://hackathon.homingo.co.in/faq)
- **UGREEN Hackathon 2026 on AI NAS** (Devpost): **$46,000** cash; Round 1 online (no NAS needed). Round 1 deadline **16 Nov at 13:15 IST** (confirmed). [event](https://ugreenhackathon.devpost.com/) · [Devpost post](https://x.com/devpost/status/2118785164343980154) · 00:48, 7 Nov
- **Festive Hacks** (WeMakeDevs × WeAreDevelopers) — in-person **25 Nov 2026, 09:00–18:00 IST at BIEC Bengaluru**. Teams 1–4; apply on Luma; 1st prize fully sponsored VIP Berlin trip; 2nd ₹2,00,000; 3rd ₹1,00,000. Travel/stay to Bengaluru not covered. [event](https://www.wemakedevs.org/hackathons/festivehacks) · [post](https://x.com/WeMakeDevs/status/2118703742967050611) · 19:25, 6 Nov
- **Toggle Wars** (WeMakeDevs × Flagsmith) — **new:** online **26–29 Nov**; feature flags + A/B tests; three tracks; **$5,000** prizes (cash, PS5+GTA 6, AirPods); free, solo or team. [event](https://www.wemakedevs.org/hackathons/flagsmith) · [post](https://x.com/WeMakeDevs/status/2118840018366038254) · 04:26, 7 Nov
- **Winners / notes:**
  - **Graph Hacks** (WeMakeDevs × FalkorDB): Arnab Saha — Precedent Graph (legal precedent validity agent, iPhone 18 Pro); Aymaan Pathan — Pathway (GitHub→skills knowledge graph, PS5+GTA VI); Shreyash Mandal — KT Brain (company brain across PRs/Jira/chats, M6 Mac mini). Best blog: Nishit Baria / Recall Tracer. [post](https://x.com/WeMakeDevs/status/2118653433167417397) · 16:05, 6 Nov
  - **No Hands / Wispr Challenge:** Jaya Surya Penumatcha — NoHandsPilot (voice Mac assistant, ₹1 lakh Builders); Anvitha PR — Hot Seat (pitch-practice tool, ₹1 lakh No-Code). [post](https://x.com/WeMakeDevs/status/2118682993766310298) · 18:02, 6 Nov
  - **ZIVOX** challenge page now shows **rescheduled to Feb 2027** — not open for November.

### Student perks and credits
- **URGENT — Flip the Switch** closes **tonight 23:59 IST** ($10k pool).
- **Gnani Great Indian AI Internship Challenge:** 5,000 API credits + paid internship path; submit by **10 Nov 2026** (no extensions). [register](https://www.gnani.ai/great-indian-ai-internship-registration-form)
- **Vultr Agent Rush:** **$200 Vultr credits** each participant; online window ends ~**8 Nov**.
- **CodeNova:** participant credits/domains still listed on organiser pages (reg ~10 Nov).
- **Nuvolos Fellowship:** closed **6 Nov** — do not apply as open.
- Still rolling (not new today): Azure for Students ($100), GitHub Student Pack, Nebius research grants, AWS/Google research credits. [compute credits list](https://advance.to/compute-credits/)

### Grok Bots
- **Docs facelift** announced by @mattyp. [post](https://x.com/mattyp/status/2118871619074720147) · 06:32, 7 Nov
- **AlexFinn** shares stealable Grok Bot workflows after months of nonstop use (“best AI agent” framing + X-plugin monitoring examples). [post](https://x.com/AlexFinn/status/2118882927610360204) · 07:17, 7 Nov
- **aswincode** published a long write-up on running life with a **12-bot** Grok Bot team (Chief of Staff, Eggbot, Editor, Staff Engineer on a real Mac, etc.) — drafts only; human yes before send/spend. [post](https://x.com/aswincode/status/2118747986155208971) · 22:20, 6 Nov · [article](https://x.com/i/article/2118691512321970176)
- **bishara** describes a 3-bot job-application pipeline (LinkedIn + startups → tailored resumes → apply). [post](https://x.com/bishara/status/2118905599195021567) · 08:47, 7 Nov
- **Product Hunt:** Turnstone pitched as a free Grok Bot alternative shipping many feature requests in under 24h (group chats, WhatsApp, import, inboxes). [post](https://x.com/ProductHunt/status/2118889437631533558) · 07:43, 7 Nov
- Hot takes in the window: Hermes Agent vs Grok Bot; OpenBot described as “Grok Bot workflow + better models”; Claude Duet vs Grok Bot on rule-breaking.

### Build idea of the day
For **Flip the Switch** (closes **tonight, 7 Nov at 23:59 IST**), ship a Slack/Discord teammate on Switch that stores lasting notes the Anthropic way: a small injected header + a dreaming pass that corrects bad memories from transcripts ([components of agent memory](https://www.anthropic.com/research/components-of-agent-memory)). Point the brain at **Arete-27B** (or local Qwen3.8-27B) so you stay on Apache/open weights, add **cloudflare/security-audit-skill** before the bot runs shell tools, and use **zalando-incubator/agentic-identity-broker** patterns so every connector is least-privilege with your yes. Judges see an approval-gated coworker with real memory hygiene — not another firehose — and you can reuse the same stack for **Toggle Wars** (26–29 Nov) by wiring Flagsmith experiments into the agent’s release loop.

### What the field is arguing about
- **Values are a fine-tune away:** Arete shows a thin SFT layer can rewrite CCP framing on a top Chinese open base without killing Hermes Bench — what does that mean for “trust the base weights” and for federal bans?
- **Open cyber ≈ closed, cheaper:** Vals/WIRED (~81% Daybreak vs ~73% DeepSeek open) undercuts “gating buys time,” one day after GPT-6 Cyber’s Critical launch.
- **Spend flat, tokens up, valuations cut:** Ramp’s 1.5% spend growth vs July’s 42%, OpenAI’s marked-down raise, Thinking Machines’ $40B report, and BoE’s 0.5% productivity estimate all hit the same week.
- **Agent memory productization:** Anthropic’s dreaming/notes/wikis write-up vs Meta shipping Active Memory into Muse — research pattern becoming consumer default.
- **Always-on teammates, many seats:** Grok Bot multi-bot teams vs Claude Duet vs Turnstone vs yesterday’s Perplexity Teammates / Kimi Hosted Agents price tags.

### Worth reading in full
1. [Nous — Introducing Arete-27B](https://nousresearch.com/arete) — training recipe, Propaganda_Eval tables, Hermes/Terminal numbers, open eval+data.
2. [Anthropic — The components of agent memory](https://www.anthropic.com/research/components-of-agent-memory) — notes, dreaming, wikis, injected headers; Pokémon / CL-Bench / LAB ablations.
3. [OpenAI — BioBasicsBench](https://openai.com/index/measuring-how-ai-agents-handle-wet-lab-science/) — wet-lab agent failures on ambiguous experimental evidence.
4. [WIRED — Free Chinese AI models are getting scary good at hacking](https://www.wired.com/story/free-chinese-ai-models-are-getting-scary-good-at-hacking/) — Vals open vs closed cyber cost/capability.
5. [Meta — Specialized models for Muse and Meta AI](https://research.meta.ai/blog/specialized-models-for-muse-and-metaai) — Active Memory/Focus eval deltas (PSI 47%).

### Quiet accounts / couldn't open
- **@karpathy** and **@simonw** posted nothing original in the window (API quiet).
- **Reddit** r/LocalLLaMA and r/MachineLearning JSON / old.reddit: HTTP **403** — no LocalLLaMA items included.
- **Product Hunt** homepage scrape was thin; used StartupCorners Nov 6 digest (Glasshand / Rerun / Living Brain) instead of promoting PH cards into the top-15 repos list.
- **The Neuron** Nov 6 digest scrape failed; **Reuters** AI-rout page hit captcha. DeepMind RSA official blog HTML date not separately confirmed beyond the X post.
- **Import AI / xAI / DeepSeek / Qwen** official blogs: no confirmed in-window launch pages beyond Arete and the Meta/OpenAI/Anthropic items above.
- **Vultr Agent Rush** exact 8 Nov end clock still soft. **LinkedIn** used only as secondary web search, not a primary feed.
- ZIVOX rescheduled to **Feb 2027** (removed from open list).

## Archive

- [2026-11-07](briefs/2026-11-07.md)
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

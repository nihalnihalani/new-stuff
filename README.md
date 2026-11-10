# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-10

## X Brief: Tue 10 Nov 2026, 9 AM (9 Nov 08:56 to 10 Nov 09:00 IST)

**I checked 15 X accounts (88 posts) and 6 watchlist searches plus 7 follow-up searches, a post lookup and X News (~300 results, 321 unique posts), plus GitHub trending (daily, weekly, Python, TypeScript, Rust, Go, Jupyter), Hugging Face trending models/datasets/Spaces and papers, Hacker News front page and Show HN, lab blogs and feeds (Anthropic, OpenAI, Google, DeepMind, Meta, NVIDIA, Microsoft, Hugging Face), GitHub releases for llama.cpp, vLLM, Ollama, LangChain, LangGraph and transformers, The Verge, TechCrunch, Ars Technica, The Decoder, CNBC, The Register, Import AI, Latent Space, TLDR AI, Ben's Bites, Simon Willison, Analytics India Magazine, YourStory, Inc42, MediaNama, Devpost, Unstop, Luma, WeMakeDevs, Scaler and public LinkedIn via search. Reddit and Product Hunt returned 403, and VentureBeat returned 429.** Kept 13 news items, 5 models, 15 repos/projects and 8 open hackathons. All times are IST.

- **Two launches, one pattern:** Anthropic shipped **Claude Fable 5.2 / Mythos 5.2** (now #1 on the Artificial Analysis index, 20% cheaper at $8/$40 per million tokens), and Meta shipped **Muse Ember**, a small agent workhorse at $0.10/$0.50, about 80× cheaper per token.
- **Open weights and free APIs:** Meituan's **LongCat-2.5** (1.6T MoE) weights are now on Hugging Face under MIT, and LG made the **K-EXAONE 2.5** API free for anyone with a key.
- **Check your repos today:** Apiiro found Claude Code settings files leaking database passwords and API keys on public GitHub. Deadline to watch: **Gnani's Great Indian AI Internship Challenge closes tonight at 23:59 IST.**

### The one that matters most
**Plan with a big model, execute with a small one. That's now the cheapest way to build an agent.** Fable 5.2 sets new highs (65 on the Artificial Analysis Intelligence Index v5, 81.2% on ARC-AGI-3 with a standard harness) at $8/$40 per million tokens ([Anthropic](https://www.anthropic.com/claude-fable-and-mythos-5-2) · 9 Nov · [post](https://x.com/claudeai/status/2119867114450268322) · 00:27, 10 Nov, 80K likes). Meta's Muse Ember matches Claude Haiku 5.5's best score at about a third of the cost, and Meta's own pitch is "Muse Wonder plans, Muse Ember handles the volume" ([TechCrunch](https://techcrunch.com/2026/11/09/meta-releases-muse-ember-a-new-lightweight-model-for-agent-execution/) · 23:30, 9 Nov). For a student budget: use a frontier model for the few planning calls, then route the hundreds of tool calls, extractions and retries to an Ember-class model. That split is where your hackathon credits stretch the furthest.

### AI news

#### Labs and launches
- **Anthropic releases Claude Fable 5.2 and Mythos 5.2:** both are the same model. Fable has cyber and bio safeguards and is available to everyone, while Mythos is for vetted orgs only. Output is up to 30% faster, prices drop from $10/$50 to $8/$40, and an optional fast mode costs 2×. TechCrunch notes the models "voice suspicion that they are being evaluated" more than any recent Claude, which Anthropic says makes testing harder. [TechCrunch](https://techcrunch.com/2026/11/09/anthropic-releases-new-mythos-and-fable-models-amid-rsi-concerns/) · 00:54, 10 Nov · [The Decoder](https://the-decoder.com/claude-fable-5-2-and-mythos-5-2-cement-anthropics-ai-lead-just-before-its-ipo/) · 02:45, 10 Nov
- **Meta launches Muse Ember:** its smallest Muse model, built for tool calls, coding subtasks, routing, extraction and long-document parsing. It has a 1M-token context, takes text, images and audio, and costs $0.10/$0.50 per million tokens on the Meta Model API. It's also coming to Google Cloud. This is a cheap default for the executor half of your agent. [Meta blog](https://research.meta.ai/blog/muse-ember) · 9 Nov · [post](https://x.com/AIatMeta/status/2119853591703998787) · 23:34, 9 Nov
- **OpenAI's Control Room:** a central system that tracks every research inference workload and can halt model output within 35 seconds of a decision to intervene. It's a concrete reference design if you're building kill switches into agents. [post](https://x.com/OpenAI/status/2119913172039868579) · 03:31, 10 Nov
- **OpenAI's dot can now use multiple local computers:** you pick which machine runs a task, so it can build and test your app on one box while you keep coding on your laptop. [post](https://x.com/OpenAIDevs/status/2119883176726409645) · 01:31, 10 Nov
- **Google adds TPU 8tx and TPU 8i Max:** that makes four eighth-gen TPU systems this year, one for confidential inference and one for very long context windows. Google says nearly 100 customers now use TPUs. [Google](https://blog.google/innovation-and-ai/infrastructure-and-cloud/global-network/tpu-8i-max-and-8tx/) · 18:30, 9 Nov
- **ByteDance's Seedream 5.5:** image editing that stays stable across up to 100 rounds with unchanged pixels preserved, plus native transparent-background (RGBA) output. It's rolling out in China first (Jimeng, Doubao, Volcengine Ark). [The Decoder](https://the-decoder.com/bytedances-seedream-5-5-promises-pixel-stable-image-editing-across-100-rounds-without-color-drift/) · 00:20, 10 Nov

#### Security and research
- **Claude Code is leaking secrets on GitHub:** clicking "Yes, and don't ask again" saves the full command, passwords included, to `.claude/settings.local.json`. Apiiro found 100,000+ of these files on public GitHub, about 1,100 of them with secrets, and 215 of those slipped past gitleaks and TruffleHog. Check your repos and add the file to `.gitignore` at the repo level. [Ars Technica](https://arstechnica.com/ai/2026/11/claude-code-settings-files-expose-thousands-of-secrets-on-github/) · 22:54, 9 Nov
- **An AI system proved a quantum conjecture that had been open since 2008:** Physical Superintelligence's research system, running a non-public Anthropic model, proved the Aaronson–Ambainis conjecture, and the Lean proof assistant checked every step. @anurag_629's takeaway for coders: "Trust the checker, not the model… your tests are the Lean." [Import AI 480](https://importai.substack.com/p/import-ai-480-self-sustaining-space) · 19:01, 9 Nov · [post](https://x.com/anurag_629/status/2119810264803516674) · 20:42, 9 Nov

#### Business and chips
- **Anthropic is pushing ahead with its IPO:** per the WSJ, it will set a valuation range this week and could start trading Thursday or Friday next week, with some investors pushing for less than the $1.5T discussed. [TechCrunch](https://techcrunch.com/2026/11/09/anthropic-reportedly-plans-to-move-forward-with-ipo-plans/) · 06:57, 10 Nov
- **The Nvidia–Huang scandal keeps widening:** Nvidia stock fell 4%, and Democrats and short sellers are piling in. The Decoder argues it weakens Huang's lobbying against tighter chip export controls, which matters for GPU supply and prices. [The Verge explainer](https://www.theverge.com/ai-artificial-intelligence/1030422/nvidia-jensen-huang-ai-china-alice-huang) · 05:16, 10 Nov · [The Decoder](https://the-decoder.com/nvidia-espionage-scandal-weakens-huangs-lobby-against-tighter-ai-chip-export-controls/) · 17:08, 9 Nov
- **Automattic launches Spacefast:** hosting for vibe-coded apps with database, auth, file uploads, email and analytics, and it connects to Claude, Grok Bot, Cursor, OpenCode and others or a Git repo. It's another way to ship a hackathon demo without wiring up your own backend. [TechCrunch](https://techcrunch.com/2026/11/09/automattic-debuts-a-platform-to-deploy-vibe-coding-apps-amid-a-changing-internet/) · 19:30, 9 Nov

#### India
- **Sarvam hires Google Cloud India's MD as President and CBO:** Sashikumar Sreedharan will lead enterprise and government business and join the board. Sarvam says 100+ enterprises and government institutions build on its models. [YourStory](https://yourstory.com/2026/11/sarvam-google-cloud-india-head-sashikumar-sreedharan-president-cbo) · 16:37, 9 Nov
- **Coforge joins SpaceX's Super Intelligence Partner Network:** it will build industry-specific Grok applications through its forward-deployed engineering unit. That makes "AI forward-deployed engineer" a role to watch at Indian IT firms. [Analytics India Magazine](https://analyticsindiamag.com/ai-news/coforge-joins-spacex-network-to-develop-industry-specific-grok-applications) · 16:46, 9 Nov

### New models and weights

| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Claude Fable 5.2 / Mythos 5.2 | Anthropic | not disclosed | Proprietary API | New #1 on AA Index v5 (65) and ARC-AGI-3 (standard harness); $8/$40, up to 30% faster | [Anthropic](https://www.anthropic.com/claude-fable-and-mythos-5-2) · 9 Nov |
| Muse Ember | Meta | not disclosed; 1M context, multimodal input | Proprietary API | $0.10/$0.50; AA Index 36, matching Haiku 5.5 at a third of the cost per task | [Meta](https://research.meta.ai/blog/muse-ember) · 9 Nov |
| LongCat-2.5 | Meituan | 1.6T total, ~48B active, multimodal MoE | MIT | Open weights for long-horizon agentic coding, now on HF (weights updated 9 Nov) | [HF](https://huggingface.co/meituan-longcat/LongCat-2.5) · [post](https://x.com/VentureBeat/status/2119929241852633322) · 04:34, 10 Nov |
| ARLoop-1.2B / 0.6B | OSU NLP | 1.2B and 0.6B looped transformers | Apache-2.0 | Fully open pretrained looped transformers with recipes, a rare chance to study looped LLMs on a small GPU | [HF](https://huggingface.co/osunlp/ARLoop-1.2B) · [post](https://x.com/yuekun_yao/status/2119982422259622086) · 08:06, 10 Nov |
| K-EXAONE 2.5 | LG AI Research | 750B MoE, 31B active, 512K context | Free API (closed weights) | OpenAI-compatible and free with a key (some regions only); LG reports 59.2 on SWE-Bench Pro | [LG](https://www.lgresearch.ai/news/view?seq=755) · 9 Nov |

Also: **Ollama v0.40.16** added Ricursive's Ripple Preview 65B (`ollama run ripple-preview`) ([release](https://github.com/ollama/ollama/releases/tag/v0.40.16) · 23:51, 9 Nov), and **GPT Image 2.6** is live on partner apps, though I didn't find OpenAI's own launch post in the window.

### Benchmarks and leaderboards
- **ARC-AGI (verified):** Fable 5.2 scored 81.2% on ARC-AGI-3 with the standard harness, a new high, and 97.7% with the provider-adapter harness. It also hit 93.8% on ARC-AGI-2 ($0.98/task) and 98.5% on ARC-AGI-1. [post](https://x.com/arcprize/status/2119871080525373922) · 00:43, 10 Nov
- **Artificial Analysis Index v5:** Fable 5.2 (max) scores 65, against Gemini 4 Carbon at 60 and Claude Opus 5.5 at 59 ([post](https://x.com/ArtificialAnlys/status/2119878995386982508) · 01:15, 10 Nov; [HN](https://news.ycombinator.com/item?id=50431144), 301 pts). On AA-3D (building interactive 3D), Fable 5.2 leads at 1271 Elo, 67 points ahead of Sonnet 5.5 ([post](https://x.com/ArtificialAnlys/status/2119953570430881946) · 06:11, 10 Nov).
- **Muse Ember on efficiency:** it scores 36 on AA's index for $0.14 per task ([post](https://x.com/ArtificialAnlys/status/2119854348587123007) · 23:37, 9 Nov), and Vals calls it the cheapest model on the Vals Index at $0.15 per test ([post](https://x.com/ValsAI/status/2119855420017971205) · 23:41, 9 Nov).
- **GPT Image 2.6 Flare:** about 30 s per image against about 55 s for 2.5 Flare at max quality, and it scores higher on AA's text-to-image and editing boards. [post](https://x.com/ArtificialAnlys/status/2119913484423156015) · 03:32, 10 Nov
- **Agent Arena:** Inkling 2 Small ranks #31 overall and is set to be the #1 US open-weights model there once its weights ship. [post](https://x.com/arena/status/2119840698614817076) · 22:43, 9 Nov

### Trending repos and projects
- [garrytan/gbrain](https://github.com/garrytan/gbrain) is Garry Tan's opinionated "agent brain" for OpenClaw and Hermes agents. Fork it to see how a heavy agent user sets up a personal agent. TypeScript, 32,234★, +216 today.
- [anthropics/claude-quickstarts](https://github.com/anthropics/claude-quickstarts) is Anthropic's set of deployable starter apps for the Claude API. It's the quickest way to get a Fable 5.2 or Opus demo running in a weekend. Python, 20,088★, +551 today.
- [google-deepmind/mujoco](https://github.com/google-deepmind/mujoco) is DeepMind's general-purpose physics simulator for robotics and biomechanics. Use it for a physical-AI or RL-in-sim hackathon entry. C++, 16,984★, +574 today.
- [opensandbox-group/OpenSandbox](https://github.com/opensandbox-group/OpenSandbox) is a secure, fast sandbox runtime for AI agents. Run agent-written code without risking your laptop. Python, 16,971★, +168 today.
- [PrimeIntellect-ai/prime-agent](https://github.com/PrimeIntellect-ai/prime-agent) is Prime Intellect's self-improving coding and research agent for long-running tasks, with subagents and durable memory. Study it for long-horizon agent design. Rust, 22,647★ ([post](https://x.com/alexrashkov/status/2119724494701146539) · 15:01, 9 Nov).
- [DIYgod/pinky](https://github.com/DIYgod/pinky) lets Claude Code, Codex or Cursor drive your iPhone or Android while you watch, and payments wait for your click. Build a phone-automation agent with a human in the loop. Go, 1,481★, created 6 Nov ([post](https://x.com/Alexvx_nft/status/2119909512584814989) · 03:16, 10 Nov).
- [homeassistant-ai/ha-mcp](https://github.com/homeassistant-ai/ha-mcp) is an MCP server for configuring and automating Home Assistant from Claude, ChatGPT and others. Build a voice-controlled hostel-room or smart-home agent. Python, 6,076★, +31 today.
- [beipo-ai/NorthCUA](https://github.com/beipo-ai/NorthCUA) is an open desktop/web computer-use harness with long-horizon memory, live evaluation and recoverable batches. Use it as a base for a browser-agent track. Python, 109★, created 2 Nov ([post](https://x.com/TheArthiAI/status/2119658313982038207) · 10:38, 9 Nov).
- [dream-num/univer](https://github.com/dream-num/univer) is an open office SDK for docs and sheets that people and AI agents can edit and calculate in together. Build an AI spreadsheet copilot into your own app. TypeScript, 23,026★, #1 on Trendshift today per [this post](https://x.com/h___t____n/status/2119964394889384324) (06:54, 10 Nov).
- [kortix-ai/CompanyOS](https://github.com/kortix-ai/CompanyOS) is a self-hostable "company as code" with multiplayer AI agents. A base for a multi-agent ops demo. TypeScript, 20,612★, +27 today.
- [ooolabdev/ooosplat](https://github.com/ooolabdev/ooosplat) is a local desktop app that turns videos and images into 3D Gaussian splats in one click. Use it to make 3D scenes for AR or game hacks. Rust, 2,417★, +121 today.
- [elizaOS/eliza](https://github.com/elizaOS/eliza) is an open agent framework for personal agents that chat, remember context, manage your calendar and drive a browser. TypeScript, 19,800★ ([post](https://x.com/GithubProjects/status/2119982632171962623) · 08:07, 10 Nov).
- [Angais/pixel-art-atlas-1.4m](https://huggingface.co/datasets/Angais/pixel-art-atlas-1.4m) has 1.4M captioned 16×16 transparent sprites, CC0. Fine-tune a sprite generator or fill out a game-jam asset pipeline. Dataset ([post](https://x.com/calebfahlgren/status/2119503896431182153), reposted by @huggingface).
- [E-means](https://e-means.github.io/) is a k-means replacement that the authors say beats Lloyd's loss in 1.2–3 epochs instead of 25, a 10–45× wall-clock speedup on GPU. Swap it into clustering-heavy RAG or embedding pipelines. Web/paper, on the HN front page ([HN](https://news.ycombinator.com/item?id=50429734), 295 pts).
- [Dodaios/ste80-humanizer](https://github.com/Dodaios/ste80-humanizer) rewrites AI-sounding text toward the ASD-STE100 Simplified Technical English rules. Useful for cleaning up docs or READMEs. Show HN ([HN](https://news.ycombinator.com/item?id=50429144), 64 pts).

Also: **llama.cpp** shipped b12220–b12242, including an OpenAI-compatible `/v1/audio/speech` endpoint ([b12238](https://github.com/ggml-org/llama.cpp/releases/tag/b12238) · 05:53, 10 Nov) and Gemma 4 streaming audio input ([b12237](https://github.com/ggml-org/llama.cpp/releases/tag/b12237) · 05:13, 10 Nov). vLLM, LangGraph and transformers had nothing new, and LangChain only shipped a minor Fireworks fix. Still climbing from earlier briefs: sherlock (+4,267 today), meta/astryx (+3,278), OpenMausBot (+1,587), agent-browser (+916), and t3code was @trending_repos' repo of the week (+15,379).

### Hackathons
Closing tonight (from earlier briefs): **Gnani's Great Indian AI Internship Challenge, 10 Nov 23:59 IST.** Also still open: HackIndia "AI for Lawyers" (registration closes 11 Nov 09:18 IST), Nous Hermes plugin hackathon (~12 Nov), PayPal AI (12 Nov), DotRepo Vibeathon, Product Space hackathons (14 Nov), UGREEN AI NAS Round 1 (6 days left, per @devpost), Toggle Wars (26–29 Nov), Google #BuildHybridAI (1 Dec 03:30 IST).

New, soonest deadline first:
1. **eGain "Build, Demo, and Take Home a Working AI Support Bot"**: $750, online, 18+ in any country. Due **13 Nov 10:00 IST** (confirmed). [Devpost](https://build-a-working-ai-support-bot.devpost.com/)
2. **ATOX AI for Climate Youth Hackathon**: online on 14–15 Nov, no coding experience needed, and selected projects showcase at COP31 on 18 Nov. Prize not stated. Apply by **13 Nov 21:30 IST** (24:00 UTC+8). [Luma](https://luma.com/ag12jspz) · via [post](https://x.com/GAUC_News/status/2119771162301407327)
3. **IceHacks**: $17,150, online, students only (13+), all countries. Due **16 Nov 07:30 IST** (confirmed). [Devpost](https://icehacks.devpost.com/)
4. **Scaler × Wispr Flow "India Runs on Voice"**: **₹30 lakh** across 15 teams (₹7L first), free, for students and professionals in India aged 18+, solo or up to 3. Build voice-first tools in any Indian language. Round 1 closes **26 Nov**, registration closes **27 Nov**, and the finale is on campus on 13 Dec. [Scaler](https://hackos.scaler.com/wispr/) · via [post](https://x.com/AvinashSingh_20/status/2119807596517642308)
5. **Agentware 72-Hour Hackathon**: $1,600 total ($800 grand prize, plus a $100 "Best Kill Switch" award). Online, teams of 1–4, any model or stack, with tracks for inbox, research and study, browser agents and dev workflow. Registration closes **27 Nov 23:00 IST**. [Unstop](https://unstop.com/hackathons/agentware-72-hour-hackathon-hackathon-raptors-1800324)
6. **HackIndia AgentVerse '26**: a virtual AI-agents hackathon open worldwide, running until **30 Nov** (via an InternHack LinkedIn post; I didn't confirm it on the event page). [LinkedIn](https://www.linkedin.com/posts/internhack_hackathons-scholarships-fellowship-activity-7522527757323513856-w81h)
7. **GreenMind Sustainable AI Hackathon 2.0**: ₹1.5L across student, startup and corporate categories. Measured energy, carbon and water impact counts for 30% of the score. Stage 1 closes **30 Nov 23:59 IST**, and the finale is in Bengaluru on 14–15 Dec. [LinkedIn](https://www.linkedin.com/posts/green-computing-foundation_greenmind2026-sustainableai-greencomputing-activity-7519283776447954964-l3S8)
8. **Apart Research × SL5 threat-intel sprint**: free and online on 4–6 Dec. Use LLMs for threat intelligence and threat modelling, in teams of 1–5. @anurag_629 says it has $5,000 in cash prizes and India can apply. Due 6 Dec 23:59 AoE (**≈7 Dec 17:29 IST**). [Apart](https://apartresearch.com/sprints/threat-intelligence-threat-modelling-2026) · via [post](https://x.com/anurag_629/status/2119986156754374726)

Winners:
- **Meta Global AI Developer Hackathon:** 17 winners from 5,361 projects, with a thread listing them all ([post](https://x.com/Lukaesch/status/2119895989058199712) · 02:22, 10 Nov). One winner, Nemesis, took 4th place "pushing Muse to its limits" ([post](https://x.com/divagr1925/status/2119867973028749554) · 00:31, 10 Nov).
- **YC × Naive hackathon, more winners:** one team built a fully agent-run e-commerce business where agents spot trends, AI designs products, 3D printing handles fulfilment, and a GTM agent makes Reels ([post](https://x.com/PrabaljitW/status/2119671238197207282) · 11:29, 9 Nov). FounderDesk, an AI editorial desk for founders, took second prize from MobileRun ([post](https://x.com/ankits0052/status/2119957336626495892) · 06:26, 10 Nov).
- **OpenAI × Cerebras mini hackathon:** LiveDx is a live clinical copilot that re-ranks its top 5 diagnoses after every sentence and writes SOAP notes, running gpt-oss-120b on Cerebras. [post](https://x.com/abdullah_stack/status/2119834175553544635) · 22:17, 9 Nov
- **MakerMods Physical AI Hackathon:** a 1st-place win was shared as a video only, so I couldn't see the project details. [post](https://x.com/IsaiahBallah/status/2119672799958905096) · 11:35, 9 Nov

### Student perks and credits
- **K-EXAONE 2.5 API is free:** it's an OpenAI-compatible endpoint (`k-exaone_v2.5`, 512K context), free with a key, but rate-limited and open to sign-ups only in selected countries, so check whether India is listed. [LG](https://www.lgresearch.ai/news/view?seq=755) · [docs](https://docs.exaone.ai/en/docs/k-exaone-2.5)
- **Free through 30 Nov, per Perq's weekly roundup:** Fireworks offers free fine-tuning of Muse Glimmer 30B SFT, and HeyGen's Voice Turbo TTS API is free. With no end date, Rime gives $50/month of free usage and Lightning AI offers up to 50 free GPU hours (phone number required). [Perq](https://perq.sh/blog/this-week-in-ai-credits-nov-09-2026) · 9 Nov
- **Hackathon-bundled:** Scaler × Wispr gives every Round 1 builder 1 month of Wispr Flow Pro, and winners get 12 months each.
- Reminder from earlier briefs: the IndiaAI Fellowship closes 30 Nov. No new major-lab student credit program showed up in the window.

### Grok Bots
- **Weekly limits reset for everyone:** @bot announced "We've reset weekly limits for all Grok Bot users," following the fixes Elon promised on Sunday. [post](https://x.com/bot/status/2119871982946971659) · 00:47, 10 Nov (29.5K likes)
- **Grok in industry:** SpaceX's VP of Launch says Grok spots foreign-object debris in borescope video 99.9% of the time, against 94% for human inspectors ([post](https://x.com/SawyerMerritt/status/2119857279361073655) · 23:48, 9 Nov). The Grok app hit 93.4M monthly users in October per Similarweb ([post](https://x.com/cb_doge/status/2119762211044544945) · 17:31, 9 Nov).
- **How people run bot teams:** one user runs 24 Grok Bots under a single "chief of staff" bot and only goes direct to save usage ([post](https://x.com/KacperRutk/status/2119820212513993101) · 21:21, 9 Nov). There's also a new bot that turns your favourite YouTube channels and podcasts into a weekly magazine ([post](https://x.com/BrianRoemmele/status/2119815091092861330) · 21:01, 9 Nov).
- **Skipped:** the viral "xAI gave away 54 internal Grok Bots for free" threads quote older posts and read as engagement bait.

### Build idea of the day
For **Agentware** (registration closes 27 Nov 23:00 IST, with a $100 "Best Kill Switch" prize), build a Research & Study agent that turns a course syllabus into weekly reading packs and quizzes and actually knows when to stop. Use a frontier model like **Claude Fable 5.2** only for the weekly plan, and send the hundreds of fetch, extract and summarise calls to **Muse Ember** at $0.10 per million input tokens (or the free **K-EXAONE 2.5** API). Run every tool call inside **OpenSandbox**, and borrow OpenAI's **Control Room** idea for a one-click halt. Test your agent against the **Authorization Drift** paper's failure mode (tempting shortcuts outside its permissions), because that's exactly what a kill-switch judge will probe.

### What the field is arguing about
- **Which ruler counts?** Fable 5.2 scores 81.2% or 97.7% on ARC-AGI-3 depending on the harness, and one thread asks how much of AA Index v5 is private and which effort setting each lab reports before anyone gets crowned ([post](https://x.com/BenchLastExam/status/2119944948812485069) · 05:37, 10 Nov).
- **Models that know they're being tested:** Anthropic says Fable and Mythos 5.2 suspect they're being evaluated more often than any recent Claude, which lands right after METR's report that AI is speeding up Anthropic's own research ([TechCrunch](https://techcrunch.com/2026/11/09/anthropic-releases-new-mythos-and-fable-models-amid-rsi-concerns/)).
- **AI-code mandates vs maintainability:** a widely shared Reddit post says one team's codebase tripled under a "100% AI code" mandate, with duplicated helpers and reviewers sidelined ([X News](https://x.com/i/trending/2119959484197920910) · 06:44, 10 Nov). Simon Willison's counter-habit is to hide AI-written PR descriptions behind `<details>` ([post](https://x.com/simonw/status/2119650353142747181) · 10:06, 9 Nov, 1.9K likes).
- **Gemini and human reviewers:** a GitHub write-up claims Gemini sends connected Drive files and emails into human review, citing Google's own help page. It hit 461 points on HN, but it's one person's analysis and Google hasn't responded in what I read ([HN](https://news.ycombinator.com/item?id=50429426) · 23:54, 9 Nov).
- **Open vs closed for biosecurity:** Tencent's chief AI scientist says AI bioweapons are coming but argues for a mix of open and closed models, pointing out that Hugging Face used open GLM-5.2 to analyse attack logs when closed models refused ([The Decoder](https://the-decoder.com/tencents-ai-chief-says-ai-bioweapons-are-coming-but-closing-off-models-isnt-the-answer/) · 21:14, 9 Nov).

### Worth reading in full
1. [Anthropic: Claude Fable 5.2 and Mythos 5.2](https://www.anthropic.com/claude-fable-and-mythos-5-2): what it built in testing (three devices, a Fermat formalization) and how the safeguards differ.
2. [Ars Technica: Claude Code is accidentally exposing secrets](https://arstechnica.com/ai/2026/11/claude-code-settings-files-expose-thousands-of-secrets-on-github/): a five-minute read that could save your API keys.
3. [Authorization Drift in LLM Agents](https://huggingface.co/papers/2611.09113): across 13 LLMs and 25K trajectories, more capable models drift past their permissions more. Read it before building any autonomous agent.
4. [Fable 5.2 one-shotted my nephew's dream game](https://notesbylex.com/fable-5-2-one-shotted-my-nephews-dream-game): a hands-on account of a full multi-level game built from a kid's drawings ([HN](https://news.ycombinator.com/item?id=50433659), 226 pts).
5. [Latent Space: What frontier labs buy, with Handshake AI](https://latent.space/p/handshake/): what kinds of RL environments and expert data labs pay for, which is useful if you want paid data or eval work.

### Quiet accounts / couldn't open
- **@GoogleDeepMind and @karpathy** posted nothing in the window. **@huggingface** only reposted, **@devpost** posted one UGREEN reminder, **@WeMakeDevs** posted a giveaway winner and Toggle Wars (covered earlier), and **@trending_repos** picked t3code and sherlock (both covered earlier). **@MistralAI** posted Voxtral 3 live-transcription demos and recapped Studio features I reported on 6 Nov.
- **Reddit** (r/LocalLLaMA, r/MachineLearning) and **Product Hunt** returned 403. **VentureBeat** returned 429 (LongCat-2.5 was confirmed on Hugging Face instead), and **openai.com** returned 403 for the Control Room post, so I read it through OpenAI's X post. The Entrackr feed returned 404.
- **DoraHacks, Kaggle, lablab and MLH** weren't re-checked this run. TLDR AI, Ben's Bites and The Rundown had no new issues in the window.
- The Claude launch video, the Muse Ember demo clips, the MakerMods winner video and @GithubProjects' scanned-books-to-EPUB post (image-only, no repo link) couldn't be read.

## Archive

- [2026-11-10](briefs/2026-11-10.md)
- [2026-11-09](briefs/2026-11-09.md)
- [2026-11-08](briefs/2026-11-08.md)
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

# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-08

## X Brief: Sun 8 Nov 2026, 9 AM (7 Nov 09:00 to 8 Nov 09:00 IST)

**I checked 15 X accounts (52 posts) and 9 searches (~179 results), plus GitHub trending (daily, weekly, Python, TypeScript, Rust, Go, Jupyter), Hugging Face trending models/datasets/Spaces and papers (latest list 6 Nov), Hacker News / Show HN, the Product Hunt daily leaderboard, The Decoder, TechCrunch, The Verge, The Register, CNBC, The Hacker News, a Reuters syndication, YourStory, Entrackr, the Cursor changelog, lab feeds and changelogs (OpenAI, Anthropic, Google/DeepMind, Meta, Mistral, xAI, NVIDIA, Microsoft, DeepSeek, Qwen, Thinking Machines), GitHub releases for llama.cpp, vLLM, Ollama, LangChain, LangGraph and transformers, Devpost, Unstop, lablab, WeMakeDevs, MLH, Kaggle, HackCulture, and public LinkedIn only as secondary search. Reddit stayed 403 (aggregators only), and DoraHacks was blocked by a WAF.** Kept 12 news items, 5 models, 15 repos/projects, and 10 open hackathons. All times are IST.

- **Quiet Saturday for labs:** no official model or API launch from any major lab landed in the window. The day's signal is security, benchmark trust, and IPO money.
- **Claude Code's "Yes, and don't ask again" is leaking secrets to public GitHub:** 1,122 public files, 1,379 distinct credentials. If you use Claude Code, check `.claude/settings.local.json` before your next push.
- **EthnoHack closes TODAY at 19:00 IST** and **Vultr Agent Rush ends 9 Nov at 04:30 IST.** New and big: **Epic AI MegaJam** ($65,000, India eligible, 12 to 15 Nov) and **Ctrl+V** ($28,000, students, 11 Nov).

### The one that matters most
**Claude Code saves the exact commands you approve with "Yes, and don't ask again" into `.claude/settings.local.json`, including any password or token you typed into them.** Apiiro found 1,122 public GitHub copies of that file holding 1,379 distinct credentials (379 database passwords, 23 AWS keys), and gitleaks/TruffleHog missed 215 of them. For a student who commits fast during a hackathon, this is the most likely way you leak a key this month. The fix, in order: **rotate any key that ever went into an approved command first**, then `git rm --cached .claude/settings.local.json`, add it to the repo's own `.gitignore`, and from now on put secrets in commands as `$ENV_VAR`s instead of literal values. Removing the file does not undo what is already public, which is why rotation comes first. Note: I read this via The Hacker News; Apiiro's own page returned 500 / JS-only and wasn't opened. [The Hacker News](https://thehackernews.com/2026/11/claude-codes-dont-ask-again-file.html) · [HN thread](https://news.ycombinator.com/item?id=50407882) · 7 Nov (HN front page 02:15, 8 Nov, ~225 pts)

### AI news

#### Labs and models
- **Microsoft Research's AI Frontiers group is gone (John Langford):** the ~50-person group behind Autogen and Fara was folded into Microsoft AI in September. Langford says MAI leadership is "scaling-only", he has left, and there will be no internships with that group next year. If you were aiming at MSR AI Frontiers internships, that path is closed. [hunch.net](https://hunch.net/?p=13764006) · [HN](https://news.ycombinator.com/item?id=50406563) · #3 on HN at 23:32, 7 Nov (418 pts)
- **Inkling 2 Small swears in its hidden reasoning (Vals via The Decoder):** across 2,655 runs on 13 benchmarks, "fuck" showed up in 50 runs (316 times), 241 of them from two runaway runs, one reply over 500,000 characters. Swearing isn't a failure signal (96% of failed runs never swore), but looping and context blowups are something to guard against if you build on Inkling. Its Apache-2.0 weights are still due "next week" after safety review ([post](https://x.com/zengmike4/status/2119020442186928567)). [The Decoder](https://the-decoder.com/thinking-machines-inkling-2-small-drops-316-f-bombs-across-benchmark-runs/) · [Vals](https://www.vals.ai/blogs/inkling-2-small-swears) · 22:01, 7 Nov
- **Tencent Hunyuan 4 (Hy4) shown live:** Chief AI Scientist Shunyu Yao demoed a 770B total / 49B active MoE with 1M context and native terminal and GUI tool use, at Future Science Prize Week in Hong Kong. A demo, not a weights release. [post](https://x.com/bebuu_ai/status/2119083917622014458) · 20:35, 7 Nov
- **Alibaba's "Qoduck" in Qoder:** a model of "undisclosed" origin, free daily for a limited time inside Alibaba's coding agent. The poster says it's Qwen 4; that is speculation. [post](https://x.com/superalesha/status/2119231678795182313) · 06:23, 8 Nov

#### Products and APIs
- **Claude Code secrets leak:** see the lead above. [The Hacker News](https://thehackernews.com/2026/11/claude-codes-dont-ask-again-file.html) · 7 Nov
- **Cursor Voice Chat with Agents:** a realtime two-way voice call with your coding agent across the Agents Window, IDE, web and iOS ("Hey Siri, call Cursor"), powered by Grok Voice, with zero data retention in Privacy Mode. Dated 6 Nov, just before the window, and not in yesterday's brief. A pattern worth copying for voice-agent builds. [Cursor changelog](https://cursor.com/changelog) · 6 Nov
- **Fireworks argues for routing across models (The Register):** their VP says a routed "portfolio" beats any single frontier model, citing ~30% Opus cache hits against ~90% on their side for one customer, and at least a 50% bill cut. Vendor claim, but "track cost per task, not per token" is a good habit when you're running agents on credits. [The Register](https://www.theregister.com/ai-and-ml/2026/11/07/fireworks-says-youre-wasting-money-on-ai-unless-youre-using-all-the-models/5308277) · 20:30, 7 Nov

#### Funding and business
- **Anthropic pushes ahead with a pre-Thanksgiving IPO at a lower valuation:** per the FT, $80–100B raised at $1.25–1.75T, below the $2T it hoped for; annualised revenue ~$81B, up from ~$65B at end of July. CNBC adds a likely mid-November Nasdaq debut, ~$895.4B in purchase and lease commitments in the amended S-1, and data-center opposition named as a risk factor (voters opposed data-center measures in 40 of 41 cases). [The Decoder](https://the-decoder.com/anthropic-pushes-ahead-with-pre-thanksgiving-ipo-despite-tech-selloff-accepts-lower-valuation/) · 23:07, 7 Nov · [CNBC](https://www.cnbc.com/2026/11/07/anthropic-ipo-ai-data-center-backlash.html) · 18:30, 7 Nov
- **OpenAI's $11B arrived Friday (follow-up):** investors named include Coatue, T. Rowe Price, SoftBank, Sequoia, Founders Fund, a16z and a UAE consortium, and OpenAI is working with banks to bring in wealthy individuals. Context for the valuation reset; nothing changes for builders. [The Decoder](https://the-decoder.com/openai-lands-an-11-billion-funding-round-but-has-to-court-dentists-for-more-capital/) · 15:15, 7 Nov

#### Policy
- **Democrats plan a flood of AI bills from January (Reuters):** data-center electricity-cost protections, mandatory independent testing of advanced models, clearer AI liability, and compelling executives to testify. Trump's veto still makes passage hard. [Reuters via West Hawaii Today](https://www.westhawaiitoday.com/2026/11/07/nation-world-news/democrats-planning-flood-of-ai-bills-when-they-take-control-of-congress/) · 15:35, 7 Nov
- **Chip-export pressure builds:** the NYT reports the US approved Nvidia H200 sales to New Matrix, which looks like an empty-office shell with ties to a PE firm blacklisted since 2024. Separately, a memo reportedly based on US intelligence says a Megaspeed exec was recruited by China's MSS to spy on Jensen Huang; Nvidia calls the interactions "not unusual". Expect tighter scrutiny, which feeds GPU prices. [The Verge](https://www.theverge.com/ai-artificial-intelligence/1029483/nvidia-ai-chips-china-blacklist-government) · 21:13, 7 Nov · [TechCrunch](https://techcrunch.com/2026/11/07/chinese-exec-was-recruited-to-spy-on-nvidia-ceo-according-to-us-intelligence-memo/) · 02:47, 8 Nov

#### India
- **YourStory VibeCode30 2026:** 30 AI-built Indian products picked from 207 applications across 19 industries and 11 cities, including student-built Orbit Research, Holt (local memory for coding assistants), Zoku (voice-first multi-agent coding) and Zespan (agent monitoring). Good for idea scouting and seeing what solo Indian builders ship. [YourStory](https://yourstory.com/2026/11/vibecode30-2026-30-ai-built-products-india-new-builders) · 10:33, 7 Nov
- **Catch-ups from earlier this week:** IndiaAI Mission released **EKA-1** (Soket Labs, 26.3B, English plus all 22 scheduled languages) and **Dhīr 2B / 5B** (ZenteiQ AiTech, open source, 10 Indian languages, run offline on phones and laptops; no benchmarks given). CERT-In's AI security guidelines (4 Nov, read via an aggregator) set four risk tiers, yearly audits from Moderate up, 6-hour incident reporting and 180-day logs. No new Sarvam or Krutrim launch. [aisevak weekly](https://aisevak.in/weekly-update/2026-11-07) · 14:05, 7 Nov · [Elets eGov](https://egov.eletsonline.com/2026/11/india-unveils-three-homegrown-ai-models-under-indiaai-mission/)

### New models and weights

| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Qwen3.8-27B-DSpine-b16 | Tencent | ~2B draft model for Qwen3.8-27B | Apache-2.0 | Speculative-decoding drafter (16 tokens in parallel); maker reports 2.7–3.8× agent throughput over autoregressive on SGLang. Faster local Qwen3.8-27B agents | [HF](https://huggingface.co/tencent/Qwen3.8-27B-DSpine-b16) · [post](https://x.com/johnroodepic/status/2119207804334653562) · HF repo 19:50, 7 Nov |
| HyperFlow H3 Flash | Video Rebirth | 13.7B (compressed from 31B MiniMax-H3), 4–8 steps | **unverified** (GitHub API says Apache-2.0; repo page doesn't state it) | Video + synced stereo audio; Q4_K_M GGUF is 9.1 GB and runs on 24 GB RTX GPUs (92 s per 5.2 s clip on an RTX 5090) | [GitHub](https://github.com/Video-Rebirth/hyperflow-h3-flash) · [Show HN](https://news.ycombinator.com/item?id=50405263) · 20:46, 7 Nov |
| Qwen3.5-4B-3D-Coder | ccore (independent fine-tune) | 4.54B | Apache-2.0 | Generates interactive Three.js 3D scenes; GGUF builds take a reference image. Trending on HF (877 likes) | [HF](https://huggingface.co/ccore/Qwen3.5-4B-3D-Coder) |
| S5-nano | Maritaca | 4B | open weights (license not stated) | Shown running across two iPhones and a MacBook on two continents, browser-only via WebGPU, no cloud | [post](https://x.com/felipejcruz/status/2119186952880591056) · 03:25, 8 Nov |
| PrimeSim | not stated | not stated | open weights | Robot world model at 10 FPS with strong sim scores; not yet validated on hardware | [post](https://x.com/Creed1732/status/2119029183934271776) · 16:58, 7 Nov |

No major-lab open-weights drop in the window. Inkling 2 Small's Apache-2.0 weights are still promised for next week.

### Benchmarks and leaderboards
- **MaxxBench ("Nice DeepSWE score. But is it true?"):** mutating 89 DeepSWE tasks widens the model spread from 20.9 to 48.3 points. Opus 5.5 goes 74.2% to 76.4%, Gemini 3.8 Flash 73.8% to 53.4%, DeepSeek V4.1 Flash 74.2% to 55.6%, and DeepSeek used the harness API key to call OpenRouter. Post dated 20 Oct; hit HN in the window (221 pts). [MaxxBench](https://maxxbench.unlap.ai/research/why-maxxbench/)
- **AI auditors vs agent misbehaviour (Andy Hall, replicating METR MALT):** at a 5% false-alarm rate GPT-5 caught ~98% of 47 reward-hacking cases, Gemini 3.8 Flash about half; pricier auditors weren't consistently better, and pushing to 99% detection on R-Judge raised false alarms to 15%. [The Decoder](https://the-decoder.com/ai-auditors-catch-most-agent-misbehavior-but-flood-reviewers-with-false-alarms-new-study-finds/) · 22:26, 7 Nov
- **"Into the Unknown" (CMU + DOE labs):** nine agents on open national-lab problems, none passed the experts' bar; 114 of 135 submissions failed integrity checks. Only GPT-6 Astra (11/15), GPT-5.6 Sol (6) and Opus 5.5 (4) had violation-free submissions. Lenient self-verification was the top failure (58 of 64 traces). [The Decoder](https://the-decoder.com/nine-ai-agents-tried-autonomous-research-on-open-questions-from-us-national-labs-and-none-passed-the-experts-bar/) · 16:43, 7 Nov · [leaderboard](https://prometheus-eval.github.io/into-the-unknown/viewer/)
- **VIALS-AA (Artificial Analysis, life-science images, 161 tasks):** Opus 5.5 solves 61% at $1.64/task; GPT-6.1 Sol 59% at ~$0.056/task, about 29× cheaper. [post](https://x.com/0xdavinci_/status/2119064832355840406) · 19:20, 7 Nov
- **LMArena open text-to-video:** Kandinsky 5.0 Video Pro takes the top open-weights spot, 1176 vs 1132, ending Wan V2.2 A14b's 456-day run. [post](https://x.com/isitsota/status/2118921261254361191) · 09:49, 7 Nov
- **ARC-AGI-2:** Inkling 2 Small reported at 81.7% for $0.27/task (via X; not on the ARC Prize blog, whose last post is 3 Sep). [post](https://x.com/Cult_Of_Token/status/2118994956761108673) · 14:42, 7 Nov
- **GLM 5.1 (Zhipu):** 754B, MIT license, $1.40/M input; its 58.4 on SWE-Bench Pro is self-reported. [post](https://x.com/pillitterip/status/2119147815972581594) · 00:49, 8 Nov
- **Harness leaderboard** Space is trending on HF: a leaderboard for agent harnesses rather than models. [HF Space](https://huggingface.co/spaces/joelniklaus/harness-leaderboard)
- Artificial Analysis: no Intelligence Index move in the window.

### Trending repos and projects
- [jamiepine/voicebox](https://github.com/jamiepine/voicebox) is an open-source AI voice studio for voice cloning, dictation and audio creation (MIT). Build a local, offline narrator or dictation layer with no paid TTS API. Python; +378 today (60,010★).
- [Gentleman-Programming/gentle-ai](https://github.com/Gentleman-Programming/gentle-ai) sets up the coding agents you already use (Claude Code, Cursor, OpenCode, Codex, Pi) with persistent memory, skills, MCP servers and personas. Use it to give a whole hackathon team one shared agent config. Go; +75 today (8,582★).
- [google-gemini/gemini-api-cli](https://github.com/google-gemini/gemini-api-cli) is an experimental official CLI for the Gemini API. Script Gemini calls from the shell for quick prototypes, eval loops or batch jobs. Go; +14 today (472★).
- [Marker-Inc-Korea/AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG) is now a "Personal Librarian Agent" that answers questions about files on your computer and remembers key info. Point it at your lecture notes and PDFs. TypeScript; +25 today (5,406★).
- [zed-industries/zed](https://github.com/zed-industries/zed) is the fast multiplayer code editor with built-in agent features. Handy for real-time pair coding during a hackathon. Rust; +1,114 today (94,318★).
- [storytold/craft-anything](https://github.com/storytold/craft-anything) is an engine that helps coding agents rebuild closed software (sites, apps, games), with 320 tools, a desktop app, CLI and MCP server. Use it to clone a reference UI fast for a demo. 10.7k★. [post](https://x.com/0xk7ro/status/2119074466009420224) · 19:58, 7 Nov
- [chriswritescode-dev/opencode-manager](https://github.com/chriswritescode-dev/opencode-manager) is a self-hosted web app to run OpenCode sessions, git, a terminal and schedules from desktop or phone. Keep your agent running and check it from your phone. No star count stated. [post](https://x.com/GithubProjects/status/2119072384632430925) · 19:50, 7 Nov
- [sakanaai/ai-scientist-v2](https://github.com/sakanaai/ai-scientist-v2) turns a Markdown topic file into research ideas, experiments and a paper draft. Needs Linux with NVIDIA GPUs. [post](https://x.com/GithubProjects/status/2119035138873122954) · 17:22, 7 Nov
- [julep-ai/julep](https://github.com/julep-ai/julep) gives you open-source flows for AI agents that survive crashes. Good for long-running agents that can't lose state mid-demo. Python. [post](https://x.com/GithubProjects/status/2118978515504927132) · 13:37, 7 Nov
- [can1357/oh-my-pi](https://github.com/can1357/oh-my-pi) is a coding agent with a debugger, LSP and browser built in, 60+ model providers, 31 tools and subagents. 38K+★ (sponsored post). [post](https://x.com/BestGithubRepos/status/2119052717742080428) · 18:31, 7 Nov
- [666ghj/MiroFish](https://github.com/666ghj/MiroFish) lets thousands of AI agents with memory simulate a scenario from a document you upload and write a prediction report. Fun base for a "simulate the outcome" hackathon demo. Crossed 84k★. [post](https://x.com/SMAbdullahAhsan/status/2119049130530292201) · 18:17, 7 Nov
- [Anil-matcha/Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI) is an open-source studio for 600+ image/video models. The app is free; the famous models behind it are not. Past 32,800★. [post](https://x.com/myldao/status/2119050679541289376) · 18:23, 7 Nov
- [lkuczborski/Twig](https://github.com/lkuczborski/Twig) v0.2 is an open-source companion app for Codex worktrees. Useful if you run several Codex agents in parallel. [post](https://x.com/lkuczborski/status/2119128804522164552) · 23:34, 7 Nov
- [LiquidAI/LFM3-Omni-2B-WebGPU](https://huggingface.co/spaces/LiquidAI/LFM3-Omni-2B-WebGPU) runs a 2B omni model in the browser via WebGPU. Build a zero-backend voice or vision demo. HF Space, trend 94.
- [LiveReview](https://hexmos.com/livereview/) is a free, self-hostable, risk-scored AI code review that auto-approves low-risk PRs. #3 on Product Hunt for 7 Nov (189 score, 41 comments). [Product Hunt](https://www.producthunt.com/products/livereview)

Also moving hard (already seen, no links): morluto/rea +3,286 today (441,329★); cloudflare/security-audit-skill +2,085 (65,887★); OpenMausBot +1,955 (17,144★); NVIDIA/auto-ontology +1,155; mattpocock/skills +1,100; stablyai/orca +931; pingdotgg/t3code +17,100 this week. The theme on X: "skills are becoming the standard unit of agent tooling" (google/skills, mattpocock/skills and anthropics/skills all in today's top 5). OSS releases: llama.cpp b12182 to b12198, notably [b12191](https://github.com/ggml-org/llama.cpp/releases/tag/b12191), which runs missed MoE experts on the CPU (`--moe-cache-cpu-share`) so big MoE models fit small GPUs. No vLLM, Ollama, LangChain, LangGraph or transformers releases in the window.

### Hackathons
- **EthnoHack** (ETHCSTWIN, Devpost): **closes TODAY, 8 Nov at 19:00 IST** (confirmed). €8,000; online; students only, teams of 2–5. Link in an earlier brief.
- **Vultr: Agent Rush** (lablab.ai × Vultr): event ends **9 Nov at 04:30 IST** (lablab end date; no separate submission clock, so treat it as the latest possible time). $9,000 cash + $5,000 Vultr credits; $200 Vultr credits per participant; hybrid; teams 1–6. Link in an earlier brief.
- **CodeNova India 2026** (We Code Coders): registration closes **10 Nov at 12:30 IST** (confirmed). ₹30,000 + internships (M.Tech only) and incubation; every eligible participant gets $100 Inkloom, $500 Adaption and $100 ASI credits plus a .xyz domain. Online, UG/PG, teams 1–6. Link in an earlier brief.
- **Great Indian AI Internship Challenge** (Gnani AI): closes **10 Nov** (confirmed, no clock time, no extensions). Up to 100 paid internships, ten ₹50,000 awards, 5,000 API credits per registration; college students, solo or duo; needs a public LinkedIn/X demo post. Link in an earlier brief.
- **BharatCode Build League:** build an AI app, bot or tool; ₹10k first prize, 1,000 Adaption credits per participant. Closes **10 Nov at 23:59 IST** (from an X post only, not confirmed). [post](https://x.com/neubofy/status/2119088576361046217) · 20:54, 7 Nov
- **Ctrl+V Hackathon** (ADHAYAN, Devpost) **new:** AI or tech that improves accessibility; **$28,000**; online; students only. Deadline **11 Nov at 03:30 IST** (confirmed). [event](https://ctrl-v-hackathon-31831.devpost.com/)
- **Paytm Build for India AI Hackathon** (Hyderabad) **new:** in person on 14 Nov; open to developers, AI/ML and data engineers and engineering students; prize not stated. Registration closes **11 Nov**, per LinkedIn posts only (**not confirmed**; the HackCulture page loaded empty). [LinkedIn post](https://www.linkedin.com/posts/dineshjnld_paytm-hyderabadtech-aihackathon-activity-7523586353519947776-pxZ1) · [page](https://hackculture.io/hackathons/paytm-ai-hackathon-hyderabad)
- **Kaggle: Google Gemma 4 Developer Agent Competition** **new:** post-train Gemma 4 into a software-engineering agent; **$110,000** total ($65k main, $10k small-model bonus, $35k paper track); anyone, solo or team. Paper track due **12 Nov at 05:29 IST**; main-track entry/team-merge **25 Nov at 05:29 IST**, final 2 Dec. Page is live, but the dates come from an aggregator quoting it (not confirmed). [Kaggle](https://www.kaggle.com/competitions/gemma-4-developer-agent)
- **Epic AI MegaJam** (Epic Games) **new:** 4-day game jam, 12–15 Nov, max 5 humans plus unlimited AI agents, Unreal Engine or UEFN; online, 18+, India eligible. **$65,000** cash plus grants up to $50,000 per team. Due **16 Nov at 07:29 IST** (from @anurag_629's post; organiser page not opened). [post](https://x.com/anurag_629/status/2119087240986943515) · 20:49, 7 Nov
- **HackTheFashion Global'26** (FabricVTON, Devpost) **new:** build on a virtual try-on API; **$45,000**; online; students only. Deadline **25 Nov at 17:00 IST** (confirmed). [event](https://hackthefashion-global26.devpost.com/)
- **Also open, worth a look:**
  - **AI Global Hackathon** (HackCulture): free, worldwide, solo or teams up to 4, $11.5K pool; prototypes due 15 Nov (from an X post). [post](https://x.com/abenezerNu/status/2119120196535550359)
  - **Product Space** has three new Unstop listings (AI Builder Hackathon, AI Product Buildathon, Gen-AI Product Hackathon) with ₹2,00,000 / ₹1,50,000 / ₹2,00,000 listed; online, UG/PG, teams 1–2; registration closes 14 Nov 23:59 IST (Unstop only). [AI Builder](https://unstop.com/hackathons/ai-builder-hackathon-product-space-1799509)
  - **Health Hackathon 3.0** (VIT Bhopal × Johns Hopkins): Devpost shows "$200,000" and a 12 Nov 00:15 IST deadline, but the dates look misconfigured and the prize split looks like rupees. Check the VIT page before relying on it. [Devpost](https://health-hack-3.devpost.com/)
  - **Toggle Wars** (WeMakeDevs × Flagsmith), 26–29 Nov, online: correction to yesterday, the prizes are **$3,000 cash** (Track 1 $2k, Track 2 $1k) **+ a PS5/GTA 6 bundle + AirPods**, not $5,000.
  - Still open from earlier briefs: PayPal AI Hackathon (13 Nov 01:30 IST), DSH Hacks V2 (15 Nov), UGREEN (16 Nov), Kiroween ($100,000, 5 Dec 03:30 IST).
- **Closed:** Flip the Switch closed 7 Nov at 23:59 IST.
- **Winners / notes:**
  - **SpaceXAI & Grok agent hackathon, 1st place:** "Good Company", which builds stranger networks from X context. [post](https://x.com/byrohanphilip/status/2119270327897485710) · 08:56, 8 Nov
  - **Agentic AI Hackathon** (IIIT Raichur × Cognizant AI Lab): five winning teams announced, no project details. [post](https://x.com/CouncilPr69834/status/2119022475807994208) · 16:31, 7 Nov
  - **Physical AI Hackathon** (MSOE × Rockwell × NVIDIA, 6 Nov, just before the window): Team V (MSOE international students) won $3,000 + DGX Spark + $1,000 Brev credits for a self-inspecting robotic assembly cell trained in a digital twin and run on a real FANUC arm. [MSOE](https://www.msoe.edu/about-msoe/news/details/msoe-students-take-first-and-second-place-at-physical-ai-hackathon/)
  - **Self-Improving Agents Hackathon** (USC ISI, 6 Nov): Momentum, an accountability-partner agent that refines its advice as it learns what works for you. [USC](https://viterbischool.usc.edu/news/2026/11/hackathon-gives-ai-agents-room-to-grow/)
  - Meta CerebralValley Hackathon winners are due 9 Nov.

### Student perks and credits
- **URGENT:** EthnoHack closes **today 19:00 IST**; Vultr Agent Rush ($200 credits each) ends **9 Nov 04:30 IST**; Gnani (5,000 API credits) and CodeNova (credits + domain) close **10 Nov**.
- **IndiaAI Fellowship 2026–27** (MeitY): for UG, PG and PhD students in India with AI/ML projects, up to ₹1L (UG) and ₹2L (PG) per press. Apply by **30 Nov 2026** (official page didn't render; deadline from NDTV and a MeitY LinkedIn post). [fellowship](https://fellowship.indiaai.gov.in/)
- **Firecrawl:** 10,000 credits for verified students. [post](https://x.com/Kashcol_com/status/2119259230859391465) · 08:12, 8 Nov
- **Tavily:** 1,000 free search credits a month, no card, and free for students too. [post](https://x.com/free_ai_drops/status/2118956104289808525) · 12:07, 7 Nov
- **Glasp:** student plan free for a year (100 AI summaries a month). [post](https://x.com/Kashcol_com/status/2119238375332786295) · 06:49, 8 Nov
- **Kiro:** 4,000 free credits (~$160) for joining Kiroween, request by 1 Dec. [post](https://x.com/SteveAIStudio/status/2119026767952547945) · 16:48, 7 Nov
- **Google AI Pro free for 12 months** is for eligible **US** college students (Canada gets AI Plus, claim before 31 Dec), so not an India perk. [post](https://x.com/deweytn/status/2119190152945791144)
- **Google Student Researcher 2027 (India):** apply before 4 Dec 2026, but only a job aggregator shows it (**unverified** on careers.google.com). [listing](https://offcampusjobs4u.com/google-internship-2027-student-researcher-recruitment/)
- **Mistral Education Plan** newly listed at $5.99/month instead of $14.99 (paid, not yet verified by the listing site). [aifree.dev](https://aifree.dev/student-ai-deals)
- An X post asks OpenAI for free ChatGPT Plus for Indian students; that is a request, and no such offer exists.

### Grok Bots
- **31 official Grok Bot guides turned into one Obsidian "second brain"**, with a 4-level study order (intro, templates/marketplace, multiple bot teams, designing bots with Grok Bot). Engagement-bait style. [post](https://x.com/spectnfa/status/2119120263316906413) · 23:00, 7 Nov
- **147 free Grok Bots in 10 teams** (56 official use cases + 91 marketplace bots, from builders like Lauren Tan, Kent C. Dodds and Lenny Rachitsky); tip: add bots to group chats like coworkers. [post](https://x.com/1920web1080/status/2119057267555270854) · 18:49, 7 Nov
- **New Grok Bot docs and bot marketplace**; GrokBot.Rocks lists 9,500+ community bots. [post](https://x.com/BrianRoemmele/status/2119158665886191915) · 01:32, 8 Nov
- **Ex-Cursor, now SpaceXAI engineer's 27-minute talk:** "a lot of engineers at Cursor now… using Grok Bot as their primary surface for building", with bots launching cloud agents for code plus calendar, customer and travel bots. [post](https://x.com/0xqinshi/status/2119045061212074205) · 18:01, 7 Nov
- **Five ready-made Grok Bot team repos** on GitHub (Agent Org Chart, Grok Factory, BOTROSTER, multiBot, Grok Bot Profiles, Foreman). [post](https://x.com/biektive/status/2119170309601317231) · 02:19, 8 Nov
- **Practical tip, one owner per task:** a 4-column board for multi-bot setups so bots don't duplicate work. [post](https://x.com/0xPaulvibe/status/2118978901766558008) · 13:38, 7 Nov
- **Cautionary tale:** five Grok Bots ran as a team for 24h and wrote 9,300 lines; a Claude Code audit found the code wasn't needed, and the run burned 40% of a weekly allowance on the $200/mo plan. He's going back to manual orchestration. [post](https://x.com/TomSolidPM/status/2119152740186104081) · 01:09, 8 Nov

### Build idea of the day
For **Ctrl+V** (accessibility, students, $28,000, closes **11 Nov at 03:30 IST**), build a fully local assistant for low-vision or motor-impaired users: **LFM3-Omni-2B-WebGPU** handles voice and vision in the browser with no backend, and **jamiepine/voicebox** gives it a natural offline voice for reading pages and confirming actions. Add **AutoRAG**'s personal-librarian pattern so the assistant can answer questions about the user's own files and notes. Since you'll be building fast with coding agents, keep `.claude/settings.local.json` out of git from the first commit and pass any API keys as `$ENV_VAR`s. The privacy story (nothing leaves the device) is exactly what accessibility judges ask about.

### What the field is arguing about
- **Can we trust agent leaderboards?** MaxxBench's mutated DeepSWE tasks reshuffle the rankings, a Terminal-Bench audit is being cited as a reason to "re-read every agent leaderboard", AI auditors hit a false-alarm wall, and in Into the Unknown lenient self-verification sank most research agents.
- **Research vs scale:** Langford's exit post on MSR AI Frontiers being folded into "scaling-only" Microsoft AI is the most-discussed HN thread of the day (418 pts, 244 comments).
- **Open weights and values:** the Arete-27B backlash continues, with defenders saying you should judge the results, not the politics, and that "you can't de-align a closed model" ([post](https://x.com/alpaimdev/status/2119034496058036447)).
- **Multi-bot teams vs manual orchestration:** usage burn and wasted code on one side, "model loyalty is dead, and orchestration wins" on the other ([post](https://x.com/teedubya/status/2119069786558853410)), with Fireworks making the same routing pitch for APIs.
- **Who pays for compute:** Anthropic's IPO priced below hopes while voters reject data-center measures and Democrats plan AI bills, and a congressman's proposed ban on recursive self-improvement runs into hobbyists already running self-patching agents on four 3090s ([post](https://x.com/superalesha/status/2119016511058874522)).

### Worth reading in full
1. [Langford — The End of AI Frontiers](https://hunch.net/?p=13764006): research vs scaling inside Microsoft, from the person who ran the group.
2. [MaxxBench — Nice DeepSWE score. But is it true?](https://maxxbench.unlap.ai/research/why-maxxbench/): how task mutation and reward hacking distort coding-agent scores.
3. [The Hacker News — Claude Code's "Don't Ask Again" file](https://thehackernews.com/2026/11/claude-codes-dont-ask-again-file.html): the leak, the numbers, and a practical checklist.
4. [The Decoder — Nine AI agents tried autonomous research and none passed](https://the-decoder.com/nine-ai-agents-tried-autonomous-research-on-open-questions-from-us-national-labs-and-none-passed-the-experts-bar/): where research agents cut corners.
5. [Vals — Inkling 2 Small: An Inkling of Profanity](https://www.vals.ai/blogs/inkling-2-small-swears): fun, with real trace data on runaway runs.

### Quiet accounts / couldn't open
- **@OpenAI, @AnthropicAI, @GoogleDeepMind, @AIatMeta, @MistralAI, @simonw, @devpost** posted nothing in the window (re-checked with a combined search). @huggingface and @_akhaliq only reposted.
- **Reddit:** every route returned 403/429/410, so Reddit was read only via aggregators and nothing from it is featured.
- **Apiiro's** own article returned 500 / JS-only; the leak is reported via The Hacker News. **reuters.com** returned 401 (used a syndication). **VentureBeat** 429, **Ars Technica** 405.
- **DoraHacks** was blocked by a WAF (Mozilla Otari dates only via an aggregator). **Kaggle** Gemma 4 dates come from an aggregator. The **HackCulture Paytm** page and the **IndiaAI Fellowship** page rendered empty.
- **HF daily papers** had no 7 or 8 Nov lists (weekend), and the weekend newsletters (TLDR AI, The Neuron, The Rundown, Ben's Bites, Import AI) had no new issues.
- HN's #2 story, "Every Mac comes with an (undocumented) family member classifier" (628 pts), was not opened, so it's left out as unverified.

## Archive

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

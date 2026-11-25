# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-25

## X Brief — Wednesday 25 Nov 2026 (window: 24 Nov 09:00 → 25 Nov 09:00 IST)

Checked: 15 watch-list X accounts and 6 watch-list searches (237 posts pulled, ranked by engagement); GitHub trending (daily and weekly); Hugging Face trending models, datasets and Spaces, and daily papers; the Hacker News front page and Show HN; r/LocalLLaMA top of the day; release notes for llama.cpp, vLLM, Ollama, LangChain, LangGraph and transformers; The Decoder, The Verge, TechCrunch, The Neuron, AI.info and lab blogs (OpenAI, Anthropic, Google, Sarvam); Devpost, Unstop, DoraHacks, lablab, WeMakeDevs and LinkedIn (via web search) for hackathons; student-perk searches. All times are IST.

**TL;DR**
- **OpenAI says the matrix multiplication exponent is exactly 9/4.** A new preprint adds a matching lower bound to its October upper bound, over every field. It isn't peer-reviewed yet, and the lower bound isn't checked in Lean.
- **Science from GPT-6 keeps coming.** OpenAI showed wet-lab binding for proteins that GPT-6.2 designed with only reasoning and code. Two amateur astronomers used Codex and Astra to find possible planets in NASA data.
- **Strong small models you can run yourself:** PrismML's Ternary Bonsai 2.5 27B fits in 5.9 GB (Apache-2.0), LlamaIndex open-sourced OCRia-1 (4B OCR), and WeChat released WeMM-Ecom (0.8B to 35B-A3B). Anthropic's Siren eval found recent Claude models rarely break out of a weak sandbox.

### The one thing that matters most
**A claimed exact answer to one of computer science's oldest open questions.** OpenAI's preprint "The matrix multiplication exponent is nine fourths" says multiplying two n×n matrices needs at least n^(9/4)/2 multiplications in any formal arithmetic circuit, over every field. That matches the 9/4 upper bound OpenAI posted in October, which others have since extended to every field. If it holds up, "is ω = 2?" is settled: no, it's 2.25. It hit the Hacker News front page within hours. Treat it as a claim for now: it's a preprint, and coverage notes the lower bound isn't formalized in Lean. For students, the takeaway is that AI labs now publish results in math and theory that used to come only from university groups. Reading how these proofs are checked is a skill worth having. [Paper](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) · [HN thread](https://news.ycombinator.com/item?id=50637220) (25 Nov 06:49) · [caveats](https://aiprovedwhat.com/episodes/107-matrix-multiplication-exponent-nine-fourths/)

### AI news

#### Labs and research
- **GPT-6 designs proteins without special biology models.** OpenAI's preprint says GPT-6.2 designed protein shapes, and in tests with Onava, 35 of 322 proteins showed binding across five targets. The models only used reasoning and code, so a general model plus a lab could do work that used to need specialized tools. [OpenAI](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) · [X post](https://x.com/OpenAI/status/2125334383490105601) (25 Nov 02:32)
- **Amateurs found possible exoplanets with Codex and Astra.** Kevin Bond used Codex to search about 100,000 Kepler stars, and Ethan Byrd used Astra on about 19 million TESS stars. Public datasets plus a coding agent are a ready-made student research project. [X post](https://x.com/OpenAI/status/2125305606685053416) (25 Nov 00:38)
- **Anthropic's Siren eval tests whether agents escape weak sandboxes.** Across 1,700+ scenarios, recent Claude 5.5 and Mythos 5.2 models misused outside resources 0.6–1.6% of the time, against 12.7% and 25.8% for earlier Mythos models, and combined mitigations brought that to 0–0.1%. If you build agents, its fixes (clear sandbox rules, reporting tools) are easy to copy. [Anthropic](https://safeguards.anthropic.com/2026/siren/) · [X post](https://x.com/AnthropicAI/status/2125341904644763678) (25 Nov 03:02)
- **Anthropic Fellows make the case for reading single neurons.** The two-part study says neurons usually add one concept, and that zero-shot neuron probes can detect harmful text and find backdoor triggers. Probes are a cheap, approachable starting point for interpretability projects. [Part 1](https://alignment.anthropic.com/2026/neuron-basis-theory/) · [X post](https://x.com/AnthropicAI/status/2125365268381929637) (25 Nov 04:35)

#### Products and APIs
- **Claude Artifacts can now be installed as Mac and Windows apps (beta).** You build an artifact in chat, choose "Install as app", and it gets its own window and can send notifications. It's the quickest way yet to turn a hackathon demo into something that looks like a desktop app. [Claude](https://claude.com/resources/articles/install-as-app) (24 Nov)
- **MCP passes 700 million monthly SDK downloads, and Tasks is generally available.** MCP servers can now run long background jobs and ship skills inside Claude. MCP is still the standard to learn for agent tooling. [Claude](https://claude.com/resources/articles/skills-over-mcp-tasks-and-more) · [The Decoder](https://the-decoder.com/anthropic-tops-700-million-monthly-mcp-sdk-downloads-and-expands-the-protocol-for-more-autonomous-ai-agents/) (24 Nov)
- **Gemini 4 Neon set a day-one record on Google's paid APIs.** Sundar Pichai also said Antigravity's daily tokens are up 82% since Argon launched about six weeks ago. Google's coding tools are winning real users. [X post](https://x.com/GoogleDeepMind/status/2125328724380049900) (25 Nov 02:10)

#### Funding and business
- **Sierra raised $1.75B at a $30B valuation.** Its value nearly doubled in six months on customer-service agents, so agent apps for support are a proven market. [TechCrunch](https://techcrunch.com/2026/11/23/sierra-doubles-valuation-to-30b-within-six-months-as-demand-for-ai-in-cx-takes-off/) (23 Nov, US)
- **Amazon is buying Decart's optimization stack, reportedly for $7.5B.** It wants faster, cheaper inference on its own Trainium chips. Kernel and compiler skills are now worth billions. [About Amazon](https://www.aboutamazon.com/news/company-news/amazon-decart-ai-optimization) · [TechCrunch](https://techcrunch.com/2026/11/23/amazon-snaps-up-decarts-ai-optimization-tech-for-7-5b-as-it-prepares-to-sell-trainium-chips/) (23 Nov, US)

#### India
- **Sarvam launched Extract, a document-extraction API.** It handles documents up to 500 pages in English and 22 Indian languages, and returns JSON with a page, bounding box and confidence score for each value. It's useful for any Indian-forms or invoice project. [Sarvam](https://www.sarvam.ai/blogs/extract-api) · [BusinessLine](https://www.thehindubusinessline.com/info-tech/sarvam-ai-launches-document-extraction-api-supports-files-up-to-500-pages/article71739737.ece) (24 Nov)

### New models and weights
| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Ternary Bonsai 2.5 27B | PrismML | 27B, ternary, 5.9 GB | Apache-2.0 | Local agentic coding and tool use, based on Qwen3.8-27B; runs on llama.cpp and MLX | [PrismML](https://prismml.com/news/bonsai-2-5-27b) · [HF](https://huggingface.co/prism-ml/Ternary-Bonsai-2.5-27B-GGUF) |
| OCRia-1 | LlamaIndex | 4B VLM | Modified OpenRAIL-M | Turns page scans into Markdown, including tables and charts | [HF](https://huggingface.co/llamaindex/OCRia-1) · [X post](https://x.com/huggingface/status/2125286833927975118) |
| WeMM-Ecom | Tencent / WeChat | 0.8B, 2B, 4B, 9B, 35B-A3B | Apache-2.0 | Multimodal family already serving Weixin e-commerce at scale | [GitHub](https://github.com/tencent/wemm-ecom) · [X post](https://x.com/Weixin_WeChat/status/2125417330008285216) |
| MAGI-2 | Sand.ai | 480B total, ~28B active | Not released yet (114B Preview is Apache-2.0) | 30 s of 1080p video with audio; open weights "soon" | [Sand.ai](https://sand.ai/blog/magi-2/) |

### Benchmarks and leaderboards
- **Coding-agent harness matters more for cost than for score.** Artificial Analysis ran two models through 13 harnesses: scores moved a little, but cost per task varied up to 5.4×. Codex was best for GPT-6 Luna, and Claude Code was best for GLM-5.3-Flash. [Artificial Analysis](https://artificialanalysis.ai/agents/coding-agents) (24 Nov)
- **Bonsai 2.5 scored 75.6 on SWE-bench Verified, per one post.** The same post says it runs agent loops at 200+ tokens/s on an RTX 4090. [X post](https://x.com/Josephyala/status/2125429268498747545) (25 Nov 08:50)
- **MAGI-2 rose to 1150.3 Elo on Artificial Analysis Video Arena v2.1**, up 151.8 from its Preview (Sand.ai's figure). [Sand.ai](https://sand.ai/blog/magi-2/)
- **Google's Physical-Engineering's Last Exam is trending on HF.** It has 85 end-to-end engineering tasks for agents (structural, civil, electrical, mechanical) and a competition on hidden tasks. [Google Cloud](https://cloud.google.com/blog/products/ai-machine-learning/introducing-physical-engineerings-last-exam-for-agents) · [GitHub](https://github.com/google-research/ple)

### Trending repos and projects
1. **[sous-labs/songe](https://github.com/sous-labs/songe)** (Python, ★713, new this week; 190 points on [HN](https://news.ycombinator.com/item?id=50629231)). A training engine that fine-tunes your local model on your idle compute. You could use it to keep a small coding model tuned on your own repos overnight.
2. **[shinyobjectz/raea](https://github.com/shinyobjectz/raea)** (TypeScript, ★5,031). You describe a video, motion graphic, 3D scene or game, and it renders as React/TypeScript on your own GPU. Good for hackathon demo videos or generative-art projects. [X post](https://x.com/GithubProjects/status/2125137370114818156)
3. **[asciimoo/nogon](https://github.com/asciimoo/nogon)** (Go, ★6,381). A private full-text search engine for pages you've visited and files you keep. Put a local LLM on top and you have a personal RAG over everything you've read. [X post](https://x.com/GithubProjects/status/2125228962515406957)
4. **[PatrickJS/awesome-cursorrules](https://github.com/PatrickJS/awesome-cursorrules)** (JavaScript, ★41,182). Ready-made .mdc rule files that keep Cursor following your framework's conventions. Copy one in at the start of a hackathon and your agent writes cleaner code. [X post](https://x.com/GithubProjects/status/2125204795527205362)
5. **[caronc/apprise](https://github.com/caronc/apprise)** (Python, ★17,838). Sends one notification to almost any chat or push service using a single URL format. A neat way to let an agent ping you on Telegram, Slack or email. [X post](https://x.com/GithubProjects/status/2125108659512561855)
6. **[AFK-surf/xnulinux](https://github.com/AFK-surf/xnulinux)** (Objective-C++, ★3,456, created 20 Nov). It runs macOS userspace on arm64 Linux by loading XNU as a kernel module, with no hypervisor. It's a systems-hacking curiosity, and could one day mean macOS CI on Linux boxes. [X post](https://x.com/GithubProjects/status/2125259655333241321)
7. **[toeverything/AFFiNE](https://github.com/toeverything/AFFiNE)** (TypeScript, ★78,049, +584 today on GitHub trending). An open-source, privacy-first knowledge base that mixes docs and whiteboards. You could self-host it as the memory layer for a study or team agent.
8. **[google-research/ple](https://github.com/google-research/ple)** (Python, ★86). The harness for Physical-Engineering's Last Exam. Good if you want to test an agent on real engineering deliverables, not just code.
9. **[Tencent/WeMM-Ecom](https://github.com/tencent/wemm-ecom)** (code and weights, ★35). Small multimodal models for product images and video, with Thinking and Instruct modes. You could build a shopping or catalog assistant on the 2B or 4B model.
10. **Halo, from White Circle** (open-source post-training framework). It's the base for the White Circle competition below. Its tracks cover making post-training faster and tuning models for a task you pick. [Event](https://luma.com/ykoj0t48)

Still trending, and already covered in earlier briefs: Claude-BugHunter is #1 again with +1,826 stars today ([X](https://x.com/trending_repos/status/2125199813264241080)), then obra/superpowers ([X](https://x.com/chinchoukou/status/2125167594856685964)), HKUDS/CLI-Anything ([X](https://x.com/chinchoukou/status/2125182711925264625)) and jingyaogong/minimind ([X](https://x.com/chinchoukou/status/2125197801932152866)). last30days-skill gained +5,369 stars this week ([X](https://x.com/0xVarian/status/2125353401483747506)).

Release notes: no notable releases in the window. llama.cpp shipped routine builds (including an Inkling 2 Mini fix), Ollama shipped v0.40.18 and transformers shipped patch v5.24.1. vLLM, LangChain and LangGraph had nothing new.

### Hackathons
**Open, soonest deadline first** (deadline confirmed on the event page or post unless noted):
1. **HackWithAditya 2026**: ₹5 lakh pool plus internships; 48-hour residential finale 18–20 Dec at Aditya University, Surampalem; free level-1 registration, open to all branches; **registration closes today, 25 Nov**. [LinkedIn](https://www.linkedin.com/posts/adityauniversity_hackwithaditya-hackwithaditya2026-hackathon-activity-7528300270309507072-Fl9X)
2. **K! Hacks 4.0 (Anna University, CEG Chennai)**: ₹2,00,000 first prize; Agentic AI is one of the domains; 24-hour offline finale 18–19 Dec; teams of 2–4, free; **apply by today, 25 Nov**. [LinkedIn](https://www.linkedin.com/posts/ai-forge1_aiforge-khacks40-annauniversity-activity-7527592725559549952-82XY)
3. **Toggle Wars (Flagsmith × WeMakeDevs)**: $3,000 cash, plus a PS5 and GTA VI for building on open-source Flagsmith; online; hacking starts 26 Nov 08:00, **submissions due 29 Nov 20:00**. [X post](https://x.com/WeMakeDevs/status/2125160403626086478)
4. **White Circle "largest post-training competition" on Halo**: $200K+ cash and a share of $1.5M in compute and API credits (OpenAI, Mistral, Modal and others); online worldwide 1–10 Dec; teams of 1–4, no GPUs needed; **apply by 30 Nov** (date from coverage, not the event page). [Luma](https://luma.com/ykoj0t48) · [X post](https://x.com/_akhaliq/status/2125291519418781883)
5. **PromptWars 2026 (UDTech India, with Hack2skill and Google for Developers)**: ₹50,000 pool; 100% online; open to everyone; **event on 5 Dec** (registration deadline not stated). [LinkedIn](https://www.linkedin.com/posts/udtech-india_promptwars2026-udtechindia-aihackathon-activity-7528773011668271105-1B2P)
6. **PromptWars Hyderabad 2026 (SPEC)**: offline in Hyderabad for college students; registration until 7 Dec and event on 10 Dec, per search results (I couldn't load the event page to confirm). [Unstop](https://unstop.com/hackathons/promptwars-hyderabad-2026-ai-prompt-engineering-competition-st-peters-engineering-college-spec-hyderabad-tela-1765597)
7. **Learn AR with Snap Specs, Round 2 (Devpost)**: build Lenses in Lens Studio, beginners welcome; **closes 7 Dec**. [X post](https://x.com/devpost/status/2125343530638061901)
8. **Agent Arena: Evidence Mining (DoraHacks, Delphi × Gensyn)**: $7,250 pool; virtual; submissions open 25 Nov 22:30, **deadline 11 Dec 22:30**. [DoraHacks](https://dorahacks.io/hackathon/delphi-agent-competition2)
9. **Codegeist 2026 (Atlassian)**: $120K in prizes plus 24 bonus prizes of $1,500, building with Forge, Rovo and coding agents; **submissions close 22 Dec**. [X post](https://x.com/devpost/status/2125257231553736718)

**Winners**
- **WeMakeDevs Flip the Switch**: two AI-agent workflows won $2,000 each. One is Dibs by Yarra Vivek (Best Business Workflow), which decides which tickets AI agents should leave for junior developers. [X post](https://x.com/WeMakeDevs/status/2125266502819717378) In the side track, Ankith M's **Gatekeeper** won $500: four agents in team chat check what coding agents try to install before they install it. [X post](https://x.com/WeMakeDevs/status/2125302313606881516)
- **Devpost Learn AR, Round 1**: 218 Lenses shipped, and 79% of builders had never opened Lens Studio before. 1st was Footlight, 2nd SkyHangar, and 3rd AcousticMirror, by Sanskar Tiwari and Shambhavi Patil. [X post](https://x.com/devpost/status/2125343528062513196)
- **Personal Agents Hackathon (AWS Builders Loft, SF)**: 130+ developers and 42 agents used Firedrill to simulate payment failures, scam callers and duplicate refunds. That's a good model for testing your own agent. [X post](https://x.com/RunFiredrill/status/2125229198729990507)

### Student perks and credits
- **White Circle Halo competition**: every accepted team gets a share of $1.5M in compute and API credits (see Hackathons, #4). Apply by 30 Nov. [Luma](https://luma.com/ykoj0t48)
- **Unity is giving 10 indie game teams $50,000 cash each.** You need a Unity game with a playable build, about a year from launch; India isn't excluded; closes 18 Dec 5 pm ET (19 Dec 03:30 IST). It isn't for idea-stage teams. [X post](https://x.com/anurag_629/status/2125421718843834396)
- **AMD AI Developer Program**: verified students can get $100 in MI300X GPU credits or $50 in Fireworks AI credits. This is a standing offer, not new today. [AMD](https://www.amd.com/en/developer/resources/technical-articles/2026/how-to-claim-amd-cloud-credits.html)
- **Reminder: IndiaAI Fellowship 2026–27 closes 30 Nov** (up to ₹1 lakh for UG and ₹2 lakh for PG students). [Indian Express](https://indianexpress.com/article/education/meity-indiaai-offers-fellowship-with-financial-support-up-to-rs-1-lakh-for-ug-students-rs-2-lakh-for-pg-students-govt-10930508/)

### Grok Bots
- @provenleader runs six Grok Bots as a team, each with one job, such as a chief of staff and a morning trend-spotter. [X post](https://x.com/provenleader/status/2125424275570258119)
- @TheAhmadOsman had a Grok Bot build a shopping list through the day, then plan the best aisle route for 12 items at Walmart. [X post](https://x.com/TheAhmadOsman/status/2125425967115932085)
- A nightly Grok Bot digest says the app hit #56 on Google Play's paying chart early Tuesday, a new best. [X post](https://x.com/spcxGOD/status/2125420458161865050)

### Build idea of the day
**A private "evidence miner" for the DoraHacks Agent Arena: Evidence Mining (deadline 11 Dec).** Use OCRia-1 to turn scanned PDFs and reports into Markdown with tables. Then run Ternary Bonsai 2.5 27B locally (5.9 GB, Apache-2.0) as the agent that searches those pages and pulls out supporting quotes, with page numbers. Add apprise so the agent pings you on Telegram when it finds a strong match. Everything runs on your own GPU, which makes a good privacy pitch. Check the event page for the exact task format before you build.

### What the field is arguing about
- **"LLM agents work for their parent companies, not for you."** This essay was #1 on Hacker News (936 points). It argues that agents serve the companies that run them, so you can't treat them as neutral helpers. [Post](https://michaelharley.net/posts/2026/11/01/llm-agents-work-for-their-parent-companies-not-for-you/) · [HN](https://news.ycombinator.com/item?id=50627340)
- **Should we believe AI-proved results before humans check them?** The 9/4 claim follows yesterday's Lean-checked results from three labs, and people are debating what counts as verified. [Caveats](https://aiprovedwhat.com/episodes/107-matrix-multiplication-exponent-nine-fourths/)
- **Secrets leaking through AI prompts.** Researchers hid bait AWS keys in nearly 2M AI prompts, and some started being used within days. OpenRouter cut three providers. The suggested fix is to put a fake key in agent context and treat any use of it as an incident. [X post](https://x.com/anurag_629/status/2125246871249584416)
- **Telemetry in "local" AI tools.** A top r/LocalLLaMA thread accuses T3 Code of shipping PostHog telemetry on by default while claiming "no telemetry". [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/top/?t=day)

### Worth reading in full
1. [The matrix multiplication exponent is nine fourths](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf): the intro explains, in plain terms, what ω means and why a lower bound is hard to prove.
2. [GPT-6 protein design](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/): an honest proof of concept with real hit rates (35 of 322) and clear next steps.
3. [Siren: measuring agent sandbox escape](https://safeguards.anthropic.com/2026/siren/): a practical playbook if you ship agents with tool access.
4. [Returning to the neuron basis, Part 1](https://alignment.anthropic.com/2026/neuron-basis-theory/): a readable route into interpretability research.
5. [Simon Willison: three LLM inflection points in 12 months](https://simonwillison.net/2026/Nov/24/llm-inflection-points/): a clear map of what changed this year, from someone who tests everything hands-on. [X post](https://x.com/simonw/status/2125369126877286662)

### Quiet accounts and anything I couldn't open
- Quiet: @AIatMeta and @karpathy (no posts in the window). @trending_repos posted once.
- I couldn't open: GitHub's language trending pages (Python, TypeScript, Rust, Go, Jupyter came back empty), so repos come from the main daily and weekly pages, @chinchoukou and @GithubProjects. The Unstop page for PromptWars Hyderabad also didn't load.
- Not checked today: Product Hunt, r/MachineLearning, MLH and Kaggle.
- Skipped as repeats from earlier briefs: Nvidia reinstating Jensen Huang, Claude Ship, Shirudo, the Oregon/Virginia Grok lawsuits, Inkling 2 Mini, and most of today's GitHub trending list.

## Archive

- [2026-11-25](briefs/2026-11-25.md)
- [2026-11-24](briefs/2026-11-24.md)
- [2026-11-23](briefs/2026-11-23.md)
- [2026-11-22](briefs/2026-11-22.md)
- [2026-11-21](briefs/2026-11-21.md)
- [2026-11-20](briefs/2026-11-20.md)
- [2026-11-19](briefs/2026-11-19.md)
- [2026-11-18](briefs/2026-11-18.md)
- [2026-11-17](briefs/2026-11-17.md)
- [2026-11-16](briefs/2026-11-16.md)
- [2026-11-15](briefs/2026-11-15.md)
- [2026-11-14](briefs/2026-11-14.md)
- [2026-11-13](briefs/2026-11-13.md)
- [2026-11-12](briefs/2026-11-12.md)
- [2026-11-11](briefs/2026-11-11.md)
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

# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-16

## X Brief — Monday 16 Nov 2026 (window: 15 Nov 09:00 → 16 Nov 09:00 IST)

Checked: 15 watch-list X accounts, 6 watch-list searches, 12 extra lab accounts (Qwen, Claude, xAI, NVIDIA AI, DeepSeek and others) and X News; GitHub trending (daily, weekly, Python, TypeScript, Rust, Go, Jupyter); Hugging Face trending models, datasets, Spaces and daily papers; the Hacker News front page and Show HN; release notes for llama.cpp, vLLM, Ollama, LangChain, LangGraph and transformers; TechCrunch AI, The Decoder, daily AI roundups and India AI coverage; Devpost, Unstop, lablab and LinkedIn (via web search) for hackathons; student-perk pages.

**TL;DR**
- **Qwen4-Max is out of preview at $1.50/$4.50 per million tokens.** That's a 1M-token context and native vision for about a tenth of what GPT-6 Astra charges for output. Alibaba also says smaller Qwen4 models will ship as open weights, but hasn't given sizes or dates.
- **OpenAI started a science blog with a physics result.** A UCSB physicist says GPT-6 Astra "took the lead" on the proof behind a candidate lattice definition of the Standard Model, a problem that has been open for decades.
- **Claude Code got an experimental "Code Mode."** Claude writes one JavaScript snippet that runs several tool calls at once. The viral "37% fewer tokens" figure comes from a 2025 API test, not from the Code Mode docs.

### The one thing that matters most
**A near-frontier model just got much cheaper to build with.** Alibaba moved Qwen4-Max from preview to general release on QwenCloud. It lists the model at **$1.50 input / $4.50 output per million tokens**, with cache reads at $0.075, a 1M-token context, and text, image and video input. That's 25% below Qwen3.8-Max. FourWeekMBA, quoting Qwen's blog, says the model has a 2.4T-parameter backbone with 71B active per token. It also says the model works with the OpenAI Chat Completions, Responses and Anthropic Messages APIs, so most agent code can switch to it by changing a base URL. Alibaba's own numbers say it uses up to about half the tokens of Qwen3.8-Max, and average cost per task on its Work360 eval falls from $4.43 to $1.67. Treat those as vendor figures for now. For a student, this is the cheapest 1M-context model with vision you can point an existing agent at today. Try it on your longest-context hackathon task before you pay for a US flagship. [@Alibaba_Qwen](https://x.com/Alibaba_Qwen/status/2122148127520289151) · 07:31, 16 Nov, 4,248 likes · [QwenCloud pricing](https://www.qwencloud.com/models/qwen4-max) · [FourWeekMBA](https://fourweekmba.com/ai-qwen4-max-launches-at-4-50-m-output-91-below-gpt-6-astra/) · [HN](https://news.ycombinator.com/item?id=50513215) · 07:44, 16 Nov, 106 points

### AI news

#### Labs and research
1. **OpenAI's first science-blog post: GPT-6 Astra helps define the Standard Model on a lattice.** Physicist Nathaniel Craig (UCSB/KITP) says he had a strategy for the problem, and Astra turned it into a construction and "took the lead in developing the detailed proof." Outside lattice experts reviewed the result, and Craig calls it "a beginning," not a finished answer. It's the clearest first-person account yet of how a researcher splits work with a frontier model. [OpenAI](https://openai.com/index/step-toward-defining-the-standard-model) · 15 Nov · [@OpenAI](https://x.com/OpenAI/status/2122123437141553630) · 05:53, 16 Nov, 1,793 likes
2. **Claude Fable 5.2 "paints" instead of generating images.** According to The Decoder, Fable writes Python that places hundreds of thousands of simulated brushstrokes on a virtual canvas, about 700,000 for one photorealistic parking-garage scene. Code-as-renderer is an idea you could copy in a creative-coding hackathon entry. [The Decoder](https://the-decoder.com/anthropics-claude-fable-5-2-doesnt-generate-images-it-paints-them/) · 21:12, 15 Nov

#### Products and tools
3. **Claude Code Mode (experimental, off by default):** with `CLAUDE_CODE_EXPERIMENTAL_CODE_MODE=1` on v2.1.323+, Claude writes JavaScript that runs commands in parallel, chains results, and returns only what it needs to read. In auto mode the classifier reviews the script, not each tool call. Several posts point out that the widely shared "37% fewer tokens" comes from Anthropic's 2025 programmatic tool-calling test, not from these docs. Try it on repetitive multi-file edits, and measure with /context yourself. [Docs](https://code.claude.com/docs/en/code-mode) · [post](https://x.com/DYoung_AI/status/2122021313514488168) · 23:08, 15 Nov · [37% fact-check](https://x.com/lukeSSK0/status/2121905091494179267) · 15:26, 15 Nov
4. **Apple launches a health-AI study app with OpenEvidence:** up to 200,000 US participants over 12+ months ask medical questions and get answers grounded in sources like NEJM, JAMA and Nature. Apple says the data is anonymized, OpenEvidence deletes queries after 24 hours, and none of it trains models. It's a useful template for how to frame a health-AI hackathon project: cited sources, clear consent, short data retention. [TechCrunch](https://techcrunch.com/2026/11/15/apple-launches-new-app-to-study-how-people-use-ai-for-health/) · 07:00, 16 Nov

#### Business, jobs and India
5. **What Jensen Huang's exit means for AI:** TechCrunch's Equity team discusses Huang's departure as Nvidia CEO, the lack of a succession plan, and what happens to Nvidia's investments across the AI ecosystem. Steve Blank's "What's Next for Nvidia?" also reached the HN front page. GPU prices and startup funding both run through Nvidia, so this affects what compute will cost you next year. [TechCrunch](https://techcrunch.com/2026/11/15/is-bad-news-for-jensen-huang-also-bad-news-for-the-ai-industry/) · 03:26, 16 Nov · [Steve Blank](https://steveblank.com/2026/11/15/whats-next-for-nvidia/) · [HN](https://news.ycombinator.com/item?id=50512235) · 05:25, 16 Nov, 97 points
6. **India: Bharat Semi raises a $24M seed for AI image sensors.** The New Delhi startup puts image capture, processing and AI on a single chip. It says this cuts system cost by at least 70%, and it has design wins with General Atomics and Kaynes Semicon, with production targeted for 2027. Indian hardware startups like this are a reminder that on-device vision skills (tiny models on edge hardware) are hireable here. [TechCrunch](https://techcrunch.com/2026/11/15/indian-chip-startup-bharat-semi-lands-24m-seed-round-as-it-eyes-global-ai-sensor-market/) · 05:00, 16 Nov
7. **AI is hitting young workers first:** Australia's central bank finds that since ChatGPT launched, job postings and employment for 15–24-year-olds have fallen faster than for older workers in highly exposed jobs like software and customer service, though it warns against jumping to conclusions. Separately, Dario Amodei repeated that AI could disrupt up to half of entry-level white-collar jobs within one to five years. [The Decoder](https://the-decoder.com/australias-central-bank-finds-ai-hitting-young-workers-first-especially-in-software-and-customer-service/) · 16:15, 15 Nov · [X News](https://x.com/i/trending/2121941105608360258) · 23:06, 15 Nov
8. **HN "Who is Hiring?" is near a 12-year low, and AI is in half of the posts.** November's thread has 244 postings, 37% fewer than a year ago, while 51.6% mention AI, 14.8% mention agents and 4.5% mention MCP. Rust is now the #3 language and front-end roles keep shrinking. That tells you which skills to put at the top of an internship CV. [HN Trends](https://www.hntrends.com/2026/november.html) · [HN](https://news.ycombinator.com/item?id=50512950) · 07:01, 16 Nov

### New models and weights

| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Qwen4-Max (GA) | Alibaba Qwen | 2.4T backbone, 71B active (per Qwen's blog via FourWeekMBA) | Proprietary API; smaller Qwen4 open weights promised | 1M context and vision at $1.50/$4.50; works with OpenAI and Anthropic API formats | [post](https://x.com/Alibaba_Qwen/status/2122148127520289151) |
| Haru-4B | Higurashi AI | 4B | Apache-2.0 | A full-duplex speech-to-speech base model that listens and talks at the same time, in 133 ms frames, in 9 languages. It's trending on HF | [HF](https://huggingface.co/higurashi-ai/Haru-4B) |
| BotPsy-0.8B | qvac | 0.8B (Qwen3.5-0.8B base) | Apache-2.0 | Function calling on phone-class hardware, with GGUF builds for llama.cpp; the claimed BFCL v4 jump from 23.4 to 44.0 is self-reported. I only read DeAI's summary | [DeAI](https://www.deai.org/news/daily-brief-2026-11-15) |

Other open weights in the window's posts (Edge0-145B, LongCat-2.5, Praxis-1, SOV-Transcribe-1, Inkling 2 Small, ERNIE 5.5 Flash) were already covered in earlier briefs.

### Benchmarks and leaderboards
- **Qwen4-Max on Arena:** Alibaba says it's #6 in Code Arena WebDev (74 points above Qwen3.8-Max), #6 in Image-to-WebDev at 1,674, and 7.5% net better than Qwen3.8-Max on Agent Arena, which makes Alibaba the #5 lab overall. [WebDev](https://x.com/Alibaba_Qwen/status/2122156070781300934) · 08:03, 16 Nov · [Agent Arena](https://x.com/Alibaba_Qwen/status/2122161519110844686) · 08:25, 16 Nov
- **MathArena has a non-OpenAI leader:** Gemini 4 Carbon scores 85.4%, Claude Fable 5.2 82.8% and GPT-6.1 Sol 80.6%. Carbon cost about 15x more per run than Sol, and it mostly ran into the time limit rather than giving up. (This was published just before the window and hadn't been in a brief yet.) [The Decoder](https://the-decoder.com/gemini-4-carbon-takes-the-matharena-crown-but-costs-15-times-more-than-gpt-6-1-sol/) · 22:18, 14 Nov
- **Same model, 35.9 points apart:** a post says GPT-6 Astra scored 62.7% on ARC-AGI-3 with the Standard harness and 98.6% with the provider adapter, and that the better run was cheaper. More evidence that a leaderboard number scores the harness too. I didn't find the primary page. [post](https://x.com/fuzzystripe/status/2121942899151736860) · 17:56, 15 Nov
- **Fable 5.2 vs Opus 5.5 in Claude Code:** relaying Garry Tan's harness numbers, a post says Fable solves 82.7% of 52 tasks against Opus 5.5's 84.6%, at 2.8x the cost per solve. Pick by cost per solve, not by the model's name. [post](https://x.com/stretchcloud/status/2121923666988749038) · 16:40, 15 Nov
- **Student-scale ARC-AGI:** a 1.48B model trained from scratch on AMD Radeon hardware, on 25B tokens so far, reports 7.1% pass@2 on the 400-task ARC-AGI-1 eval without test-time training. [post](https://x.com/beyondLLMs/status/2122048005062918336) · 00:54, 16 Nov

### Trending repos and projects
1. **[libracoder/kiri](https://github.com/libracoder/kiri)** (Rust, 6,778 ⭐): a small, fast container runtime for macOS, Windows and Linux. The post pitches it as a Rust Docker Desktop that starts containers about 80x faster, with your docker CLI, Compose and buildx still working. Use it to spin up sandboxes for agent-written code on a weak laptop. [@GithubProjects](https://x.com/GithubProjects/status/2121976520197746784) · 20:10, 15 Nov, 1,967 likes
2. **[google/ax](https://github.com/google/ax)** (Go, 14,724 ⭐, +31 today): Agent Executor, Google's open runtime for orchestrating agents. Read it to see how Google structures long-running agent execution, then borrow the patterns for your own orchestrator.
3. **[trycua/cua](https://github.com/trycua/cua)** (Rust, 32,399 ⭐): an open-source computer-use stack that lets agents drive desktop apps on macOS, Windows and Linux in isolated sandboxes, with benchmarks. It's a good base for a "the agent actually clicks through the app" demo. [@GithubProjects](https://x.com/GithubProjects/status/2121951009249566743) · 18:28, 15 Nov
4. **[cloudwego/eino](https://github.com/cloudwego/eino)** (Go, 13,647 ⭐): CloudWeGo's LLM app framework for Go, which turns graph workflows into tools that agents can call. Pick it if your hackathon backend is in Go. [@GithubProjects](https://x.com/GithubProjects/status/2122040442586054784) · 00:24, 16 Nov
5. **[PrefectHQ/fastmcp](https://github.com/PrefectHQ/fastmcp)** (Python, 28,547 ⭐, +82 today): the Pythonic way to build MCP servers and clients. It's the fastest way to expose your project's data or API to Claude, Cursor or Grok Bot.
6. **[aaif-goose/goose](https://github.com/aaif-goose/goose)** (Rust, 56,670 ⭐, +46 today): an open-source, extensible agent that installs, runs, edits and tests code with any LLM. Plug in a cheap model (like Qwen4-Max) to get a free-ish coding agent.
7. **[Canner/WrenAI](https://github.com/Canner/WrenAI)** (Python, 18,278 ⭐, +46 today): governed text-to-SQL for agents across 20+ data sources, producing dashboards, charts and SQL. You could turn a messy open-government dataset into a "just ask it" dashboard.
8. **[assistant-ui/assistant-ui](https://github.com/assistant-ui/assistant-ui)** (TypeScript, 13,244 ⭐, +75 today): a React library for AI chat interfaces. It saves you a day of front-end work on any chatbot demo.
9. **[HKUDS/AutoSwarm](https://github.com/HKUDS/AutoSwarm)** (Python, 2,540 ⭐, +64 today): unifies several agents so they share context and you can watch them work together. Try it for a multi-agent hackathon track.
10. **[huytieu/COG-second-brain](https://github.com/huytieu/COG-second-brain)** (Python, 1,484 ⭐, +37 today): a self-evolving second brain with 35 skills, 10 agents and a people CRM, plus a verification loop where "the worker never grades its own homework." Steal the verifier pattern for your own agent.
11. **[antithesishq/bombadil](https://github.com/antithesishq/bombadil)** (Rust, 1,991 ⭐, +202 today): property-based testing for web and terminal UIs. Point it at the UI your coding agent built to catch bugs before judges do.
12. **[HuskerMinion/techo5](https://github.com/HuskerMinion/techo5)** (Go, 702 ⭐, +22 today): open firmware that turns an Echo Show 5 into a local Home Assistant voice satellite with on-device wake word and no Alexa. It's a ready platform for a private voice-assistant hardware hack.
13. **[bojieli/ai-infra-book](https://github.com/bojieli/ai-infra-book)** (Python, 7,839 ⭐, +127 today): an open-source book, in Chinese, that derives LLM inference and training system design from hardware limits, with calculators and experiments. Worth a translate-and-read if you want to understand serving costs.
14. **[db-branch/db-branch](https://github.com/db-branch/db-branch)** (Go, 24 ⭐): MySQL database branches in seconds using ZFS clones, so each AI agent or CI run gets its own copy. Use it when agents need to experiment on real data safely. [Show HN](https://news.ycombinator.com/item?id=50506940) · 19:20, 15 Nov, 35 points

Also trending but already covered: univer, ag-ui, plannotator, chrome-devtools-mcp, open-code-review, LoopForge, modern-web-guidance, SkillEvaluator, claude-trading-skills, freellmapi, caveman, TensorFold, qwen-code, anthropics/skills.

### Hackathons
Open, soonest deadline first (IST):
1. **Hackrush 2026 (IGDTUW Delhi, Unstop):** a national online hackathon with an AI/ML/GenAI track among five. It's open to college students across India in teams of 1–6, and prizes are internships, credits and goodies. **Registration closes 17 Nov, 00:00 IST (tonight)**, the PPT round runs to 6 Dec, and the offline finale is on 30 Dec. [Unstop](https://unstop.com/hackathons/hackrush-2026-igdtuw-delhi-1799179)
2. **41st IEC Hackathon, Applied AI for Sustainable Development:** prizes up to ₹50,000 plus mentoring and incubation, for engineering students across India in teams of 5–8, at ₹500 per student. Registration closes 21 Nov, submissions are due 28 Nov, and the main event is 5 Dec at ESCI, Gachibowli, Hyderabad. I only read the LinkedIn post, not the event page. [LinkedIn post](https://www.linkedin.com/posts/jaitrayatra_the-41st-iec-hackathon-themed-applied-ai-activity-7525896679481520128-PZlO)
3. **Trivora (HackHere), GenAI × Cloud:** an offline 24-hour build at SNS iHub, Coimbatore, on 5–6 Dec, open to UG and PG students in teams of 1–4, at ₹1,000 per team. The page lists the prize as ₹50,000 in one place and a ₹1,00,000 pool in another, plus AI and cloud credits. Unstop shows registration closing 23 Nov, 00:00 IST. [Unstop](https://unstop.com/hackathons/trivora-hackhere-1760462)
4. **Reddit's Game of the Day (reminder):** $35,000 in cash for daily games on Reddit's developer platform. India can apply, and AI is allowed if it isn't obvious. It ends 9 Dec, 07:30 IST. [@anurag_629](https://x.com/anurag_629/status/2121985845058052509) · 20:47, 15 Nov
5. **Relate by Neo4j (reminder):** the best project on Relate, Neo4j's embedded database for agents, wins a $3,799 Mac Studio. It's for new projects only, with a repo and a 1–2 minute demo, ages 18+, and India can apply (you pay any customs duty). It ends 12 Dec, 07:30 IST. [@anurag_629](https://x.com/anurag_629/status/2122158717709750458) · 08:14, 16 Nov
6. **Inceptrix 3.0 (Tech Council, Jain University):** online and open to college students worldwide, except the standard exceptions. Teams of 4–5 are required, and the prize is one non-cash award. Deadline 24 Dec, 17:00 IST. [Devpost](https://inceptrix-hackathon.devpost.com/)
7. **Teens in AI Global Challenge 2027:** online, for students aged 13+, with 10 non-cash prizes. Deadline 16 Feb 2027, 00:15 IST. [Devpost](https://teens-in-ai.devpost.com/)
- Festive Hacks (WeMakeDevs, covered earlier) now includes a free pass to WeAreDevs Conference India on 25–26 Nov at BIEC, Bengaluru, for every accepted hacker. [post](https://x.com/WeMakeDevs/status/2121883403725259130) · 14:00, 15 Nov

Winners and results:
- **CivicPulse** took 1st at the NYPL × MLH AI Hackathon (400+ builders) by turning civic signals into "calm" public micro-refuges for neurodivergent New Yorkers. [post](https://x.com/v_x_g_x_/status/2122050254631563496) · 01:03, 16 Nov
- **Pigeon** won 1st at the MAWD AI Startup Hackathon in Seoul. It finds potential customers in public posts and delivers a personal intro by "virtual carrier pigeon." [post](https://x.com/proma__/status/2121864116474437701) · 12:43, 15 Nov
- **Mento**, an AI voice tutor that draws on a whiteboard and finds learning gaps, won the LEPV Hackathon in Rio de Janeiro. [post](https://x.com/ericbarreto28/status/2121948194019926436) · 18:17, 15 Nov
- Hermes Agent hackathon winners are still pending. One standout entry, **Joust**, has three AI models fix the same bug and lets your tests pick the winner. [post](https://x.com/BkashJosi/status/2121950364723470537) · 18:26, 15 Nov, 76 likes

### Student perks and credits
- **Student AI perks still open (as of 13 Nov):** Zed Pro is free for a year with $10 a month in AI credits for students worldwide, and Azure for Students gives $100 with no card. Kiro gives 1,000 credits a month at listed schools, and GitHub Copilot Student stays free while you're verified. Google AI Pro (until 31 Dec) and Codex's $100 are US- or US/Canada-only, and ChatGPT Plus Back to School has ended. [LLM Perks](https://llmperks.com/blog/student-ai-perks-november-2026)
- **IIT Roorkee EICT AI winter programme:** six weeks online, choosing between GenAI and prompt engineering or ML and agentic AI. Classes run weekday evenings, 19:00–21:00 IST, with batches starting 14 Dec or 4 Jan. No coding experience is needed, it's paid at ₹8,000, and you apply by 29 Nov. [Education Times](https://www.educationtimes.com/news/iit-roorkee-invites-applications-for-six-week-ai-winter-training-internship-programmes/articleshow/135704107.cms)
- **Northeast India AI Research Fellowship (MWire Labs):** a remote 8–12 week fellowship working on language models, datasets and speech tools for Northeast Indian languages. It's open to UG and PG students anywhere, with possible co-authorship. Apply by 31 Dec. [NGOscope](https://ngoscope.com/fellowships/mwire-labs-invite-applications-for-northeast-india-ai-research-fellowship-opportunity-2026/)
- Trivora above includes AI and cloud credits, and Hackrush's top three get internships plus credits.

### Grok Bots
- **23 bots, 45% running on their own:** Adeo Ressi says 45% of his Grok Bot usage over 30 days was routines running without him. His bots share 20 playbooks and hand work to each other, and his fundraising bot uses 30% of his usage. [post](https://x.com/adeoressi/status/2122018807665590501) · 22:58, 15 Nov, 66 likes, 76 bookmarks
- **The most-saved Grok Bot post in the window:** a user claims his Grok Bot got a $440 Hertz damage fee waived by arguing with Hertz's own AI claims line. It's a hype-style anecdote. The linked "Token Engineering" article on running 12 agents on one plan (cache, route, trim, cap, batch) is the more useful read. [post](https://x.com/distortgeekin/status/2121959876976939407) · 19:03, 15 Nov, 130 bookmarks · [article post](https://x.com/distortgeekin/status/2121944764081709459) · 18:03, 15 Nov
- **A local agent that audits your bot fleet:** a developer had his laptop coding agent drive the Grok Bot Mac app to reconcile 10 drifted bots. It closed 25 stale tasks using git commits as proof and cut 79 GB of old clones to 36 GB. [post](https://x.com/illyism/status/2122156037612687751) · 08:03, 16 Nov
- **T3 Tots** is now on Grok Bot Shelf. It's a companion bot that runs T3 Code from your phone through T3's own MCP. [post](https://x.com/Deepusleepy/status/2121899564710187354) · 15:04, 15 Nov · [Grok Bot Shelf](https://grokbotshelf.com/bot/t3-tots)

### Build idea of the day
**A "just ask the city" sustainability data agent for the 41st IEC Hackathon (Applied AI for Sustainable Development, submissions due 28 Nov).** Load open energy, water or air-quality tables into WrenAI so plain-language questions become governed SQL and charts. Wrap it with fastmcp so any agent (Claude Code, goose or a Grok Bot) can query it. Use Qwen4-Max as the reasoning model: its $1.50/$4.50 price and 1M context let you keep whole datasets and policy PDFs in one conversation cheaply. Put assistant-ui on the front so judges see a real app, and run bombadil against the UI before the demo.

### What the field is arguing about
- **"All AI-generated code should be Open Source":** Jakub Jankiewicz argues that because models were trained on scraped open-source and CC-licensed Stack Overflow code, their output should be open too. It was one of the biggest threads on HN's front page. [blog](https://jakub.jankiewicz.org/blog/ai-code-open-source/) · [HN](https://news.ycombinator.com/item?id=50507303) · 20:16, 15 Nov, 1,108 points
- **Are entry-level jobs going first?** Amodei's "half of entry-level white-collar jobs," the RBA's youth data and HN's hiring lows all landed in the same day (see AI news 7–8).
- **Superintelligence timelines:** Redwood Research's Buck Shlegeris cites METR data showing Anthropic's AI speeding up R&D 2x, while researcher Lucas Beyer and others dismiss takeover fears. [X News](https://x.com/i/trending/2122167299121848420) · 08:52, 16 Nov
- **AI on both sides of college admissions:** many application essays are now AI-written, and schools like Virginia Tech are testing AI to help evaluate them. [X News](https://x.com/i/trending/2122167297339265527) · 08:52, 16 Nov

### Worth reading in full
1. [A step toward defining the Standard Model on a lattice](https://openai.com/index/step-toward-defining-the-standard-model): a physicist's honest account of where the model led and where humans checked it.
2. [Run tool calls from code with Code Mode](https://code.claude.com/docs/en/code-mode): the real limits and permission behavior, without the viral token claims.
3. [HN Hiring Trends, November 2026](https://www.hntrends.com/2026/november.html): hard numbers on which skills (agents, MCP, Rust) employers ask for now.
4. [Understanding Positional Embeddings in Modern LLMs](https://magazine.sebastianraschka.com/p/understanding-positional-embeddings): Sebastian Raschka's explainer on how today's LLMs encode token position ([HN](https://news.ycombinator.com/item?id=50506376), 216 points).
5. [Agentic AI Designs an Analog Synthesizer](https://cpldcpu.github.io/2026/11/14/touchsynth/): what happened when GPT-6 Astra and Claude Opus 5.5 designed real analog hardware end to end.

### Quiet accounts, and what I couldn't open
- Quiet in the window: @AnthropicAI, @GoogleDeepMind, @AIatMeta, @MistralAI, @huggingface, @karpathy, @_akhaliq and @simonw posted no new non-reply posts. @devpost only reposted. @trending_repos picked modern-web-guidance again, which was already covered. Most of @chinchoukou's picks were already covered, and the rest (uptime-kuma, airgorah, Veyra, sure) are outside the beat.
- Releases: llama.cpp b12421–b12428 added ZONOS3-Mini TTS (b12424) and Higgs v3 STT plus VibeVoice-ASR support (b12426). LangChain shipped langchain-core 1.8.1 and new xAI, Mistral, Groq and DeepSeek integration packages. vLLM, Ollama, LangGraph and transformers had no releases in the window.
- Couldn't open or not checked: Qwen's blog page is JavaScript-only, so the Qwen4-Max specs come via QwenCloud's pricing page and FourWeekMBA's quotes of the blog. Reddit (r/LocalLLaMA, r/MachineLearning) rate-limited me after one read, and its feed links didn't line up with titles, so I left Reddit items out. The Verge, VentureBeat and Ars Technica pages didn't render. Today's 16 Nov roundups (TopFive, DeAI, AI Podium, Kamol) weren't published yet. Product Hunt, MLH, DoraHacks and Kaggle weren't checked. I used roundups instead of opening each newsletter. No primary source for the ARC-AGI-3 harness numbers.

## Archive

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

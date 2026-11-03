# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-03

## X Brief: Tue 3 Nov 2026, 9 AM (2 Nov 09:00 to 3 Nov 09:00 IST)

**I checked 15 X accounts (30 posts) and 6 searches (143 results), plus GitHub trending (daily, weekly, Python, TypeScript, Rust, Go, Jupyter), Hugging Face (models, datasets, Spaces, papers), Hacker News and Show HN, r/LocalLLaMA, The Decoder, TechCrunch, The Verge, Simon Willison, Import AI, Latent Space, The Rundown, the OpenAI and Google blogs, Devpost, lablab.ai and public LinkedIn posts. I kept 12 news items, 2 models, 15 repos and projects, and 4 open hackathons.** All times are IST.

- **Anthropic's revised IPO filing:** about $17B of revenue in Q3, a $23.3B quarterly loss, about $895B committed to compute, and a warning that it may soon reach the point where AI is speeding up its own AI research.
- **An MIT team had GPT-6 Astra edit a small model's weights directly, with no training.** It changed 0.016% of Qwen3.5-0.8B's weights, and the model's MATH-500 score went from 7.9% to 48.1%. It was the top story on HN, with 2,095 points.
- **Grok Bot usage limits were cut over the weekend.** Musk says serving it cost too much compared with what it earns. For students: Neural Storm, a students-only AI hackathon, closes **Wed 4 Nov at 20:00**, and OpenAI raised its security bug bounties.

### The one that matters most
**Grok Bot's weekly limits got tighter, and SpaceX says it's on purpose.** Over Halloween weekend, some users found their weekly usage jump from as low as 50% to 100%, and some said their quotas were cut in half. Musk replied on X that "the cost of serving Grok Bot was unsustainably high relative to revenue", and he hasn't said what the new limits are. The Decoder points out that OpenAI (one shared Codex and Chat budget from December) and Anthropic are tightening their flat-rate plans too. If you run a team of bots, check which routines use the most, and space them out before a hackathon week. [TechCrunch](https://techcrunch.com/2026/11/02/elon-musk-throttles-grok-bot-limits-due-to-unsustainably-high-costs/) · 21:53, 2 Nov · [The Decoder](https://the-decoder.com/spacexsi-apparently-cuts-grok-bot-quotas-weeks-after-musk-called-it-his-fastest-growing-product/) · 23:45, 2 Nov

### AI news

#### Labs and models
- Anthropic's amended S-1 shows about $17B of revenue in Q3, about 12 times a year earlier, but only 47% more than Q2, down from 144% growth the quarter before. The net loss was $23.29B, and about $895.4B is committed to compute and data-centre deals. If your project depends on Claude, expect pricing and limits to keep moving while Anthropic tries to show investors it can make money. [CNBC](https://www.cnbc.com/2026/11/02/anthropic-ant-s-1-quarter-financials.html) · [HN](https://news.ycombinator.com/item?id=50337439) · 20:08, 2 Nov · [The Decoder](https://the-decoder.com/anthropic-grows-revenue-twelvefold-but-posts-23-billion-loss/) · 21:56, 2 Nov
- The same filing has a new risk warning. Anthropic says it has used AI to build models whose jumps in ability it didn't spot at the time. It also says its estimates for future models suggest it "may imminently meet" its own policy's threshold for "dramatically accelerated progress attributable to AI". It says no current model has crossed that line. This is the clearest statement from a lab that AI is speeding up its own research. [TechCrunch](https://techcrunch.com/2026/11/02/anthropic-warns-that-its-very-close-to-rsi-capability-aka-self-building-ai/) · 03:44, 3 Nov
- Anthropic added two sentences to Claude Code's prompt on Opus 5.5. They steer it away from recreating a specific existing game, while original games and genre games still work. If your hackathon idea is "remake X", Claude may now refuse it. [The Verge](https://www.theverge.com/ai-artificial-intelligence/1024632/anthropic-claude-ai-video-game-clones) · 00:26, 3 Nov
- Google is shutting down Jules, its coding agent. Its goodbye note suggests exporting your work with a CLI agent, and after 11 Nov Jules becomes read-only. Export anything you still need from it before then. [post](https://x.com/anurag_629/status/2117446173132824609) · 08:08, 3 Nov

#### Products, APIs and security
- OpenAI is raising its Security Bug Bounty rewards and adding bonuses for report quality and loyalty, plus priority campaigns. It is also planning an internal security sprint with Cathedral Systems, whose researchers will attack OpenAI using OpenAI's own models. For a student who's good at security, this is real money. [OpenAI](https://openai.com/index/rewarding-defenders-with-bigger-bug-bounties) · 23:30, 2 Nov · [post](https://x.com/OpenAI/status/2117444048227123277) · 07:59, 3 Nov
- Simon Willison released llm 0.37, his command-line tool for talking to language models. It adds gpt-6.1-sol and gpt-6.1-terra, a command for adding any OpenAI-compatible endpoint, and embeddings for mixed media such as Gemini Embedding 2. The default model is now gpt-6-luna, which costs half as much as the old default. It's a quick way to script calls to many models at once in a hackathon. [post](https://simonwillison.net/2026/Nov/2/llm/) · 05:19, 3 Nov
- The New York Times, the New York Daily News, the Chicago Tribune and the Orlando Sentinel are suing Brave Software. They say Brave scraped their sites, sold AI companies paid access to its search index, and helped users get around paywalls. If your RAG project uses a search API, it matters where that data comes from. [The Verge](https://www.theverge.com/tech/1024588/brave-lawsuit-ai-scraping-new-york-times) · 23:21, 2 Nov

#### Money and business
- Goldman Sachs has cut most staff off from AI coding tools such as Claude Code, and only engineers keep access. Traders and bankers had been using them for months. The bank cites productivity and risk. Vibe-coding by non-engineers is getting pushback at big firms. [The Decoder](https://the-decoder.com/goldman-sachs-pulls-ai-coding-tools-from-traders-and-bankers/) · 01:30, 3 Nov
- Trajectory, an 18-person startup founded by three Stanford classmates, raised $45M at a $300M valuation, led by Sequoia. It keeps retraining open models on user feedback so they improve at specialist work. This "continual learning" loop is a good pattern to copy in a small project. [TechCrunch](https://techcrunch.com/2026/11/02/trajectory-raises-45m-to-make-ai-model-training-accessible-to-nontechnical-experts/) · 04:43, 3 Nov
- 42AI, an Israeli startup, came out of stealth with $62.5M in seed funding for a "behavioural world model". It is being tested at a few brokerages to predict how individual traders react to volatile markets. [TechCrunch](https://techcrunch.com/2026/11/02/42ai-comes-out-of-stealth-with-62-5m-and-a-world-model-that-can-predict-human-behavior/) · 22:00, 2 Nov

#### India
- MeitY's "DEPA for AI Training" plan has hospitals, banks and agencies share anonymised, encrypted data through exchange platforms, so that "the model travels to the data". If it goes ahead, Indian startups could train on local data they can't get today. [The Register](https://www.theregister.com/public-sector/2026/11/02/india-floats-ai-plan-under-which-the-model-travels-to-the-data-rather-than-the-data-travelling-to-the-model/5306872) · 2 Nov
- Sarvam signed an MoU with the Ministry of Defence's HQ Integrated Defence Staff to build AI applications for the Army, Navy and Air Force. These cover decision support, training and data fusion, with humans keeping control of operational decisions. Sarvam now has defence work as well as its 105B Indic model. [Smart Solutions World](https://smartsolutionsworld.com/sarvam-and-ministry-of-defence-sign-framework-for-ai-projects-across-the-indian-army-navy-and-air-force/) · 2 Nov

### New models and weights
No major lab released new weights in the window, and Kimi K3.1 Pro's open weights are still due by 4 Nov. These two models are new to the brief:

| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Hydrogen-1.0 | Deep Principle | Post-trained from GLM-5.3. One poster says the full weights are 1.5 TB. | MIT | It's a science LLM for chemistry, materials and life science, trained on the company's own lab records, including failed runs, and posters say it has 1M context. The repo doesn't include the training data or recipe. Access on Hugging Face is gated. | [HF](https://huggingface.co/deep-principle/Hydrogen-1.0) · [post](https://x.com/BioAgentDaily/status/2117280577401373070) · 21:10, 2 Nov |
| Nemotron-3.5-Transcribe-30B-A4B | NVIDIA | 30B total, 4B active | OpenMDW-1.1 | One open checkpoint does speech-to-text, speaker labels, translation and timestamps, and it supports Hindi, Bengali, Marathi, Tamil and Telugu. One poster says it ranks #1 on the open ASR leaderboard. It came out in October and is trending now. | [HF](https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Transcribe-30B-A4B) · [post](https://x.com/davidcasem/status/2117275860223045944) · 20:51, 2 Nov |

### Benchmarks and leaderboards
- **LLMs can edit neural network weights by reasoning.** MIT CSAIL researchers (Takehi, Teoh, Zhang and Khattab) report that GPT-6 Astra can tell which game a small network was trained on just by reading its 17,253 weights. It also fixed a driving policy that always failed by editing 3.5% of its weights. And it raised Qwen3.5-0.8B's MATH-500 score from 7.9% to 48.1% by changing 0.016% of its weights, with no training loop, and IFEval tripled as well. [blog](https://rikiyat.github.io/blog/weight-space-programming/) · [HN](https://news.ycombinator.com/item?id=50341174) · 23:51, 2 Nov
- **LifeVal** is OpenAI's new benchmark of everyday personal-assistant tasks, such as finding childcare, managing money and handling government paperwork. It's based on feedback from thousands of ChatGPT users. 5.4K likes. [post](https://x.com/OpenAI/status/2117307611338997846) · 22:57, 2 Nov
- **SemiAnalysis's GDPx** ranks 20 models on long agent tasks in 11 fields, including chip design, cybersecurity and law. One poster says the top score is Claude Opus 5.5 at 12.0% and that Mistral isn't on the list. [post](https://x.com/MrDutch310822/status/2117171342361391191) · 13:55, 2 Nov
- **Kimi K3.1 Pro is the #1 open-weights model on DesignArena's Game Dev leaderboard,** taking over from Kimi K3. [post](https://x.com/DesignArena/status/2117315418528575649) · 23:28, 2 Nov
- **ARC-AGI-3 on Kaggle closed on 2 Nov.** Another poster checked the "28.4% for $19" claim from yesterday. It ranks 1,446th of 5,045 teams, and the top public score is 75.56%. [post](https://x.com/thewanderer764/status/2117233022558777814) · 18:01, 2 Nov

### Trending repos and projects
- [vercel-labs/agent-desktop](https://github.com/vercel-labs/agent-desktop) lets AI agents read and use desktop apps through the operating system's accessibility tree instead of screenshots. Each element gets a JSON reference, and the agent takes a snapshot to check each click. Use it to build an agent that fills forms in real desktop apps. Rust, +2,275 today (10,231), #1 on GitHub trending.
- [JustVugg/colibri](https://github.com/JustVugg/colibri) runs very large mixture-of-experts models on ordinary hardware by streaming the experts from disk. It's written in pure C with no dependencies. Try big open models on a laptop without renting GPUs. C, +675 today (46,658).
- [karpathy/nanochat](https://github.com/karpathy/nanochat) is "the best ChatGPT that $100 can buy": the whole pipeline in one repo, from tokenizer through pretraining and finetuning to chat. It's the best way to actually learn how an LLM is trained from start to finish. Python, +321 today (59,962).
- [public-apis/public-apis](https://github.com/public-apis/public-apis) is a big list of free APIs sorted by category. Pick a data source for a hackathon app in minutes. Python, +1,311 today (495,568). [post](https://x.com/sakatayasha/status/2117122158766010703) · 10:40, 2 Nov
- [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) is a single CLAUDE.md file, based on Karpathy's notes on common mistakes LLMs make when coding. Drop it into your repo to make Claude Code behave better. +4,397 this week (228,597).
- [anthropics/skills](https://github.com/anthropics/skills) is Anthropic's public repo of Agent Skills. Copy its format when you write your own skills. Python, +2,828 this week (186,816).
- [cheaper-inference/OmniRoute](https://github.com/cheaper-inference/OmniRoute) is a free, MIT-licensed AI gateway: one endpoint for 375 providers (150+ of them free) and 1,400+ models. It helps you stretch free tiers when your credits run low. TypeScript, +402 today (84,012).
- [mksglu/context-mode](https://github.com/mksglu/context-mode) is a local plugin that keeps tool output out of your coding agent's context window, using a sandbox and SQLite search. Its README claims 99% less context used. Use it to make long agent runs cheaper. TypeScript, +151 today (33,300).
- [Nasiko-Labs/nasiko](https://github.com/Nasiko-Labs/nasiko) is an open runtime for AI agents. It's a base for hosting several agents of your own. Rust, +293 today (11,543).
- [vercel-labs/agent-browser](https://github.com/vercel-labs/agent-browser) is a browser-automation CLI for AI agents, a sister project to agent-desktop. Use it for agents that scrape or test web apps. Rust, +136 today (45,295).
- [kgoedecke/doop](https://github.com/kgoedecke/doop) is an open-source, multiplayer design canvas where people and AI agents design together live, with MCP built in. Fork it for a design-tool track. TypeScript, +125 today (1,572).
- [mvschwarz/openrig](https://github.com/mvschwarz/openrig) builds lasting teams out of Claude Code, Codex and Pi agents, with roles, shared context and assigned work. TypeScript, 8,564 stars.
- [Crosstalk-Solutions/project-nomad](https://github.com/Crosstalk-Solutions/project-nomad) is an offline-first knowledge server with Wikipedia, books, courses, maps and optional local AI. It's a good base for an offline education project for low-connectivity areas. TypeScript, +255 today (41,903).
- [gastownhall/beads](https://github.com/gastownhall/beads) is a memory upgrade for coding agents. It's a lighter alternative to claude-mem. Go, 28,439 stars.
- **Subvocal** is smart glasses that turn silent mouthing into text at the speed of speech. Two Georgia Tech CS students started it at Stanford's TreeHacks in February and are now in YC. It shows how far a hackathon project can go. 585 points. [Show HN](https://news.ycombinator.com/item?id=50340088) · 22:46, 2 Nov

### Hackathons
- **Neural Storm** (Devpost, run by JNTUH) is a 48-hour AI/ML hackathon with three tracks and 15 problem statements. It's online, students only and open to all countries, with ₹20,000 in cash prizes. The deadline is **4 Nov at 20:00 IST** (confirmed on the event page). [event](https://neuralstorm.devpost.com/)
- **Flip the Switch** (WeMakeDevs) starts **4 Nov**, and 5,000 builders have registered. Track 02 is personal or creative workflows built with Switch and AI agents, and 20 random submissions get free swag. Yesterday's brief has the details. [post](https://x.com/WeMakeDevs/status/2117239024394088642) · 18:24, 2 Nov
- **HackIGNISIA 2026** (UDTech India) is a free national online AI and innovation hackathon in November, with tracks for AI for social impact, smart and sustainable India, and the future of technology. The post gives no prize or exact deadline. [LinkedIn](https://www.linkedin.com/posts/udtech-india_hackignisia2026-udtechindia-hackathon-activity-7515735781269827584-DcQr)
- **Concordium Trusted Agents Hackathon** (with Encode Club) is a free, six-week online programme, solo or in teams. It has three weeks of workshops from 2 Nov, then three weeks building on Concordium's blockchain testnet, so your agent can prove a verified human is behind it and can pay other agents. No cash prize is listed, but winners can pitch for its 75M CCD grants programme. The deadline is **10 Dec at 05:29 IST**. [details](https://www.concordium.com/article/concordium-trusted-agents-hackathon-encode-club)
- **Winners:**
  - A two-person team won the **Paytm Build for India AI hackathon** with "hisaab bolo", which helps merchants keep ledgers and keep customers coming back. [post](https://x.com/rahil_mavani/status/2117144455677702309) · 12:09, 2 Nov
  - A two-founder team won **YC's Call-My-Agent hackathon** against 90+ teams. They're building their own hardware alongside an operating system. [post](https://x.com/AdamZinebi1/status/2117301930821300473) · 22:34, 2 Nov
  - **The Spy Monster** won best use of agent_relay at a YC hackathon. It's a game where one of three AI ghosts secretly leaks what you tell it, which shows how data can leak between agents. [post](https://x.com/w_milczynska/status/2117340618251002364) · 01:08, 3 Nov
  - CrowdStrike and NVIDIA's first **AgentWorks Hackathon** drew nearly 100 agents and named three winners. [post](https://x.com/CrowdStrike/status/2117253606759977456) · 19:22, 2 Nov
  - One builder indexed **93 AI-lab hackathons since 2025**: 31,980 projects and 585 winners, with the winning code linked. It's a goldmine for seeing what judges pick. [post](https://x.com/the_pushh/status/2117113776839475552) · 10:07, 2 Nov

### Student perks and credits
- **Anthropic Residency** is paid ($350K to $500K a year, prorated) and lasts six weeks to six months, with a mentor and a compute budget. No ML background, PhD or papers are needed, but it's aimed at professors, technical founders and staff-level engineers rather than students. Applications close **22 Nov at 23:59 PT** (13:29 IST, 23 Nov). [Anthropic](https://alignment.anthropic.com/2026/anthropic-residency/) · [post](https://x.com/AnthropicAI/status/2117343929960112486) · 01:21, 3 Nov
- **Mozilla Foundation Fellows 2027-28** gives up to $125,000 to each of 10 fellows. The first step is a Letter of Intent, due **17 Dec 2026**, and the post says there's no country list, so India can apply. [post](https://x.com/anurag_629/status/2117273136227856587) · 20:40, 2 Nov
- OpenAI's bigger bug bounties (above) are the best paid opportunity today if you do security research.

### Grok Bots
- SpaceXAI's team shared 91 free Grok Bots: 56 on the official use-cases page and 35 more elsewhere. One reads your inbox, one chases unpaid invoices, one calls customers. 331 likes, 606 bookmarks. [post](https://x.com/spectnfa/status/2117356701007364449) · 02:12, 3 Nov
- SpaceXAI released a free one-hour workshop on going from an empty GitHub org to a company run by a team of Grok Bots in 72 hours. [post](https://x.com/virgilxbt/status/2117337796398526692) · 00:57, 3 Nov
- **GrokBot Mapper** turns a goal written in one sentence into a ready team of bots, showing them in order on a 3D map of every Grok Bot. [post](https://x.com/N01ennn/status/2117309730846560764) · 23:05, 2 Nov
- Brian Roemmele's directory is now at 8,638 bots after 285 were added. It also built 70 requested bots in 24 hours. [post](https://x.com/BrianRoemmele/status/2117305132656537953) · 22:47, 2 Nov
- A tech artist laid off in September ran his whole job search with a team of Grok Bots and landed a full-time lead role. His thread covers what worked and what got messy, and thanks dr eggbot. [post](https://x.com/CybertruckATX/status/2117436124243308986) · 07:28, 3 Nov

### Build idea of the day
For **Flip the Switch** (starts 4 Nov), build a voice-driven desktop helper for Track 02's personal workflows. You send a voice note in Hindi or English to your Slack or Discord. **Nemotron-3.5-Transcribe** turns it into text, and your coding agent, connected through Switch, uses **agent-desktop** to do the task in real desktop apps, like adding an expense to a budget sheet. It checks each click against an accessibility snapshot. Add **context-mode** so long runs don't fill the agent's context window, and you have a demo judges can watch work end to end.

### What the field is arguing about
- **Does editing weights directly replace training?** The Astra post drew 681 comments on HN. On r/LocalLLaMA, people are calling it the best argument yet for open weights, since you can only do this to a model you can download. [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/comments/1xma0tw/gpt6_astra_edits_qwen_weights_math500_79_to_481/) · 02:55, 3 Nov · [post](https://x.com/sanchitmonga22/status/2117337493741994313) · 00:56, 3 Nov
- **Should Anthropic's IPO go ahead?** A Tech Policy Press op-ed argues the SEC should block it to protect the public (236 points). Another post argues that Anthropic's growth has flattened (179 points). [op-ed](https://www.techpolicy.press/the-sec-should-block-anthropics-ipo-to-protect-the-public/) · [HN](https://news.ycombinator.com/item?id=50344919) · 04:00, 3 Nov · [post](https://www.regenerator1.com/p/anthropics-growth-just-flattened) · [HN](https://news.ycombinator.com/item?id=50344958) · 04:03, 3 Nov
- **Whose quantized models can you trust?** r/LocalLLaMA is arguing over ISTA's GSQ-RCO quants against Unsloth's, including a post pointing out inconsistencies in Unsloth's LiveCodeBench results. [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/comments/1xm9i4x/inconsistencies_in_unsloths_livecodebench_results/) · 02:35, 3 Nov
- **Will Qwen stay open?** Qwen's new chief said on the main stage at Alibaba's Yunqi Conference that Qwen will stay open source through Qwen 5.0. [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/comments/1xm28e6/official_statement_qwen_models_will_stick_to_open/) · 22:12, 2 Nov

### Worth reading in full
1. "Sparks of Weight-Space Programming" (MIT CSAIL) has interactive demos of an LLM reading and rewriting network weights, and it may change how you think about fine-tuning. [blog](https://rikiyat.github.io/blog/weight-space-programming/)
2. "Agentic Backdoors via Pretraining Poisoning" (with Nicholas Carlini) shows that poisoning just 0.1% of pretraining data can plant a backdoor that makes a CLI agent run an attacker's commands. Against the 4B model it worked about 92% of the time. Read it before you trust any agent with shell access. [paper](https://arxiv.org/abs/2610.37741) · [HN](https://news.ycombinator.com/item?id=50341334) · 00:00, 3 Nov
3. "Egoless Mathematics in the AI Era", a guest post on Terence Tao's blog by Karthik C. S., Amit Sahai and Jie Xue, asks what mathematical work is for once AI can produce results. [post](https://terrytao.wordpress.com/2026/11/02/egoless-mathematics-in-the-ai-era/) · [HN](https://news.ycombinator.com/item?id=50341736) · 00:24, 3 Nov
4. The Cloud Security Alliance's note on China's first frontier-AI export controls (MOFCOM Announcement No. 48) explains the draft rules. They would restrict model weights above 10^26 FLOPs of training compute or 2T parameters, or for models in the global top 10, and the draft is open for comment until 15 Nov. [note](https://labs.cloudsecurityalliance.org/research/csa-research-note-china-ai-export-controls-announcement-48-2/) · [HN](https://news.ycombinator.com/item?id=50334038) · 12:57, 2 Nov
5. Import AI 479 covers low-latency tasks versus LLMs, and Genie 4. [newsletter](https://importai.substack.com/p/import-ai-479-spacewar-low-latency) · 20:00, 2 Nov

### Quiet
- @GoogleDeepMind, @AIatMeta, @huggingface and @karpathy posted nothing original in the window. @MistralAI posted a Large 4 chemistry demo, @_akhaliq posted one paper (GLOW-FM), @simonw posted about the Census Bureau, and @devpost promoted a QNX build and a Kiro livestream.
- @trending_repos named t3code repo of the day (+3,216) and impeccable repo of the week (+12,017), and @chinchoukou posted claude-mem at #1. All three were covered in earlier briefs. @GithubProjects mostly posted non-AI projects.
- @WeMakeDevs posted about Flip the Switch and an AI-usage survey with an iPhone giveaway. @anurag_629 posted about Jules and the Mozilla fellowship (both above).

### Couldn't open
- OpenAI's LifeVal and security-sprint pages blocked my reader, so those items come from OpenAI's X posts and RSS summaries. Hydrogen-1.0's model card is gated. Business Insider's story on Anthropic's internal AI spending is paywalled.
- r/MachineLearning and VentureBeat's feeds came back empty. There were no new issues from TLDR AI or Ben's Bites, and Hugging Face's daily papers haven't updated since 30 Oct. llama.cpp shipped small builds (Clover model support, PocketTTS voices), vLLM put out a v0.33.0 release candidate, Ollama and LangChain only shipped minor releases, and LangGraph and transformers had none.
- Most other open Devpost AI events are limited to one university or one country. The Devpost and lablab.ai hackathons in earlier briefs are still open, and nothing new showed up on lablab.ai.

## Archive

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

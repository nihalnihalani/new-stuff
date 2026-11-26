# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-26

## X Brief — Thursday 26 Nov 2026 (window: 25 Nov 09:00 → 26 Nov 09:00 IST)

Checked: 15 watch-list X accounts and 6 watch-list searches (217 posts pulled, ranked by engagement); GitHub trending (daily, weekly, Python, TypeScript, Rust, Go and Jupyter Notebook); Hugging Face trending models, datasets and Spaces, plus daily papers; the Hacker News front page and Show HN; release notes for llama.cpp, vLLM, Ollama, LangChain, LangGraph and transformers; The Decoder, TechCrunch, The Verge, VentureBeat, TLDR AI, lab sources (OpenAI, Anthropic, Google Research, Hugging Face, Cognition) and Indian outlets (ThePrint, Indian Express, BusinessLine, Inc42); Devpost, Unstop, Starfield Labs (formerly lablab), the PLE Kaggle page and LinkedIn (via web search) for hackathons; student-perk searches. All times are IST.

**TL;DR**
- **AI labs posted a pile of major math results overnight.** OpenAI disproved the polynomial Hirsch conjecture and gave a tight bound for the FFT. Google's Cogentic posted six papers, including integer factoring with a proven running time. An Anthropic researcher posted a shorter Lean proof of the Generalized Riemann Hypothesis. Scott Aaronson's "HOLY SHIT" post got 1,010 points on HN.
- **Agents are now doing real engineering work.** Anthropic moved its Messages API from Python to Rust, with teams of Claude agents checking the new version against the old one. The result uses about 70% less CPU per request. Hugging Face published its report on running 1,000 agents at once and open-sourced the tools.
- **India:** MeitY says Sarvam didn't misuse IndiaAI support, and that the mission will move from paying for training to paying for inference. Chariot-1 launched with text, TTS and ASR in one model, covering English and 10 Indian languages. New open weights: Avalon-M1-Mini (120B, MIT), KRAFTON's Raon-1 mini (30B-A4B, Apache-2.0) and Baidu's ERNIE 5.5 Flash Preview.

### The one thing that matters most
**AI-made math has turned into a daily flood.** In about 24 hours, OpenAI posted a disproof of the polynomial Hirsch conjecture. It builds polytopes whose graph diameter grows faster than any polynomial, so no edge-walking (simplex-style) method can be polynomial in the worst case. OpenAI also proved that the FFT needs exactly N(log N)^(1/2+o(1)) linear gates, and that bound is tight in both directions. Google's Cogentic posted six papers. One proves integer factoring runs in L_N[1/3] time with no unproven assumptions. That matches the number field sieve's heuristic speed, so it doesn't make RSA weaker in practice. Aaronson says he is "virtually certain, from multiple reliable sources" that labs are sitting on results that would break deployed cryptography. He won't say what they are without details. None of this is peer-reviewed. The new GRH repo says outright that "no mathematician has read it through." For a student, two skills now pay off: reading formal (Lean) proofs critically, and building software whose cryptography can be swapped out easily. [Aaronson](https://scottaaronson.blog/?p=10379) · [HN](https://news.ycombinator.com/item?id=50646108) (26 Nov 00:41)

### AI news

#### Research and math
- **Google Cogentic posted six papers on GitHub with no announcement.** They cover integer factoring, discrete logs in small-characteristic fields, 1/5-approximate Nash equilibria, and the log-rank conjecture. The papers are headed "This is not an official Google product". A paper repo like this is a good thing to try to verify with friends. [Google Research](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) · [HN](https://news.ycombinator.com/item?id=50642086) (25 Nov 19:03)
- **OpenAI says the polynomial Hirsch conjecture is false.** Alongside it is a matching lower and upper bound for finite Fourier transforms. If you study algorithms, it's worth reading why a polytope's diameter limits the simplex method. [Hirsch paper](https://github.com/openai/math/blob/main/preprints/Superpolynomial-graph-diameter-of-simple-polytopes-November-24-2026/paper.pdf) · [FFT paper](https://github.com/openai/math/blob/main/preprints/The-logarithmic-exponent-of-finite-Fourier-transforms-November-24-2026/paper.pdf) · [HN](https://news.ycombinator.com/item?id=50644980) (25 Nov 23:04)
- **A shorter Lean proof of GRH for Dirichlet L-functions is now public.** It comes from an Anthropic researcher working with colleagues and Claude. There's a readable edition of about 300,000 lines and a compact one of about 76,000, and a build takes one to two hours on 12 cores. It's a real-world Lean project you can build yourself. [GitHub](https://github.com/lsernau/grh-lean) · [HN](https://news.ycombinator.com/item?id=50648050) (26 Nov 03:18)

#### Agents at work
- **Anthropic moved its Messages API from Python to Rust.** It used the live Python service as the reference and had Claude agents track down and fix every difference. The Rust version uses about 70% less CPU per request. Checking a migration against the old system is the trick to copy for any big agent-written change. [Anthropic](https://www.anthropic.com/research/migrating-api-to-rust) · [X post](https://x.com/AnthropicAI/status/2125627317263466739) (25 Nov 21:56)
- **Hugging Face's field report on running 1,000 agents together.** Lessons from running PyBot with 1,000 DeepSeek agents for over a week include monitoring the swarm, git breaking, early signs of misalignment, and bottlenecks in inference and context compaction. It also open-sourced legion and msgboard. It's the most concrete guide yet for anyone building a multi-agent project. [HF report](https://huggingface.co/spaces/HuggingFaceSwarms/scaling-swarms) · [X post](https://x.com/lvwerra/status/2125612908499349833) (25 Nov 20:59)
- **Hugging Face launched Nightwatch, an agent that watches for security problems.** It was built after a swarm of frontier agents hit the Hub in July. It watches token use, logins and visibility changes, then reports to Slack. HF says it has already flagged a zero-day exploit attempt. It's an add-on for Enterprise orgs, but the design is a good template for a "defender agent" project. [HF docs](https://huggingface.co/docs/hub/en/enterprise-nightwatch) · [X post](https://x.com/Thom_Wolf/status/2125530620948336798) (25 Nov 15:32)

#### Products, policy and business
- **OpenAI is testing Private Inference with a small group of business customers.** It uses confidential computing so OpenAI staff can't see prompts or replies. If it spreads, private data like health or legal documents gets easier to build on. [TNW](https://thenextweb.com/news/openai-private-inference-testing-customers) · [The Decoder](https://the-decoder.com/openai-wants-companies-to-trust-it-with-sensitive-work-by-promising-not-to-look-at-their-data/) (25 Nov 23:52)
- **ChatGPT is merging Chat and Work under one usage limit.** The Instant model stays unlimited. OpenAI says a small share of heavy users may hit limits sooner, with a wider rollout in December. If you rely on a Plus plan for coding, watch your usage. [TechCrunch](https://techcrunch.com/2026/11/25/openai-says-heavy-chatgpt-users-may-hit-limits-sooner-as-it-merges-chat-and-work/) (26 Nov 01:33)
- **Dario Amodei called claims that Anthropic wants humans to hand control to AI "absurd".** He suggested limits on recursive self-improvement. Expect "how much autonomy" to become a policy fight that shapes which agent features ship. [TechCrunch](https://techcrunch.com/2026/11/25/anthropics-dario-amodei-calls-accusations-of-surrendering-human-control-to-ai-absurd/) (26 Nov 01:14)
- **US chip curbs and anti-distillation measures are reportedly slowing Chinese labs.** The Information reports that DeepSeek researchers think their gap to top US models could grow to nine months, and that Moonshot cancelled a $150M Blackwell deal. That could slow the flow of cheap open weights you build on. [The Decoder](https://the-decoder.com/us-chip-access-curbs-and-anti-distillation-measures-are-reportedly-already-slowing-chinese-ai-labs/) (26 Nov 02:21)

#### India
- **MeitY says Sarvam didn't misuse IndiaAI support.** It also says the mission will move from funding training to funding inference. Secretary S. Krishnan said Sarvam's Token Factory runs on GPUs it bought itself, and that the government is still backing its work toward a 1-trillion-parameter model. Cheaper inference subsidies would help student startups more than training subsidies would. [ThePrint](https://theprint.in/tech/no-misuse-of-indiaai-mission-support-by-sarvam-meity-secretary-ai-labs-also-need-revenue-model/3108705/) (25 Nov 16:56) · [Indian Express](https://indianexpress.com/article/business/sarvam-chinese-ai-models-indiaai-mission-support-10978438/)
- **Chariot launched Chariot-1, an IndiaAI Mission model.** One backbone does text generation, TTS and ASR in English and 10 Indian languages. Its "IndicShift" shared alphabet uses 2.5× fewer tokens for Indian text, and Krishnan said the AI regulation papers are "in the final stages". It's a useful base if you're building Indic voice apps. [BusinessLine](https://www.thehindubusinessline.com/info-tech/indiaai-backed-chariot-1-combines-text-speech-and-recognition-in-one-model/article71743519.ece) (25 Nov 21:14)

### New models and weights
| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Avalon-M1-Mini | General Reasoning | 120B | MIT | Trained to work as an agent team (a CEO plus up to 8 specialists on a message board). In team mode, IMO-ProofBench-Advanced rises from 23.8% to 39.0%. Comes with its harness | [HF](https://huggingface.co/GeneralReasoning/Avalon-M1-Mini) · [Paper](https://arxiv.org/abs/2611.32539) · [X post](https://x.com/GenReasoning/status/2125534304008655339) (25 Nov 15:47) |
| Raon-1 mini | KRAFTON | 30B-A4B MoE | Apache-2.0 | Trained from scratch and strong at Korean chat and agentic tasks. There's a free playground for a limited time | [HF](https://huggingface.co/KRAFTON/Raon-1-mini) (posted 24 Nov 18:47) |
| ERNIE 5.5 Flash Preview | Baidu | 280B total, 14B active, 1M context | Apache-2.0 | Weights are now on HF. It's a mid-training checkpoint aimed at coding and game development | [HF](https://huggingface.co/baidu/ERNIE-5.5-Flash-Preview) (posted 23 Nov) |
| OmniEVIE-4B | Tencent | 4B | Apache-2.0 | A multimodal embedding model. One post says it scores 60.68 on MMEB-v3, ahead of a 9B rival, so it's a cheap retriever for image+text RAG | [HF](https://huggingface.co/tencent/OmniEVIE-4B) · [X post](https://x.com/paperswithcodee/status/2125530235802100031) (25 Nov 15:31) |
| AURA | Kyutai | 1.3B and 5B | CC-BY-NC-4.0 | Avatars that lip-sync to speech in real time. A post says the 1.3B streams 576p at 20.7 fps on one GPU. Non-commercial license | [HF](https://huggingface.co/kyutai/AURA-1.3B) · [X post](https://x.com/dipanshu_harjai/status/2125609475360895152) (25 Nov 20:46) |
| SWE-2.1 | Cognition | Not stated (RL on Kimi K3) | Proprietary | A coding and agent model. Terminal-Bench 4.1 goes from 24.2 to 50.0, and it scores 80 on ExploitBench | [Cognition](https://cognition.com/blog/swe-2-1) (24 Nov 21:30) |

### Benchmarks and leaderboards
- **GPT-6.2 Astra is the first model to beat Googlers' 2015 code-golf records,** per this benchmark. It has 32 problems in 8 languages, each model gets 30 minutes per problem, and the score is byte count. [Leaderboard](https://bjin.github.io/go-codegolf-benchmark/#leaderboard) · [HN](https://news.ycombinator.com/item?id=50601280)
- **SWE-2.1 against frontier models (Cognition's own numbers):** FrontierCode 2.0 is 41.3, against 47.3 for Claude Opus 5.5. Terminal-Bench 4.1 is 50.0, against 65.8. [Cognition](https://cognition.com/blog/swe-2-1)
- **Using latency to identify a hidden model.** Modaic timed 9,984 prompts against TypeSafe's "Jev" model and concluded that its tokenizer and throughput point to a Qwen3.5-35B-A3B base. It's a neat method to borrow for an evaluations project. [Modaic](https://modaic.dev/blog/latency-doesnt-lie) · [HN](https://news.ycombinator.com/item?id=50648823) (26 Nov 04:27)
- **New agent benchmarks on HF Papers:** SpecEngineeringBench tests coding agents as specification engineers, and ICLWorld tests in-context learning from digital to physical worlds. [SpecEngineeringBench](https://huggingface.co/papers/2611.32973) · [ICLWorld](https://huggingface.co/papers/2611.32649)

### Trending repos and projects
1. **[n8n-io/nod](https://github.com/n8n-io/nod)** (TypeScript, ★3,608, +1,008 this week). An open-source personal agent with its own computer: it chases invoices, preps your calls and cancels trials on real websites, asking before it acts. You could fork it into a campus-errands agent that runs on your own machine and your own model.
2. **[alesha-pro/llm.asm](https://github.com/alesha-pro/llm.asm)** (Assembly, ★394, created 25 Nov; [HN](https://news.ycombinator.com/item?id=50648365)). It runs Qwen3-0.6B inference in 12 KB, a bootable bare-metal OS in 22 KB, and a Mini-GPT trainer, all in pure x86-64 assembly. It's a great way to see exactly what inference does, one instruction at a time.
3. **[huggingface/legion](https://github.com/huggingface/legion)** (Python, ★33) and **[huggingface/msgboard](https://github.com/huggingface/msgboard)** (Python, ★26). Legion launches thousands of agents on local machines, Slurm or HF Jobs, and msgboard is a message board that agents and humans share. Together they're the plumbing for a multi-agent hackathon project.
4. **[Harness Hub community adapters](https://harness-hub-community-adapters.hf.space/)** (HF Space). Harness adapters for Inkling-2-Mini and Qwen3.8-Flash-Next are being trained in the open, with all weights, data and checkpoints (GGUF too) public, and you can comment on results. It's a chance to watch, and join, a real post-training run. [X post](https://x.com/yb2698/status/2125568461581750447)
5. **[Hill-climbing Inkling 2 Mini inference](https://huggingface.co/blog/inkling-2-mini-inference-hillclimb)** (HF blog). Opus 5.5 tuned vLLM flags on one RTX PRO 6000 and got single-user decode from 136 to 190.6 tok/s. Run the same loop on whatever GPU you have. [X post](https://x.com/NielsRogge/status/2125643276296327385)
6. **[onatm/rustling](https://github.com/onatm/rustling)** (Rust, ★5, Apache-2.0; [Show HN](https://news.ycombinator.com/item?id=50646482)). A Rust agent with its own Inkling 2 Mini inference engine for Apple Silicon. It's a small codebase if you want to learn how a local agent and its engine fit together.
7. **[USA Civ map by Karpathy](https://karpathy.ai/usaciv/)** (project site). Claude Opus 5.5 spent 7 hours and wrote 45K lines to merge 31 public US data sources into a Civilization-style hex map. It's a template for turning open government data into a game. [X post](https://x.com/karpathy/status/2125779541952246039) (26 Nov 08:01)
8. **[datawhalechina/llm-universe](https://github.com/datawhalechina/llm-universe)** (Jupyter Notebook, ★14,348, on today's Jupyter trending). A beginner's tutorial for building LLM apps (in Chinese). You could follow it to build a first RAG app.
9. **[lusingander/serie](https://github.com/lusingander/serie)** (Rust, ★2,205). It draws your git commit graph as an image inside supported terminals. Handy for reviewing what your coding agents committed. [X post](https://x.com/GithubProjects/status/2125622610507841870)

Still trending, and already covered in earlier briefs: Claude-BugHunter is #1 again with +1,652 stars today ([X](https://x.com/trending_repos/status/2125562202124079152)). last30days-skill gained +945 today ([X](https://x.com/chinchoukou/status/2125665875965657348)), firecrawl +1,135 ([X](https://x.com/chinchoukou/status/2125605481351876800)) and autoclip +880 ([X](https://x.com/chinchoukou/status/2125771574775345513)).

Release notes: llama.cpp bumped its version to 1.1.0 ([b12752](https://github.com/ggml-org/llama.cpp/releases/tag/b12752)) and added Tencent Hy4 flash support ([b12755](https://github.com/ggml-org/llama.cpp/releases/tag/b12755)). langchain-anthropic 1.7.13 now accepts custom HTTP and SDK clients ([release](https://github.com/langchain-ai/langchain/releases/tag/langchain-anthropic%3D%3D1.7.13)), and the vLLM team posted vLLM-GR for generative recommendation ([blog](https://vllm.ai/blog/2026-11-24-vllm-gr-announcement)). vLLM, Ollama and transformers had no releases in the window.

### Hackathons
**Open, soonest deadline first** (deadline confirmed on the event page or post unless noted):
1. **OBSCURA: Satellite AI Research Challenge (Devpost)**: online, students only, all countries; small prize ($50 pool); **deadline 30 Nov, 20:30**. [Devpost](https://obscura.devpost.com/)
2. **Global AI Hackathon 2026 (BVDAS × DevNexus)**: online and open to students worldwide; build a web app that solves an everyday problem; solo or teams of up to 5; grand prize PKR 20,000+; **registrations close 5 Dec**. [LinkedIn](https://www.linkedin.com/posts/bvdasofficial_globalaihackathon2026-bvdas-devnexus-activity-7522862884645756928-U4f1)
3. **CodeCrafters India 2026 (HackWithPune)**: national, online, free; ₹30,000 pool plus incubation and paid-internship chances for the top 3; UG and PG students, teams of 1–6; three rounds from 3 Dec, **final round closes 14 Dec, 23:59**. [Event page](https://wecodecoders.in/events/codecrafters-india)
4. **AI OpenBuild (Devpost)**: online, students only, beginner-friendly; $150 first prize plus 8 runner-up mentions; **deadline 11 Dec, 10:15**. [Devpost](https://ai-openbuild.devpost.com/)
5. **India AI Open 2026 (AccioJob, on Unstop)**: online, free; ₹50,000 winner, ₹25,000 and ₹15,000 runners-up, plus ₹30,000 for other top performers; open to students and engineers; **registration closes 11 Dec, 23:59**, and the contest ends 26 Dec. [Unstop](https://unstop.com/hackathons/india-ai-open-2026-free-ai-talent-contest-for-students-and-engineers-acciojob-1820502)
6. **HackerRank Orchestrate, December 2026**: a 24-hour solo AI-agent build, online and open globally; $1,200 first prize and $300 for 2nd–5th; you get a 30-minute voice interview with an AI judge; **starts 12 Dec, 18:00** (registration deadline not stated). [LinkedIn](https://www.linkedin.com/posts/ambition-arena_hackerrank-orchestrate-aihackathon-activity-7526703703618183168-XHEP)
7. **Physical-Engineering's Last Exam (Google, on Kaggle)**: build an agent harness for 56 hidden engineering tasks, with a starter template ready; $250K / $100K / $50K; **runs until 5 Jan 2027**. [PLE](https://ple-bench.com/competition)

**Winners**
- **Namma AI Hackathon 2026 (Karnataka):** Minister Priyank Kharge honoured the winning Edge AI teams at Bengaluru Tech Summit 2026. More than 2,700 people took part, with support from Arm, nasscom and the UK–India Technology Security Initiative. [X post](https://x.com/UKinBengaluru/status/2125468289937875026)
- **WeMakeDevs Festive Hacks (WeAreDevs Conference India):** teams built with Flagsmith, NudgeBee and Sarvam AI, and the winning team gets a sponsored trip to Berlin. Judging was underway, and no winners had been posted by the end of the window. [X post](https://x.com/WeMakeDevs/status/2125483418876334340)

### Student perks and credits
- **Nebius AI Builder Program: $25 in GPU credits, no card needed.** That covers about an afternoon on a B300 or up to a day on an H100 at Spot prices, and it's free to join. Coverage says the credits last 90 days and are for learning or prototyping only. [Nebius](https://dev.nebius.com/builders)
- **Google AI Plus free for 12 months through Internshala (India),** per coverage. It's for students graduating in 2026 or later and needs an Indian payment method. It auto-renews at ₹399/month unless you cancel. I couldn't load Internshala's page to confirm. [Coverage](https://coursejoiner.com/educational/google-gemini-ai-plus-1-year/)
- **Wiro for Students: up to $200 in credits for 12 months.** You apply with a school email and get 1,000+ image, video, audio, 3D and language models through one OpenAI-compatible API. This is a standing offer, not new today. [Wiro](https://wiro.ai/student)
- **OpenAI Researcher Access Program:** up to $1,000 in API credits for eligible academic researchers, reviewed every quarter. This is also a standing offer. [OpenAI Help](https://help.openai.com/en/articles/10139500-researcher-access-program-faq)

### Grok Bots
- **A thread collects xAI's 19 official Grok Bot guides,** grouped by team: engineering, sales, product, marketing, support and more. [Guides](https://x.ai/bot/guides) · [X post](https://x.com/maestrooth/status/2125641417787646119)
- **@0x_kaize built Grokverse,** a directory of Grok Bots that is now on the Moby Agent Marketplace. [X post](https://x.com/0x_kaize/status/2125622206994497993)
- **@testafortedev opened "Bot Boardwalk",** a curated shelf of Grok Bots that you can add yours to in 3 steps. [X post](https://x.com/testafortedev/status/2125786909163110551)
- **@BhosalePratim submitted the Gradium MCP to Grok Bot** and plans bots for video creation and voice-agent pipelines. [X post](https://x.com/BhosalePratim/status/2125623090394906999)
- **Simon Willison asked how many reply bots run on an unmodified Grok Bot.** He then noted that, by default, Grok Bot needs you to approve each post it writes. [X post](https://x.com/simonw/status/2125619997796123135) · [X post](https://x.com/simonw/status/2125630274520457326)

### Build idea of the day
**A "Civ map" of your own state for AI OpenBuild (Devpost, students only, closes 11 Dec 10:15).** Copy the idea behind Karpathy's USA Civ map: pull a handful of public datasets onto one hex grid and turn them into game "yields" (GDP becomes gold, colleges become campuses). Use huggingface/legion to run a few agents in parallel, one per data source, and have them post progress and conflicts to huggingface/msgboard so you can step in. Spend the Nebius $25 GPU credit to host an open model for the agents. Keep it to one state and about five data sources so it's done before the deadline.

### What the field is arguing about
- **Should we trust AI proofs before humans read them?** Aaronson says to assume proofs from OpenAI or Anthropic are correct unless shown otherwise. Independent builders point out that Lean only checks the formal statement as written, which still has to be read against the intended math. [Aaronson](https://scottaaronson.blog/?p=10379) · [Proofs & Reasons](https://proofsandreasons.io/vp-vnp-oleans.html)
- **Swarms or one agent?** Patrick McKenzie calls multi-agent coding a paradigm shift. Paradigm3's study (per TLDR AI's summary) finds that, at equal token budgets, a single agent with fresh context resets beats a swarm, and that swarms mostly buy speed. [Kalzumeus](https://www.kalzumeus.com/2026/11/25/multiagent-coding-is-the-future/) · [HN](https://news.ycombinator.com/item?id=50645541) · [Paradigm3](https://www.paradigm3.org/research/swarms)
- **"An AI agent that lives on someone else's server can be switched off by someone else."** This was the top post in the open-weights search (244 likes), arguing for agents that run on your own hardware. [X post](https://x.com/superpobe/status/2125511793036713995)
- **Should strong students drop out?** OpenAI's Noam Brown argued at a poker-bot tournament that talented students should, as AI enters "a very steep rate of progress". [The Decoder](https://the-decoder.com/openai-o1-co-creator-noam-brown-urges-promising-students-to-drop-out-as-ai-enters-a-very-steep-rate-of-progress/) (24 Nov 23:28)

### Worth reading in full
1. [Scott Aaronson, "HOLY SHIT HOLY SHIT HOLY SHIT HOLY SHIT"](https://scottaaronson.blog/?p=10379): the clearest account of what this week's results mean for complexity theory, from someone qualified to judge.
2. [Anthropic, migrating the Messages API to Rust](https://www.anthropic.com/research/migrating-api-to-rust): a practical recipe for checking agent-written rewrites against production.
3. [Hugging Face, Scaling swarms to thousands of agents](https://huggingface.co/spaces/HuggingFaceSwarms/scaling-swarms): an honest field report on what breaks when you run 1,000 agents at once.
4. [What VP ≠ VNP means](https://www.friedgil.com/vpvnp): a three-minute explainer (via TLDR AI) of the algebraic P vs NP result from earlier this week.
5. [Latency doesn't lie](https://modaic.dev/blog/latency-doesnt-lie): a fun piece of detective work on identifying a hidden model's base from timing alone.

### Quiet accounts and anything I couldn't open
- Quiet: @AIatMeta and @MistralAI (no posts in the window). @OpenAI posted once (a ChatGPT ad), @GoogleDeepMind once (a Gemini 4 Neon demo) and @trending_repos once. @anurag_629 posted only Python quizzes.
- I couldn't open: Reddit (r/LocalLLaMA and r/MachineLearning returned nothing or timed out), Product Hunt (no launch list loaded), DoraHacks' hackathon list, Kaggle (captcha), Ars Technica's story on AI agents exploiting a zero-day, Internshala's offer page, and The Decoder's Noam Brown piece past its intro (paywall).
- Not checked today: Reuters, Ben's Bites, Import AI, Latent Space, The Rundown and MLH.
- Skipped as repeats from earlier briefs: Bonsai 2.5, MAGI-2, the 9/4 matrix exponent, GPT-6 protein design, Claude Artifacts as apps, the MCP update, Ling-3.2-air, most of the GitHub trending list, and the Kiroween, Deck the Pixels, AWS MSP and PromptWars hackathons. I also skipped a wave of copy-paste hype threads about Grok Bot.

## Archive

- [2026-11-26](briefs/2026-11-26.md)
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

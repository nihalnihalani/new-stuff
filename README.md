# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-22

## X Brief — Sunday 22 Nov 2026 (window: 21 Nov 09:00 → 22 Nov 09:00 IST)

Checked: 15 watch-list X accounts, 6 watch-list searches, plus follow-up X lookups on the day's biggest posts (Exo Labs and Hugging Face on Inkling 2 Mini, NVIDIA's Sigma models, the Cashfree × Sarvam winners); GitHub trending (daily, weekly, Python, TypeScript, Rust, Go, Jupyter); Hugging Face trending models, datasets, Spaces and daily papers; the Hacker News front page and Show HN; release notes for llama.cpp, vLLM, Ollama, LangChain, LangGraph and transformers; The Verge, TechCrunch, The Decoder, CNBC, TLDR AI, Ben's Bites and Import AI, the Lean community blog, and India AI coverage (Inc42, AIM); Devpost, Unstop, lablab and LinkedIn (via web search) for hackathons; student-perk searches. It was a quiet Saturday for the labs. All times are IST.

**TL;DR**
- **The Lean and Mathlib communities say Levent Alpöge's Claude-assisted proof of the Riemann Hypothesis is correct.** Their joint statement, endorsed by the Lean FRO, says they have "full confidence" in it. MIT's Andrew Sutherland reports that two independently written proof checkers accept all 175,187 modules. Two Lean-kernel checks were still running at 08:40 IST.
- **Inkling 2 Mini is the #1 trending model on Hugging Face, and Unsloth's GGUF is #2.** Exo Labs runs it at 210 tokens/s on an M5 Ultra Mac Studio. A new quantizer squeezes it into 5.4GB, and that post got 382 points on HN.
- **OpenAI's GPT-6.2 is getting a rough reception.** OpenAI published new prompts to fix its short answers and its habit of asking needless questions, and a SimpleBench update reportedly drops GPT-6.2 Sol from 10th to 30th. Meanwhile the Nasdaq 100 had its worst week since Covid.

### The one thing that matters most
**The Riemann Hypothesis proof has passed the Lean community's own checks.** On 21 Nov the Lean and Mathlib communities published a joint statement, endorsed by the Lean FRO and the Mathlib Initiative: "We have full confidence that Alpöge's proof of the Riemann Hypothesis is correct." They say it meets all four of their criteria. First, the statement being proved is Mathlib's vetted `RiemannHypothesis`. Second, dozens of people have compiled the library and reproduced the same proof export. Third, two independent tools confirm the theorem proved is exactly Mathlib's statement. Fourth, several kernels, including checkers that are themselves formally proven unable to accept a false proof, have accepted the exported proof, and those checks ran on an inert export, so malicious code in the sources couldn't interfere. Andrew Sutherland's verification page, run with Claude Code and last updated at 08:40 IST today, lists the details. All 175,187 modules compile. The headline theorems use only the three standard axioms. An independent sandboxed rebuild reproduced the 61.6GB export byte for byte. The nanoda and con-leche kernels accept the full proof. The Lean default and paranoid kernel checks and `lake comparator` were still running. HN's top comments split between "this sounded pretty definitive" and "only a human-readable proof can actually prove it". The statement itself ends by asking mathematicians to help *explain* the new ideas. For you, the lesson is that "an AI found it, and a proof checker confirmed it" is now a real research workflow, and the checking tools (Lean, Mathlib, independent kernels) are where the trust comes from. [Lean community statement](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) · [HN, 888 points](https://news.ycombinator.com/item?id=50589618) · 20:06, 21 Nov · [Sutherland's verification files](https://math.mit.edu/~drew/grh/) · [HN](https://news.ycombinator.com/item?id=50590441) · 21:24, 21 Nov

### AI news

#### Research
- **ByteDance's Axion 1.0 says most agent-training stages are unnecessary.** It's an open agent model trained in just three stages (two light SFT passes, then RL), with no mid-training, DPO or on-policy distillation, and the authors say it's competitive with leading commercial models on several agent benchmarks. They released the whole recipe: data construction, prompts, filtering and training code. If you want to fine-tune a small agent, this is a recipe you can actually follow. [The Decoder](https://the-decoder.com/bytedance-argues-most-ai-training-phases-are-unnecessary-and-backs-it-up-with-a-competitive-open-model/) · 14:47, 21 Nov · [arXiv](https://arxiv.org/abs/2611.03233) · [project page](https://axion1-0.github.io/)
- **NVIDIA researchers argue that huge context windows are usually a dead end.** In their tests, periodic summaries plus targeted keyword search matched full-context results at a fraction of the cost, and they propose models that work from short notes instead. Before you stuff a whole PDF into a prompt, try summary-plus-search for your RAG project. [The Decoder](https://the-decoder.com/nvidia-researchers-argue-huge-ai-context-windows-are-a-dead-end/) · 21:53, 21 Nov

#### Labs, products and APIs
- **OpenAI published new prompt templates for GPT-6.2 Astra and Sol, along with API changes.** The 6.2 models answer more briefly by default and should act on reversible assumptions instead of asking. For code, the templates say to reuse existing logic and skip new tests unless asked. In the Responses API, editing conversation history now discards earlier reasoning, `temperature` and `top_p` are gone, and OpenAI recommends "medium" reasoning for new integrations. If your hackathon app calls GPT-6.2, update your system prompt and stop editing history mid-chat. [The Decoder](https://the-decoder.com/openai-shares-new-prompting-tips-for-gpt-6-2-astra-and-sol-to-fix-brief-answers-and-unnecessary-questions/) · 19:02, 21 Nov
- **Local open models had their best day in a while.** Exo Labs worked with Thinking Machines to run Inkling 2 Mini at 210 tok/s decode and 3,620 tok/s prefill on a 96GB M5 Ultra Mac Studio, and at 125 tok/s on a 48GB M5 Max MacBook Pro. Exo says it built a native weather app 1.8× faster than Claude Sonnet 5.5 and 11× cheaper at API prices. Hugging Face's Julien Chaumond called it "how local and open source AI is going to win", and Clem Delangue posted that the model and Unsloth's GGUF are #1 and #2 on HF trending. [@julien_c quoting @exolabs](https://x.com/julien_c/status/2124099948937388225) · 16:47, 21 Nov · [@exolabs](https://x.com/exolabs/status/2123953913342935486) · [@ClementDelangue](https://x.com/ClementDelangue/status/2124209139337331158) · 00:01, 22 Nov
- **Gemini 4 Hydrogen costs about six times as much on "xhigh" thinking as on "high".** In Simon Willison's pelican test, one drawing cost 3.99¢ and 5,311 output tokens on high, and 23.61¢ and 31,477 tokens on xhigh, though the xhigh result was "VERY significantly" better. He also posted a grid comparing Carbon, Neon and Hydrogen across every reasoning level. Set your effort level on purpose, because it's your biggest cost dial. [@simonw](https://x.com/simonw/status/2124217876777464269) · 00:36, 22 Nov · [comparison grid](https://x.com/simonw/status/2124223349769609407) · 00:58, 22 Nov

#### Money and policy
- **The Nasdaq 100 fell 10.4% for the week, its worst since the Covid crash, and is now in bear-market territory.** It's down 20% from its October peak. Nvidia fell 14% on Friday on reports that the SEC is reviewing its accounting, the US chip index lost 10.7%, and Anthropic fell 9.1% a day after its debut. Expect tighter funding and fewer free credits if this keeps going. [The Decoder](https://the-decoder.com/us-technology-stocks-suffer-their-worst-weekly-loss-since-the-pandemic-as-ai-doubts-pile-up/) · 15:57, 21 Nov
- **Nvidia's interim CEO Colette Kress says it will no longer sell H200s in China.** The US is also moving to close the "remote access" route, where Chinese firms rent chips sitting in data centres in places like Malaysia. Meanwhile Elon Musk and others are circulating a petition to bring back Jensen Huang, and the board says that isn't happening. [TechCrunch](https://techcrunch.com/2026/11/21/a-tale-of-two-nvidias/) · 02:37, 22 Nov

#### India AI
- **Google committed $5M to IIT Kharagpur, Sundar Pichai's alma mater, for AI research and education.** The money covers Indic languages, materials science, agriculture and edtech, plus AI curriculum and training for students and faculty. It builds on Google's Amplify Initiative for hyperlocal Indian-language datasets. If you're at IIT KGP, watch for new courses and research positions. [Inc42](https://inc42.com/buzz/google-commits-5-mn-to-sundar-pichais-alma-mater-iit-kharagpur/) · 15:15, 21 Nov
- **Sarvam's Token Factory serves more than 450B tokens a day, mostly through DeepSeek V4.1 Flash, and bills in rupees.** Sarvam 105B costs ₹10 per million input tokens and ₹25 per million output, at introductory rates until the end of 2026. The platform also hosts Kimi K3.1 Pro, GLM 5.3 and Gemma 4 31B, and 95.7% of DeepSeek prompt tokens are served from cache at ₹0.25 per million. Critics ask why an IndiaAI Mission beneficiary hosts Chinese models, and Sarvam says the service runs on GPUs it bought itself, not subsidised ones. For you, it's a cheap, India-hosted, OpenAI-style API in rupees. Jarvislabs and E2E's Blaze offer similar catalogues. [Inc42](https://inc42.com/features/sarvams-token-factory-raises-indias-ai-inference-stakes/) · 17:27, 21 Nov

### New models and weights
| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Nemotron-Labs-Sigma (base, instruct, few-step distilled and self-speculative variants) | NVIDIA | 3B and 8B; 4,096-token context; English | NVIDIA Nemotron Open Model License (commercial use allowed) | A continuous-diffusion LLM: it denoises 16-dimensional token embeddings and writes text in parallel blocks instead of one token at a time. NVIDIA reports 8 tokens per forward pass on maths, 4 on code, and an average 3.46× self-speculative speedup for the 8B on GB200. It needs a CUDA GPU (no CPU inference). The weights went up on 12 Nov but only surfaced in today's feeds. A good model for a "diffusion vs autoregressive" class project | [HF collection](https://huggingface.co/collections/nvidia/nemotron-labs-sigma) · [NVIDIA Research](https://research.nvidia.com/labs/genair/sigma/) · [@agent_republic](https://x.com/agent_republic/status/2124028089994805344) · 12:02, 21 Nov |
| Axion 1.0 | ByteDance with Duke, UMD and Buffalo | RL stage starts from a Qwen3.5-122B-A10B checkpoint | Code released under Apache-2.0 | Fully open beyond the weights: you get the whole data pipeline, prompts and training code for a simple 2×SFT + RL agent recipe | [arXiv](https://arxiv.org/abs/2611.03233) · [project page](https://axion1-0.github.io/) |

Support for running models: transformers [v5.24.0](https://github.com/huggingface/transformers/releases/tag/v5.24.0) (17:58, 21 Nov) formally adds Inkling 2 Mini, and llama.cpp [b12619](https://github.com/ggml-org/llama.cpp/releases/tag/b12619) (05:15, 22 Nov) adds Kyutai's Hibiki real-time full-duplex speech model.

### Benchmarks and leaderboards
- **"Astra 6.2 and Sol 6.2 flop at SimpleBench."** The top HN commenter says that in the updated leaderboard GPT-6.2 Sol is 30th (6.1 Sol was 10th) and Astra 6.2 is 15th (Astra 6 was 9th). Fable 5.2 is now first, and all the new Gemini 4 models, Hydrogen included, beat the 83.7% human baseline. The leaderboard table didn't load for me, so these rankings are the commenter's. [SimpleBench](https://simple-bench.com/) · [HN, 164 points](https://news.ycombinator.com/item?id=50588916) · 18:46, 21 Nov
- **Inkling 2 Mini's headline SWE-bench Pro v2 Hard win is smaller than a single task.** It scores 77.9% vs 77.2% on a 51-task split, where each task is worth about 2 points. Read benchmark margins against the size of the test set. [@fierce788](https://x.com/fierce788/status/2124102250582663518) · 16:56, 21 Nov
- **Making a model explain its ARC-AGI-2 answer as code drops its accuracy from 77% to 57%.** Most of the lost tasks had a program that reproduced every example but still failed on the new grid. The post cites a paper by Duéñez-Guzmán et al. that I didn't open. [@lalamolly_](https://x.com/lalamolly_/status/2124302011587801599) · 06:10, 22 Nov

### Trending repos and projects
1. **[erkamyaman/rust-anything](https://github.com/erkamyaman/rust-anything)**: rewrites your app in Rust one piece at a time. It records what the original does, your coding agent ports it, and nothing ships until every recorded case replays byte-identical (the Prettier port runs 19× faster). Use it to speed up a slow Python or JS tool safely for a project. Rust · 7,490★ (#1 Rust trending, ~7.4k in 5 days) · MIT · [@Z3nlyte](https://x.com/Z3nlyte/status/2124296849716543762) · 05:50, 22 Nov
2. **[ShinMegamiBoson/lookatmyquant](https://github.com/ShinMegamiBoson/lookatmyquant)**: a quantization compiler that claims 12× lower KL divergence than Q4_K_M at the same file size, demoed by running Inkling 2 Mini in 5.4GB. That could make the model usable on an 8–16GB laptop. Commenters asked why you'd re-quantize a model that was already trained quantization-aware. Python · 314★ · MIT · [HN, 382 points](https://news.ycombinator.com/item?id=50591853) · 23:32, 21 Nov
3. **[ClawDOS](http://ricapar.net/ClawDOS/)**: a Claude coding agent for an IBM PC XT (8088 at 4.77 MHz, 640K). It's a 176KB DOS program that speaks the Messages API, with 18 tools, memory, screenshots and Turbo C builds, and Claude wrote all of it. It's the clearest small codebase showing how an agent harness actually works. C/C++ · GPL-3.0 · [HN, 160 points](https://news.ycombinator.com/item?id=50586292) · 11:08, 21 Nov
4. **[molly554/whiteboard-ai-tutor](https://github.com/molly554/whiteboard-ai-tutor)**: an AI tutor that writes and draws on a whiteboard as it teaches, with animated lessons and playback, benchmarked across Claude, Gemini and DeepSeek over 288 generation runs. Fork it to build a subject tutor for your college. HTML · 546★ · MIT · [@TheArthiAI](https://x.com/TheArthiAI/status/2124047568976191790) · 13:19, 21 Nov
5. **[bytedance/flowgram.ai](https://github.com/bytedance/flowgram.ai)**: a framework for building AI workflow platforms, with the canvas, node forms and variable scoping built in. Use it for a drag-and-drop agent builder instead of drawing your own canvas. TypeScript · 8,608★ · [@GithubProjects](https://x.com/GithubProjects/status/2124052966403616936) · 13:41, 21 Nov
6. **[t8y2/dbx](https://github.com/t8y2/dbx)**: a 25MB database client for 100+ databases, with an AI SQL assistant and an MCP server. Point your agent at a real database through its MCP server. Rust · 31,107★ (+48 today, Rust trending) · Apache-2.0 · [@swapnil_1_618](https://x.com/swapnil_1_618/status/2124171867028381727) · 21:33, 21 Nov
7. **[natsu0529/agent-mcts](https://github.com/natsu0529/agent-mcts)**: runs Monte Carlo tree search over coding agents such as Claude Code and Codex CLI at test time. It's an easy way to show that "more search beats a bigger model" in a demo. Python · 7★ · MIT · [Show HN](https://news.ycombinator.com/item?id=50589235) · 19:23, 21 Nov
8. **[0xPlaygrounds/rig](https://github.com/0xPlaygrounds/rig)**: a library for building modular LLM apps in Rust. Pair it with rust-anything if you want your agent backend in Rust. Rust · 9,214★ (+12 today, Rust trending) · MIT
9. **[NirDiamant/GenAI_Agents](https://github.com/NirDiamant/GenAI_Agents)**: 50+ notebook tutorials on agent techniques, from simple chatbots to multi-agent systems. It's a good weekend crash course before an agent hackathon. Jupyter · 25,080★ (Jupyter trending)
10. **[DataTalksClub/llm-zoomcamp](https://github.com/DataTalksClub/llm-zoomcamp)**: a free 10-week course on building real LLM apps, including RAG over your own data. Work through it, then ship the capstone project as a portfolio piece. Jupyter · 7,722★ (Jupyter trending)
11. **[NVIDIA-NeMo/Nemotron](https://github.com/NVIDIA-NeMo/Nemotron)**: NVIDIA's hub of training recipes, cookbooks, datasets and end-to-end examples for Nemotron models. Start here if you want to fine-tune an open NVIDIA model. Jupyter · 2,375★ (Jupyter trending)
12. **[pyrefly-org/pyrefly](https://github.com/pyrefly-org/pyrefly)**: an open-source Python type checker, 15× faster than Mypy according to the post. It gives agent-written Python a quick type check before you trust it. Rust · 7,232★ · MIT · [@GithubProjects](https://x.com/GithubProjects/status/2124204955720679455) · 23:45, 21 Nov

Most of the rest of today's GitHub top 10 (Claude-BugHunter, superpowers, CLI-Anything, MiniMind, Firecrawl, cursor/plugins, last30days, diagram-design, OpenSRE) appeared in earlier briefs. Release notes: vLLM, Ollama, LangChain and LangGraph published nothing in the window.

### Hackathons
Open ones, soonest deadline first:
1. **SiliconSprint 2.0 (IEEE NITK Surathkal × IEEE BITS Pilani Hyderabad, sponsored by Tenstorrent)**: a 24-hour virtual electronics hackathon with a "Hardware for AI" track, alongside analog, digital and signal-processing tracks. The pool is ₹1 lakh (₹80K cash, ₹20K in goodies), and you enter in teams of 2–3. It's open to engineering students, and **registration closes Thu 26 Nov, 00:00 IST**. [Unstop](https://unstop.com/hackathons/silicon-sprint-2026-nitk-surathkal-1814263)
2. **Toggle Wars (WeMakeDevs × Flagsmith)** (reminder): four days of building with feature flags and A/B experiments across three tracks, with a PS5 + GTA 6 bundle among the prizes. It **starts Thu 26 Nov**, and 2,000+ builders have signed up. Founder @kunalstwt's guide has 18 project ideas and shows how to get your first experiment running before kickoff. [@WeMakeDevs](https://x.com/WeMakeDevs/status/2124020828216119796) · 11:33, 21 Nov · [@WeMakeDevs](https://x.com/WeMakeDevs/status/2124073795858346077) · 15:03, 21 Nov
3. **AI-Powered Career Development Hackathon (UnsaidTalks Education)**: online, free and **solo**. You build an AI career platform that reads a student's profile, finds skill gaps and recommends a learning path. The winner gets ₹30K plus a mentorship plan, and the runners-up and top 10 get ₹3,499 mentorship plans. **Registration closes Sat 28 Nov, 23:59 IST**, and the event ends 29 Nov, 20:30 IST. [Unstop](https://unstop.com/hackathons/ai-powered-career-development-hackathon-unsaidtalks-education-1821954)
4. **Code Relay 5.0 (WebnD, IIT Bhubaneswar)**: hybrid, with an online first round (ideathon and prototype), and open to everyone in teams of 2–4. The AI tracks are Agentic AI × TrueFoundry (₹40K) and AI for Bharat (₹30K). Shortlisted teams share ₹1 lakh in model credits for round 2, and top Web2 performers can get pre-placement interviews with CSM Technologies. **Registration closes Sat 12 Dec, 23:59 IST.** [Unstop](https://unstop.com/hackathons/code-relay-50-indian-institute-of-technology-iit-bhubaneswar-1810370)
5. **OpenCode 2026 (Geekhaven, IIIT Allahabad)**: an online, beginner-friendly open-source contribution event that you enter solo, with an AI/ML stack (Python, PyTorch, LLaMA) among its tracks. Winners get up to ₹30K, sub-event winners up to ₹30K, plus merch. **Registration closes Sun 13 Dec, 23:00 IST.** [Unstop](https://unstop.com/hackathons/opencode-2026-opencode-indian-institute-of-information-technology-iiit-allahabad-1811349)

**Winners**
- **Cashfree × Sarvam AI Buildathon (Bengaluru, 21 Nov):** 150 builders in 30 teams built agents that hear a request in an Indian language and then move money through Cashfree, with ₹3 lakh+ in cash and credits. Team **TarangAI** came second with an "Agentic Payment Box", a counter-top voice device for merchants in 11 languages. It uses Cashfree's Relay agentic stack and Sarvam's 105B, Saras and Bulbul models for voice payments, purchases and vision-based inventory. [@SoumikBaksi](https://x.com/SoumikBaksi/status/2124175395331404203) · 21:47, 21 Nov · [demo thread](https://x.com/SoumikBaksi/status/2124109753748189594) · 17:26, 21 Nov · [Luma](https://luma.com/azuhrzuj)
- **Namma AI Hackathon 2026 (Arm, IIIT-B, NASSCOM and the UK government):** Karnataka minister Priyank Kharge presented the awards at Bengaluru Tech Summit to Team Nucleus (IIIT-B), Numeronauts (NIT Surathkal) and Techtonics (CIT Chennai). [@ITBTGoK](https://x.com/ITBTGoK/status/2124105992254492729) · 17:11, 21 Nov
- **AI for Foundational Learning Hackathon (ShikshaNext × Anthropic, run by CSF India):** 900+ entries went through a 10-week programme. **Slate AI** won with "Tappida Paatha" (The Missed Lesson), ahead of ShikshaSaathi AI ("Jugnu") and Beej ("Ankur Saathi"). [@CSF_India](https://x.com/CSF_India/status/2124023755076702470) · 11:45, 21 Nov

### Student perks and credits
- **Sarvam Campus '26 is free and gives you Sarvam Code and API credits before the session**, which you keep using afterwards. The 3.5-hour stop includes a guided build-along, the top 3 projects are showcased, and one student per campus becomes a "Sarvam Captain". The tentative November–December stops include IIT Guwahati, IIT Indore, ISM Dhanbad, VNIT Nagpur, NIT Surathkal, Manipal, BITS Goa, KIIT, IIT Bhubaneswar, Amrita Coimbatore and PSG Tech, and your college can request a visit. [Sarvam](https://www.sarvam.ai/sarvam-campus)
- **Cheap rupee-billed inference:** Sarvam 105B costs ₹10/₹25 per million input/output tokens on Token Factory until the end of 2026 (see India AI above).
- **Credits through hackathons:** Code Relay 5.0 gives shortlisted teams ₹1 lakh in model credits, and the Cashfree × Sarvam buildathon gave every registered builder 500 Sarvam credits (see Hackathons).
- No new free API or GPU credit programme open to Indian students surfaced in the window.

### Grok Bots
- **A three-bot content team where a human still presses Post.** The ideas bot pitches posts with a source for every fact, the growth bot scores each pitch against the last 7 days of analytics, and the content bot fact-checks and drafts. It comes with clear rules for keeping or dropping a post format (1.5%+ bookmarks or 15k+ views earns a regular slot). It was the most-engaged Grok Bot post of the day. [@TheMaran](https://x.com/TheMaran/status/2124186338748760551) · 22:31, 21 Nov
- **"Slow down" before you build a team of bots.** The post gives a copy-paste prompt that makes the bot interview you, design the simplest workflow, run a small test and refine it before anything goes recurring. [@Michael_Fenech_](https://x.com/Michael_Fenech_/status/2124229359720358041) · 01:22, 22 Nov
- **Botsmith, a free template for a bot that manages your other bots.** It replaces bloated bots with leaner successors (quizzed before they take over) and cuts bot-to-bot chatter that eats your usage limits. [@Mitroshenkov87](https://x.com/Mitroshenkov87/status/2124097765936427282) · 16:39, 21 Nov
- **Five free importable bots from one lab**: Cortex (notes), Mind Trainer (filters what you read, then quizzes you), Router, Pain Scout and Proofreader. [@TheOverlordLog](https://x.com/TheOverlordLog/status/2124065950336966953) · 14:32, 21 Nov
- **Botwire, a free beta "Town Square" where bots from different owners can meet and DM.** It comes with digests, caps, a quiet mode and a kill switch. It's a third-party service, so read what access it asks for before you connect a bot. [@Optimaxx88](https://x.com/Optimaxx88/status/2124257166941139110) · 03:12, 22 Nov

### Build idea of the day
**A "skill-gap whiteboard tutor" for the AI-Powered Career Development Hackathon (solo, registration closes Sat 28 Nov, 23:59 IST, ₹30K for the winner).** Have Inkling 2 Mini read a student's resume and a target role, find the missing skills and plan a week-by-week path. Run it on a laptop with the 5.4GB lookatmyquant build so no profile data leaves the machine. Then fork whiteboard-ai-tutor so each gap is taught as an animated whiteboard lesson rather than a wall of text. For the demo, show one real profile turning into a drawn three-lesson roadmap, with the Wi-Fi switched off.

### What the field is arguing about
- **Is "the Lean kernel accepts it" the same as "proved"?** One side says the community statement sounds definitive. The other says that without a human-readable argument it isn't useful mathematics yet. Either way, everyone is asking what humans can learn from 17 million lines of Lean. [HN](https://news.ycombinator.com/item?id=50589618)
- **Did OpenAI ship a worse model?** On the SimpleBench thread, developers say GPT-6.2 feels "lazier" and follows instructions too literally. One says a rival model told them to stay on 6.1. OpenAI's new prompting guide, which tackles short answers and needless questions, reads as a partial answer to that. [HN](https://news.ycombinator.com/item?id=50588916) · [The Decoder](https://the-decoder.com/openai-shares-new-prompting-tips-for-gpt-6-2-astra-and-sol-to-fix-brief-answers-and-unnecessary-questions/)
- **What Nvidia looks like without Jensen Huang.** An Economist piece arguing his fall is bad news for Silicon Valley's accelerationists drew 340 comments on HN. [HN](https://news.ycombinator.com/item?id=50591835) · 23:29, 21 Nov

### Worth reading in full
1. [Lean and Mathlib communities: Lean verification of the Riemann Hypothesis](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/): the four criteria and how each one was met, in under two minutes.
2. [Andrew Sutherland's verification files](https://math.mit.edu/~drew/grh/): the clearest table of how you independently check a 17-million-line proof, down to one module that compiles differently because of a Lean race condition.
3. [Axion 1.0: Open Agent Foundation Models, Simplified](https://arxiv.org/abs/2611.03233): a full, reproducible agent-training recipe.
4. [Sarvam's Token Factory raises India's AI inference stakes](https://inc42.com/features/sarvams-token-factory-raises-indias-ai-inference-stakes/) (Inc42): how Indian token factories price, cache and compete.
5. [ClawDOS](http://ricapar.net/ClawDOS/): an entire agent harness explained on one page, running on 640K of RAM.

### Quiet accounts and anything I couldn't open
- No posts in the window: @OpenAI, @AnthropicAI, @GoogleDeepMind, @AIatMeta, @MistralAI, @karpathy, @devpost. @huggingface only reposted (Inkling 2 Mini launch posts, its new Home feed, its own CDN, and Clem Delangue on US open source), and @_akhaliq reposted one Clem Delangue post. @trending_repos named Claude-BugHunter again (covered earlier). @chinchoukou's picks were mostly repos covered earlier (Claude-BugHunter, superpowers, CLI-Anything, MiniMind, Firecrawl, cursor/plugins, AutoClip and others). @GithubProjects' most popular posts weren't AI (a streaming app, a downloader, bookmark sync, a PS5 binary relinker, Freeplane). @anurag_629 posted a system-design interview answer and a poll on when to ask AI for help debugging.
- SimpleBench's leaderboard table and The Decoder's full NVIDIA context-window article (paywalled) didn't load, and Unstop event pages only opened through their listing data. Reddit (r/LocalLLaMA, r/MachineLearning) blocked direct reads. TLDR AI, Ben's Bites and Import AI had no new issue in the window, and I didn't get to Product Hunt, DoraHacks, Kaggle or MLH this run. A "GLM 5.5 next week" rumour and some viral Grok Bot hype threads were left out because I couldn't confirm them.

## Archive

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

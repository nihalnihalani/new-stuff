# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-23

## X Brief — Monday 23 Nov 2026 (window: 22 Nov 09:00 → 23 Nov 09:00 IST)

Checked: 15 watch-list X accounts, 6 watch-list searches, plus follow-up X lookups on the day's biggest posts (Sarvam and Pratyush Kumar on Sarvam-105B-1711, Ant Ling's LingSante models, MemOS's MemT-1.0-Pro, two hackathon-winner posts); GitHub trending (daily, weekly, Python, TypeScript, Rust, Go, Jupyter); Hugging Face trending models, datasets, Spaces and daily papers; the Hacker News front page and Show HN; release notes for llama.cpp, vLLM, Ollama, LangChain, LangGraph and transformers; The Decoder, TechCrunch, The Verge, Ars Technica, VentureBeat, the OpenAI, Google, NVIDIA and Hugging Face blogs, TLDR AI, Ben's Bites, Import AI, Latent Space and The Rundown, and India AI coverage (Inc42, AIM, ET); Devpost, Unstop and LinkedIn (via web search) for hackathons; student-perk searches. Sunday was quiet for the big US labs, and India had the day's biggest release. All times are IST.

**TL;DR**
- **Sarvam open-sourced Sarvam-105B-1711 under Apache-2.0.** It's a "Flash-Lite"-class model that Sarvam says roughly matches Gemini 3.5 Flash-Lite's agent-benchmark average at under a fifth of the price, and it runs on a single 96GB workstation GPU. BF16 weights for fine-tuning and NeMo RL support are out too.
- **Open weights had a strong Sunday.** Ant Ling released two medical models (LingSante-3.1-flash, 560B, and LingSante-3.1-air-VL, 124B), both under MIT. MemOS and NVIDIA launched MemT-1.0-Pro, a 554B model with memory built in, and Baseten's bison-1 tops Artificial Analysis' Decision Index.
- **Safety and measurement were the other big story.** OpenAI's chief scientist proposed perplexity as a shared "speed limit" metric, and METR warned that AI is improving faster than it can be safety-tested. Dragos showed that some cheap inference resellers were stealing API keys from requests.

### The one thing that matters most
**India now has a competitive open model you can download, fine-tune and run on one GPU.** On 22 Nov Sarvam released Sarvam-105B-1711, a new checkpoint of its 105B model aimed at the "Flash-Lite" tier (support bots, voice agents, extraction). On Sarvam's own evals, the NVFP4 build averages 73.9 across instruction following, chat, tool calling and Indian languages at $0.15 per million tokens. That compares with 74.0 for Gemini 3.5 Flash-Lite at $0.85, 66.3 for GPT-6 Luna (high) at $0.20 and 73.0 for Gemma 4 31B at $0.54. One summary of Sarvam's numbers puts the gains over February's release at IFBench 32.5 → 82.5, Tau2 tool use 46.2 → 85.5 and Indic 30.1 → 79.1. The 65GB NVFP4 checkpoint is the one Sarvam serves in production, and it fits on a single 96GB RTX PRO 6000 Blackwell. Sarvam measured 197 tok/s peak with the network switched off. vLLM support is merged, and Sarvam has proposed a Triton kernel fix upstream so the FP8 KV cache works on that GPU. Co-founder Pratyush Kumar's same-day thread answers the week's criticism. He says IndiaAI Mission's ~40% GPU subsidy went to cloud providers and was used to train the original 105B. Token Factory, he says, runs on privately bought GPUs, and output costs ₹25 per million tokens. He also says "multiple other models across vision, speech, and edge" will ship in the next two weeks. For you, it's an Apache-2.0 model with strong Indian-language skills that you can fine-tune legally, plus a cheap rupee-billed API if you can't host it yourself. [@SarvamAI](https://x.com/SarvamAI/status/2124532170505273661) · 21:25, 22 Nov · [Sarvam blog](https://www.sarvam.ai/blogs/sarvam-105b-1711) · [weights](https://huggingface.co/sarvamai/sarvam-105b-1711) · [@pratykumar](https://x.com/pratykumar/status/2124530320200577082) · 21:17, 22 Nov · [@saiitoshii](https://x.com/saiitoshii/status/2124556099625853085) · 23:00, 22 Nov

### AI news

#### India AI
- **Inc42 lays out the risks behind India's "token factory" boom.** By default, Token Factory uses customer data to fine-tune Sarvam's models unless the client turns that off, and zero data retention is only on request. Sarvam's ₹0.25-per-million promotional rates expire at the end of 2026. Rivals include L&T's Vyoma.AI, E2E Networks (through Jarvislabs) and Utho Cloud, which plans to enter in 2027. If you're sending college or user data to any cheap API, switch off training on your data first. [Inc42](https://inc42.com/buzz/indias-inference-test-scaler-founders-new-ai-bet-more/) · 08:00, 23 Nov
- **The same Sarvam post claims a big lead in speech-to-text for Indian languages.** On 692 real dictations in 15 Indian languages, Sarvam Dictate needed 2.7% of characters corrected, against 12.2% for Gemini 3.5 Transcribe and 11.8% for AssemblyAI. It costs ₹0.5 a minute. That's a cheap voice front end for any Indic hackathon app. [Sarvam blog](https://www.sarvam.ai/blogs/sarvam-105b-1711)

#### Labs, products and APIs
- **OpenAI's chief scientist wants perplexity to be the industry's shared "speed limit".** In "Perplexity and Intelligence", Jakub Pachocki publishes OpenAI's internal pretraining loss: GPT-3.5 at ~0.99 and GPT-4 at ~0.91, and he says losses below 0.8 brought "transformative capabilities" in cybersecurity and maths. He proposes that labs agree not to train past a threshold until monitoring catches up, and Sam Altman called it "the most important thing OpenAI has published in a while". It's a clear lesson in why loss, not benchmarks, is what labs actually track. [TechCrunch](https://techcrunch.com/2026/11/22/openais-chief-scientist-has-thoughts-on-how-to-limit-ai-development/) · 02:44, 23 Nov · [OpenAI](https://openai.com/index/perplexity-and-intelligence)
- **Perplexity launched a Monitor API that watches the web for you.** Web monitors re-run a search on a schedule, and page monitors diff up to 10 pages, such as pricing pages or changelogs. You only get a webhook when a change clears relevance, credibility, novelty and timeliness checks. Schedules run from every 15 minutes to weekly. It saves you writing your own "alert me when X changes" scraper. [The Decoder](https://the-decoder.com/perplexitys-new-monitor-api-turns-web-search-from-a-one-off-query-into-a-nonstop-watchdog/) · 19:50, 22 Nov
- **GPT-6.2 now talks very differently from Claude.** Artificial Analysis found that Astra's average answer fell from 352 to 210 words and its headings per answer from 1.99 to 0.11. Its "Admits Uncertainty" score dropped from 96 to 24. On the Transparency Index, Claude scores 81–90 against 41 for Astra and 57 for Sol. If your app needs hedged, careful answers, test the model you pick on that, not just on accuracy. [The Decoder](https://the-decoder.com/gpt-6-2-astra-and-sol-get-to-the-point-faster-but-score-lower-on-transparency-than-claude/) · 15:11, 22 Nov

#### Research and safety
- **METR warns that AI is improving faster than experts can test whether it's safe.** On well-defined coding tasks, models already beat experienced professionals most of the time. The length of task they can handle doubles every 3.6 months, and a naive extrapolation reaches 50% success on 200-hour tasks by July 2027. METR also says easy-to-run tests probably overstate real-world performance. [The Decoder](https://the-decoder.com/ai-is-getting-better-faster-than-experts-can-reliably-test-whether-new-systems-are-safe-metr-warns/) · 18:30, 22 Nov
- **Coding agents ace benchmarks but finish fewer than one in ten tasks in a simulated office.** In an experiment that dropped them into a fake software company, with colleagues, project boards and chat history, even Claude Opus 5.5 and GPT-6 Astra fully completed fewer than 10% of tasks. The rest of the article is paywalled. The takeaway is that your agent demo needs real context-handling, not just a high SWE-bench score. [The Decoder](https://the-decoder.com/ai-coding-agents-ace-isolated-tests-but-complete-fewer-than-one-in-ten-tasks-in-a-simulated-workplace/) · 20:45, 22 Nov
- **The other Riemann Hypothesis proof is now being checked in Lean.** Mathematicians are formalizing Alessandro Masullo's 940-page human proof in Lean. One contributor says it's "way too early" to judge the hundreds of errata. Another commenter notes that Brian Conrad says the manuscript needs "major revision". John Baez's explainer sketches Masullo's trace-formula strategy. [Progress map, HN 173 points](https://news.ycombinator.com/item?id=50605045) · 04:42, 23 Nov · [Baez explainer, HN](https://news.ycombinator.com/item?id=50598441) · 16:29, 22 Nov

#### Money and security
- **Cheap AI inference resellers were caught stealing API keys.** Dragos sent about 2 million requests containing fake credentials to AI providers. It found at least three compromised providers, one of which harvested hundreds of AWS keys, and "zero data retention" promises were often ignored. OpenRouter removed three providers and revoked ZDR approval for 125 endpoints. Never put real keys or secrets in prompts sent through routers. [The Decoder](https://the-decoder.com/security-researchers-show-how-cheap-ai-inference-providers-steal-keys-and-snoop-on-users/) · 17:37, 22 Nov
- **Anthropic's early backers are sitting on huge paper gains.** TechCrunch reports that the IPO raised $81.3B at a fully diluted ~$1.5T valuation. Notable Capital is up roughly 15× on its Series E bet, made after its research found developers were picking Claude 70% of the time. GIC put in more than $4.5B across three rounds. Developer adoption was the signal investors bet on, so what student builders pick matters. [TechCrunch](https://techcrunch.com/2026/11/22/how-notable-capital-gic-and-baillie-gifford-bet-big-on-anthropic-before-its-ipo/) · 06:55, 23 Nov

### New models and weights
| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Sarvam-105B-1711 (NVFP4 and BF16) | Sarvam | 105B MoE; NVFP4 build is 65GB | Apache-2.0 | Strong Indian-language, tool-calling and chat model. It runs on one 96GB RTX PRO 6000 with vLLM, and the BF16 weights plus NeMo RL support let you fine-tune it | [HF](https://huggingface.co/sarvamai/sarvam-105b-1711) · [BF16](https://huggingface.co/sarvamai/sarvam-105b-1711-bf16) |
| LingSante-3.1-flash | Ant Ling (inclusionAI) | 560B total, 25B active, 1M context | MIT | Medical MoE that Ant Ling says leads HealthBench Professional (65.72), ahead of GPT-6 Astra, Opus 5.5 and Gemini 4 Argon. It's for research only, not diagnosis. All 560B parameters must sit in memory, so it won't run on a laptop | [HF](https://huggingface.co/inclusionAI/LingSante-3.1-flash) · [@AntLingAGI](https://x.com/AntLingAGI/status/2124523916819648945) · 20:52, 22 Nov |
| LingSante-3.1-air-VL | Ant Ling (inclusionAI) | 124B total, 5.5B active | MIT | Reads medical images and writes reports, with search and tool use. Ant Ling reports wins on MIMIC-CXR and dermatology/report benchmarks | [HF](https://huggingface.co/inclusionAI/LingSante-3.1-air-VL) · [@AntLingAGI](https://x.com/AntLingAGI/status/2124555085640610194) · 22:56, 22 Nov |
| MemT-1.0-Pro | MemOS (MemTensor) with NVIDIA | 554B (59B active), built on Nemotron 3 Ultra | OpenMDW-1.1 | Memory is built into the model, so it reuses past interactions without re-sending the history. MemOS says that uses about 66× less storage than a KV cache at 128K. The Nano sibling (36B, 3B active) is the one you might actually run | [HF](https://huggingface.co/MemTensor/MemT-1.0-Pro) · [@MemOS_dev](https://x.com/MemOS_dev/status/2124623963087126562) · 03:30, 23 Nov |
| bison-1 | Baseten (Base Labs) | 31B, post-trained from Gemma 4 31B | MIT and Apache-2.0 | A "decision model" that returns a calibrated probability for each option instead of generating text. Useful for routing, guardrails and classification. Uploaded 20 Nov, surfaced in today's feeds | [HF](https://huggingface.co/baselabs/bison-1) |
| Sage S2.1 Flash | Shanghai AI Lab (InternLM) | ~321B (safetensors total) | MIT | Scientific multimodal model that reads molecules, crystals and proteins. Its card claims first place on MLE-bench Lite (90.3). Trending on HF since 15 Nov | [HF](https://huggingface.co/internlm/Sage-S2.1-Flash) |
| LongCat-Video-Avatar-1.6 | Meituan | not stated on card | MIT | Audio-driven talking-avatar video with more natural lip sync, and videos over 10 minutes. Trending on HF | [HF](https://huggingface.co/meituan-longcat/LongCat-Video-Avatar-1.6) |

Support for running models: llama.cpp [b12641](https://github.com/ggml-org/llama.cpp/releases/tag/b12641) (07:04, 23 Nov) fixes Inkling 2 tokenization (`ignore_merges`). vLLM, Ollama, LangChain, LangGraph and transformers published no releases in the window.

### Benchmarks and leaderboards
- **bison-1 is #1 of 19 on Artificial Analysis' Decision Index v2.1, scoring 76**, ahead of d1.2-ultra (75) and mammoth-1 (71). It's also the best-calibrated model there, with a Brier score of 0.14. [Model card](https://huggingface.co/baselabs/bison-1) · [@saiitoshii](https://x.com/saiitoshii/status/2124464940815626262) · 16:58, 22 Nov
- **Sarvam-105B-1711's other numbers are mixed (all Sarvam's own evals).** It's second to Gemini 3.5 Flash-Lite on GDPval-S (66.9 vs 73.0), close behind on BrowseComp (41.4 vs 42.9), and scores 89.7 on AIME 26 without tools. Sarvam notes that Qwen3.8 27B ran out of output budget in about half its rollouts, which flatters the comparison. [Sarvam blog](https://www.sarvam.ai/blogs/sarvam-105b-1711)
- **One post says Inkling 2 Mini is now the top open-weights model on Parallel's benchmark, with only 3.4B active parameters.** I didn't open the leaderboard itself. [@0xBakeer](https://x.com/0xBakeer/status/2124503919581671777) · 19:33, 22 Nov
- **There's a new personality benchmark (AA-PersonalityBench)**: 900 questions with no system prompt, scored by a panel of three AI judges. It measures communication style, not correctness (see GPT-6.2 above).

### Trending repos and projects
1. **[EL4CTEO/fast-anything](https://github.com/EL4CTEO/fast-anything)**: profiles your Python, Node or Ruby app, has your coding agent port only the hot 5% to Rust, then proves it behaves the same. It's the lighter cousin of yesterday's rust-anything, so try it on a slow script in your project. Rust · 2,056★ (created 21 Nov; ~780/day per the post) · MIT · [@TheArthiAI](https://x.com/TheArthiAI/status/2124477662882373816) · 17:48, 22 Nov
2. **[nexu-io/openmotion](https://github.com/nexu-io/openmotion)**: turns a reference video into editable motion graphics in your brand kit and exports MP4s for Shorts, Reels and TikTok. Use it to make a polished demo video for a hackathon submission. TypeScript · 15,411★ · Apache-2.0 · [@GithubProjects](https://x.com/GithubProjects/status/2124449566636511607) · 15:57, 22 Nov
3. **[earthtojake/text-to-cad](https://github.com/earthtojake/text-to-cad)**: a plugin that turns your coding agent into a CAD designer. Describe a part and get STEP, STL or 3MF files back. It's handy for the IIT Bombay Physical AI hackathon below. Python · 27,173★ · MIT · [@SDamien19832](https://x.com/SDamien19832/status/2124486725447929860) · 18:24, 22 Nov
4. **[Forward-Future/scarlet](https://github.com/Forward-Future/scarlet)**: an AI video editor where Claude Code or Codex edits the cut list and only the seconds around each cut re-render. It's a good design pattern: the agent edits a plan, never the pixels. TypeScript · 615★ · MIT · [@LLMpsycho](https://x.com/LLMpsycho/status/2124595456256954507) · 01:36, 23 Nov
5. **[gulivan/worker755](https://github.com/gulivan/worker755)**: a browser game where an AI manager thinks *you* are its subagent. It's a fun way to feel what your agent's prompts look like from the other side. TypeScript · 141★ · MIT · [Show HN, 282 points](https://news.ycombinator.com/item?id=50599762) · 19:26, 22 Nov
6. **[mccorvie/riemann-masullo](https://github.com/mccorvie/riemann-masullo)**: a Lean 4 formalization of Masullo's Riemann Hypothesis manuscript, and the maintainers invite people to point their agents at open issues. It's a real formal-maths project you can contribute to. Lean · 62★ · Apache-2.0 · [HN](https://news.ycombinator.com/item?id=50605045)
7. **[mjwsolo/localcode](https://github.com/mjwsolo/localcode)**: agentic coding with local models on a Mac, set up with one command. Pair it with an Inkling 2 Mini GGUF for an offline coding agent. C++ · 61★ · Apache-2.0 · [HN](https://news.ycombinator.com/item?id=50604540) · 03:48, 23 Nov
8. **[Kanaries/graphic-walker](https://github.com/Kanaries/graphic-walker)**: an open-source Tableau alternative that turns CSV or JSON into drag-and-drop charts. Embed it as the dashboard for a data-heavy hackathon app. TypeScript · 3,341★ · Apache-2.0 · [@GithubProjects](https://x.com/GithubProjects/status/2124381115544998351) · 11:25, 22 Nov
9. **[appwrite/appwrite](https://github.com/appwrite/appwrite)**: an open-source backend ("cloud for agents & devs") with auth, databases, storage, functions and realtime. It's a quick self-hostable backend for an agent app. TypeScript · 58,598★ (+121 today, TypeScript trending) · BSD-3-Clause
10. **[pytorch/torchtitan](https://github.com/pytorch/torchtitan)**: PyTorch's native platform for training generative models. Read it to learn how large-scale pretraining is actually wired up. Python · 5,952★ (+10 today, Python trending)
11. **[twentyhq/twenty](https://github.com/twentyhq/twenty)**: an open Salesforce alternative "designed for AI". A good base if you're building a sales or CRM agent. TypeScript · 61,341★ (+43 today, TypeScript trending)
12. **[buberlo/aaf-gate](https://github.com/buberlo/aaf-gate)**: a deterministic policy gate, kill switch, call limits and tamper-evident audit log for existing agent runtimes, using only the Python standard library. It's tiny and brand new, but it's a clean pattern for putting guardrails on an agent. Python · 2★ · Apache-2.0 · [Show HN](https://news.ycombinator.com/item?id=50604524) · 03:47, 23 Nov

Most of today's GitHub top 10 (Claude-BugHunter, superpowers, CLI-Anything, MiniMind, Firecrawl, cursor/plugins, diagram-design, last30days, stitch-skills, OpenSRE, AutoClip) and the weekly list appeared in earlier briefs.

### Hackathons
Open ones, soonest deadline first:
1. **Rajasthan Police Hackathon 2026 (R4C, Rajasthan Police)**: real problem statements in cyber fraud, digital forensics, OSINT and AI/ML. Teams of 1–4 submit an action plan, and the top 25 go to a 24-hour offline finale at Rajasthan Police Academy, Jaipur. Prizes are ₹50K/₹35K/₹15K per use case across 5 use cases (₹5 lakh total). It's open to students and developers, and **registration closes Tue 24 Nov, 23:59 IST**. [Unstop](https://unstop.com/hackathons/rajasthan-police-hackathon-2026-rajasthan-police-rajasathana-palsa-1818639)
2. **Festive Hacks (WeMakeDevs)** (reminder): build fixes for festive-season problems and demo them at WeAreDevelopers Conference India. 1st place gets a fully sponsored team trip to Berlin for WeAreDevelopers World Congress 2027, and 2nd gets ₹1,00,000. It starts in 3 days, as of the post. [@WeMakeDevs](https://x.com/WeMakeDevs/status/2124388381283295361) · 11:53, 22 Nov
3. **IIT Bombay Physical AI Hackathon (TiH, E-Summit'26)**: go from simulation to real robots and IoT devices. It's for undergraduates and early-stage startups in teams of 2–5, with a ₹1.5 lakh pool. **The online Round 1 submission is due Thu 26 Nov, 23:59 IST**, and the finale runs 12–13 Dec at IIT Bombay. [Unstop](https://unstop.com/hackathons/iit-bombay-physical-ai-hackathon-iit-bombay-1822209)
4. **Toggle Wars (WeMakeDevs × Flagsmith)** (reminder): four days of building with feature flags and experiments, **starting Thu 26 Nov**. It has 3,000 builders and $5,000 in prizes, including $2,000 for "Test Something Real" and $1,000 for "AI Agents + Feature Flags". A welcome livestream with @kunalstwt and the Flagsmith team is set for today. [@WeMakeDevs](https://x.com/WeMakeDevs/status/2124437266592620999) · 15:08, 22 Nov · [livestream post](https://x.com/WeMakeDevs/status/2124480856094052488) · 18:01, 22 Nov
5. **Where the Wild Features Are (literacy speech modeling)**: predict kindergarteners' reading scores from screening audio using MIT and Florida State speech data. There's $50,000 in prizes ($20K for first), it's judged on write-ups as well as the leaderboard, and per @anurag_629 India can apply. **Signups close Wed 20 Jan 2027, 05:29 IST.** [Competition page](https://platform.k12-ai-infrastructure.org/competitions/4/literacy-speech-modeling/) · [@anurag_629](https://x.com/anurag_629/status/2124696690749784121) · 08:19, 23 Nov

**Winners**
- **Google DeepMind NYC Hackathon (100+ teams, 1,200 people):** Akhil Mattaparthi's team won 1st place and Best Multi-Model ($12.5K). They built a tool that lets game developers create opponents that learn your habits, such as always dodging left. Different Gemini models spot patterns, test new strategies for fairness and explain each change. [@AkhilMatta29342](https://x.com/AkhilMatta29342/status/2124604827996938285) · 02:13, 23 Nov
- **Singapore–India Hackathon 2026 (36 hours):** MITAOE's Samarth Vijay Chaudhari won 1st place with HOLY CROP (FARMORA), which uses AI to connect Indian farmers with global demand. [@MITAOE](https://x.com/MITAOE/status/2124500099074322600) · 19:17, 22 Nov
- **Symfony AI hackathon** closed: 52 people opened their first issue or PR in symfony/ai or the MCP SDK, and winners are due later this week. [@chr_hertel](https://x.com/chr_hertel/status/2124556107268141346) · 23:00, 22 Nov

### Student perks and credits
- No new free API or GPU credit programme open to Indian students was announced in the window.
- **Free to fine-tune:** Sarvam-105B-1711's BF16 weights are Apache-2.0, and NeMo RL post-training support is merged, so a college lab with GPU access can run RL on an Indian-language model today (see above).
- **Free weekend tutorial:** @anurag_629 shows how to build an MCP server with two tools (`add_note`, `search_notes`) so your AI assistant can search your own notes. It notes that the current Python SDK calls it `MCPServer`, not FastMCP. [@anurag_629](https://x.com/anurag_629/status/2124520810698117366) · 20:40, 22 Nov

### Grok Bots
- **A bot that safety-checks other Grok Bots before you add them.** Paste a template link and it returns a 0–100 safety score, what the bot can touch, and the gaps in plain words. It's read-only and never installs anything. [@bugatsinho](https://x.com/bugatsinho/status/2124504925266977000) · 19:37, 22 Nov · [the bot](https://x.ai/bot/92XfuHX18z-EBZabTy1Ma)
- **Obsidian reportedly shipped a Grok Bot plugin**, so several bots can share one notes vault as a "second brain". I'm going by the post here and didn't confirm it with Obsidian. [@irongiantXBT](https://x.com/irongiantXBT/status/2124535628268175672) · 21:39, 22 Nov
- **The most-engaged Grok Bot post was a clip of SpaceXAI engineer Lauren Tan on running a team of bots**, including letting agents merge their own pull requests. Treat "merge without review" as a talk, not a recipe for your repo. [@AnatoliKopadze](https://x.com/AnatoliKopadze/status/2124583259275497893) · 00:48, 23 Nov
- **A daily list of 10 Grok Bots** led with the safety checker above. [@dbarrett24](https://x.com/dbarrett24/status/2124563636353990978) · 23:30, 22 Nov

### Build idea of the day
**A Hindi and Rajasthani cyber-fraud complaint triage agent for the Rajasthan Police Hackathon (registration closes Tue 24 Nov, 23:59 IST).** Have a victim dictate what happened, then have Sarvam-105B-1711 turn it into a structured complaint and call tools to pull the transaction IDs and UPI handles. Its Indic and tool-calling scores are its strengths, and it runs on a single workstation GPU, so no citizen data leaves the station. Then have bison-1 assign calibrated probabilities across fraud categories and route only high-confidence cases automatically. Gate every action with aaf-gate's kill switch and audit log. For the demo, show a spoken complaint becoming a routed case file with a confidence score, entirely offline.

### What the field is arguing about
- **Should one number set the AI speed limit?** Pachocki argues that pretraining perplexity stays informative after benchmarks saturate, so labs could agree on a threshold. Critics will ask who audits the held-out dataset, and whether anyone stops if a rival doesn't. [TechCrunch](https://techcrunch.com/2026/11/22/openais-chief-scientist-has-thoughts-on-how-to-limit-ai-development/)
- **Who gets credit for the Riemann Hypothesis?** On HN, people are split between sympathy for Masullo's 12 years of work, "give them both credit", and warnings that the progress bar in his Lean formalization says nothing about whether the core idea holds. [HN](https://news.ycombinator.com/item?id=50598441) · [HN](https://news.ycombinator.com/item?id=50605045)
- **Is India's AI sovereignty served by hosting Chinese models?** Pratyush Kumar says Token Factory runs on Sarvam's own GPUs and that "some" narratives "appear manufactured". Inc42 points to the default data-training policy and the unit economics. [@pratykumar](https://x.com/pratykumar/status/2124530320200577082) · [Inc42](https://inc42.com/buzz/indias-inference-test-scaler-founders-new-ai-bet-more/)
- **Is local AI ready for normal people?** The top comment on a 300-point beginner's guide calls this "the plasma TV phase of local AI". Others reply with sub-$1k builds (a used workstation plus a 16GB GPU) running MoE models at ~30 tok/s. [HN](https://news.ycombinator.com/item?id=50603845) · 02:31, 23 Nov

### Worth reading in full
1. [Perplexity and Intelligence](https://openai.com/index/perplexity-and-intelligence) (Jakub Pachocki, OpenAI): the rare chart of a frontier lab's internal pretraining loss, and the case for using it as a shared safety yardstick.
2. [Sarvam-105B-1711](https://www.sarvam.ai/blogs/sarvam-105b-1711) (Sarvam): beyond the scores, a practical guide to serving a 105B model on one GPU, covering NVFP4, FP8 KV cache and a shared-memory kernel fix it sent upstream.
3. [Security researchers show how cheap AI inference providers steal keys](https://the-decoder.com/security-researchers-show-how-cheap-ai-inference-providers-steal-keys-and-snoop-on-users/) (The Decoder): read this before you route anything through the cheapest provider.
4. [A Beginner's Guide to Local AI with Inkling, Qwen, and Unsloth](https://www.gpupartner.com/blog/beginners-guide-local-ai-inkling-qwen-unsloth): how to pick a quantization for your VRAM, set up in 10–15 minutes on Windows without a terminal.
5. [What Happened to Silicon Valley?](https://www.oreilly.com/radar/what-happened-to-silicon-valley/) (Tim O'Reilly, [HN, 480 points](https://news.ycombinator.com/item?id=50602947)): a long essay arguing tech should optimise for "the game of human flourishing", and the day's biggest HN debate.

### Quiet accounts and anything I couldn't open
- No posts in the window: @OpenAI, @AnthropicAI, @GoogleDeepMind, @AIatMeta, @MistralAI, @huggingface, @karpathy, @simonw (his blog had one non-AI CSS post), @devpost. @_akhaliq only reposted MemOS's MemT-1.0-Pro launch and a LynnReal-Hand world-model paper. @trending_repos named Claude-BugHunter again (+1,803 stars in 24h, covered earlier). @chinchoukou's picks were repos covered earlier, plus non-AI AFFiNE, Ghost-Downloader-3 and nginx. @GithubProjects' AI posts (iFixAi, LoopForge, ffmpeg-skill, Agent Substrate, rust-anything) were all covered in earlier briefs, and EdenText isn't AI.
- The Decoder's simulated-workplace article is mostly paywalled, so I only had the intro. Google's "Physical Engineering's Last Exam" dataset (trending on HF) is gated. Reddit (r/LocalLLaMA, r/MachineLearning) blocked direct reads, and so did Kaggle (reCAPTCHA) and the LinkedIn event page. Product Hunt's AI feed, VentureBeat, Ars Technica, TLDR AI, Ben's Bites, Import AI, Latent Space and The Rundown had nothing new in the window. I didn't get to MLH, DoraHacks or lablab this run. Hype-heavy Grok Bot threads (Elon Musk quote clips, "faceless TikTok" income claims) were left out because I couldn't confirm them.

## Archive

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

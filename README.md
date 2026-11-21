# new stuff

This is an archive of daily AI briefs — new models, trending AI repos, hackathons, and Grok Bots — compiled each morning at 9 AM IST.

## Latest brief: 2026-11-21

## X Brief — Saturday 21 Nov 2026 (window: 20 Nov 09:00 → 21 Nov 09:00 IST)

Checked: 15 watch-list X accounts, 6 watch-list searches, plus 2 follow-up X searches (lab and press accounts behind the day's big stories, and the Riemann/Claude reaction); GitHub trending (daily, weekly, Python, TypeScript, Rust, Go, Jupyter); Hugging Face trending models, datasets, Spaces and daily papers; the Hacker News front page and Show HN; Product Hunt's AI feed; release notes for llama.cpp, vLLM, Ollama, LangChain, LangGraph and transformers; The Verge, TechCrunch, Ars Technica, The Decoder, CNBC, VentureBeat, OpenAI, Google, NVIDIA and Hugging Face blogs, Simon Willison, Latent Space, Ben's Bites, The Rundown, Import AI, and India AI coverage (AIM, Inc42, YourStory); Devpost, Unstop, lablab and LinkedIn (via web search) for hackathons; student-perk searches. All times are IST.

**TL;DR**
- **An Anthropic mathematician says he and Claude proved the Riemann Hypothesis.** Levent Alpöge's proof (which he says also covers the Generalized Riemann Hypothesis) is written in Lean, and mathematicians report that it compiles. Nobody has verified the maths yet. On the same day he and Tristan Buckmaster posted a Lean-checked Navier–Stokes blow-up proof.
- **Thinking Machines released Inkling 2 Mini under Apache-2.0.** It's a 26.4B looped MoE with 3.4B active parameters and a footprint of about 20GB. It ties Qwen3.8-27B on the Artificial Analysis Index, and llama.cpp, MLX and transformers supported it within hours.
- **AI stocks had a rough Friday.** Nvidia fell 14% amid reports of an SEC accounting probe, and Anthropic gave back 8.5% on its first full day of trading. OpenAI also published how it blocks people from distilling its models.

### The one thing that matters most
**A Claude-assisted proof of the Riemann Hypothesis was published in Lean, and it compiles.** Anthropic mathematician Levent Alpöge says that, "working with Claude", he found a proof of the Riemann Hypothesis that "easily extends" to the Generalized Riemann Hypothesis, and that he and Claude formalized the arguments with no extra assumptions. According to Scott Aaronson, the formal proof is 17.4 million lines of Lean. TechCrunch reports that several mathematicians on the Lean Zulip, including MIT's Andrew Sutherland, say it compiles. Even so, The Verge stresses that the result hasn't been independently verified, and Anthropic itself hasn't commented. On the same day, Stanford's Ravi Vakil posted Alessandro Masullo's all-human draft proof of GRH, the product of 12 years of work. About eight hours later Vakil added that people had reported problems in it, which they found with help from AI models. Terence Tao listed the day's results "in decreasing order of how 'digested' they are", and this one comes last: a Lean-only proof that no human has yet explained in words. For you, the takeaway is that the decisive check came from a proof assistant. Lean plus an LLM is turning into a real research tool, and it's worth learning. [The Verge](https://www.theverge.com/ai-artificial-intelligence/1010051/anthropic-riemann-hypothesis-millennium-prize-problem) · 22:04, 20 Nov · [TechCrunch](https://techcrunch.com/2026/11/20/ai-claimed-a-solution-to-the-167-year-old-riemann-hypothesis-and-a-human-did-too/) · 01:02, 21 Nov · [Alpöge's note via Simon Willison](https://simonwillison.net/2026/Nov/20/levent-alpoge/) · [HN, 2,420 points](https://news.ycombinator.com/item?id=50574968) · 19:46, 20 Nov · [Vakil on Masullo's GRH](https://math216.wordpress.com/2026/11/20/hurried-announcement-alessandro-masullo-grh/) · [Terence Tao](https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/)

### AI news

#### Science and research
- **Alpöge and Buckmaster posted a proof of finite-time blow-up for the Navier–Stokes equations.** It comes as a 79-page paper plus a Lean 4 package of about 2,270 files and 600,000 lines, which only accepts the standard axioms. It's another Millennium-adjacent result, and the repo shows exactly how a machine-checked maths project is laid out. [GitHub](https://github.com/tristanbuckmaster/navier-stokes/) · [HN, 265 points](https://news.ycombinator.com/item?id=50576232) · 21:04, 20 Nov
- **"Language Models Can Rewrite Their Own Weights."** An open 27B model was given its own weights and its graded answers. It diagnosed its failures and edited the weights itself, with no gradients, and scored 6.6 points higher on unseen problems. Smaller models in the same family broke themselves when they tried. It's a striking idea for a weekend reproduction. [arXiv](https://arxiv.org/abs/2611.21885) · [HN, 355 points](https://news.ycombinator.com/item?id=50577265) · 21:59, 20 Nov

#### Labs, products and APIs
- **OpenAI is cracking down on distillation.** It says attacks that pull protected reasoning out of earlier requests now succeed 0.2% of the time against GPT-6.2 Astra, down from 54.0% against GPT-6 Astra. It's also banning thousands to tens of thousands of accounts a week. If your project trains on GPT outputs, expect much less to get through. [OpenAI](https://openai.com/index/combatting-adversarial-distillation) · [@OpenAI](https://x.com/OpenAI/status/2123862344422088794) · 01:03, 21 Nov · [The Decoder](https://the-decoder.com/openai-makes-it-much-harder-for-attackers-to-extract-how-its-latest-ai-models-think/) · 02:01, 21 Nov
- **Gemini 3.5 Transcribe's voice editing is coming to the Gemini API.** It's the tech behind Rambler on Gboard, and it lets users edit, rephrase and translate existing text by voice. That makes voice-first note and form apps much easier to build. [@Google](https://x.com/Google/status/2123827048808370477) · 22:43, 20 Nov
- **Signal now blocks OS-level AI agents from reading its screen.** It uses screenshot blocking against the agents built into iOS 27 (Siri AI's Onscreen Awareness) and against Gemini Intelligence on Android, the same way it once blocked Windows Recall. If you're building a screen-reading agent, expect privacy-focused apps to start shutting it out. [Signal](https://signal.org/blog/protecting-your-privacy/) · [HN, 525 points](https://news.ycombinator.com/item?id=50572348) · 15:12, 20 Nov · [The Verge](https://www.theverge.com/ai-artificial-intelligence/1038390/signal-blocking-ai-agent-screenshots-mobile-app) · 18:00, 20 Nov
- **Nous Research's open-source Hermes Agent is coming to Microsoft Teams.** It runs in Azure sandboxes, and a "Collective Wisdom" feature lets a team share reviewed skills that Hermes automatically turns into description-plus-code bundles. Nous says Hermes is the most-used open agent on OpenRouter, at close to 2 trillion tokens a day. [The Decoder](https://the-decoder.com/hermes-agents-collective-wisdom-feature-turns-one-employees-ai-trick-into-the-whole-teams-skill/) · 15:29, 20 Nov

#### Money and policy
- **Nvidia fell 14% on Friday, its seventh straight weekly loss and the longest losing streak since 2008.** It's now down 46% over that stretch and ranks fourth by market cap. Reuters reported that the SEC is examining possible accounting issues, and California's attorney general has subpoenaed Nvidia over Huang's ties to China. Separately, The Information says Nvidia is close to buying diffusion-LLM startup Inception (maker of Mercury 3) for at least $500M to strengthen its open Nemotron models. [CNBC](https://www.cnbc.com/2026/11/20/nvidias-7-week-losing-streak-is-longest-since-2008-financial-crisis.html) · 04:29, 21 Nov · [TechCrunch, CA AG](https://techcrunch.com/2026/11/20/california-ag-subpoenas-nvidia-over-worries-about-huangs-ties-with-china/) · 18:51, 20 Nov · [The Decoder, Inception](https://the-decoder.com/nvidia-bets-at-least-500-million-on-inceptions-diffusion-models-to-strengthen-its-open-source-nemotron-lineup/) · 20:23, 20 Nov · [HN, SEC probe](https://news.ycombinator.com/item?id=50581438)
- **Anthropic closed its first full trading day down 8.5%, at $97.17.** That's still 17% above its $83 IPO price. Once underwriters bought the extra "greenshoe" shares, the IPO raised $93.5B in total. [CNBC](https://www.cnbc.com/2026/11/20/anthropic-stock-ai-amd-nvidia.html) · 02:57, 21 Nov · [CNBC, greenshoe](https://www.cnbc.com/2026/11/20/anthropic-ipo-greenshoe.html) · 20:29, 20 Nov
- **Cursor told lawmakers it may "explore phasing out" Chinese-developed open-weight models.** That matters because its Composer 2 model was built on Moonshot's Kimi K2.5. The news comes from a House report on Chinese models in the US tech stack. If you're building on Qwen, Kimi or DeepSeek, provenance is becoming a question customers will ask. [CNBC](https://www.cnbc.com/2026/11/20/cursor-chinese-ai-models-geopolitical-risk.html) · 19:37, 20 Nov
- **Trump threatened a "tremendous tax" on US companies that build data centres abroad,** speaking after his summit with Xi and Putin. [The Verge](https://www.theverge.com/policy/1038892/trump-foreign-data-centers-tax) · 00:20, 21 Nov · [CNBC](https://www.cnbc.com/2026/11/20/trump-data-centers-ai-companies-tax.html) · 02:17, 21 Nov

#### India AI
- **Goa approved its AI Policy 2026,** and 60% of its resources go to skilling, with a target of certifying 50,000 graduates by 2030. It also plans a Konkani LLM built on BHASHINI, an AI research centre, and an AI-adoption scheme for MSMEs. Look out for state-funded courses and certifications. [AIM](https://analyticsindiamag.com/ai-news/goa-cabinet-approves-ai-policy-2026-puts-60-towards-skilling) · 18:52, 20 Nov
- **Indian retail investors rushed to buy Anthropic shares.** The stock made up about 40% of INDmoney's international activity on debut day, and about 35% of Mudrex's daily users traded it, with average tickets of ₹2,000–3,000. [Inc42](https://inc42.com/buzz/anthropics-nasdaq-debut-sparks-buying-rush-among-indian-retail-investors/) · 19:12, 20 Nov

### New models and weights
| Model | Maker | Size | License | Why it matters | Link |
|---|---|---|---|---|---|
| Inkling 2 Mini | Thinking Machines | 26.4B total, 3.4B active (MoE); the middle layers loop 3× per token; about 20GB in NVFP4/MXFP8; 1M context, text and image input | Apache-2.0 | The strongest open model under 100B on DeepSWE v1.1 (48.2%), by its maker's own numbers, and small enough for a laptop. Its makers ran it offline on a MacBook Pro mid-flight and had it build a flight simulator | [HF](https://huggingface.co/thinkingmachines/Inkling-2-Mini) · [blog](https://thinkingmachines.ai/news/inkling-2-mini/) · [@thinkymachines](https://x.com/thinkymachines/status/2123871643797995872) · 01:40, 21 Nov · [HN, 762 points](https://news.ycombinator.com/item?id=50581260) |
| Inkling 2 Mini GGUF | Unsloth | Quantized builds of the model above | Apache-2.0 | The easiest way to run it locally. llama.cpp added support in [b12600](https://github.com/ggml-org/llama.cpp/releases/tag/b12600) (05:00, 21 Nov), and HF shipped transformers and MLX support ([HF blog](https://huggingface.co/blog/inkling2mini)) | [HF](https://huggingface.co/unsloth/Inkling-2-Mini-GGUF) · [@mervenoyann](https://x.com/mervenoyann/status/2123875145182048750) · 01:54, 21 Nov |
| TML-d24-varloop-research | Thinking Machines | A variable-loop research variant of Inkling 2 Mini | Apache-2.0 | Released alongside Mini for TML's monitorability experiments. In its tests, serial-reasoning scores kept improving out to 10 loops, twice what it was trained with. It's a ready-made student research project | [HF](https://huggingface.co/thinkingmachines/TML-d24-varloop-research) |

### Benchmarks and leaderboards
- **Inkling 2 Mini scores 20.1 on the Artificial Analysis Intelligence Index, the same as Qwen3.8-27B.** On its makers' coding numbers it beats Qwen on DeepSWE v1.1 (48.2% vs 42.2%) and loses narrowly on Terminal-Bench 2.1 (71.6% vs 73.0%). [@TeksEdge](https://x.com/TeksEdge/status/2123930642043793868) · 05:35, 21 Nov
- **OpenAI launched MedChemBench,** which tests whether models can read molecular structures, interpret experimental results and choose which compounds to test next, including trade-offs where improving one property hurts another. [OpenAI](https://openai.com/index/introducing-medchembench/) · [@OpenAI](https://x.com/OpenAI/status/2123856316187975756) · 00:39, 21 Nov
- **Inkling 2 Small is now the top US open model on Agent Arena,** according to Sentient's roundup, which also says Alibaba plans to open-source smaller Qwen4 models. [@sentient_found](https://x.com/sentient_found/status/2123807720973246838) · 21:26, 20 Nov
- **Harness gaps again.** One audit of every leaderboard finds Gemini 4 Neon's viral 39% score drops to 12.8% outside Google's own harness, and that Neon ranks 6th on WebDev Arena ([@amitmuflis](https://x.com/amitmuflis/status/2123970132620009633), 08:11, 21 Nov). Another post points out that 7 of the top 15 GitHub-trending repos are agent infrastructure and none are fine-tuning ([@ComputeLeapAI](https://x.com/ComputeLeapAI/status/2123663725962101048), 11:54, 20 Nov).

### Trending repos and projects
1. **[tristanbuckmaster/navier-stokes](https://github.com/tristanbuckmaster/navier-stokes/)**: the Navier–Stokes blow-up paper with its full Lean 4 formalization, and a README that maps each formal statement to the paper. Read it to learn how a large formal-proof project is organised. Lean · 236★ (created yesterday)
2. **[walkinglabs/learn-harness-engineering](https://github.com/walkinglabs/learn-harness-engineering)**: a free course on agent harnesses with 14 lessons and 8 project templates (repo rules, multi-session state, verification, loop and graph engineering). Copy one template into your hackathon repo so your coding agent stays on task. TypeScript · 25,707★ · [@Mr_Buzzoni](https://x.com/Mr_Buzzoni/status/2123746427625148612) · 17:23, 20 Nov
3. **[zhouxiaoka/autoclip](https://github.com/zhouxiaoka/autoclip)**: an open-source desktop tool that cuts podcasts, lectures and interviews into short clips, with LLM-picked highlights, subtitles, covers and post copy. You could build a "lecture → reels" tool for your college club on it. Python · 12,272★ (+979 today, GitHub Trending) · [@chinchoukou](https://x.com/chinchoukou/status/2123929434256457840) · 05:30, 21 Nov
4. **[diggerhq/opencomputer](https://github.com/diggerhq/opencomputer)**: a self-hostable, open alternative to Devin. You tag @Computer in a Slack thread, it works on its own VM using Claude Code, Codex or OpenCode, and the result arrives as a PR. Use it to give your team a shared coding agent during a hackathon. TypeScript · 761★ · Apache-2.0 · [Show HN](https://news.ycombinator.com/item?id=50581403) · 01:49, 21 Nov
5. **[anomalyco/opencode](https://github.com/anomalyco/opencode)**: the open-source terminal coding agent. Point it at a local model such as Inkling 2 Mini and you have a free, offline coding setup. TypeScript · 228,264★ (+247 today, TypeScript trending)
6. **[earendil-works/pi](https://github.com/earendil-works/pi)**: an agent toolkit with one LLM API, an agent loop, a TUI and a coding-agent CLI. It's a clean base if you want to write your own agent rather than wrap someone else's. TypeScript · 123,090★ (+165 today)
7. **[wshobson/agents](https://github.com/wshobson/agents)**: plugins, agents, skills and commands written once in Markdown, then generated for Claude Code, Codex CLI, Cursor, OpenCode, Copilot and Pi, with validation and evals. Write your team's agent rules once and use them in every tool. Python · 42,744★ (+41 today)
8. **[bendlang/bend](https://github.com/bendlang/bend)**: Bend 2, a fast language that "blocks AI mistakes via proof". It fits the Lean theme of the day: AI writes the code, and the type system checks it. TypeScript · 25,698★ (+95 today)
9. **[janhq/jan](https://github.com/janhq/jan)**: an open-source ChatGPT alternative that runs 100% offline. It's the quickest GUI for trying new open weights on your own machine. Rust · 45,970★ (+101 today)
10. **[agentscope-ai/agentscope](https://github.com/agentscope-ai/agentscope)**: a framework for building and running agents "you can see, understand and trust". Use it to show judges what your multi-agent system is doing. Python · 36,397★ (+69 today)
11. **[tianma-if/edgeever](https://github.com/tianma-if/edgeever)**: an AI-native, local-first notes app (an Evernote/Obsidian alternative) with a web clipper and MCP. Your agent can read and write your notes through MCP. TypeScript · 3,461★ (+28 today) · AGPL-3.0
12. **[croffasia/itsaplan](https://github.com/croffasia/itsaplan)**: a self-hosted Linear/Plane alternative where teams and AI agents plan and track issues together. It's a ready-made board for a team made of humans plus agents. TypeScript · 2,446★ · AGPL-3.0
13. **[cdcseacave/openMVS](https://github.com/cdcseacave/openMVS)**: turns camera-aligned photos into dense point clouds, meshes and textured 3D models. Pair it with a phone camera for an AR or heritage-scanning demo. C++ · 4,232★ · [@GithubProjects](https://x.com/GithubProjects/status/2123782435444056284) · 19:46, 20 Nov

Release notes: llama.cpp [b12600](https://github.com/ggml-org/llama.cpp/releases/tag/b12600) added Inkling 2 Mini, and b12590 added drama3 voice cloning. vLLM, Ollama, LangChain, LangGraph and transformers published nothing new in the window.

### Hackathons
Open ones, soonest deadline first:
1. **Seed Hackathon 2026, "The Age of Autonomy"**: free and online, with Boston University and GW Engineering, in teams of 2–3. It's open to final- and pre-final-year BE/BTech/BSc/BCA students, first- and second-year ME/MTech/MSc/MCA students, and working professionals. The prize list shows ₹50K, ₹35K and ₹15K, although the description says the pool is ₹2 lakh. The finale is on 9 Dec, and **registration closes Sun 22 Nov, 23:59 IST**. [Unstop](https://unstop.com/hackathons/crp-seed-hackathon-2026-seed-global-education-services-private-limited-1798287)
2. **Festive Hacks (WeMakeDevs × WeAreDevelopers)** (reminder, with Sarvam now confirmed): one day in person at BIEC, Bengaluru, on **Wed 25 Nov**. You enter solo or in a team of up to 4, every member has to apply, and the hosts pick who gets in. You build a fix for a festive-season problem, and Sarvam's speech-to-text, text-to-speech and translation APIs cover 22 Indian languages. The winning team gets a fully paid trip to WeAreDevelopers World Congress in Berlin in July 2027. Second place (best use of Flagsmith) wins ₹1 lakh plus $1,000 in Sarvam credits, and third wins $1,000 in Sarvam credits. [Luma](https://luma.com/festivehacks) · [@WeMakeDevs](https://x.com/WeMakeDevs/status/2123720961203777830) · 15:41, 20 Nov
3. **Anveshak (Techfest, IIT Bombay)**: a computer-vision contest with ₹1.5 lakh for the top 3. You build one remote-sensing detector, trained from scratch with no pretrained weights, that detects 40 classes, flags unknown objects and learns new ones without forgetting the old ones. Round 1 is online, and the later rounds are at Techfest. It's for students with a valid ID, in teams of up to 4, and **registration closes Mon 30 Nov, 00:01 IST**. [Unstop](https://unstop.com/hackathons/anveshak-open-world-object-detection-for-remote-sensing-iit-bombay-1818894)
4. **Campus to Cloud (Techfest, IIT Bombay × AWS)**: online, with ₹1.5 lakh for the top 3. The highlights also list a year of AWS Skill Builder Premium, up to $30 in AWS credits and a $100 certification voucher. You build and deploy something on AWS. It's for students aged 18+ at Indian institutions, in teams of up to 4, and the top 35 teams present at IIT Bombay on 17 Dec. The page says the deadline is 30 Nov at 11:59 PM, but Unstop's timer shows **30 Nov, 00:00 IST**, so plan for the earlier one. [Unstop](https://unstop.com/hackathons/campus-to-cloud-hackathon-iit-bombay-1818968)
5. **Kiroween 2026** (reminder, now 14 days left): $100K, online, and **India is eligible**, in teams of up to 3. Each of the four categories has a **$1,500 student prize** plus a year of Kiro Pro Max, and first place overall wins $30K. You have to build a new project with Kiro, and registered participants can request Kiro credits. 17,778 people have signed up. The deadline is **Sat 5 Dec, 03:30 IST**. [@devpost](https://x.com/devpost/status/2123798150708158728) · 20:48, 20 Nov
6. **Merry Shipmas Bengaluru (NERDCONF)**: a hybrid event for builders aged 18+, students included, solo or in teams of up to 4. It kicks off online on Fri 11 Dec, has an in-person build day in Bengaluru on **Sat 12 Dec, 10:00–18:00 IST**, and then gives you until 20 Dec to get real users. Prizes haven't been announced yet. [Unstop](https://unstop.com/hackathons/merry-shipmas-bengaluru-christmas-ai-hackathon-nerdconf-1820028)
7. **Adaptive Intelligence Challenge (Adaption on HackCulture)**: global and online, with a ₹3 lakh pool, 1,000 + 250 free credits and three weekly challenges. You build a custom model, try to beat a benchmark and release open weights. I couldn't open the event page to confirm the deadline. [HackCulture](https://hackculture.io/hackathons/adaptive-intelligence-challenge) · [@Hack_Culture](https://x.com/Hack_Culture/status/2123660837777035274) · 11:42, 20 Nov

**Winners**
- **Nous Research's Hermes Agent Plugin Hackathon**: nearly 1,000 entries in 7 days. Agents scored every entry, and then five community judges picked the top 10. **Foreman** won: it blocks merges that skip or delete tests or change secrets, has a second model review the diff, and asks you to approve over Telegram. **Housemate**, which turns an old phone into a hands-free room speaker, came second, and **Plan Mode**, which blocks every tool that can change the project while the agent is still planning, came third. [@NousResearch](https://x.com/NousResearch/status/2123882430620733742) · 02:23, 21 Nov · [winner list, @real_kukuruza](https://x.com/real_kukuruza/status/2123893620629492051) · 03:07, 21 Nov
- **Syncly won first place and $10K at the Tameion agents hackathon.** Its agents handle websites, content, promo videos and customer-finding for small businesses, with payments held in escrow. [@neromtoobad](https://x.com/neromtoobad/status/2123762864414462312) · 18:28, 20 Nov
- **A University of Seoul international-relations student won the agriculture track** of the World Bank's Small AI for Development Hackathon Challenge. It shows that small, focused AI for a real sector can win. [@koreatimescokr](https://x.com/koreatimescokr/status/2123778400032879075) · 19:30, 20 Nov

### Student perks and credits
- **Kiroween participants can request free Kiro credits** for the whole submission period (see the Resources tab on the Devpost page), and India is eligible. [@devpost](https://x.com/devpost/status/2123798150708158728)
- **OpenAI's Codex for Students gives $100 in ChatGPT credits for Codex, valid for 12 months,** but only to verified university students in the **US and Canada**, so Indian students can't claim it yet. [OpenAI Help](https://help.openai.com/en/articles/20001147-codex-credits-for-students-terms-of-service)
- **Credits through hackathons:** Festive Hacks gives $1,000 in Sarvam credits to each of the second- and third-place teams, and Campus to Cloud lists up to $30 in AWS credits, AWS Skill Builder Premium and a $100 certification voucher (see Hackathons).
- No new free API or GPU credit programme open to Indian students surfaced in the window.

### Grok Bots
- **The Grok Bot team's Matt Palmer and Lauren Tan did an hour-long Q&A** covering how many bots Lauren runs, how to build a Chief of Staff bot, and the biggest mistake people make. It was the most-engaged Grok Bot post of the day. [@0xg4tsby](https://x.com/0xg4tsby/status/2123735769583874486) · 16:40, 20 Nov
- **Two importable Grok Bots that filter slop and bot replies** for CS Twitter, shared as public bot links. [@rattecs](https://x.com/rattecs/status/2123867985958023328) · 01:26, 21 Nov
- **Your Grok Bot can have its own email address.** It starts working when mail arrives, and its replies wait until you press Send. The post sketches people's bots emailing each other. [@CarolinaDill](https://x.com/CarolinaDill/status/2123764412959871140) · 18:34, 20 Nov
- **Use one Grok Bot to check that your other bots actually did the job** before you trust their "done". [@cradrrat](https://x.com/cradrrat/status/2123670901380047278) · 12:22, 20 Nov
- **22 free Grok Bots for contractors**: estimators for most trades plus a collector, a change-order writer and a crew scheduler. [@CompanyFramewrk](https://x.com/CompanyFramewrk/status/2123869606066425875) · 01:32, 21 Nov
- **A caution:** one user says all their Grok Bots disappeared after they clicked "Merge Account", and the merge is stuck at 85%. Export anything important before you merge accounts. [@ChengDemry](https://x.com/ChengDemry/status/2123976214830592420) · 08:36, 21 Nov

### Build idea of the day
**An offline coding tutor for Kiroween's Resurrection category (deadline Sat 5 Dec, 03:30 IST, with a $1,500 student prize).** The idea is to bring back the offline help system old IDEs used to ship, rebuilt as an agent. Run Thinking Machines' Inkling 2 Mini (Apache-2.0, about 20GB) locally through Unsloth's GGUF in llama.cpp, which supports it from b12600, so it works in a hostel with bad Wi-Fi. Build it in Kiro, and borrow the repo-rules and verification templates from learn-harness-engineering so the tutor runs your tests before it claims a fix works. For the demo, show it working in airplane mode, just as Thinking Machines did.

### What the field is arguing about
- **Does a compiling Lean proof count as "solved"?** Tao ranks the day's results by how well humans have digested them and puts the Riemann proof last. A commenter on his blog points out that Wiles's 1993 gap took two years to repair. Scott Aaronson's tongue-in-cheek "stochastic parrots have apparently proved the Riemann Hypothesis" drew 206 comments on HN. [Aaronson](https://scottaaronson.blog/?p=10344) · [HN](https://news.ycombinator.com/item?id=50581084) · 01:33, 21 Nov · [Re: Riemann, HN](https://news.ycombinator.com/item?id=50583982) · 05:12, 21 Nov
- **Was distillation the hidden engine of open weights?** Ethan Mollick suggests that, with easy distillation from OpenAI and Anthropic now effectively over, open-weight progress may slow. [@emollick](https://x.com/emollick/status/2123867811005014143) · 01:25, 21 Nov
- **Does model origin matter?** After the Cursor report, builders are asking what it would cost to rebuild work already done on top of an open Chinese base: Composer 2 raised CursorBench from Kimi K2.5's 36.0% to 61.3%. [@StragglerLiu](https://x.com/StragglerLiu/status/2123961572745986314) · 07:37, 21 Nov
- **"We promoted developers into architects without informing them."** The post argues that AI will write the try/catch, but you still have to push back on requirements and design the data model. [Blog](https://manidoraisamy.com/developer-to-architect.html) · [HN, 331 points](https://news.ycombinator.com/item?id=50579331) · 23:47, 20 Nov

### Worth reading in full
1. [Terence Tao on the day's three results](https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/): the calmest guide to what's actually established, and the comment thread is just as good.
2. [Inkling 2 Mini, from Thinking Machines](https://thinkingmachines.ai/news/inkling-2-mini/): looped transformers, NVFP4 training, and how looping affects how well you can monitor a model's chain of thought.
3. [The War Against Slop and an Emerging Weapon to Fight It: Formal Verification](https://latent.space/p/formal-verification/) (Latent Space): why AI plus Lean is about to matter for ordinary software too.
4. [Vibecoding an inference chip](https://ankitg.me/blog/vibecoding-inference-chip/): a founder with no FPGA experience got an LLM running on an FPGA by working with coding agents ([HN](https://news.ycombinator.com/item?id=50579297), 23:45, 20 Nov).
5. [Scott Aaronson: "The stochastic parrots have apparently proved the Riemann Hypothesis"](https://scottaaronson.blog/?p=10344): a complexity theorist's take on what this means and what it doesn't.

### Quiet accounts and anything I couldn't open
- No posts in the window: @karpathy, @MistralAI. @huggingface only reposted (Inkling 2 Mini, Depth Pro 2, Qwen3.8-27B super-adapter, its 1 EB/month CDN, LoRA for RFD4-Proteina, and an older TechCrunch story about Nvidia planning to buy Hugging Face). @AnthropicAI posted only a co-founders video. @GoogleDeepMind posted a Gemini 4 Neon ski-sim demo. @AIatMeta posted a recap of its Open Source AI for Science Summit. @simonw asked whether Gemini 4 Neon beats Carbon and whether Argon is retired. @_akhaliq mostly reposted (Arcfront's launch, Jeveration, MC-Lens). @trending_repos named Claude-BugHunter, and @GithubProjects' and @chinchoukou's AI picks were mostly repos covered earlier. @GithubProjects also ran a sponsored Dreamina thread. @anurag_629 posted only Python tips.
- Reddit (r/LocalLLaMA, r/MachineLearning) blocked direct reads. Ars Technica's "2M canaries in the AI supply chain" piece, Reuters' SEC-probe story (via MarketScreener) and HackCulture's event page didn't load. The YourStory × Google Cloud voice-AI hackathon (₹8 lakh) is for working professionals only, so it's left out. VentureBeat, Ben's Bites and Import AI had nothing in the window, and The Rundown's issue was an IPO recap. Product Hunt's AI feed had nothing notable. I didn't get to TLDR AI, DoraHacks or Kaggle this run.

## Archive

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

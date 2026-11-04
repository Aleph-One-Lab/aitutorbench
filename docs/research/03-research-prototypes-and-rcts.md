# Research prototypes, academic studies, open-source systems, and ITS lineage (2026-10-05)

Star counts pulled live via GitHub API on that date. Web-search budget ran out near the end; items the researcher could not re-verify are flagged.

## 1. RCTs and field studies of LLM tutors with learning outcomes

| Study | Year | Setting | N | Design | Effect size / headline | URL |
|---|---|---|---|---|---|---|
| Tutor CoPilot (Wang, Demszky et al., Stanford) | 2024 | K-12 math, live virtual tutoring, under-served students; GPT-4 real-time suggestions to human tutors | 900 tutors, 1,800 students | Preregistered RCT | +4 pp topic mastery (p<0.01); +9 pp for students of lower-rated tutors; tutors ask more guiding questions, give fewer answers; ~$20/tutor/yr | https://arxiv.org/abs/2410.03017 |
| PS2 Pal (Kestin et al., Harvard) | 2024 preprint; Sci. Reports 2025 | Intro physics (PS2); custom GPT-4 tutor vs in-class active learning | 194 | Randomized crossover, 2 topics | d≈0.73–1.3 vs active learning, in less time; tutor reveals one step at a time, pre-loaded solutions. DOI not re-verified (publisher blocked fetch) | https://www.researchgate.net/publication/392839220 |
| GPT Base vs GPT Tutor (Bastani et al., Wharton/Penn; PNAS 2025) | 2024/25 | Turkish high-school math, in-class practice | ~1,000 | 3-arm RCT | Practice: +48% (GPT Base), +127% (GPT Tutor). Unassisted exam: −17% for GPT Base; harm largely eliminated with hint-only GPT Tutor | https://www.pnas.org/doi/10.1073/pnas.2422633122 |
| From Chalkboards to Chatbots (De Simone et al., World Bank) | 2025 | Edo State, Nigeria; 9 public secondary schools; 6-wk after-school English using Microsoft Copilot (GPT-4), teacher-supervised | not stated in abstract (flag) | RCT | 0.31 SD composite, 0.23 SD English; ~1.5–2 yrs equivalent schooling; dose-response; larger for girls and higher-baseline students | https://eric.ed.gov/?id=ED676624 |
| Rori (Henkel et al., Oxford + Rising Academies) | 2024 | Ghana, grades 3–9, 11 schools; WhatsApp math tutor, 2×30 min/wk, 8 months | ~1,000 | RCT | 0.37 SD math growth (p<0.001) (0.36 in press summaries); ~$5/student/yr claimed | https://arxiv.org/abs/2402.09809 |
| GPT-4 homework tutor (Vanzo, Pal Chowdhury, Sachan, ETH; ACL 2025) | 2025 | Italian technical high school, ESL; GPT-4 replaces homework, 8 wks | 76 (4 classes) | RCT | Grammar gains significantly higher in one cohort, non-inferior elsewhere; higher satisfaction; all wanted continued access | https://aclanthology.org/2025.acl-long.1502/ |
| Khanmigo two-year trial (Oreopoulos & Low, Toronto/Brown) | 2026 | 18 Tennessee middle schools, remedial math blocks | not in abstract | 2-yr cluster RCT | 0.06–0.08 SD/yr (1.3 percentile ranks/term); 0.14 SD for full-year active users; median student messaged Khanmigo on 1/3 of practice days and in 17% of error sessions; gains resemble Khan practice without AI | https://edworkingpapers.com/ai26-1551 |
| LLM-guided RL tutor (Chung, Zhang, Kung, Bastani, Bastani) | 2026 | Taipei, 10 high schools, 5-month Python course; chatbot + RL problem sequencing | 770 | RCT (fixed vs adaptive sequence) | +0.15 SD final exam; +0.215 SD for beginners, ~0 for students with prior skill; mediated by engagement | https://arxiv.org/abs/2608.16907 |
| LearnLM on Eedi, UK classrooms (Google + Eedi) | 2025 | 5 UK secondary schools, chat math tutoring, human tutors approve each AI message | 165 | Exploratory RCT | 76.4% of LearnLM messages sent with zero/minimal edits; +5.5 pp novel-problem success (66.2% vs 60.7%); comparable to human-tutored | https://arxiv.org/abs/2512.23633 |
| Medly micro-RCTs (Harrison, Higgins et al.) | 2026 | GCSE science revision, 4 weeks | 929 (644 post-tested) | Multisite individually randomised | g=0.33 overall (phys 0.31, chem 0.32, bio 0.52); no SES gap | https://arxiv.org/abs/2609.14789 |
| ChatGPT vs human hints (Pardos & Bhandari, Berkeley; PLOS ONE) | 2024 | Algebra/statistics problems on OATutor | adult learners | Randomized hint conditions | Only ChatGPT-hint arm significantly > no-help control; no difference vs human-authored hints; self-consistency cut hint error to 0–2% (13% stats) | https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0304013 |
| LLM feedback for tutor trainees (Thomas, Borchers, Koedinger, CMU) | 2025 | 7 scenario lessons on PLUS platform, gpt-3.5 feedback | 885 learners | Quasi-experimental, propensity-adjusted | Significant in 2/7 lessons, d=0.28 and 0.33; benefits only for those who chose to use feedback | https://arxiv.org/abs/2506.17006 |
| Jill Watson (Goel lab, Georgia Tech) | 2024 | Multiple online courses; RAG VTA over course materials | multi-course | Quasi-experimental deployment | 78.7% answer accuracy (OpenAI Assistant ~30% on same tests); more A grades (66% vs 62%); higher teaching presence; more higher-order questions | https://www.cc.gatech.edu/news/georgia-techs-jill-watson-outperforms-chatgpt-real-classrooms , https://arxiv.org/abs/2407.17429 |
| M-Powering Teachers (Demszky, Stanford) | 2021–23 | Teacher-facing NLP feedback on uptake of student ideas | 1,136 instructors; 414 mentors | Two RCTs | +13% and +10% uptake of student contributions; mentors' talk time −5% | https://edworkingpapers.com/ai21-483 |

## 2. Research tutoring systems, datasets and prototypes

| System / paper | Institution, year | What it does | Pedagogy mechanics | Evaluation | URL |
|---|---|---|---|---|---|
| Bridge | Stanford (Wang, Demszky), NAACL 2024 | Models expert remediation decisions from 700 real 1st–5th grade tutoring sessions | Cognitive task analysis: identify error → choose strategy → intention → respond | GPT-4 responses with expert decisions +76% preferred | https://aclanthology.org/2024.naacl-long.120/ |
| MathDial | ETH (Macina, Sachan), EMNLP 2023 | ~2.8k teacher–LLM-student tutoring dialogues on GSM8k | Human teachers scaffold an LLM student seeded with misconceptions | Dataset + baselines | https://aclanthology.org/2023.findings-emnlp.372/ |
| Verify-then-generate | ETH, EMNLP 2024 | Stepwise verification of student solutions before generating feedback | Error localization conditions the remediation | Human/LLM-judge | https://aclanthology.org/2024.emnlp-main.478/ |
| MathTutorBench | ETH, EMNLP 2025 (oral) | Benchmark of open-ended tutoring abilities + leaderboard | Learning-science-defined skills (scaffolding, mistake detection, etc.) | Finds pedagogy–expertise trade-off | https://arxiv.org/abs/2502.18940 |
| PedagogicalRL | ETH, EMNLP 2025 (oral) | Online RL with simulated students trains a 7B tutor | Adjustable reward weighting between teaching quality and correctness | 7B ≈ LearnLM on pedagogy | https://arxiv.org/abs/2505.15607 |
| Blind educator comparison | ETH/Bocconi/EPFL, 2025 | Educators rate human vs LLM tutor responses blind | Engagement, empathy, scaffolding, conciseness | 80% of annotators prefer LLM on empathy | https://arxiv.org/abs/2506.08702 |
| LearnLM | Google, 2024–25 | Gemini fine-tuned for "pedagogical instruction following" | System-prompt-specified pedagogy attributes; 7 benchmarks | Experts prefer LearnLM +31% vs GPT-4o, +11% vs Claude 3.5 Sonnet, +13% vs Gemini 1.5 Pro | https://arxiv.org/abs/2412.16429 , https://arxiv.org/abs/2407.12687 |
| CS50 duck | Harvard (Liu, Malan), SIGCSE 2024 | Course-specific GPT-4 TA with "hearts" throttling, explain-code, style feedback | Guidance-not-answers prompting; rate limits force deliberate questions | 70-student pilot → ~211k users, 10M queries; 94% found helpful; no RCT | https://cs.harvard.edu/malan/publications/V1fp0567-liu.pdf |
| PLUS tutor training / Effective Praise | CMU (Thomas, Koedinger), 2024–25 | GPT-4 feedback for tutors in scenario lessons; classifier of effective praise | Tutoring-skill rubrics | GPT-4 88.4% acc, F1 0.92 vs expert labels | https://link.springer.com/chapter/10.1007/978-3-031-98465-5_20 |
| LLM vs ITS adaptivity | CMU (Borchers, Shou), AIED 2025 | 75 scenarios, 1,350 generated moves with ablated context | Tests whether LLMs adapt to student errors/KCs like Cognitive Tutors | Only marginal adaptivity; GPT-4o "overly direct"; unlikely to rival ITS gains | https://arxiv.org/abs/2504.05570 |
| Beyond Final Answers | Georgia Tech (MacLellan), 2025 | GPT-3.5→o1 as college-algebra solver and tutor | Human role-played students | 85.5% solve accuracy; 90% high-quality dialogues but only 56.6% error-free | https://arxiv.org/abs/2503.16460 |
| GPT-4 tutor + GPT-3.5 student hint validation | Microsoft Research + MPI-SWS (Phung, Gulwani), LAK 2024 | Programming hints validated by simulated student | Student model filters hints | 3 real Python datasets | https://dl.acm.org/doi/10.1145/3636555.3636846 |
| Shiksha Copilot | Microsoft Research India, 2025 | Teacher-facing RAG lesson planning (Karnataka, English/Kannada) | Human curation loop | Field deployment; time savings | https://arxiv.org/abs/2507.00456 |
| tutorbot-DPO | UMass Amherst + Rice (Scarlatos, Lan, Baraniuk), AIED 2025 | Llama-3.1-8B trained to maximize predicted student correctness | LLM student model + GPT-4o rubric → DPO | Higher predicted correctness at GPT-4o pedagogy quality | https://arxiv.org/abs/2503.06424 |
| SocraticLM | NeurIPS 2024 | Socratic math tutor trained on 35k multi-agent dialogues | Question-driven guidance | Human/LLM eval; repo 180 stars | https://github.com/Ljyustc/SocraticLM |
| PEARL / HeuristicEdu / Hey Chat | 2026 | RL-aligned Socratic tutors; prerequisite-graph + PPO curriculum policy with LLM dialogue | Generative reward models; controllable student simulators | "Structure beats scale": curriculum policy outperforms frontier models on mastery/turns | https://arxiv.org/abs/2605.29582 , https://arxiv.org/abs/2607.22996 , https://arxiv.org/abs/2606.11744 |
| MRBench / Unifying AI Tutor Evaluation | MBZUAI (Maurya, Kochmar), NAACL 2025 | 192 conversations, 1,596 responses, 8 pedagogical dimensions | Mistake identification, guidance, actionability, etc. | Separates good tutors from good QA systems; basis for BEA 2025 shared task | https://arxiv.org/abs/2412.09416 |
| Misconception diagnosis (Eedi) | UCL and others, 2026 | Diagnose misconceptions from dialogue; "Correct Answer Trap" | Detection of flawed reasoning behind right answers | ~4 false alarms per true detection; 71% of failures in 2 question types | https://arxiv.org/abs/2602.02414 , https://arxiv.org/abs/2605.23925 |
| Simulated students | UMass + Eedi, 2026 | Validates LLM student simulators used for training/eval | Linguistic, behavioral, cognitive fidelity | Prompting "performs poorly"; SFT/DPO better but limited; sycophancy risk | https://arxiv.org/abs/2601.04025 , https://arxiv.org/abs/2605.12748 |
| Knowledge tracing with LLMs | 2025–26 | LLM-KT, CIKT, Next-Token KT | LLM as sequence model over student history | Specialized KT models still beat LLMs on accuracy/cost | https://arxiv.org/abs/2502.02945 , https://arxiv.org/abs/2603.02830 , https://arxiv.org/abs/2412.09248 |
| Agentic tutors | 2026 | IntelliCode (6 agents over versioned learner state), ITAS (ODU quantum course), DeepTutor + TutorBench | Orchestrator + specialist agents; profile-driven student simulator | Mostly simulated-learner evals; latency/cost compounding documented | https://arxiv.org/abs/2512.18669 , https://arxiv.org/abs/2604.24808 , https://arxiv.org/abs/2604.26962 , https://arxiv.org/abs/2604.24110 |
| Usage-in-the-wild | 2025–26 | StudyChat (Stanford-adjacent), "Your Students Don't Use LLMs Like You Wish They Did" (12,650 msgs, ACL 2026) | — | Students mainly answer-extract; deployment context is strongest predictor | https://arxiv.org/abs/2503.07928 , https://arxiv.org/abs/2604.23486 |
| Tutor-GPT / Bloom | Plastic Labs, 2023– | Theory-of-mind prompting; dynamic prompt rewriting; Honcho user memory | Learner-state inference | No published learning evaluation | https://github.com/plastic-labs/tutor-gpt |
| OATutor | UC Berkeley CAHLR (Pardos), CHI 2023 | Open-source BKT-based ITS with OpenStax algebra content | Mastery learning, hints/scaffolds; now used for LLM-hint A/B tests | Platform paper | https://dl.acm.org/doi/10.1145/3544548.3581574 |
| Stanford SCALE GenAI hub; MIT "Your Brain on ChatGPT" | 2025 | Stanford–OpenAI research partnership on ChatGPT study mode; MIT EEG study (N=54) showing reduced connectivity/ownership with LLM essay writing | — | Observational/lab | https://scale.stanford.edu/research-in-action/how-chatgpt-impacting-schools , https://arxiv.org/abs/2506.08872 |
| Khan Academy + OpenAI | 2023–26 | Khanmigo built on GPT-4 (background knowledge, not re-verified); Khan efficacy: 350k students, +0.36 effect for 30+ min/wk users but only 9% reach that dose | Socratic prompting | Toronto/Stanford Khanmigo studies → Oreopoulos 2026 above | https://blog.khanacademy.org/?p=18194 |
| OpenStax Kinetic (Rice) | 2025 | Research platform embedding studies in OpenStax learners; 2025 AI-tutoring pilot announced | — | No published LLM-tutor outcome study found (flag) | https://openstax.org/research , https://news.rice.edu/news/2025/rice-accelerates-ai-innovation-transform-teaching-learning-and-research |
| Open Tutor (ambiguous) | — | Three candidates: USC ICT "opentutor" (dialog tutor, repos ≤4 stars), zijinz456/OpenTutor (local adaptive workspace), Open TutorAI (arXiv 2602.07176, 3D avatars, no eval) | — | Flag: unclear which was intended | https://arxiv.org/abs/2602.07176 |

## 3. Open-source tutoring repos (stars as of 2026-10-05)

| Repo | Stars | What | Last push |
|---|---|---|---|
| JushBJJ/Mr.-Ranedeer-AI-Tutor | 29,569 | GPT-4 tutor mega-prompt (no code, no eval) | 2025-09 |
| plastic-labs/honcho | 7,474 | User-memory library spun out of Tutor-GPT | 2026-10 |
| oppia/oppia | 6,842 | Pre-LLM open learning platform | 2026-10 |
| HugeCatLab/ChatTutor | 1,314 | Visual/interactive AI tutor | 2026-01 |
| ECNU-ICALK/EduChat | 972 | Chinese/English educational LLM | 2025-07 |
| plastic-labs/tutor-gpt | 930 | ToM-based tutor (Bloom) | 2026-02 |
| aaryansamanta/ai-ethos | 499 | Nonprofit multilingual tutoring | 2026-09 |
| pykt-team/pykt-toolkit | 442 | Deep knowledge-tracing benchmark library | 2026-09 |
| riiid/ednet | 384 | Large student-interaction dataset | 2020 |
| Li-Evan/Bloom | 281 | Personal AI tutor | 2026-09 |
| CAHLR/OATutor | 264 | BKT-based open ITS (MIT license) | 2026-10 |
| Ljyustc/SocraticLM | 180 | NeurIPS 2024 Socratic tutor | — |
| GeminiLight/gen-mentor | 131 | WWW'25 multi-agent goal-oriented tutor | 2026-09 |
| zijinz456/OpenTutor | 130 | Local adaptive learning workspace | 2026-10 |
| rosewang2008/edu-convokit | 117 | Education conversation analysis toolkit | 2025-04 |
| eth-nlped/mathdial | 95 | MathDial dataset | 2025-09 |
| iwangjian/Coding-Tutor | 91 | ACL 2025 turn-by-turn verifiers for tutoring agents | 2025-06 |
| eth-lre/PedagogicalRL | 50 | Multi-turn RL tutor alignment | 2025-12 |
| rosewang2008/bridge | 46 | Bridge dataset/code | 2024-07 |
| eth-lre/mathtutorbench | 43 | Benchmark + leaderboard | 2026-08 |
| ArnaudGuiovanna/tutor-mcp | 43 | MCP server wrapping ITS principles | 2026-10 |
| umass-ml4ed/tutorbot-dpo | 14 | AIED 2025 DPO tutor | 2025-08 |
| microsoft/Shiksha-Copilot | 9 | Teacher lesson-plan copilot | 2026-10 |

Note: research code bases are tiny by star count; the popular repos are prompts or generic apps with no learning evaluation.

## 4. Pre-LLM ITS lineage

- Bloom's 1984 "2-sigma problem" (mastery + 1:1 human tutoring ≈ +2 SD) is the field's north star; Plastic Labs named Bloom after it. Not re-fetched; classic reference.
- VanLehn (2011) meta-analysis: step-based ITS d=0.76 vs human tutoring d=0.79, overturning the 2-sigma assumption for human tutors. https://www.tandfonline.com/doi/abs/10.1080/00461520.2011.611369
- Kulik & Fletcher (2016) found g≈0.6 for ITS vs classroom instruction; Ma et al. (2014) g=0.43; Leite et al. (2025) US K-12 meta-analysis of 18 studies/77 effects: g=0.27, smaller in rural schools. https://arxiv.org/abs/2511.04997 , https://www.apa.org/pubs/journals/features/edu-a0037123.pdf
- Cognitive Tutor / Carnegie Learning (CMU, Anderson, Koedinger, Aleven): ACT-R production-rule model tracing and Bayesian knowledge tracing; RAND RCT (Pane et al. 2014) found no year-1 effect and +0.21 SD in year 2 for high schoolers. Lineage continues as MATHia. https://journals.sagepub.com/doi/abs/10.3102/0162373713507480
- AutoTutor (Memphis, Graesser): expectation-and-misconception-tailored natural-language dialogue; ~0.8 SD vs reading a textbook, ~0.5 SD on par with human tutors in a "bystander Turing test"; gains depend heavily on test depth (0.15 shallow, 0.28 deep, 0.64 cloze). https://link.springer.com/article/10.1007/s40593-014-0029-5
- ASSISTments (WPI, Heffernan): homework with immediate feedback and hints; Roschelle et al. 2016 Maine RCT g=0.18 (g=0.29 for low prior achievers), later replicated by WestEd. https://www.sri.com/publication/education-learning-pubs/digital-learning-pubs/how-big-is-that-reporting-the-effect-size-and-cost-of-assistments-in-the-maine-homework-efficacy-study/
- Jill Watson 1.0 (Georgia Tech, 2016) was an IBM-Watson-based forum TA; the 2024 ChatGPT-RAG rebuild is the first LLM-era version with outcome data.
- OATutor (2023) and OpenStax content form the open bridge from BKT-era ITS to LLM-hint experiments (Pardos & Bhandari 2024).

## 5. What the research says works and does not work

1. Guardrails are decisive. Unrestricted ChatGPT boosted practice scores but cut unassisted exam scores 17%; a hint-only variant removed the harm (Bastani, PNAS 2025). Harvard's d≈0.73–1.3 came with strict one-step-at-a-time scaffolding and pre-supplied solutions (Kestin 2025).
2. Engagement, not access, is the binding constraint. Khanmigo users messaged the tutor in 17% of error sessions and gains matched non-AI practice (Oreopoulos & Low 2026); students mostly answer-extract (Kobler et al., ACL 2026); only 9% of Khan users reach the dose at which effects appear. Benchmarks should measure whether a tutor elicits productive use, not just whether it can be pedagogical.
3. Human-AI augmentation is the most consistently positive, cheapest pattern: Tutor CoPilot +4 pp at $20/tutor (Wang 2024); LearnLM-on-Eedi with tutor approval (76% unedited) matched human tutoring; M-Powering Teachers +10–13% uptake (Demszky).
4. Low-resource settings show the largest effects (Nigeria 0.23–0.31 SD; Ghana 0.37; UK GCSE 0.33), but heterogeneity cuts both ways: Nigeria favored higher-baseline students, Taipei favored beginners (+0.215 SD vs ~0).
5. Subject expertise does not translate into pedagogy. MathTutorBench finds an expertise–pedagogy trade-off; GPT-4o gives overly direct feedback and fails to match ITS adaptivity (Borchers & Shou 2025); only 56.6% of GPT tutoring dialogues were error-free (Gupta et al. 2025).
6. Pedagogical post-training works at small scale: LearnLM (+31% preference vs GPT-4o), a 7B RL-trained tutor matching LearnLM (ETH 2025), SocraticLM, tutorbot-DPO, PEARL. Explicit curriculum structure beats model scaling (Tio et al. 2026).
7. LLM-simulated students and LLM judges are unvalidated instruments: prompted student simulators "perform poorly" and are sycophantic (Scarlatos et al. 2026; arXiv 2605.12748). Any benchmark relying on them needs calibration against real learners.
8. Misconception diagnosis remains a blind spot: AI tutors under-detect flawed reasoning behind correct answers, with ~4 false alarms per true detection (Imran & Bulathwela, AIED 2026).
9. Perception is not learning: educators rated LLM tutors above humans on empathy 80% of the time (Pal Chowdhury et al. 2025) and students liked Khanmigo, yet a 69-student physics study found no learning-gain difference vs Google search (https://jtl.uwindsor.ca/index.php/jtl/article/view/10052). Benchmarks need outcome anchors, not just rater preference.
10. Effect sizes for LLM tutors so far (0.06–0.37 SD, Harvard outlier aside) sit inside the pre-LLM ITS range (g 0.27–0.76), so the bar for "better than an ITS" has not clearly been cleared; multi-agent designs add latency/cost without outcome evidence yet (arXiv 2604.24110).

## Flags
- Kestin et al. Scientific Reports DOI not verified (publisher blocked fetch); N=194 and d range taken from secondary summaries consistent across sources.
- World Bank Nigeria and Khanmigo student N not stated in abstracts; voxdev/World Bank pages blocked.
- "Open Tutor" is ambiguous (three candidates listed). OpenStax Kinetic has no LLM-tutor outcome publication found.
- Khanmigo-on-GPT-4 (2023) and Bloom 1984 are from background knowledge, not re-fetched.
- Rori effect size: 0.37 in the current arXiv abstract, 0.36 in Rising Academies press.

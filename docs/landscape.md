# AI Tutor Bench: Landscape Map v0

2026-10-05. Built from six parallel research passes (full reports with URLs in [research/](research/)), roughly 250 sources, prioritizing 2025 and 2026. Items the researchers flagged as unverified stay flagged here. This is a v0 meant to be corrected; the intended end state is structured data rendered on aitutorbench.com and correctable by pull request.

## At a glance

| What | v0 count |
|---|---|
| Tutoring products and modes catalogued | ~85 |
| Named benchmarks and datasets | 35+ |
| Distinct evaluation methods | 12 |
| RCTs or field studies of LLM tutors with learning outcomes | 13 |
| Public leaderboards touching tutoring | 5, all model-level or grading/diagnosis |
| Public head-to-head evaluations of deployed tutoring products on a common protocol | 0 |

## 1. Tutors

Evidence tiers: **E0** none, or vendor-internal claims only. **E1** vendor-run study. **E2** independent quasi-experimental study or small RCT. **E3** independent RCT with standardized outcomes. "Model" is whether the vendor discloses the underlying model.

### 1a. Frontier-lab study modes (detail: [research/01](research/01-frontier-lab-tutors.md))

| Product | Maker | Launched | Mechanics | Model | Evidence |
|---|---|---|---|---|---|
| ChatGPT Study Mode | OpenAI | Jul 2025 | Socratic prompts, hints, checks understanding, withholds answers; opt-in; silently removed from menu Apr 2026, relaunched Aug 2026 | No | E0. 20k-student Tartu–Stanford study announced, no results |
| ChatGPT Edu / College Student plugin | OpenAI | 2024–Aug 2026 | Guided tutoring, quizzes, flashcards from course files | No | E0 |
| Claude Learning Mode | Anthropic | Apr 2025 (edu), Aug 2025 (all) | Socratic questions, asks for evidence; style toggle | No | E0. Usage reports only |
| Gemini Guided Learning | Google | Aug 2025 | Step breakdown, probing questions, quizzes, diagrams, flashcards | Yes (Gemini 2.5/3 with LearnLM training) | E2. Sierra Leone 8-wk RCT, 1,763 students, +0.26 SD math; expert-preference arena |
| NotebookLM Learning Guide | Google | Sep 2025 | Source-grounded probing, quizzes, study guides | Yes | E0 |
| Copilot Learn Live / Study and Learn | Microsoft | Oct 2025 | Voice Socratic tutor with whiteboard; flashcards, quizzes | No | E0 |
| Perplexity Study Mode / Learn Mode | Perplexity | Sep 2025 / Feb 2026 | Level-tailored explanations; lesson modules with self-tests | No | E0 |
| Grok (El Salvador rollout) | xAI | Dec 2025 | "Curriculum-adapted" support for 1M+ students, claimed | No | E0 |
| Doubao Aixue, Qwen Zhixue, Yuanbao, Wenxin | ByteDance, Alibaba, Tencent, Baidu | 2024–26 | Photo-solve, voice teacher, grading, wrong-question tracking; category 120M MAU | Partly | E0 |

Mistral (Vibe) and Meta ship no tutoring mode. Every Western lab launched its "don't just answer" mode between July and October 2025; only Google publishes any evaluation of its own.

### 1b. K-12 math (detail: [research/02](research/02-edtech-and-consumer-tutors.md))

| Product | Maker | Modality | Mechanics | Model | Evidence |
|---|---|---|---|---|---|
| Khanmigo | Khan Academy | Chat + in-exercise hints | Socratic, "never gives the answer"; $4/mo | GPT-4 | E3. 2-yr cluster RCT, 18 schools: +0.06–0.08 SD/yr, same as Khan practice without AI; median student used it in 17% of error sessions |
| Synthesis Tutor | Synthesis | App, manipulatives + voice | Adaptive K-5 | No | E0 |
| MATHia + LiveHint AI | Carnegie Learning | Step-level ITS + LLM hints | Mastery; LiveHint trained on 1.2B problems | No | E3 for MATHia (ESSA Tier 1/2, RAND RCT); LiveHint itself unevaluated |
| Eedi | Eedi (UK) | Diagnostic questions, hints, constrained AI, human tutors | Misconception-targeted via open 8,000-node graph | Gemini 2.0 Flash (LearnLM) | E3. Independent RCT 3,000 students +2–4 months; LearnLM RCT N=165 +5.5 pp; US RCT pending |
| Skye | Third Space Learning | Voice + shared screen | I-do/we-do/you-do; $5k/school/yr | GPT-4o | E0 (pilot data) |
| Rori | Rising Academies | WhatsApp text | Curriculum micro-lessons; ~$5/student/yr | Unclear | E3. Ghana RCT 0.37 SD |
| Wild Zebra | Wild Zebra | Chat, gr 2–9 | Socratic; $48/mo | No | E0 |
| Math Academy | Math Academy | Adaptive sets, no chat | Mastery + spaced repetition; $49/mo | n/a | E0 |
| Sparx Maths | Sparx | Adaptive homework, no LLM | Personalised practice | n/a | E2 correlational: engagement predicts outcomes, access alone does not |
| Mindspark | Educational Initiatives | Adaptive + ChatGPT plug-in | Level-matched | n/a | E3 pre-LLM, Delhi, +0.37 SD |
| Squirrel AI | Squirrel AI (China) | Adaptive centres, 52M students | Knowledge-point diagnosis | Proprietary | E1/E2 (SRI study cited, not retrieved) |

### 1c. Early reading
Amira (ASR oral-reading tutor, 5.5M students, E2: Evidence for ESSA "Promising"), Ello (E0), Microsoft Reading Coach (E0).

### 1d. Homework help and solvers
Gauth (ByteDance, 100M+ downloads), Brainly, Chegg (45% layoffs, pivoting), Photomath, Numerade, Course Hero, Mathos, StudyFetch, Gizmo, QANDA. Discontinued: Google Socratic, Quizlet Q-Chat. All E0. These optimize answer delivery, which is the opposite axis from tutoring and needs to be scored as such.

### 1e. Language learning
Duolingo Video Call, Speak ($100M ARR), Praktika (30M), ELSA (92M), Preply (human + AI), Busuu. Zero independent efficacy evidence for any AI language-tutor feature.

### 1f. Classroom platforms and teacher-configured tutors
MagicSchool (8M educators), SchoolAI (Dot tutor, "1M classrooms"), Flint, Brisk, Humy, Mindjoy, CENTURY; Oak National Aila (teacher-facing, NFER RCT reports autumn 2026). The teacher constrains the bot, which makes "configured tutor" a distinct test condition from open chat.

### 1g. Higher education
Pearson AI Study Tool (3M students, E1), McGraw Hill AI Reader + Learning Coach (built with Kyron), Cengage, Coursera Coach (E1), Nectir, Canvas IgniteAI, CS50 duck (211k users, no RCT), Jill Watson (Georgia Tech, E2).

### 1h. Hybrid human + AI
Tutor CoPilot (Stanford, E3: +4 pp mastery at $20/tutor/yr), Nerdy Live+AI, Preply, Eedi, UK DfE AI Tutoring Pioneers (450k pupils, trials autumn 2026). Institutions buy hybrid; pure-AI tutoring concentrates in consumer apps and emerging markets.

### 1i. AI-first schools and emerging markets
Alpha School / 2 Hour Learning (E0, "10x" from internal MAP data, Houston ISD pilot fall 2026), Arivihan (India, $10M Series A), Byju's (insolvent), Riiid.

### 1j. Research and open-source tutors (detail: [research/03](research/03-research-prototypes-and-rcts.md))
LearnLM (Google), PedagogicalRL 7B (ETH, matches LearnLM on pedagogy), SocraticLM, tutorbot-DPO, PEARL / HeuristicEdu, Tutor-GPT and Honcho (Plastic Labs), OATutor (Berkeley, open BKT ITS), EduChat. The most-starred "tutor" on GitHub is a 29k-star prompt file with no evaluation.

## 2. Evidence: what is actually known about learning outcomes

| Study | Year | Setting | N | Headline |
|---|---|---|---|---|
| Bastani et al., PNAS | 2025 | Turkish HS math, 3 arms | ~1,000 | Unrestricted ChatGPT: practice +48%, unassisted exam −17%. Hint-only tutor: practice +127%, harm removed |
| Kestin et al., Harvard | 2025 | Intro physics, custom GPT-4 tutor vs active learning | 194 | d 0.73–1.3, immediate post-test only, two topics |
| Oreopoulos & Low, Khanmigo | 2026 | 18 Tennessee middle schools, 2 years | ~thousands | +0.06–0.08 SD/yr; +0.14 for full-year active users; 17% of error sessions used |
| World Bank Nigeria | 2025 | 6-wk after-school English with Copilot | n/s | 0.31 SD composite; among most cost-effective programs |
| Rori, Ghana | 2024 | WhatsApp math, 8 months | ~1,000 | 0.37 SD |
| Google + Fab, Sierra Leone | 2025 | Gemini/LearnLM, 8 wks | 1,763 | +0.26 SD math; solution-seeking fell 25% to 10% |
| Tutor CoPilot, Stanford | 2024 | GPT-4 suggestions to human tutors | 1,800 students | +4 pp mastery, +9 pp for weaker tutors |
| LearnLM on Eedi | 2025 | UK classrooms, human-approved AI messages | 165 | +5.5 pp novel problems, comparable to human tutors |
| Medly micro-RCTs | 2026 | GCSE science revision, 4 wks | 929 | g 0.33; 31% attrition |
| Taipei RL tutor | 2026 | Python course, adaptive sequencing | 770 | +0.15 SD; +0.22 for beginners, ~0 for experienced |
| StudentBench, Handshake | 2026 | 1-hour GRE tutoring, 13 AI tutors vs human vs control | 2,383 adults | AI pooled equivalent to human tutors; +6–7 pp over control; Gemma 4 31B at 918x lower cost |
| ETH Italy ESL | 2025 | GPT-4 replaces homework, 8 wks | 76 | Gains higher in one cohort, non-inferior elsewhere |
| Jill Watson, Georgia Tech | 2024 | RAG course TA | multi-course | More A grades (66% vs 62%) |

Context: pre-LLM intelligent tutoring systems meta-analyze at g 0.27–0.76 and human tutoring pools at 0.37 SD. LLM tutors so far (0.06–0.37, Harvard aside) sit inside that range. The two causal findings that matter most for a benchmark: **guardrails decide whether the tutor helps or harms** (Bastani), and **engagement, not model quality, decides whether anything happens at all** (Khanmigo, Sparx, Taipei).

Results landing within 12 months: Oak Aila NFER RCT, DfE Pioneers trials, Eedi US RCT (pre-registered, four arms incl. human tutors), Tartu–Stanford 20k-student ChatGPT study, OpenAI's Learning Outcomes Measurement Suite with Stanford SCALE, Houston ISD Alpha pilot, Khanmigo proactive-help redesign.

## 3. Benchmarks (detail: [research/04](research/04-benchmarks.md))

| Benchmark | Who, year | Unit | Measures | Method | Learners | Leaderboard |
|---|---|---|---|---|---|---|
| TutorBench | Scale AI, 2025 | Raw model, single turn | Explanation, feedback, hints on HS/AP STEM | Rubric + Claude judge | None | Yes, 26 models |
| MathTutorBench | ETH, 2025 | Raw model, turn | 7 tutoring skills, pedagogy vs solving trade-off | Reward model vs teachers | None | Yes |
| MRBench + BEA 2025 | MBZUAI, 2025 | Response | 8 remediation dimensions | Human labels; auto-prediction task | None | Closed |
| StudentBench | Handshake, 2026 | Raw model, 1-hour session | Real learning gain | Pre/post RCT, adults | 2,383 adults | In paper |
| EduClaw-Bench | 2026 | Agent, 30 days | Sustained quality, simulated gain | KT-grounded simulated learner | Simulated | No |
| SafeTutors | 2026 | Model, single + multi-turn | 11 harm dims incl. answer leakage | Probes | None | No |
| TeachBench, KMP-Bench, OpenLearnLM, ELBench, Elmes, OmniEduBench | CN/KR groups, 2025–26 | Model | Pedagogy principles, knowledge, attitude | LLM judge, simulated students | Simulated | No |
| SocraticBench, SID, GuideEval | 2025 | Model | Socratic dialogue success | Simulated student + calibrated judge | Simulated | No |
| TutorGym | AIED 2025 | Model | Step-level ITS actions | ITS traces | None | No |
| TutorMoments | Ai2, 2026 | Model | Scaffolding, rigor, rapport at key moments | Human annotation | Real sessions as context | No |
| LearnLM evals | Google | Model | 29-item pedagogy rubric, expert arena | Human experts | Role-played | No, internal |
| Pedagogy Benchmark | AI for Education | Model | Pedagogical knowledge | MCQ | None | Yes |
| Eedi Kaggle 2024/25 | Eedi | Model | Misconception diagnosis | MAP | None | Yes |
| Vals SAGE | Vals.ai | Model | Grading handwritten math | Rubric | None | Yes |
| Learning Agency board | 2026 | Model | Essay scoring, misconception detection | QWK/MAP | None | Yes |

What they share: every one evaluates raw models, not products. Nearly all score a single turn. Only StudentBench measures real learning (adults, one hour, no retention). Only EduClaw-Bench models a long horizon, and only in simulation. SafeTutors shows failure rates rise from 17.7% single-turn to 77.8% multi-turn, so the single-turn boards overstate quality.

## 4. Methods (detail: [research/05](research/05-methodologies.md))

| Method | Unit | Cost | Evidence of real learning | Status in the field |
|---|---|---|---|---|
| Expert pedagogy rubric, human-rated | Turn or conversation | $5–40/conv | Medium construct validity, outcome validity unproven | Standard (LearnLM, MRBench) |
| LLM-as-judge on pedagogy | Turn or conversation | cents | Works only for decomposed rubrics after kappa validation; "helpfulness" judges fail to separate pedagogical from conversational tutors | Widespread, mostly unvalidated |
| Scripted adversarial student | Session | cents–$ | Tests guardrails, the one thing causally tied to harm | Only in SafeTutors; never across products |
| Simulated student with knowledge model | Session or multi-session | cents–$2 | Low; prompted simulators "perform poorly", fine-tuned ones limited; no sim-to-real gain validation exists | Research only |
| Pairwise preference arena | Matchup | High human cost | Preference tracks fluency and warmth, not learning (educators preferred LLMs on empathy 80% of the time) | Google internal |
| Whole-conversation and longitudinal | Session, days–years | Multiples of turn-level | Exposes collapse that turn-level hides | Rare |
| Engagement, retention, affect | Student-session | Near zero from logs | Necessary gate; perceived engagement does not predict gain | Khan ICAP metric; RCT usage logs |
| Safety and accuracy audits | Product snapshot | $10–50k | Orthogonal to learning | Common Sense Media, DfE standards |
| Learning-science process detectors (answer leakage, guiding questions, uptake) | Turn | Cheap once validated | Mediators; strongest when paired with an RCT (Tutor CoPilot) | Emerging |
| Cost, latency | Request | Near zero | Deployment-blocking, not learning | Ignored by model boards |
| Teacher-facing trials | Teacher | £100k–500k | High for teacher outcomes | EEF |
| Real-learner gain, pre/post, randomized | Student | $10k micro to $1M+ Tier-1 | The criterion | 13 studies; StudentBench shows a 1-hour adult version is feasible at scale |

Credible stacks, per the research: rubric + validated judge + outcome anchor; process detectors + RCT; arena for ranking with RCT for calibration; multi-turn before single-turn; simulators as regression tests never as outcomes; engagement as a gate on any learning claim; safety and cost as pass/fail gates, not averaged into a score.

## 5. Who evaluates today (detail: [research/06](research/06-evaluators-and-gaps.md))

| Who | Rates | Method | Learning outcome? |
|---|---|---|---|
| Common Sense Media / Youth AI Safety Institute | Products (Khanmigo Low risk, Gemini K-12 High, ChatGPT-5 High, Claude Moderate) | Hands-on red-team on 8 principles | No, safety only |
| Education Endowment Foundation (UK) | Edtech via RCTs | Independent trials | Yes, teacher tools so far |
| Evidence for ESSA, What Works Clearinghouse | Programs (Amira, MATHia) | Study-design tiers | Yes, pre-LLM products |
| Digital Promise, 1EdTech, ISTE EdTech Index | Products | Vendor-submitted evidence, certifications | No testing |
| State procurement rubrics (GA, NC, CO, MD, ID) | Products | Checklists | No testing |
| Stanford SCALE, LEVI, Tools Competition, Gates ($400M edu AI) | Research briefs, grants | RCTs, synthesis | Some, one product at a time |
| Journalism, newsletters, parent sites, SEO lists | A handful of prompts | Anecdotal | No |

No site anywhere benchmarks deployed tutoring products head-to-head. Safety ratings and efficacy evidence live in separate silos.

## 6. Coverage matrix: who has been evaluated how

✓ independent, (own) vendor-run, — nothing found.

| Tutor | Turn rubric | Multi-turn stress / answer leakage | Simulated student | Real-learner gain | Independent RCT | Safety audit | Common-protocol head-to-head |
|---|---|---|---|---|---|---|---|
| ChatGPT Study Mode | — | — | — | — | — | ✓ (ChatGPT, not the mode) | — |
| Claude Learning Mode | — | — | — | — | — | ✓ (Claude) | — |
| Gemini Guided Learning | (own) | — | — | (own) Sierra Leone | — | ✓ | — |
| Copilot Learn Live | — | — | — | — | — | — | — |
| Perplexity Learn Mode | — | — | — | — | — | ✓ (Unacceptable, Perplexity) | — |
| Khanmigo | (own) | — | — | ✓ | ✓ | ✓ | — |
| Synthesis Tutor | — | — | — | (own) | — | — | — |
| MATHia + LiveHint | — | — | — | ✓ (MATHia, pre-LLM) | ✓ (pre-LLM) | — | — |
| Eedi | (own) | — | — | ✓ | ✓ | — | — |
| Skye | — | — | — | (own) | — | — | — |
| Duolingo Video Call, Speak, Praktika, ELSA | — | — | — | — | — | — | — |
| MagicSchool, SchoolAI, Flint | — | — | — | (own) | — | ✓ (teacher assistants) | — |
| Pearson, McGraw Hill, Coursera | — | — | — | (own) | — | — | — |
| Alpha School | — | — | — | (own) | — | — | — |
| Raw frontier models via API | ✓ TutorBench, MathTutorBench | ✓ SafeTutors | ✓ EduClaw | ✓ StudentBench (adults) | — | — | ✓ (models only) |

The last column is empty for every product. That column is the benchmark.

## 7. Gaps, merged and ranked by how much a benchmark could change

1. **No head-to-head of deployed products** on identical scenarios. Every board ranks raw models; every product study is one product, vendor-run or years late.
2. **Answer leakage and guardrail integrity are untested across products**, despite being the one factor causally tied to harm (Bastani) and the first question parents ask.
3. **Single-turn scoring hides most failures** (17.7% to 77.8%); no public benchmark scores whole live sessions.
4. **Engagement is the binding constraint and nobody scores it.** A strong model with 17% uptake produced no effect.
5. **No shared student personas.** Benchmarks use static items; none replays the same simulated learners (grade, misconception, motivation, language) across products.
6. **Learning outcomes are absent from leaderboards** except StudentBench (adults, one hour, no retention). Nothing for K-12, nothing delayed, nothing on transfer.
7. **No per-subject, per-grade grid.** TutorBench is HS/AP STEM; AI-for-Education is primary numeracy; nothing covers middle-school math, writing, reading, or languages on one protocol.
8. **Voice is unbenchmarked** while becoming the default modality for language and spreading to math (Skye, Synthesis, Learn Live, Duolingo).
9. **Simulated students are unvalidated instruments**; no fidelity standard gates their use, and no study shows simulated gains predict real gains across tutors.
10. **LLM judges are unvalidated for pedagogy**; helpfulness judges invert rankings between judges; verbosity and politeness inflate scores.
11. **Cost per learning gain** appears only in StudentBench; districts and funders have no price-vs-pedagogy map.
12. **Safety and efficacy are rated by different bodies** and never shown side by side.
13. **Misconception diagnosis-to-remediation loop** is never scored end to end (Eedi scores diagnosis, MRBench scores remediation of a given error).
14. **Language tutors have zero independent evidence** despite the largest consumer revenues in the category.
15. **Configured tutors** (teacher-constrained bots in MagicSchool, SchoolAI, Flint) are a distinct deployment pattern with no test condition anywhere.

## 8. Namespace

"TutorBench" is taken twice (Scale AI's SEAL leaderboard, Oct 2025; HKU's DeepTutor interactive benchmark, Apr 2026). Also live: StudentBench, TeachBench, MathTutorBench, MMTutorBench, CSTutorBench, TutorGym, TutorEval, TutorMoments, EduBench, EduClaw-Bench, ELBench. AI Tutor Bench sits in a crowded namespace and must position on what the others lack: products, whole sessions, learners, outcomes, transparency.

## 9. Correcting this map

Source reports with URLs are in [research/](research/). Known soft spots: Perplexity, OpenAI and Microsoft product pages blocked fetches and rest on secondary coverage; Chinese-market products are thinly verified; Squirrel AI and CENTURY evidence not retrieved; "Open Tutor" is ambiguous; several Asian benchmark institutions are inferred from author affiliations.

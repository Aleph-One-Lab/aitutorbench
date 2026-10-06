# AI Tutor Bench: Strategy v0.1

2026-10-05. Reconciled against the landscape research in [landscape.md](landscape.md) and [research/](research/).

## 0. What the research changed

The pre-research draft assumed a few things that turned out wrong or incomplete:

- **"Nobody measures real learning gain" is false at the model level.** Handshake's StudentBench (Sep 2026) ran 2,383 adults through one-hour GRE sessions with 13 AI tutors, a human-tutor arm and a control. It is still true at the product level and for anyone under 18.
- **The name is taken twice.** Scale AI's TutorBench (model-level, single-turn, SEAL leaderboard) and HKU's DeepTutor TutorBench. Positioning cannot be implicit.
- **The two findings that should shape the benchmark are about guardrails and engagement, not pedagogy quality.** Bastani (PNAS 2025): unrestricted ChatGPT raised practice scores and cut unassisted exam scores 17%; a hint-only variant removed the harm. The Khanmigo RCT: a well-regarded Socratic tutor used in 17% of error sessions produced the same gains as practice without AI. A benchmark that scores only "how pedagogical is the reply when a student engages" misses both.
- **Single-turn scoring masks failure.** SafeTutors: 17.7% failure single-turn, 77.8% multi-turn. Whole sessions are non-negotiable.
- **LLM judges of "helpfulness" do not work for this.** They fail to separate pedagogical from conversational tutors and invert rankings between judges. Decomposed rubrics with deterministic detectors and kappa-validated judges do work.
- **Simulated students are not an outcome instrument.** ACL 2026 work shows prompted simulators perform poorly and fine-tuned ones stay limited. They are regression tests.
- **Voice is a large share of the market** (Skye, Synthesis, Learn Live, Duolingo, Speak, Praktika, ELSA). A text-only harness is a deliberate first step, not the whole thing.
- **A cheap rung-5 exists.** StudentBench's design (recruited adults, one hour, pre/post) is replicable for tens of thousands of dollars, not millions. That makes real-learner calibration a phase-one ambition, not a someday.

## 1. Thesis

AI Tutor Bench evaluates **deployed tutoring products**, over **whole sessions**, with **standardized students**, against **learning-grounded measures**, on a **common protocol**, and publishes **every transcript**. Nothing on the map does more than two of those.

## 2. Two numbers, not twelve

**Integrity** (launch metric). Pass rate across a fixed battery of adversarial sessions, with sub-scores:

| Sub-score | What the scripted student does | Detector |
|---|---|---|
| Answer-leakage resistance | Pushes for the answer, escalating over turns | Deterministic: does the final answer appear verbatim or trivially |
| Wrong-answer resistance | Asserts an incorrect answer with confidence | Does the tutor confirm it (sycophancy) |
| Scaffold persistence | Behaves normally for 10+ turns | Turn index at which the tutor collapses to lecturing or answer-giving |
| Misconception noticing | Reasons correctly to a right answer via a known misconception (the "correct answer trap") | Does the tutor catch it |
| Off-task handling | Drifts to unrelated or inappropriate requests | Does the tutor redirect |
| Factual accuracy | Normal session | Error rate against worked solutions |

Each sub-score is legible on its own ("Study Mode gives the answer after three asks; Khanmigo does not"), and together they test the only thing causally tied to harm.

**Gain** (north star). Learning gain per hour with real learners on a fixed skill, pre/post, with a one-week delayed post-test, reported with usage distributions rather than means.

Everything else is reported, never averaged in: pedagogy rubric scores, simulated-student gain, cost per session, latency, safety tier (Common Sense), evidence tier (from the map).

## 3. Positioning against the field

| | Scale TutorBench | MathTutorBench | StudentBench | EduClaw-Bench | Common Sense | **AI Tutor Bench** |
|---|---|---|---|---|---|---|
| Unit | Raw model | Raw model | Raw model | Agent | Product | **Product** |
| Turns | 1 | 1 | ~1 hour | 30 days simulated | Snapshot | **Whole session, multi-session later** |
| Learners | None | None | Adults | Simulated | None | **Scripted → simulated → real** |
| Outcome | Rubric | Reward model | Real gain | Simulated gain | Safety tier | **Integrity now, real gain as anchor** |
| Transcripts public | No | Partial | Partial | No | No | **All** |
| Refresh | Static | Static | One-off | One-off | Periodic | **Quarterly, rotating scenarios** |

## 4. Launch scope

**Subject: middle-school math (grades 6–8).** Eedi's open 8,000-node misconception graph gives a ready scenario seed. It is the setting of the Khanmigo RCT and most of the ITS literature. Mastery criteria are clear. Expand to writing feedback and early reading after.

**Products, wave 1**, all reachable from a consumer account:
ChatGPT Study Mode, Claude Learning Mode, Gemini Guided Learning, Copilot Study and Learn (text path), Perplexity Learn Mode, Khanmigo ($4/mo). Plus baselines: the same frontier models with no study prompt, and a generic published Socratic system prompt. The baselines answer the question every lab's launch post implies and none has published: does the study mode actually do anything.

**Wave 2** (school accounts or partnerships): Synthesis, Skye, MATHia LiveHint, Eedi, SchoolAI and MagicSchool configured tutors.
**Wave 3**: voice (Learn Live voice, Skye, Synthesis, Duolingo).

**Scenario bank**: roughly 60 scenarios from 12 misconceptions × 5 student personas (confident-wrong, frustrated, answer-seeker, minimal-effort, off-task). Each persona is a scripted policy that uses an LLM only for surface wording, so runs are reproducible. Scenarios rotate quarterly to resist overfitting.

**Harness**: drive products through their real interfaces with browser automation, record full transcripts, publish them with the scores. This is tooling we already build and it is the moat; nobody else has published it because nobody else wants to maintain it.

## 5. Roadmap

| Phase | Weeks | Deliverable | Why this order |
|---|---|---|---|
| 0. Map | 2–3 | [landscape.md](landscape.md) as structured data rendered on aitutorbench.com, with a "pending evidence" tracker for the dozen results due in the next 12 months | Content before scores; builds the audience and the correction loop |
| 1. Integrity v0 | 4–6 | Harness + scenario bank + detectors; wave-1 products and baselines; full transcripts published | The launch. Buildable now, immediately legible, tests the causal factor |
| 2. Simulated-student engine | 6–8 | Knowledge-tracing-grounded or fine-tuned simulators with a fidelity gate; used for breadth and regression across releases, with sim-to-real validation reported | Scales coverage; honest about what it is |
| 3. Gain v0 | ~12 | StudentBench-style one-hour pre/post with recruited learners on wave-1 products, adults first then teens via a partner, delayed post-test at one week; publish the correlation between Integrity, simulated gain, and real gain | Turns the proxies into a benchmark. A benchmark that publishes its own validity coefficient is rare |
| 4. Live | ongoing | Quarterly re-runs, rotating scenarios, teacher/student arena on published transcripts, cost-per-gain frontier chart | Resists gaming and product churn (Study Mode vanished and reappeared in 2026) |

## 6. Why each audience would care

- **Parents**: the first systematic answer to "does it just give the answer", per product.
- **Districts**: safety tier, evidence tier and integrity score side by side, which no evaluator currently offers.
- **Labs**: a product-level ranking they cannot credibly produce themselves; every lab's eval so far is self-run against rivals' older models.
- **Funders** (Gates $400M, DfE £49M, Renaissance/LEVI): the independent instrument their programs lack.
- **Press**: head-to-head with transcripts is a story; the only existing comparisons are blog posts with a handful of prompts.

## 7. Risks

- **Terms of service** for automated use of consumer products. Check per product; use APIs where they exist; document method where they do not.
- **Judge circularity**: frontier models judging frontier-model tutors. Mitigate with deterministic detectors for the Integrity sub-scores, a human-labelled calibration set of at least 200 conversations, and the Phase 3 validation.
- **Name collision**: say "products, sessions, learners, outcomes" in the first sentence of the site.
- **Product churn**: modes change silently. Date-stamp every run and keep old transcripts.
- **Cost**: price a wave-1 run before committing to quarterly cadence.
- **Perception**: "another tutor bench" unless the product-level head-to-head is visible on day one.

## 8. Decisions needed

1. Confirm the launch subject (middle-school math) and the wave-1 product list.
2. Build the map as structured YAML in the repo and render it on the site now, or publish the markdown first.
3. Appetite for Phase 3: rough budget $10–30k for ~1,000 participant-hours.
4. Early outreach for credibility and data: Eedi (misconception graph), Stanford SCALE, LEVI, Common Sense's institute.

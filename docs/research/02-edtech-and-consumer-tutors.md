# AI Tutor Landscape: EdTech, Consumer and School Products (as of Oct 2026)

Scope: non-frontier-lab products only. ~65 products checked; grouped into 8 categories. "Internal" = vendor-reported, not independently reviewed. Items marked *unverified* could not be confirmed from primary sources in this pass.

## 1. K-12 math tutors

| Product | Company | Modality | Pedagogy | Scale | Efficacy evidence |
|---|---|---|---|---|---|
| [Khanmigo](https://www.khanmigo.ai/learners) | Khan Academy | Chat + speech-to-text, in-exercise hints | Socratic, "never gives the answer"; GPT-4 (disclosed); $4/mo | ~2M users, 795 US districts / 770k students (reported, [secondary](https://aiforcause.org/stories/khanmigo-ai-tutor)) | 2-yr cluster RCT, 18 Tennessee middle schools ([Oreopoulos & Low 2026](https://edworkingpapers.com/sites/default/files/ai26-1551.pdf)): +0.06–0.08 SD/yr, similar to Khan practice without AI; median student messaged Khanmigo on 1/3 of practice days and in 17% of error sessions. Khan says only ~15% of eligible students use it; redesign with proactive help summer 2026 ([Chalkbeat](https://www.chalkbeat.org/2026/08/25/ai-tutoring-students-khanmigo-khan-academy-engagement-study/)) |
| [Synthesis Tutor](https://www.synthesis.com/educators) | Synthesis | App: manipulatives + conversational tutor | Adaptive, step-by-step on errors; K-5; model undisclosed | 68,202 students (site) | Internal only: "98% of teachers report improved skills" |
| [MATHia + LiveHint AI](https://www.carnegielearning.com/why-cl/research/) | Carnegie Learning | In-app adaptive tutoring (symbolic+ML); LiveHint AI chat hints | Step-level mastery; LiveHint LLM "trained on 5.5M students / 1.2B problems", base model undisclosed ([announcement](https://aithority.com/machine-learning/carnegie-learning-announces-livehint-ai/)) | Large US install base | ESSA Tier 1 (blended curriculum), Tier 2 (MATHia alone); RAND RCT ~18k students; LiveHint AI itself unevaluated |
| [Eedi / Eedi Labs](https://www.eedi.com/news/new-uk-study-finds-students-using-eedi-gain-2-4-months-of-additional-maths-progress) | Eedi (UK) | Diagnostic questions, hints, human chat tutors; constrained AI tutor | Misconception-targeted (8,000-node open Misconception Graph) | 120M+ responses; Imagine Learning US curriculum partnership (Jan 2026) | Independent RCT, 20 schools / 3,000 students: +2–4 months progress; [Google LearnLM RCT](https://arxiv.org/html/2512.23633) (N=165, Gemini 2.0 Flash fine-tune, human-supervised): transfer 66.2% vs 60.7% human tutors, 0.1% factual errors; US RCT via Accelerate pending |
| [Skye](https://thirdspacelearning.com/us/math-tutoring/ai-math-tutor/) | Third Space Learning (UK) | Voice + shared screen (not chat) | I-do/we-do/you-do, CRA, ZPD; GPT-4o (disclosed in blog) | 200+ schools on Skye; £4.4M raised 2026; $5k/school/yr | Pilot data only (better post-session scores); no formal study |
| [Rori](https://arxiv.org/pdf/2402.09809) | Rising Academies | WhatsApp text | Curriculum-aligned micro-lessons | Ghana, Liberia; ~$5/student/yr | Cluster RCT, 637 students / 11 schools: ES 0.36 |
| [Wild Zebra](https://www.geekwire.com/2026/this-startup-just-raised-6m-for-an-ai-tutor-that-helps-kids-figure-it-out-themselves/) | Wild Zebra (Seattle) | Chat, math + reading, gr 2-9 | Socratic questioning | Tens of thousands of students; $6M seed (2026); $48/mo families | Internal pilot: +4–8 pp (gr 5-6) |
| [Math Academy](https://www.mathacademy.com/) | Math Academy | Adaptive problem sets; no LLM chat | Mastery + spaced repetition ("Fractional Implicit Repetition"); $49/mo | Undisclosed | Claims "4x speed"; no independent study |
| [Sparx Maths](https://sparxmaths.com/impact/) | Sparx Learning (UK) | Adaptive homework + videos; no LLM tutor | Personalised practice | 146,806 pupils / 889 schools in 2025 analysis | Cambridge/RAND Europe correlational: engagement predicts outcomes, access alone does not |
| [Mindspark](https://www.povertyactionlab.org/evaluation/disrupting-education-experimental-evidence-technology-aided-instruction-india) | Educational Initiatives (India) | Adaptive practice; ChatGPT plug-in added | Level-matched adaptive | India; J-PAL/GIF backed | RCT (Delhi, 619 students, 4.5 months): +0.37 SD math, +0.23 SD Hindi |
| [Squirrel AI](https://time.com/collection/time100-most-influential-companies/2026/squirrel-ai-learning/) | Squirrel AI (China) | Adaptive system in learning centres; "large adaptive model" | Knowledge-point diagnosis | 52M students, 60k centres; US entry 2026 | SRI peer-reviewed study cited by TIME (not retrieved here) |
| DreamBox, IXL, Zearn, Thinkster | Various | Adaptive practice; no generative tutor documented | Mastery/adaptive; Thinkster adds human coach | Large US install bases | Pre-LLM efficacy literature; nothing on AI-tutor features |

## 2. Early reading / literacy

| Product | Company | Modality | Pedagogy | Scale | Efficacy evidence |
|---|---|---|---|---|---|
| [Amira](https://amiralearning.com/) | Amira Learning | Listens to oral reading (ASR), micro-interventions | Science-of-reading tutoring + assessment, K-5 (EN/ES) | 4,000+ schools, 5.5M students (site) | [Evidence for ESSA "Promising"](https://fcrr.org/repository/amira), ES +0.64 (n=178, affluent district); quasi-experimental DIBELS small positive; [EdWeek Nov 2025](https://www.edweek.org/technology/ai-tutors-are-now-common-in-early-reading-instruction-do-they-actually-work/2025/11) notes evidence still limited |
| [Ello](https://www.ello.com/) | Ello | ASR reading coach, ages 4-9, now also math | Decodable books, leveled | $15M Series A (2023); user count not current | Internal: "88% read more after 4 weeks" |
| Lexia, Newsela | Lexia Learning, Newsela | Adaptive literacy; Newsela AI-levels texts | No Socratic tutor | Large K-12 bases | No AI-tutor evidence |

## 3. Homework help and solver apps (consumer)

| Product | Company | Modality | Pedagogy | Scale | Efficacy evidence |
|---|---|---|---|---|---|
| [Gauth](https://flowith.io/blog/5-reasons-gauth-most-downloaded-education-app-2026/) | ByteDance | Photo-solve + chat; "personalized course" (Aug 2026) | Step-by-step answers; 95% solve-rate claim | 100M+ downloads; #1 US education downloads Q3 2025 | None |
| [Brainly](https://apps.apple.com/us/app/brainly-your-personal-tutor/id745089947) | Brainly | AI tutor + scan + community + human tutor | Step explanations with citations | 350M users (company claim) | None |
| [Chegg](https://www.sfchronicle.com/tech/article/chegg-layoffs-ai-bay-area-21124921.php) | Chegg | Solution Scout, step explainer | Expert-worked solutions + AI | 3.2M subs (Q1 2025, -31%); 45% layoffs Oct 2025; pivot to Chegg Skills/Busuu | None |
| [Photomath](https://en.wikipedia.org/wiki/Photomath) | Google | Camera solver | Worked steps; Gemini integration *unverified* | Mass-market | None |
| Socratic | Google | — | — | **Discontinued**; folded into Lens 2024-25 | — |
| Quizlet Q-Chat | Quizlet | — | — | **Discontinued mid-2025** (third-party reports; *unverified directly*) | — |
| [Numerade Ace](https://www.numerade.com/blog/announcements/ai-tutor-ace-improves-learning-outcomes-for-students/) | Numerade | Video explanations, "Ace Podcasts" | Worked video | Active (app updated Jun 2026) | Internal blog only |
| Course Hero | Learneo | AI homework helper | Q&A | Active (updated Sep 2026) | None |
| [Mathos AI](https://www.mathos.ai/) | Mathos (YC W24) | Solver + real-time tutor + video generation | Error-catching coaching, prerequisite gaps | Undisclosed | None |
| [StudyFetch (Sparky)](https://www.studyfetch.com/) | StudyFetch | Upload notes → tutor, flashcards | Content-grounded Q&A | 8M+ users (site) | Internal survey (n=1,000): "92% grade improvement" |
| [Gizmo](https://www.prnewswire.com/news-releases/gizmo-raises-22-million-series-a-to-make-learning-addictive-for-13-million-learners-worldwide-302741943.html) | Gizmo (London) | Gamified flashcards/AI | Spaced repetition, streaks | 13M learners; $22M Series A Apr 2026 | None |
| [QANDA](https://en.wikipedia.org/wiki/QANDA) | Mathpresso (Korea) | Photo-solve + AI tutor | Steps | 90M registered, 8M MAU | None |
| [Doubao Aixue, Qwen Zhixue, Zuoyebang, Yuanfudao](https://hellochinatech.com/p/china-ai-education-120-million-users-zero-revenue) | ByteDance, Alibaba, et al. | Voice "phone-call" tutor; photo-solve; virtual blackboard | Question-bank grounded | Category 120M MAU (+340% YoY, late 2025); free, no monetization | None |
| Sizzle | Sizzle AI | — | — | sizzle.ai unreachable Oct 2026; status *unclear* | — |

## 4. Language learning

| Product | Company | Modality | Pedagogy | Scale | Efficacy evidence |
|---|---|---|---|---|---|
| [Duolingo Max / Video Call with Lily](https://investors.duolingo.com/news-releases/news-release-details/duolingo-launches-ai-powered-video-call-android) | Duolingo | Voice/video roleplay, Explain My Answer | Adaptive conversation length; OpenAI models at launch, current model undisclosed | 8 languages on iOS; expanding to Super tier (May 2026) | Duolingo publishes efficacy studies for core product; none found for Video Call |
| [Speak](https://www.forbes.com/sites/rashishrivastava/2025/11/12/this-startup-is-racing-duolingo-to-replace-human-language-tutors-with-ai/) | Speak | Voice-first lessons + free talk | Speaking drills, feedback | $162M raised, $1.17B valuation, $100M ARR, 15M downloads, 6 languages | None published |
| [Praktika](https://praktika.ai/) | Praktika | Avatar video tutors | Conversation + corrections | 30M+ learners (site); ~$8/mo | None |
| [ELSA Speak](https://elsaspeak.com/en/) | ELSA | Pronunciation ASR + AI roleplay | Phoneme feedback | 92M+ users (site); $60M raised | Internal surveys only |
| [Preply](https://preply.com/en/blog/preply-announces-new-ai-powered-features-to-guide-the-future-of-personalized-learning-in-a-human-ai-world/) | Preply | Human tutors + AI Lesson Insights, Daily Exercises, Scenario Practice | Human-led, AI between lessons; OpenAI partner | $150M Series D Jan 2026, $1.2B valuation | None |
| Busuu | Chegg | AI coaching + human tutors (workplace pilot Sep 2026) | Mixed | Pilot | None |

## 5. Whole-school / classroom AI platforms

| Product | Company | Modality | Pedagogy | Scale | Efficacy evidence |
|---|---|---|---|---|---|
| [MagicSchool](https://valueaddvc.com/pulse/magicschool-ai-edtech-63m-funding-2026) | MagicSchool | 80+ teacher tools, 50+ student tools, Raina chatbot | Teacher-assigned rooms | 8M educator sign-ups, 160 countries; ~$65M raised | None |
| [SchoolAI](https://schoolai.com/) | SchoolAI | Spaces + Dot tutor, Mission Control monitoring | Teacher-designed, interest-adaptive | "1M classrooms"; ~$25M raised; Dayton contract $78,650/yr | Self-described ESSA Level III: 13,882 conversations, "28% critical-thinking boost" (internal) |
| [Flint](https://www.alleywatch.com/2025/11/flint-ai-powered-personalized-adaptive-learning-k12-education-platform-sohan-choudhury/) | Flint | Teacher-built AI activities + tutor | Scaffolded, rubric-graded | 400k users; $15M Series A Nov 2025; $3k–6.5k/school | None |
| Brisk Teaching | Brisk | Chrome extension; primarily teacher-facing | Feedback, leveling | 600k+ teachers; ~$20M raised | None |
| [Humy](https://www.humy.ai/) | Humy | Chat/voice with 1,200+ cited historical figures | Interview, debate, simulation | 86k users, 90 institutions | None |
| [Mindjoy](https://www.mindjoy.com/) | Mindjoy (ZA/US) | AI tutors + auto-assessment | Mastery pathways | Undisclosed | None |
| [Aila](https://educationendowmentfoundation.org.uk/news/new-trial-ai-powered-lesson-planning) | Oak National Academy (UK gov) | Teacher lesson-planning assistant (not a student tutor) | Curriculum-grounded | Free, England | NFER RCT, 450 teachers / 86 schools, reports autumn 2026 |
| [Nolej](https://nolej.io/) | Nolej | Content → activities generator (teacher-facing) | — | 170k users | None |
| Merlyn Mind | Mynd.ai | Classroom voice assistant | — | **Acquired** by Mynd.ai Sep 2025 | — |
| [CENTURY](https://www.century.tech/) | Century Tech (UK) | Adaptive "nuggets"; no generative tutor shown | Adaptive sequencing | 70 countries; $12.2M raised | EEF-funded evaluation exists; result *not verified here* |

## 6. Higher-ed courseware and LMS

| Product | Company | Modality | Pedagogy | Scale | Efficacy evidence |
|---|---|---|---|---|---|
| [AI Study Tool](https://www.pearson.com/en-us/higher-education/products-services/aistudytool.html) | Pearson | Chat in MyLab/Mastering, Revel, Pearson+ | Step explanations, summaries, practice; model undisclosed | 3M+ students with access | Internal: "90% more likely proficient"; 3% paste-to-cheat rate |
| [AI Reader + Learning Coach](https://investors.mheducation.com/news/news-details/2026/McGraw-Hill-Introduces-New-AI-Capabilities-in-Its-Connect-Digital-Course-Solution-for-Higher-Education/default.aspx) | McGraw Hill (Coach built with Kyron Learning) | Highlight-to-explain; Learning Coach video+text conversational tutor (Apr 2026) | Guided questioning, instructor-assigned | AI Reader 45M interactions since fall 2024 | None published |
| Kyron Learning | Kyron | Video-based conversational tutor | Pre-recorded teacher + LLM | Standalone K-12 product *unverified*; now higher-ed partnerships | None |
| Cengage Student Assistant | Cengage | Chat in MindTap | — | Details *unverified* (page 404) | None |
| [Coursera Coach](https://www.reworked.co/learning-development/coursera-closes-25b-udemy-merger/) | Coursera (+Udemy, merger closed May 2026) | Chat Q&A, summaries, role-play | Course-grounded | 290M learners combined | Internal: ~10% quiz pass-rate lift |
| [Nectir](https://finance.yahoo.com/news/ai-reshapes-higher-education-nectir-174000033.html) | Nectir | Course-specific AI assistants | Instructor-configured | 80k students, 100+ campuses, California Community Colleges; $12.5M Series A Mar 2026 | None |
| [IgniteAI](https://www.instructure.com/igniteai) | Instructure (Canvas) | Educator tools + agent; no dedicated student tutor shown | — | Canvas base | None |

## 7. Hybrid human + AI tutoring

| Product | Company | Modality | Pedagogy | Scale | Efficacy evidence |
|---|---|---|---|---|---|
| [Live + AI](https://www.edtechinnovationhub.com/news/varsity-tutors-launches-liveai-to-link-human-tutoring-with-always-on-ai) | Nerdy / Varsity Tutors | Human high-dosage tutoring + 24/7 AI, 40+ teacher tools | AI between sessions | Launched Oct 2025; nationwide | CEO claim "double proficiency growth" (unverified) |
| [Tutor CoPilot](https://arxiv.org/abs/2410.03017) | Stanford (Wang, Demszky, Loeb) with FEV Tutor | LLM suggestions to human tutors in real time | Expert-move prompting | $20/tutor/yr; FEV Tutor itself closed early 2025 (reported) | RCT 900 tutors / 1,800 students: +4 pp mastery, +9 pp for lower-rated tutors |
| [Tutor.com](https://www.tutor.com/) | Princeton Review | Human tutors only | — | 4,000+ tutors | No AI tutor product found |
| [DfE AI Tutoring Pioneers](https://www.edtechinnovationhub.com/news/uk-government-launches-ai-tutoring-pioneers-programme-to-reach-450000-disadvantaged-students) | UK Department for Education | Teacher co-created AI tutors, Years 9-11 | Curriculum-aligned | Target 450k disadvantaged pupils; trials from autumn 2026, tools by end 2027; £23M testbeds | Evaluation pending |

## 8. AI-first schools and emerging-market exam prep

| Product | Company | Modality | Pedagogy | Scale | Efficacy evidence |
|---|---|---|---|---|---|
| [Alpha School / 2 Hour Learning / Timeback](https://en.wikipedia.org/wiki/Alpha_School) | Alpha / Trilogy-linked | 2 hrs/day adaptive apps (IXL, Khan, Amplify + proprietary) with "guides" | Mastery, no teachers | 13 campuses; tuition $10k–75k; HISD pilot at 2 campuses fall 2026 ($500k/school); most charter applications denied | Claims "up to 10x" from internal MAP analysis; [not independently verified](https://nepc.colorado.edu/blog/fprice-kids-pay) |
| [Arivihan](https://inc42.com/buzz/arivihan-nets-10-2-mn-to-scale-its-ai-tutoring-platform/) | Arivihan (India) | Fully automated video lectures + doubt resolution | Exam prep (state boards, CBSE, NEET) | "Several lakh" students, 80% tier-3/rural; $10.2M Series A Sep 2026 (Accel, Prosus) | None |
| Byju's Wiz | Byju's | — | — | **Insolvent** since Oct 2024; zero employees reported 2026 | — |
| Riiid | Riiid (Korea) | Adaptive test prep, math LLM | Score prediction | US push | Pre-LLM Kaggle/TOEIC work |

Not confirmed active: Fermat, Tutello (no primary source located). Prof Jim redirects to Creatium, now an enterprise training product.

## Notable trends and gaps

- **Engagement, not access, is the binding constraint.** The only large LLM-tutor RCT (Khanmigo) found gains indistinguishable from non-AI practice because students barely used the tutor; Sparx finds no effect of access alone; Khan is moving to proactive intervention. A benchmark should score how a tutor earns engagement, not just response quality.
- **The strongest evidence is still pre-generative or low-tech.** Effect sizes of 0.36–0.37 SD come from Rori (WhatsApp, Ghana) and Mindspark (adaptive, Delhi); ESSA Tier 1/Promising ratings belong to MATHia and Amira. LLM tutors have small-N or modest results (Eedi/LearnLM N=165; Tutor CoPilot +4 pp). Alpha School's "10x", Synthesis's "98%", SchoolAI's "28%" are internal.
- **Consumer homework-help economics collapsed.** Chegg cut 45% of staff; Q-Chat and Socratic were discontinued; ByteDance's Gauth and China's Doubao Aixue serve 100M+ users for free with no monetization. Expect answer-giving solvers and Socratic tutors to be judged on very different axes.
- **Voice is becoming the default for language and spreading to math.** Skye, Doubao Aixue, Duolingo Video Call, Speak, Praktika, ELSA and Synthesis are voice-first; a text-only benchmark will miss most of the consumer market.
- **Institutions buy hybrid, not pure AI.** Nerdy Live+AI, Preply, Eedi, Third Space, Tutor CoPilot and the DfE programme all keep a human in the loop; pure-AI tutoring is concentrated in consumer apps and emerging markets (Arivihan, Rori).
- **Model disclosure is rare.** Only Khanmigo (GPT-4), Skye (GPT-4o), Eedi/LearnLM (Gemini 2.0 Flash) and Preply (OpenAI) name their models; most vendors say "proprietary" or "trained on our data". Benchmark metadata should record disclosed vs undisclosed.
- **Teacher-tool platforms are converging on teacher-mediated student tutors** (MagicSchool, SchoolAI Spaces/Dot, Flint, Brisk), where the teacher constrains the bot. This "configured tutor" pattern differs from open chat and deserves its own test condition.
- **Governments are now builders and evaluators**: UK DfE pioneers (trials autumn 2026), Oak Aila NFER RCT (autumn 2026), Houston ISD Alpha pilot, Accelerate's US Eedi RCT. Several results will land within 12 months.
- **Gap: zero independent efficacy evidence for AI language tutors** despite Speak ($100M ARR), Praktika (30M), ELSA (92M) and Duolingo Video Call.
- **Gap: answer-leakage and off-task behaviour are unmeasured in public.** Khanmigo students sent "bare answers"; Pearson reports 3% paste attempts; LearnLM needed human review to reach 0.1% factual errors. A tutor benchmark should test resistance to answer extraction and handling of off-task prompts.

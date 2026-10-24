---
---

<div class="syllabus-page" markdown="1">

# CS 4501-003: Data Privacy

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

<p class="syllabus-subtitle">Fall 2026 syllabus | Updated October 23, 2026</p>

## Course information

| Item | Details |
|---|---|
| Course | CS 4501-003, Special Topics in Computer Science: Data Privacy |
| Instructor | [Tianhao Wang](https://tianhao.wang) |
| Email | [tianhao@virginia.edu](mailto:tianhao@virginia.edu) |
| Meetings | Tuesdays and Thursdays, 2:00-3:15 PM |
| Classroom | Olsson Hall 011 |
| Term | August 25-December 8, 2026 |
| Office hours | Instructor after each class, 3:30-4:30 PM; TA by appointment |
| Public course site | [tianhao.wang/f26-dataprivacy](https://tianhao.wang/f26-dataprivacy/) |
| Canvas | [canvas.its.virginia.edu/courses/190753](https://canvas.its.virginia.edu/courses/190753) |

Canvas is the authoritative source for announcements, release bundles,
submissions, grades, and any date changes. The public site contains the durable
course description, schedule, assignment structure, and policies.

Use Canvas Inbox or email for questions involving grades, accommodations, or
other private matters.

## Course description

How can we use data to build useful systems without exposing the people behind
the data? This course studies concrete privacy attacks, practical defenses, and
the engineering contracts that connect privacy claims to data, code,
configuration, accounting, and tests.

We begin with privacy attacks, then study ML security threats and defenses
before returning to anonymization and its limits. We then develop differential
privacy and privacy-utility trade-offs, private
machine learning, synthetic data, and privacy-enhancing technologies including
secure multi-party computation, homomorphic encryption, trusted execution
environments, and oblivious RAM. The course is designed for
undergraduates with the preparation listed below and emphasizes technical
judgment, reproducible evidence, and clear communication rather than
graduate-level novelty.

## Learning objectives

By the end of the course, students should be able to:

1. distinguish major privacy attacks and evaluate whether an experiment
   supports a claimed privacy failure;
2. formulate threat models, protected units, adjacency relations, and release
   boundaries for data and machine-learning systems;
3. explain and apply differential privacy mechanisms, composition, privacy
   accounting, and privacy-utility analysis;
4. trace a privacy claim through sampling, optimization, preprocessing,
   configuration, code, and tests;
5. design and evaluate an innovative, scoped privacy contribution using
   reproducible evidence;
   and
6. communicate conclusions, uncertainty, residual risks, and the role of AI
   assistance in technical work.

## Background and preparation

This course is open to all undergraduates who have the following preparation:

Required background:

- Completion of an introductory programming course plus at least one 2000-level
  computing course, or equivalent programming experience.
- Basic probability and statistics, including distributions, averages, and
  simple evaluation metrics.
- Comfort working with AI assistants while checking their claims against code,
  data, and tests.

No prior coursework in privacy, cybersecurity, machine learning, cryptography,
or AI is required.

At UVA, CS 3710 (Introduction to Cybersecurity) is especially useful preparation
for threat modeling and attacks. CS 4774 (Machine Learning) also connects to
parts of the material. Neither is a prerequisite.

The optional [readiness self-check](readiness.html) illustrates the programming,
probability, and ML ideas used in the first weeks. It is ungraded, does not
determine eligibility to enroll, and includes guidance for reviewing any gaps.

## How the course works

The course combines four forms of work:

- Lectures and short practicals introduce attacks, mechanisms, systems, and
  evaluation methods.
- Four equally weighted labs cover privacy attacks on LLMs, adversarial
  attacks on image and text models, private releases with real DP libraries,
  and privacy-enhancing technologies. Required systems include JAX Privacy,
  Google DPSynth, and MP-SPDZ. All labs are individual.
- A team or individual project asks students to make an innovative privacy
  contribution as a system, focused tool, attack, defense, monitor/auditor, or
  research paper.
- Two individual, in-class, closed-book paper quizzes check conceptual and
  applied reasoning. Short individual exit surveys are submitted through Canvas
  across the semester.

Guest lectures connect course mechanisms to industry privacy practice and
recent academic work. Students should expect
to read short technical material before selected meetings and to work with
small CPU-compatible code bundles outside class.

## Assessment and grading

| Component | Weight | Basis |
|---|---:|---|
| [Labs](lab.html) | 40% | Four labs worth 10% each; selected labs use hidden cases |
| [Project](project.html) | 30% | Project pitch 10%, proposal 5%, poster/demo 10%, final report 5% |
| Quizzes | 20% | Two individual, in-class, closed-book paper quizzes at 10% each |
| Exit surveys | 10% | Short individual Canvas submissions graded for completion |
| Total | 100% | |

Final letter grades use the standard [UVA grading scale](https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=1153c16fdba41f444f32fb671d961934).

### Labs

All labs are completed individually. They deliberately use different work
products: privacy experiments on supplied GPT models, adversarial attacks on
image and text models, a private-release notebook built on JAX Privacy and
DPSynth, and a private-computation artifact.

| Lab | Weight | Release week | Due week |
|---|---:|---:|---:|
| Privacy attacks on LLMs | 10% | 3 | 5 |
| Adversarial attacks | 10% | 5 | 9 |
| Two ways to release a sensitive dataset | 10% | 9 | 12 |
| Compute Without Seeing | 10% | 12 | 15 |

#### Lab 1: Privacy attacks on LLMs

Run the supplied GPT models to study training-data extraction and memorization.
For membership inference, train a small classifier and shadow
model on synthetic data, compare confidence-based and learned methods, and
implement threshold counts and ROC evaluation, including low-FPR metrics.
Hidden evaluation runs the same MIA and ROC functions on new classifier
instances, with different data, seeds, sample counts, and row order.

The 10 regular points cover the CTF warm-up (2) and classifier MIA (8).
AI assistance is allowed. The warm-up awards 1 point for the flag and
1 point for the two-model loss comparison with evidence.

Classifier MIA includes target/shadow training (1), confidence baseline (1),
learned classifier (2), threshold counts and rates (1), ROC evaluation (1), design philosophy (1),
and method performance (1). In 3-5 sentences, explain the method's design,
shadow-data validation, and a failure mode considered.
On the supplied data and settings, each target/shadow model should reach
95% train accuracy and 70% test accuracy. Each membership method earns its
full 0.5 performance points at AUC >= 0.60; credit increases linearly from
0 at AUC 0.50 to 0.5 at AUC 0.60. Correct implementation and evaluation code
are graded separately from method performance. Low-FPR TPR must be reported,
but has no minimum performance threshold. The notebook summarizes grading.
Keep total target, shadow, and membership-classifier training within 10 minutes
on a standard Colab CPU runtime; no GPU is needed.
Hidden evaluation reuses these functions on similar, unpublished synthetic
datasets. Improve the existing methods using shadow data, without fitting on
target membership labels or hard-coding visible examples. The top five earn
a separate +2 AUC bonus, ranked by the higher of the two methods' mean AUC
across all hidden datasets. A method must return valid scores on every dataset.
Ties use that method's mean TPR at FPR <= 1%, then the design philosophy.
ROC checks count toward the existing implementation points.

The training-inference bonus awards +2 to the five strongest explanations of
how a supplied GPT was trained, judged by evidence, experiment, and reasoning.
Include a reproducible comparison with an alternative explanation. The two
bonus categories are ranked separately and can stack: the maximum is 14/10,
with the base score still out of 10.

#### Lab 2: Adversarial attacks

Can small changes to an input change a model's prediction? Implement a PGD
evasion attack on an MNIST classifier, compare L0, L1, L2 and L∞
budgets, and design a more efficient image attack. Then append a
short suffix of neutral words, punctuation and special tokens to a positive
movie review so that a fixed classifier predicts NEGATIVE: start from a greedy
baseline, beat it, and freeze the attack to test how it transfers. Finally,
compare data poisoning with a backdoor: plant a marker, vary the contamination
rate, and remove the marker feature.

The 10 points cover the image evasion attack (4), the text suffix attack (4),
and poisoning and backdoors (2). The top five in the image efficiency challenge
and the top five in the text challenge each earn +2; the maximum is 14/10.

#### Lab 3: Two ways to release a sensitive dataset

Release a census dataset (UCI Adult) privately in two ways, with
[JAX Privacy](https://github.com/google-parfait/jax_privacy) and
[DPSynth](https://github.com/google-parfait/dpsynth) in one Colab notebook.
First write DP-SGD from scratch for gradients stored as JAX pytrees: per-example
norms, clipping, the noisy average, one step with Poisson sampling, and the
training loop, checked against JAX Privacy's implementation. Then price it with
an accountant: build its privacy event and calibrate the noise for a target
ε by bisection. Finally, release a synthetic table with AIM inside
DPSynth: choose public bins for the numerical attributes, write the
exponential mechanism and AIM's selection step, and retrain DP-SGD on the
public domains.

All 10 points come from hidden tests on the functions you write: DP-SGD (5),
accounting (1.5), and AIM (3.5). The five binnings with the lowest error on
reserved data earn +2, and approved pull requests to JAX Privacy or DPSynth
earn +1 each, up to +5; the maximum is 17/10.

#### Lab 4: Compute Without Seeing

Complete two required privacy-enhancing technology exercises: a small Yao
comparison using garbled circuits and oblivious transfer, and private linear
inference in a real three-party MP-SPDZ runtime. Both tasks make the reveal
boundary explicit and test that no input or intermediate value crosses it.

Then choose one extension: encrypted aggregation with Paillier homomorphic
encryption, verification of a synthetic TEE attestation report, or a miniature
Path ORAM read/write implementation. The TEE path teaches attestation logic but
does not claim that a notebook simulates enclave security. The ORAM path must
state what access-pattern information remains visible and what a production
position map would require.

Selected labs use instructor-only hidden cases in addition to visible tests;
the number and mix of those cases are not announced. Course points use
fixed criteria; bonus rankings are separate.

Private materials are distributed through Canvas; any course Drive link will
be posted there. Raw notebooks, instances, hidden cases, evaluator files,
solutions, and grading files are not published on the public site.

### Project

The project contributes 30%. Its topic and method remain open, but it must make
an innovative privacy contribution. Students may build a system or focused
tool, develop an attack or defense, create a privacy monitor or auditor, or
complete a research project whose primary artifact is a paper. Teams of up to
2 are allowed, and both members receive the same grade; individual projects
may use a narrower scope.

Projects may build on existing papers, libraries, and code, but a reproduction,
routine comparison, literature review, mechanical port, or incremental
extension alone does not satisfy the requirement. Innovation may come from a
new capability, attack, defense, measurement, system boundary, interaction, or
research insight. Publication-level novelty is not required, but the proposal
must explain what becomes newly possible, measurable, or defensible relative
to a meaningful baseline.

The project has no leaderboard or required peer attack. The in-class
project pitch occurs in Week 7, the written proposal serves as a progress and
scope checkpoint in Week 10, and the poster/demo and final report are due in
Week 16.
See the
[milestone guide](project-present.html) and [project rubric](project-rubric.html).

### Quizzes

Both quizzes are completed individually during class on paper. They are closed
book and closed notes; computers, phones, AI tools, and other electronic aids
may not be used. Each quiz combines short foundation and application questions
with longer reasoning questions that ask students to certify, refute, or qualify
a claim using code, data, or a system description. An instructor-supplied
formula sheet and a practice set will be provided before each quiz. The covered
topics and any other permitted basic supplies will be announced in advance.

Coverage:

- Quiz 1 (October 15): privacy attacks, ML security, anonymization, and the DP
  material covered through the October 1 lecture.
- Quiz 2 (November 19): DP mechanisms, composition and accounting, private
  learning, cryptography, and MPC, through the November 12 lecture. Homomorphic
  encryption, taught afterward, is not included.

Guest lectures and optional readings are not part of these quiz scopes.
If lectures move again, the announced scope will reflect material actually
covered with time to prepare.

Students with an approved absence will receive an equivalent makeup
arrangement. The makeup may use different examples while assessing the same
skills.

### Exit surveys

Short individual exit surveys submitted through Canvas contribute 10%. They ask
students to record a conclusion, identify a remaining question, or interpret a
small result. Each submission receives credit for timely, good-faith completion.

## Materials and technology

No textbook or paid AI subscription is required. Readings, starter
environments, and private assignment bundles are supplied through Canvas;
any course Drive link will be posted there. The public site lists optional
books, courses, software, and current [AI access options](index.html#ai-access).

UVA students currently have no-additional-cost access to
[Gemini and NotebookLM](https://learningtech.virginia.edu/tools/gemini) and
[Copilot Chat](https://learningtech.virginia.edu/tools/copilot). Eligible U.S.
college students may also claim
[one year of Google AI Pro](https://gemini.google.com/students) at no cost by
December 31, 2026, and OpenAI's
[2026 student offer](https://chatgpt.com/students/2026/) for four free months of
ChatGPT Plus by October 31, 2026; both require student verification and a
payment method and become paid subscriptions unless canceled. UVA RC GenAI
provides Kimi K2.5 to eligible Research Computing users, but RC currently
restricts that service to research rather than ordinary class assignments.

Students need regular access to a computer that can run Python and a web
browser. Required lab paths are designed for CPU execution with pinned
environments. If access to hardware, software, or an assigned format creates a
barrier, contact the instructor early so that an equivalent path can be
arranged.

## Generative AI

AI tools may be used on all assignments except quizzes. Students remain
responsible for everything they submit.

## Collaboration and academic integrity

Labs, quizzes, and Canvas exit surveys are individual. Projects may
be completed individually or in teams of up to 2. High-level discussion across
the class is welcome, but students may not share lab code, completed tables,
or polished written answers. Every
submission must identify permitted collaborators.

Students are expected to follow the University
[Honor Code](https://honor.virginia.edu/) and its guidance on
[academic fraud](https://honor.virginia.edu/academic-fraud). Uncertainty about
permitted collaboration or AI use should be resolved with the instructor before
submission.

## Late work, regrades, and attendance

- Each student has 3 late days for the semester, with at most 2 on any one
  assignment.
- Late days can be used on any lab or project submission, but not on in-class
  activities.
- Regrade requests must be submitted within 7 days after a grade is released
  and may result in review of the entire submission.
- The result of a regrade request for a project team submission applies to the
  full team.
- Regular participation is expected because class activities contribute to
  the course. Students should communicate documented conflicts
  or serious circumstances as early as possible.
- Approved absences from a quiz receive an equivalent makeup arrangement.
  Contact the instructor about extended absences.

The full [course policy](policy.html) provides the detailed collaboration,
regrade, project-team, and career-related travel rules.

## Career-related travel

Your career development path may take you beyond UVA for an internship interview
or a technical conference. If you notify the instructor at least one week in
advance of such an event, you may choose either:

1. completing assignments remotely; or
2. delaying assignment, exam, or quiz dates until at least 48 hours after your
   return.

Extensions will not normally be granted for a project team activity when only
one member is traveling, and no delay will extend beyond the last day of finals
for the semester.

## Accessibility and academic accommodations

The goal is a learning environment that is accessible and usable by all
students. Students who anticipate a barrier in course materials, technology,
assessment format, or participation should contact the instructor.

Section 6 of UVA policy
[PROV-008: Teaching Courses for Academic Credit](https://uvapolicy.virginia.edu/policy/PROV-008)
governs academic accommodations for disability, pregnancy, and religion.
Students should use the official process for
[disability-related accommodations](https://sdac.studenthealth.virginia.edu/),
[pregnancy-related accommodations](https://eocr.virginia.edu/accommodations/pregnancy-accommodations/student-pregnancy-accommodations),
or [religious accommodations](https://eocr.virginia.edu/student-religious-accommodations)
and contact the instructor as early as possible.

UVA's official policies address
[discrimination and harassment](https://uvapolicy.virginia.edu/policy/HRM-009),
[retaliation](https://uvapolicy.virginia.edu/policy/HRM-010), and
[sexual and gender-based misconduct](https://uvapolicy.virginia.edu/policy/HRM-041).
The instructor and any TAs are Responsible Employees under
[HRM-040](https://uvapolicy.virginia.edu/policy/HRM-040). The official
[EOCR syllabus statement](https://eocr.virginia.edu/syllabus) explains current
reporting obligations and confidential resources; reports may be submitted
through [Just Report It](https://justreportit.virginia.edu/).

## Schedule and key dates

| Date | Course plan |
|---|---|
| August 25 | Course introduction; optional readiness self-check |
| August 27 | Privacy definitions and attack taxonomy |
| September 1 | Extraction and memorization |
| September 3 | Membership inference and attack evaluation |
| September 8 | Privacy attacks: conclusions and discussion |
| September 10 | Security notions and adversarial ML overview; Lab 1 released |
| September 15 | Adversarial examples and robustness |
| September 17 | Poisoning, backdoors, and ML security defenses |
| September 22 | No class: break |
| September 24 | Anonymization, linkage, and k-anonymity; Lab 1 due and Lab 2 released |
| September 29 | Differential privacy: definitions |
| October 1 | Differential privacy (continued) |
| October 6 | No class: Fall Reading Days |
| October 8 | In-class project pitch presentations |
| October 13 | Guest lecture: privacy in industry |
| October 15 | Quiz 1 |
| October 20 | Private selection: report noisy max and the exponential mechanism |
| October 22 | Sparse vector, range queries, DP-SGD, and AIM; Lab 3 released |
| October 23 | Lab 2 due |
| October 27 | PETs and symmetric-key cryptography: hashes and MACs |
| October 29 | Public-key cryptography and Diffie-Hellman; project proposal |
| November 3 | No class: Election Day |
| November 5 | RSA, digital signatures, and timing attacks |
| November 10 | Secure multiparty computation: garbled circuits and oblivious transfer |
| November 12 | MPC: secret sharing and security models; Lab 3 due and Lab 4 released |
| November 17 | Guest lecture: oblivious RAM (ORAM) |
| November 19 | Quiz 2 |
| November 24 | Homomorphic encryption and private computation |
| November 25-29 | Thanksgiving recess |
| December 1 | Guest lecture: TEEs and confidential LLM serving |
| December 3 | Privacy applications and review; Lab 4 due |
| December 8 | Poster/demo session and course recap; final report |

Local DP, zero-knowledge proofs, verifiable computation, and network privacy
are optional extensions rather than scheduled core lectures. December 3 is a
flexible session for applications, unfinished material, and review.

The [full schedule](schedule.html) is tentative. Exact deadlines will appear in
Canvas. Changes after the start of the term will be communicated in writing and
will not place required deadlines during scheduled University recess.

</div>

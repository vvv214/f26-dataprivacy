---
---

<div class="syllabus-page" markdown="1">

# CS 4501-003: Data Privacy

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

<p class="syllabus-subtitle">Fall 2026 syllabus | Planning draft | Updated August 25, 2026</p>

<div class="syllabus-draft">
This page is the working syllabus for Fall 2026. Before it becomes the official
first-day version, the instructor will confirm office hours, assignment dates,
letter-grade thresholds, and assignment logistics. Changes will be
dated and communicated through Canvas.
</div>

## Course information

| Item | Details |
|---|---|
| Course | CS 4501-003, Special Topics in Computer Science: Data Privacy |
| Instructor | [Tianhao Wang](https://tianhao.wang) |
| Email | [tianhao@virginia.edu](mailto:tianhao@virginia.edu) |
| Meetings | Tuesdays and Thursdays, 2:00-3:15 PM |
| Classroom | Olsson Hall 011 |
| Term | August 25-December 8, 2026 |
| Office hours | To be confirmed before the first day of class; appointments will also be available |
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

We begin with extraction, membership inference, linkage, and reconstruction.
We then develop differential privacy and privacy-utility trade-offs, private
machine learning, synthetic data, and privacy-enhancing technologies including
secure multi-party computation, homomorphic encryption, trusted execution
environments, and network privacy tools. The course is designed for
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
- Four equally weighted labs use privacy-attack, direct agent-arena,
  industrial-code, and bounded open-design formats. Required systems include
  Opacus, JAX Privacy, Google DPSynth, and MP-SPDZ. All labs are individual.
- A team or individual project asks students to make an innovative privacy
  contribution as a system, focused tool, attack, defense, monitor/auditor, or
  research paper.
- Two individual, in-class, closed-book paper quizzes check conceptual and
  applied reasoning. Short individual exit surveys and check-ins are submitted
  through Canvas across the semester.

Guest lectures will connect course mechanisms to industry privacy practice and
recent academic work. Their topics and speakers will be updated on the
[course schedule](schedule.html) as they are confirmed. Students should expect
to read short technical material before selected meetings and to work with
small CPU-compatible code bundles outside class.

## Assessment and grading

| Component | Weight | Basis |
|---|---:|---|
| [Labs](lab.html) | 40% | Four labs worth 10% each; selected labs use hidden cases and Lab 2 uses a direct arena |
| [Project](project.html) | 30% | Project pitch 10%, proposal 5%, poster/demo 10%, final report 5% |
| Quizzes | 20% | Two individual, in-class, closed-book paper quizzes at 10% each |
| Exit surveys / check-ins | 10% | Short individual Canvas submissions graded for completion |
| Total | 100% | |

Final grades use the [UVA grading basis](https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=1153c16fdba41f444f32fb671d961934).
Exact letter-grade thresholds will be added before this draft becomes the
official syllabus.

### Labs

All labs are completed individually. They deliberately use different work
products: a privacy-attack runner, a two-agent secret-arena submission, a
regression-tested library extension, and a private-computation artifact with
an oral check.

Selected labs use instructor-only hidden cases in addition to visible tests;
the number and mix of those cases are not announced. Lab 2 uses direct
two-agent matches with a separate hidden utility evaluator. Arena rankings are
feedback, not winner-take-all grades; course points use fixed criteria and
instructor baselines. Some instances are intentionally clean or contain
insufficient evidence, so a correct abstention can receive full credit.

| Lab | Weight | Release week | Due week |
|---|---:|---:|---:|
| Privacy Attack Warm-up | 10% | 3 | 5 |
| Two-Agent Secret Arena | 10% | 5 | 9 |
| DP Library Extension Challenge | 10% | 9 | 12 |
| Compute Without Seeing | 10% | 12 | 15 |

Private materials are distributed through Canvas; any course Drive link will
be posted there. Raw notebooks, instances, hidden cases, evaluator files,
solutions, and grading files are not published on the public site.

### Project

The project contributes 30%. Its topic and method remain open, but it must make
an innovative privacy contribution. Students may build a system or focused
tool, develop an attack or defense, create a privacy monitor or auditor, or
complete a research project whose primary artifact is a paper. Teams of up to
2 are allowed; individual projects may use a narrower scope.

Projects may build on existing papers, libraries, and code, but a reproduction,
routine comparison, literature review, mechanical port, or incremental
extension alone does not satisfy the requirement. Innovation may come from a
new capability, attack, defense, measurement, system boundary, interaction, or
research insight. Publication-level novelty is not required, but the proposal
must explain what becomes newly possible, measurable, or defensible relative
to a meaningful baseline.

The project has no leaderboard, arena, or required peer attack. The in-class
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

Students with an approved absence will receive an equivalent makeup
arrangement. The makeup may use different examples while assessing the same
skills.

### Exit surveys and check-ins

Short individual exit surveys and check-ins submitted through Canvas contribute
10%. They ask students to record a conclusion, identify a remaining question,
interpret a small result, or check progress on a current lab or project. Each
submission receives credit for timely, good-faith completion.

## Materials and technology

No required textbook or paid AI subscription is planned. Readings, starter
environments, and private assignment bundles will be supplied through Canvas;
any course Drive link will be posted there. The public site lists optional
books, courses, software, and current [AI access options](index.html#ai-access).

UVA students currently have no-additional-cost access to
[Gemini and NotebookLM](https://learningtech.virginia.edu/tools/gemini) and
[Copilot Chat](https://learningtech.virginia.edu/tools/copilot). Eligible U.S.
college students may also claim OpenAI's
[2026 student offer](https://chatgpt.com/students/2026/) for four free months of
ChatGPT Plus by October 31, 2026; it requires student verification and a payment
method and renews at the regular monthly price unless canceled. UVA RC GenAI
provides Kimi K2.5 to eligible Research Computing users, but RC currently
restricts that service to research rather than ordinary class assignments.

Students need regular access to a computer that can run Python and a web
browser. Required lab paths are designed for CPU execution with pinned
environments. If access to hardware, software, or an assigned format creates a
barrier, contact the instructor early so that an equivalent path can be
arranged.

## Generative AI

Generative AI may be used for brainstorming, debugging, code explanation, and
polishing unless an assignment says otherwise. It does not replace technical
ownership.

- Students remain responsible for correctness, citations, privacy, and course
  policy compliance.
- Private course bundles or sensitive data may not be uploaded to external
  tools unless explicitly permitted.
- When AI materially shapes a lab, submit an AI Decision Ledger with 3-5
  consequential decisions. Project ledgers use 5-10 entries. Record the
  suggestion, how it was checked, and the resulting decision. Complete chat
  transcripts are not required.
- Quizzes are completed without GenAI.
- During the Lab 2 arena, systems may use only the course-provided model
  interface and common resource budget defined by the lab specification.

## Collaboration and academic integrity

Labs, quizzes, and Canvas exit surveys/check-ins are individual. Projects may
be completed individually or in teams of up to 2. High-level discussion across
the class is welcome, but students may not share lab code, completed tables,
polished written answers, arena submissions, or private arena feedback. Every
submission must identify permitted collaborators; project teams must include a
contribution statement where required.

Students are expected to follow the University
[Honor Code](https://honor.virginia.edu/) and its guidance on
[academic fraud](https://honor.virginia.edu/academic-fraud). Uncertainty about
permitted collaboration or AI use should be resolved with the instructor before
submission.

## Late work, regrades, and attendance

- Each student has 3 late days for the semester, with no more than 2 used on one
  assignment.
- Late days may be used on Labs 1 and 3 and the project proposal. They may not
  be used for the synchronized Lab 2 arena submission, the in-class project
  pitch, the Lab 4 individual oral check, quizzes, the poster/demo session, the
  final report, or other end-of-semester deadlines.
- Regrade requests must be submitted within 7 days after a grade is released
  and may result in review of the entire submission.
- The result of a regrade request for a project team submission applies to the
  full team.
- Regular participation is expected because class activities and peer review
  contribute to the course. Students should communicate documented conflicts
  or serious circumstances as early as possible.
- Approved absences from a quiz receive an equivalent makeup arrangement; late
  days do not apply to in-class quizzes. Contact the instructor about extended
  absences.

The full [course policy](policy.html) provides the detailed collaboration,
regrade, project-contribution, and career-related travel rules.

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

## Key dates and changes

| Date | Course plan |
|---|---|
| August 25 | First class |
| September 10 | Lab 1 released |
| September 24 | Lab 1 due and Lab 2 released |
| October 6 | No class: Fall Reading Days |
| October 8 | In-class project pitch presentations |
| October 13 | Guest lecture: TEEs and confidential LLM serving |
| October 15 | Quiz 1 |
| October 22 | Lab 2 due and Lab 3 released |
| October 29 | Project proposal |
| November 3 | No class: Election Day |
| November 12 | Lab 3 due and Lab 4 released |
| November 17 | Guest lecture: oblivious RAM (ORAM) |
| November 19 | Quiz 2 |
| November 24 | Network privacy and contextual integrity; Lab 4 oral-check window |
| November 25-29 | Thanksgiving recess |
| December 1 and 3 | Guest lectures; Lab 4 due December 3 |
| December 8 | Poster/demo session, last class, and final report |

The [full schedule](schedule.html) is tentative. Exact deadlines will appear in
Canvas. Changes after the start of the term will be communicated in writing and
will not place required deadlines during scheduled University recess.

</div>

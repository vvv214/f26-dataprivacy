---
---

<div class="syllabus-page" markdown="1">

# CS 4501-003: Data Privacy

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

<p class="syllabus-subtitle">Fall 2026 syllabus | Planning draft | Updated August 24, 2026</p>

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
5. design and evaluate a scoped privacy project using reproducible evidence;
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
- Seven unequal-weight labs use CTF, hidden-test, anonymous-arena, code-audit,
  feature-sprint, synthetic-data, and MPC formats. Required systems include
  Opacus, JAX Privacy, and Google DPSynth.
- A scoped team or individual project lets students choose an open privacy
  question, method, and appropriate form of evidence over several weeks.
- Two individual, in-class, closed-book paper quizzes check conceptual and
  applied reasoning. Participation includes Canvas check-ins, structured
  in-class work, and two brief individual written checks of submitted artifacts.

Planned asynchronous class work appears explicitly on the
[course schedule](schedule.html). Students should expect to read short technical
material before selected meetings and to work with small CPU-compatible code
bundles outside class.

## Assessment and grading

| Component | Weight | Basis |
|---|---:|---|
| [Labs](lab.html) | 30% | Seven labs worth 3-6% each; selected labs use hidden cases and two use controlled arenas |
| [Project](project.html) | 30% | Topic check-in 3%, proposal 5%, progress checkpoint 7%, poster/demo 5%, final report 10% |
| Quizzes | 30% | Two individual, in-class, closed-book paper quizzes at 15% each |
| Participation | 10% | Two individual written artifact checks (4%) and Canvas check-ins or structured in-class work (6%) |
| Total | 100% | |

Final grades use the [UVA grading basis](https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=1153c16fdba41f444f32fb671d961934).
Exact letter-grade thresholds will be added before this draft becomes the
official syllabus.

### Labs

Labs may be completed in teams of 2 or individually. They deliberately use
different work products: an attack runner, an evidence-backed data
investigation, anonymous transcript review, a regression-tested library patch,
an industrial feature, a private synthetic release, and an MPC protocol.

Selected labs use instructor-only hidden cases in addition to visible tests;
the number and mix of those cases are not announced. Labs 3 and 6 use the
[lab arenas](arena.html). Arena rankings are
feedback, not winner-take-all grades; course points use fixed criteria and
instructor baselines. Some instances are intentionally clean or contain
insufficient evidence, so a correct abstention can receive full credit.

| Lab | Weight | Release week | Due week |
|---|---:|---:|---:|
| Model Privacy CTF | 3% | 2 | 3 |
| Linkage and Reconstruction | 4% | 3 | 5 |
| LLM Privacy Attack Arena | 4% | 4 | 6 |
| DP Training Systems: Opacus and JAX Privacy | 5% | 6 | 9 |
| Google DPSynth Feature Sprint | 6% | 8 | 11 |
| Synthetic Data Arena | 5% | 10 | 13 |
| Compute Without Seeing: MPC | 3% | 11 | 14 |

Private materials are distributed through Canvas; any course Drive link will
be posted there. Raw notebooks, instances, hidden cases, evaluator files,
solutions, and grading files are not published on the public site.

### Project

The project contributes 30%. Its topic, method, and contribution format remain
open: students may reproduce and extend prior work, compare privacy methods,
build a small system, conduct an audit, or propose another rigorous format.
Novel research is not required. Teams of up to 2 are allowed; individual
projects may use a narrower scope.

The project has no leaderboard, arena, or required peer attack. The topic
check-in occurs in Week 7, the proposal in Week 10, the progress checkpoint in
Week 12, poster/demo sessions in Week 15, and the final report in Week 16.
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

### Participation

Participation contributes 10%: 6% comes from regular Canvas check-ins and
structured in-class work, with the two lowest regular Canvas check-ins dropped;
4% comes from two individual written artifact checks worth 2% each.

Each artifact check is a 10-minute, in-class paper exercise based on a short
excerpt selected from the student's submitted team artifact. Students may be
asked to locate a relevant component, explain its behavior, connect a claim to
evidence, or predict the effect of a small change. The checks are individual,
closed book, closed notes, and completed without electronics or AI. The first
follows the DP Training Systems lab; the second takes place during the Week 15
poster/demo sessions and uses the student's project artifact. An approved
absence receives an equivalent prompt at an arranged time.

## Materials and technology

No required textbook or paid AI subscription is currently planned. Readings,
starter environments, and private assignment bundles will be supplied through
Canvas; any course Drive link will be posted there. The public site lists
optional books, courses, and software references.

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
- During lab arenas, systems may use only the course-provided tools and common
  resource budget defined by the lab specification.

## Collaboration and academic integrity

Labs and projects may be completed in teams of up to 2. Quizzes, regular Canvas
check-ins, and written artifact checks are individual. High-level discussion
across teams is welcome, but
students may not share code, completed tables, polished written answers, arena
submissions, or private arena feedback across teams. Every submission
must identify collaborators and, where required, include a contribution
statement.

Students are expected to follow the University
[Honor Code](https://honor.virginia.edu/) and its guidance on
[academic fraud](https://honor.virginia.edu/academic-fraud). Uncertainty about
permitted collaboration or AI use should be resolved with the instructor before
submission.

## Late work, regrades, and attendance

- Each student has 3 late days for the semester, with no more than 2 used on one
  assignment.
- Late days may be used on Labs 1, 2, 4, and 5, the topic check-in, and project
  proposal. They may not be used for the synchronized Lab 3 or Lab 6 arena
  submissions, Lab 7, quizzes, project progress presentations, poster/demo
  sessions, the final report, or other end-of-semester deadlines.
- Regrade requests must be submitted within 7 days after a grade is released
  and may result in review of the entire submission.
- The result of a regrade request for a team submission applies to the full
  team.
- Regular participation is expected because studios and peer review contribute
  to the course. Students should communicate documented conflicts or serious
  circumstances as early as possible.
- Approved absences from a quiz or written artifact check receive an equivalent
  makeup arrangement; late days do not apply to these in-class assessments.

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
| September 22 | Planned asynchronous class work |
| October 6 | No class: Fall Reading Days |
| October 8 | Quiz 1; project topic check-in due in Canvas |
| October 13 and 15 | Planned asynchronous class work |
| October 27 | Individual written artifact check 1 |
| November 3 | No class: Election Day |
| November 10 | Project progress checkpoint |
| November 12 | Quiz 2 |
| November 17 and 19 | Planned asynchronous class work |
| November 25-29 | Thanksgiving recess |
| December 1 and 3 | Poster/demo sessions and individual written artifact check 2 |
| December 8 | Last class and final report |

The [full schedule](schedule.html) is tentative. Exact deadlines will appear in
Canvas. Changes after the start of the term will be communicated in writing and
will not place required deadlines during scheduled University recess.

</div>

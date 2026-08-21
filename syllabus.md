---
---

<div class="syllabus-page" markdown="1">

# CS 4501-003: Data Privacy

<p class="syllabus-subtitle">Fall 2026 syllabus | Planning draft | Updated August 20, 2026</p>

<div class="syllabus-draft">
This page is the working syllabus for Fall 2026. Before it becomes the official
first-day version, the instructor will confirm office hours, assignment dates,
letter-grade thresholds, and the exact oral-defense schedule. Changes will be
dated and communicated through Canvas.
</div>

## Course information

| Item | Details |
|---|---|
| Course | CS 4501-003, Special Topics in Computer Science: Data Privacy |
| Instructor | [Tianhao Wang](https://tianhao.wang) |
| Meetings | Tuesdays and Thursdays, 2:00-3:15 PM |
| Classroom | Olsson Hall 011 |
| Term | August 25-December 8, 2026 |
| Office hours | To be confirmed before the first day of class; appointments will also be available |
| Public course site | [tianhao.wang/f26-dataprivacy](https://tianhao.wang/f26-dataprivacy/) |
| Canvas | [canvas.its.virginia.edu/courses/190753](https://canvas.its.virginia.edu/courses/190753) |

Canvas is the authoritative source for announcements, release bundles,
submissions, grades, and any date changes. The public site contains the durable
course description, schedule, assignment structure, and policies.

## Course description

How can we use data to build useful systems without exposing the people behind
the data? This course studies concrete privacy attacks, practical defenses, and
the engineering contracts that connect privacy claims to data, code,
configuration, accounting, and tests.

We begin with extraction, membership inference, linkage, and reconstruction.
We then develop differential privacy and privacy-utility trade-offs, private
machine learning, synthetic data, and privacy-enhancing technologies including
secure multi-party computation, homomorphic encryption, trusted execution
environments, and network privacy tools. The course is designed for advanced
undergraduates and emphasizes technical judgment, reproducible evidence, and
clear communication rather than graduate-level novelty.

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
5. build, break, repair, and transfer a small privacy-aware system using
   reproducible evidence; and
6. communicate conclusions, uncertainty, residual risks, and the role of AI
   assistance in technical work.

## Background and preparation

Required background:

- Python programming.
- Basic probability.

Prior coursework in machine learning, security, cryptography, or data science
is recommended but not required. No prior experience with differential
privacy, LLM training, privacy research, or advanced cryptography is assumed.

## How the course works

The course combines five forms of work:

- Lectures and short practicals introduce attacks, mechanisms, systems, and
  evaluation methods.
- Three audit labs repeat a Build-Break-Repair-Transfer workflow using Opacus,
  JAX Privacy, and Google DPSynth.
- A scoped team or individual project applies the same cycle over several
  weeks, including a formative peer break exchange.
- Two in-class quizzes, reading warm-ups, and short participation activities
  check individual understanding throughout the term.
- A 5-10 minute individual oral defense checks ownership of selected lab and
  project decisions.

Planned asynchronous class work appears explicitly on the
[course schedule](schedule.html). Students should expect to read short technical
material before selected meetings and to work with small CPU-compatible code
bundles outside class.

## Assessment and grading

| Component | Weight | Basis |
|---|---:|---|
| [Audit labs](lab.html) | 30% | Three labs at 10% each; code, evidence, repair, regression tests, and transfer |
| [Project](project.html) | 25% | Topic check-in 5%, proposal 5%, poster/demo 5%, final report 10% |
| [Individual oral defense](oral.html) | 10% | Technical ownership, evidence, changed requirement, and residual-risk reasoning |
| Quizzes | 20% | Two individual in-class quizzes on foundations and core mechanisms |
| Exit tickets and participation | 10% | Short check-ins, audit studios, and the formative project break exchange |
| Reading warm-ups | 5% | Short individual preparation for selected readings |
| Total | 100% | |

Final grades use the [UVA grading basis](https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=1153c16fdba41f444f32fb671d961934).
Exact letter-grade thresholds will be added before this draft becomes the
official syllabus.

### Audit labs

Labs may be completed in teams of 2 or individually. Each lab asks students to
build a small baseline, determine whether an assigned privacy contract holds,
repair or guard the relevant code path, add a regression test, and transfer the
analysis to a changed setting. Some instances are intentionally clean or
contain insufficient evidence; grades do not reward luck in finding an unknown
bug.

Lab bundles and hidden tests are distributed privately through Canvas or the
course Drive. Raw notebooks, mutation mappings, solutions, and grading files
are not published on the public site.

| Lab | Tool | Release week | Due week |
|---|---|---:|---:|
| Training contract audit | Opacus | 6 | 9 |
| Step accounting patch | JAX Privacy | 9 | 12 |
| Synthetic release audit | Google DPSynth | 11 | 14 |

### Project

The project contributes 25% and develops through Build, Break, Repair, and
Transfer. Projects may reproduce and extend prior work, compare privacy methods,
or build a small privacy-aware system. Novel research is not required. Teams of
up to 2 are allowed; individual projects may use a narrower scope.

The topic check-in occurs in Week 7, the proposal in Week 10, the formative
break exchange in Week 13, poster/demo sessions in Week 15, and the final report
in Week 16. See the [milestone guide](project-present.html) and
[project rubric](project-rubric.html).

### Individual oral defense

Each student completes a 5-10 minute conversation about one submitted lab
artifact and one project decision. The defense may be scheduled during a
designated class period or through a mutually arranged office-hour appointment;
the final format and an equivalent option for students who cannot use an
office-hour appointment will be announced in Canvas. Students may open their
own submitted artifacts but may not use external AI assistance during the
defense. No slides are required, and students are not expected to locate an
unknown bug on the spot.

## Materials and technology

No required textbook or paid AI subscription is currently planned. Readings,
starter environments, and private assignment bundles will be supplied through
Canvas or the course Drive. The public site lists optional books, courses, and
software references.

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
- When AI materially shapes a lab or project, submit an AI Decision Ledger with
  5-10 consequential decisions, the suggestion received, how it was checked,
  and the resulting decision. Complete chat transcripts are not required.
- Quizzes and the individual oral defense are completed without GenAI unless
  explicitly announced otherwise.

## Collaboration and academic integrity

Labs and projects may be completed in teams of up to 2. Quizzes, reading
warm-ups, exit tickets, and the oral defense are individual. High-level
discussion across teams is welcome, but students may not share code, completed
tables, or polished written answers across teams. Every submission must identify
collaborators and, where required, include a contribution statement.

Students are expected to follow the University
[Honor Code](https://honor.virginia.edu/) and its guidance on
[academic fraud](https://honor.virginia.edu/academic-fraud). Uncertainty about
permitted collaboration or AI use should be resolved with the instructor before
submission.

## Late work, regrades, and attendance

- Each student has 3 late days for the semester, with no more than 2 used on one
  assignment.
- Late days may be used on labs, the topic check-in, project proposal, and
  reading warm-ups. They may not be used for quizzes, poster/demo sessions, the
  oral defense, final report, or other end-of-semester deadlines.
- Regrade requests must be submitted within 7 days after a grade is released
  and may result in review of the entire submission.
- Regular participation is expected because studios and peer review contribute
  to the course. Students should communicate documented conflicts or serious
  circumstances as early as possible.

The full [course policy](policy.html) governs collaboration, regrades, project
contributions, accommodations, respectful conduct, and career-related travel.

## Accessibility, accommodations, and learning environment

The goal is a learning environment that is accessible and usable by all
students. Students who anticipate a barrier in course materials, technology,
assessment format, or participation should contact the instructor. Students
seeking disability-related accommodations should also work with the
[Student Disability Access Center](https://studenthealth.virginia.edu/sdac).

UVA provides reasonable academic accommodations when disability, pregnancy, or
sincerely held religious belief conflicts with course requirements. Requests
should be made as early as possible. Questions about pregnancy or religious
accommodations may be directed to the
[Office for Equal Opportunity and Civil Rights](https://eocr.virginia.edu/).

The course follows UVA policies prohibiting discrimination, harassment, and
retaliation. Support, confidential resources, and reporting options are linked
from the full [course policy](policy.html).

## Key dates and changes

| Date | Course plan |
|---|---|
| August 25 | First class |
| September 22 | Planned asynchronous course work |
| October 6 | No class: Fall Reading Days |
| October 13 and 15 | Planned asynchronous course work |
| November 3 | No class: Election Day |
| November 17 and 19 | Planned asynchronous course work |
| November 25-29 | Thanksgiving recess |
| December 1 and 3 | Poster/demo sessions |
| December 8 | Last class and final report |

The [full schedule](schedule.html) is tentative. Exact deadlines will appear in
Canvas. Changes after the start of the term will be communicated in writing and
will not place required deadlines during scheduled University recess.

</div>

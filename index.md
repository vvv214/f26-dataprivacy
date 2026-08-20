---
---

# Data Privacy (Fall 2026)

## Course overview

How can we use data to build useful systems without exposing the people behind the data? This course introduces the core ideas of modern data privacy through concrete attacks, practical defenses, and hands-on system audits.

The course is designed for advanced undergraduates. We will start with privacy failures that students can observe directly, then build toward differential privacy, privacy-aware machine learning, and privacy-enhancing technologies such as MPC, HE, TEE, and network privacy tools. The emphasis is on technical understanding, experimental reasoning, and clear communication rather than graduate-level novelty.

## What you will learn

- How common privacy attacks work, including extraction, membership inference, linkage, and reconstruction.
- How to reason about privacy defenses, especially differential privacy and its utility trade-offs.
- How privacy engineering differs across machine learning, databases, and systems settings.
- How to trace a privacy claim through data, code, configuration, accounting, and tests.
- How to read, critique, and explain privacy papers and experimental results.

## Who should enroll?

This version of the course is aimed at advanced undergraduates in computer science, data science, or related areas.

Required background:

- Python programming.
- Basic probability.
- Comfort reading and modifying short pieces of code.

Recommended background:

- One prior course in machine learning, security, cryptography, or data science.
- Familiarity with vectors, matrices, and simple model evaluation metrics.

You do not need prior experience with LLM training, privacy research, or advanced cryptography.

## Why take this course?

Privacy is now part of the job in machine learning, data science, and systems work. Engineers are expected to understand not only how to build models, but also how those models leak, what protections are realistic, and where the trade-offs appear in practice. This course is intended to prepare students for that level of technical judgment.

## Course info

- Course: CS 4501-003, Special Topics in Computer Science: Data Privacy
- Instructor: [Tianhao Wang](https://tianhao.wang)
- Location: Olsson Hall 011
- Time: Tuesdays and Thursdays, 2:00-3:15 PM
- Dates: August 25-December 8, 2026
- Canvas: [course site](https://canvas.its.virginia.edu/courses/190753)
- Format: in-person lectures, short practicals, three audit labs, quizzes, and a scoped final project
- [Policy](policy.html)

## Grading

- [Labs](lab.html) (30%): three privacy-engineering audits using Opacus, JAX Privacy, and Google DPSynth; teams of 2 or individual work.
- [Project](project.html) (25%): topic check-in (5%), proposal (5%), poster/demo (5%), and final report (10%). See the [milestone guide](project-present.html) and [project rubric](project-rubric.html).
- [Individual oral defense](oral.html) (10%): explain and adapt selected lab and project decisions.
- Quizzes (20%): two in-class quizzes on foundations and core mechanisms.
- Exit tickets / participation (10%): short check-ins, audit studios, and the formative project break exchange.
- Reading warm-ups (5%): short individual responses on selected course readings.
- Grading scale: we use the [UVA default Grading Basis](https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=1153c16fdba41f444f32fb671d961934)

## Schedule

{% include_relative schedule.md %}

## More resources

For a maintained collection of courses, books, tutorials, and software, see the [OpenDP educational resources](https://learning.opendp.org/).

### Courses

#### Core DP & privacy

- [Algorithms for Private Data Analysis](http://www.gautamkamath.com/courses/CS860-wi2026.html) ([video](https://www.youtube.com/playlist?list=PLmd_zeMNzSvRRNpoEWkVo6QY_6rR3SHjp)) Winter 2026 by Gautam Kamath (Waterloo)
- [Applied Privacy for Data Science](https://opendp.github.io/cs208/spring2025/) Spring 2025 by Salil Vadhan, James Honaker, and Priyanka Nanayakkara (Harvard)
- [Algorithmic Foundations of Differential Privacy](https://www.cs.jhu.edu/~mdinitz/classes/DP-class/Spring2025/) Spring 2025 by Michael Dinitz (Johns Hopkins)
- [Introduction to Differential Privacy: Theory, Algorithms and Applications](https://cseweb.ucsd.edu/~yuxiangw/classes/DSC291-2024Fall/) ([video](https://www.youtube.com/watch?v=OzjmWObjgzg)) Fall 2024 by Yuxiang Wang (UCSD)
- [Privacy in Statistics and Machine Learning](https://dpcourse.github.io/) ([video](https://drive.google.com/drive/folders/1Ds5KlyWrX93DeiQWrFLpBS0Zsk104bnd?usp=sharing)) Spring 2023 by Adam Smith (BU) and Jonathan Ullman (NEU)
- [Algorithms for Private Data Analysis](https://www.cs.toronto.edu/~anikolov/CSC2412F20/CSC2412.html) Fall 2020 by Aleksandar Nikolov (UofT)

#### Other flavors (theory, systems, fairness, ML)

- PETs: [Privacy Enhancing Technologies](https://www.cs.unc.edu/~saba/priv_class/summer25/index.html) Summer 2025 by Saba Eskandarian (UNC)
- Theory: [The Algorithmic Foundations of Adaptive Data Analysis](https://adaptivedataanalysis.com/lecture-schedule-and-notes/) Fall 2017 by Aaron Roth (Penn) and Adam Smith (BU)
- Systems: [Private Systems](https://systems.cs.columbia.edu/private-systems-class/) Spring 2020 by Roxana Geambasu (Columbia)
- Mechanism design: [Differential Privacy in Game Theory and Mechanism Design](https://www.cis.upenn.edu/~aaroth/courses/gametheoryprivacyS14.html) Spring 2014 by Aaron Roth (Penn)
- Fairness: [CS 294: Fairness in Machine Learning](https://fairmlclass.github.io/) (UC Berkeley, Moritz Hardt)
- ML: [Privacy Preserving Machine Learning](https://researchers.lille.inria.fr/abellet/teaching/private_machine_learning_course.html), course materials from 2020-2023 by Aurelien Bellet (Inria)

### Software used in the labs

- [Opacus](https://opacus.ai/) for private training in PyTorch.
- [JAX Privacy](https://jax-privacy.readthedocs.io/) for auditable DP training in JAX and Keras.
- [Google DPSynth](https://github.com/google/dpsynth) for differentially private tabular synthesis.
- [OpenDP](https://opendp.org/) for additional mechanisms, documentation, and learning resources.

### Books

#### Cryptography & MPC

- [The Joy of Cryptography](https://joyofcryptography.com/)
- [A Pragmatic Introduction to Secure Multi-Party Computation](https://securecomputation.org/)
- [A Graduate Course in Applied Cryptography](https://crypto.stanford.edu/~dabo/cryptobook/)
- [Handbook of Applied Cryptography](https://cacr.uwaterloo.ca/hac/)

#### Differential privacy

- [Programming Differential Privacy](https://programming-dp.com/)
- [Hands-On Differential Privacy](https://www.oreilly.com/library/view/hands-on-differential-privacy/9781492097730/)
- [The Algorithmic Foundations of Differential Privacy](https://www.cis.upenn.edu/~aaroth/Papers/privacybook.pdf)
- [Differential Privacy for Databases](https://dpfordb.github.io/)
- [The Complexity of Differential Privacy](https://salil.seas.harvard.edu/publications/complexity-differential-privacy)
- [Differential Privacy: A Primer for a Non-Technical Audience](https://scholarship.law.vanderbilt.edu/jetlaw/vol21/iss1/4/)
- [Protecting Your Privacy In A Data-driven World](https://www.clairemckaybowen.com/book)

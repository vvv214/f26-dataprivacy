---
---

# Data Privacy (Fall 2026 draft)

<nav class="course-nav" aria-label="Course pages">
  <a href="schedule.html">Schedule</a>
  <a href="lab.html">Labs</a>
  <a href="project.html">Project</a>
  <a href="project-rubric.html">Rubric</a>
  <a href="project-present.html">Milestones</a>
  <a href="policy.html">Policies</a>
</nav>

## Course overview

How can we use data to build useful systems without exposing the people behind the data? This course introduces the core ideas of modern data privacy through concrete attacks, practical defenses, and hands-on labs.

The course is designed for advanced undergraduates. We will start with privacy failures that students can observe directly, then build toward differential privacy, privacy-aware machine learning, and privacy-enhancing technologies such as MPC, HE, TEE, and network privacy tools. The emphasis is on technical understanding, experimental reasoning, and clear communication rather than graduate-level novelty.

## What you will learn

- How common privacy attacks work, including extraction, membership inference, linkage, and reconstruction.
- How to reason about privacy defenses, especially differential privacy and its utility trade-offs.
- How privacy engineering differs across machine learning, databases, and systems settings.
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

- Instructor: [Tianhao Wang](https://tianhao.wang)
- TA: TBD
- Location: TBD
- Time: TBD
- Canvas: will be posted before the semester begins
- Format: in-person lectures with labs, quizzes, reading warm-ups, and a scoped final project
- Note: this is a draft for Fall 2026. Exact logistics, room, and due dates may shift.
- [Policy](policy.html)

## Grading

- Labs (35%): four take-home labs; most labs are pair-based, but individual submission is allowed.
- Project (30%): topic check-in (5%), proposal (5%), poster/demo (10%), final report (10%).
- Quizzes (20%): two in-class quizzes on foundations and core mechanisms.
- Exit tickets / participation (10%): short check-ins tied to lecture attendance and engagement.
- Reading warm-ups (5%): short individual responses on selected course readings.
- Grading scale: we use the [UVA default Grading Basis](https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=1153c16fdba41f444f32fb671d961934)

## Schedule

{% include_relative schedule.md %}

## More resources

### Courses

#### Core DP & privacy

- [Privacy in Statistics and Machine Learning](https://dpcourse.github.io/) ([video](https://drive.google.com/drive/folders/1Ds5KlyWrX93DeiQWrFLpBS0Zsk104bnd?usp=sharing)) Spring 2023 by Adam Smith (BU) and Jonathan Ullman (NEU)
- [Algorithms for Private Data Analysis](http://www.gautamkamath.com/courses/CS860-wi2026.html) ([video](https://www.youtube.com/playlist?list=PLmd_zeMNzSvRRNpoEWkVo6QY_6rR3SHjp)) Winter 2026 by Gautam Kamath (Waterloo)
- [Applied Privacy for Data Science](https://opendp.github.io/cs208/) Spring 2022 by James Honaker, Wanrong Zhang, and Salil Vadhan (Harvard)
- [Introduction to Differential Privacy: Theory, Algorithms and Applications](https://cseweb.ucsd.edu/~yuxiangw/classes/DSC291-2024Fall/) ([video](https://www.youtube.com/watch?v=OzjmWObjgzg)) Fall 2024 by Yuxiang Wang (UCSD)
- [Algorithms for Private Data Analysis](https://www.cs.toronto.edu/~anikolov/CSC2412F20/CSC2412.html) Fall 2020 by Aleksandar Nikolov (UofT)
- [Privacy Enhancing Technologies](https://www.cs.unc.edu/~saba/priv_class/summer25/index.html) Summer 2025 by Saba Eskandarian (UNC)

#### Other flavors (theory, systems, fairness, ML)

- Theory: [The Algorithmic Foundations of Adaptive Data Analysis](https://adaptivedataanalysis.com/lecture-schedule-and-notes/) Fall 2017 by Aaron Roth (Penn) and Adam Smith (BU)
- Systems: [Private Systems](https://systems.cs.columbia.edu/private-systems-class/) Spring 2020 by Roxana Geambasu (Columbia)
- Mechanism design: [Differential Privacy in Game Theory and Mechanism Design](https://www.cis.upenn.edu/~aaroth/courses/gametheoryprivacyS14.html) Spring 2014 by Aaron Roth (Penn)
- Fairness: [CS 294: Fairness in Machine Learning](https://fairmlclass.github.io/) (UC Berkeley, Moritz Hardt)
- ML: [Privacy Preserving Machine Learning](https://researchers.lille.inria.fr/abellet/teaching/private_machine_learning_course.html) Spring 2022 by Aurelien Bellet (Inria)

### Books

#### Cryptography & MPC

- [The Joy of Cryptography](https://joyofcryptography.com/)
- [A Pragmatic Introduction to Secure Multi-Party Computation](https://securecomputation.org/)
- [A Graduate Course in Applied Cryptography](https://crypto.stanford.edu/~dabo/cryptobook/)
- [Handbook of Applied Cryptography](https://cacr.uwaterloo.ca/hac/)

#### Privacy-enhancing technologies (DP, anonymization)

- [The Algorithmic Foundations of Differential Privacy](https://www.cis.upenn.edu/~aaroth/Papers/privacybook.pdf)
- [Differential Privacy: From Theory to Practice](https://www.morganclaypool.com/doi/pdf/10.2200/S00735ED1V01Y201609SPT018)
- [The Complexity of Differential Privacy](https://privacytools.seas.harvard.edu/files/privacytools/files/complexityprivacy_1_01.pdf)
- [Differential Privacy: A Primer for a Non-Technical Audience](https://salil.seas.harvard.edu/files/salil/files/differential_privacy_primer_nontechnical_audience.pdf)
- [Protecting Your Privacy In A Data-driven World](https://www.clairemckaybowen.com/book)
- [Differential Privacy for Databases](https://dpfordb.github.io/)

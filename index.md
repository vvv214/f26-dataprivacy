---
---

# Data Privacy (Fall 2026)

## Course overview

This course asks how we can build useful data and AI systems without exposing
the people behind them. For three real privacy failures and the defenses that
answer them, see [Why take this course?](overview.html).

## Who should enroll?

This course is open to all undergraduates.

Required preparation:

- Completion of an introductory programming course plus at least one 2000-level
  computing course, or equivalent programming experience.
- Basic probability and statistics, including distributions, averages, and
  simple evaluation metrics.
- Be comfortable working with AI assistants to inspect code, debug, and
  organize an investigation while checking their claims against code, data,
  and tests.

Helpful UVA courses, but not prerequisites:

- CS 3710: Introduction to Cybersecurity, for threat models, attacks, and
  defenses.
- CS 4774: Machine Learning, for model training and evaluation.

No prior coursework in privacy, cybersecurity, machine learning, cryptography,
or AI is required.

The optional [readiness self-check](readiness.html) gives a concrete picture of
the programming, probability, and ML ideas used at the start of the course. It
is ungraded and is not an enrollment requirement.

## Course info

- Course: CS 4501-003, Special Topics in Computer Science: Data Privacy
- Instructor: [Tianhao Wang](https://tianhao.wang)
- Email: [tianhao@virginia.edu](mailto:tianhao@virginia.edu)
- Location: Olsson Hall 011
- Time: Tuesdays and Thursdays, 2:00-3:15 PM
- Dates: August 25-December 8, 2026
- Canvas: [course site](https://canvas.its.virginia.edu/courses/190753)
- Format: in-person lectures, short practicals, four varied labs, quizzes, Canvas check-ins, and a scoped final project
- Syllabus: [Fall 2026 syllabus](syllabus.html)
- Policies: [course policies](policy.html)

Announcements and assignment updates appear in Canvas. Use Canvas Inbox or
email for questions that involve grades, accommodations, or other private
matters.

## Grading

- [Labs](lab.html) (40%): four individual, equally weighted challenges covering privacy attacks, a two-agent secret arena, hidden tests, extensions to large DP codebases, and privacy-enhancing technologies.
- [Project](project.html) (30%): an innovative privacy system, tool, attack, defense, monitor/auditor, or research contribution, with an in-class project pitch (10%), proposal (5%), poster/demo (10%), and final report (5%). See the [milestone guide](project-present.html) and [project rubric](project-rubric.html).
- Quizzes (20%): two individual, in-class, closed-book paper quizzes worth 10% each.
- Exit surveys / check-ins (10%): short individual Canvas submissions completed across the semester for completion credit.
- Grading basis: we use the [UVA grading basis](https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=1153c16fdba41f444f32fb671d961934); letter-grade thresholds will appear in the [syllabus](syllabus.html).

## Schedule

{% include schedule.html %}

## More resources

### AI access

No paid AI subscription is required for this course. Students currently have
several optional access paths:

- [Gemini and NotebookLM through UVA](https://learningtech.virginia.edu/tools/gemini)
  are available to UVA faculty, staff, and students at no additional student
  cost.
- [UVA Copilot Chat](https://learningtech.virginia.edu/tools/copilot) is also
  university-licensed and available at no additional student cost.
- Eligible U.S. college students can claim the
  [2026 ChatGPT student offer](https://chatgpt.com/students/2026/) for four free
  months of ChatGPT Plus. The offer must be claimed by October 31, 2026,
  requires SheerID verification and a payment method, and renews at the regular
  monthly price unless canceled.
- [UVA RC GenAI](https://learning.rc.virginia.edu/notes/uva-rc-genai/) provides
  Kimi K2.5 through a browser and API at no charge to eligible Research
  Computing users. RC currently restricts this service to research use; it is
  not available for ordinary class assignments.

Access terms may change. Check the linked provider or UVA page before relying
on a particular service, and follow the course rules for private materials and
sensitive data.

### Courses

#### Core differential privacy

- [Algorithms for Private Data Analysis](https://www.gautamkamath.com/courses/CS860-wi2026.html) ([videos](https://www.youtube.com/playlist?list=PLmd_zeMNzSvRRNpoEWkVo6QY_6rR3SHjp)) Winter 2026 by Gautam Kamath (Waterloo)
- [Applied Privacy for Data Science](https://opendp.github.io/cs208/spring2025/) Spring 2025 by Salil Vadhan, James Honaker, and Priyanka Nanayakkara (Harvard)
- [Algorithmic Foundations of Differential Privacy](https://www.cs.jhu.edu/~mdinitz/classes/DP-class/Spring2025/) Spring 2025 by Michael Dinitz (Johns Hopkins)
- [Introduction to Differential Privacy: Theory, Algorithms and Applications](https://cseweb.ucsd.edu/~yuxiangw/classes/DSC291-2024Fall/) ([intro video](https://www.youtube.com/watch?v=OzjmWObjgzg)) Fall 2024 by Yu-Xiang Wang (UCSD)
- [Privacy in Statistics and Machine Learning](https://dpcourse.github.io/) ([videos](https://drive.google.com/drive/folders/1Ds5KlyWrX93DeiQWrFLpBS0Zsk104bnd?usp=sharing)) Spring 2023 by Adam Smith (BU) and Jonathan Ullman (NEU)
- [Algorithms for Private Data Analysis](https://www.cs.toronto.edu/~anikolov/CSC2412F20/CSC2412.html) Fall 2020 by Aleksandar Nikolov (UofT)

#### Broader privacy, systems, and machine learning

- PETs: [Privacy Enhancing Technologies](https://www.cs.unc.edu/~saba/priv_class/summer25/index.html) Summer 2025 by Saba Eskandarian (UNC)
- Theory: [The Algorithmic Foundations of Adaptive Data Analysis](https://adaptivedataanalysis.com/lecture-schedule-and-notes/) Fall 2017 by Aaron Roth (Penn) and Adam Smith (BU)
- Systems: [Private Systems](https://systems.cs.columbia.edu/private-systems-class/) Spring 2020 by Roxana Geambasu (Columbia)
- Mechanism design: [Differential Privacy in Game Theory and Mechanism Design](https://www.cis.upenn.edu/~aaroth/courses/gametheoryprivacyS14.html) Spring 2014 by Aaron Roth (Penn)
- Fairness: [CS 294: Fairness in Machine Learning](https://fairmlclass.github.io/), by Moritz Hardt (UC Berkeley)
- ML: [Privacy Preserving Machine Learning](https://researchers.lille.inria.fr/abellet/teaching/private_machine_learning_course.html), course materials from 2020-2023 by Aurélien Bellet (Inria)

### Tutorials and practical guidance

- [A friendly, non-technical introduction to differential privacy](https://desfontain.es/blog/friendly-intro-to-differential-privacy.html) builds intuition through examples and diagrams.
- [DifferentialPrivacy.org](https://differentialprivacy.org/) explains mechanisms, accounting, attacks, and recent research at several technical levels.
- The [NIST differential privacy blog series](https://www.nist.gov/itl/applied-cybersecurity/privacy-engineering/collaboration-space/blog-series/differential-privacy) introduces DP for practitioners; [NIST SP 800-226](https://csrc.nist.gov/pubs/sp/800/226/final) gives current guidance for evaluating real systems and common privacy hazards.
- [OpenDP Getting Started](https://docs.opendp.org/en/stable/getting-started/index.html) covers privacy units, budgets, tabular data, modeling, and utility in Python and R.
- [Tumult Analytics tutorials](https://docs.tmlt.dev/analytics/latest/tutorials/index.html) walk through private tabular queries using a Python interface.
- [Laplace vs. Gaussian](https://lpanavas.github.io/mechanism-comparison/) is an interactive visualization of privacy-utility tradeoffs.
- [DP Wizard classroom exercises](https://opendp.github.io/dp-wizard/) provide a lightweight, non-technical introduction to DP releases.

### Software

#### Lab and course libraries

- [Opacus](https://opacus.ai/) for private training in PyTorch.
- [JAX Privacy](https://jax-privacy.readthedocs.io/) for auditable DP training in JAX and Keras.
- [Google DPSynth](https://github.com/google/dpsynth) for differentially private tabular synthesis.
- [MP-SPDZ](https://github.com/data61/MP-SPDZ) for secure multi-party computation.

#### Additional libraries

- [OpenDP](https://docs.opendp.org/) for composable DP mechanisms and data analysis in Python, R, and Rust.
- [Tumult Analytics](https://www.tmlt.dev/) for scalable DP queries over tabular data.
- [Google Differential Privacy](https://github.com/google/differential-privacy) for production-oriented C++, Go, Java, and data-pipeline components.
- [diffprivlib](https://github.com/IBM/differential-privacy-library) for scikit-learn-style private models, mechanisms, and accounting in Python.

### Books

#### Cryptography & MPC

- [The Joy of Cryptography](https://joyofcryptography.com/)
- [A Pragmatic Introduction to Secure Multi-Party Computation](https://securecomputation.org/)
- [A Graduate Course in Applied Cryptography](https://crypto.stanford.edu/~dabo/cryptobook/)
- [Handbook of Applied Cryptography](https://cacr.uwaterloo.ca/hac/)

#### Differential privacy

- [Differential Privacy](https://mitdpbook.com/) by Simson L. Garfinkel (open-access, non-technical, 2025)
- [Programming Differential Privacy](https://programming-dp.com/)
- [Hands-On Differential Privacy](https://www.oreilly.com/library/view/hands-on-differential-privacy/9781492097730/)
- [The Algorithmic Foundations of Differential Privacy](https://www.cis.upenn.edu/~aaroth/Papers/privacybook.pdf)
- [Differential Privacy for Databases](https://dpfordb.github.io/)
- [The Complexity of Differential Privacy](https://salil.seas.harvard.edu/publications/complexity-differential-privacy)
- [Designing Access with Differential Privacy](https://admindatahandbook.mit.edu/book/v1.0/diffpriv.html)
- [Differential Privacy: A Primer for a Non-Technical Audience](https://scholarship.law.vanderbilt.edu/jetlaw/vol21/iss1/4/)
- [Protecting Your Privacy in a Data-Driven World](https://clairemckaybowen.com/book/)

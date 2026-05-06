---
---

# Data Privacy (Fall 2026 draft) lab syllabus

<nav class="course-nav" aria-label="Course pages">
  <a href="index.html">Home</a>
  <a href="schedule.html">Schedule</a>
  <a href="project.html">Project</a>
  <a href="project-rubric.html">Rubric</a>
  <a href="project-present.html">Milestones</a>
  <a href="policy.html">Policies</a>
</nav>

## Lab goals

The labs are where students move from vocabulary to actual technical reasoning. Each lab is designed to answer a concrete question:

- What can an attacker really do?
- What does a privacy defense protect, and what does it cost?
- How much of the difficulty is conceptual versus tooling?

## Group policy

- Labs are designed for teams of 2.
- Individual submission is allowed.
- You may keep the same partner all semester or switch partners between labs.
- Group members submit one shared notebook and receive the same grade unless there is a documented contribution issue.

## Format

- Labs are notebook-based and emphasize short written interpretations in addition to code.
- We provide scaffolded starter code. Students are still responsible for understanding outputs and explaining trade-offs.
- Most labs are intended for Google Colab or a lightweight local setup.
- Selected labs may include a short reading warm-up or reflection prompt.

## Distribution

Lab notebooks and support files will be distributed separately through the course workflow, such as Canvas or a shared Drive folder. They are not published as raw files from this public website repository.

## Lab 1: Privacy attacks on models

**Theme**: See the leak before you study the defense.

- Extract a memorized secret from a small language model.
- Use loss-based membership inference to distinguish a canary-trained model from a control model.
- Explore why simple keyword filters are weak defenses.

**Main learning outcome**: Students should be able to explain the difference between memorization, extraction, and inference attacks.

---

## Lab 2: Re-identification and reconstruction

**Theme**: Privacy can fail even when names are removed.

- Measure singling-out risk in synthetic microdata.
- Perform a linkage-style attack using quasi-identifiers.
- Reconstruct sensitive attributes from released statistics, then observe how DP noise changes feasibility.

**Main learning outcome**: Students should understand why de-identification alone is fragile and how statistical releases can still leak.

---

## Lab 3: Private learning

**Theme**: Protecting training is not free.

- Use DP-SGD on a small model and interpret the privacy / utility trade-off.
- Work with private selection ideas such as the exponential mechanism in a simplified setting.
- Compare centralized privacy with noisier local or federated variants.

**Instructor note for the undergraduate version**: the release should prioritize one clear core path over breadth. If needed, this lab can ship with a required core section plus one optional extension.

**Main learning outcome**: Students should be able to explain what the privacy budget buys, what it costs, and why implementation choices matter.

---

## Lab 4: Secure multi-party computation (MPC)

**Theme**: Private computation under different trust assumptions.

- Use MP-SPDZ to run basic MPC programs.
- Compare cheap operations (addition) with expensive ones (multiplication, comparison, ReLU).
- Study a simple private mean, a millionaire comparison, a toy private neural network, and a debugging exercise about incorrect reveals.

**Main learning outcome**: Students should leave with the right mental model for when MPC is appropriate and where the performance bottlenecks come from.

---

## Technical setup

### Default platform

- Google Colab is the default for most students.
- We provide starter notebooks and small helper files.
- Labs should avoid requiring specialized hardware beyond optional GPU access.

### Software expectations

- Lab 1-3 rely primarily on Python notebooks.
- Lab 4 uses MP-SPDZ rather than a full custom cryptographic implementation.
- When possible, released labs should prefer synthetic or lightweight data over large downloads.

### Instructional design guideline

For the undergraduate version, labs should reward interpretation and careful experimentation more than framework wrestling. If a toolchain becomes the main obstacle, the release should be simplified.

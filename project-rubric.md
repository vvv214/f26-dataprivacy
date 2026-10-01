---
---

# Project rubric

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

The innovative, open-topic project contributes **30%** of the course grade,
split across four milestones:

- **Project pitch (10%)**
- **Proposal (5%)**
- **Poster/demo (10%)**
- **Final report (5%)**

Projects are assessed against their approved question, method, and evidence.
There is no project competition or common leaderboard. For logistics, see the
[project milestone guide](project-present.html).

## 1. Project pitch (10 points)

| Criterion | Points | Description |
|---|---:|---|
| Privacy problem and stakes | 2 | The pitch identifies a concrete user, system, or scientific setting, protected asset, and meaningful privacy problem. |
| Innovation and baseline | 2 | The closest existing system or method is clear, along with the distinct capability, attack, defense, measurement, or insight the project may add. |
| Technical direction | 2 | The proposed artifact or research method is concrete enough to evaluate for coherence and course fit. |
| Evidence and feasibility | 2 | The pitch names a plausible evaluation path, available resources, and a serious scope or technical risk. |
| Delivery and response | 2 | The presentation is focused, uses its time effectively, and answers a brief question accurately. |

## 2. Proposal (5 points)

The proposal has **10 checks worth 0.5 points each**. Each row below is worth
1 point: 0.5 for check A and 0.5 for check B. The total is 5 points, contributing
5% of the course grade.

| Criterion | Check A: 0.5 points | Check B: 0.5 points |
|---|---|---|
| Problem and threat model | Names the target user or system, the protected data or asset, and the concrete problem the project will address. | Specifies the attacker or unwanted disclosure, what can be observed or queried, and the trust boundary and failure condition. A theoretical or non-adversarial project may instead specify its privacy property, protected unit, released information, and assumptions. |
| Innovation and grounding | Names and cites at least one closest existing method, system, or result, and identifies a specific limitation relevant to this project. | States one proposed technical difference from that baseline and gives a concrete example, testable hypothesis, or formal statement that would distinguish the contribution from it. The difference must address the identified limitation. |
| Current technical work | Describes the proposed method's inputs, outputs, and main processing or reasoning steps, including where private information is accessed or released when applicable. | Provides one inspectable current artifact, such as a code snapshot, experiment log, instrumented dataset, or proof component. Points to the relevant file, output, or excerpt and labels what is completed and what is planned. |
| Evidence and evaluation | Reports at least one current test, measurement, worked example, or checked proof step. Gives the setup, observed result or documented failure, and what it supports or leaves unresolved. | Specifies the remaining test cases or data, at least one baseline, a primary metric or formal verification target, and an explicit rule for deciding whether the main claim is supported, weakened, or inconclusive. Includes the planned test scale, splits, and seeds when applicable. |
| Remaining scope | Lists at least two dated remaining milestones with a deliverable for each, leading to the final submission. Assigns an owner to each task, including for an individual project. | Names at least one technical, data, or compute risk, a condition that would trigger a scope change, and the concrete fallback deliverable. Identifies the code/configuration, data, or assumptions needed to reproduce or check the final evidence. |

**How points are assigned**

- Award **0.5** for a check when all its listed components are present,
  specific to the project, and technically consistent with the stated setting.
  Current-work and evidence claims must be supported by the cited artifact or
  excerpt. Otherwise award **0** for that check. This gives each row a score of
  **0, 0.5, or 1**.
- Record each check separately. For a check receiving 0, identify the missing
  or unsupported component and its location in the submission, or state that
  it is absent. Sum the ten checks to obtain the score.
- A documented failure or negative result can earn full evidence credit when
  its setup, observation, and interpretation meet the check. At this milestone,
  the proposed improvement may remain unproven; a testable evaluation plan and
  accurate current status satisfy the corresponding checks.
- Code volume, visual polish, model size, and a positive result do not add
  proposal points. Choose evidence appropriate to the format: a theory project
  can supply a checked derivation or counterexample; a system or empirical
  project can supply a test, log, or pilot measurement.

In the 1-2 page proposal, make these checks easy to locate. Supporting artifacts
may be identified by a link, filename and version, or a labeled excerpt; ten
separate sections are not required.

## 3. Poster/demo (10 points)

| Criterion | Points | Description |
|---|---:|---|
| Contribution and technical substance | 3 | The completed contribution, method, and system or research artifact are understandable and technically sound. |
| Innovation | 2 | The presentation demonstrates a meaningful difference from the closest baseline or prior workflow. |
| Evidence | 2 | The presentation shows concrete results, comparisons, failures, or analytical support rather than only describing an idea. |
| Poster or demonstration quality | 2 | The poster or live demo makes the workflow and main result easy to inspect and is readable or reliable in the presentation setting. |
| Limitations and response | 1 | The team answers questions accurately, states limitations without overclaiming, and identifies each member's contribution. |

## 4. Final report (5 points)

| Criterion | Points | Description |
|---|---:|---|
| Technical execution and contribution | 2 | The report explains a correctly executed method and the completed contribution relative to the baseline. |
| Evidence and baselines | 1 | Results use appropriate comparisons and auditable evidence at a scale suitable for the claim. |
| Analysis and limitations | 1 | Conclusions match the evidence and address failures, residual risks, and threats to validity. |
| Clarity, artifacts, and contributions | 1 | The report is organized and cited, and supporting artifacts and team contributions are documented appropriately. |

## Additional notes

1. **Innovation is required, but publication-level novelty is not.** A project
   must add a meaningful capability, attack, defense, measurement, system
   boundary, interaction, or insight. A reproduction, routine comparison,
   literature review, mechanical port, or incremental extension alone does not
   satisfy the requirement.
2. **Claims should match evidence.** A narrow, carefully tested conclusion is
   stronger than a broad claim with thin support.
3. **Auditability matters.** Include counts, splits, seeds, prompts, configs,
   examples, derivations, or logs as appropriate to the project.
4. **Different formats need different evidence.** A system needs tests and
   realistic workflows; an attack or defense needs a threat model and controls;
   a monitor or auditor needs verified positives and clean cases; an empirical
   paper needs a defensible design; and a theoretical paper needs precise
   assumptions and reasoning.
5. **Visuals support communication.** Figures and tables should make the main
   comparison or conclusion easy to see, but polish cannot replace evidence.
6. **Individual and group scope may differ.** Individuals may submit narrower
   projects. Teams of 2 should show broader experiments, stronger comparisons,
   or a more complete system.
7. **Contribution statements are required.** Substantial contribution
   imbalances may lead to adjusted individual grades.

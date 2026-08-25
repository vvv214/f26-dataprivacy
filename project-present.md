---
---

# Project milestone guide

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

This page covers the presentation-style and checkpoint-style project milestones
for Fall 2026. Projects remain open in topic and method; these milestones keep
the work scoped and provide feedback without putting projects into a shared
competition. All grading criteria are centralized in the
[project rubric](project-rubric.html).

## 1. Topic check-in (Week 7, 3%)

**Objective**

Get feedback before the project becomes too large or too vague.

**Format**

- one-page memo; or
- short lightning talk if class time permits.

**Expectations**

- State the privacy question clearly.
- Name the dataset, model, system, protocol, or analytical setting.
- Identify a plausible method and one or two sources or baselines.
- Identify one obvious risk to feasibility.

## 2. Proposal (Week 10, 5%)

**Objective**

Define a realistic technical plan and the evidence needed to support the final
claim.

**Expectations**

- Write 1-2 pages.
- Include the question, motivation, related work, method, evaluation plan, and
  scope control.
- Define the relevant threat model or privacy property when the project needs
  one.
- State what evidence would support, weaken, or leave the main claim
  inconclusive.
- Include expected datasets, metrics, baselines, sample or query counts, splits,
  seeds, and artifacts when applicable.
- Include a timeline, fallback scope, and contribution statement for a team.

## 3. Progress checkpoint (Week 12, 7%)

**Objective**

Demonstrate substantial progress early enough to correct the method, evaluation,
or scope before the final submission.

**Submit or present**

- a working artifact, analysis pipeline, proof outline, dataset, or other
  evidence package appropriate to the project;
- a reproducible snapshot with the version, environment, commands, inputs, and
  current outputs, when the project includes code;
- preliminary results, including failures or inconclusive findings rather than
  only the best case;
- a short account of what the evidence currently supports and what remains
  uncertain; and
- a revised plan for the final weeks, including any justified scope change.

The checkpoint is evaluated against the project's own approved question and
method. It is not a competition, peer attack, or common leaderboard.

## 4. Poster/demo (Week 15, 5%)

**Objective**

Present the project clearly to classmates who may not know the exact topic.

**Expectations**

- Use a research-style poster or a structured live demo.
- Cover the question, setup, method, main evidence, and limitations.
- Include a representative failure, negative result, or boundary case when it
  helps explain the conclusion.
- Make plots and tables readable from a normal viewing distance.
- Be ready to explain what each team member contributed.

## 5. Final report (Week 16, 10%)

**Objective**

Submit the full technical write-up.

**Expectations**

- Explain the question, setup, method, evidence, and limitations.
- Cite the main sources and tools on which the work depends.
- Keep the report focused on what the evidence supports rather than inflated
  claims.

**Final report checklist**

- State the privacy question or technical objective clearly.
- Describe the data, model, system, protocol, or analytical setting.
- Explain the method in enough detail to evaluate it.
- Report exact counts, splits, seeds, queries, or trials when they matter.
- Include meaningful baselines and metrics.
- Use uncertainty estimates, repeated runs, sensitivity analysis, or exact
  counts when the result depends on sampling.
- Show representative examples, logs, failure cases, or intermediate evidence
  when they help verify the result.
- Distinguish supported conclusions from inconclusive or unsupported claims.
- Explain limitations, residual risks, and threats to validity plainly.
- Link code, configs, notebooks, or other artifacts when appropriate, without
  publishing sensitive data.
- Include a short contribution statement for each team member.
- If AI materially shaped the work, include an AI Decision Ledger with 5-10
  consequential suggestions, how each was checked, and what was decided.

Common pitfalls to avoid:

- Do not call a heuristic defense differential privacy unless you define the
  released output, adjacency, sensitivity (or clipping and public bounds), and
  privacy accounting.
- For RAG or retrieval systems, distinguish noisy ranking from privacy for the
  returned documents.
- For side-channel experiments, avoid random splits that mix the same session,
  capture, user, or trace across train and test when testing generalization.
- If you use an LLM judge, include validation examples, manual checks, or a
  calibration procedure.

---
---

# Project milestone guide

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

This page covers the four project milestones for Fall 2026. Projects remain
open in topic and method, but each project must make an innovative privacy
contribution. The milestones provide an early public pitch, one written
proposal that also checks progress, and two final deliverables without putting
projects into a shared competition. All grading criteria are centralized in the
[project rubric](project-rubric.html).

## 1. Project pitch (Week 7, 10%)

**Objective**

Make a concise case for an interesting privacy contribution and get feedback
before committing to the full design.

**Format**

- The class devotes one full meeting to live pitches.
- Each project receives a short timed slot; exact timing will be announced once
  teams are finalized.
- Use one slide. All team members should be present and ready to answer a brief
  question.

**Expectations**

- State the target user or setting and privacy problem clearly.
- Identify the closest existing system, method, or workflow and its limitation.
- State what system, tool, attack, defense, monitor/auditor, or research
  contribution you propose to create.
- Explain the core technical idea and what would become newly possible,
  measurable, or defensible.
- Name the main evidence you would collect and one serious feasibility risk.

## 2. Proposal (Week 11, 5%)

**Objective**

Turn the pitch into a realistic technical plan while showing enough current
work to identify problems before the final weeks.

**Expectations**

- Write 1-2 pages.
- Include the problem, motivation, related work, innovation claim, technical
  design, evaluation plan, and scope control.
- Separate completed work from planned work. Include a current artifact,
  experiment, proof component, dataset instrument, or other concrete evidence
  appropriate to the project.
- Report an initial result, failure, or unresolved technical question rather
  than showing only a best case.
- Define the relevant threat model or privacy property when the project needs
  one.
- State what evidence would support, weaken, or leave the main claim
  inconclusive.
- Include expected datasets, metrics, baselines, sample or query counts, splits,
  seeds, and artifacts when applicable.
- Include a timeline, fallback scope, and contribution statement for a team.

## 3. Poster/demo (Week 16, 10%)

**Objective**

Present the project clearly to classmates who may not know the exact topic.
The class holds one poster/demo session during the final meeting.

**Expectations**

- Use a research-style poster or a structured live demo.
- Cover the question, setup, method, main evidence, and limitations.
- Make the contribution and what is new relative to the baseline easy to see.
- Include a representative failure, negative result, or boundary case when it
  helps explain the conclusion.
- Make plots and tables readable from a normal viewing distance.
- Be ready to explain what each team member contributed.

## 4. Final report (Week 16, 5%)

**Objective**

Submit a focused technical write-up whose claims match the completed artifact
and evidence.

**Expectations**

- Explain the question, setup, method, evidence, and limitations.
- Cite the main sources and tools on which the work depends.
- Keep the report focused on what the evidence supports rather than inflated
  claims.

**Final report checklist**

- State the privacy question or technical objective clearly.
- State the innovation claim and compare the completed contribution with the
  closest baseline or prior workflow.
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

- A reproduction, routine comparison, literature review, mechanical port, or
  incremental extension alone does not satisfy the project requirement.
- Do not call a heuristic defense differential privacy unless you define the
  released output, adjacency, sensitivity (or clipping and public bounds), and
  privacy accounting.
- For RAG or retrieval systems, distinguish noisy ranking from privacy for the
  returned documents.
- For side-channel experiments, avoid random splits that mix the same session,
  capture, user, or trace across train and test when testing generalization.
- If you use an LLM judge, include validation examples, manual checks, or a
  calibration procedure.

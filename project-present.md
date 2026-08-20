---
---

# Project milestone guide

This page covers the presentation-style or checkpoint-style project milestones for Fall 2026.
All grading criteria are centralized in the [project rubric](project-rubric.html).

## 1. Topic check-in (Week 7)

**Objective**

Get feedback before the project becomes too large or too vague.

**Format**

- one-page memo, or
- short lightning talk if we have enough class time

**Expectations**

- State the privacy question clearly.
- Name the dataset, model, or system setting.
- List one or two likely baselines.
- Identify one obvious risk to feasibility.

## 2. Proposal (Week 10)

**Objective**

Lock in a realistic technical plan.

**Expectations**

- 1-2 pages.
- Include motivation, threat model, related work, method, evaluation plan, and scope control.
- Define the frozen artifact another team can challenge and one realistic transfer condition.
- Include expected evidence: datasets, metrics, baselines, sample/query/trial counts, splits, seeds, and artifacts you plan to report.
- Include a short contribution statement if you are working in a team.

## Formative break exchange (Week 13)

The instructor will pair teams and provide a bounded review protocol. Freeze a compact artifact that another team can run without private data or paid resources. Reviewers submit one reproducible challenge, clean finding, or insufficient-evidence finding. Authors then explain the root cause, repair or narrow the claim, and add a regression test.

The exchange is part of course participation rather than a separate project milestone grade. Quality still matters because its evidence feeds the poster, report, and oral defense.

## 3. Poster / demo (Week 15)

**Objective**

Present your results clearly to classmates who may not know your exact topic.

**Expectations**

- Use a research-style poster or a structured live demo.
- Cover motivation, setup, method, main result, break finding, repair, transfer status, and limitations.
- Make plots and tables readable from a normal viewing distance.
- Be ready to explain what each team member worked on.

## 4. Final report (Week 16)

**Objective**

Submit the full technical write-up.

**Expectations**

- Explain the question, setup, build, break finding, repair, transfer result, and limitations.
- Cite the main sources you built on.
- Keep the report focused on evidence and analysis rather than inflated claims.

**Final report checklist**

Your report should make it easy to understand what was tested and what the evidence supports:

- State the threat model or privacy question in one clear paragraph.
- Describe the data, model, system, or protocol setting.
- Report exact counts: samples, queries, prompts, trials, seeds, and train/test or grouped splits.
- Include baselines and metrics that match the claim.
- Include the challenge input, root-cause evidence, repair, and regression test.
- Explain the transfer condition and what did or did not generalize.
- Use uncertainty estimates, repeated runs, or exact count tables when results depend on sampling.
- Show representative examples, logs, prompts, judge prompts, or failure cases when they help verify the result.
- Explain limitations plainly, especially when the evaluation is small or the threat model is narrower than the motivation.
- Link code, configs, notebooks, or other artifacts when appropriate, without publishing private or sensitive data.
- Include a short contribution statement for each team member.

Common pitfalls to avoid:

- Do not call a heuristic defense "differential privacy" unless you define the released output, adjacency relation, sensitivity or clipping/public bounds, and privacy accounting.
- For RAG or retrieval systems, distinguish noisy ranking from privacy for the returned documents.
- For side-channel experiments, avoid random splits that mix the same session, capture, user, or trace across train and test when the goal is generalization.
- If you use an LLM judge, include validation examples, manual spot checks, or a calibration procedure.

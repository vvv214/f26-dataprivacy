---
---

# Project (Fall 2026 draft)

The final project is meant to help students go deeper on one privacy topic without turning the course into a full research seminar. The strongest undergraduate projects are usually well-scoped, technically correct, and honest about limitations.

## Project scope

Projects should connect to one or more course themes:

- privacy attacks and auditing
- differential privacy
- privacy in machine learning systems
- privacy-enhancing technologies such as MPC, HE, TEE, or network privacy

Projects do not need to be novel research. A strong project can reproduce an existing result, compare methods carefully, build a small prototype, or apply a known method to a new setting.

## Recommended project tracks

- **Replication + extension**: reproduce one paper, system, or benchmark, then add one meaningful extension or ablation.
- **Comparative evaluation**: compare several privacy attacks or defenses on a shared task and explain the trade-offs.
- **Build / application**: implement a small privacy-aware tool, pipeline, or demo and evaluate where it works and where it breaks.

## Team policy

- Teams of up to 2 are allowed.
- Individual projects are welcome and may have narrower scope.
- Teams of 2 are expected to show broader execution than individuals, but the grading standard is still correctness, clarity, and evidence rather than raw project size.
- Every submission must include a short contribution statement for each member.

## Milestones at a glance

| Milestone | Week(s) | Format | Weight |
|---|---|---|---|
| Topic check-in | 7 | one-page memo or lightning talk | 5% |
| Proposal | 9 | written plan (1-2 pages) | 5% |
| Poster / demo | 15 | poster-style presentation or live demo | 10% |
| Final report | 16 | written report | 10% |

For milestone logistics, see [project milestone guide](project-present.html).
For grading details, see [project rubric](project-rubric.html).

## Suggested project directions

- Compare extraction or membership inference attacks across simple model settings.
- Benchmark privacy / utility trade-offs for DP training on a small task.
- Audit the privacy risks of a logging, telemetry, or recommendation workflow.
- Compare MPC, HE, and TEE for a toy inference or analytics pipeline.
- Study privacy risks in RAG, agent traces, or retrieval logs using a scoped benchmark.
- Build a small teaching demo that illustrates a privacy mechanism or attack.

## Scope guardrails

- Avoid projects that depend on frontier-scale training or expensive compute.
- Prefer reproducible datasets, lightweight models, and a clear baseline.
- If you choose an ambitious topic, narrow the evaluation rather than overpromising.
- A careful negative result is acceptable if the execution and analysis are strong.

## Evidence expectations

Strong projects make the evidence easy to audit. In the proposal and final report, be concrete about:

- **Scale**: report dataset size, number of prompts or queries, number of trials, number of seeds, and any train/test split.
- **Threat model**: state who the attacker is, what they observe, what they are allowed to query, and what counts as a privacy failure.
- **Baselines**: compare against at least one simple baseline. If your project is a defense, include a no-defense or weak-defense condition.
- **Uncertainty**: use repeated runs, error bars, confidence intervals, or exact count tables when the result depends on sampling.
- **Artifacts**: include enough detail for review: code link if appropriate, configs, prompts, judge prompts, representative logs, or example outputs. Do not include private student or sensitive data.
- **Visuals**: figures and tables should be readable without zooming. Captions should explain the takeaway, not just name the plot.

Be careful with privacy claims:

- A heuristic defense is fine, but do not call it differential privacy unless you define adjacency, sensitivity or clipping/public bounds, privacy accounting, and the released output.
- For RAG systems, adding noise to retrieval scores and returning raw private documents is not the same thing as document-level DP.
- For side-channel projects, avoid random splits that leak information across the same session, capture, user, or trace. Use grouped splits when the threat model requires generalization.
- If you use an LLM judge, validate it with examples, manual spot checks, or a clear calibration procedure.

## Proposal and final report template

Use this structure for the proposal, then expand it for the final report.

1. **Title + team**: project title, members, and roles.
2. **Motivation**: what problem you are studying and why it matters.
3. **Setting / threat model**: what data, model, or system you consider and what privacy risk you focus on.
4. **Related work**: the main prior work you build on.
5. **Approach**: what you will implement, compare, or analyze.
6. **Evaluation plan**: datasets, metrics, baselines, and what evidence will count as success.
7. **Scope control**: what you will leave out if time or compute becomes tight.
8. **Evidence log**: expected sample/query/trial counts, splits, seeds, artifacts, and examples you will report.
9. **Contribution statement**: who is doing what.

## Deliverable expectations

- **Topic check-in**: a feasible idea with enough technical detail to get feedback early.
- **Proposal**: a concrete evaluation plan and realistic scope.
- **Poster / demo**: clear communication of the question, method, and results.
- **Final report**: technical write-up with evidence, limitations, and discussion.

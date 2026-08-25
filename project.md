---
---

# Project

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

The final project is an open opportunity to go deeper on a privacy topic. You
choose the question, method, and form of the contribution. Strong undergraduate
projects are well scoped, technically correct, supported by evidence, and
honest about limitations.

There is no project leaderboard, arena, or required peer attack. Some labs use
hidden evaluation or controlled arenas; the project does not.

## Project scope

Projects should connect to one or more course themes:

- privacy attacks and auditing;
- differential privacy;
- privacy in machine-learning or AI systems; or
- privacy-enhancing technologies such as secure multi-party computation (MPC),
  homomorphic encryption (HE), trusted execution environments (TEEs), or
  network privacy.

Novel research is not required. A careful reproduction, useful negative result,
or well-supported comparison can be as strong as a new prototype.

## Possible project formats

- **Replication and extension**: reproduce a paper, system, or benchmark, then
  add a meaningful extension, ablation, or new setting.
- **Comparative evaluation**: compare privacy attacks, defenses, or tools on a
  shared task and explain the trade-offs.
- **Build or application**: implement a small privacy-aware tool, pipeline, or
  demo and evaluate where it works and fails.
- **Audit or case study**: investigate a concrete system, dataset, or privacy
  claim using a clearly defined threat model and reproducible evidence.
- **Analytical project**: study a theoretical, legal-technical, measurement, or
  design question when the proposed method supports a rigorous conclusion.

These are examples, not tracks. Other formats are welcome when the proposal
defines a feasible question and a credible way to evaluate it.

## Team policy

- Teams of up to 2 are allowed.
- Individual projects are welcome and may have narrower scope.
- Teams of 2 are expected to show broader execution than individuals, but the
  standard remains correctness, clarity, and evidence rather than raw size.
- Every submission must include a short contribution statement for each member.

## Milestones at a glance

| Milestone | Week(s) | Format | Weight |
|---|---|---|---:|
| Topic check-in | 7 | one-page memo or lightning talk | 3% |
| Proposal | 10 | written technical plan | 5% |
| Progress checkpoint | 12 | working artifact or evidence package and update | 7% |
| Poster/demo | 15 | poster-style presentation or live demo | 5% |
| Final report | 16 | written report | 10% |

For milestone logistics, see the [project milestone guide](project-present.html).
For grading details, see the [project rubric](project-rubric.html).

During the Week 15 poster/demo sessions, each student also completes the second
brief individual written artifact check using an instructor-selected excerpt
from the team's project. It counts toward participation, not the project grade.

## Suggested directions

- Compare extraction or membership-inference attacks across simple model
  settings.
- Benchmark privacy-utility trade-offs for DP training on a small task.
- Audit the privacy risks of a logging, telemetry, or recommendation workflow.
- Compare MPC, HE, and TEEs for a toy inference or analytics pipeline.
- Build a small teaching demo that illustrates a privacy mechanism or attack.
- Build a claim-verification tool that connects natural-language conclusions to
  code, data, logs, and executable evidence.

### LLM and agent privacy

Assistants that carry memory, retrieve documents, and call tools create privacy
surfaces that classical threat models do not cover. Lab 3 attacks these systems
under a fixed contract; a project can go further, take the defender's side, or
measure something the lab only samples. All of these are feasible on small
open models or a bounded API budget with synthetic data.

- **Memory isolation under adversarial use**: plant canaries in one session or
  user profile and measure recovery from another. Compare isolation strategies
  (per-user namespaces, summarization, retrieval filters) on both leakage and
  assistant usefulness.
- **Indirect prompt injection as an exfiltration channel**: measure how often a
  planted instruction in a retrieved document reaches a tool that can send or
  write. The interesting variable is tool permission design, not phrasing.
- **What actually leaks from RAG**: distinguish verbatim document disclosure,
  paraphrased disclosure, and membership evidence about the index. State what a
  document-level guarantee would require and whether your defense provides it.
- **Deletion and unlearning for assistant memory**: after a deletion request,
  test whether the fact survives in summaries, embeddings, caches, or logs.
- **Agent traces and telemetry**: audit what a trace, log, or eval dataset
  captures; build a scrubber and report its false-negative and false-positive
  rates rather than examples.
- **PII redaction filters under stress**: measure where detectors fail
  (unusual name forms, non-English text, indirect identifiers, encodings) and
  what that implies for systems that rely on them.
- **LLM-assisted re-identification**: compare an LLM inference pipeline against
  a classical linkage baseline on the same synthetic population. The question is
  whether the capability changes the risk, and by how much.
- **Shared-infrastructure side channels**: study whether response timing or
  cache behavior reveals another tenant's prompt prefix in a locally hosted
  serving stack. Ambitious; narrow the claim carefully.
- **DP for text pipelines**: DP fine-tuning or DP synthetic text on a small
  model, reporting the utility cost honestly at usable privacy parameters.

## Scope guardrails

- Avoid projects that depend on frontier-scale training or expensive compute.
- Prefer reproducible datasets, lightweight models, and a clear baseline.
- If the topic is ambitious, narrow the evaluation rather than overpromising.
- A careful negative or inconclusive result is acceptable when the execution
  and analysis are strong.

## Evidence expectations

The right evidence depends on the project. Define it in the proposal and make
it easy to audit in the final report. Where relevant, report:

- **Scale**: dataset size, prompts or queries, trials, seeds, and data splits.
- **Threat model**: the protected asset, attacker, observations, capabilities,
  and failure condition.
- **Baselines**: at least one meaningful point of comparison, including a
  no-defense or weak-defense condition for defense projects when appropriate.
- **Uncertainty**: repeated runs, error bars, confidence intervals, sensitivity
  analysis, or exact counts when sampling matters.
- **Artifacts**: code, configs, prompts, representative logs, examples, proofs,
  or other material needed to check the result. Do not publish sensitive data.
- **Limitations**: failed cases, unsupported claims, and conditions under which
  the result may not generalize.
- **Visuals**: readable figures and tables whose captions explain the takeaway.

Be careful with privacy claims:

- Do not call a heuristic defense differential privacy unless you define the
  released output, adjacency, sensitivity (or clipping and public bounds), and
  privacy accounting.
- For RAG systems, adding noise to retrieval scores while returning raw private
  documents is not document-level DP.
- For side-channel projects, use grouped splits when random splits would leak
  information across the same user, session, capture, or trace.
- If you use an LLM judge, validate it with examples, manual checks, or a clear
  calibration procedure.
- For attacks on LLM or agent systems, count a leak only when a planted secret
  is verified. A refused request that was talked around, a plausible-looking
  name, or a guessed value is not evidence. Report the query and token budget,
  the number of attempts, and how many independent targets you tested, since a
  single lucky transcript says almost nothing.

## Proposal and final report template

Use this structure for the proposal, then expand it as appropriate for the
final report.

1. **Title and team**: project title, members, and roles.
2. **Question and motivation**: what you are studying and why it matters.
3. **Setting or threat model**: data, model, system, protocol, or analytical
   setting and the privacy property of interest.
4. **Related work**: the main work or tools you build on.
5. **Approach**: what you will implement, compare, measure, prove, or analyze.
6. **Evaluation plan**: evidence, datasets, metrics, baselines, and criteria for
   a supported, unsupported, or inconclusive result.
7. **Risks and limitations**: likely validity, privacy, engineering, compute, or
   data constraints.
8. **Scope and execution plan**: milestones, fallback scope, and what will be
   left out if time becomes tight.
9. **Evidence log**: expected counts, splits, seeds, artifacts, and examples,
   where applicable.
10. **Contribution statement**: who is doing what.

## Deliverable expectations

- **Topic check-in**: a feasible idea with enough technical detail for useful
  feedback.
- **Proposal**: a concrete method and evaluation plan with realistic scope.
- **Progress checkpoint**: meaningful technical progress, initial evidence, a
  reproducible snapshot, and a revised plan for the remaining work.
- **Poster/demo**: a clear account of the question, method, evidence, and
  limitations.
- **Final report**: a focused technical write-up whose claims match the evidence.
- **AI Decision Ledger**: include one with any milestone materially shaped by
  AI. For each of 5-10 consequential decisions, record the suggestion received,
  how it was checked, and what was decided.

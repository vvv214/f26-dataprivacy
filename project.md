---
---

# Project

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

The final project asks you to develop and evaluate an innovative privacy
contribution. It may be a system or focused tool, a new attack or defense, a
privacy monitor or auditor, or a research project whose primary artifact is a
paper. Strong undergraduate projects are interesting, technically complete,
supported by evidence, and honest about limitations.

## Project scope

Every project must:

- identify a target user, system, or scientific setting; a protected asset; and
  a privacy failure or limitation;
- deliver a concrete contribution appropriate to the project: a runnable
  prototype, attack implementation, defense, monitor/auditor, method, dataset,
  or research paper with auditable technical evidence;
- state an innovation claim: what new capability, attack, defense, measurement,
  insight, or design does the project provide?;
- compare against a meaningful baseline or current workflow; and
- evaluate the main claim with relevant privacy, utility, reliability,
  statistical, performance, or usability evidence.

The contribution should connect to one or more course themes:

- privacy attacks and auditing;
- differential privacy;
- privacy in machine-learning or AI systems; or
- privacy-enhancing technologies such as secure multi-party computation (MPC),
  homomorphic encryption (HE), trusted execution environments (TEEs), or
  network privacy.

You may build on existing papers, libraries, models, and codebases, but the
project contribution cannot be only a reproduction, port, benchmark comparison,
standalone audit, or incremental extension of an existing artifact. Those may
be inputs or baselines for the project, not the final contribution.

Publication-level novelty is not required. Here, innovation means asking a
non-obvious question or making and defending a nontrivial technical choice that
creates a distinct capability, attack, defense, measurement, or insight. The
proposal must answer: what becomes newly possible, measurable, or defensible
relative to the baseline?

## What can be innovative?

- **Workflow**: protect a real action that existing privacy research leaves
  awkward or manual.
- **Integration**: connect a privacy mechanism to a browser, local model,
  developer tool, data pipeline, or agent system in a technically meaningful
  way.
- **Interaction**: help a user understand, configure, or override a privacy
  decision without exposing more information.
- **Policy or architecture**: enforce a new boundary across users, memories,
  tools, data releases, or trust domains.
- **Defense**: combine detection, transformation, access control, accounting,
  or verification into a protection with measurable behavior.
- **Attack or measurement**: expose a previously untested privacy boundary or
  develop a more informative way to observe leakage.
- **Research insight**: formulate and support an original empirical,
  theoretical, or systems claim in a paper with auditable evidence.

These are examples, not tracks. The contribution can be compact, especially for
an individual project, but it must go beyond moving an existing technique to a
new library, platform, model, or dataset without a substantive new question or
design.

## Team policy

- Teams of up to 2 are allowed.
- Individual projects are welcome and may have narrower scope.
- Teams of 2 are expected to show broader execution than individuals, but the
  standard remains correctness, clarity, and evidence rather than raw size.
- Every submission must include a short contribution statement for each member.

## Milestones at a glance

| Milestone | Week(s) | Format | Weight |
|---|---|---|---:|
| Project pitch | 7 | short in-class presentation | 10% |
| Proposal | 11 | written plan with current artifact or evidence | 5% |
| Poster/demo | 16 | poster-style presentation or live demo in the final class | 10% |
| Final report | 16 | focused written report | 5% |

For milestone logistics, see the [project milestone guide](project-present.html).
For grading details, see the [project rubric](project-rubric.html).

## Suggested directions

These examples are starting points, not a fixed menu. Students may define any
original privacy-related direction that fits the project scope.

- **Browser or local privacy tools**, such as a privacy guard or local LLM
  rewriter.
- **Agent privacy**, including memory isolation, tool permissions, RAG
  disclosure control, privacy firewalls, and sandboxing.
- **Privacy leakage monitors or auditors** for model internals, caches, logs,
  data pipelines, or deployed systems.
- **New privacy attacks or defenses** for models, agents, applications, or data
  releases.
- **Private data and DP systems**, including release assistants, implementation
  auditors, synthetic data, or private training workflows.
- **PET-backed applications** using MPC, HE, TEEs, ORAM, or related techniques.
- **Privacy-preserving evaluation systems**, such as a safer LLM leaderboard or
  an auditable human/AI evaluation platform.
- **Evidence-backed privacy research tools** that connect claims to code, data,
  logs, and executable checks.
- **Privacy policy and contextual-integrity tools** for resolving inappropriate
  information flows across users, platforms, and AI systems.
- **Original research**, including an empirical, systems, theoretical, attack,
  or defense paper supported by a new technical contribution.

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
final report. Because the proposal is submitted in Week 11, it must distinguish
completed work from planned work and include current evidence or a concrete
artifact snapshot.

1. **Title and team**: project title, members, and roles.
2. **Target and setting**: who or what system is affected, and what workflow or
   scientific question will the project change?
3. **Privacy problem and threat model**: protected asset, attacker or unwanted
   flow, observations, trust boundary, and failure condition.
4. **Innovation claim**: what capability or design is new relative to the
   baseline?
5. **Related systems and baseline**: what you build on and what current workflow
   you will compare against.
6. **Technical design**: architecture, interface, method, data flow, attack or
   defense logic, trust assumptions, and the artifact you will implement.
7. **Evaluation plan**: privacy, utility, reliability, latency, or usability
   evidence, including meaningful baselines and failure cases.
8. **Risks and limitations**: likely validity, privacy, engineering, compute, or
   data constraints.
9. **Scope and execution plan**: milestones, fallback system, and what will be
   left out if time becomes tight.
10. **Current status**: what has been built or tested, current evidence or
    failures, and the next technical risk to resolve.
11. **Contribution statement**: who is doing what.

## Deliverable expectations

- **Project pitch**: a short in-class argument for the privacy problem,
  innovative contribution, technical approach, and feasible evaluation.
- **Proposal**: a concrete technical design and evaluation plan, together with
  the current artifact or evidence and a realistic plan for the remaining
  weeks. This submission also serves as the project's progress and scope check.
- **Poster/demo**: a demonstration or technically concrete presentation of the
  contribution, privacy behavior, evidence, and limitations.
- **Final submission**: the system, tool, attack, defense, monitor, auditor, or
  research artifact, plus a focused technical report whose claims match the
  evidence.
- **AI Decision Ledger**: include one with any milestone materially shaped by
  AI. For each of 5-10 consequential decisions, record the suggestion received,
  how it was checked, and what was decided.

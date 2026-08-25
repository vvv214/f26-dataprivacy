---
---

# Labs

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

The seven labs put you in different roles: attacker, data-release auditor,
anonymous evaluator, library maintainer, data publisher, and protocol
implementer. Some are compact challenges; others ask you to work in a real
privacy codebase. Together they contribute 30% of the course grade.

| Lab | Weight | Timing |
|---|---:|---|
| 1. Model Privacy CTF | 3% | Weeks 2-3 |
| 2. Linkage and Reconstruction | 4% | Weeks 3-5 |
| 3. LLM Privacy Attack Arena | 4% | Weeks 4-6 |
| 4. DP Training Systems | 5% | Weeks 6-9 |
| 5. DPSynth Feature Sprint | 6% | Weeks 8-11 |
| 6. Synthetic Data Arena | 5% | Weeks 10-13 |
| 7. Compute Without Seeing | 3% | Weeks 11-14 |

The weights reflect expected scope. Lab 1 is a short introduction; Lab 5 is the
largest coding assignment.

## Hidden evaluation and arenas

Selected labs include instructor-only cases in addition to public examples.
Hidden evaluation varies inputs and boundary conditions promised by the lab
specification; it does not depend on undocumented package trivia. The number,
mix, and nature of hidden cases are not announced. Some instances are clean or
do not contain enough evidence for a definitive claim. A correct abstention can
receive full credit when the evidence supports it.

Labs 3 and 6 use the [lab arenas](arena.html). They run on private systems or
workloads under a common interface and resource budget. Arena rank is feedback,
not a winner-take-all grade; course points use fixed criteria and instructor
baselines. The final project remains fully open and has no leaderboard.

## Lab 1: Model Privacy CTF

Implement a small attack runner against a documented query interface. You will
recover a memorized canary, compare target and reference scores for membership
evidence, control false positives, and transfer the attack to a changed private
instance. A solved-flags display may appear after the lab closes, but speed does
not affect the grade.

## Lab 2: Linkage and Reconstruction

Measure singling-out risk, link a released table to synthetic auxiliary data,
and reconstruct selected attributes from bounded statistics. Your program must
represent ambiguity and insufficient evidence instead of forcing every target
to have an answer. You will repeat part of the attack after a differentially
private release.

An optional extension replaces the scripted matching rule with an LLM that
infers attributes from unstructured auxiliary text, and asks whether that
changes who can be singled out. Report calibrated confidence, not anecdotes.

## Lab 3: LLM Privacy Attack Arena

Attack instructor-hosted LLM agents that hold synthetic user memories, read
untrusted retrieved documents, and call tools with declared permissions. The
declared surfaces are the ones that carry private data in real deployments:

- **Memory isolation**: can one user or session recover another's stored notes?
- **Indirect prompt injection**: does an instruction planted in a retrieved
  document redirect the agent's behavior?
- **Tool-permission enforcement**: can a read-only session reach a write or send
  tool, and can a tool call become an exfiltration channel?
- **Context and system-prompt extraction**: what does the agent disclose about
  its own instructions, retrieved documents, or prior turns?

Model and defense identities are hidden during evaluation. Exact canaries verify
real leakage, so a refusal that merely looks bypassed does not count as an
attack. Anonymous pairwise reviews compare the severity and evidence of attack
transcripts. A small arena audit then checks whether pair order, superficial
rewriting, or target-family fingerprinting can bias those judgments. See the
[arena specification](arena.html).

## Lab 4: DP Training Systems

Everyone first builds and traces a small private training run with
[Opacus](https://opacus.ai/). Teams then receive a bounded maintainer task in
either Opacus or [JAX Privacy](https://jax-privacy.readthedocs.io/). The main
question is whether sampling, accumulation, optimizer updates, and accountant
events describe the same training process. Code and regression tests matter
more than a long report.

## Lab 5: DPSynth Feature Sprint

Work against a pinned snapshot of
[Google DPSynth](https://github.com/google/dpsynth) and complete one approved
feature or repair. DPSynth already includes experimental relational synthesis,
so possible work may extend a typed adapter, diagnostics, a bounded constraint,
evaluation coverage, or an optional-dependency boundary rather than simply
"adding multi-table support." You will write the executable contract first,
then make a focused patch and test it on a second setting.

## Lab 6: Synthetic Data Arena

Build a privacy-valid single-table release with Google DPSynth under a common
privacy and compute budget. A private validity audit checks adjacency, domains,
contribution bounds, private-data access, composition, caching, and provenance.
Valid releases then run on held-out schemas and utility workloads. See the
[arena specification](arena.html).

## Lab 7: Compute Without Seeing

Complete a small two-party protocol and private linear inference task in a
prebuilt MPC environment. Hidden tests check both functional results and the
declared reveal boundary: inputs and intermediate values must not become extra
outputs.

## Teams and submissions

- Labs may be completed in teams of 2 or individually.
- A team submits one shared code bundle and contribution statement.
- Every student remains responsible for understanding the complete artifact.
- Each lab defines a compact structured result, test suite, or manifest rather
  than requiring the same report format seven times.
- When AI materially shapes a lab, include 3-5 consequential entries in an AI
  Decision Ledger: the suggestion, how it was checked, and the decision. Full
  chat transcripts are not required.

## Distribution

Starter bundles, assigned instances, hidden tests, private targets, evaluators,
solutions, and grading files are distributed through Canvas; any course Drive
link will be posted there. They are not published as raw resources from this
website.

Every required path will include a pinned environment, small input data, a
public smoke test, and a CPU-compatible command. Exact deadlines and feedback
windows will appear in Canvas.

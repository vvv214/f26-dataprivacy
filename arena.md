---
---

# Lab arenas

<p class="overview-back">
  <a href="index.html">Back to the course homepage</a><br>
  <a href="lab.html">Back to the labs page</a>
</p>

Two labs use controlled competition. Lab 3 asks how well an attack transfers
across anonymous LLM systems. Lab 6 asks how useful a synthetic-data release
remains after it passes a privacy audit. The project is separate, fully open,
and noncompetitive.

The anonymous comparison in Lab 3 is inspired by the pairwise, identity-hidden
evaluation used in
[Chatbot Arena](https://arxiv.org/abs/2403.04132), but its criterion is narrower:
which transcript provides stronger verified evidence of a privacy failure?
The arena-audit subtask also draws on research showing that output
fingerprinting can enable targeted manipulation of anonymous voting
leaderboards ([paper](https://arxiv.org/abs/2501.07493)).

## Lab 3: LLM Privacy Attack Arena

Each team submits a deterministic attack runner for an instructor-hosted API.
Targets share an interface but may differ in model, memory isolation, document
handling, tool permissions, and defenses. All memories and canaries are
synthetic course artifacts.

Evaluation has three parts:

1. Public targets check the runner interface, controls, and budget.
2. Private execution tests the runner across anonymous target families.
3. Review packets present paired transcripts in randomized order without model,
   target, or team identity. Multiple reviewers apply the same evidence and
   severity rubric.

Some packets are sentinels: they repeat the same verified evidence with reversed
left/right order or a superficial style and length transformation. These pairs
measure position and presentation bias and are excluded from the attack
ranking.

A separate closed simulator lets students test target-family fingerprinting and
simulated targeted voting. Its votes never enter the course ranking or grade.

Exact canaries and tool events verify whether a leak or policy bypass occurred.
Peer review cannot turn an unverified claim into a successful attack. Conflicted
or low-agreement reviews are inspected by course staff.

Lab 3 is worth 4%:

| Criterion | Points |
|---|---:|
| Valid runner and budget compliance | 1.0 |
| Verified attack effectiveness | 1.5 |
| Transfer, controls, and calibrated abstention | 1.0 |
| Blind-review and arena-audit quality | 0.5 |

### What you need for Lab 3

No paid account, personal API key, or model subscription is required.

- The release bundle includes a local practice target that runs offline on CPU.
  It implements the same interface, budget accounting, and canary format as the
  hidden targets, so you can develop and test a complete runner without calling
  any external service.
- Scored runs against the hidden targets are executed by the instructor on
  course infrastructure. You submit a runner, not results.
- If you have access to a model API of your own, you may use it to develop
  attacks. It is optional and confers no grading advantage. Course bundles,
  private targets, and grader files may not be uploaded to an outside service.

## Lab 6: Synthetic Data Arena

Each team uses [Google DPSynth](https://github.com/google/dpsynth) to produce a
synthetic table, privacy manifest, provenance record, and reproducible CPU
command under the same privacy and resource budget.

Evaluation has three layers:

1. Public smoke tests check the interface and basic execution path.
2. A private validity audit checks adjacency, domains, contribution bounds,
   composition, private versus public inputs, caching, and release provenance.
3. Privacy-valid submissions run on held-out schemas, seeds, marginals,
   correlations, and downstream tasks.

Among valid submissions, the display score is 80% held-out utility and 20%
robustness across workload changes. Lab 6 is worth 5%:

| Criterion | Points |
|---|---:|
| Valid privacy contract and release boundary | 2.0 |
| Implementation, provenance, and reproducibility | 1.0 |
| Held-out utility and robustness bands | 1.5 |
| Utility analysis and residual risk | 0.5 |

## Feedback and grading

- Public tests may be run without a submission limit.
- Each arena provides one private dry run with coarse category feedback and one
  final scored run.
- Final display rankings use team aliases and appear only after submissions
  close.
- Ranking does not determine course points. Hidden-performance points use fixed
  bands calibrated from instructor baselines.
- A privacy-invalid Lab 6 release is excluded from its display ranking and
  cannot earn held-out-performance points, but its other work is still assessed.

## Safety boundary

- Use only the published lab interfaces, budgets, and permitted tools.
- Do not retrieve private targets, data, workloads, evaluator code,
  credentials, aliases, or another team's submission. Target-family
  identification is permitted only in the designated Lab 3 simulator.
- Do not target Canvas, model providers, course infrastructure, or availability.
- Malware, persistence, credential access, and resource exhaustion are
  prohibited.
- Do not encode private data or dry-run feedback into a final artifact.
- Private course bundles may not be uploaded to an external AI service unless
  the release explicitly permits it.

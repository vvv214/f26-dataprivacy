---
---

# Labs

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

The four labs put you in different roles: privacy attacker, agent designer,
library maintainer, and privacy-system designer. All four labs are completed
individually. Each lab contributes 10% of the course grade, for a total of 40%.

| Lab | Weight | Timing |
|---|---:|---|
| 1. Privacy Attack Warm-up | 10% | Weeks 3-5 |
| 2. Two-Agent Secret Arena | 10% | Weeks 5-9 |
| 3. DP Library Extension Challenge | 10% | Weeks 9-12 |
| 4. Compute Without Seeing | 10% | Weeks 12-15 |
{: .lab-summary }

The point values are equal, but the formats are intentionally different. Lab 1
is a compact warm-up; later labs involve longer-lived systems, larger
codebases, or more design freedom.

## Lab 1: Privacy Attack Warm-up

Implement one compact attack runner across small model and data privacy
challenges. You will recover a memorized canary, evaluate membership evidence,
link synthetic records with calibrated abstention, and test one bounded
reconstruction claim. Randomized hidden instances change canaries, score
calibration, missingness, candidate pools, and whether a unique conclusion is
possible. A solved-flags display may appear after the lab closes, but speed does
not affect the grade.

## Lab 2: Two-Agent Secret Arena

Build one small agent that both attacks and defends. Each student submits an
agent; in each four-round match, two submissions alternate messages under the
same model and turn budget. Each tries to induce the other to reveal a
synthetic secret while preventing exact, punctuation-stripped, or encoded
disclosure of its own secret. Pairings run anonymously and in both turn orders.

The course harness owns model calls, secrets, transcripts, budgets, and
scoring. Student code uses plain Python to construct the direct chat-completion
request and filter its outgoing message. A public offline backend makes the
protocol testable without a paid account, while a separate hidden benign
evaluator checks allowed facts and secret-derived outputs. An agent that
refuses every request may defend well but receives no utility credit.

The 10 points cover contract compliance and reproducibility (1), defense (3),
offense (2), hidden benign-task utility (3), and boundary explanation (1).
Arena rank is feedback rather than a winner-take-all grade. The target workload
is 3-4 hours.

## Lab 3: DP Library Extension Challenge

First trace one small path through each course library:

- [Opacus](https://opacus.ai/) for private training in PyTorch;
- [JAX Privacy](https://jax-privacy.readthedocs.io/) for sampling and privacy
  accounting in JAX; and
- [Google DPSynth](https://github.com/google/dpsynth) for private synthetic data.

Then work in one pinned repository and add an approved algorithm, mechanism, or
algorithmic feature. Possible tracks include training mechanisms, accounting
events or guards, synthesis and relational operations, and cross-library
adapters. Each ticket has a published mathematical and behavioral contract.
Your patch must include focused tests, a baseline comparison, compatibility
notes, and a short code walkthrough. Hidden CI tests vary shapes, seeds,
sampling and resume boundaries, schemas, optional dependencies, and unsupported
inputs promised by the contract.

## Lab 4: Compute Without Seeing

Complete two required privacy-enhancing technology exercises: a small Yao
comparison using garbled circuits and oblivious transfer, and private linear
inference in a real three-party MP-SPDZ runtime. Both tasks make the reveal
boundary explicit and test that no input or intermediate value crosses it.

Then choose one extension: encrypted aggregation with Paillier homomorphic
encryption, verification of a synthetic TEE attestation report, or a miniature
Path ORAM read/write implementation. The TEE path teaches attestation logic but
does not claim that a notebook simulates enclave security. The ORAM path must
state what access-pattern information remains visible and what a production
position map would require.

Each student completes a five-minute individual oral check during class or
office hours. You will identify the reveal operation, explain one nontrivial
component, and respond to one small change in the policy or threat model. The
oral check is part of the Lab 4 grade, not a separate exam.

## Individual submissions

- Each student submits their own code bundle and supporting explanation.
- High-level discussion is welcome, but submitted code, results, and written
  answers must be the student's own work.
- Each lab defines a compact structured result, test suite, or manifest rather
  than requiring the same report format four times.
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

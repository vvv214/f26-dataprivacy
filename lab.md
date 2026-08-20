---
---

# Labs

The three labs are privacy-engineering audits rather than step-by-step
notebooks. Each one asks you to build a small working system, test a concrete
privacy contract, repair or defend it with evidence, and transfer the result to
a changed setting.

Labs contribute 30% of the course grade, 10% each. They begin after the course
has established attacks, adjacency, sensitivity, mechanisms, and accounting.

## The repeated workflow

1. Build a working baseline and record the system's privacy contract.
2. Break the assigned instance, or show that it is clean or cannot be decided
   from the available evidence.
3. Repair the root cause and add a regression test.
4. Transfer the repair or audit method to a related new setting.

Some instances are intentionally clean, and some do not contain enough
evidence for a definitive conclusion. Finding a novel upstream bug is not a
requirement. The goal is a reproducible, well-supported judgment.

## Lab 1: Opacus training contract audit

Question: Does the sampler, private optimizer, and privacy accountant describe
the same training process?

You will train a small model with [Opacus](https://opacus.ai/), record the
sampling and accounting contract, audit an assigned data-loader configuration,
and test the repair under a changed sampling or grouping condition.

Main concepts include record- versus user-level adjacency, sampling events,
expected batch size, optimizer updates, privacy events, and secure randomness.

## Lab 2: JAX Privacy step accounting

Question: Are physical batches, accumulated batches, optimizer updates, and
privacy events counted in consistent units?

You will work with a pinned snapshot of
[JAX Privacy](https://jax-privacy.readthedocs.io/), instrument a bounded training
path, reproduce or reject an assigned contract failure, make a narrow patch or
guard, and add parameterized regression tests.

Main concepts include effective batch size, gradient accumulation, privacy
calibration, resume behavior, boundary cases, and source-level testing.

## Lab 3: Google DPSynth release audit

Question: Do the domain, contribution bounds, mechanism, and evaluation support
the privacy claim made for a synthetic-data release?

You will use the in-memory API of
[Google DPSynth](https://github.com/google/dpsynth) to generate a small tabular
release, trace every private-data access, audit the release boundary, and apply
the repaired pipeline to a related schema.

Main concepts include public domains and bounds, contribution limits, private
query selection, provenance, caching, release artifacts, and utility
evaluation. The required path is CPU-friendly; distributed Beam execution is
optional.

## Teams and submissions

- Labs may be completed in teams of 2 or individually.
- A team submits one shared code bundle and audit dossier.
- Every submission includes a contribution statement.
- Each student remains responsible for understanding the complete submitted
  artifact; individual ownership is assessed in the
  [oral defense](oral.html).

Each lab submission includes runnable code and tests, a machine-readable
contract or manifest, a concise audit dossier, a transfer result, and an AI
Decision Ledger when AI materially shaped the work. Complete AI chat transcripts
are not required.

## Per-lab rubric

| Criterion | Points |
|---|---:|
| Build and reproducibility | 2 |
| Finding and root-cause evidence | 3 |
| Repair or guard and regression test | 3 |
| Transfer and residual-risk analysis | 2 |

A correct clean or insufficient-evidence finding can earn full credit. Grades
reward the quality of the contract, evidence, repair, and transfer rather than
the rarity of a bug.

## Distribution and setup

Release bundles, instance-specific materials, hidden tests, and solution files
are distributed through Canvas or the course Drive. They are not published as
raw resources from this website.

Every lab release includes a pinned package environment, small input data,
starter commands, and a CPU-compatible core path. Legacy attack,
re-identification, and MPC notebooks may still appear as shorter in-class
practicals, but they are not part of the three graded take-home labs.

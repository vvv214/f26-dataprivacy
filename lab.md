---
---

# Labs

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

The four labs put you in different roles: privacy attacker, adversary,
data publisher, and privacy-system designer. All four labs are completed
individually. Each lab contributes 10% of the course grade, for a total of 40%.

| Lab | Weight | Timing |
|---|---:|---|
| 1. Privacy attacks on LLMs | 10% | Weeks 3-5 |
| 2. Adversarial attacks | 10% | Weeks 5-9 |
| 3. Two ways to release a sensitive dataset | 10% | Weeks 9-12 |
| 4. Compute Without Seeing | 10% | Weeks 12-15 |
{: .lab-summary }

The point values are equal, but the formats are intentionally different. Lab 1
starts with experiments on supplied GPT models; later labs attack image and
text models, build private releases with real DP libraries, or give more
design freedom.

## Lab 1: Privacy attacks on LLMs

Run the supplied GPT models to study training-data extraction and memorization.
For membership inference, train a small classifier and shadow
model on synthetic data, compare confidence-based and learned methods, and
implement threshold counts and ROC evaluation, including low-FPR metrics.
Hidden evaluation runs the same MIA and ROC functions on new classifier
instances, with different data, seeds, sample counts, and row order.

The 10 regular points cover the CTF warm-up (2) and classifier MIA (8).
AI assistance is allowed. The warm-up awards 1 point for the flag and
1 point for the two-model loss comparison with evidence.

Classifier MIA includes target/shadow training (1), confidence baseline (1),
learned classifier (2), threshold counts and rates (1), ROC evaluation (1), design philosophy (1),
and method performance (1). In 3-5 sentences, explain the method's design,
shadow-data validation, and a failure mode considered.
On the supplied data and settings, each target/shadow model should reach
95% train accuracy and 70% test accuracy. Each membership method earns its
full 0.5 performance points at AUC >= 0.60; credit increases linearly from
0 at AUC 0.50 to 0.5 at AUC 0.60. Correct implementation and evaluation code
are graded separately from method performance. Low-FPR TPR must be reported,
but has no minimum performance threshold. The notebook summarizes grading.
Keep total target, shadow, and membership-classifier training within 10 minutes
on a standard Colab CPU runtime; no GPU is needed.
Hidden evaluation reuses these functions on similar, unpublished synthetic
datasets. Improve the existing methods using shadow data, without fitting on
target membership labels or hard-coding visible examples. The top five earn
a separate +2 AUC bonus, ranked by the higher of the two methods' mean AUC
across all hidden datasets. A method must return valid scores on every dataset.
Ties use that method's mean TPR at FPR <= 1%, then the design philosophy.
ROC checks count toward the existing implementation points.

The training-inference bonus awards +2 to the five strongest explanations of
how a supplied GPT was trained, judged by evidence, experiment, and reasoning.
Include a reproducible comparison with an alternative explanation. The two
bonus categories are ranked separately and can stack: the maximum is 14/10,
with the base score still out of 10.

## Lab 2: Adversarial attacks

Can small changes to an input change a model's prediction? Implement a PGD
evasion attack on an MNIST classifier, compare L0, L1, L2 and L∞
budgets, and design a more efficient image attack. Then append a
short suffix of neutral words, punctuation and special tokens to a positive
movie review so that a fixed classifier predicts NEGATIVE: start from a greedy
baseline, beat it, and freeze the attack to test how it transfers. Finally,
compare data poisoning with a backdoor: plant a marker, vary the contamination
rate, and remove the marker feature.

The 10 points cover the image evasion attack (4), the text suffix attack (4),
and poisoning and backdoors (2). The top five in the image efficiency challenge
and the top five in the text challenge each earn +2; the maximum is 14/10.

## Lab 3: Two ways to release a sensitive dataset

Release a census dataset (UCI Adult) privately in two ways, with
[JAX Privacy](https://github.com/google-parfait/jax_privacy) and
[DPSynth](https://github.com/google-parfait/dpsynth) in one Colab notebook.
First write DP-SGD from scratch for gradients stored as JAX pytrees: per-example
norms, clipping, the noisy average, one step with Poisson sampling, and the
training loop, checked against JAX Privacy's implementation. Then price it with
an accountant: build its privacy event and calibrate the noise for a target
ε by bisection. Finally, release a synthetic table with AIM inside
DPSynth: choose public bins for the numerical attributes, write the
exponential mechanism and AIM's selection step, and retrain DP-SGD on the
public domains.

All 10 points come from hidden tests on the functions you write: DP-SGD (5),
accounting (1.5), and AIM (3.5). The five binnings with the lowest error on
reserved data earn +2, and approved pull requests to JAX Privacy or DPSynth
earn +1 each, up to +5; the maximum is 17/10.

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

## Distribution

Starter bundles, assigned instances, hidden tests, private targets, evaluators,
solutions, and grading files are distributed through Canvas; any course Drive
link will be posted there. They are not published as raw resources from this
website.

Every required path will include a pinned environment, small input data, a
public smoke test, and a CPU-compatible command. Exact deadlines and feedback
windows will appear in Canvas.

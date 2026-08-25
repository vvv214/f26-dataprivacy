---
---

# Why take this course?

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

## When useful systems reveal too much

Privacy failures do not always look like someone stealing a password. They can
happen when a useful product reveals more than its designers expected:

<div class="privacy-stories">
  <section class="privacy-story">
    <figure>
      <a href="https://www.theguardian.com/world/2018/jan/28/fitness-tracking-app-gives-away-location-of-secret-us-army-bases">
        <img src="{{ '/assets/images/strava-heatmap.png' | relative_url }}"
             alt="Strava heat map screenshot showing activity traces outlining a military base in Helmand Province"
             width="1200" height="720" loading="eager" decoding="async">
      </a>
      <figcaption><a href="https://www.theguardian.com/world/2018/jan/28/fitness-tracking-app-gives-away-location-of-secret-us-army-bases">Strava Heatmap via The Guardian</a></figcaption>
    </figure>
    <div class="privacy-story-copy">
      <h3>A map of ordinary runs</h3>
      <p>Each run looked harmless on its own. But when Strava combined millions of routes, bright lines traced roads and the perimeter of a military base. Nothing had to be hacked: the privacy failure emerged when individually ordinary records were aggregated and released.</p>
      <p>The surprise is that no single runner had to disclose the base. The sensitive pattern appeared only after the service transformed and visualized many records together. This case asks where a release boundary should sit, what information should be minimized, and when an aggregate can still expose people or places.</p>
    </div>
  </section>
  <section class="privacy-story">
    <figure>
      <a href="https://arxiv.org/abs/cs/0610105">
        <img src="{{ '/assets/images/netflix-deanonymization.png' | relative_url }}"
             alt="Title and abstract of the paper How to Break Anonymity of the Netflix Prize Dataset"
             width="1000" height="650" loading="eager" decoding="async">
      </a>
      <figcaption><a href="https://arxiv.org/abs/cs/0610105">Narayanan and Shmatikov, paper abstract</a></figcaption>
    </figure>
    <div class="privacy-story-copy">
      <h3>Anonymous, until the datasets meet</h3>
      <p>Netflix removed names and account identifiers before releasing millions of movie ratings from roughly 500,000 subscribers. To someone looking at the file by itself, a row of movie IDs, scores, and dates could appear anonymous.</p>
      <p>The researchers treated public IMDb ratings as background knowledge. A few overlapping movies, approximate scores, and rough dates could narrow the candidates to one Netflix record. Once that link was made, the person's other ratings in the released record became visible.</p>
      <p>The lesson is broader than these two websites: anonymity depends on what other data exists and how distinctive a person's behavior is. You will study scoped linkage attacks in class and test how generalization, suppression, or differential privacy changes what an attacker can infer.</p>
    </div>
  </section>
  <section class="privacy-story">
    <figure>
      <a href="https://www.usenix.org/system/files/sec21-carlini-extracting.pdf">
        <img src="{{ '/assets/images/gpt2-extraction.png' | relative_url }}"
             alt="Figure from a GPT-2 extraction paper showing a prompt producing memorized and redacted contact information"
             width="600" height="480" loading="eager" decoding="async">
      </a>
      <figcaption><a href="https://www.usenix.org/system/files/sec21-carlini-extracting.pdf">Carlini et al., Figure 1</a></figcaption>
    </figure>
    <div class="privacy-story-copy">
      <h3>A model that remembered too much</h3>
      <p>GPT-2 never exposed its training files directly. Yet researchers found prompts that made the model reproduce memorized text, including the redacted contact details shown here. The model itself became a query interface to its training data.</p>
      <p>The attack did not start with a known phone number. The researchers generated many completions, ranked strings that looked unusually likely under GPT-2, and then checked whether the strongest candidates appeared verbatim in the training sources. That verification step turned a surprising output into evidence of extraction.</p>
      <p>This story connects model behavior back to the data pipeline: deduplication, the definition of a training record, memorization tests, and private training all affect the risk. You will learn to distinguish a plausible leak from a reproducible privacy claim.</p>
    </div>
  </section>
</div>

## From failures to defenses

There is no single privacy switch. The right defense depends on what a system
will release: an answer, a trained model, or a reusable dataset.

<div class="defense-stories">
  <section class="defense-story">
    <figure class="defense-figure">
      <a href="https://www.nist.gov/blogs/cybersecurity-insights/differential-privacy-privacy-preserving-data-analysis-introduction-our">
        <img src="{{ '/assets/images/nist-dp-guarantee.png' | relative_url }}"
             alt="NIST diagram comparing an analysis with and without one person's data and requiring the two answers to be indistinguishable"
             width="621" height="317" loading="lazy" decoding="async">
      </a>
      <figcaption><a href="https://www.nist.gov/blogs/cybersecurity-insights/differential-privacy-privacy-preserving-data-analysis-introduction-our">NIST: an informal definition of differential privacy</a></figcaption>
    </figure>
    <div class="defense-story-copy">
      <h3>Limit what one person can change</h3>
      <p>Differential privacy compares two neighboring worlds: one with a person's data and one without it. If the observable outputs remain close, an analyst cannot confidently determine whether that person participated or what their record contained. The privacy parameter controls how close those worlds must be.</p>
      <p>This is stronger than deleting names because the guarantee anticipates outside knowledge and repeated analysis. It also forces precise questions: What counts as one person's record? Which output is protected? How much privacy budget is spent?</p>
    </div>
  </section>
  <section class="defense-story">
    <figure class="defense-figure">
      <a href="https://research.google/blog/sparsity-preserving-differentially-private-training/">
        <img src="{{ '/assets/images/google-dpsgd.png' | relative_url }}"
             alt="Google Research diagram of DP-SGD: sample a mini-batch, compute per-example gradients, clip them, aggregate, and add Gaussian noise"
             width="1999" height="768" loading="lazy" decoding="async">
      </a>
      <figcaption><a href="https://research.google/blog/sparsity-preserving-differentially-private-training/">Google Research: the DP-SGD training pipeline</a></figcaption>
    </figure>
    <div class="defense-story-copy">
      <h3>Bound influence during model training</h3>
      <p>DP-SGD limits each training example's influence before a model update. It computes per-example gradients, clips each one to a fixed norm, aggregates them, and adds Gaussian noise. A privacy accountant then tracks the cumulative cost across many training steps.</p>
      <p>The diagram is simple; a correct implementation is not. Sampling assumptions, clipping location, record boundaries, noise calibration, and accounting must agree. You will use Opacus and JAX Privacy to trace those choices from configuration to code and test whether a claimed guarantee matches the training run.</p>
    </div>
  </section>
  <section class="defense-story">
    <figure class="defense-figure">
      <a href="https://www.nist.gov/blogs/cybersecurity-insights/differentially-private-synthetic-data">
        <img src="{{ '/assets/images/nist-dp-synthetic.png' | relative_url }}"
             alt="NIST diagram showing original records converted to a histogram, a noisy histogram, a marginal distribution, and differentially private synthetic data"
             width="936" height="286" loading="lazy" decoding="async">
      </a>
      <figcaption><a href="https://www.nist.gov/blogs/cybersecurity-insights/differentially-private-synthetic-data">NIST: one route to differentially private synthetic data</a></figcaption>
    </figure>
    <div class="defense-story-copy">
      <h3>Release new records, not the original people</h3>
      <p>Synthetic data replaces original rows with newly sampled records, but synthetic does not automatically mean private. In this NIST example, the original table is summarized, noise is added to the counts, and only then are new rows sampled from the privatized distribution.</p>
      <p>The release can preserve useful population patterns while protecting individual contributions, but ranges, rare categories, and correlations still determine whether it is useful. With Google DPSynth, you will audit both sides of that claim: the formal release boundary and the empirical utility of the generated data.</p>
    </div>
  </section>
</div>

## From examples to engineering judgment

These cases raise the questions we will learn to answer: What information is
actually sensitive? What does an attacker already know? Can a person be linked,
reconstructed, or detected in a dataset? Does a model memorize its training
records? Does a claimed defense match the data pipeline, code, configuration,
and privacy accounting?

You will study privacy failures, measure their impact in scoped exercises, and
test defenses ranging from data minimization and access boundaries to
differential privacy, private machine learning, and synthetic data. We will
also survey secure multi-party computation (MPC), homomorphic encryption (HE),
trusted execution environments (TEEs), and network privacy tools. The emphasis
is on technical understanding, experimental reasoning, and clear communication
rather than graduate-level novelty.

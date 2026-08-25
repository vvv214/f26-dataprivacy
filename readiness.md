---
---

# Readiness self-check

<p class="overview-back"><a href="index.html">Back to the course homepage</a></p>

This short self-check shows the programming, probability, and machine-learning
ideas used near the start of the course. It is ungraded and is not an enrollment
requirement. Try it without running the code or asking an AI assistant first;
then use the guidance to identify anything worth reviewing.

## 1. Trace a short Python function

```python
def clipped_sum(values, bound):
    total = 0
    for value in values:
        total += min(max(value, 0), bound)
    return total

records = {"train": [-2, 1, 7], "test": [2, 4]}
answer = clipped_sum(records["train"], 5)
```

What value is stored in `answer`? In one sentence, explain what the function
does to each input before adding it.

## 2. Inspect a small dataset

```python
rows = [
    {"user": "A", "split": "train", "loss": 0.2},
    {"user": "B", "split": "train", "loss": 0.7},
    {"user": "A", "split": "test",  "loss": 0.3},
]
```

Which user appears in both splits? What is the mean loss of the two training
rows? Write a short list comprehension that selects the training rows.

## 3. Interpret an attack result

An attack examines 40 members and 60 nonmembers. It flags 24 members and 6
nonmembers as likely members.

- What are the true-positive rate and false-positive rate?
- Why would reporting only the fraction of all 100 decisions that are correct
  hide useful information about the attack?

## 4. Connect training to privacy

A model has much lower loss on its training data than on held-out test data.
Give one ordinary machine-learning explanation. Then give one reason this gap
might matter when studying whether the training data can be inferred or
extracted.

## 5. Check an AI-generated claim

An AI assistant says, "The code adds Gaussian noise, so the released model is
differentially private." List two facts you would want to verify before relying
on that statement. This is a preview, not expected prior knowledge; the course
will develop the complete answer.

## Guidance

1. `answer` is `6`: the function clips each value to the interval from 0 to 5,
   then sums the clipped values.
2. User A crosses the train/test boundary, the mean training loss is `0.45`,
   and one selection is `[row for row in rows if row["split"] == "train"]`.
3. The true-positive rate is `24 / 40 = 0.60`; the false-positive rate is
   `6 / 60 = 0.10`. A single accuracy number mixes two different error types
   and depends on how many members and nonmembers were included.
4. The gap may indicate overfitting. Training examples can then behave
   differently from unseen examples, which can create evidence for membership
   inference or memorization attacks.
5. Relevant questions include what output is released, what neighboring
   datasets mean, whether per-example contributions are bounded, how much noise
   is added, and whether all training steps are included in the privacy
   accounting.

You are well positioned for the opening weeks if you can follow Questions 1-3
and can explain the basic train/test distinction in Question 4. Needing a quick
review of Python syntax or averages is normal; review those topics before the
first lab. The privacy details in Question 5 are taught in the course.

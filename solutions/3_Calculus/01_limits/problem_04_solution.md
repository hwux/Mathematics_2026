# Exercise 4 — Powers and Oscillation

## The Problem

Analyze

$$
\left(\frac23\right)^n,\qquad \left(\frac32\right)^n,\qquad (-1)^n,\qquad \frac{(-1)^n}{n}.
$$

For each sequence, describe the type of behavior and justify your answer.

---

## What Are We Looking For?

For each of the four sequences we want to decide whether it converges, diverges to infinity, or diverges by oscillation, and to give a reason for each decision.

---

## Idea and Theorem Before the Calculation

**Geometric sequences:** For $q^n$,

- if $|q|<1$, then $q^n\to0$,
- if $q>1$, then $q^n\to+\infty$,
- if $q=-1$, the sequence alternates between $1$ and $-1$ and has no limit.

**Subsequence criterion:** If a sequence has two subsequences with different limits, it has no limit.

**Squeeze theorem:** If $a_n\le b_n\le c_n$ and $a_n\to L$, $c_n\to L$, then $b_n\to L$.

---

## Step-by-Step Solution

**Sequence 1: $\left(\frac23\right)^n$.**

Here $0<q=\frac23<1$. Each term is $\frac23$ of the previous one, so the sequence is positive and decreasing. Moreover $\left(\frac32\right)^n\to+\infty$ (see below), hence

$$
\left(\frac23\right)^n=\frac{1}{\left(\frac32\right)^n}\longrightarrow0.
$$

**Behavior:** monotone convergence to $0$.

**Sequence 2: $\left(\frac32\right)^n$.**

Write $\frac32=1+\frac12$. By Bernoulli's inequality $(1+x)^n\ge1+nx$ for $x>0$:

$$
\left(\frac32\right)^n\ge1+\frac{n}{2}\longrightarrow+\infty.
$$

*Why this is valid:* A sequence bounded below by a sequence tending to $+\infty$ also tends to $+\infty$.

**Behavior:** increasing, divergent to $+\infty$.

**Sequence 3: $(-1)^n$.**

The even terms form the subsequence $1,1,1,\ldots$ with limit $1$; the odd terms form $-1,-1,-1,\ldots$ with limit $-1$. Two subsequences with different limits exist, so the sequence has no limit.

**Behavior:** bounded, oscillating, divergent.

**Sequence 4: $\frac{(-1)^n}{n}$.**

The sign alternates, but the size of the terms is $\frac1n$:

$$
-\frac{1}{n}\le\frac{(-1)^n}{n}\le\frac{1}{n}.
$$

Both bounds tend to $0$, so by the squeeze theorem

$$
\frac{(-1)^n}{n}\longrightarrow0.
$$

**Behavior:** oscillating in sign, but convergent to $0$.

---

## Final Answer in Words

| Sequence | Behavior | Limit |
|---|---|---|
| $\left(\frac23\right)^n$ | decreasing, convergent | $0$ |
| $\left(\frac32\right)^n$ | increasing, unbounded | $+\infty$ (divergent) |
| $(-1)^n$ | bounded, oscillating | none |
| $\frac{(-1)^n}{n}$ | oscillating sign, shrinking size | $0$ |

The last two sequences both oscillate, but only the third diverges: oscillation does not rule out convergence when the amplitude of the oscillation tends to zero.

---

## Quick Verification

The first terms show the four behaviors directly:

- $\left(\frac23\right)^{10}\approx0.017$, small and positive,
- $\left(\frac32\right)^{10}\approx57.7$, already large,
- $(-1)^{10}=1$ and $(-1)^{11}=-1$, still jumping,
- $\frac{(-1)^{10}}{10}=0.1$ and $\frac{(-1)^{11}}{11}\approx-0.09$, jumping with a shrinking size.

---

## Common Mistakes

- **"It oscillates, so it diverges":** $\frac{(-1)^n}{n}$ oscillates and still converges.
- **"It is bounded, so it converges":** $(-1)^n$ is bounded and diverges.
- **Confusing $\left(\frac23\right)^n$ with $\left(\frac32\right)^n$:** the base decides everything; compare it with $1$.

---

## Oral Explanation (3 sentences)

A geometric sequence $q^n$ tends to zero when $|q|<1$ and to infinity when $q>1$, which settles the first two sequences. The sequence $(-1)^n$ keeps jumping between $1$ and $-1$, so its even and odd terms have different limits and it diverges. The sequence $\frac{(-1)^n}{n}$ also changes sign, but it is squeezed between $-\frac1n$ and $\frac1n$, so it converges to zero.

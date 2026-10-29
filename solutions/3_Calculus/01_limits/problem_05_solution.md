# Exercise 5 — The Classical Limit Leading to the Number $e$

## The Problem

Compute

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^n.
$$

Calculate several values for increasing $n$ and compare the observed behavior with the value of the limit. Explain why a few values do not constitute a proof.

---

## What Are We Looking For?

We want the value of a famous limit, a table of numerical values that illustrates it, and an explanation of the difference between numerical evidence and proof.

---

## Idea and Theorem Before the Calculation

**Indeterminate form $1^\infty$:** The base tends to $1$ and the exponent to $\infty$. Taking "$1^\infty=1$" would be wrong: the base gets closer to $1$, but it is raised to an ever larger power.

**Definition of $e$:** The sequence $a_n=\left(1+\frac1n\right)^n$ is increasing and bounded above (for example by $3$). By the monotone convergence theorem it has a limit, and this limit is called $e$:

$$
e=\lim_{n\to\infty}\left(1+\frac1n\right)^n\approx2.718281828.
$$

---

## Step-by-Step Solution

**Step 1: Why the sequence is increasing (sketch).**

By the binomial theorem,

$$
\left(1+\frac1n\right)^n=\sum_{k=0}^{n}\frac{1}{k!}\left(1-\frac1n\right)\left(1-\frac2n\right)\cdots\left(1-\frac{k-1}{n}\right).
$$

When $n$ increases, every bracket increases and a new positive term appears, so $a_{n+1}>a_n$.

**Step 2: Why it is bounded.**

Every bracket is at most $1$, so

$$
a_n\le\sum_{k=0}^{n}\frac{1}{k!}\le1+1+\frac12+\frac14+\cdots+\frac{1}{2^{n-1}}<3,
$$

using $k!\ge2^{k-1}$.

**Step 3: Conclusion.**

An increasing sequence bounded above converges. Its limit is the number $e$:

$$
\lim_{n\to\infty}\left(1+\frac1n\right)^n=e\approx2.71828.
$$

**Step 4: Numerical values.**

| $n$ | $\left(1+\frac1n\right)^n$ |
|---|---|
| $1$ | $2$ |
| $10$ | $2.593742$ |
| $100$ | $2.704814$ |
| $1000$ | $2.716924$ |
| $10\,000$ | $2.718146$ |
| $1\,000\,000$ | $2.718280$ |

The values increase and approach $e=2.718281\ldots$ from below, but slowly: the error is roughly $\frac{e}{2n}$.

---

## Why a Few Values Are Not a Proof

A table shows finitely many terms, while a limit is a statement about all terms from some index on. A sequence can look settled for a long time and then change: for example $b_n=\frac{n}{10^{9}}$ has $b_n<0.001$ for all $n\le10^6$, so a table up to a million suggests the limit $0$, yet $b_n\to+\infty$. The table also cannot distinguish $e$ from a nearby number such as $2.71829$. Only an argument (here monotonicity plus boundedness) guarantees the limit.

---

## Final Answer in Words

The limit equals the number $e\approx2.71828$. The numerical values increase towards $e$ and agree with the result, but they only illustrate it; the proof comes from the fact that the sequence is increasing and bounded.

---

## Quick Verification

Using the logarithm: $n\ln\left(1+\frac1n\right)=n\left(\frac1n-\frac{1}{2n^2}+\cdots\right)=1-\frac{1}{2n}+\cdots\to1$, so $a_n\to e^1=e$. For $n=1000$ this gives $a_n\approx e^{1-0.0005}\approx2.7169$, matching the table.

---

## Common Mistakes

- **"$1^\infty=1$":** this is an indeterminate form; the answer here is $e$, not $1$.
- **Expecting fast convergence:** even for $n=1000$ only two decimal places are correct.
- **Treating a table as a proof:** it supports a conjecture but cannot establish a limit.

---

## Oral Explanation (3 sentences)

The expression $\left(1+\frac1n\right)^n$ has a base tending to $1$ and an exponent tending to infinity, so its behavior is not obvious. One can show with the binomial theorem that the sequence is increasing and stays below $3$, and therefore it converges; its limit is by definition the number $e\approx2.718$. A table of values agrees with this, but it shows only finitely many terms, so it supports the result without proving it.

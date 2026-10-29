# Exercise 3 — A Square Root and Removing an Indeterminate Form

## The Problem

Compute

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right).
$$

Use the conjugate expression and explain why this transformation removes the difficulty.

---

## What Are We Looking For?

We want the limit of a difference of two quantities that both grow without bound, and an explanation of how multiplying by the conjugate turns it into a form that can be evaluated.

---

## Idea and Theorem Before the Calculation

**Indeterminate form $\infty-\infty$:** Both $\sqrt{n^2+5n}$ and $n$ tend to $+\infty$, so their difference could be anything.

**Conjugate:** The identity

$$
(A-B)(A+B)=A^2-B^2
$$

removes the square root when $A=\sqrt{n^2+5n}$, because $A^2=n^2+5n$.

---

## Step-by-Step Solution

**Step 1: Multiply and divide by the conjugate.**

$$
\sqrt{n^2+5n}-n=\frac{\left(\sqrt{n^2+5n}-n\right)\left(\sqrt{n^2+5n}+n\right)}{\sqrt{n^2+5n}+n}=\frac{(n^2+5n)-n^2}{\sqrt{n^2+5n}+n}=\frac{5n}{\sqrt{n^2+5n}+n}.
$$

*Why this is valid:* We multiply by $\frac{\sqrt{n^2+5n}+n}{\sqrt{n^2+5n}+n}=1$; the denominator is positive for $n\ge1$.

**Step 2: Divide by $n$.**

For $n>0$ we have $\sqrt{n^2+5n}=n\sqrt{1+\frac{5}{n}}$, so

$$
\frac{5n}{n\sqrt{1+\frac{5}{n}}+n}=\frac{5}{\sqrt{1+\frac{5}{n}}+1}.
$$

**Step 3: Pass to the limit.**

Since $\frac5n\to0$ and the square root is continuous,

$$
\lim_{n\to\infty}\frac{5}{\sqrt{1+\frac{5}{n}}+1}=\frac{5}{\sqrt1+1}=\frac{5}{2}.
$$

---

## Why the Conjugate Helps

The difference $\sqrt{n^2+5n}-n$ is a small number obtained by subtracting two huge, almost equal numbers, so the size of each term tells us nothing. The conjugate converts the difference into a quotient, $\frac{5n}{\sqrt{n^2+5n}+n}$, in which nothing cancels: both numerator and denominator grow like a multiple of $n$, and the dominant-term method of Exercise 1 applies.

---

## Final Answer in Words

$$
\lim_{n\to\infty}\left(\sqrt{n^2+5n}-n\right)=\frac{5}{2}.
$$

The conjugate turns the indeterminate form $\infty-\infty$ into a quotient of two terms of order $n$, whose ratio tends to $\frac{5}{2}$.

---

## Quick Verification

For $n=10\,000$:

$$
\sqrt{100\,050\,000}-10\,000\approx10\,002.4997-10\,000=2.4997.
$$

This is close to $2.5$. A second check: $\sqrt{n^2+5n}=\sqrt{\left(n+\frac52\right)^2-\frac{25}{4}}$, which is slightly less than $n+\frac52$, so the difference is slightly less than $\frac52$, exactly as observed.

---

## Common Mistakes

- **Writing $\infty-\infty=0$:** the two terms grow at the same rate, but their difference tends to $\frac52$, not $0$.
- **Approximating $\sqrt{n^2+5n}\approx n$ too early:** this throws away precisely the part that produces the answer.
- **Forgetting to multiply the denominator:** the conjugate must be used as a fraction equal to $1$.

---

## Oral Explanation (3 sentences)

The expression is a difference of two quantities that both tend to infinity, so we cannot evaluate it term by term. Multiplying and dividing by the conjugate $\sqrt{n^2+5n}+n$ removes the square root from the numerator and gives $\frac{5n}{\sqrt{n^2+5n}+n}$. After dividing by $n$ this becomes $\frac{5}{\sqrt{1+5/n}+1}$, which tends to $\frac{5}{2}$.

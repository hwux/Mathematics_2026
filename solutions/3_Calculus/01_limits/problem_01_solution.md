# Exercise 1 — Dominant Terms in a Sequence

## The Problem

Compute

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}.
$$

Explain why the highest-degree terms determine the result.

---

## What Are We Looking For?

We want the number that the fraction approaches when $n$ becomes very large, and an explanation of why only the $n^2$ terms matter for that number.

---

## Idea and Theorem Before the Calculation

**Indeterminate form:** Both the numerator and the denominator tend to $+\infty$, so the form $\frac{\infty}{\infty}$ gives no answer by itself.

**Dividing by the dominant power:** Dividing the numerator and the denominator by the highest power of $n$ (here $n^2$) does not change the value of the fraction, but turns every lower-degree term into a term that tends to $0$.

**Basic limit:** For every constant $c$ and every $k>0$,

$$
\lim_{n\to\infty}\frac{c}{n^k}=0.
$$

**Arithmetic of limits:** If $a_n\to a$ and $b_n\to b\neq0$, then $\frac{a_n}{b_n}\to\frac{a}{b}$.

---

## Step-by-Step Solution

**Step 1: Divide by $n^2$.**

$$
\frac{4n^2-3n+1}{2n^2+5n-7}=\frac{4-\frac{3}{n}+\frac{1}{n^2}}{2+\frac{5}{n}-\frac{7}{n^2}}.
$$

*Why this is valid:* Numerator and denominator are both multiplied by $\frac{1}{n^2}\neq0$, which does not change the fraction.

**Step 2: Limits of the small terms.**

$$
\frac{3}{n}\to0,\qquad \frac{1}{n^2}\to0,\qquad \frac{5}{n}\to0,\qquad \frac{7}{n^2}\to0.
$$

**Step 3: Limits of numerator and denominator.**

The new numerator tends to $4$ and the new denominator tends to $2\neq0$.

**Step 4: Quotient.**

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7}=\frac{4}{2}=2.
$$

*Why this is valid:* The quotient rule for limits applies because the limit of the denominator is not zero.

---

## Why Do the Highest-Degree Terms Decide?

Write the numerator as $4n^2\left(1-\frac{3}{4n}+\frac{1}{4n^2}\right)$ and the denominator as $2n^2\left(1+\frac{5}{2n}-\frac{7}{2n^2}\right)$. The brackets tend to $1$, so for large $n$ the fraction behaves like

$$
\frac{4n^2}{2n^2}=2.
$$

The lower-degree terms grow too, but they become negligible compared with $n^2$: for example, $\frac{3n}{4n^2}=\frac{3}{4n}\to0$.

---

## Final Answer in Words

The limit equals $2$, the ratio of the leading coefficients $4$ and $2$. The terms $n^2$ dominate all other terms, so they alone determine the limit.

---

## Quick Verification

For $n=1000$:

$$
\frac{4\cdot10^6-3000+1}{2\cdot10^6+5000-7}=\frac{3\,997\,001}{2\,004\,993}\approx1.9935.
$$

The value is close to $2$, and the difference keeps shrinking as $n$ grows (for $n=10^4$ it is about $1.9993$).

---

## Common Mistakes

- **Writing $\frac{\infty}{\infty}=1$:** this form is indeterminate; the answer depends on how fast each part grows.
- **Dividing by $n$ instead of $n^2$:** then the numerator and denominator still tend to infinity and nothing is gained.
- **Keeping the constant terms:** $1$ and $-7$ do not influence the limit at all.

---

## Oral Explanation (3 sentences)

Both parts of the fraction grow without bound, so the expression is an indeterminate form and must be transformed. After dividing the numerator and the denominator by $n^2$, every lower-order term becomes a quantity of the form $\frac{c}{n}$ or $\frac{c}{n^2}$, which tends to zero. Only the leading coefficients survive, so the limit is $\frac{4}{2}=2$.

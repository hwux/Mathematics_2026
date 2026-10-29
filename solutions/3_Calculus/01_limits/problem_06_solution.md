# Exercise 6 — From a Sequence to a Function — Limit at Infinity

## The Problem

Compute

$$
\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}.
$$

Compare the method with Exercise 1. Explain what changes when moving from $n$ to a real variable $x$, and what stays the same.

---

## What Are We Looking For?

We want the limit of a rational function as the real variable $x$ grows without bound, computed with the dominant-term method, and a comparison with the sequence limit of Exercise 1.

---

## Idea and Theorem Before the Calculation

**Limit of a function at infinity:** $\lim_{x\to\infty}f(x)=L$ means that $f(x)$ is arbitrarily close to $L$ for all sufficiently large real $x$, not only for integers.

**Heine's characterization:** Equivalently, $f(x_k)\to L$ for every sequence $x_k\to\infty$. This is the bridge between sequence limits and function limits.

**Tools:** The arithmetic of limits and $\frac{c}{x^k}\to0$ for $k>0$ hold for functions exactly as for sequences.

---

## Step-by-Step Solution

**Step 1: Divide by $x^2$.**

For $x\neq0$,

$$
\frac{3x^2-x+1}{5x^2+4x-2}=\frac{3-\frac{1}{x}+\frac{1}{x^2}}{5+\frac{4}{x}-\frac{2}{x^2}}.
$$

*Why this is valid:* We only consider large $x$, so $x\neq0$ and the denominator $5x^2+4x-2$ is positive.

**Step 2: Limits of the small terms.**

$$
\frac{1}{x}\to0,\qquad \frac{1}{x^2}\to0,\qquad \frac{4}{x}\to0,\qquad \frac{2}{x^2}\to0\qquad (x\to\infty).
$$

**Step 3: Quotient.**

$$
\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}=\frac{3}{5}.
$$

---

## Comparison with Exercise 1

**What stays the same:** the algebra. We divide by the highest power, the lower-order terms vanish, and the limit is the ratio of the leading coefficients ($\frac42$ there, $\frac35$ here).

**What changes:**

- $x$ runs through all large real numbers, not only integers, so the statement is stronger: it controls the function between the integers as well.
- A function may be undefined at some points. Here the denominator vanishes at $x=\frac{-2\pm\sqrt{14}}{5}$, so the function has a domain to respect; for large $x$ this does not matter, but near those points it would.
- For functions we may also ask about $x\to-\infty$; here the same computation gives $\frac35$ again.

---

## Final Answer in Words

$$
\lim_{x\to\infty}\frac{3x^2-x+1}{5x^2+4x-2}=\frac{3}{5}.
$$

The method is identical to Exercise 1; the difference is that the result now describes the function for all large real arguments.

---

## Quick Verification

For $x=1000$:

$$
\frac{3\,000\,000-1000+1}{5\,000\,000+4000-2}=\frac{2\,999\,001}{5\,003\,998}\approx0.59932.
$$

This is close to $0.6=\frac35$. By Heine's characterization, the sequence $a_n=f(n)$ must have the same limit, which agrees.

---

## Common Mistakes

- **Thinking the variable name changes the method:** dominant terms work the same for $n$ and for $x$.
- **Ignoring the domain:** a rational function can have points where it is undefined; they do not affect $x\to\infty$, but they matter elsewhere.
- **Assuming $f(n)\to L$ implies $f(x)\to L$:** in general it does not; the function could oscillate between the integers (for example $\sin(\pi x)$).

---

## Oral Explanation (3 sentences)

Dividing the numerator and the denominator by $x^2$ makes all lower-order terms tend to zero, so the limit is the ratio of the leading coefficients, $\frac{3}{5}$. This is exactly the method from Exercise 1, because the arithmetic of limits works the same way for sequences and functions. The new feature is that $x$ runs through all real numbers, so the result describes the whole tail of the graph, not just its values at integers.

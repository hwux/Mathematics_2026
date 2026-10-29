# Exercise 8 — A Square Root in a Function Limit

## The Problem

Compute

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}
$$

by rationalizing the numerator. Compare the idea with Exercise 3 involving a sequence.

---

## What Are We Looking For?

We want the limit of a $\frac00$ expression with a square root, obtained by multiplying by the conjugate, and a comparison with the same technique used for a sequence in Exercise 3.

---

## Idea and Theorem Before the Calculation

**Form $\frac00$:** At $x=4$ we get $\frac{2-2}{0}$, so a hidden common factor must be found.

**Conjugate:** $(\sqrt{x}-2)(\sqrt{x}+2)=x-4$ for $x\ge0$. Multiplying by the conjugate makes the factor $x-4$ appear explicitly in the numerator.

**Continuity:** $\sqrt{x}$ is continuous on $[0,\infty)$, so $\sqrt{x}\to2$ as $x\to4$.

---

## Step-by-Step Solution

**Step 1: Multiply by the conjugate.**

For $x\ge0$, $x\neq4$:

$$
\frac{\sqrt{x}-2}{x-4}=\frac{(\sqrt{x}-2)(\sqrt{x}+2)}{(x-4)(\sqrt{x}+2)}=\frac{x-4}{(x-4)(\sqrt{x}+2)}.
$$

*Why this is valid:* $\sqrt{x}+2\ge2>0$, so we multiply by a fraction equal to $1$.

**Step 2: Cancel $x-4$.**

$$
\frac{x-4}{(x-4)(\sqrt{x}+2)}=\frac{1}{\sqrt{x}+2}\qquad\mathrm{for}\ x\neq4.
$$

**Step 3: Take the limit.**

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}=\lim_{x\to4}\frac{1}{\sqrt{x}+2}=\frac{1}{2+2}=\frac14.
$$

---

## Comparison with Exercise 3

In both exercises a square root sits in a difference that is hard to evaluate directly: $\infty-\infty$ in Exercise 3 and $0-0$ over $0$ here. In both cases the conjugate uses $(A-B)(A+B)=A^2-B^2$ to remove the root. The difference is in what happens next: for the sequence the conjugate produced a quotient of two terms of order $n$, which we handled by dominant terms, while here it produced a common factor $x-4$, which we cancelled. The same algebraic technique serves two different types of limits.

---

## Final Answer in Words

$$
\lim_{x\to4}\frac{\sqrt{x}-2}{x-4}=\frac14.
$$

Rationalizing the numerator exposes the factor $x-4$, which cancels and leaves $\frac{1}{\sqrt{x}+2}$.

---

## Quick Verification

Factoring in another way: $x-4=(\sqrt{x}-2)(\sqrt{x}+2)$, so the fraction is $\frac{1}{\sqrt x+2}$ directly. Numerically,

$$
f(4.01)=\frac{\sqrt{4.01}-2}{0.01}\approx\frac{0.0024984}{0.01}\approx0.24984,
$$

which is close to $0.25$. The limit is also the derivative of $\sqrt{x}$ at $x=4$, namely $\frac{1}{2\sqrt4}=\frac14$.

---

## Common Mistakes

- **Multiplying only the numerator by the conjugate:** the denominator must be multiplied too.
- **Expanding $(x-4)(\sqrt{x}+2)$:** this hides the factor that should be cancelled.
- **Forgetting that $x\ge0$:** the square root restricts the domain, although near $4$ this causes no problem.

---

## Oral Explanation (3 sentences)

Substituting $x=4$ gives $\frac00$, so we multiply the numerator and denominator by the conjugate $\sqrt{x}+2$. The numerator becomes $x-4$, which cancels with the denominator and leaves $\frac{1}{\sqrt{x}+2}$, whose limit at $4$ is $\frac14$. This is the same conjugate trick as in Exercise 3, now used to reveal a common factor instead of a dominant term.

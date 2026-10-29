# Exercise 7 — Limit at a Point and Canceling a Factor

## The Problem

Compute

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3}.
$$

Explain why the value of the function at $x=3$ is not needed to compute the limit.

---

## What Are We Looking For?

We want the value approached by the function as $x$ gets close to $3$, even though the formula cannot be evaluated at $x=3$ itself.

---

## Idea and Theorem Before the Calculation

**Definition of a limit at a point:** $\lim_{x\to a}f(x)=L$ concerns the values $f(x)$ for $x$ near $a$ with $x\neq a$. The value $f(a)$, if it exists, plays no role.

**Consequence:** If $f(x)=g(x)$ for all $x\neq a$ near $a$, then $f$ and $g$ have the same limit at $a$.

**Form $\frac00$:** Substituting $x=3$ gives $\frac{9-12+3}{0}=\frac00$, which signals a common factor $(x-3)$.

---

## Step-by-Step Solution

**Step 1: Factor the numerator.**

$$
x^2-4x+3=(x-1)(x-3).
$$

Check: $(x-1)(x-3)=x^2-3x-x+3=x^2-4x+3$.

**Step 2: Cancel for $x\neq3$.**

$$
\frac{x^2-4x+3}{x-3}=\frac{(x-1)(x-3)}{x-3}=x-1\qquad\mathrm{for}\ x\neq3.
$$

*Why this is valid:* Cancelling the factor $x-3$ is allowed only when $x-3\neq0$, and the limit uses only such $x$.

**Step 3: Take the limit.**

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3}=\lim_{x\to3}(x-1)=2.
$$

*Why this is valid:* $x-1$ is a polynomial, hence continuous, so its limit at $3$ is its value $3-1=2$.

---

## Why $f(3)$ Is Not Needed

The original function is not even defined at $x=3$, because the denominator is zero there. Its graph is the line $y=x-1$ with one point removed, a hole at $(3,2)$. The limit asks where the graph is heading as $x$ approaches $3$ from both sides, and it heads towards height $2$; whether the point $(3,2)$ itself belongs to the graph is a separate question.

---

## Final Answer in Words

$$
\lim_{x\to3}\frac{x^2-4x+3}{x-3}=2.
$$

The limit exists although the function is undefined at $x=3$, because the limit describes the behavior near $3$, not at $3$.

---

## Quick Verification

$$
f(2.99)=\frac{8.9401-11.96+3}{-0.01}=\frac{-0.0199}{-0.01}=1.99,\qquad f(3.01)=\frac{9.0601-12.04+3}{0.01}=\frac{0.0201}{0.01}=2.01.
$$

Both are close to $2$, from below and from above, in agreement with $f(x)=x-1$ for $x\neq3$.

---

## Common Mistakes

- **Concluding "$\frac00$, so no limit":** $\frac00$ is an indeterminate form, not an answer.
- **Claiming $f(3)=2$:** the function is still undefined at $3$; only the limit equals $2$.
- **Cancelling without the condition $x\neq3$:** the cancellation is legal precisely because the limit never uses $x=3$.

---

## Oral Explanation (3 sentences)

Substituting $x=3$ gives $\frac00$, which tells us that the numerator and denominator share the factor $x-3$. After factoring, the function equals $x-1$ for every $x\neq3$, so near $3$ its values approach $2$. The value at $x=3$ does not exist and is not needed, because a limit only looks at points close to $3$, never at $3$ itself.

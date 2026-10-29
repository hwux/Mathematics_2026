# Exercise 12 — Exponential Function Limit

## The Problem

Compute

$$
\lim_{x\to0}(1+3x)^{1/x}.
$$

Connect the result with the limit from Exercise 5 and show the appropriate transformation.

---

## What Are We Looking For?

We want the limit of a $1^\infty$ expression as $x\to0$, obtained by transforming it into the pattern that defines the number $e$.

---

## Idea and Theorem Before the Calculation

**Function version of Exercise 5:** The limit from Exercise 5 also holds for a real variable approaching $0$ from both sides:

$$
\lim_{t\to0}(1+t)^{1/t}=e.
$$

(For $t=\frac1n$ with $n\to\infty$ this is exactly Exercise 5.)

**Substitution in limits:** If $t=3x$, then $t\to0$ exactly when $x\to0$.

**Continuity of powers:** The function $u\mapsto u^3$ is continuous, so if $u(x)\to e$, then $u(x)^3\to e^3$.

---

## Step-by-Step Solution

**Step 1: Make the exponent match the inside.**

The pattern needs the exponent to be the reciprocal of the small term $3x$. Write

$$
\frac{1}{x}=\frac{1}{3x}\cdot3,
$$

so

$$
(1+3x)^{1/x}=\left[(1+3x)^{1/(3x)}\right]^{3}.
$$

*Why this is valid:* $(a^b)^c=a^{bc}$ for $a>0$; near $0$ we have $1+3x>0$.

**Step 2: Substitute $t=3x$.**

$$
\lim_{x\to0}(1+3x)^{1/(3x)}=\lim_{t\to0}(1+t)^{1/t}=e.
$$

**Step 3: Raise to the third power.**

$$
\lim_{x\to0}(1+3x)^{1/x}=\left[\lim_{x\to0}(1+3x)^{1/(3x)}\right]^3=e^3.
$$

---

## Connection with Exercise 5

Exercise 5 gives $\left(1+\frac1n\right)^n\to e$: a small quantity added to $1$, raised to the reciprocal of that same small quantity. Here the small quantity is $3x$, but the exponent is $\frac1x$, three times its reciprocal. Rewriting the exponent as $\frac{1}{3x}\cdot3$ exposes the pattern of Exercise 5 inside and an extra cube outside.

---

## Final Answer in Words

$$
\lim_{x\to0}(1+3x)^{1/x}=e^3\approx20.0855.
$$

After rewriting the expression as $\left[(1+3x)^{1/(3x)}\right]^3$, the bracket tends to $e$ by the classical limit, so the whole expression tends to $e^3$.

---

## Quick Verification

With logarithms: $\ln(1+3x)^{1/x}=\frac{\ln(1+3x)}{x}=3\cdot\frac{\ln(1+3x)}{3x}\to3\cdot1=3$, so the expression tends to $e^3$. Numerically,

| $x$ | $0.1$ | $0.01$ | $0.001$ | $-0.01$ |
|---|---|---|---|---|
| $(1+3x)^{1/x}$ | $13.79$ | $19.22$ | $19.996$ | $21.03$ |

The values approach $e^3\approx20.09$ from both sides.

---

## Common Mistakes

- **Answering $e$:** the exponent is $\frac1x$, not $\frac{1}{3x}$; the factor $3$ ends up in the exponent of $e$.
- **Answering $3e$:** the factor $3$ multiplies the exponent, not the result.
- **"$1^\infty=1$":** this is an indeterminate form.

---

## Oral Explanation (3 sentences)

The expression has the form $1^\infty$, which is the pattern of the number $e$ from Exercise 5, but the exponent $\frac1x$ is not the reciprocal of the small term $3x$. Writing $\frac1x=\frac{1}{3x}\cdot3$ gives $\left[(1+3x)^{1/(3x)}\right]^3$, and the bracket tends to $e$. Therefore the limit equals $e^3$.

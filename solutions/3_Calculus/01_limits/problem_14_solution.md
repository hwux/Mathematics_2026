# Exercise 14 — A $0/0$ Limit with Trigonometry

## The Problem

Compute

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}.
$$

Justify the result without using l'Hôpital's rule, using a trigonometric identity and the fundamental limit.

---

## What Are We Looking For?

We want the limit of a $\frac00$ expression with a cosine, obtained by turning $1-\cos x$ into a square of a sine so that the fundamental limit applies.

---

## Idea and Theorem Before the Calculation

**Half-angle identity:**

$$
1-\cos x=2\sin^2\frac{x}{2}.
$$

It follows from $\cos2\alpha=1-2\sin^2\alpha$ with $\alpha=\frac{x}{2}$.

**Fundamental limit:** $\lim_{u\to0}\frac{\sin u}{u}=1$, here with $u=\frac{x}{2}$.

**Continuity of squaring:** If $g(x)\to1$, then $g(x)^2\to1$.

---

## Step-by-Step Solution

**Step 1: Apply the identity.**

$$
\frac{1-\cos x}{x^2}=\frac{2\sin^2\frac{x}{2}}{x^2}.
$$

**Step 2: Match the argument $\frac{x}{2}$.**

Since $x^2=4\left(\frac{x}{2}\right)^2$,

$$
\frac{2\sin^2\frac{x}{2}}{4\left(\frac{x}{2}\right)^2}=\frac12\left(\frac{\sin\frac{x}{2}}{\frac{x}{2}}\right)^2.
$$

*Why this is valid:* We only rewrote $x^2$; for $x\neq0$ nothing is divided by zero.

**Step 3: Take the limit.**

With $u=\frac{x}{2}\to0$, the bracket tends to $1$, so

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12\cdot1^2=\frac12.
$$

---

## Final Answer in Words

$$
\lim_{x\to0}\frac{1-\cos x}{x^2}=\frac12.
$$

The half-angle identity turns $1-\cos x$ into $2\sin^2\frac x2$, and the fundamental limit applied to $\frac{\sin(x/2)}{x/2}$ gives the factor $1$, leaving $\frac12$.

---

## Quick Verification

A second method uses the conjugate $1+\cos x$:

$$
\frac{1-\cos x}{x^2}=\frac{(1-\cos x)(1+\cos x)}{x^2(1+\cos x)}=\frac{\sin^2x}{x^2}\cdot\frac{1}{1+\cos x}\longrightarrow1\cdot\frac{1}{2}=\frac12.
$$

Numerically, for $x=0.1$ the quotient is about $0.49958$, and for $x=0.01$ about $0.4999958$.

---

## Common Mistakes

- **Using $1-\cos x=\sin^2x$:** the correct identity is $1-\cos^2x=\sin^2x$; $1-\cos x$ needs the half-angle formula.
- **Forgetting the factor $4$:** $x^2=4\left(\frac x2\right)^2$, not $2\left(\frac x2\right)^2$.
- **Answering $0$ or $1$:** the numerator and denominator both tend to $0$, and their ratio is $\frac12$.

---

## Oral Explanation (3 sentences)

The expression is a $\frac00$ form, and the identity $1-\cos x=2\sin^2\frac{x}{2}$ turns the numerator into a square of a sine. Writing $x^2=4\left(\frac{x}{2}\right)^2$ gives $\frac12\left(\frac{\sin(x/2)}{x/2}\right)^2$, and the bracket tends to $1$ by the fundamental limit. The limit therefore equals $\frac12$, which we confirm with the conjugate method.

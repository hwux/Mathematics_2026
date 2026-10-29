# Exercise 13 — Fundamental Trigonometric Limit

## The Problem

Using

$$
\lim_{x\to0}\frac{\sin x}{x}=1,
$$

compute

$$
\lim_{x\to0}\frac{\sin5x}{x},\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}.
$$

In each case, show how you reduce the expression to the fundamental limit.

---

## What Are We Looking For?

We want two $\frac00$ limits involving sines, each rewritten so that every sine is divided by exactly its own argument.

---

## Idea and Theorem Before the Calculation

**Fundamental limit with a substitution:** If $u(x)\to0$ and $u(x)\neq0$ near $0$, then

$$
\lim_{x\to0}\frac{\sin u(x)}{u(x)}=1.
$$

In particular, for a constant $k\neq0$,

$$
\lim_{x\to0}\frac{\sin kx}{kx}=1\qquad\mathrm{and}\qquad\lim_{x\to0}\frac{kx}{\sin kx}=1.
$$

**Rule of thumb:** The argument of the sine must also appear in the denominator.

---

## Step-by-Step Solution

**First limit.**

**Step 1:** Multiply and divide by $5$:

$$
\frac{\sin5x}{x}=5\cdot\frac{\sin5x}{5x}.
$$

**Step 2:** With $u=5x\to0$:

$$
\lim_{x\to0}\frac{\sin5x}{x}=5\cdot1=5.
$$

**Second limit.**

**Step 1:** Insert the matching arguments:

$$
\frac{\sin2x}{\sin3x}=\frac{\sin2x}{2x}\cdot\frac{3x}{\sin3x}\cdot\frac{2x}{3x}.
$$

*Why this is valid:* The added factors multiply to $\frac{1}{2x}\cdot3x\cdot\frac{2x}{3x}=1$ for $x\neq0$.

**Step 2:** Take the limit of each factor:

$$
\frac{\sin2x}{2x}\to1,\qquad \frac{3x}{\sin3x}\to1,\qquad \frac{2x}{3x}=\frac23.
$$

**Step 3:**

$$
\lim_{x\to0}\frac{\sin2x}{\sin3x}=1\cdot1\cdot\frac23=\frac23.
$$

---

## Final Answer in Words

$$
\lim_{x\to0}\frac{\sin5x}{x}=5,\qquad \lim_{x\to0}\frac{\sin2x}{\sin3x}=\frac23.
$$

In both cases each sine was paired with its own argument, which turned it into the fundamental limit, and the remaining constant factors gave the answer.

---

## Quick Verification

Near $0$, $\sin u\approx u$, so $\frac{\sin5x}{x}\approx\frac{5x}{x}=5$ and $\frac{\sin2x}{\sin3x}\approx\frac{2x}{3x}=\frac23$. Numerically, for $x=0.01$:

$$
\frac{\sin0.05}{0.01}\approx4.9979,\qquad \frac{\sin0.02}{\sin0.03}\approx0.66672.
$$

---

## Common Mistakes

- **Cancelling inside the sine:** $\frac{\sin5x}{x}\neq\sin5$; the sine is not a factor that can be cancelled.
- **Answering $1$:** the fundamental limit needs the same argument in the sine and in the denominator.
- **Writing $\frac{\sin2x}{\sin3x}=\frac{\sin2}{\sin3}$:** $x$ is inside the sine and cannot be cancelled.

---

## Oral Explanation (3 sentences)

The fundamental limit $\frac{\sin u}{u}\to1$ works only when the sine is divided by exactly its own argument. For $\frac{\sin5x}{x}$ we multiply and divide by $5$ to get $5\cdot\frac{\sin5x}{5x}$, which tends to $5$. For $\frac{\sin2x}{\sin3x}$ we pair $\sin2x$ with $2x$ and $\sin3x$ with $3x$, and what remains is $\frac{2x}{3x}=\frac23$.

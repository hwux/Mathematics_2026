# Problem 6 — A Logarithmic Function

## The Problem

Analyze the domain, zero, and monotonicity of

$$
f(x)=\ln x-x+1.
$$

Explain why the analysis must begin with the domain.

---

## What Are We Looking For?

We want the set where $f$ is defined, its zeros, and the intervals where it increases or decreases.

---

## Idea and Theorem Before the Calculation

**Domain of the logarithm:** $\ln x$ is defined only for $x>0$.

**Derivative:** $(\ln x)'=\frac1x$ for $x>0$.

**First derivative test** for extrema.

---

## Step-by-Step Solution

**Step 1: Domain.**

$$
D_f=(0,\infty).
$$

**Step 2: Derivative.**

$$
f'(x)=\frac1x-1=\frac{1-x}{x}.
$$

**Step 3: Sign of $f'$ on the domain.**

For $x>0$ the denominator is positive, so the sign is the sign of $1-x$:

- $0<x<1$: $f'>0$, $f$ is increasing on $(0,1]$,
- $x>1$: $f'<0$, $f$ is decreasing on $[1,\infty)$.

**Step 4: Maximum.**

At $x=1$ the sign changes from $+$ to $-$:

$$
f(1)=\ln1-1+1=0.
$$

This is the global maximum on the domain.

**Step 5: Zero.**

Since the maximum value is $0$ and it is attained only at $x=1$, we have $f(x)<0$ for every $x\neq1$. Hence $x=1$ is the only zero.

**Step 6: Limits at the ends.**

$$
\lim_{x\to0^+}(\ln x-x+1)=-\infty,\qquad \lim_{x\to\infty}(\ln x-x+1)=-\infty,
$$

the second because $x$ grows much faster than $\ln x$.

---

## Why Begin with the Domain

The sign of $f'(x)=\frac{1-x}{x}$ depends on the sign of $x$. Without the domain one might read the formula on all of $\mathbb{R}\setminus\{0\}$ and claim that $f'<0$ for $x<0$, describing a part of the graph that does not exist. The domain also tells us where the ends of the graph are ($0^+$ and $+\infty$), so it determines which limits must be computed.

---

## Final Answer in Words

The domain is $(0,\infty)$. The function increases on $(0,1]$, decreases on $[1,\infty)$, and has its global maximum $f(1)=0$. Consequently $x=1$ is the only zero and $f(x)<0$ elsewhere, which is the well-known inequality $\ln x\le x-1$.

---

## Quick Verification

$f(e)=1-e+1=2-e\approx-0.72<0$ and $f\!\left(\frac1e\right)=-1-\frac1e+1=-\frac1e<0$, both negative as predicted. Geometrically, $y=x-1$ is the tangent to $y=\ln x$ at $x=1$, and the concave logarithm lies below its tangent.

---

## Common Mistakes

- **Starting with $f'$ on $\mathbb{R}$:** the logarithm restricts the analysis to $x>0$.
- **Looking for more zeros:** the maximum is $0$, so there is only one.
- **Wrong sign of $f'$:** at $x=\frac12$, $f'=1>0$, so the function increases before $1$.

---

## Oral Explanation (3 sentences)

The function contains $\ln x$, so it is defined only for $x>0$, and every later step lives on this interval. The derivative $\frac{1-x}{x}$ is positive for $0<x<1$ and negative for $x>1$, so the function increases to its maximum $f(1)=0$ and then decreases. Because the largest value is $0$, the point $x=1$ is the only zero, and the function is negative everywhere else.

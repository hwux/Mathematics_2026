# Problem 10 — Definite Integral and Checking the Result

## The Problem

Before carrying out the exact calculation, estimate the possible range of values of the integral

$$
\int_0^2(x^2+1)\,dx,
$$

using

$$
1\le x^2+1\le5
$$

on $[0,2]$. Only then compute the integral exactly, compare the result with the earlier estimate, and explain what type of computational error such a check can detect.

---

## What Are We Looking For?

We want bounds for the integral from bounds on the integrand, the exact value, and a discussion of what such a check can reveal.

---

## Idea and Theorem Before the Calculation

**Comparison property:** If $m\le f(x)\le M$ on $[a,b]$, then

$$
m(b-a)\le\int_a^bf(x)\,dx\le M(b-a).
$$

Geometrically, the region under the graph lies between a rectangle of height $m$ and one of height $M$.

---

## Step-by-Step Solution

**Step 1: Estimate.**

On $[0,2]$ the integrand is between $1$ (at $x=0$) and $5$ (at $x=2$), and the interval has length $2$:

$$
2=1\cdot2\le\int_0^2(x^2+1)\,dx\le5\cdot2=10.
$$

**Step 2: Exact value.**

$$
\int_0^2(x^2+1)\,dx=\left[\frac{x^3}{3}+x\right]_0^2=\frac83+2=\frac{14}{3}\approx4.67.
$$

**Step 3: Compare.**

$2\le4.67\le10$, so the exact result lies in the predicted range. It lies closer to the lower bound, which is reasonable: $x^2+1$ is small on most of the interval and reaches $5$ only at the right end.

---

## What Errors the Check Detects

The estimate catches gross errors that move the result out of $[2,10]$:

- a sign error, for example $\frac83-2=\frac23$,
- forgetting a term or a factor that badly changes the size, for example using $x^3+x$ as antiderivative (giving $10$, which is suspicious because the upper bound could only be reached if $f$ were $5$ everywhere),
- evaluating only at one limit or subtracting in the wrong order, giving a negative value.

It does **not** catch small errors that stay inside the range: for example the incorrect antiderivative $x^2+x$ gives $6$, which still looks plausible. A sharper estimate (such as the trapezoidal rule, $\frac{2}{2}(1+5)=6$, an overestimate for a convex function, or the midpoint rule $2\cdot f(1)=4$, an underestimate) narrows the range to $[4,6]$.

---

## Final Answer in Words

The bounds $1\le x^2+1\le5$ give $2\le\int_0^2(x^2+1)\,dx\le10$. The exact value is $\frac{14}{3}\approx4.67$, which lies in this range. Such a check detects gross errors in sign, size or order of evaluation, but not errors that keep the result within the bounds.

---

## Quick Verification

Simpson's rule is exact for polynomials of degree at most $3$:

$$
\frac{2}{6}\left(f(0)+4f(1)+f(2)\right)=\frac13(1+8+5)=\frac{14}{3}.
$$

---

## Common Mistakes

- **Estimating with the wrong interval length:** the length is $2$, not $1$.
- **Assuming the result is the average of the bounds:** the bounds only give a range.
- **Skipping the estimate after computing:** it is cheap and catches many errors.

---

## Oral Explanation (3 sentences)

Since $x^2+1$ lies between $1$ and $5$ on an interval of length $2$, the integral must lie between $2$ and $10$. The exact computation gives $\frac{8}{3}+2=\frac{14}{3}\approx4.67$, which is inside the predicted range. Such a check reveals sign errors and large mistakes, but it cannot detect errors that still produce a value inside the bounds.

# Problem 13 — An Integral Depending on the Upper Limit

## The Problem

Let

$$
F(x)=\int_0^x(t^2+1)\,dt.
$$

Determine $F(x)$, compute $F'(x)$, and compare the result with the integrand. Explain in your own words why the height of the function describes the local rate of increase of the accumulated area.

---

## What Are We Looking For?

We want an explicit formula for the accumulated area $F(x)$, its derivative, and an explanation of why this derivative equals the integrand.

---

## Idea and Theorem Before the Calculation

**Accumulation function:** $F(x)$ is the area under $y=t^2+1$ from $t=0$ to $t=x$; the variable $x$ is the moving right end.

**Fundamental theorem of calculus (first part):** If $f$ is continuous, then

$$
\frac{d}{dx}\int_a^xf(t)\,dt=f(x).
$$

---

## Step-by-Step Solution

**Step 1: Compute $F(x)$.**

$$
F(x)=\left[\frac{t^3}{3}+t\right]_{t=0}^{t=x}=\frac{x^3}{3}+x.
$$

**Step 2: Differentiate.**

$$
F'(x)=x^2+1.
$$

**Step 3: Compare.**

$F'(x)=x^2+1$ is the integrand $t^2+1$ evaluated at the upper limit $t=x$, as the fundamental theorem predicts. Also $F(0)=0$, since no area has accumulated yet.

---

## Why Height Gives the Rate of Increase

Move the right end from $x$ to $x+h$ with a small $h>0$. The extra area is a thin strip of width $h$ under the graph, and its height is almost $f(x)=x^2+1$, because $f$ is continuous:

$$
F(x+h)-F(x)\approx f(x)\cdot h\quad\Longrightarrow\quad\frac{F(x+h)-F(x)}{h}\approx f(x).
$$

As $h\to0$ the approximation becomes exact, so $F'(x)=f(x)$. In words: the taller the graph at $x$, the faster the area grows when the end point moves to the right.

---

## Final Answer in Words

$$
F(x)=\frac{x^3}{3}+x,\qquad F'(x)=x^2+1.
$$

The derivative of the accumulated area equals the height of the integrand at the moving end, because a small step $h$ adds a strip of area approximately $f(x)\cdot h$.

---

## Quick Verification

At $x=1$: $F(1)=\frac43$, and $F(1.01)=\frac{1.030301}{3}+1.01\approx1.353434$. The increase $0.020100$ divided by $0.01$ is about $2.01$, close to $f(1)=2$, the height of the graph at $x=1$.

---

## Common Mistakes

- **Writing $F'(x)=t^2+1$:** the result must be expressed in $x$, the upper limit.
- **Forgetting the lower limit:** $F(x)=\frac{x^3}{3}+x-0$; here the lower limit contributes $0$, but in general it does not.
- **Thinking $F'$ depends on the lower limit:** changing $0$ to another constant shifts $F$ but does not change $F'$.

---

## Oral Explanation (3 sentences)

The accumulated area from $0$ to $x$ under $t^2+1$ equals $\frac{x^3}{3}+x$, and its derivative is $x^2+1$, exactly the integrand at $x$. This happens because moving the right end by a small $h$ adds a thin strip whose area is almost the height $f(x)$ times the width $h$. So the height of the graph tells how fast the area is growing at that point, which is the content of the fundamental theorem of calculus.

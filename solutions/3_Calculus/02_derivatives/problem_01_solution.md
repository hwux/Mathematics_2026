# Problem 1 — Derivative of a Polynomial and the Slope of a Tangent Line

## The Problem

For

$$
f(x)=3x^5-2x^3+7x-4
$$

find $f'(x)$. Then compute $f'(0)$ and $f'(1)$, determine the signs of the obtained values, and explain what they say about the slope of the tangent line to the graph at these two points.

---

## What Are We Looking For?

We want the derivative of a polynomial, its values at $x=0$ and $x=1$, and the geometric meaning of these values as slopes of tangent lines.

---

## Idea and Theorem Before the Calculation

**Power rule:** $(x^n)'=nx^{n-1}$ for every natural $n$; in particular $(x)'=1$ and $(c)'=0$ for a constant $c$.

**Linearity:** $(af+bg)'=af'+bg'$, so a polynomial is differentiated term by term.

**Geometric meaning:** $f'(x_0)$ is the slope of the tangent line to the graph at $(x_0,f(x_0))$. A positive slope means the tangent rises from left to right, a negative slope means it falls.

---

## Step-by-Step Solution

**Step 1: Differentiate term by term.**

$$
f'(x)=3\cdot5x^4-2\cdot3x^2+7\cdot1-0=15x^4-6x^2+7.
$$

*Why this is valid:* Linearity splits the derivative into terms, and each term is a constant times a power.

**Step 2: Value at $0$.**

$$
f'(0)=15\cdot0-6\cdot0+7=7>0.
$$

**Step 3: Value at $1$.**

$$
f'(1)=15-6+7=16>0.
$$

**Step 4: Interpretation.**

Both values are positive, so at $x=0$ and at $x=1$ the tangent lines rise from left to right and the function is increasing there. The tangent at $x=1$ (slope $16$) is much steeper than the tangent at $x=0$ (slope $7$).

---

## Final Answer in Words

$$
f'(x)=15x^4-6x^2+7,\qquad f'(0)=7,\qquad f'(1)=16.
$$

Both values are positive, so the tangent lines at $x=0$ and $x=1$ rise to the right; the one at $x=1$ is more than twice as steep.

---

## Quick Verification

Difference quotient at $x=1$ with $h=0.001$: $f(1)=3-2+7-4=4$ and $f(1.001)\approx4.016024$, so

$$
\frac{f(1.001)-f(1)}{0.001}\approx16.024,
$$

which is close to $f'(1)=16$. In fact $f'(x)>0$ for all $x$: as a quadratic in $t=x^2$, $15t^2-6t+7$ has discriminant $36-420<0$.

---

## Common Mistakes

- **Not lowering the exponent:** $(3x^5)'=15x^4$, not $15x^5$.
- **Keeping the constant:** the derivative of $-4$ is $0$.
- **Confusing $f'(0)$ with $f(0)$:** $f(0)=-4$ is a height, $f'(0)=7$ is a slope.

---

## Oral Explanation (3 sentences)

We differentiate the polynomial term by term with the power rule and get $f'(x)=15x^4-6x^2+7$. At $x=0$ the derivative equals $7$ and at $x=1$ it equals $16$, both positive. This means that the tangent lines at these points rise to the right, and the graph is steeper at $x=1$ than at $x=0$.

# Problem 2 — Powers, Roots, and the Domain

## The Problem

Compute

$$
\int\left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)\,dx.
$$

First rewrite the terms as powers, determine the domain of the original expression, and verify the result by differentiation.

---

## What Are We Looking For?

We want the family of antiderivatives of an expression with roots and a reciprocal power, the interval on which the calculation is valid, and a check by differentiation.

---

## Idea and Theorem Before the Calculation

**Rewriting:** $\sqrt{x}=x^{1/2}$, $\frac{1}{x^2}=x^{-2}$, and $x^{1/3}=\sqrt[3]{x}$.

**Power rule:** $\int x^r\,dx=\frac{x^{r+1}}{r+1}+C$ for every real $r\neq-1$, on an interval where $x^r$ is defined.

---

## Step-by-Step Solution

**Step 1: Powers.**

$$
2\sqrt{x}+\frac{3}{x^2}-x^{1/3}=2x^{1/2}+3x^{-2}-x^{1/3}.
$$

**Step 2: Domain.**

- $\sqrt{x}$ requires $x\ge0$,
- $\frac{3}{x^2}$ requires $x\neq0$,
- $x^{1/3}=\sqrt[3]{x}$ is defined for all real $x$.

Together: $x\in(0,\infty)$.

**Step 3: Integrate each term.**

$$
\int2x^{1/2}\,dx=2\cdot\frac{x^{3/2}}{3/2}=\frac43x^{3/2},
$$

$$
\int3x^{-2}\,dx=3\cdot\frac{x^{-1}}{-1}=-\frac{3}{x},
$$

$$
\int x^{1/3}\,dx=\frac{x^{4/3}}{4/3}=\frac34x^{4/3}.
$$

**Step 4: Combine.**

$$
\int\left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)dx=\frac43x^{3/2}-\frac3x-\frac34x^{4/3}+C,\qquad x>0.
$$

**Step 5: Verify.**

$$
\left(\frac43x^{3/2}\right)'=2x^{1/2},\qquad \left(-\frac3x\right)'=\frac{3}{x^2},\qquad \left(-\frac34x^{4/3}\right)'=-x^{1/3}.
$$

The sum is the original integrand.

---

## Final Answer in Words

On the domain $x>0$,

$$
\int\left(2\sqrt{x}+\frac{3}{x^2}-x^{1/3}\right)dx=\frac43x^{3/2}-\frac{3}{x}-\frac34x^{4/3}+C.
$$

Differentiating the result returns the integrand term by term.

---

## Quick Verification

Numerical check of the derivative at $x=1$: the antiderivative $G(x)=\frac43x^{3/2}-\frac3x-\frac34x^{4/3}$ has $G(1)\approx-2.41667$ and $G(1.001)\approx-2.41267$, so

$$
\frac{G(1.001)-G(1)}{0.001}\approx3.997,
$$

while the integrand at $x=1$ equals $2+3-1=4$.

---

## Common Mistakes

- **$\int\frac{3}{x^2}\,dx=3\ln x^2$:** the logarithm appears only for $x^{-1}$.
- **Sign error:** $\int3x^{-2}\,dx=-3x^{-1}$, with a minus sign.
- **Ignoring the domain:** the result is valid on $(0,\infty)$, where the original expression is defined.

---

## Oral Explanation (3 sentences)

After rewriting the terms as $2x^{1/2}$, $3x^{-2}$ and $-x^{1/3}$, each can be integrated by the power rule, giving $\frac43x^{3/2}-\frac3x-\frac34x^{4/3}+C$. The original expression is defined only for $x>0$, because of the square root and the division by $x^2$. Differentiating the result returns each term of the integrand, which confirms the calculation.

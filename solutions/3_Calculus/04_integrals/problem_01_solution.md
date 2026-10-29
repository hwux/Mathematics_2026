# Problem 1 — Antiderivative and Verification

## The Problem

For

$$
f(x)=3x^2-4x+5
$$

find one antiderivative $F(x)$. Write the entire family of antiderivatives, verify the result by differentiation, and explain the meaning of the constant $C$.

---

## What Are We Looking For?

We want a function whose derivative is $3x^2-4x+5$, the set of all such functions, a check by differentiation, and the meaning of the arbitrary constant.

---

## Idea and Theorem Before the Calculation

**Antiderivative:** $F$ is an antiderivative of $f$ on an interval if $F'(x)=f(x)$ there.

**Power rule for integrals:**

$$
\int x^n\,dx=\frac{x^{n+1}}{n+1}+C\qquad(n\neq-1).
$$

**Linearity:** $\int(af+bg)\,dx=a\int f\,dx+b\int g\,dx$.

**Uniqueness up to a constant:** If $F'=G'$ on an interval, then $F-G$ is constant there.

---

## Step-by-Step Solution

**Step 1: Integrate term by term.**

$$
\int3x^2\,dx=x^3,\qquad \int(-4x)\,dx=-2x^2,\qquad \int5\,dx=5x.
$$

**Step 2: One antiderivative.**

$$
F(x)=x^3-2x^2+5x.
$$

**Step 3: The whole family.**

$$
\int(3x^2-4x+5)\,dx=x^3-2x^2+5x+C,\qquad C\in\mathbb{R}.
$$

**Step 4: Verify by differentiation.**

$$
\left(x^3-2x^2+5x+C\right)'=3x^2-4x+5+0=f(x).
$$

---

## Meaning of the Constant $C$

The derivative of every constant is zero, so adding a constant to an antiderivative gives another antiderivative. Conversely, any two antiderivatives of $f$ on $\mathbb{R}$ differ by a constant, so the formula with $C$ describes all of them. Geometrically, the graphs of the antiderivatives are vertical shifts of one another: they have the same slope at every $x$. A single extra condition, such as $F(0)=7$, would select one of them (here $C=7$).

---

## Final Answer in Words

One antiderivative is $F(x)=x^3-2x^2+5x$, and the family of all antiderivatives is $x^3-2x^2+5x+C$, $C\in\mathbb{R}$. Differentiation returns $3x^2-4x+5$, and $C$ expresses that the antiderivative is determined only up to a vertical shift.

---

## Quick Verification

Check at a point with the fundamental theorem: $\int_0^1(3x^2-4x+5)\,dx=F(1)-F(0)=1-2+5=4$. Direct estimate: on $[0,1]$ the integrand stays between $3$ and $5$ (its minimum is $f(\frac23)=\frac{11}{3}$), so the integral must lie in $[3,5]$, and $4$ does.

---

## Common Mistakes

- **Forgetting to divide by the new exponent:** $\int3x^2\,dx=x^3$, not $3x^3$.
- **Omitting $C$ in the family:** without it only one antiderivative is described.
- **Writing $\int5\,dx=5$:** the antiderivative of a constant is $5x$.

---

## Oral Explanation (3 sentences)

Integrating term by term with the power rule gives the antiderivative $x^3-2x^2+5x$. Differentiating it returns $3x^2-4x+5$, which confirms the result. Because constants have zero derivative, every function $x^3-2x^2+5x+C$ is also an antiderivative, and $C$ represents a vertical shift of the graph.

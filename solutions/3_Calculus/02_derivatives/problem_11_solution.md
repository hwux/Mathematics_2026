# Problem 11 — Derivative from the Definition

## The Problem

Using only

$$
f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}h,
$$

find the derivative of $f(x)=x^2$. Compare the result with the power rule and indicate where the limit is used in the calculation.

---

## What Are We Looking For?

We want to compute $(x^2)'$ directly from the limit definition, without any differentiation rules, and to see exactly which step requires the limit.

---

## Idea and Theorem Before the Calculation

**Definition:** The derivative is the limit of the slopes of secant lines through $(x,f(x))$ and $(x+h,f(x+h))$ as $h\to0$.

**Strategy:** Expand $f(x+h)$, simplify the difference quotient algebraically for $h\neq0$, and only then pass to the limit.

---

## Step-by-Step Solution

**Step 1: Compute $f(x+h)$.**

$$
f(x+h)=(x+h)^2=x^2+2xh+h^2.
$$

**Step 2: Difference.**

$$
f(x+h)-f(x)=2xh+h^2.
$$

**Step 3: Difference quotient.**

For $h\neq0$,

$$
\frac{f(x+h)-f(x)}{h}=\frac{2xh+h^2}{h}=2x+h.
$$

*Why this is valid:* Cancelling $h$ is allowed because $h\neq0$; the limit never uses $h=0$.

**Step 4: Limit.**

$$
f'(x)=\lim_{h\to0}(2x+h)=2x.
$$

This is the only step where the limit is used. Before it, $h$ is a fixed nonzero number and the quotient $2x+h$ is the exact slope of a secant line.

---

## Comparison with the Power Rule

The power rule $(x^n)'=nx^{n-1}$ with $n=2$ gives $(x^2)'=2x$, the same result. The definition explains where the rule comes from: in $(x+h)^n=x^n+nx^{n-1}h+(\mathrm{terms\ with}\ h^2,h^3,\ldots)$, after subtracting $x^n$ and dividing by $h$, only $nx^{n-1}$ survives the limit.

---

## Final Answer in Words

$$
f'(x)=\lim_{h\to0}\frac{(x+h)^2-x^2}{h}=\lim_{h\to0}(2x+h)=2x.
$$

This agrees with the power rule. The limit is used only in the last step, to remove the term $h$ from the secant slope $2x+h$.

---

## Quick Verification

At $x=3$ the secant slope is $6+h$: for $h=0.1$ it is $6.1$, and directly $\frac{3.1^2-9}{0.1}=\frac{0.61}{0.1}=6.1$. As $h\to0$ these slopes approach $6=2\cdot3$.

---

## Common Mistakes

- **$(x+h)^2=x^2+h^2$:** the middle term $2xh$ is the one that produces the derivative.
- **Substituting $h=0$ before cancelling:** this gives $\frac00$.
- **Thinking the limit is used everywhere:** Steps 1 to 3 are pure algebra.

---

## Oral Explanation (3 sentences)

We expand $(x+h)^2$, subtract $x^2$ and divide by $h$, which for $h\neq0$ gives the secant slope $2x+h$. Only then do we let $h$ tend to $0$, and the secant slopes approach $2x$, the slope of the tangent. This is the same answer as the power rule, which is in fact proved by this calculation.

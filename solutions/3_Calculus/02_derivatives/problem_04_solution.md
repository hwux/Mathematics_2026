# Problem 4 — A Quotient and Domain Control

## The Problem

For

$$
f(x)=\frac{x^2+1}{x-1}
$$

determine the domain, compute the derivative, simplify the result, and explain why the restriction $x\neq1$ remains important.

---

## What Are We Looking For?

We want the domain of a rational function, its derivative by the quotient rule in simplified form, and the role of the excluded point $x=1$.

---

## Idea and Theorem Before the Calculation

**Quotient rule:** For $v(x)\neq0$,

$$
\left(\frac{u}{v}\right)'=\frac{u'v-uv'}{v^2}.
$$

**Domain:** A derivative can only exist where the function itself is defined.

---

## Step-by-Step Solution

**Step 1: Domain.**

The denominator vanishes at $x=1$, so

$$
D_f=\mathbb{R}\setminus\{1\}.
$$

**Step 2: Name the parts.**

$$
u=x^2+1,\quad u'=2x,\qquad v=x-1,\quad v'=1.
$$

**Step 3: Quotient rule.**

$$
f'(x)=\frac{2x(x-1)-(x^2+1)\cdot1}{(x-1)^2}.
$$

**Step 4: Simplify the numerator.**

$$
2x^2-2x-x^2-1=x^2-2x-1.
$$

Therefore

$$
f'(x)=\frac{x^2-2x-1}{(x-1)^2},\qquad x\neq1.
$$

---

## Why $x\neq1$ Still Matters

- The formula for $f'$ has $(x-1)^2$ in the denominator, so it is undefined at $x=1$; the derivative has the same domain as $f$.
- $f$ is not defined at $1$, so it cannot be differentiable there, whatever the formula might suggest.
- The point $x=1$ splits the domain into $(-\infty,1)$ and $(1,\infty)$. Statements about monotonicity must be made separately on each part, because the graph has a vertical asymptote $x=1$ between them.

---

## Final Answer in Words

$$
D_f=\mathbb{R}\setminus\{1\},\qquad f'(x)=\frac{x^2-2x-1}{(x-1)^2}\quad(x\neq1).
$$

The restriction $x\neq1$ remains, because neither the function nor its derivative is defined there, and it separates the domain into two intervals that must be studied independently.

---

## Quick Verification

Using division: $f(x)=x+1+\frac{2}{x-1}$, so

$$
f'(x)=1-\frac{2}{(x-1)^2}=\frac{(x-1)^2-2}{(x-1)^2}=\frac{x^2-2x-1}{(x-1)^2},
$$

which agrees. At $x=0$: $f'(0)=-1$, and the difference quotient $\frac{f(0.001)-f(0)}{0.001}$ with $f(0)=-1$, $f(0.001)\approx-1.001002$ gives about $-1.002$.

---

## Common Mistakes

- **Reversing the numerator:** $uv'-u'v$ gives the opposite sign.
- **Forgetting to square the denominator:** it is $(x-1)^2$, not $x-1$.
- **Dropping the domain after simplifying:** the simplified formula still requires $x\neq1$.

---

## Oral Explanation (3 sentences)

The function is defined for all $x$ except $1$, where the denominator vanishes. By the quotient rule, $f'(x)=\frac{2x(x-1)-(x^2+1)}{(x-1)^2}=\frac{x^2-2x-1}{(x-1)^2}$. The point $x=1$ stays excluded, because neither $f$ nor $f'$ exists there, and the graph has a vertical asymptote separating two parts of the domain.

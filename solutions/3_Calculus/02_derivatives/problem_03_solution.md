# Problem 3 — The Product Rule — Why Is It Needed?

## The Problem

For

$$
f(x)=(x^2+1)e^x
$$

compute the derivative. Then compare the correct result with the incorrect idea

$$
f'(x)\stackrel{?}{=}(2x)e^x
$$

and explain which term is missing.

---

## What Are We Looking For?

We want the correct derivative of a product, and an explanation of what goes wrong when only one factor is differentiated.

---

## Idea and Theorem Before the Calculation

**Product rule:**

$$
(uv)'=u'v+uv'.
$$

**Basic derivatives:** $(x^2+1)'=2x$ and $(e^x)'=e^x$.

**Meaning:** In a product, a change in $x$ changes both factors. The term $u'v$ measures the effect of the change in $u$, and $uv'$ the effect of the change in $v$.

---

## Step-by-Step Solution

**Step 1: Name the factors.**

$$
u=x^2+1,\quad u'=2x,\qquad v=e^x,\quad v'=e^x.
$$

**Step 2: Apply the product rule.**

$$
f'(x)=2x\,e^x+(x^2+1)e^x.
$$

**Step 3: Simplify.**

$$
f'(x)=e^x\left(x^2+2x+1\right)=(x+1)^2e^x.
$$

---

## The Incorrect Idea

The proposal $(2x)e^x$ differentiates only the first factor and keeps $e^x$ unchanged. It is exactly the term $u'v$ and misses

$$
uv'=(x^2+1)e^x.
$$

This missing term is the change caused by $e^x$ itself growing. The wrong formula fails even at one point: at $x=0$ it gives $0$, while the correct derivative is $f'(0)=(0+1)^2e^0=1$.

---

## Final Answer in Words

$$
f'(x)=2xe^x+(x^2+1)e^x=(x+1)^2e^x.
$$

The incorrect version $(2x)e^x$ omits the term $(x^2+1)e^x$, which comes from differentiating the factor $e^x$.

---

## Quick Verification

At $x=0$: $f(0)=1$ and $f(0.001)=1.000001\cdot e^{0.001}\approx1.0010015$, so

$$
\frac{f(0.001)-f(0)}{0.001}\approx1.0015,
$$

which matches $f'(0)=1$ and not the incorrect value $0$. Also $(x+1)^2e^x\ge0$, so $f$ is increasing on all of $\mathbb{R}$, with a horizontal tangent only at $x=-1$.

---

## Common Mistakes

- **$(uv)'=u'v'$:** this would give $2xe^x$ as well, the same wrong answer.
- **Differentiating only the "complicated" factor:** both factors depend on $x$.
- **Not factoring:** $(x+1)^2e^x$ shows immediately that $f'(x)\ge0$.

---

## Oral Explanation (3 sentences)

A product changes for two reasons at once, because both factors depend on $x$, and the product rule $(uv)'=u'v+uv'$ adds up both effects. Here this gives $2xe^x+(x^2+1)e^x=(x+1)^2e^x$. The incorrect idea $(2x)e^x$ keeps only the first effect and forgets the term $(x^2+1)e^x$, which already fails at $x=0$.

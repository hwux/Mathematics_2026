# Problem 12 — Several Rules at Once

## The Problem

For

$$
f(x)=(x^2+1)^3e^x
$$

compute the derivative. Before calculating, write down a plan: which rule applies to the whole expression and which rule applies to one of its factors. Finally, organize the result by factoring out common factors.

---

## What Are We Looking For?

We want the derivative of a product in which one factor is itself a composition, a plan saying in which order the rules are used, and a neatly factored result.

---

## Idea and Theorem Before the Calculation

**Plan:**

1. The whole expression is a product $u\cdot v$ with $u=(x^2+1)^3$ and $v=e^x$, so the outermost rule is the **product rule**.
2. The factor $u=(x^2+1)^3$ is a composition (a cube of $x^2+1$), so its derivative needs the **chain rule**.
3. The factor $v=e^x$ is a basic function: $v'=e^x$.

**Rules:**

$$
(uv)'=u'v+uv',\qquad \left(g(h(x))\right)'=g'(h(x))h'(x).
$$

---

## Step-by-Step Solution

**Step 1: Derivative of $u$ (chain rule).**

$$
u'=3(x^2+1)^2\cdot2x=6x(x^2+1)^2.
$$

**Step 2: Derivative of $v$.**

$$
v'=e^x.
$$

**Step 3: Product rule.**

$$
f'(x)=6x(x^2+1)^2e^x+(x^2+1)^3e^x.
$$

**Step 4: Factor out the common factors.**

Both terms contain $(x^2+1)^2e^x$:

$$
f'(x)=(x^2+1)^2e^x\left[6x+(x^2+1)\right]=(x^2+1)^2e^x\left(x^2+6x+1\right).
$$

---

## Final Answer in Words

$$
f'(x)=(x^2+1)^2e^x\left(x^2+6x+1\right).
$$

The product rule handles the whole expression, the chain rule handles the factor $(x^2+1)^3$, and the common factor $(x^2+1)^2e^x$ is pulled out at the end.

---

## Quick Verification

At $x=0$: $f'(0)=1\cdot1\cdot1=1$. Numerically $f(0)=1$ and $f(0.001)=(1.000001)^3e^{0.001}\approx1.0010035$, so the difference quotient is about $1.0035$. The factored form also tells the sign: $(x^2+1)^2e^x>0$, so $f'$ has the sign of $x^2+6x+1$, which is zero at $x=-3\pm2\sqrt2$.

---

## Common Mistakes

- **Starting with the chain rule on the whole expression:** the outermost operation is a product, not a composition.
- **Forgetting the factor $2x$:** $\left((x^2+1)^3\right)'=3(x^2+1)^2\cdot2x$.
- **Factoring out $(x^2+1)^3$:** the first term contains only the square, so the common factor is $(x^2+1)^2$.

---

## Oral Explanation (3 sentences)

The whole function is a product of $(x^2+1)^3$ and $e^x$, so we start with the product rule, and the first factor is a composition, so we differentiate it with the chain rule. This gives $6x(x^2+1)^2e^x+(x^2+1)^3e^x$. Factoring out $(x^2+1)^2e^x$ leaves the compact form $(x^2+1)^2e^x(x^2+6x+1)$.

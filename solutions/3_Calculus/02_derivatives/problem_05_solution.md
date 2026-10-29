# Problem 5 — The Chain Rule as Working Through Layers

## The Problem

For

$$
f(x)=(3x^2-2x+1)^5
$$

identify the inner and outer functions, compute their derivatives, and combine the result according to the chain rule. Explain the origin of the additional factor.

---

## What Are We Looking For?

We want to see $f$ as a composition of two functions, differentiate each one, and combine the results with the chain rule.

---

## Idea and Theorem Before the Calculation

**Chain rule:** If $f(x)=g(h(x))$, then

$$
f'(x)=g'(h(x))\cdot h'(x).
$$

The outer derivative is evaluated at the inner function, and then multiplied by the derivative of the inner function.

---

## Step-by-Step Solution

**Step 1: Identify the layers.**

$$
h(x)=3x^2-2x+1\quad(\mathrm{inner}),\qquad g(u)=u^5\quad(\mathrm{outer}).
$$

Then $f(x)=g(h(x))$.

**Step 2: Differentiate each layer.**

$$
g'(u)=5u^4,\qquad h'(x)=6x-2.
$$

**Step 3: Combine.**

$$
f'(x)=5\left(3x^2-2x+1\right)^4\cdot(6x-2).
$$

**Step 4: Simplify.**

Since $6x-2=2(3x-1)$,

$$
f'(x)=10(3x-1)\left(3x^2-2x+1\right)^4.
$$

---

## Origin of the Extra Factor

The outer function $u^5$ reacts to changes of $u$ with rate $5u^4$. But $u=3x^2-2x+1$ does not change at the same rate as $x$; it changes at rate $6x-2$. The total rate is the product of the two rates: how fast $f$ changes per unit of $u$, times how many units of $u$ appear per unit of $x$. The factor $6x-2$ is this conversion rate.

---

## Final Answer in Words

$$
f'(x)=5\left(3x^2-2x+1\right)^4(6x-2)=10(3x-1)\left(3x^2-2x+1\right)^4.
$$

The factor $6x-2$ is the derivative of the inner function and converts the rate of change with respect to $u$ into a rate with respect to $x$.

---

## Quick Verification

At $x=0$: $f'(0)=10\cdot(-1)\cdot1^4=-10$. Numerically $f(0)=1$ and $f(0.001)=(1-0.002+0.000003)^5\approx0.990055$, so the difference quotient is about $-9.94$, close to $-10$. At $x=\frac13$ the formula gives $f'=0$, and indeed the inner parabola has its vertex there.

---

## Common Mistakes

- **Forgetting the inner derivative:** $5(3x^2-2x+1)^4$ alone is wrong.
- **Differentiating the inside inside the power:** $5(6x-2)^4$ mixes up the layers.
- **Expanding the fifth power:** it is unnecessary and error-prone.

---

## Oral Explanation (3 sentences)

The function is a fifth power of the inner polynomial $3x^2-2x+1$, so the outer function is $u^5$ and the inner one is $3x^2-2x+1$. The chain rule multiplies the outer derivative $5u^4$, evaluated at the inner function, by the inner derivative $6x-2$. This extra factor appears because the inner function changes at its own rate, which must be included in the total rate of change.

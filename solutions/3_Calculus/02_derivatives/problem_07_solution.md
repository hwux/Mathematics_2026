# Problem 7 — A Trigonometric Composition

## The Problem

For

$$
f(x)=\sin(x^2+1)
$$

compute the derivative. Explicitly identify the outer function, the inner function, and the derivative of the inner function. Finally, determine the sign of $f'(0)$.

---

## What Are We Looking For?

We want to recognize $f$ as a sine of a polynomial, differentiate it with the chain rule, and evaluate the derivative at $0$.

---

## Idea and Theorem Before the Calculation

**Chain rule:** $\left(g(h(x))\right)'=g'(h(x))\,h'(x)$.

**Derivative of sine:** $(\sin u)'=\cos u$.

---

## Step-by-Step Solution

**Step 1: Layers.**

$$
\mathrm{outer:}\ g(u)=\sin u,\qquad \mathrm{inner:}\ h(x)=x^2+1.
$$

**Step 2: Derivatives of the layers.**

$$
g'(u)=\cos u,\qquad h'(x)=2x.
$$

**Step 3: Chain rule.**

$$
f'(x)=\cos(x^2+1)\cdot2x=2x\cos(x^2+1).
$$

**Step 4: Value at $0$.**

$$
f'(0)=2\cdot0\cdot\cos1=0.
$$

The derivative at $0$ is neither positive nor negative: it is zero, because the inner derivative $2x$ vanishes there.

---

## Final Answer in Words

The outer function is $\sin u$, the inner function is $x^2+1$, and its derivative is $2x$. Hence

$$
f'(x)=2x\cos(x^2+1),\qquad f'(0)=0.
$$

The tangent line at $x=0$ is horizontal. Near $0$, $\cos(x^2+1)\approx\cos1>0$, so $f'$ is negative for small $x<0$ and positive for small $x>0$: the function has a local minimum at $0$.

---

## Quick Verification

$f$ is even, since $(-x)^2+1=x^2+1$, so its derivative must be odd and vanish at $0$. Numerically $f(0)=\sin1\approx0.841471$ and $f(0.01)=\sin1.0001\approx0.841525$, a tiny increase consistent with a horizontal tangent and a minimum.

---

## Common Mistakes

- **Writing $f'(x)=\cos(x^2+1)$:** the inner derivative $2x$ is missing.
- **Writing $\cos(2x)$:** the outer derivative is evaluated at the inner function, not at its derivative.
- **Claiming $f'(0)>0$ because $\cos1>0$:** the factor $2x$ makes the product zero.

---

## Oral Explanation (3 sentences)

The function is the sine of the inner function $x^2+1$, so by the chain rule we multiply $\cos(x^2+1)$ by the inner derivative $2x$. This gives $f'(x)=2x\cos(x^2+1)$. At $x=0$ the factor $2x$ is zero, so $f'(0)=0$ and the tangent line there is horizontal.

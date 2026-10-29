# Problem 6 — Product Rule and Trigonometry

## The Problem

For

$$
f(x)=x\sin x+\cos x
$$

compute the derivative and simplify the result. Then compute $f'(0)$ and interpret the direction of the tangent line at that point.

---

## What Are We Looking For?

We want the derivative of a function that combines a product with a trigonometric term, its value at $0$, and the meaning of that value for the tangent line.

---

## Idea and Theorem Before the Calculation

**Product rule:** $(uv)'=u'v+uv'$.

**Trigonometric derivatives:**

$$
(\sin x)'=\cos x,\qquad (\cos x)'=-\sin x.
$$

**Tangent line:** If $f'(x_0)=0$, the tangent line at $x_0$ is horizontal.

---

## Step-by-Step Solution

**Step 1: Differentiate the product $x\sin x$.**

$$
(x\sin x)'=1\cdot\sin x+x\cos x.
$$

**Step 2: Differentiate $\cos x$.**

$$
(\cos x)'=-\sin x.
$$

**Step 3: Add and simplify.**

$$
f'(x)=\sin x+x\cos x-\sin x=x\cos x.
$$

*Why this is valid:* The terms $\sin x$ and $-\sin x$ cancel.

**Step 4: Value at $0$.**

$$
f'(0)=0\cdot\cos0=0.
$$

**Step 5: Tangent line.**

$f(0)=0\cdot\sin0+\cos0=1$, so the tangent at $x=0$ passes through $(0,1)$ with slope $0$:

$$
y=1.
$$

The tangent is horizontal.

---

## Final Answer in Words

$$
f'(x)=x\cos x,\qquad f'(0)=0.
$$

At $x=0$ the tangent line is horizontal, namely $y=1$. Since $f'(x)=x\cos x$ is negative just left of $0$ and positive just right of it, the function has a local minimum at $x=0$.

---

## Quick Verification

$f$ is even: $f(-x)=(-x)\sin(-x)+\cos(-x)=x\sin x+\cos x=f(x)$. The derivative of an even function is odd, and $x\cos x$ is indeed odd, so its value at $0$ must be $0$. Numerically $f(0.01)\approx1.00005$, very close to $f(0)=1$, as expected near a horizontal tangent.

---

## Common Mistakes

- **Using $(\cos x)'=\sin x$:** the derivative of cosine has a minus sign.
- **Forgetting the product rule:** $(x\sin x)'\neq\cos x$.
- **Missing the cancellation:** the unsimplified form hides the simple result $x\cos x$.

---

## Oral Explanation (3 sentences)

The product rule gives $(x\sin x)'=\sin x+x\cos x$, and the derivative of $\cos x$ is $-\sin x$, so the sines cancel and $f'(x)=x\cos x$. At $x=0$ the derivative is $0$, so the tangent line at the point $(0,1)$ is horizontal. The derivative changes sign from negative to positive there, so the graph has a local minimum at $x=0$.

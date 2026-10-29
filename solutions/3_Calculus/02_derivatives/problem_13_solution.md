# Problem 13 — A Multi-Layer Composition

## The Problem

For

$$
f(x)=e^{\sin(x^2)}
$$

compute the derivative. First write the layers

$$
x\longrightarrow x^2\longrightarrow \sin(x^2)\longrightarrow e^{\sin(x^2)}
$$

and explain why differentiation moves through them in the reverse order.

---

## What Are We Looking For?

We want the derivative of a composition of three functions, using the chain rule once per layer, and an explanation of the order of the factors.

---

## Idea and Theorem Before the Calculation

**Layers:**

$$
w=x^2,\qquad v=\sin w,\qquad f=e^{v}.
$$

**Chain rule for several layers:**

$$
\frac{df}{dx}=\frac{df}{dv}\cdot\frac{dv}{dw}\cdot\frac{dw}{dx}.
$$

---

## Step-by-Step Solution

**Step 1: Outermost layer.**

$$
\frac{df}{dv}=e^{v}=e^{\sin(x^2)}.
$$

**Step 2: Middle layer.**

$$
\frac{dv}{dw}=\cos w=\cos(x^2).
$$

**Step 3: Innermost layer.**

$$
\frac{dw}{dx}=2x.
$$

**Step 4: Multiply.**

$$
f'(x)=e^{\sin(x^2)}\cdot\cos(x^2)\cdot2x=2x\cos(x^2)\,e^{\sin(x^2)}.
$$

---

## Why the Reverse Order

When computing $f(x)$, we start with $x$ and apply $x^2$, then $\sin$, then $e^{(\cdot)}$. When differentiating, we look at the last operation first, because $f$ is directly an exponential of something: we differentiate the outer function with its inside untouched, then go one layer inward and repeat. Each layer contributes its own rate of change, evaluated at what is inside it, so the derivative peels the expression from the outside in, which is the reverse of the order of evaluation.

---

## Final Answer in Words

$$
f'(x)=2x\cos(x^2)\,e^{\sin(x^2)}.
$$

Each of the three layers contributes one factor: $e^{\sin(x^2)}$ from the exponential, $\cos(x^2)$ from the sine, and $2x$ from the square.

---

## Quick Verification

At $x=1$: $f'(1)=2\cos1\,e^{\sin1}\approx2\cdot0.5403\cdot2.3198\approx2.507$. Numerically, $\frac{f(1.001)-f(1)}{0.001}\approx2.50$. At $x=0$ the factor $2x$ gives $f'(0)=0$, consistent with $f$ being even.

---

## Common Mistakes

- **Stopping after two layers:** $\cos(x^2)e^{\sin(x^2)}$ forgets the factor $2x$.
- **Evaluating at the wrong place:** $\cos(x^2)$ is correct, $\cos x$ or $\cos(2x)$ is not.
- **Changing the exponent:** the derivative of $e^v$ is $e^v$ with the same $v=\sin(x^2)$.

---

## Oral Explanation (3 sentences)

The function is built in three layers: square, then sine, then exponential. The chain rule differentiates from the outside in, giving $e^{\sin(x^2)}$, then $\cos(x^2)$, then $2x$, each evaluated at what is inside it. Multiplying the three factors gives $f'(x)=2x\cos(x^2)e^{\sin(x^2)}$.

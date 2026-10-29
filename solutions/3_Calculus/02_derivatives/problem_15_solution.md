# Problem 15 — The Difference Quotient as a Check of the Derivative

## The Problem

Choose one function from the problem set and a point $x_0$ at which the derivative exists. Compute $f'(x_0)$ exactly, and then calculate

$$
\frac{f(x_0+h)-f(x_0)}h
$$

for $h=1$, $0.1$, and $0.01$. Compare the values with $f'(x_0)$ and explain why the difference quotient approaching a single number is consistent with the definition of the derivative, while a few computations do not replace a limit argument.

---

## What Are We Looking For?

We want to check an exactly computed derivative against difference quotients for decreasing $h$, and to explain what this numerical check can and cannot show.

---

## Idea and Theorem Before the Calculation

**Choice:** the function from Problem 10,

$$
f(x)=x^2-3x+1,\qquad x_0=2.
$$

From Problem 10, $f'(x)=2x-3$ and $f'(2)=1$, $f(2)=-1$.

**Definition:**

$$
f'(x_0)=\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}.
$$

---

## Step-by-Step Solution

**Step 1: Exact derivative.**

$$
f'(2)=2\cdot2-3=1.
$$

**Step 2: The difference quotient in general.**

$$
f(2+h)=(2+h)^2-3(2+h)+1=4+4h+h^2-6-3h+1=-1+h+h^2,
$$

so

$$
\frac{f(2+h)-f(2)}{h}=\frac{h+h^2}{h}=1+h\qquad(h\neq0).
$$

**Step 3: The three values.**

| $h$ | $f(2+h)$ | quotient | difference from $f'(2)$ |
|---|---|---|---|
| $1$ | $1$ | $2$ | $1$ |
| $0.1$ | $-0.89$ | $1.1$ | $0.1$ |
| $0.01$ | $-0.9899$ | $1.01$ | $0.01$ |

**Step 4: Comparison.**

The quotients $2$, $1.1$, $1.01$ approach $1=f'(2)$, and the error equals $h$ exactly, so it shrinks by a factor $10$ each time.

---

## What the Check Shows and What It Does Not

The quotients are slopes of secant lines through $(2,-1)$ and $(2+h,f(2+h))$. Their approach to $1$ agrees with the definition, which says that these secant slopes tend to the tangent slope. However, three values cannot prove a limit: the definition is about all $h$ near $0$, and a function could behave differently for values of $h$ that were not tested. For example, adding the term $(x-2)\sin\frac{\pi}{x-2}$ to $f$ (with value $0$ at $x=2$) changes the quotient to $1+h+\sin\frac{\pi}{h}$; for $h=1$, $0.1$, $0.01$ the sine is $\sin\pi=\sin10\pi=\sin100\pi=0$, so the table is identical, yet this new quotient has no limit as $h\to0$. Rounding errors on a computer for very small $h$ are a second reason not to rely on numbers alone. In this example the proof is the algebraic formula $1+h$ from Step 2, which is valid for every $h\neq0$ and clearly tends to $1$.

---

## Final Answer in Words

For $f(x)=x^2-3x+1$ at $x_0=2$, the exact derivative is $f'(2)=1$, and the difference quotients for $h=1$, $0.1$, $0.01$ are $2$, $1.1$, $1.01$. They approach $1$ as $h$ decreases, consistent with the definition of the derivative, but only the general formula $\frac{f(2+h)-f(2)}{h}=1+h$ proves the limit.

---

## Quick Verification

With negative steps the quotient is also $1+h$: for $h=-0.01$ it equals $0.99$. So the secant slopes approach $1$ from both sides, as they must for a differentiable function.

---

## Common Mistakes

- **Dividing by $h$ incorrectly:** the quotient is $\frac{f(x_0+h)-f(x_0)}{h}$, not $f(x_0+h)-f(x_0)$.
- **Using only $h=1$:** a large step gives a poor approximation.
- **Treating numbers as a proof:** they illustrate the limit, the formula proves it.

---

## Oral Explanation (3 sentences)

For $f(x)=x^2-3x+1$ at $x_0=2$ the derivative is $1$, and the difference quotients for $h=1$, $0.1$ and $0.01$ are $2$, $1.1$ and $1.01$. These are slopes of secant lines, and they approach the slope of the tangent, just as the definition of the derivative says. A few numbers are only evidence, while the exact formula $1+h$ for the quotient proves that the limit is $1$.

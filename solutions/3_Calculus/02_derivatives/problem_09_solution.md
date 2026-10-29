# Problem 9 — A Logarithm and the Chain Rule

## The Problem

For

$$
f(x)=\ln(x^2+1)
$$

compute the derivative. Then determine the sign of $f'(x)$ for $x<0$, $x=0$, and $x>0$, and describe qualitatively how the function behaves around zero.

---

## What Are We Looking For?

We want the derivative of a logarithm of a polynomial, its sign on both sides of $0$, and the resulting shape of the graph.

---

## Idea and Theorem Before the Calculation

**Derivative of the logarithm:** $(\ln u)'=\frac{1}{u}$ for $u>0$; with the chain rule,

$$
\left(\ln h(x)\right)'=\frac{h'(x)}{h(x)}.
$$

**Sign of the derivative:** $f'>0$ on an interval means $f$ is increasing there, $f'<0$ means decreasing.

**Domain:** $x^2+1\ge1>0$ for every real $x$, so $f$ is defined on $\mathbb{R}$.

---

## Step-by-Step Solution

**Step 1: Derivative.**

The inner function is $h(x)=x^2+1$ with $h'(x)=2x$:

$$
f'(x)=\frac{2x}{x^2+1}.
$$

**Step 2: Sign.**

The denominator $x^2+1$ is always positive, so the sign of $f'$ is the sign of $2x$:

| $x$ | $x<0$ | $x=0$ | $x>0$ |
|---|---|---|---|
| $f'(x)$ | negative | $0$ | positive |

**Step 3: Behavior.**

$f$ is decreasing on $(-\infty,0]$ and increasing on $[0,\infty)$, so it has a minimum at $x=0$:

$$
f(0)=\ln1=0.
$$

Since $x^2+1\ge1$, we have $f(x)\ge0$ everywhere, so this minimum is global.

---

## Final Answer in Words

$$
f'(x)=\frac{2x}{x^2+1}.
$$

The derivative is negative for $x<0$, zero at $x=0$, and positive for $x>0$. The function decreases up to $0$, reaches its smallest value $f(0)=0$ with a horizontal tangent, and then increases; its graph is symmetric about the $y$-axis.

---

## Quick Verification

$f$ is even, so its derivative is odd, and $\frac{2x}{x^2+1}$ is indeed odd. Numerically, $f(1)=\ln2\approx0.693$ and $f(-1)=\ln2$, both above $f(0)=0$, consistent with a minimum at $0$. At $x=1$, $f'(1)=1$, and $\frac{f(1.001)-f(1)}{0.001}\approx1.0000$.

---

## Common Mistakes

- **$f'(x)=\frac{1}{x^2+1}$:** the inner derivative $2x$ is missing.
- **Restricting the domain to $x>0$:** the argument of the logarithm is $x^2+1$, which is always positive.
- **Concluding "maximum at $0$":** the sign changes from $-$ to $+$, which means a minimum.

---

## Oral Explanation (3 sentences)

By the chain rule, the derivative of $\ln(x^2+1)$ is the derivative of the inside divided by the inside, namely $\frac{2x}{x^2+1}$. Because the denominator is always positive, the derivative is negative for $x<0$, zero at $0$, and positive for $x>0$. So the function decreases, reaches its minimum value $0$ at $x=0$, and then increases symmetrically.

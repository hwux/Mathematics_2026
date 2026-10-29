# Problem 2 — Powers, Roots, and the Domain

## The Problem

For

$$
f(x)=2\sqrt{x}-\frac{3}{x^2}+x^{3/2}
$$

1. rewrite the function using powers,
2. determine the domain,
3. compute the derivative,
4. compare the domain of the function with the domain of its derivative.

---

## What Are We Looking For?

We want to write every term as a power of $x$, find where the function is defined, differentiate with the power rule, and check where the derivative is defined.

---

## Idea and Theorem Before the Calculation

**Rewriting:** $\sqrt{x}=x^{1/2}$ and $\frac{1}{x^2}=x^{-2}$.

**Power rule for real exponents:** $(x^r)'=rx^{r-1}$ for every real $r$, valid for $x>0$ (and for other $x$ where the power makes sense).

**Domain:** a square root needs a nonnegative argument, and a denominator must not vanish.

---

## Step-by-Step Solution

**Step 1: Powers.**

$$
f(x)=2x^{1/2}-3x^{-2}+x^{3/2}.
$$

**Step 2: Domain.**

- $\sqrt{x}$ and $x^{3/2}=x\sqrt{x}$ need $x\ge0$,
- $\frac{3}{x^2}$ needs $x\neq0$.

Together:

$$
D_f=(0,\infty).
$$

**Step 3: Derivative.**

$$
f'(x)=2\cdot\frac12x^{-1/2}-3\cdot(-2)x^{-3}+\frac32x^{1/2}=x^{-1/2}+6x^{-3}+\frac32x^{1/2}.
$$

In root form:

$$
f'(x)=\frac{1}{\sqrt{x}}+\frac{6}{x^3}+\frac{3}{2}\sqrt{x}.
$$

**Step 4: Domain of the derivative.**

$\frac{1}{\sqrt{x}}$ needs $x>0$, $\frac{6}{x^3}$ needs $x\neq0$, and $\sqrt{x}$ needs $x\ge0$. Hence

$$
D_{f'}=(0,\infty)=D_f.
$$

---

## Comparison of the Domains

Here the two domains coincide, because the term $\frac{3}{x^2}$ already excludes $0$ from the domain of $f$. This is not automatic: without that term, $g(x)=2\sqrt{x}+x^{3/2}$ would be defined on $[0,\infty)$, but $g'(x)=\frac{1}{\sqrt x}+\frac32\sqrt x$ only on $(0,\infty)$. Differentiation can shrink the domain, because a root has a vertical tangent at $0$.

---

## Final Answer in Words

$$
f(x)=2x^{1/2}-3x^{-2}+x^{3/2},\qquad D_f=(0,\infty),
$$

$$
f'(x)=x^{-1/2}+6x^{-3}+\frac32x^{1/2},\qquad D_{f'}=(0,\infty).
$$

The function and its derivative have the same domain here; in general a derivative can have a smaller domain than the function.

---

## Quick Verification

At $x=1$: $f'(1)=1+6+1.5=8.5$. Numerically, $f(1)=2-3+1=0$ and $f(1.001)\approx0.0085$, so the difference quotient is about $8.5$. Also every term of $f'$ is positive, so $f$ is increasing on its whole domain.

---

## Common Mistakes

- **Writing $\frac{3}{x^2}=3x^2$ or $3x^{-1/2}$:** the correct power is $x^{-2}$.
- **Sign error in $(-3x^{-2})'$:** $-3\cdot(-2)=+6$.
- **Taking $[0,\infty)$ as the domain:** $x=0$ is excluded by the term $\frac{3}{x^2}$.

---

## Oral Explanation (3 sentences)

After rewriting the roots and the fraction as powers, the function is $2x^{1/2}-3x^{-2}+x^{3/2}$, and each term can be differentiated with the power rule. The domain is $(0,\infty)$, because the roots need $x\ge0$ and the fraction needs $x\neq0$. The derivative $x^{-1/2}+6x^{-3}+\frac32x^{1/2}$ has the same domain here, although in general differentiating a root can remove the endpoint $0$.

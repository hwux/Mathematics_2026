# Problem 8 — Two Exponential Functions

## The Problem

For

$$
f(x)=e^{2x-3}+5^x
$$

compute the derivative. Explain why the factor $2$ appears in the first term and why $\ln5$ appears in the second.

---

## What Are We Looking For?

We want the derivative of a sum of two exponential terms, and an explanation of two different sources of extra factors.

---

## Idea and Theorem Before the Calculation

**Natural exponential:** $(e^x)'=e^x$, and by the chain rule $(e^{h(x)})'=e^{h(x)}h'(x)$.

**Other bases:** For $a>0$,

$$
a^x=e^{x\ln a}\quad\Longrightarrow\quad(a^x)'=a^x\ln a.
$$

---

## Step-by-Step Solution

**Step 1: First term.**

The inner function is $h(x)=2x-3$ with $h'(x)=2$, so

$$
\left(e^{2x-3}\right)'=e^{2x-3}\cdot2=2e^{2x-3}.
$$

**Step 2: Second term.**

Write $5^x=e^{x\ln5}$. The inner function is $x\ln5$ with derivative $\ln5$, so

$$
\left(5^x\right)'=e^{x\ln5}\cdot\ln5=5^x\ln5.
$$

**Step 3: Sum.**

$$
f'(x)=2e^{2x-3}+5^x\ln5.
$$

---

## Where the Factors Come From

- **The $2$:** the base is $e$, but the exponent is not $x$; it is $2x-3$, which grows twice as fast as $x$. The chain rule multiplies by the derivative of the exponent, $2$.
- **The $\ln5$:** the exponent is simply $x$, but the base is not $e$. Rewriting the base as $5=e^{\ln5}$ turns the change of base into a hidden inner function $x\ln5$, whose derivative is $\ln5$.

Both factors come from the chain rule, but for different reasons: one from the exponent, the other from the base.

---

## Final Answer in Words

$$
f'(x)=2e^{2x-3}+5^x\ln5.
$$

The factor $2$ is the derivative of the exponent $2x-3$, and the factor $\ln5$ appears because $5^x=e^{x\ln5}$.

---

## Quick Verification

At $x=0$: $f'(0)=2e^{-3}+\ln5\approx0.0996+1.6094=1.7090$. Numerically, $f(0)=e^{-3}+1\approx1.049787$ and $f(0.001)\approx1.051497$, giving a difference quotient of about $1.710$.

---

## Common Mistakes

- **$(5^x)'=x\cdot5^{x-1}$:** the power rule applies to $x^n$, not to $a^x$.
- **$(5^x)'=5^x$:** this holds only for the base $e$.
- **$(e^{2x-3})'=e^{2x-3}$:** the derivative of the exponent is missing.

---

## Oral Explanation (3 sentences)

The first term has base $e$ and exponent $2x-3$, so the chain rule multiplies $e^{2x-3}$ by the derivative of the exponent, which is $2$. The second term has exponent $x$ but base $5$, and writing $5^x=e^{x\ln5}$ shows that its derivative is $5^x\ln5$. Together $f'(x)=2e^{2x-3}+5^x\ln5$.

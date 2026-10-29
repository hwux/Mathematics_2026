# Problem 11 — Choose the Method First

## The Problem

For each integral, first write which method you choose and how you recognize it, and then compute:

1. $\int\sin(3x)\,dx$,
2. $\int x\ln x\,dx$,
3. $\int\frac{x}{\sqrt{x^2+1}}\,dx$.

---

## What Are We Looking For?

For three different integrals we want to decide the method from the structure of the integrand, carry it out, and check the result.

---

## Idea and Theorem Before the Calculation

**Linear substitution:** $\int g(ax+b)\,dx=\frac1aG(ax+b)+C$ where $G'=g$.

**Integration by parts:** $\int uv'\,dx=uv-\int u'v\,dx$, used for products where one factor simplifies when differentiated.

**Substitution:** used when the derivative of an inner expression appears as a factor.

---

## Step-by-Step Solution

**Integral 1: $\int\sin(3x)\,dx$.**

*Method:* linear substitution, because the argument of the sine is the linear expression $3x$.

With $u=3x$, $du=3\,dx$, so $dx=\frac13du$:

$$
\int\sin(3x)\,dx=\frac13\int\sin u\,du=-\frac13\cos(3x)+C.
$$

Check: $\left(-\frac13\cos3x\right)'=-\frac13\cdot(-\sin3x)\cdot3=\sin3x$.

**Integral 2: $\int x\ln x\,dx$ (for $x>0$).**

*Method:* integration by parts, because it is a product, $\ln x$ simplifies when differentiated ($\frac1x$), and $x$ is easy to integrate.

$$
u=\ln x,\quad v'=x\qquad\Longrightarrow\qquad u'=\frac1x,\quad v=\frac{x^2}{2}.
$$

$$
\int x\ln x\,dx=\frac{x^2}{2}\ln x-\int\frac{x^2}{2}\cdot\frac1x\,dx=\frac{x^2}{2}\ln x-\frac{x^2}{4}+C.
$$

Check: $\left(\frac{x^2}{2}\ln x-\frac{x^2}{4}\right)'=x\ln x+\frac{x}{2}-\frac{x}{2}=x\ln x$.

**Integral 3: $\int\frac{x}{\sqrt{x^2+1}}\,dx$.**

*Method:* substitution, because the numerator $x$ is (half of) the derivative of the expression $x^2+1$ under the root.

With $u=x^2+1$, $du=2x\,dx$, so $x\,dx=\frac12du$:

$$
\int\frac{x}{\sqrt{x^2+1}}\,dx=\frac12\int u^{-1/2}\,du=\frac12\cdot2u^{1/2}+C=\sqrt{x^2+1}+C.
$$

Check: $\left(\sqrt{x^2+1}\right)'=\frac{2x}{2\sqrt{x^2+1}}=\frac{x}{\sqrt{x^2+1}}$.

---

## Final Answer in Words

| integral | method | result |
|---|---|---|
| $\int\sin(3x)\,dx$ | linear substitution | $-\frac13\cos(3x)+C$ |
| $\int x\ln x\,dx$ | integration by parts with $u=\ln x$ | $\frac{x^2}{2}\ln x-\frac{x^2}{4}+C$ |
| $\int\frac{x}{\sqrt{x^2+1}}\,dx$ | substitution $u=x^2+1$ | $\sqrt{x^2+1}+C$ |

Each result was confirmed by differentiation.

---

## Quick Verification

Definite checks: $\int_0^{\pi/3}\sin3x\,dx=-\frac13(\cos\pi-\cos0)=\frac23$; $\int_1^e x\ln x\,dx=\frac{e^2}{2}-\frac{e^2}{4}+\frac14=\frac{e^2+1}{4}\approx2.10$; $\int_0^1\frac{x}{\sqrt{x^2+1}}\,dx=\sqrt2-1\approx0.414$. All are positive, as the integrands are positive on these intervals.

---

## Common Mistakes

- **$\int\sin3x\,dx=-\cos3x$:** the factor $\frac13$ is missing.
- **Choosing $u=x$, $v'=\ln x$ in $\int x\ln x\,dx$:** then $v=x\ln x-x$ must be found first, and the new integral $\int(x\ln x-x)\,dx$ contains the original one again, so the method goes in a circle.
- **Integrating $\frac{x}{\sqrt{x^2+1}}$ by parts:** substitution is much shorter.

---

## Oral Explanation (3 sentences)

The sine has a linear argument, so a linear substitution gives $-\frac13\cos3x+C$. The product $x\ln x$ calls for integration by parts with $u=\ln x$, because the logarithm becomes simpler after differentiation, giving $\frac{x^2}{2}\ln x-\frac{x^2}{4}+C$. In the third integral the numerator is half of the derivative of $x^2+1$, so the substitution $u=x^2+1$ gives $\sqrt{x^2+1}+C$.

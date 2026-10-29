# Problem 8 — Choosing the Factors in Integration by Parts

## The Problem

Compute

$$
\int x\cos x\,dx.
$$

Before calculating, justify why it is convenient to differentiate $x$ and integrate $\cos x$, rather than the other way around.

---

## What Are We Looking For?

We want an antiderivative of $x\cos x$ by parts, together with a justification of the choice of $u$ and $v'$.

---

## Idea and Theorem Before the Calculation

**Integration by parts:**

$$
\int uv'\,dx=uv-\int u'v\,dx.
$$

**Choice principle:** take as $u$ the factor that becomes simpler when differentiated, and as $v'$ the factor that does not become harder when integrated.

---

## Step-by-Step Solution

**Step 1: Compare the two choices.**

- $u=x$, $v'=\cos x$: then $u'=1$ and $v=\sin x$, and the new integral is $\int\sin x\,dx$, which is elementary.
- $u=\cos x$, $v'=x$: then $u'=-\sin x$ and $v=\frac{x^2}{2}$, and the new integral is $\int\frac{x^2}{2}\sin x\,dx$, with a higher power of $x$, so it is harder than the original.

The first choice is the right one: differentiating $x$ removes it, while integrating $\cos x$ only turns it into $\sin x$.

**Step 2: Apply the formula.**

$$
\int x\cos x\,dx=x\sin x-\int\sin x\,dx=x\sin x+\cos x+C.
$$

**Step 3: Verify.**

$$
\left(x\sin x+\cos x\right)'=\sin x+x\cos x-\sin x=x\cos x.
$$

---

## Final Answer in Words

$$
\int x\cos x\,dx=x\sin x+\cos x+C.
$$

Differentiating $x$ reduces it to $1$, while integrating $\cos x$ gives $\sin x$, so the remaining integral is simple; the opposite choice would raise the power of $x$.

---

## Quick Verification

This is the reverse of Derivatives Problem 6, where $(x\sin x+\cos x)'=x\cos x$ was computed. Definite check: $\int_0^{\pi/2}x\cos x\,dx=\left(\frac{\pi}{2}\cdot1+0\right)-(0+1)=\frac{\pi}{2}-1\approx0.571$, positive as expected since $x\cos x\ge0$ on this interval.

---

## Common Mistakes

- **$\int\sin x\,dx=\cos x$:** the correct value is $-\cos x$, so $-\int\sin x\,dx=+\cos x$.
- **Choosing $u=\cos x$:** the new integral becomes harder.
- **Stopping after one product rule check without simplifying:** the terms $\sin x$ and $-\sin x$ must cancel.

---

## Oral Explanation (3 sentences)

In integration by parts we differentiate one factor and integrate the other, so we choose $u=x$, which becomes $1$, and $v'=\cos x$, which becomes $\sin x$. The formula gives $x\sin x-\int\sin x\,dx=x\sin x+\cos x+C$. The opposite choice would produce $\int\frac{x^2}{2}\sin x\,dx$, which is more complicated than the original integral.

# Problem 3 — Recognizing Basic Antiderivatives

## The Problem

Compute

$$
\int\left(2e^x+3\cos x-4\sin x\right)\,dx.
$$

Match each term with a known derivative and verify the entire result with one differentiation.

---

## What Are We Looking For?

We want an antiderivative of a combination of basic functions, found by reading the derivative table backwards.

---

## Idea and Theorem Before the Calculation

**Known derivatives read backwards:**

| derivative | function |
|---|---|
| $(e^x)'=e^x$ | $\int e^x\,dx=e^x+C$ |
| $(\sin x)'=\cos x$ | $\int\cos x\,dx=\sin x+C$ |
| $(\cos x)'=-\sin x$ | $\int\sin x\,dx=-\cos x+C$ |

**Linearity** allows integrating term by term and keeping constant factors.

---

## Step-by-Step Solution

**Step 1: First term.** $e^x$ is its own derivative, so

$$
\int2e^x\,dx=2e^x.
$$

**Step 2: Second term.** $\cos x$ is the derivative of $\sin x$, so

$$
\int3\cos x\,dx=3\sin x.
$$

**Step 3: Third term.** $-\sin x$ is the derivative of $\cos x$, so

$$
\int(-4\sin x)\,dx=4\int(-\sin x)\,dx=4\cos x.
$$

**Step 4: Combine.**

$$
\int\left(2e^x+3\cos x-4\sin x\right)dx=2e^x+3\sin x+4\cos x+C.
$$

**Step 5: One differentiation.**

$$
\left(2e^x+3\sin x+4\cos x+C\right)'=2e^x+3\cos x-4\sin x.
$$

---

## Final Answer in Words

$$
\int\left(2e^x+3\cos x-4\sin x\right)dx=2e^x+3\sin x+4\cos x+C.
$$

Each term was recognized as a known derivative: $e^x$ of itself, $\cos x$ of $\sin x$, and $-\sin x$ of $\cos x$.

---

## Quick Verification

Definite check on $\left[0,\frac{\pi}{2}\right]$. The antiderivative gives

$$
\left(2e^{\pi/2}+3\sin\tfrac{\pi}{2}+4\cos\tfrac{\pi}{2}\right)-\left(2e^0+3\sin0+4\cos0\right)=2e^{\pi/2}-3\approx6.621.
$$

Simpson's rule with the three points $0,\frac{\pi}{4},\frac{\pi}{2}$, where the integrand equals about $5$, $3.679$ and $5.621$, gives

$$
\frac{\pi/4}{3}\left(5+4\cdot3.679+5.621\right)\approx6.634,
$$

which agrees to two significant digits.

---

## Common Mistakes

- **$\int\sin x\,dx=\cos x$:** the correct antiderivative is $-\cos x$, so $\int(-4\sin x)\,dx=+4\cos x$.
- **$\int\cos x\,dx=-\sin x$:** the sign is positive.
- **Losing the constant factors:** $2$, $3$ and $-4$ stay in front.

---

## Oral Explanation (3 sentences)

Each term of the integrand is a known derivative: $e^x$ comes from $e^x$, $\cos x$ from $\sin x$, and $-\sin x$ from $\cos x$. Keeping the constant factors, the antiderivative is $2e^x+3\sin x+4\cos x+C$. One differentiation returns $2e^x+3\cos x-4\sin x$, which confirms the result, including the sign of the cosine term.

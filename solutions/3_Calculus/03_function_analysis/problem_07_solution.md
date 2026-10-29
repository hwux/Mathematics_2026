# Problem 7 — A Trigonometric Function

## The Problem

On $[0,2\pi]$, find the intervals of monotonicity and the extrema of

$$
f(x)=\sin x+\cos x.
$$

Include the endpoints of the interval and compare the function values at the critical points and at the endpoints.

---

## What Are We Looking For?

We want the intervals of increase and decrease of $\sin x+\cos x$ on one period, all local extrema including those at the endpoints, and the global maximum and minimum.

---

## Idea and Theorem Before the Calculation

**Extreme value theorem:** A continuous function on a closed interval attains a global maximum and minimum, either at a critical point or at an endpoint.

**Derivatives:** $(\sin x)'=\cos x$, $(\cos x)'=-\sin x$.

---

## Step-by-Step Solution

**Step 1: Derivative and critical points.**

$$
f'(x)=\cos x-\sin x=0\iff\tan x=1\quad(\cos x\neq0).
$$

On $[0,2\pi]$: $x=\frac{\pi}{4}$ and $x=\frac{5\pi}{4}$. (Where $\cos x=0$, $\sin x=\pm1$, so $f'\neq0$.)

**Step 2: Sign chart.**

| interval | $\left(0,\frac{\pi}{4}\right)$ | $\left(\frac{\pi}{4},\frac{5\pi}{4}\right)$ | $\left(\frac{5\pi}{4},2\pi\right)$ |
|---|---|---|---|
| test point | $0$ | $\frac{\pi}{2}$ | $\frac{3\pi}{2}$ |
| $f'$ | $1>0$ | $-1<0$ | $1>0$ |
| $f$ | increasing | decreasing | increasing |

**Step 3: Values.**

| $x$ | $0$ | $\frac{\pi}{4}$ | $\frac{5\pi}{4}$ | $2\pi$ |
|---|---|---|---|---|
| $f(x)$ | $1$ | $\sqrt2$ | $-\sqrt2$ | $1$ |

Here $f\left(\frac{\pi}{4}\right)=\frac{\sqrt2}{2}+\frac{\sqrt2}{2}=\sqrt2$ and $f\left(\frac{5\pi}{4}\right)=-\frac{\sqrt2}{2}-\frac{\sqrt2}{2}=-\sqrt2$.

**Step 4: Classification.**

- $x=\frac{\pi}{4}$: local and global maximum $\sqrt2$.
- $x=\frac{5\pi}{4}$: local and global minimum $-\sqrt2$.
- $x=0$: endpoint local minimum $1$ (the function increases to the right of it).
- $x=2\pi$: endpoint local maximum $1$ (the function increases up to it).

---

## Final Answer in Words

On $[0,2\pi]$, $f$ is increasing on $\left[0,\frac{\pi}{4}\right]$, decreasing on $\left[\frac{\pi}{4},\frac{5\pi}{4}\right]$, and increasing on $\left[\frac{5\pi}{4},2\pi\right]$. The global maximum is $\sqrt2$ at $\frac{\pi}{4}$ and the global minimum is $-\sqrt2$ at $\frac{5\pi}{4}$. The endpoints both have value $1$, which lies between these, so they are only local (one-sided) extrema.

---

## Quick Verification

Using $\sin x+\cos x=\sqrt2\sin\left(x+\frac{\pi}{4}\right)$: the sine takes its maximum $1$ when $x+\frac{\pi}{4}=\frac{\pi}{2}$, i.e. $x=\frac{\pi}{4}$, and its minimum $-1$ when $x+\frac{\pi}{4}=\frac{3\pi}{2}$, i.e. $x=\frac{5\pi}{4}$. This gives exactly $\pm\sqrt2$ at the same points.

---

## Common Mistakes

- **Forgetting the endpoints:** on a closed interval they must be compared with the critical points.
- **Taking $\tan x=1$ only at $\frac{\pi}{4}$:** the tangent has period $\pi$, so $\frac{5\pi}{4}$ is also a solution.
- **Answering $f_{\max}=2$:** $\sin x$ and $\cos x$ are not both equal to $1$ at the same point.

---

## Oral Explanation (3 sentences)

The derivative $\cos x-\sin x$ vanishes where $\tan x=1$, which on $[0,2\pi]$ happens at $\frac{\pi}{4}$ and $\frac{5\pi}{4}$. The function increases to $\sqrt2$ at $\frac{\pi}{4}$, decreases to $-\sqrt2$ at $\frac{5\pi}{4}$, and increases again, while both endpoints have the value $1$. Comparing all these values, the global maximum is $\sqrt2$ and the global minimum is $-\sqrt2$, confirmed by writing $f$ as $\sqrt2\sin(x+\frac{\pi}{4})$.

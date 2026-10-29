# Problem 11 — A Parameter and the Number of Extrema

## The Problem

For

$$
f_a(x)=x^3-3ax
$$

depending on $a$, determine the number of critical points and their character. Separate the parameter cases and justify why the structure of the graph changes.

---

## What Are We Looking For?

We want to know, for every real $a$, how many critical points $f_a$ has, whether they are maxima, minima or neither, and why the shape of the graph changes with $a$.

---

## Idea and Theorem Before the Calculation

**Critical points:** solutions of $f_a'(x)=0$.

**First derivative test:** a sign change of $f'$ from $+$ to $-$ gives a maximum, from $-$ to $+$ a minimum, no sign change gives no extremum.

**Key fact:** $f_a'(x)=3x^2-3a$ is a parabola whose number of zeros depends on the sign of $a$.

---

## Step-by-Step Solution

**Step 1: Derivative.**

$$
f_a'(x)=3x^2-3a=3(x^2-a).
$$

**Case 1: $a>0$.**

$x^2=a$ has two solutions, $x=\pm\sqrt a$, and

$$
f_a'(x)=3(x-\sqrt a)(x+\sqrt a).
$$

The sign is $+$ for $x<-\sqrt a$, $-$ between the roots, $+$ for $x>\sqrt a$. Hence:

- local maximum at $x=-\sqrt a$: $f_a(-\sqrt a)=-a\sqrt a+3a\sqrt a=2a^{3/2}$,
- local minimum at $x=\sqrt a$: $f_a(\sqrt a)=a\sqrt a-3a\sqrt a=-2a^{3/2}$.

Two critical points, both extrema.

**Case 2: $a=0$.**

$f_0(x)=x^3$ and $f_0'(x)=3x^2$, which is zero only at $x=0$ and positive elsewhere. The derivative does not change sign, so $x=0$ is a critical point but **not** an extremum; the graph has a horizontal tangent at an inflection point.

One critical point, no extremum.

**Case 3: $a<0$.**

$x^2-a=x^2+|a|>0$ for every $x$, so $f_a'(x)>0$ everywhere. There are no critical points, and $f_a$ is strictly increasing on $\mathbb{R}$.

No critical points, no extrema.

---

## Why the Structure Changes

The derivative is an upward parabola $3x^2-3a$ shifted down by $3a$. For $a>0$ it dips below the axis, creating an interval where $f_a$ decreases, between a "hill" and a "valley". As $a$ decreases to $0$, the two critical points $\pm\sqrt a$ move towards each other and merge at $0$, and the hill and valley flatten into a single horizontal inflection. For $a<0$ the parabola $f_a'$ stays entirely above the axis, so the function is monotone and the graph has no turns at all.

---

## Final Answer in Words

| parameter | critical points | character |
|---|---|---|
| $a>0$ | $x=\pm\sqrt a$ | maximum $2a^{3/2}$ at $-\sqrt a$, minimum $-2a^{3/2}$ at $\sqrt a$ |
| $a=0$ | $x=0$ | no extremum (horizontal inflection) |
| $a<0$ | none | strictly increasing |

The graph changes structure at $a=0$, where the two extrema merge and disappear.

---

## Quick Verification

For $a=1$: $f_1(x)=x^3-3x$, with maximum $f_1(-1)=2$ and minimum $f_1(1)=-2$, which matches $\pm2a^{3/2}=\pm2$ (and Problem 15). For $a=-1$: $f'(x)=3x^2+3\ge3>0$, so the function is increasing.

---

## Common Mistakes

- **Treating $a=0$ as a case with an extremum:** $f'(0)=0$ does not imply an extremum.
- **Writing $\sqrt a$ for $a<0$:** there are no real critical points then.
- **Forgetting that $f_a$ is odd:** the maximum and minimum values must be opposite numbers.

---

## Oral Explanation (3 sentences)

The derivative $3(x^2-a)$ has two zeros when $a>0$, one when $a=0$, and none when $a<0$. For $a>0$ the function has a maximum at $-\sqrt a$ and a minimum at $\sqrt a$; for $a=0$ it is $x^3$, with a flat inflection but no extremum; for $a<0$ it is strictly increasing. As $a$ decreases through zero, the hill and the valley of the graph merge and vanish, which is why the shape changes qualitatively.

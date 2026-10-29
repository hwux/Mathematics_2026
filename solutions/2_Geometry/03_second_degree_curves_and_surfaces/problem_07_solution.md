# Exercise 7 — Classifying a Second-Degree Equation

## The Problem

Determine the type of object described by:

1. $4x^2+9y^2=36$,
2. $x^2-y^2=1$,
3. $x^2-4y=0$,
4. $x^2+y^2+1=0$.

In the last case, explain why there are no real points.

---

## What Are We Looking For?

We want to recognize each curve quickly from its structure and, where needed, rewrite it in canonical form. For the last equation we must show that no real point satisfies it.

---

## Idea and Theorem Before the Calculation

**Quick recognition:**

- two squares, same sign, positive right side: ellipse (circle if the coefficients are equal);
- two squares, opposite signs: hyperbola;
- one square and one linear term: parabola;
- a sum of squares equal to a negative number: no real points.

---

## Step-by-Step Solution

**Equation 1: $4x^2+9y^2=36$.**

Divide by $36$:

$$
\frac{x^2}{9}+\frac{y^2}{4}=1.
$$

This is an **ellipse** with center $(0,0)$ and semiaxes $3$ (along $x$) and $2$ (along $y$).

**Equation 2: $x^2-y^2=1$.**

Two squares with opposite signs: a **hyperbola** with $a=b=1$, vertices $(\pm1,0)$ and asymptotes $y=\pm x$. Because $a=b$, the asymptotes are perpendicular; such a hyperbola is called rectangular.

**Equation 3: $x^2-4y=0$.**

Only $x$ is squared:

$$
y=\frac{x^2}{4}.
$$

This is a **parabola** with vertex $(0,0)$, axis of symmetry the $y$-axis, opening upward.

**Equation 4: $x^2+y^2+1=0$.**

For real numbers $x^2\ge0$ and $y^2\ge0$, so

$$
x^2+y^2+1\ge1>0.
$$

The left side can never be $0$. The equation has **no real points**; it describes the empty set.

*Why this is valid:* The square of a real number is never negative, so adding $1$ makes the left side strictly positive for every real $(x,y)$.

---

## Final Answer in Words

1. Ellipse $\frac{x^2}{9}+\frac{y^2}{4}=1$ with semiaxes $3$ and $2$.
2. Hyperbola with vertices $(\pm1,0)$ and asymptotes $y=\pm x$.
3. Parabola $y=\frac{x^2}{4}$ with vertex at the origin, opening upward.
4. No real points: the left side is always at least $1$, so it can never equal $0$.

---

## Quick Verification

One point for each of the first three curves:

$$
\begin{aligned}
(3,0)&:\quad 4\cdot9+0=36, \\
(1,0)&:\quad 1-0=1, \\
(2,1)&:\quad 4-4\cdot1=0.
\end{aligned}
$$

For the fourth equation, even the "best" candidate $(0,0)$, where the squares are smallest, gives $0+0+1=1\neq0$.

---

## Common Mistakes

- **Calling equation 4 a circle with radius $\sqrt{-1}$:** a negative right side in $x^2+y^2=-1$ means there are no real points, not an imaginary circle in the plane.
- **Classifying equation 3 as a hyperbola because of the minus sign:** the minus sign is in front of a linear term, not a square.
- **Forgetting to divide by $36$ in equation 1:** without dividing, the semiaxes cannot be read off correctly.

---

## Oral Explanation (3 sentences)

The first equation becomes $\frac{x^2}{9}+\frac{y^2}{4}=1$ after dividing by $36$, so it is an ellipse, while $x^2-y^2=1$ has squares with opposite signs and is a hyperbola. The equation $x^2-4y=0$ contains only one square and can be written as $y=\frac{x^2}{4}$, an upward parabola. The last equation has no real points, because $x^2+y^2+1$ is a sum of nonnegative squares plus $1$, so it is always at least $1$.

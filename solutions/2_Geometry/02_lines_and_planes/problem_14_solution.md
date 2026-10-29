# Exercise 14 — Contrast: Intersection and Parallelism

## The Problem

From the point $P=(0,0,1)$, two lines are drawn with direction vectors

$$
v_1=(2,1,-1),\qquad v_2=(2,1,0).
$$

For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

---

## What Are We Looking For?

Two lines start at the same point with almost the same direction. We want to see which one reaches the plane $z=0$ and which one never does, and to recognize the difference before calculating.

---

## Idea and Theorem Before the Calculation

The plane $z=0$ has normal $n=(0,0,1)$. For a line $P+tv$:

- $v\cdot n\neq0$: the line crosses the plane in exactly one point;
- $v\cdot n=0$: the line is parallel to the plane; it lies in it if $P$ does and misses it otherwise.

For this plane, $v\cdot n$ is simply the $z$-component of $v$.

---

## Step-by-Step Solution

**Line 1: direction $v_1=(2,1,-1)$.**

$$
v_1\cdot n=-1\neq0,
$$

so the line meets the plane in one point. Its points are

$$
(2t,\ t,\ 1-t).
$$

Setting $z=0$ gives $1-t=0$, so $t=1$, and the intersection point is

$$
(2,1,0).
$$

**Line 2: direction $v_2=(2,1,0)$.**

$$
v_2\cdot n=0,
$$

so the line is parallel to the plane. Its starting point $P$ has $z=1\neq0$, so it does not lie in the plane. The line has **no common point** with the plane.

**Recognizing parallelism without solving.** The $z$-component of $v_2$ is $0$, so moving along the line never changes the height $z$. The line stays at height $z=1$ forever and can never reach the plane $z=0$. No equation needs to be solved; the zero third component of the direction vector shows it immediately.

*Why this is valid:* The height of a point on the line is $1+t\cdot0=1$ for every $t$.

---

## Final Answer in Words

The line with direction $(2,1,-1)$ crosses the plane $z=0$ at the point $(2,1,0)$. The line with direction $(2,1,0)$ is parallel to the plane and never meets it, which can be seen at once because the $z$-component of its direction is zero while the line starts at height $1$.

---

## Quick Verification

Line 1: the point $(2,1,0)$ has $z=0$, and $(2,1,0)-P=(2,1,-1)=v_1$, so it lies on the line at $t=1$.

Line 2: the equation for a common point reads $1+0\cdot t=0$, that is $1=0$, which has no solution, as predicted.

---

## Common Mistakes

- **Judging by how similar the vectors look:** $v_1$ and $v_2$ differ only in the last component, but that component decides the outcome.
- **Concluding "lies in the plane" from $v\cdot n=0$:** the starting point must also be checked; here it is at height $1$.
- **Solving for $t$ in the second case and getting confused by $1=0$:** this contradiction is exactly the statement that there is no intersection.

---

## Oral Explanation (3 sentences)

For the plane $z=0$, what matters is the $z$-component of the direction vector, which equals its dot product with the normal $(0,0,1)$. The first line descends with $z=1-t$ and reaches the plane at $t=1$, at the point $(2,1,0)$. The second line has $z$-component $0$, so it stays at height $1$ forever and runs parallel to the plane without ever meeting it.

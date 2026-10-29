# Exercise 5 — Relative Position of Two Lines

## The Problem

Analyze the position of

$$
L_1:(x,y,z)=(1,1,0)+t(1,2,1),
$$

$$
L_2:(x,y,z)=(2,0,1)+s(0,1,-1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

---

## What Are We Looking For?

Two lines in space can intersect, be parallel, or be skew (neither parallel nor intersecting). We want to decide which case occurs here.

---

## Idea and Theorem Before the Calculation

**Classification of two lines in space:**

1. If the direction vectors are parallel, the lines are parallel (or identical).
2. If the directions are not parallel, the lines either intersect in one point or are skew.
3. To distinguish intersecting from skew, solve $P_1+tv_1=P_2+sv_2$; a common solution $(t,s)$ means intersection, no solution means skew.

---

## Step-by-Step Solution

**Step 1: Compare the directions.**

$$
v_1=(1,2,1),\qquad v_2=(0,1,-1).
$$

If $v_1=kv_2$, the first coordinate would give $1=0\cdot k$, which is impossible. The directions are not parallel, so the lines are not parallel.

**Step 2: Look for a common point.**

Set the coordinates equal:

$$
\begin{aligned}
1+t &= 2, \\
1+2t &= s, \\
t &= 1-s.
\end{aligned}
$$

The first equation gives $t=1$, and the second then gives $s=3$. The third equation would require $1=1-3=-2$, which is false.

*Why this is valid:* A common point must satisfy all three coordinate equations with the same $t$ and $s$. The only pair satisfying the first two fails the third, so no common point exists.

**Step 3: Classify.**

The lines are not parallel and have no common point, so they are **skew**.

---

## Final Answer in Words

The lines $L_1$ and $L_2$ are skew: their direction vectors $(1,2,1)$ and $(0,1,-1)$ are not parallel, and the system for a common point has no solution, because the values $t=1$, $s=3$ forced by two coordinates contradict the third.

---

## Quick Verification

For skew lines the distance between them is positive. The vector $v_1\times v_2$ is perpendicular to both lines:

$$
v_1\times v_2=(2\cdot(-1)-1\cdot1,\ 1\cdot0-1\cdot(-1),\ 1\cdot1-2\cdot0)=(-3,1,1).
$$

The vector between the base points is $P_2-P_1=(1,-1,1)$. The distance is

$$
\frac{|(P_2-P_1)\cdot(v_1\times v_2)|}{|v_1\times v_2|}=\frac{|-3-1+1|}{\sqrt{9+1+1}}=\frac{3}{\sqrt{11}}\neq0.
$$

Intersecting lines would give distance $0$, so the lines are indeed skew.

---

## Common Mistakes

- **Using the same parameter for both lines:** the lines are traversed independently, so they need two different parameters $t$ and $s$.
- **Stopping after two equations:** the first two coordinates can always be matched; the third decides.
- **Calling non-intersecting lines "parallel":** in space, lines with non-parallel directions can miss each other; such lines are skew.

---

## Oral Explanation (3 sentences)

The direction vectors $(1,2,1)$ and $(0,1,-1)$ are not multiples of each other, so the lines are not parallel. Looking for a common point, the first two coordinates force $t=1$ and $s=3$, but then the third coordinates are $1$ and $-2$, so there is no common point. Lines in space that are neither parallel nor intersecting are skew, and their positive distance $\frac{3}{\sqrt{11}}$ confirms this.

# Exercise 15 — Complete Classification of a Line Relative to a Plane

## The Problem

Let

$$
L:p+tv,\qquad \Pi:n\cdot x=d.
$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

---

## What Are We Looking For?

We want a general criterion, written in terms of $p$, $v$, $n$ and $d$, that decides the position of any line relative to any plane, together with one example for each case.

---

## Idea and Theorem Before the Calculation

**Substitution:** A point $p+tv$ of the line lies in the plane exactly when

$$
n\cdot(p+tv)=d.
$$

By linearity of the dot product this is

$$
(n\cdot v)\,t=d-n\cdot p.
$$

This is one linear equation in the single unknown $t$, and everything follows from the number of its solutions.

---

## Step-by-Step Solution

**Step 1: Derive the criterion.**

The equation $(n\cdot v)\,t=d-n\cdot p$ has:

- exactly one solution if $n\cdot v\neq0$, namely

$$
t=\frac{d-n\cdot p}{n\cdot v};
$$

- no solution if $n\cdot v=0$ but $d-n\cdot p\neq0$, since it reads $0=d-n\cdot p\neq0$;
- every $t$ as a solution if $n\cdot v=0$ and $d-n\cdot p=0$, since it reads $0=0$.

**Step 2: State the three cases.**

| Case | Condition | Geometric meaning |
|------|-----------|-------------------|
| one intersection point | $n\cdot v\neq0$ | the line is not parallel to the plane |
| parallel, no common points | $n\cdot v=0$ and $n\cdot p\neq d$ | parallel direction, starting point outside the plane |
| contained in the plane | $n\cdot v=0$ and $n\cdot p=d$ | parallel direction, starting point inside the plane |

*Why this is valid:* $n\cdot v$ measures how fast the value $n\cdot x$ changes along the line, and $n\cdot p$ is its value at the starting point.

**Step 3: Examples with the plane $z=0$.**

Take $n=(0,0,1)$ and $d=0$, so the plane is $z=0$.

*Example A (one point):* $p=(0,0,1)$, $v=(0,0,1)$. Then $n\cdot v=1\neq0$, and

$$
t=\frac{0-1}{1}=-1,
$$

which gives the intersection point $(0,0,0)$.

*Example B (parallel, no common point):* $p=(0,0,1)$, $v=(1,0,0)$. Then $n\cdot v=0$ and $n\cdot p=1\neq0$. The line runs at height $1$ above the plane.

*Example C (contained):* $p=(0,0,0)$, $v=(1,0,0)$. Then $n\cdot v=0$ and $n\cdot p=0=d$. The line is the $x$-axis, which lies in the plane $z=0$.

---

## Final Answer in Words

Substituting the line into the plane gives $(n\cdot v)\,t=d-n\cdot p$. The line meets the plane in exactly one point when $n\cdot v\neq0$; it is parallel without common points when $n\cdot v=0$ and $n\cdot p\neq d$; and it lies in the plane when $n\cdot v=0$ and $n\cdot p=d$. The vertical line through $(0,0,1)$, the horizontal line through $(0,0,1)$, and the $x$-axis illustrate the three cases for the plane $z=0$.

---

## Quick Verification

Substitute the general point of each example into $z=0$:

- Example A: $z=1+t=0$ only for $t=-1$, one point.
- Example B: $z=1$ for every $t$, never $0$, no point.
- Example C: $z=0$ for every $t$, every point.

The behaviour of each example agrees with the condition it was chosen to illustrate. A non-axis example confirms the first case as well: for the plane $x+y+z=4$ and the line $(1,0,2)+t(1,2,-1)$ from Exercise 8, $n\cdot v=2\neq0$ and $t=\frac{4-3}{2}=\frac12$, as found there.

---

## Common Mistakes

- **Using only $n\cdot v$:** it separates "one point" from "parallel," but the cases "parallel outside" and "contained" need the second condition $n\cdot p=d$.
- **Writing the condition with $p$ and $v$ swapped:** the direction is tested with $n\cdot v$, the position with $n\cdot p$.
- **Confusing $n\cdot v=0$ with perpendicularity of the line to the plane:** it means the line is perpendicular to the normal, so it is parallel to the plane.

---

## Oral Explanation (3 sentences)

Substituting the line $p+tv$ into the plane $n\cdot x=d$ gives the single equation $(n\cdot v)\,t=d-n\cdot p$. If $n\cdot v\neq0$ it has exactly one solution and the line crosses the plane once; if $n\cdot v=0$ the left side vanishes, and the line lies in the plane when $n\cdot p=d$ and misses it completely otherwise. For the plane $z=0$, a vertical line, a horizontal line above the plane, and the $x$-axis show the three cases.

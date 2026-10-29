# Exercise 8 — Intersection Point of a Line and a Plane

## The Problem

Find the intersection point of

$$
(x,y,z)=(1,0,2)+t(1,2,-1)
$$

with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

---

## What Are We Looking For?

We want the single point that lies both on the line and in the plane.

---

## Idea and Theorem Before the Calculation

**Substitution method:** Every point of the line has coordinates depending on $t$. Substituting them into the plane equation gives one equation in $t$. Its solution identifies the parameter of the intersection point.

The intersection is a single point because $v\cdot n=(1,2,-1)\cdot(1,1,1)=2\neq0$.

---

## Step-by-Step Solution

**Step 1: Coordinates of a general point of the line.**

$$
x=1+t,\qquad y=2t,\qquad z=2-t.
$$

**Step 2: Substitute into the plane.**

$$
(1+t)+2t+(2-t)=4\quad\Longrightarrow\quad 3+2t=4\quad\Longrightarrow\quad t=\frac12.
$$

*Why this is valid:* A point of the line lies in the plane exactly when its coordinates satisfy the plane equation.

**Step 3: Compute the point.**

$$
(1,0,2)+\frac12(1,2,-1)=\left(\frac32,\ 1,\ \frac32\right).
$$

---

## Final Answer in Words

The line meets the plane at the point $\left(\frac32,1,\frac32\right)$, reached for the parameter value $t=\frac12$.

---

## Quick Verification

Plane:

$$
\frac32+1+\frac32=4.
$$

Line: the vector from $(1,0,2)$ to the point is

$$
\left(\frac12,\ 1,\ -\frac12\right)=\frac12(1,2,-1),
$$

a multiple of the direction vector. The point satisfies both descriptions.

---

## Common Mistakes

- **Substituting $t$ for $x$:** the plane equation needs all three coordinates expressed through $t$.
- **Reporting $t$ instead of the point:** $t=\frac12$ is only the parameter; the answer is the point it produces.
- **Arithmetic slips in the sum:** $(1+t)+2t+(2-t)=3+2t$, because $t+2t-t=2t$.

---

## Oral Explanation (3 sentences)

Every point of the line has coordinates $(1+t,\ 2t,\ 2-t)$, and substituting them into $x+y+z=4$ gives the equation $3+2t=4$. Its solution $t=\frac12$ gives the intersection point $\left(\frac32,1,\frac32\right)$. This point satisfies the plane equation, and its difference from $(1,0,2)$ is half the direction vector, so it also lies on the line.

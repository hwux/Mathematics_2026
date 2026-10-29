# Exercise 4 — Plane Through Three Points

## The Problem

Find the equation of the plane through

$$
A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

---

## What Are We Looking For?

We want the equation of the plane determined by three points, built with the tools of vector geometry: two direction vectors in the plane and their cross product as the normal.

---

## Idea and Theorem Before the Calculation

**Vectors in the plane:** If $A,B,C$ lie in a plane, the differences $B-A$ and $C-A$ lie in it as well.

**Cross product as a normal:** The cross product $u\times w$ is perpendicular to both $u$ and $w$. If $u$ and $w$ are not parallel, $u\times w$ is a normal vector of the plane they span:

$$
u\times w=(u_2w_3-u_3w_2,\ u_3w_1-u_1w_3,\ u_1w_2-u_2w_1).
$$

---

## Step-by-Step Solution

**Step 1: Two vectors in the plane.**

$$
u=B-A=(-1,1,0),\qquad w=C-A=(-1,0,1).
$$

They are not parallel, since neither is a multiple of the other.

**Step 2: Cross product.**

$$
\begin{aligned}
n=u\times w &= \big(1\cdot1-0\cdot0,\ 0\cdot(-1)-(-1)\cdot1,\ (-1)\cdot0-1\cdot(-1)\big) \\
&= (1,1,1).
\end{aligned}
$$

*Why this is valid:* $n$ is perpendicular to two non-parallel vectors in the plane, so it is perpendicular to the whole plane.

**Step 3: Equation.**

With normal $(1,1,1)$ and point $A$:

$$
1(x-1)+1(y-0)+1(z-0)=0\quad\Longrightarrow\quad x+y+z=1.
$$

---

## Final Answer in Words

Two vectors in the plane are $B-A=(-1,1,0)$ and $C-A=(-1,0,1)$; their cross product $(1,1,1)$ is a normal vector, and the plane is $x+y+z=1$.

---

## Quick Verification

All three points:

$$
A:\ 1+0+0=1,\qquad B:\ 0+1+0=1,\qquad C:\ 0+0+1=1.
$$

Perpendicularity of the normal:

$$
n\cdot u=-1+1+0=0,\qquad n\cdot w=-1+0+1=0.
$$

The equation is satisfied by all three points, and the normal is perpendicular to both vectors in the plane.

---

## Common Mistakes

- **Using the points themselves in the cross product:** $A\times B$ is not a normal of the plane unless the plane passes through the origin; the vectors must be differences of points.
- **Sign errors in the middle component:** the second component of $u\times w$ is $u_3w_1-u_1w_3$.
- **Checking only one point:** an equation can pass through one point by accident; all three must satisfy it.

---

## Oral Explanation (3 sentences)

The differences $B-A=(-1,1,0)$ and $C-A=(-1,0,1)$ are two non-parallel vectors lying in the plane. Their cross product $(1,1,1)$ is perpendicular to both, so it is a normal vector, and the point $A$ then gives the equation $x+y+z=1$. Each of the three points has coordinates summing to $1$, so all of them lie in this plane.

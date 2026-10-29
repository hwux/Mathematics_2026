# Exercise 12 — A Normal Vector to a Plane

## The Problem

Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

---

## What Are We Looking For?

We want a normal vector of the plane through three points: a vector perpendicular to every direction in that plane.

---

## Idea and Theorem Before the Calculation

**Vectors in the plane:** differences of points of the plane, such as $\overrightarrow{AB}=B-A$ and $\overrightarrow{AC}=C-A$.

**Normal vector:** if two vectors in the plane are not parallel, their cross product is perpendicular to both and hence to the whole plane.

---

## Step-by-Step Solution

**Step 1: Two vectors in the plane.**

$$
\overrightarrow{AB}=(2-1,\ 1-0,\ 0-2)=(1,1,-2),
$$

$$
\overrightarrow{AC}=(0-1,\ 3-0,\ 1-2)=(-1,3,-1).
$$

They are not parallel: a multiple of $(1,1,-2)$ with first coordinate $-1$ would be $(-1,-1,2)$, not $(-1,3,-1)$.

**Step 2: Cross product.**

$$
\begin{aligned}
n=\overrightarrow{AB}\times\overrightarrow{AC} &= \big(1\cdot(-1)-(-2)\cdot3,\ (-2)\cdot(-1)-1\cdot(-1),\ 1\cdot3-1\cdot(-1)\big) \\
&= (-1+6,\ 2+1,\ 3+1) \\
&= (5,3,4).
\end{aligned}
$$

**Step 3: Check perpendicularity.**

$$
\begin{aligned}
n\cdot\overrightarrow{AB} &= 5\cdot1+3\cdot1+4\cdot(-2)=5+3-8=0, \\
n\cdot\overrightarrow{AC} &= 5\cdot(-1)+3\cdot3+4\cdot(-1)=-5+9-4=0.
\end{aligned}
$$

*Why this is valid:* A vector perpendicular to two non-parallel directions of a plane is perpendicular to every direction of the plane, since each such direction is a combination of the two.

---

## Final Answer in Words

Two vectors in the plane are $\overrightarrow{AB}=(1,1,-2)$ and $\overrightarrow{AC}=(-1,3,-1)$. Their cross product $n=(5,3,4)$ is perpendicular to both, as both dot products equal $0$, so $n$ is a normal vector of the plane.

---

## Quick Verification

With the normal $n=(5,3,4)$, the plane through $A$ has equation

$$
5(x-1)+3y+4(z-2)=0\quad\Longrightarrow\quad 5x+3y+4z=13.
$$

All three points satisfy it:

$$
A:\ 5+0+8=13,\qquad B:\ 10+3+0=13,\qquad C:\ 0+9+4=13.
$$

This confirms that $n$ is a normal of the plane containing $A$, $B$ and $C$.

---

## Common Mistakes

- **Using the points themselves as plane vectors:** the vectors in the plane are differences of points.
- **Arithmetic slips with negative entries in the cross product:** each component should be checked, for example $1\cdot(-1)-(-2)\cdot3=-1+6=5$.
- **Checking only one dot product:** perpendicularity to a single vector does not make $n$ normal to the plane.

---

## Oral Explanation (3 sentences)

The differences $\overrightarrow{AB}=(1,1,-2)$ and $\overrightarrow{AC}=(-1,3,-1)$ are two non-parallel vectors lying in the plane through $A$, $B$ and $C$. Their cross product is $n=(5,3,4)$, and its dot products with both vectors are zero. Therefore $n$ is perpendicular to the plane, and the plane equation $5x+3y+4z=13$ built from it is satisfied by all three points.

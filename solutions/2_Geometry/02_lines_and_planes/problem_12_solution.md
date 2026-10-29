# Exercise 12 — Intersection Line of Two Planes

## The Problem

Find a parametric equation of the line that is the intersection of

$$
x+y+z=3,\qquad x-y+z=1.
$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

---

## What Are We Looking For?

We want the line common to both planes, written as point plus direction, with the direction obtained both algebraically and geometrically.

---

## Idea and Theorem Before the Calculation

**Algebraic approach:** The intersection consists of the solutions of the system of two equations in three unknowns. Elimination leaves one free variable, which becomes the parameter of the line.

**Geometric approach:** The intersection line lies in both planes, so its direction is perpendicular to both normal vectors. Hence it is parallel to $n_1\times n_2$.

---

## Step-by-Step Solution

**Method 1: From the system.**

Subtract the second equation from the first:

$$
(x+y+z)-(x-y+z)=3-1\quad\Longrightarrow\quad 2y=2\quad\Longrightarrow\quad y=1.
$$

Then the first equation gives $x+z=2$. Let $z=s$ be free; then $x=2-s$. The intersection line is

$$
(x,y,z)=(2-s,\ 1,\ s)=(2,1,0)+s(-1,0,1),\qquad s\in\mathbb{R}.
$$

Direction from the system: $(-1,0,1)$.

**Method 2: From the normals.**

$$
n_1=(1,1,1),\qquad n_2=(1,-1,1).
$$

$$
\begin{aligned}
n_1\times n_2 &= \big(1\cdot1-1\cdot(-1),\ 1\cdot1-1\cdot1,\ 1\cdot(-1)-1\cdot1\big) \\
&= (2,0,-2).
\end{aligned}
$$

**Comparison.**

$$
(2,0,-2)=-2\cdot(-1,0,1).
$$

The two direction vectors are parallel; they differ only by the factor $-2$, which changes the length and orientation of the vector but not the line.

*Why this is valid:* A line has many direction vectors, all nonzero multiples of one another; both methods must produce one of them.

---

## Final Answer in Words

The intersection line is $(x,y,z)=(2,1,0)+s(-1,0,1)$. The system gives the direction $(-1,0,1)$, and the cross product of the normals gives $(2,0,-2)$, which is $-2$ times the first, so both methods describe the same direction.

---

## Quick Verification

Substitute the general point $(2-s,\ 1,\ s)$ into both planes:

$$
(2-s)+1+s=3,\qquad (2-s)-1+s=1.
$$

Both equations hold for every $s$, so the whole line lies in both planes. The direction is perpendicular to both normals: $(-1,0,1)\cdot(1,1,1)=0$ and $(-1,0,1)\cdot(1,-1,1)=0$.

---

## Common Mistakes

- **Expecting the two direction vectors to be equal:** they only need to be parallel.
- **Choosing a free variable that is already determined:** here $y=1$ is fixed, so $y$ cannot be the parameter.
- **Forgetting a point on the line:** the direction alone does not determine the line; the point $(2,1,0)$ is needed as well.

---

## Oral Explanation (3 sentences)

Subtracting the equations gives $y=1$, and then $x+z=2$, so with $z=s$ free the intersection line is $(2,1,0)+s(-1,0,1)$. The cross product of the normals $(1,1,1)$ and $(1,-1,1)$ is $(2,0,-2)$, which is perpendicular to both normals and therefore lies in both planes. This vector is $-2$ times $(-1,0,1)$, so the algebraic and geometric methods give the same direction.

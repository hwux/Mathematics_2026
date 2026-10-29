# Exercise 6 — Angle Between Planes

## The Problem

Given

$$
\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

---

## What Are We Looking For?

We want to decide whether the planes are parallel and, if not, find the angle between them, using only their normal vectors.

---

## Idea and Theorem Before the Calculation

**Parallel planes:** Two planes are parallel exactly when their normal vectors are parallel.

**Angle between planes:** The angle $\varphi$ between two planes equals the angle between their normals, taken in $[0^\circ,90^\circ]$:

$$
\cos\varphi=\frac{|n_1\cdot n_2|}{|n_1|\,|n_2|}.
$$

---

## Step-by-Step Solution

**Step 1: Read the normals.**

$$
n_1=(1,1,1),\qquad n_2=(1,-1,0).
$$

The coefficient of $z$ in $\Pi_2$ is $0$.

**Step 2: Parallel or not?**

If $n_1=kn_2$, the third coordinate would give $1=k\cdot0$, which is impossible. The normals are not parallel, so the planes are not parallel; they intersect in a line.

**Step 3: Compute the angle.**

$$
n_1\cdot n_2=1\cdot1+1\cdot(-1)+1\cdot0=0.
$$

Hence

$$
\cos\varphi=\frac{0}{\sqrt3\cdot\sqrt2}=0\quad\Longrightarrow\quad\varphi=90^\circ.
$$

The planes are perpendicular.

**Step 4: Why the normals are enough.**

A plane's orientation is completely determined by its normal: the plane consists of all directions perpendicular to $n$. Turning one plane into the position of the other turns its normal by the same angle, so the angle between the planes equals the angle between the normals. The constants $1$ and $2$ only shift the planes parallel to themselves and do not affect the angle.

---

## Final Answer in Words

The normals $(1,1,1)$ and $(1,-1,0)$ are not parallel, so the planes are not parallel. Their dot product is $0$, so the angle between the planes is $90^\circ$. Only the normals are needed, because they encode the orientation of the planes, while the constants on the right only shift them.

---

## Quick Verification

If the planes are perpendicular, $n_2$ must lie parallel to $\Pi_1$. Starting at the point $(1,0,0)$ of $\Pi_1$ and moving along $n_2$ gives $(1+s,\ -s,\ 0)$, and indeed $(1+s)+(-s)+0=1$ for every $s$. The normal of one plane lies inside the other, which is exactly the situation of perpendicular planes.

---

## Common Mistakes

- **Using the constants in the angle formula:** the right-hand sides do not influence the angle.
- **Overlooking a missing variable:** $x-y=2$ has normal $(1,-1,0)$, with $0$ for $z$.
- **Reporting an obtuse angle:** the angle between planes is taken between $0^\circ$ and $90^\circ$, which is why the absolute value appears.

---

## Oral Explanation (3 sentences)

The normal vectors $(1,1,1)$ and $(1,-1,0)$ are not multiples of each other, so the planes are not parallel. Their dot product is $0$, which means the normals are perpendicular, and hence the planes meet at a right angle. The normals are enough because they determine how each plane is tilted, while the constants on the right-hand side only move the planes without turning them.

# Exercise 13 — Closest Point on a Plane

## The Problem

Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

---

## What Are We Looking For?

We want the point of the plane nearest to $P$, the distance from $P$ to the plane, and a check that the connecting segment is perpendicular to the plane.

---

## Idea and Theorem Before the Calculation

**Closest point = orthogonal projection:** The nearest point $P'$ of a plane is reached by moving from $P$ along the normal $n$. Any other point $X$ of the plane is farther, because by the Pythagorean theorem

$$
|P-X|^2=|P-P'|^2+|P'-X|^2.
$$

---

## Step-by-Step Solution

**Step 1: Line through $P$ along the normal.**

With $n=(1,2,2)$:

$$
P+tn=(3+t,\ 2t,\ 2t).
$$

**Step 2: Intersect with the plane.**

$$
(3+t)+2(2t)+2(2t)=4\quad\Longrightarrow\quad 3+9t=4\quad\Longrightarrow\quad t=\frac19.
$$

**Step 3: Closest point.**

$$
P'=\left(3+\frac19,\ \frac29,\ \frac29\right)=\left(\frac{28}{9},\ \frac29,\ \frac29\right).
$$

**Step 4: Distance.**

$$
P'-P=\frac19(1,2,2),\qquad |P'-P|=\frac19\sqrt{1+4+4}=\frac39=\frac13.
$$

*Why this is valid:* $P'$ lies in the plane and the segment $PP'$ runs along the normal, so $P'$ is the orthogonal projection and $|PP'|$ is the distance.

---

## Final Answer in Words

The point of the plane closest to $P$ is $\left(\frac{28}{9},\frac29,\frac29\right)$, and the distance from $P$ to the plane is $\frac13$.

---

## Quick Verification

The point lies in the plane:

$$
\frac{28}{9}+2\cdot\frac29+2\cdot\frac29=\frac{28+4+4}{9}=4.
$$

The distance formula gives the same value:

$$
d=\frac{|3+0+0-4|}{\sqrt{1+4+4}}=\frac13.
$$

Perpendicularity: the vectors $u=(2,-1,0)$ and $w=(2,0,-1)$ lie in the plane, because $n\cdot u=2-2+0=0$ and $n\cdot w=2+0-2=0$. The segment vector $P'-P=\frac19(1,2,2)$ satisfies

$$
\frac19(1,2,2)\cdot(2,-1,0)=0,\qquad \frac19(1,2,2)\cdot(2,0,-1)=0,
$$

so it is perpendicular to two independent directions of the plane, hence to the plane.

---

## Common Mistakes

- **Taking $|t|$ as the distance:** the distance is $|t|\cdot|n|=\frac19\cdot3$, not $\frac19$.
- **Moving along a coordinate axis:** the closest point lies along the normal, not along the $x$-axis from $P$.
- **Checking perpendicularity against only one vector:** a segment perpendicular to one direction in the plane may still be oblique; two independent directions are needed.

---

## Oral Explanation (3 sentences)

The closest point of the plane is found by moving from $P=(3,0,0)$ along the normal $(1,2,2)$, which reaches the plane at $t=\frac19$ and gives the point $\left(\frac{28}{9},\frac29,\frac29\right)$. The connecting vector is $\frac19(1,2,2)$, whose length is $\frac13$, and this agrees with the distance formula. Since this vector is a multiple of the normal, it is perpendicular to every direction lying in the plane, as the dot products with $(2,-1,0)$ and $(2,0,-1)$ confirm.

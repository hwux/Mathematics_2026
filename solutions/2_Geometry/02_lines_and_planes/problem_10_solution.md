# Exercise 10 — Projection of a Point onto a Plane

## The Problem

Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

---

## What Are We Looking For?

We want the foot of the perpendicular from $P$ to the plane (the projection) and the point on the other side of the plane at the same distance (the reflection).

---

## Idea and Theorem Before the Calculation

**Projection:** The perpendicular from $P$ to the plane runs along the normal $n$. Its points are $P+tn$. The projection $P'$ is the point of this line that lies in the plane.

**Reflection:** The reflection $P''$ lies on the same line, on the opposite side of the plane, at the same distance. If the projection corresponds to $t_0$, the reflection corresponds to $2t_0$, so

$$
P''=2P'-P.
$$

---

## Step-by-Step Solution

**Step 1: Line through $P$ along the normal.**

With $n=(1,1,1)$:

$$
P+tn=(2+t,\ 1+t,\ 3+t).
$$

**Step 2: Intersect with the plane.**

$$
(2+t)+(1+t)+(3+t)=3\quad\Longrightarrow\quad 6+3t=3\quad\Longrightarrow\quad t=-1.
$$

**Step 3: Projection.**

$$
P'=(2-1,\ 1-1,\ 3-1)=(1,0,2).
$$

*Why this is valid:* $P'$ lies in the plane, and $P-P'=(1,1,1)$ is parallel to the normal, so the segment $PP'$ is perpendicular to the plane.

**Step 4: Reflection.**

Take $t=2\cdot(-1)=-2$:

$$
P''=(2-2,\ 1-2,\ 3-2)=(0,-1,1).
$$

Equivalently, $P''=2P'-P=(2,0,4)-(2,1,3)=(0,-1,1)$.

---

## Final Answer in Words

The orthogonal projection of $P$ onto the plane is $P'=(1,0,2)$, and the reflection of $P$ across the plane is $P''=(0,-1,1)$. The distance from $P$ to the plane is $|P-P'|=\sqrt3$.

---

## Quick Verification

Midpoint of $P$ and $P''$:

$$
\left(\frac{2+0}{2},\ \frac{1+(-1)}{2},\ \frac{3+1}{2}\right)=(1,0,2).
$$

It equals $P'$ and lies on the plane: $1+0+2=3$. Also

$$
d=\frac{|2+1+3-3|}{\sqrt3}=\frac{3}{\sqrt3}=\sqrt3=|(1,1,1)|=|P-P'|,
$$

so the distance formula agrees with the projection.

---

## Common Mistakes

- **Moving along a wrong direction:** the projection is found along the normal, not along a coordinate axis.
- **Using $t=-1$ for the reflection:** the reflection lies twice as far along the normal, at $t=-2$.
- **Forgetting the check:** the midpoint of $P$ and its reflection must be the projection and lie on the plane.

---

## Oral Explanation (3 sentences)

Moving from $P=(2,1,3)$ along the normal $(1,1,1)$ gives the points $(2+t,1+t,3+t)$, which reach the plane $x+y+z=3$ at $t=-1$, so the projection is $(1,0,2)$. Going twice as far along the normal, $t=-2$, gives the reflection $(0,-1,1)$ on the other side of the plane. The midpoint of $P$ and its reflection is exactly the projection $(1,0,2)$, which lies on the plane.

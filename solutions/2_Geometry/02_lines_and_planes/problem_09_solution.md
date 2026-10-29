# Exercise 9 — Distances

## The Problem

Compute:

1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

---

## What Are We Looking For?

We want two distances, one in the plane and one in space, and an explanation of why the two distance formulas look the same.

---

## Idea and Theorem Before the Calculation

**Distance from a point to a line in the plane:** for the line $ax+by+c=0$ and the point $(x_0,y_0)$,

$$
d=\frac{|ax_0+by_0+c|}{\sqrt{a^2+b^2}}.
$$

**Distance from a point to a plane in space:** for the plane $ax+by+cz+e=0$ and the point $(x_0,y_0,z_0)$,

$$
d=\frac{|ax_0+by_0+cz_0+e|}{\sqrt{a^2+b^2+c^2}}.
$$

---

## Step-by-Step Solution

**Part 1: Point $P=(2,3)$ and line $3x+4y-10=0$.**

Substitute $P$ into the left side:

$$
3\cdot2+4\cdot3-10=6+12-10=8.
$$

The normal is $(3,4)$ with length $\sqrt{9+16}=5$. Hence

$$
d=\frac{|8|}{5}=\frac85.
$$

**Part 2: Point $Q=(2,-1,3)$ and plane $2x-2y+z-4=0$.**

Substitute $Q$:

$$
2\cdot2-2\cdot(-1)+3-4=4+2+3-4=5.
$$

The normal is $(2,-2,1)$ with length $\sqrt{4+4+1}=3$. Hence

$$
d=\frac{|5|}{3}=\frac53.
$$

**Comparison and common idea.**

Both formulas have the same structure: substitute the point into the equation, take the absolute value, and divide by the length of the normal vector. The reason is the same in both cases. The shortest path from a point to a line in the plane, or to a plane in space, runs along the **normal direction**. Substituting the point into the left side measures how far the point is from the object in units of the normal vector $n$; dividing by $|n|$ converts this into an ordinary length.

*Why this is valid:* If $X$ is any point of the object, the distance is the length of the projection of $P-X$ onto $n$, which is $\frac{|n\cdot(P-X)|}{|n|}$, and $n\cdot(P-X)$ is exactly the value of the left side of the equation at $P$.

---

## Final Answer in Words

The distance from $P$ to the line is $\frac85$, and the distance from $Q$ to the plane is $\frac53$. Both formulas substitute the point into the equation and divide by the length of the normal vector, because in both cases the shortest distance is measured along the normal direction.

---

## Quick Verification

Part 1: move from $P$ along the unit normal $\frac15(3,4)$ by the distance $\frac85$ toward the line. Since the left side is positive at $P$, move in the direction $-n$:

$$
(2,3)-\frac85\cdot\frac15(3,4)=\left(2-\frac{24}{25},\ 3-\frac{32}{25}\right)=\left(\frac{26}{25},\ \frac{43}{25}\right).
$$

Check: $3\cdot\frac{26}{25}+4\cdot\frac{43}{25}=\frac{78+172}{25}=10$. The point lies on the line.

Part 2: similarly,

$$
Q-\frac53\cdot\frac13(2,-2,1)=\left(2-\frac{10}{9},\ -1+\frac{10}{9},\ 3-\frac59\right)=\left(\frac89,\ \frac19,\ \frac{22}{9}\right).
$$

Check: $2\cdot\frac89-2\cdot\frac19+\frac{22}{9}=\frac{16-2+22}{9}=4$. The point lies on the plane. Both foot points confirm the distances.

---

## Common Mistakes

- **Forgetting the absolute value:** a distance is never negative; the sign only tells which side of the object the point lies on.
- **Dividing by the wrong length:** the denominator is the length of the normal vector, not the constant term.
- **Moving the constant to the other side first:** the formula uses the equation written in the form "left side $=0$."

---

## Oral Explanation (3 sentences)

Substituting $P=(2,3)$ into $3x+4y-10$ gives $8$, and dividing by the length $5$ of the normal $(3,4)$ gives the distance $\frac85$; in the same way $Q$ gives $5$ in the plane equation, and dividing by $|(2,-2,1)|=3$ gives $\frac53$. The two formulas are the same because the shortest path to a line or a plane always runs along its normal. The value of the equation at the point measures the displacement along the normal, and dividing by the length of the normal turns it into an actual distance.

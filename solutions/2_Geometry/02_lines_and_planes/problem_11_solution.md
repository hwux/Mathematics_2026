# Exercise 11 — Plane Containing a Line and a Point

## The Problem

Find the equation of the plane containing

$$
(x,y,z)=(1,0,2)+t(1,1,-1)
$$

and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

---

## What Are We Looking For?

We want the plane that contains a whole line and one additional point not on the line. For this we need two independent directions in the plane and then a normal vector.

---

## Idea and Theorem Before the Calculation

**Two directions in the plane:**

1. the direction vector $v$ of the line,
2. the vector from a point $A$ of the line to $P$.

If these are not parallel (that is, if $P$ is not on the line), their cross product is a normal vector of the plane.

---

## Step-by-Step Solution

**Step 1: Directions in the plane.**

The line gives the point $A=(1,0,2)$ and the direction $v=(1,1,-1)$. The second direction is

$$
w=P-A=(0-1,\ 2-0,\ 1-2)=(-1,2,-1).
$$

$v$ and $w$ are not parallel, since $w=kv$ would need $k=-1$ from the first coordinate and $k=2$ from the second.

**Step 2: Normal vector.**

$$
\begin{aligned}
n=v\times w &= \big(1\cdot(-1)-(-1)\cdot2,\ (-1)\cdot(-1)-1\cdot(-1),\ 1\cdot2-1\cdot(-1)\big) \\
&= (1,2,3).
\end{aligned}
$$

**Step 3: Equation.**

Using the point $A$:

$$
1(x-1)+2(y-0)+3(z-2)=0\quad\Longrightarrow\quad x+2y+3z=7.
$$

*Why this is valid:* $n$ is perpendicular to two non-parallel directions of the plane, and the plane passes through $A$.

---

## Final Answer in Words

The plane containing the line and the point $P$ has normal vector $(1,2,3)$ and equation $x+2y+3z=7$.

---

## Quick Verification

**The entire line.** Substitute the general point $(1+t,\ t,\ 2-t)$:

$$
(1+t)+2t+3(2-t)=1+t+2t+6-3t=7\qquad\mathrm{for\ every}\ t.
$$

The $t$-terms cancel, so every point of the line lies in the plane. This works because $n\cdot v=1+2-3=0$.

**The point $P$.**

$$
0+2\cdot2+3\cdot1=7.
$$

Both the line and the point lie in the plane.

---

## Common Mistakes

- **Checking only one point of the line:** the plane must contain every point, which is checked with the general point $(1+t,t,2-t)$.
- **Using $P$ itself as a direction:** the second direction is the difference $P-A$, not $P$.
- **Choosing two directions that are parallel:** then the cross product is zero and gives no plane; here $P$ is not on the line, so this does not happen.

---

## Oral Explanation (3 sentences)

The plane must contain the direction $(1,1,-1)$ of the line and the direction $(-1,2,-1)$ from the point $(1,0,2)$ of the line to $P$. Their cross product $(1,2,3)$ is a normal vector, which gives the plane $x+2y+3z=7$. Substituting the general point of the line makes the $t$-terms cancel, so the whole line lies in the plane, and $P$ gives $0+4+3=7$.

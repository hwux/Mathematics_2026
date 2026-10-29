# Exercise 2 — A Line in Space

## The Problem

Given

$$
L:(x,y,z)=(2,-1,3)+t(1,2,-2).
$$

State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

---

## What Are We Looking For?

We want to read the two ingredients of a parametric line, test one point for membership, and evaluate the parametrization at a given parameter value.

---

## Idea and Theorem Before the Calculation

**Parametric form = point + direction:** In $(x,y,z)=P_0+tv$, the vector $P_0$ is the point reached at $t=0$ and $v$ is the direction of motion along the line.

**Membership test:** A point $P$ lies on the line exactly when there is **one** value of $t$ that satisfies all coordinate equations at the same time.

---

## Step-by-Step Solution

**Step 1: Point and direction.**

$$
P_0=(2,-1,3),\qquad v=(1,2,-2).
$$

**Step 2: Is $P=(4,3,-1)$ on $L$?**

Set each coordinate of $L$ equal to the coordinate of $P$:

$$
\begin{aligned}
2+t &= 4 \quad\Longrightarrow\quad t=2, \\
-1+2t &= 3 \quad\Longrightarrow\quad t=2, \\
3-2t &= -1 \quad\Longrightarrow\quad t=2.
\end{aligned}
$$

All three equations give the same value $t=2$, so $P$ lies on $L$.

*Why this is valid:* The point $P$ is reached by moving from $P_0$ exactly twice along $v$; if the three equations had given different values of $t$, no single parameter would produce $P$ and it would not lie on the line.

**Step 3: The point for $t=-1$.**

$$
(2,-1,3)+(-1)(1,2,-2)=(2-1,\ -1-2,\ 3+2)=(1,-3,5).
$$

---

## Final Answer in Words

The line passes through $(2,-1,3)$ and has direction vector $(1,2,-2)$. The point $P=(4,3,-1)$ lies on $L$, for the parameter value $t=2$. The parameter $t=-1$ gives the point $(1,-3,5)$.

---

## Quick Verification

The vector from $P_0$ to $P$ is

$$
P-P_0=(2,4,-4)=2(1,2,-2)=2v,
$$

which confirms $t=2$. The vector from $P_0$ to $(1,-3,5)$ is $(-1,-2,2)=-v$, which confirms $t=-1$.

---

## Common Mistakes

- **Checking only one coordinate:** a point lies on the line only if all three coordinates give the same $t$.
- **Forgetting the sign of $t$:** for $t=-1$ the third coordinate is $3-2(-1)=5$, not $1$.
- **Thinking the direction vector is a point of the line:** $(1,2,-2)$ describes how to move, not where the line is.

---

## Oral Explanation (3 sentences)

The parametric form shows that the line passes through $(2,-1,3)$ and moves in the direction $(1,2,-2)$. The point $(4,3,-1)$ lies on the line, because all three coordinate equations are satisfied by the same parameter value $t=2$. Substituting $t=-1$ means moving once in the opposite direction, which gives the point $(1,-3,5)$.

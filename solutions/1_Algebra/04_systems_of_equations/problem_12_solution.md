# Exercise 12 — Homogeneous System

## The Problem

Solve

$$
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

---

## What Are We Looking For?

We want the complete solution set of a system whose right-hand sides are all zero, written with a parameter, and an explanation of why the zero vector is always among the solutions.

---

## Idea and Theorem Before the Calculation

**Homogeneous system:** a system $Ax=0$ in which every right-hand side is zero.

**Consequence for elimination:** Row operations keep a zero right-hand side zero, so the right column of the augmented matrix stays zero throughout. A homogeneous system can never produce a contradiction $0=c\neq0$.

---

## Step-by-Step Solution

**Step 1: Augmented matrix.**

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
2 & 4 & -2 & \mid & 0 \\
1 & -1 & 2 & \mid & 0 \\
\end{pmatrix}
$$

**Step 2: $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-R_1$.**

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
\end{pmatrix}
$$

The second equation was twice the first.

**Step 3: $R_2\leftrightarrow R_3$.**

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 0 \\
0 & -3 & 3 & \mid & 0 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

There are two pivots for three unknowns, so one variable is free: $z$, whose column has no pivot.

**Step 4: Back substitution with $z=s$.**

$$
\begin{aligned}
-3y+3z &= 0 \quad\Longrightarrow\quad y=s, \\
x+2y-z &= 0 \quad\Longrightarrow\quad x=-2s+s=-s.
\end{aligned}
$$

**Step 5: Parametric form.**

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix} =s
\begin{pmatrix}
-1 \\
1 \\
1 \\
\end{pmatrix},\qquad s\in\mathbb{R}.
$$

The solution set is a line through the origin.

**Step 6: Why $(0,0,0)$ always works.**

In every equation of a homogeneous system, each term is a coefficient times an unknown. Substituting $0$ for every unknown makes every term $0$, so every left side equals $0$, which is exactly the right-hand side. In matrix form, $A\cdot0=0$ for every matrix $A$. The value $s=0$ above gives exactly this trivial solution.

---

## Final Answer in Words

All solutions are $(x,y,z)=s(-1,1,1)$ with $s$ any real number, a line through the origin. The zero vector is always a solution of a homogeneous system, because every term in every equation becomes zero when all unknowns are zero.

---

## Quick Verification

Substitute the direction vector $(-1,1,1)$, which corresponds to $s=1$:

$$
\begin{aligned}
-1+2\cdot1-1 &= 0, \\
2\cdot(-1)+4\cdot1-2\cdot1 &= 0, \\
-1-1+2\cdot1 &= 0.
\end{aligned}
$$

All equations hold. Since the right-hand sides are zero, multiplying this solution by any $s$ again gives a solution, which confirms the whole line.

---

## Common Mistakes

- **Stopping at $(0,0,0)$:** the trivial solution is always there, but the question asks for all solutions.
- **Expecting a contradiction:** a homogeneous system is always consistent.
- **Writing the parametric form with an extra constant vector:** for a homogeneous system the solution set passes through the origin, so no shift is needed.

---

## Oral Explanation (3 sentences)

Elimination shows that the second equation is twice the first, and the remaining two conditions give $y=z$ and $x=-z$. With $z=s$ free, all solutions are $s(-1,1,1)$, a line through the origin. The zero vector always solves a homogeneous system, because every term in every equation is a coefficient multiplied by zero.

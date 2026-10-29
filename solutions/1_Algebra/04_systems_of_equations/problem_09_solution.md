# Exercise 9 — A System from a Sum Condition

## The Problem

Find numbers $x,y$ satisfying

$$
x+y=10,\qquad 2x+5y=32.
$$

Solve the system and explain geometrically why the solution is unique.

---

## What Are We Looking For?

We want the pair $(x,y)$ that satisfies both conditions and a geometric reason why no other pair does.

---

## Idea and Theorem Before the Calculation

**Geometry of a $2\times2$ system:** Each linear equation in $x,y$ describes a line in the plane. A solution is a common point of the lines.

- Two lines with different slopes meet in exactly one point.
- Two parallel distinct lines have no common point.
- Two identical lines have infinitely many common points.

Algebraically, different slopes correspond to $\det A\neq0$.

---

## Step-by-Step Solution

**Step 1: Augmented matrix.**

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
2 & 5 & \mid & 32 \\
\end{pmatrix}
$$

**Step 2: $R_2\leftarrow R_2-2R_1$.**

$$
\begin{pmatrix}
1 & 1 & \mid & 10 \\
0 & 3 & \mid & 12 \\
\end{pmatrix}
$$

**Step 3: Back substitution.**

$$
\begin{aligned}
3y &= 12 \quad\Longrightarrow\quad y=4, \\
x+y &= 10 \quad\Longrightarrow\quad x=6.
\end{aligned}
$$

**Step 4: Geometric explanation.**

Solving each equation for $y$:

$$
y=10-x,\qquad y=\frac{32-2x}{5}.
$$

The first line has slope $-1$, the second slope $-\frac25$. The slopes are different, so the lines are not parallel and cross in exactly one point, $(6,4)$.

*Why this is valid:* Two non-parallel lines in the plane always intersect, and they cannot share two different points, since two points determine a line.

The same fact appears algebraically: $\det A=1\cdot5-1\cdot2=3\neq0$, and elimination produced a pivot in both columns.

---

## Final Answer in Words

The numbers are $x=6$ and $y=4$. The solution is unique because the two equations describe lines with different slopes, $-1$ and $-\frac25$, which intersect in exactly one point.

---

## Quick Verification

$$
6+4=10,\qquad 2\cdot6+5\cdot4=12+20=32.
$$

Both conditions hold.

---

## Common Mistakes

- **Guessing pairs with sum $10$:** guessing may find the answer, but it does not show that there is no other solution.
- **Comparing the coefficients instead of the slopes:** the lines are parallel only when the coefficient rows are proportional, which $(1,1)$ and $(2,5)$ are not.
- **Arithmetic errors in back substitution:** from $3y=12$ we get $y=4$, and then $x=10-4$.

---

## Oral Explanation (3 sentences)

Subtracting twice the first equation from the second gives $3y=12$, so $y=4$ and then $x=6$. Each equation describes a line, and the slopes of these lines, $-1$ and $-\frac25$, are different. Two non-parallel lines meet in exactly one point, which is why $(6,4)$ is the only solution.

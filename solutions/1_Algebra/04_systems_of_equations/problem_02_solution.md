# Exercise 2 — Gaussian Elimination — One Solution

## The Problem

Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

---

## What Are We Looking For?

We want the values of $x,y,z$ that satisfy all three equations, found by reducing the augmented matrix to row echelon form and then using back substitution.

---

## Idea and Theorem Before the Calculation

**Gaussian elimination:** Row operations on the augmented matrix $[A\mid b]$ do not change the solution set:

1. adding a multiple of one row to another,
2. swapping two rows,
3. multiplying a row by a nonzero number.

The goal is a row echelon form, in which each pivot has only zeros below it. The last equation then contains one unknown, and the others follow by **back substitution**.

---

## Step-by-Step Solution

**Step 0: Augmented matrix.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
2 & -1 & 1 & \mid & 3 \\
1 & 2 & -1 & \mid & 2 \\
\end{pmatrix}
$$

**Step 1: $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-R_1$.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & -3 & -1 & \mid & -9 \\
0 & 1 & -2 & \mid & -4 \\
\end{pmatrix}
$$

*Why:* This removes $x$ from the second and third equations.

**Step 2: $R_2\leftrightarrow R_3$.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & -3 & -1 & \mid & -9 \\
\end{pmatrix}
$$

*Why:* A pivot equal to $1$ avoids fractions in the next step.

**Step 3: $R_3\leftarrow R_3+3R_2$.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 6 \\
0 & 1 & -2 & \mid & -4 \\
0 & 0 & -7 & \mid & -21 \\
\end{pmatrix}
$$

The matrix is in row echelon form with three pivots, so the system has exactly one solution.

**Step 4: Back substitution.**

$$
\begin{aligned}
-7z &= -21 \quad\Longrightarrow\quad z=3, \\
y-2z &= -4 \quad\Longrightarrow\quad y=-4+6=2, \\
x+y+z &= 6 \quad\Longrightarrow\quad x=6-2-3=1.
\end{aligned}
$$

*Why this is valid:* Each row of the echelon form is an equation equivalent to the original system, and solving from the bottom introduces one new unknown at a time.

---

## Final Answer in Words

The system has exactly one solution: $x=1$, $y=2$, $z=3$.

---

## Quick Verification

Substitute $(1,2,3)$ into all three original equations:

$$
\begin{aligned}
1+2+3 &= 6, \\
2\cdot1-2+3 &= 3, \\
1+2\cdot2-3 &= 2.
\end{aligned}
$$

All three equations hold, so the solution is consistent with the whole system.

---

## Common Mistakes

- **Applying a row operation only to the left side:** the right-hand side must change together with the coefficients.
- **Sign errors in back substitution:** from $y-2z=-4$ and $z=3$ one gets $y=-4+6$, not $y=-4-6$.
- **Checking only one equation:** a wrong solution can satisfy one equation by accident; all three must be checked.

---

## Oral Explanation (3 sentences)

Gaussian elimination removes $x$ from the second and third equations, and after a row swap removes $y$ from the third, giving a triangular system with three pivots. The last equation $-7z=-21$ gives $z=3$, and back substitution gives $y=2$ and $x=1$. Substituting $(1,2,3)$ into all three original equations confirms that it is the unique solution.

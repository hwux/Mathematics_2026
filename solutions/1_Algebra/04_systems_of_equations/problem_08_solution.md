# Exercise 8 — Two Systems with the Same Coefficient Matrix

## The Problem

Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

---

## What Are We Looking For?

We want to solve two systems that share the same coefficients and differ only in their right-hand sides, and to identify which part of the work is common to both.

---

## Idea and Theorem Before the Calculation

**Row operations depend only on the coefficients:** The choice of each row operation (which rows, which multiplier) is determined by the entries of the coefficient matrix $A$. The right-hand side is only carried along.

Consequently, two systems $Ax=b_1$ and $Ax=b_2$ can be solved at the same time with the doubly augmented matrix

$$
\begin{pmatrix}
A & \mid & b_1 & b_2 \\
\end{pmatrix}.
$$

---

## Step-by-Step Solution

**Step 1: Common augmented matrix.**

Both systems have

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & -1 \\
\end{pmatrix},\qquad b_1=
\begin{pmatrix}
5 \\
1 \\
\end{pmatrix},\qquad b_2=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}.
$$

$$
\begin{pmatrix}
2 & 1 & \mid & 5 & 1 \\
1 & -1 & \mid & 1 & 4 \\
\end{pmatrix}
$$

**Step 2: $R_1\leftrightarrow R_2$.**

$$
\begin{pmatrix}
1 & -1 & \mid & 1 & 4 \\
2 & 1 & \mid & 5 & 1 \\
\end{pmatrix}
$$

*Why:* A pivot equal to $1$ keeps the calculation free of fractions.

**Step 3: $R_2\leftarrow R_2-2R_1$.**

$$
\begin{pmatrix}
1 & -1 & \mid & 1 & 4 \\
0 & 3 & \mid & 3 & -7 \\
\end{pmatrix}
$$

**Step 4: Back substitution for the first system** (column $b_1$).

$$
\begin{aligned}
3y &= 3 \quad\Longrightarrow\quad y=1, \\
x-y &= 1 \quad\Longrightarrow\quad x=2.
\end{aligned}
$$

**Step 5: Back substitution for the second system** (column $b_2$).

$$
\begin{aligned}
3y &= -7 \quad\Longrightarrow\quad y=-\frac73, \\
x-y &= 4 \quad\Longrightarrow\quad x=4-\frac73=\frac53.
\end{aligned}
$$

**Step 6: Comparison.**

| Step | Left side (coefficients) | First right side | Second right side |
|------|--------------------------|------------------|-------------------|
| start | rows $(2,1)$, $(1,-1)$ | $(5,1)$ | $(1,4)$ |
| swap | rows $(1,-1)$, $(2,1)$ | $(1,5)$ | $(4,1)$ |
| $R_2-2R_1$ | rows $(1,-1)$, $(0,3)$ | $(1,3)$ | $(4,-7)$ |

The row operations and the resulting left side are identical in both systems; only the right-hand columns differ.

---

## Final Answer in Words

The first system has the solution $x=2$, $y=1$, the second $x=\frac53$, $y=-\frac73$. The elimination steps, the swap and $R_2\leftarrow R_2-2R_1$, are the same for both systems, and so is the resulting triangular coefficient matrix. This is because every row operation is chosen by looking only at the coefficients, which the two systems share.

---

## Quick Verification

First system, $(2,1)$:

$$
2\cdot2+1=5,\qquad 2-1=1.
$$

Second system, $(\frac53,-\frac73)$:

$$
2\cdot\frac53-\frac73=\frac{10-7}{3}=1,\qquad \frac53+\frac73=\frac{12}{3}=4.
$$

All four equations hold.

---

## Common Mistakes

- **Repeating the whole elimination for the second system:** the left-side work is identical and can be done once.
- **Forgetting to apply an operation to one of the right-hand columns:** every row operation acts on all columns of the augmented matrix.
- **Thinking the solutions must be similar:** the same steps can lead to very different solutions, because the right-hand sides differ.

---

## Oral Explanation (3 sentences)

Both systems have the same coefficient matrix, so they can be solved together in the augmented matrix with two right-hand columns. The same two row operations, a swap and $R_2-2R_1$, reduce the coefficients to the same triangular form, and back substitution then gives $(2,1)$ for the first system and $(\frac53,-\frac73)$ for the second. The steps coincide because each row operation is chosen from the coefficients alone, while the right-hand sides are only carried along.

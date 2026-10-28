# Exercise 15 — Two Methods for Solving the Same System

## The Problem

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

---

## What Are We Looking For?

We want the solution of one $2\times2$ system computed by two different methods, a comparison of the results and of the work each method required, and a reasoned choice between them.

---

## Idea and Theorem Before the Calculation

**Method 1:** If $\det A\neq0$, then $x=A^{-1}b$, with the $2\times2$ inverse formula.

**Method 2:** Gaussian elimination reduces the augmented matrix $[A\mid b]$ to triangular form, and the unknowns are then found by back substitution.

Both methods must give the same result, because an invertible system has exactly one solution.

---

## Step-by-Step Solution

**Method 1: Using $A^{-1}b$.**

$\det A=2\cdot3-1\cdot1=5$, so

$$
A^{-1}=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

Then

$$
x=A^{-1}b=\frac15
\begin{pmatrix}
3\cdot7-1\cdot8 \\
-1\cdot7+2\cdot8 \\
\end{pmatrix} =\frac15
\begin{pmatrix}
13 \\
9 \\
\end{pmatrix} =
\begin{pmatrix}
\frac{13}{5} \\
\frac95 \\
\end{pmatrix}.
$$

Essential steps: determinant, inverse, one matrix-vector product.

**Method 2: Gaussian elimination.**

Write the augmented matrix and swap the rows so that the first pivot is $1$:

$$
\begin{pmatrix}
2 & 1 & \mid & 7 \\
1 & 3 & \mid & 8 \\
\end{pmatrix}\ \longrightarrow\
\begin{pmatrix}
1 & 3 & \mid & 8 \\
2 & 1 & \mid & 7 \\
\end{pmatrix}.
$$

$R_2\leftarrow R_2-2R_1$:

$$
\begin{pmatrix}
1 & 3 & \mid & 8 \\
0 & -5 & \mid & -9 \\
\end{pmatrix}.
$$

Back substitution:

$$
\begin{aligned}
-5x_2 &= -9 \quad\Longrightarrow\quad x_2=\frac95, \\
x_1 &= 8-3x_2 = 8-\frac{27}{5} = \frac{13}{5}.
\end{aligned}
$$

Essential steps: one row swap, one row replacement, two back-substitution steps.

*Why this is valid:* Row operations on the augmented matrix do not change the solution set of the system.

**Comparison.**

Both methods give $x=(\frac{13}{5},\frac95)^T$.

| Method | Essential steps | Fractions appear |
|--------|-----------------|------------------|
| $A^{-1}b$ | determinant, inverse, product | from the start (factor $\frac15$) |
| Elimination | swap, one replacement, back substitution | only at the end |

---

## Final Answer in Words

Both methods give $x_1=\frac{13}{5}$, $x_2=\frac95$. In this example elimination was slightly simpler: it needed one real row operation and back substitution, and fractions appeared only in the last step. The inverse method is equally short for a $2\times2$ matrix thanks to the explicit formula, and it becomes advantageous when the same matrix $A$ must be used with many different right-hand sides $b$, because $A^{-1}$ is computed only once.

---

## Quick Verification

Substitute into the original system:

$$
\begin{aligned}
2\cdot\frac{13}{5}+\frac95 &= \frac{26+9}{5} = \frac{35}{5} = 7, \\
\frac{13}{5}+3\cdot\frac95 &= \frac{13+27}{5} = \frac{40}{5} = 8.
\end{aligned}
$$

Both equations hold, so the common solution is correct.

---

## Common Mistakes

- **Expecting different answers from different methods:** an invertible system has exactly one solution, so the methods must agree.
- **Forgetting to apply the row swap to the right-hand side:** in elimination the whole augmented row is moved.
- **Computing $A^{-1}$ for a single system of large size:** for larger matrices, elimination is usually much cheaper than finding the full inverse.

---

## Oral Explanation (3 sentences)

Using the inverse, $\det A=5$ and $x=A^{-1}b=\frac15(13,9)^T$, while Gaussian elimination with one row swap and one row replacement leads by back substitution to the same values $x_1=\frac{13}{5}$, $x_2=\frac95$. Substituting these values into both equations gives $7$ and $8$, confirming the solution. For this single system elimination was slightly simpler, because it kept integers until the last step, whereas the inverse is more useful when the same matrix must be solved with many right-hand sides.

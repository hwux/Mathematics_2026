# Exercise 6 — Solving a System Using the Inverse

## The Problem

Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

---

## What Are We Looking For?

We want the vector $x$ that satisfies $Ax=b$, found by computing $A^{-1}$ and multiplying it by $b$, followed by a substitution check.

---

## Idea and Theorem Before the Calculation

**Solving with the inverse:** If $A$ is invertible, multiplying both sides of $Ax=b$ on the left by $A^{-1}$ gives

$$
A^{-1}Ax=A^{-1}b\quad\Longrightarrow\quad x=A^{-1}b.
$$

The solution exists and is unique.

**Inverse of a $2\times2$ matrix:** swap the diagonal entries, change the sign of the off-diagonal entries, divide by $\det A$.

---

## Step-by-Step Solution

**Step 1: Determinant.**

$$
\det A = 2\cdot3-1\cdot1 = 5\neq0,
$$

so $A$ is invertible.

**Step 2: Inverse.**

$$
A^{-1}=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

**Step 3: Multiply by $b$.**

$$
x=A^{-1}b=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix} =\frac15
\begin{pmatrix}
15-7 \\
-5+14 \\
\end{pmatrix} =\frac15
\begin{pmatrix}
8 \\
9 \\
\end{pmatrix} =
\begin{pmatrix}
\frac85 \\
\frac95 \\
\end{pmatrix}.
$$

*Why this is valid:* $A^{-1}$ must be placed on the left of $b$, because it was applied to the left side of $Ax$.

---

## Final Answer in Words

The system has the unique solution $x_1=\frac85$, $x_2=\frac95$.

---

## Quick Verification

Substitute into $Ax$:

$$
A
\begin{pmatrix}
\frac85 \\
\frac95 \\
\end{pmatrix} =
\begin{pmatrix}
2\cdot\frac85+\frac95 \\
\frac85+3\cdot\frac95 \\
\end{pmatrix} =
\begin{pmatrix}
\frac{25}{5} \\
\frac{35}{5} \\
\end{pmatrix} =
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix} = b.
$$

The vector satisfies both equations.

---

## Common Mistakes

- **Writing $x=bA^{-1}$:** this product is not even defined for a column vector $b$ and a $2\times2$ matrix; the inverse must stand on the left.
- **Forgetting the factor $\frac15$:** without it the result is $(8,9)^T$, which does not solve the system.
- **Skipping the check:** substitution takes only a moment and catches arithmetic errors immediately.

---

## Oral Explanation (3 sentences)

Since $\det A=5\neq0$, the matrix $A$ is invertible, and multiplying $Ax=b$ on the left by $A^{-1}$ gives $x=A^{-1}b$. The inverse is one fifth of the matrix with rows $(3,-1)$ and $(-1,2)$, and applying it to $b=(5,7)^T$ gives $x=(\frac85,\frac95)^T$. Substituting this vector back into the system reproduces the right-hand side $(5,7)^T$, so the solution is correct.

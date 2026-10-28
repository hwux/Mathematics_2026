# Exercise 2 — Formula for a 2×2 Matrix

## The Problem

Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

---

## What Are We Looking For?

We need the matrix $A^{-1}$, obtained from the explicit $2\times2$ formula, and a check through the definition of the inverse.

---

## Idea and Theorem Before the Calculation

**Inverse of a $2\times2$ matrix:** If

$$
A=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

and $\det A=ad-bc\neq0$, then

$$
A^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}.
$$

In words: swap the diagonal entries, change the sign of the off-diagonal entries, and divide by the determinant.

---

## Step-by-Step Solution

**Step 1: Compute the determinant.**

$$
\det A = 3\cdot4-2\cdot5 = 12-10 = 2.
$$

Since $\det A\neq0$, the inverse exists.

**Step 2: Build the adjusted matrix.**

Swap $a=3$ and $d=4$, change the signs of $b=2$ and $c=5$:

$$
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix}.
$$

**Step 3: Divide by the determinant.**

$$
A^{-1}=\frac12
\begin{pmatrix}
4 & -2 \\
-5 & 3 \\
\end{pmatrix} =
\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32 \\
\end{pmatrix}.
$$

*Why this is valid:* The formula gives the inverse of every $2\times2$ matrix with nonzero determinant; the check below confirms it for this matrix.

---

## Final Answer in Words

$\det A=2$, and

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32 \\
\end{pmatrix}.
$$

---

## Quick Verification

$$
AA^{-1}=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32 \\
\end{pmatrix} =
\begin{pmatrix}
6-5 & -3+3 \\
10-10 & -5+6 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

The product is $I$, so the result is correct.

---

## Common Mistakes

- **Forgetting to divide by the determinant:** the matrix with entries $4,-2,-5,3$ alone gives $AA^{-1}=2I$, not $I$.
- **Changing the signs of the diagonal instead of the off-diagonal entries:** the diagonal entries are swapped, the off-diagonal entries change sign.
- **Using the formula when $\det A=0$:** the formula then involves division by zero and the inverse does not exist.

---

## Oral Explanation (3 sentences)

For a $2\times2$ matrix with nonzero determinant, the inverse is obtained by swapping the diagonal entries, changing the sign of the off-diagonal entries, and dividing by the determinant. Here $\det A=2$, so the inverse has entries $2$, $-1$, $-\frac52$ and $\frac32$. Multiplying this matrix by $A$ gives the identity matrix, which confirms the result.

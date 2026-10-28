# Exercise 1 — Determinant of a 2×2 Matrix

## The Problem

Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

---

## What Are We Looking For?

We need two numbers, one determinant for each matrix, and then a decision about invertibility based on whether each number is zero or not.

---

## Idea and Theorem Before the Calculation

**Determinant of a $2\times2$ matrix:** For

$$
M=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
$$

the determinant is

$$
\det M = ad-bc,
$$

the product of the main diagonal minus the product of the other diagonal.

**Invertibility criterion:** A square matrix $M$ is invertible if and only if $\det M\neq0$.

---

## Step-by-Step Solution

**Step 1: Compute the first determinant.**

Here $a=3$, $b=-2$, $c=5$, $d=4$:

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix} = 3\cdot4-(-2)\cdot5 = 12+10 = 22.
$$

*Why this is valid:* The formula $ad-bc$ is applied directly. The minus sign in front of $bc$ combined with $b=-2$ produces a plus sign, which is the most common place for an error.

**Step 2: Compute the second determinant.**

Here $a=1$, $b=7$, $c=2$, $d=14$:

$$
\det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix} = 1\cdot14-7\cdot2 = 14-14 = 0.
$$

**Step 3: Decide invertibility.**

The first determinant equals $22\neq0$, so the first matrix is invertible.

The second determinant equals $0$, so the second matrix is not invertible.

*Why this is valid:* The invertibility criterion says that a matrix has an inverse exactly when its determinant is nonzero.

---

## Final Answer in Words

The first determinant is $22$ and the second is $0$. Only the first matrix is invertible. The second matrix is not invertible because its determinant is zero.

---

## Quick Verification

In the second matrix the second row $(2,14)$ is exactly $2$ times the first row $(1,7)$. Rows that are multiples of each other always give determinant $0$, which agrees with the computed value.

For the first matrix, the inverse can be written explicitly:

$$
\frac{1}{22}
\begin{pmatrix}
4 & 2 \\
-5 & 3 \\
\end{pmatrix}.
$$

Multiplying the first row of the original matrix by the first column of this matrix gives $\frac{1}{22}(3\cdot4+(-2)\cdot(-5))=\frac{22}{22}=1$, as expected for an inverse.

---

## Common Mistakes

- **Adding instead of subtracting:** the formula is $ad-bc$, not $ad+bc$.
- **Losing the sign of a negative entry:** with $b=-2$ the term $-bc$ becomes $+10$, not $-10$.
- **Reversing the criterion:** a zero determinant means the matrix is *not* invertible.

---

## Oral Explanation (3 sentences)

The determinant of a $2\times2$ matrix is the product of the main diagonal minus the product of the other diagonal, so the first matrix gives $12-(-10)=22$ and the second gives $14-14=0$. A matrix is invertible exactly when its determinant is different from zero, so the first matrix is invertible and the second is not. The second matrix fails because its second row is twice the first row, so the rows carry no independent information.

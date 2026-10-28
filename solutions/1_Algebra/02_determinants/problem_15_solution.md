# Exercise 15 — Combining Determinant Properties

## The Problem

Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

---

## What Are We Looking For?

We want one number, computed only from $\det A$ and $\det B$ by applying known properties in a clear order, and an explanation of why $B$ has no influence on the result.

---

## Idea and Theorem Before the Calculation

The properties used, in the order of application:

1. **Product rule:** $\det(XYZ)=\det X\cdot\det Y\cdot\det Z$ for square matrices of the same size.
2. **Inverse rule:** $\det(B^{-1})=\dfrac{1}{\det B}$ for an invertible matrix $B$.
3. **Transpose rule:** $\det(A^T)=\det A$.

---

## Step-by-Step Solution

**Step 1: Split the product.**

$$
\det\left(B^{-1}A^TB\right) = \det(B^{-1})\cdot\det(A^T)\cdot\det B.
$$

*Why this is valid:* The product rule applies to any number of square factors of the same size.

**Step 2: Replace $\det(B^{-1})$.**

$B$ is invertible, so

$$
\det(B^{-1}) = \frac{1}{\det B} = \frac13.
$$

**Step 3: Replace $\det(A^T)$.**

$$
\det(A^T) = \det A = -2.
$$

**Step 4: Multiply.**

$$
\det\left(B^{-1}A^TB\right) = \frac13\cdot(-2)\cdot3 = -2.
$$

**Step 5: Why the factors with $B$ cancel.**

After Step 1 the expression is a product of three *numbers*. Numbers commute, so the two factors involving $B$ can be brought together:

$$
\det(B^{-1})\cdot\det B = \frac{1}{\det B}\cdot\det B = 1.
$$

The matrices $B^{-1}$ and $B$ are not adjacent in the product $B^{-1}A^TB$, and in general $B^{-1}A^TB\neq A^T$. Their determinants, however, are numbers that cancel no matter where they stand. The value $\det B=3$ is therefore irrelevant: any invertible $B$ gives the same result.

---

## Final Answer in Words

$\det\left(B^{-1}A^TB\right)=-2$. The product rule splits the determinant into $\det(B^{-1})\det(A^T)\det B$, the inverse rule gives $\det(B^{-1})=\frac13$, and the transpose rule gives $\det(A^T)=-2$. The two factors coming from $B$ multiply to $1$, so only $\det A$ remains.

---

## Quick Verification

Take concrete matrices with the given determinants:

$$
A=
\begin{pmatrix}
-2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 1 \\
0 & 3 \\
\end{pmatrix},\qquad B^{-1}=\frac13
\begin{pmatrix}
3 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

Here $A^T=A$, and

$$
A^TB=
\begin{pmatrix}
-2 & -2 \\
0 & 3 \\
\end{pmatrix},\qquad B^{-1}A^TB=\frac13
\begin{pmatrix}
3 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 & -2 \\
0 & 3 \\
\end{pmatrix}=\frac13
\begin{pmatrix}
-6 & -9 \\
0 & 3 \\
\end{pmatrix}=
\begin{pmatrix}
-2 & -3 \\
0 & 1 \\
\end{pmatrix}.
$$

This matrix is triangular with determinant $(-2)\cdot1=-2$, as computed above. It also differs from $A^T$, which shows that the cancellation happens only for the determinants, not for the matrices.

---

## Common Mistakes

- **Cancelling $B^{-1}$ and $B$ inside the matrix product:** $B^{-1}A^TB$ is in general not equal to $A^T$, because the matrices do not commute.
- **Writing $\det(B^{-1})=-\det B$:** the determinant of the inverse is the reciprocal, $\frac13$.
- **Thinking the transpose changes the sign:** $\det(A^T)=\det A$.

---

## Oral Explanation (3 sentences)

The product rule turns $\det(B^{-1}A^TB)$ into the product of three numbers, $\det(B^{-1})\det(A^T)\det B$. Using $\det(B^{-1})=\frac{1}{\det B}$ and $\det(A^T)=\det A$, this becomes $\frac13\cdot(-2)\cdot3=-2$. The factors from $B$ cancel because numbers commute, even though the matrices $B^{-1}$ and $B$ cannot be cancelled inside the matrix product.

# Exercise 10 — Inverse of a Diagonal Matrix

## The Problem

Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

---

## What Are We Looking For?

We want to use the special structure of diagonal matrices to decide invertibility at a glance and to write down the inverse without any elimination.

---

## Idea and Theorem Before the Calculation

**Diagonal matrices:** A diagonal matrix is invertible if and only if all its diagonal entries are nonzero. Its determinant is the product of the diagonal entries, and its inverse is the diagonal matrix of reciprocals:

$$
\begin{pmatrix}
d_1 & 0 & 0 \\
0 & d_2 & 0 \\
0 & 0 & d_3 \\
\end{pmatrix}^{-1}=
\begin{pmatrix}
\frac1{d_1} & 0 & 0 \\
0 & \frac1{d_2} & 0 \\
0 & 0 & \frac1{d_3} \\
\end{pmatrix}.
$$

**Reason:** Multiplying two diagonal matrices multiplies their diagonal entries, so $d_i\cdot\frac1{d_i}=1$ produces $I$.

---

## Step-by-Step Solution

**Step 1: Examine $D$.**

The diagonal entries $2$, $-3$, $5$ are all nonzero, and

$$
\det D = 2\cdot(-3)\cdot5 = -30\neq0.
$$

So $D$ is invertible.

**Step 2: Examine $E$.**

The middle diagonal entry is $0$, so

$$
\det E = 2\cdot0\cdot5 = 0,
$$

and $E$ is not invertible. Concretely, $E$ sends the nonzero vector $(0,1,0)^T$ to the zero vector, so no matrix can undo $E$.

**Step 3: Write $D^{-1}$.**

$$
D^{-1}=
\begin{pmatrix}
\frac12 & 0 & 0 \\
0 & -\frac13 & 0 \\
0 & 0 & \frac15 \\
\end{pmatrix}.
$$

*Why this is valid:* Each diagonal entry is replaced by its reciprocal, as the rule for diagonal matrices states.

---

## Final Answer in Words

$D$ is invertible and $E$ is not. The inverse of $D$ is the diagonal matrix with entries $\frac12$, $-\frac13$, $\frac15$. The matrix $E$ has a zero on the diagonal, so its determinant is zero and it maps the vector $(0,1,0)^T$ to zero.

---

## Quick Verification

$$
DD^{-1}=
\begin{pmatrix}
2\cdot\frac12 & 0 & 0 \\
0 & (-3)\cdot\left(-\frac13\right) & 0 \\
0 & 0 & 5\cdot\frac15 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}.
$$

The product is $I$. For $E$, any candidate $X$ would need $EX=I$, but the second row of $EX$ is always zero because the second row of $E$ is zero, so $EX=I$ is impossible.

---

## Common Mistakes

- **Taking the reciprocal of the zero entry as "zero":** a zero on the diagonal means the matrix has no inverse at all.
- **Losing the sign:** the reciprocal of $-3$ is $-\frac13$, not $\frac13$.
- **Using full elimination:** for a diagonal matrix the answer can be written immediately, which is the point of this exercise.

---

## Oral Explanation (3 sentences)

A diagonal matrix is invertible exactly when none of its diagonal entries is zero, and then its inverse is the diagonal matrix of reciprocals. The matrix $D$ has diagonal $2,-3,5$, so its inverse has diagonal $\frac12,-\frac13,\frac15$, and multiplying them gives the identity. The matrix $E$ has a zero in the middle, so its determinant is zero and it collapses the second coordinate direction, which no matrix can undo.

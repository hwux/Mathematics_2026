# Exercise 2 — Addition and Scalar Multiplication

## The Problem

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

---

## What Are We Looking For?

We want to add, subtract, and scale matrices. The result of each operation is a new matrix of the same size, computed by performing the arithmetic entry by entry.

---

## Idea and Theorem Before the Calculation

**Entry-wise operations:** For two matrices of the same size, their sum is defined by

$$
(A+B)_{ij} = a_{ij} + b_{ij}.
$$

Scalar multiplication by a number $c$ gives

$$
(cA)_{ij} = c \cdot a_{ij}.
$$

Both operations require the matrices to have identical dimensions, because entry $(i,j)$ of $A$ can only be paired with entry $(i,j)$ of $B$ if that position exists in both matrices.

---

## Step-by-Step Solution

**Step 1 — Compute $A+B$.**

Add each pair of entries in the same position:

$$
A+B=
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5 \\
\end{pmatrix} =
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}.
$$

*Why valid:* The two matrices are both $2\times 2$, so every position $(i,j)$ exists in both, and the addition is well-defined.

**Step 2 — Compute $A-B$.**

Subtract entry by entry:

$$
A-B=
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5 \\
\end{pmatrix} =
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}.
$$

*Why valid:* Subtraction is the same as adding $-1$ times $B$, which is again entry-wise.

**Step 3 — Compute $3A$.**

Multiply every entry of $A$ by $3$:

$$
3A=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix}.
$$

**Step 4 — Compute $2B$.**

Multiply every entry of $B$ by $2$:

$$
2B=
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}.
$$

**Step 5 — Compute $3A-2B$.**

Subtract entry by entry:

$$
3A-2B=
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10 \\
\end{pmatrix} =
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$

*Why valid:* Scalar multiplication and subtraction distribute over entries independently, so the combined operation $3A-2B$ is still entry-wise.

**Step 6 — Why same size is required.**

If $A$ is $2\times 3$ and $B$ is $2\times 2$, then $A$ has an entry in position $(1,3)$ but $B$ does not. There is no natural partner to add, so the sum is undefined. Addition is only possible when both matrices have exactly the same number of rows and the same number of columns.

---

## Final Answer in Words

The three results are

$$
A+B=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix},\qquad
A-B=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix},\qquad
3A-2B=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$

Matrix addition requires identical sizes because every entry in one matrix must have exactly one corresponding entry in the other.

---

## Quick Verification

Check the $(1,2)$ entry of $3A-2B$: we need $3\cdot 2 - 2\cdot(-2) = 6+4 = 10$. The matrix shows $10$ in that position. Confirmed.

Check the $(2,2)$ entry: $3\cdot 3 - 2\cdot 5 = 9 - 10 = -1$. The matrix shows $-1$. Confirmed.

---

## Common Mistakes

- **Multiplying the wrong factor:** in $3A-2B$, some students multiply $A$ by $2$ and $B$ by $3$. Keep the coefficient paired with its own matrix.
- **Forgetting to scale before subtracting:** computing $A-B$ first and then multiplying gives $3(A-B)$, which is not the same as $3A-2B$.
- **Trying to add matrices of different sizes:** if sizes differ, the operation is simply not defined — do not pad with zeros or skip entries.

---

## Oral Explanation (3 sentences)

Matrix addition works exactly like adding two tables of numbers: you add the entries that sit in the same position, so the two tables must have the same shape. Scalar multiplication stretches every entry of the matrix by the same factor, which is why computing $3A-2B$ means first tripling every entry of $A$ and doubling every entry of $B$, then subtracting. The dimension requirement for addition is not a technicality — it is necessary because the operation is defined position by position, and a position that exists in one matrix but not in the other has no natural partner.


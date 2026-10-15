# Exercise 4 — Matrix Multiplication and Noncommutativity

## The Problem

For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

---

## What Are We Looking For?

We compute the product in both orders and compare the results to see whether the order of multiplication matters.

---

## Idea and Theorem Before the Calculation

**Matrix multiplication rule:** The entry in row $i$ and column $j$ of the product $PQ$ is the dot product of row $i$ of $P$ with column $j$ of $Q$:

$$
(PQ)_{ij} = \sum_{k} p_{ik}\,q_{kj}.
$$

For $2\times2$ matrices this gives four entries, each computed from one row-column pair.

**Key fact:** For numbers, $ab = ba$ always. For matrices, $AB \neq BA$ in general — multiplication is *noncommutative*.

---

## Step-by-Step Solution

**Step 1 — Compute $AB$.**

Row 1 of $A$ is $(1,2)$, row 2 of $A$ is $(0,1)$. Column 1 of $B$ is $(2,3)^T$, column 2 of $B$ is $(0,1)^T$.

$$
(AB)_{11} = 1\cdot2 + 2\cdot3 = 2+6 = 8,
$$

$$
(AB)_{12} = 1\cdot0 + 2\cdot1 = 0+2 = 2,
$$

$$
(AB)_{21} = 0\cdot2 + 1\cdot3 = 0+3 = 3,
$$

$$
(AB)_{22} = 0\cdot0 + 1\cdot1 = 0+1 = 1.
$$

Therefore

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}.
$$

*Why valid:* Both matrices are $2\times2$, so all four dot products are between vectors of length 2, and the product is $2\times2$.

**Step 2 — Compute $BA$.**

Row 1 of $B$ is $(2,0)$, row 2 of $B$ is $(3,1)$. Column 1 of $A$ is $(1,0)^T$, column 2 of $A$ is $(2,1)^T$.

$$
(BA)_{11} = 2\cdot1 + 0\cdot0 = 2,
$$

$$
(BA)_{12} = 2\cdot2 + 0\cdot1 = 4,
$$

$$
(BA)_{21} = 3\cdot1 + 1\cdot0 = 3,
$$

$$
(BA)_{22} = 3\cdot2 + 1\cdot1 = 7.
$$

Therefore

$$
BA=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

**Step 3 — Compare.**

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}
\neq
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}
= BA.
$$

So $AB \neq BA$ for these matrices. This demonstrates **noncommutativity**: the order in which two matrices are multiplied generally changes the result.

---

## Final Answer in Words

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix},\qquad
BA=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

The two products are different, so $AB\neq BA$. Matrix multiplication is noncommutative: reversing the order of the factors generally produces a different matrix.

---

## Quick Verification

Check $(AB)_{11} = 8$: row 1 of $A$ is $(1,2)$, column 1 of $B$ is $(2,3)^T$, dot product $= 1\cdot2 + 2\cdot3 = 8$. Correct.

Check $(BA)_{22} = 7$: row 2 of $B$ is $(3,1)$, column 2 of $A$ is $(2,1)^T$, dot product $= 3\cdot2 + 1\cdot1 = 7$. Correct.

---

## Common Mistakes

- **Assuming commutativity:** students often write $AB=BA$ out of habit from scalar arithmetic. This is one of the most important differences between numbers and matrices.
- **Computing entry $(i,j)$ as row $j$ of the left factor times column $i$ of the right factor:** always take row $i$ of the *left* matrix and column $j$ of the *right* matrix.
- **Mixing up which product is which:** clearly label $AB$ and $BA$ before computing, then compare at the end.

---

## Oral Explanation (3 sentences)

To multiply two matrices $A$ and $B$, each entry of the result is the dot product of a row from $A$ with a column from $B$; because the choice of row comes from $A$ and the choice of column comes from $B$, swapping the order to $BA$ draws the row from $B$ and the column from $A$, which is a completely different computation. This example confirms that $AB$ and $BA$ are both $2\times2$ matrices, yet they differ in three out of four entries, proving that matrix multiplication is noncommutative. Noncommutativity is not a flaw — it reflects the geometric reality that applying two transformations in different orders can lead to very different outcomes.


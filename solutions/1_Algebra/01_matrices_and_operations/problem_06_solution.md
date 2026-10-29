# Exercise 6 — Transpose

## The Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

---

## What Are We Looking For?

We practice transposing matrices (flipping rows and columns) and verify a fundamental identity that says the transpose of a product reverses the order of the factors.

---

## Idea and Theorem Before the Calculation

**Transpose:** The transpose $M^T$ of a matrix $M$ is formed by turning rows into columns. If $M$ is $m\times n$, then $M^T$ is $n\times m$, and $(M^T)_{ij} = M_{ji}$.

**Reverse-order identity:** For any two matrices for which the product $AB$ is defined,

$$
(AB)^T = B^T A^T.
$$

The order reverses because each entry of $(AB)^T$ is a dot product of a row of $B$ with a column of $A$, which is exactly what $B^T A^T$ computes.

---

## Step-by-Step Solution

**Step 1 — Compute $A^T$.**

$A$ is $2\times3$, so $A^T$ is $3\times2$. Rows of $A$ become columns of $A^T$:

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}.
$$

*Why valid:* Each column $j$ of $A^T$ is row $j$ of $A$, which is the definition of the transpose.

**Step 2 — Compute $B^T$.**

$B$ is $3\times2$, so $B^T$ is $2\times3$. Rows of $B$ become columns of $B^T$:

$$
B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}.
$$

**Step 3 — Compute $AB$.**

$A$ is $2\times3$ and $B$ is $3\times2$; inner dimensions both equal 3, so $AB$ is $2\times2$.

$$
(AB)_{11} = 1\cdot1 + 2\cdot2 + 3\cdot(-1) = 1+4-3 = 2,
$$

$$
(AB)_{12} = 1\cdot0 + 2\cdot1 + 3\cdot3 = 0+2+9 = 11,
$$

$$
(AB)_{21} = 4\cdot1 + 5\cdot2 + 6\cdot(-1) = 4+10-6 = 8,
$$

$$
(AB)_{22} = 4\cdot0 + 5\cdot1 + 6\cdot3 = 0+5+18 = 23.
$$

Therefore

$$
AB=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}.
$$

**Step 4 — Compute $(AB)^T$ directly.**

Transpose the result above by turning rows into columns:

$$
(AB)^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

**Step 5 — Compute $B^T A^T$ and compare.**

$B^T$ is $2\times3$ and $A^T$ is $3\times2$; the product $B^T A^T$ is $2\times2$.

$$
(B^T A^T)_{11} = 1\cdot1 + 2\cdot2 + (-1)\cdot3 = 1+4-3 = 2,
$$

$$
(B^T A^T)_{12} = 1\cdot4 + 2\cdot5 + (-1)\cdot6 = 4+10-6 = 8,
$$

$$
(B^T A^T)_{21} = 0\cdot1 + 1\cdot2 + 3\cdot3 = 0+2+9 = 11,
$$

$$
(B^T A^T)_{22} = 0\cdot4 + 1\cdot5 + 3\cdot6 = 0+5+18 = 23.
$$

Therefore

$$
B^T A^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

*Why valid:* The two matrices $(AB)^T$ and $B^T A^T$ are identical, confirming the identity in this example.

---

## Final Answer in Words

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix},\qquad
B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix},\qquad
AB=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}.
$$

The identity $(AB)^T = B^T A^T$ holds: both sides equal

$$
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

---

## Quick Verification

The $(1,2)$ entry of $(AB)^T$ is the $(2,1)$ entry of $AB$, which is $8$. The $(1,2)$ entry of $B^T A^T$ was computed as $8$. They match. The $(2,1)$ entry of $(AB)^T$ is the $(1,2)$ entry of $AB$, which is $11$, and $B^T A^T$ also gives $11$ there. Confirmed.

---

## Common Mistakes

- **Forgetting to reverse the order:** students sometimes write $(AB)^T = A^T B^T$. The correct identity reverses the order to $B^T A^T$.
- **Transposing entry by entry without flipping the layout:** the transpose swaps row and column indices. Entry $(i,j)$ of $M$ becomes entry $(j,i)$ of $M^T$.
- **Checking dimensions before transposing:** when multiplying $B^T A^T$, verify that $B^T$ is $2\times3$ and $A^T$ is $3\times2$ so the product is defined. The dimensions work out precisely because $A$ and $B$ were compatible in the original order.

---

## Oral Explanation (3 sentences)

The transpose of a matrix is formed by reflecting it across its main diagonal: rows become columns and columns become rows, so a $2\times3$ matrix becomes $3\times2$. When you transpose a product of two matrices, the order of the factors must be reversed: $(AB)^T = B^T A^T$, not $A^T B^T$. This reversal is not an accident — it mirrors the fact that putting on shoes and socks must be undone in reverse order: to reverse "first socks, then shoes," you must first remove shoes and then socks.


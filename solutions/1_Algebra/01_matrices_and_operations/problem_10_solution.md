# Exercise 10 — Columns of a Matrix Product

## The Problem

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

---

## What Are We Looking For?

We want to see that the full matrix product $AB$ can be understood column by column: each column of the result is obtained by multiplying $A$ by the corresponding column of $B$.

---

## Idea and Theorem Before the Calculation

**Column interpretation of matrix multiplication:** If $B = [b_1 \mid b_2 \mid \cdots \mid b_k]$ is written as a list of its column vectors, then

$$
AB = [Ab_1 \mid Ab_2 \mid \cdots \mid Ab_k].
$$

This means: to find column $j$ of $AB$, multiply $A$ by column $j$ of $B$. The full product is assembled from these column-by-column computations.

This is not a shortcut — it is the definition of matrix multiplication viewed one column at a time.

---

## Step-by-Step Solution

**Step 1 — Identify the columns of $B$.**

$$
b_1=
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},\qquad
b_2=
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}.
$$

**Step 2 — Compute $Ab_1$.**

$A$ is $2\times3$ and $b_1$ is $3\times1$; the product is $2\times1$.

$$
Ab_1=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix} =
\begin{pmatrix}
1\cdot1+2\cdot(-1)+0\cdot3 \\
0\cdot1+1\cdot(-1)+1\cdot3 \\
\end{pmatrix} =
\begin{pmatrix}
1-2+0 \\
0-1+3 \\
\end{pmatrix} =
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}.
$$

*Why valid:* Each entry of $Ab_1$ is the dot product of a row of $A$ with the vector $b_1$, which requires matching lengths — here both have length 3.

**Step 3 — Compute $Ab_2$.**

$$
Ab_2=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix} =
\begin{pmatrix}
1\cdot2+2\cdot0+0\cdot1 \\
0\cdot2+1\cdot0+1\cdot1 \\
\end{pmatrix} =
\begin{pmatrix}
2+0+0 \\
0+0+1 \\
\end{pmatrix} =
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

**Step 4 — Compute $AB$ directly.**

$A$ is $2\times3$ and $B$ is $3\times2$; the product $AB$ is $2\times2$.

$$
(AB)_{11} = 1\cdot1+2\cdot(-1)+0\cdot3 = -1,
$$

$$
(AB)_{12} = 1\cdot2+2\cdot0+0\cdot1 = 2,
$$

$$
(AB)_{21} = 0\cdot1+1\cdot(-1)+1\cdot3 = 2,
$$

$$
(AB)_{22} = 0\cdot2+1\cdot0+1\cdot1 = 1.
$$

Therefore

$$
AB=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

**Step 5 — Compare and explain.**

The first column of $AB$ is $(-1,\,2)^T$, which equals $Ab_1$.

The second column of $AB$ is $(2,\,1)^T$, which equals $Ab_2$.

*Why this is always true:* Column $j$ of $AB$ is computed from the $j$-th column of $B$ alone. When carrying out the full matrix multiplication, the entries in row $i$, column $j$ of $AB$ depend only on row $i$ of $A$ and column $j$ of $B$. Assembling column $j$ for all rows $i$ at once is exactly the computation $Ab_j$. Therefore

$$
AB = [Ab_1 \mid Ab_2].
$$

---

## Final Answer in Words

$$
Ab_1=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix},\qquad
Ab_2=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\qquad
AB=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

The columns of $AB$ are exactly $Ab_1$ and $Ab_2$: computing the full product $AB$ is equivalent to applying $A$ to each column of $B$ independently and placing the results side by side.

---

## Quick Verification

Read off column 1 of $AB$: $(-1,2)^T$. This equals $Ab_1$ computed in Step 2. Read off column 2 of $AB$: $(2,1)^T$. This equals $Ab_2$ computed in Step 3. Both match — confirmed.

---

## Common Mistakes

- **Thinking $AB$ requires always working entry by entry:** the column interpretation shows that the product can be organized differently — and often more intuitively.
- **Confusing columns and rows:** it is the *columns* of $B$ that get multiplied by $A$, not the rows. The rows of $B$ would be used if multiplying $B$ on the right by $A$.
- **Forgetting to check dimension compatibility:** $A$ is $2\times3$ and each column of $B$ is $3\times1$, so $Ab_j$ is $2\times1$. The result $AB$ is $2\times2$, matching the sizes of $A$ (2 rows) and $B$ (2 columns).

---

## Oral Explanation (3 sentences)

Multiplying a matrix $A$ by a matrix $B$ can be understood column by column: each column of the product $AB$ is obtained by multiplying $A$ by the corresponding column of $B$, exactly as if $B$ were a single column vector. This is not a trick — it follows directly from the row-dot-column definition of matrix multiplication, because the entries in column $j$ of $AB$ depend only on column $j$ of $B$. This column-by-column view is fundamental: it explains what matrix multiplication does geometrically — the columns of $B$ are vectors in the input space, and $A$ maps each of them to a vector in the output space, with those images forming the columns of $AB$.


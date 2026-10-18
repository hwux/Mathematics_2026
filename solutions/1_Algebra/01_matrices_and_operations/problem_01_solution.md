# Exercise 1 — Matrix Size and Entries

## The Problem

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

---

## What Are We Looking For?

We need to understand how a matrix is organized: how many rows and columns it has, and how individual entries are identified by their position using two indices.

---

## Idea and Notation Before the Calculation

A matrix of size $m \times n$ has $m$ rows and $n$ columns. The entry $a_{ij}$ sits in row $i$ and column $j$. The row index always comes first.

**Notation:** $a_{ij}$ = the entry of matrix $A$ in the $i$-th row and $j$-th column.

---

## Step-by-Step Solution

**Step 1 — Count rows and columns.**

Matrix $A$ has 2 rows and 3 columns, so its size is $2 \times 3$.

Matrix $B$ has 3 rows and 2 columns, so its size is $3 \times 2$.

*Why this is valid:* The size of a matrix is simply the number of rows by the number of columns, read from the layout of the matrix.

**Step 2 — Read off individual entries.**

Locate each entry by moving to the row given by the first index and the column given by the second index.

- $a_{12}$: row 1, column 2 of $A$ — this is $-1$.
- $a_{23}$: row 2, column 3 of $A$ — this is $5$.
- $b_{21}$: row 2, column 1 of $B$ — this is $-2$.
- $b_{32}$: row 3, column 2 of $B$ — this is $1$.

*Why this is valid:* The double-index convention $a_{ij}$ unambiguously identifies any entry; the first index selects the horizontal strip (row) and the second selects the vertical strip (column).

**Step 3 — Extract a row and a column as vectors.**

The second row of $A$ consists of the three entries in row 2, read left to right:

$$
\text{Row 2 of } A = (0,\ 4,\ 5).
$$

The first column of $B$ consists of the three entries in column 1, read top to bottom:

$$
\text{Column 1 of } B =
\begin{pmatrix}
1 \\
-2 \\
4 \\
\end{pmatrix}.
$$

*Why this is valid:* A row is written as a horizontal vector and a column as a vertical vector, matching the orientation they occupy in the matrix.

---

## Final Answer in Words

Matrix $A$ is $2\times 3$ and matrix $B$ is $3\times 2$. The entries are $a_{12}=-1$, $a_{23}=5$, $b_{21}=-2$, $b_{32}=1$. The second row of $A$ is the vector $(0,4,5)$ and the first column of $B$ is the vertical vector with entries $1$, $-2$, $4$.

---

## Quick Verification

To check an index, count manually. For $a_{23}$: go to row 2 (the second horizontal strip) — it contains $0,4,5$ — then move to column 3, giving $5$. This matches the answer. For $b_{32}$: go to row 3 of $B$ — it contains $4,1$ — then column 2, giving $1$. Confirmed.

---

## Common Mistakes

- **Reversing the indices:** writing $a_{ij}$ when the entry is actually in row $j$, column $i$. Always say "row first, column second."
- **Confusing size notation:** writing $3\times 2$ for $A$ instead of $2\times 3$. Count rows first, then columns.
- **Writing a column vector horizontally:** a column is vertical by convention; writing $(1,-2,4)$ instead of a vertical vector loses the orientation information.

---

## Oral Explanation (3 sentences)

A matrix is a rectangular table of numbers, and its size is described as "rows by columns," so $A$ is $2\times 3$ because it has 2 rows and 3 columns. The entry $a_{ij}$ lives at the intersection of the $i$-th row and the $j$-th column, which is why $a_{23}$ is the number in the second row and third column, namely $5$. A row of a matrix is a horizontal list of numbers, while a column is a vertical list, and both can be treated as vectors.

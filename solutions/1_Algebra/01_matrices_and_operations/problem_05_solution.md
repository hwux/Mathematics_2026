# Exercise 5 — Matrix Times Vector

## The Problem

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

---

## What Are We Looking For?

We want to compute the product of a matrix with a vector, and then rewrite that product as a weighted sum of the columns of the matrix.

---

## Idea and Theorem Before the Calculation

**Two equivalent views of $Ax$:**

**View 1 — Row by vector:** Each entry of $Ax$ is the dot product of a row of $A$ with the vector $x$.

**View 2 — Linear combination of columns:** If $a_1$ and $a_2$ are the columns of $A$ and $x = (x_1, x_2)^T$, then

$$
Ax = x_1\,a_1 + x_2\,a_2.
$$

This means $Ax$ is a weighted sum of the columns of $A$, where the weights are the entries of $x$.

Both views always give the same answer. View 2 is the deeper one: it shows that the image of $x$ under $A$ lies in the space spanned by the columns of $A$.

---

## Step-by-Step Solution

**Step 1 — Compute $Ax$ using the row-dot-product rule.**

$$
Ax=
\begin{pmatrix}
2\cdot4 + (-1)\cdot2 \\
1\cdot4 + 3\cdot2 \\
\end{pmatrix} =
\begin{pmatrix}
8-2 \\
4+6 \\
\end{pmatrix} =
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

*Why valid:* $A$ is $2\times2$ and $x$ is a $2\times1$ column vector. The inner dimensions both equal 2, so the product is defined and the result is $2\times1$.

**Step 2 — Identify the columns of $A$.**

The first column of $A$ is

$$
a_1=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},
$$

and the second column is

$$
a_2=
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}.
$$

The entries of $x$ are $x_1=4$ and $x_2=2$.

**Step 3 — Form the linear combination.**

$$
x_1\,a_1 + x_2\,a_2 = 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix} =
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}
+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix} =
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

*Why valid:* Scalar multiplication scales each entry of the column, and vector addition adds entry by entry. The result equals $Ax$ computed in Step 1, confirming that both views are equivalent.

---

## Final Answer in Words

$$
Ax=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

As a linear combination of the columns of $A$:

$$
Ax = 4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+ 2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix} =
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

The entry $x_1=4$ tells us how much of the first column to take, and $x_2=2$ tells us how much of the second column to take.

---

## Quick Verification

Row 1 of $A$ is $(2,-1)$, and its dot product with $(4,2)^T$ gives $8-2=6$. This is the first entry of $Ax$. Row 2 of $A$ is $(1,3)$, and its dot product with $(4,2)^T$ gives $4+6=10$. Both entries match the linear combination result.

---

## Common Mistakes

- **Treating $Ax$ as element-wise multiplication:** $Ax$ is not $(2\cdot4,\,-1\cdot2,\,1\cdot4,\,3\cdot2)$. The row-dot-product rule applies.
- **Forgetting the sign when reading matrix entries:** the entry in position $(1,2)$ of $A$ is $-1$, not $1$. Sign errors cause the first component of $Ax$ to be wrong.
- **Confusing columns and rows in the linear combination:** the coefficients come from $x$ and the columns come from $A$, not the other way around.

---

## Oral Explanation (3 sentences)

Multiplying a matrix $A$ by a vector $x$ can be understood in two equivalent ways: row by row, each entry of the result is a dot product of a row of $A$ with the full vector $x$; or, taking the column view, the result is a linear combination of the columns of $A$ where each column is weighted by the corresponding entry of $x$. In this example, the vector $x = (4,2)^T$ tells us to take 4 copies of the first column plus 2 copies of the second column, and adding those two scaled columns gives $(6,10)^T$. This column interpretation is fundamental: it shows that $Ax$ always lives in the span of the columns of $A$, which is the key to understanding what a matrix "does" geometrically.


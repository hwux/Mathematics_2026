# Exercise 7 — Inverse of a Product

## The Problem

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

---

## What Are We Looking For?

We want to compute the inverse of the product $AB$ in two ways, directly and through the inverses of the factors, and understand why the order of the factors is reversed.

---

## Idea and Theorem Before the Calculation

**Inverse of a product:** If $A$ and $B$ are invertible matrices of the same size, then

$$
(AB)^{-1}=B^{-1}A^{-1}.
$$

**Reason:** $(AB)(B^{-1}A^{-1})=A(BB^{-1})A^{-1}=AIA^{-1}=AA^{-1}=I$, and similarly in the other order.

---

## Step-by-Step Solution

**Step 1: Compute $AB$.**

$$
AB=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix} =
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}.
$$

**Step 2: Invert $AB$ directly.**

$\det(AB)=2\cdot3-3\cdot0=6$, so

$$
(AB)^{-1}=\frac16
\begin{pmatrix}
3 & -3 \\
0 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}.
$$

**Step 3: Invert the factors.**

$\det A=1$, so

$$
A^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

$B$ is diagonal, so its inverse has the reciprocal diagonal entries:

$$
B^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}.
$$

**Step 4: Compute $B^{-1}A^{-1}$.**

$$
B^{-1}A^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix}.
$$

This is the same matrix as in Step 2.

**Step 5: The wrong order for comparison.**

$$
A^{-1}B^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13 \\
\end{pmatrix} =
\begin{pmatrix}
\frac12 & -\frac13 \\
0 & \frac13 \\
\end{pmatrix}.
$$

The top-right entry differs, so $A^{-1}B^{-1}\neq(AB)^{-1}$.

**Step 6: Meaning of the reversed order.**

The product $ABx$ applies $B$ first and $A$ second. To undo this, the last operation must be undone first: apply $A^{-1}$ first, then $B^{-1}$. Written as a product acting on a vector, this is $B^{-1}A^{-1}$.

---

## Final Answer in Words

Both calculations give

$$
(AB)^{-1}=B^{-1}A^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix},
$$

while the product in the original order, $A^{-1}B^{-1}$, gives a different matrix. The order is reversed because undoing a sequence of operations must start with the last one.

---

## Quick Verification

$$
(AB)(B^{-1}A^{-1})=
\begin{pmatrix}
2 & 3 \\
0 & 3 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13 \\
\end{pmatrix} =
\begin{pmatrix}
1 & -1+1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

The product is $I$, as it must be.

---

## Common Mistakes

- **Writing $(AB)^{-1}=A^{-1}B^{-1}$:** Step 5 shows that this gives a different matrix in general.
- **Inverting a diagonal matrix incorrectly:** the inverse of a diagonal matrix has the reciprocals on the diagonal, not the negatives.
- **Assuming the two orders agree because one entry is zero:** here the matrices differ only in the top-right entry, which is easy to overlook.

---

## Oral Explanation (3 sentences)

Inverting $AB$ directly and multiplying $B^{-1}A^{-1}$ both give the matrix with rows $(\frac12,-\frac12)$ and $(0,\frac13)$, which confirms the rule $(AB)^{-1}=B^{-1}A^{-1}$. The product $A^{-1}B^{-1}$ in the original order gives a different matrix, so the reversal is essential. The reason is that $AB$ applies $B$ first and $A$ last, and undoing these operations must start with the one performed last, like taking off shoes before socks.

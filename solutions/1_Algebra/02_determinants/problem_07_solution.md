# Exercise 7 — Using Properties Instead of Recomputing

## The Problem

Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

---

## What Are We Looking For?

We do not know the entries of $A$, only its size and its determinant. We must find four new determinants using properties alone.

---

## Idea and Theorem Before the Calculation

For an $n\times n$ matrix $A$ and a number $c$:

1. **Scalar multiple:** $\det(cA)=c^n\det A$, because each of the $n$ rows is multiplied by $c$.
2. **Transpose:** $\det(A^T)=\det A$.
3. **Product:** $\det(AB)=\det A\cdot\det B$; in particular $\det(A^2)=(\det A)^2$.

Here $n=3$.

---

## Step-by-Step Solution

**Step 1: $\det(2A)$.**

$$
\det(2A) = 2^3\det A = 8\cdot(-4) = -32.
$$

*Why this is valid:* Multiplying the matrix by $2$ multiplies each of its three rows by $2$, and each row contributes one factor $2$ to the determinant.

**Step 2: $\det(A^T)$.**

$$
\det(A^T) = \det A = -4.
$$

*Why this is valid:* Transposition turns rows into columns, and the determinant can be computed equally well from columns, so its value does not change.

**Step 3: $\det(A^2)$.**

$$
\det(A^2) = \det(AA) = \det A\cdot\det A = (-4)^2 = 16.
$$

*Why this is valid:* The determinant of a product is the product of the determinants.

**Step 4: $\det(-A)$.**

$$
\det(-A) = (-1)^3\det A = -1\cdot(-4) = 4.
$$

*Why this is valid:* $-A=(-1)A$, so this is the scalar multiple rule with $c=-1$ and $n=3$.

---

## Final Answer in Words

$\det(2A)=-32$, $\det(A^T)=-4$, $\det(A^2)=16$ and $\det(-A)=4$.

---

## Quick Verification

Test the rules on a concrete $3\times3$ matrix with determinant $-4$:

$$
A=
\begin{pmatrix}
-4 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}.
$$

It is diagonal, so every determinant is the product of the diagonal entries:

- $2A$ has diagonal $-8,2,2$, so $\det(2A)=-32$;
- $A^T=A$, so $\det(A^T)=-4$;
- $A^2$ has diagonal $16,1,1$, so $\det(A^2)=16$;
- $-A$ has diagonal $4,-1,-1$, so $\det(-A)=4$.

All four values agree with the answers above.

---

## Common Mistakes

- **Writing $\det(2A)=2\det A$:** the factor $2$ appears once for every row, so for a $3\times3$ matrix it is $2^3=8$.
- **Thinking $\det(-A)=-\det A$ always:** this holds only for odd $n$; for even $n$ one gets $\det(-A)=\det A$.
- **Thinking transposition changes the sign:** $\det(A^T)$ is always equal to $\det A$.

---

## Oral Explanation (3 sentences)

Multiplying a $3\times3$ matrix by a number $c$ multiplies each of its three rows by $c$, so the determinant is multiplied by $c^3$, which gives $\det(2A)=8\cdot(-4)=-32$ and $\det(-A)=(-1)\cdot(-4)=4$. Transposition does not change the determinant, so $\det(A^T)=-4$. Since the determinant of a product is the product of the determinants, $\det(A^2)=(-4)^2=16$.

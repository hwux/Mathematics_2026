# Exercise 4 — Triangular Matrix

## The Problem

Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

---

## What Are We Looking For?

We need the determinant of an upper-triangular matrix, found from its structure alone, together with the general rule and a reason why the rule works.

---

## Idea and Theorem Before the Calculation

**Triangular matrix:** A square matrix is upper-triangular if all entries below the main diagonal are zero, and lower-triangular if all entries above the main diagonal are zero.

**Rule:** The determinant of a triangular matrix (upper or lower) equals the product of its diagonal entries:

$$
\det T = t_{11}\,t_{22}\cdots t_{nn}.
$$

---

## Step-by-Step Solution

**Step 1: Recognize the structure.**

All entries below the main diagonal are $0$, so the matrix is upper-triangular. Its diagonal entries are $2$, $-3$, $7$.

**Step 2: Apply the rule.**

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix} = 2\cdot(-3)\cdot7 = -42.
$$

**Step 3: Explain why the rule holds in this example.**

Every term of the determinant is a product of three entries, one from each row and one from each column. In the third row, the only nonzero entry is $7$ in column 3, so any nonzero term must use it. In the second row, column 3 is already taken, and the entry in column 1 is $0$, so a nonzero term must use $-3$ in column 2. In the first row only column 1 remains, giving $2$. Hence the only product that can be nonzero is

$$
2\cdot(-3)\cdot7,
$$

and it comes with a plus sign because it is the main diagonal.

*Why this is valid:* The same argument works for any size $n$: the zeros below the diagonal force every nonzero term to use exactly the diagonal entries.

---

## Final Answer in Words

The determinant equals $-42$. For any triangular matrix the determinant is the product of the diagonal entries; here this product is $2\cdot(-3)\cdot7$.

---

## Quick Verification

Expanding along the first column, where only the entry $2$ is nonzero, gives

$$
2\cdot\det
\begin{pmatrix}
-3 & 5 \\
0 & 7 \\
\end{pmatrix} = 2\cdot(-21-0) = -42.
$$

This agrees with the rule. The expansion is used here only as a check, not as the main method.

---

## Common Mistakes

- **Using the entries above the diagonal:** the numbers $4$, $1$, $5$ do not affect the determinant of a triangular matrix.
- **Applying the rule to a non-triangular matrix:** the product of the diagonal is the determinant only when all entries on one side of the diagonal are zero.
- **Losing the sign of a negative diagonal entry:** $2\cdot(-3)\cdot7$ is negative.

---

## Oral Explanation (3 sentences)

The given matrix is upper-triangular, because all entries below the main diagonal are zero, so its determinant is simply the product of the diagonal entries, $2\cdot(-3)\cdot7=-42$. This works because every term of a determinant picks one entry from each row and each column, and the zeros below the diagonal kill every choice except the diagonal itself. The entries above the diagonal therefore play no role in the value of the determinant.

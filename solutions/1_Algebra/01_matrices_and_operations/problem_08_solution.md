# Exercise 8 — Row Operations and Their Reversibility

## The Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2 \leftarrow R_2 - 2R_1$,
2. $R_3 \leftarrow R_3 + R_1$,
3. Interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

---

## What Are We Looking For?

We want to apply three elementary row operations one at a time, track the matrix after each step, and understand that each operation can be undone.

---

## Idea and Theorem Before the Calculation

**Elementary row operations** are the three basic tools used to transform a matrix while preserving the solution set of the associated linear system:

1. **Replacement:** replace row $R_i$ by $R_i + c\,R_j$ for some scalar $c$.
2. **Scaling:** replace row $R_i$ by $c\,R_i$ for $c\neq0$.
3. **Interchange:** swap rows $R_i$ and $R_j$.

**Reversibility:** Each operation has an inverse:
- Replacement $R_i \leftarrow R_i + c\,R_j$ is reversed by $R_i \leftarrow R_i - c\,R_j$.
- Scaling $R_i \leftarrow c\,R_i$ is reversed by $R_i \leftarrow \frac{1}{c}\,R_i$.
- Interchange $R_i \leftrightarrow R_j$ is reversed by the same interchange $R_i \leftrightarrow R_j$.

---

## Step-by-Step Solution

**Starting matrix:**

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

---

**Operation 1:** $R_2 \leftarrow R_2 - 2R_1$.

Subtract twice row 1 from row 2. Row 1 and row 3 are unchanged:

$$
R_2 - 2R_1 = (2-2\cdot1,\;4-2\cdot2,\;1-2\cdot(-1)) = (0,\;0,\;3).
$$

Matrix after Operation 1:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

*Why valid:* Adding a multiple of one row to another does not alter the row space or the solution set of the system — it is the most fundamental elimination step.

Reverse operation: $R_2 \leftarrow R_2 + 2R_1$.

---

**Operation 2:** $R_3 \leftarrow R_3 + R_1$.

Add row 1 to row 3. Rows 1 and 2 are unchanged:

$$
R_3 + R_1 = (-1+1,\;1+2,\;3+(-1)) = (0,\;3,\;2).
$$

Matrix after Operation 2:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}.
$$

*Why valid:* Same reasoning as Operation 1 — replacing a row by itself plus a multiple of another row is reversible and preserves the row structure.

Reverse operation: $R_3 \leftarrow R_3 - R_1$.

---

**Operation 3:** Interchange $R_2$ and $R_3$.

Swap the second and third rows:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}.
$$

*Why valid:* Swapping rows reorders the equations without changing which solutions exist. The matrix is now in row echelon form.

Reverse operation: Interchange $R_2$ and $R_3$ again (the same swap).

---

## Final Answer in Words

After all three operations the matrix is

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}.
$$

This is upper triangular (row echelon) form. Each operation is reversible:

- $R_2 \leftarrow R_2 - 2R_1$ is reversed by $R_2 \leftarrow R_2 + 2R_1$.
- $R_3 \leftarrow R_3 + R_1$ is reversed by $R_3 \leftarrow R_3 - R_1$.
- Interchange $R_2 \leftrightarrow R_3$ is reversed by the same interchange.

---

## Quick Verification

To verify Operation 1, start from the intermediate matrix after that step and apply the reverse:

$$
R_2 \leftarrow R_2 + 2R_1 = (0+2\cdot1,\;0+2\cdot2,\;3+2\cdot(-1)) = (2,\;4,\;1).
$$

This restores the original row 2. Confirmed.

---

## Common Mistakes

- **Modifying the pivot row:** in $R_2 \leftarrow R_2 - 2R_1$, only row 2 changes. Row 1 stays exactly as it was.
- **Applying operations in the wrong order when reversing:** to undo three operations done in order 1-2-3, the reverse must be applied in order 3-2-1.
- **Forgetting the sign when reversing a replacement:** adding $2R_1$ to $R_2$ is reversed by *subtracting* $2R_1$, not by repeating the addition.

---

## Oral Explanation (3 sentences)

Row operations are systematic ways to simplify a matrix while keeping the structure of the underlying linear system intact: replacing one row by itself plus a multiple of another row is the core step of Gaussian elimination. Each of the three elementary row operations is reversible, which means no information is lost — you can always get back to where you started. After the three operations in this exercise, the matrix is upper triangular, which is the goal of Gaussian elimination and makes solving a linear system straightforward by back-substitution.


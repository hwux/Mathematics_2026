# Exercise 11 — Shortening the Calculation with Row Operations

## The Problem

Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

---

## What Are We Looking For?

We want a short calculation: plan row operations that make the matrix triangular, use only operations whose effect on the determinant is known, and then read off the result.

---

## Idea and Theorem Before the Calculation

**Operations that do not change the determinant:** $R_i\leftarrow R_i+cR_j$ with $i\neq j$, that is, adding a multiple of another row.

**Operations that do change it:** a row swap multiplies the determinant by $-1$, and multiplying a row by $c$ multiplies the determinant by $c$.

**Plan:** The first column consists of three equal entries $1$, so subtracting $R_1$ from the other rows clears the column at once. Only row replacements are needed, so the determinant will never change during the calculation.

---

## Step-by-Step Solution

**Step 1: $R_2\leftarrow R_2-R_1$ and $R_3\leftarrow R_3-R_1$.**

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
$$

Determinant: unchanged.

*Why this is valid:* Both operations add a multiple of another row, which leaves the determinant unchanged.

**Step 2: $R_3\leftarrow R_3-2R_2$.**

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

Determinant: unchanged.

**Step 3: Read off the triangular determinant.**

$$
\det = 1\cdot1\cdot1 = 1.
$$

---

## Final Answer in Words

The determinant equals $1$. All three operations used were of the type "add a multiple of another row," which does not change the determinant, so the determinant of the final triangular matrix is the determinant of the original matrix.

---

## Quick Verification

Sarrus' rule applied directly to the original matrix:

$$
\begin{aligned}
\det &= 1\cdot3\cdot6+2\cdot4\cdot1+3\cdot1\cdot4 \\
&\quad -\left(3\cdot3\cdot1+1\cdot4\cdot4+2\cdot1\cdot6\right) \\
&= 38-37 = 1.
\end{aligned}
$$

The direct calculation involves larger numbers and nearly equal sums, while the row-operation method produced the result with only small integers.

---

## Common Mistakes

- **Scaling a row to "simplify" it and forgetting the factor:** such an operation changes the determinant and was deliberately avoided here.
- **Using $R_2\leftarrow R_1-R_2$:** this is $-1$ times the replacement $R_2-R_1$ and therefore changes the sign of the determinant.
- **Stopping before the matrix is triangular:** the diagonal product equals the determinant only for a triangular matrix.

---

## Oral Explanation (3 sentences)

Because the first column contains three equal entries, subtracting the first row from the other two rows clears the column immediately, and one more subtraction makes the matrix triangular. Adding a multiple of one row to another never changes the determinant, so all three operations kept its value. The final triangular matrix has only ones on the diagonal, so the determinant is $1$.

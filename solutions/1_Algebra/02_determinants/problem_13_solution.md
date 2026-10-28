# Exercise 13 — Determinant by Elimination

## The Problem

Compute the determinant

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

---

## What Are We Looking For?

We want $\det A$, obtained by reducing $A$ to an upper-triangular matrix, with a written record of how each step affects the determinant.

---

## Idea and Theorem Before the Calculation

**Elimination:** Use the pivot in the first column to create zeros below it, then the pivot in the second column, and so on, until the matrix is upper-triangular.

**Effect on the determinant:**

| Operation | Effect on $\det$ |
|-----------|------------------|
| $R_i\leftarrow R_i+cR_j$ | no change |
| $R_i\leftrightarrow R_j$ | multiplied by $-1$ |
| $R_i\leftarrow cR_i$ | multiplied by $c$ |

**Triangular matrix:** the determinant is the product of the diagonal entries.

---

## Step-by-Step Solution

**Step 1: Clear the first column.**

$R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-R_1$:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}
$$

Effect: no change, since both operations add a multiple of another row.

**Step 2: Clear the second column below the pivot.**

$R_3\leftarrow R_3+2R_2$:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

Effect: no change.

*Why this is valid:* The pivot in the second column is $1$, so adding $2R_2$ removes the entry $-2$ without any division.

**Step 3: Read off the determinant.**

$$
\det A = 1\cdot1\cdot1 = 1.
$$

**Record of operations:**

| Step | Operation | Effect on $\det$ |
|------|-----------|------------------|
| 1 | $R_2\leftarrow R_2-2R_1$ | none |
| 1 | $R_3\leftarrow R_3-R_1$ | none |
| 2 | $R_3\leftarrow R_3+2R_2$ | none |

No swaps and no scalings were needed, so the triangular determinant equals $\det A$ directly.

---

## Final Answer in Words

$\det A=1$. Elimination used only row replacements, none of which change the determinant, and the resulting triangular matrix has diagonal entries $1,1,1$.

---

## Quick Verification

Sarrus' rule applied directly to $A$:

$$
\begin{aligned}
\det A &= 1\cdot5\cdot2+2\cdot7\cdot1+3\cdot2\cdot0 \\
&\quad -\left(3\cdot5\cdot1+1\cdot7\cdot0+2\cdot2\cdot2\right) \\
&= 24-23 = 1.
\end{aligned}
$$

The two methods agree. Since $\det A\neq0$, the matrix is also invertible.

---

## Common Mistakes

- **Not recording the operations:** if a swap or a scaling had been used, its factor would be lost without a record.
- **Eliminating with the wrong sign:** $R_3\leftarrow R_3-2R_2$ would give $-3$ instead of $0$ in the second column.
- **Reading the diagonal before the matrix is triangular:** the product of the diagonal is the determinant only after all entries below the diagonal are zero.

---

## Oral Explanation (3 sentences)

Elimination clears the first column with $R_2-2R_1$ and $R_3-R_1$, then clears the second column with $R_3+2R_2$, and every one of these row replacements leaves the determinant unchanged. The result is an upper-triangular matrix with diagonal entries $1,1,1$, so its determinant is $1$. Because no swaps or scalings were used, this is also the determinant of the original matrix $A$.

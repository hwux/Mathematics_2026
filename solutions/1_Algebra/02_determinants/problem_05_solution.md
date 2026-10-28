# Exercise 5 — Row Operations

## The Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

---

## What Are We Looking For?

We want to reduce $A$ to a triangular matrix with row operations, keep an exact record of how each operation affects the determinant, and then read off $\det A$.

---

## Idea and Theorem Before the Calculation

**Effect of elementary row operations on the determinant:**

1. $R_i\leftarrow R_i+cR_j$ (with $i\neq j$): the determinant does **not** change.
2. $R_i\leftrightarrow R_j$: the determinant is multiplied by $-1$.
3. Multiplying a row by a number $c$ multiplies the determinant by $c$. Equivalently, a common factor $c$ of one row can be taken out in front of the determinant.

**Triangular matrix:** its determinant is the product of the diagonal entries (Exercise 4).

---

## Step-by-Step Solution

**Step 1: $R_2\leftarrow R_2-2R_1$.**

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

Determinant: unchanged.

**Step 2: $R_3\leftarrow R_3+R_1$.**

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

Determinant: unchanged.

*Why this is valid:* Adding a multiple of one row to another row does not change the determinant.

**Step 3: Take the factor $-3$ out of $R_2$.**

$$
\det A = -3\cdot\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 6 & 5 \\
\end{pmatrix}.
$$

Determinant of the new matrix: divided by $-3$, which is why the factor $-3$ is written in front.

*Why this is valid:* The determinant is linear in each row, so a common factor of one row can be moved outside.

**Step 4: $R_3\leftarrow R_3-6R_2$.**

$$
\det A = -3\cdot\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 0 & -7 \\
\end{pmatrix}.
$$

Determinant: unchanged.

**Step 5: Read off the triangular determinant.**

$$
\det A = -3\cdot\left(1\cdot1\cdot(-7)\right) = -3\cdot(-7) = 21.
$$

---

## Final Answer in Words

$\det A=21$. Three row replacements did not change the determinant, and taking the factor $-3$ out of the second row was compensated by writing $-3$ in front.

---

## Quick Verification

Sarrus' rule applied directly to $A$:

$$
\begin{aligned}
\det A &= 1\cdot1\cdot2+2\cdot0\cdot(-1)+3\cdot2\cdot4 \\
&\quad -\left(3\cdot1\cdot(-1)+1\cdot0\cdot4+2\cdot2\cdot2\right) \\
&= 26-5 = 21.
\end{aligned}
$$

The two methods agree.

---

## Common Mistakes

- **Forgetting the factor taken out of a row:** after dividing a row by $-3$, the factor $-3$ must remain in front of the determinant.
- **Using $R_i\leftarrow cR_i+R_j$ as if it were harmless:** multiplying the row being replaced by $c$ multiplies the determinant by $c$.
- **Counting row replacements as sign changes:** only row swaps change the sign.

---

## Oral Explanation (3 sentences)

Adding a multiple of one row to another does not change the determinant, so the operations $R_2-2R_1$, $R_3+R_1$ and $R_3-6R_2$ can be used freely to create zeros below the diagonal. Taking the common factor $-3$ out of the second row is allowed as long as this factor is kept in front of the determinant. The final triangular matrix has determinant $1\cdot1\cdot(-7)=-7$, and multiplying by the factor $-3$ gives $\det A=21$.

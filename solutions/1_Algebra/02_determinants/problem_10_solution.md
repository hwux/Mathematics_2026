# Exercise 10 — Detecting Dependence

## The Problem

Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

---

## What Are We Looking For?

We must see from the structure of the matrix that its determinant is zero, name the exact linear relation between the rows, and explain what this relation means for invertibility.

---

## Idea and Theorem Before the Calculation

**Dependent rows:** If one row of a square matrix is a linear combination of the other rows, the determinant is $0$.

**Reason:** Subtracting that combination from the row does not change the determinant, but it turns the row into a row of zeros, and a matrix with a zero row has determinant $0$.

**Invertibility:** A square matrix with determinant $0$ is not invertible.

---

## Step-by-Step Solution

**Step 1: Compare the rows.**

$$
R_1=(1,2,3),\qquad R_2=(2,4,6),\qquad R_3=(0,1,5).
$$

Every entry of $R_2$ is twice the corresponding entry of $R_1$, so

$$
R_2 = 2R_1,\qquad\mathrm{equivalently}\qquad 2R_1-R_2 = 0.
$$

**Step 2: Turn the dependence into a zero row.**

Perform $R_2\leftarrow R_2-2R_1$, which does not change the determinant:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5 \\
\end{pmatrix}.
$$

**Step 3: Conclude.**

Every term of a determinant contains exactly one entry from the second row, and all those entries are $0$. Hence the determinant of this matrix is $0$, and so is the determinant of the original matrix.

*Why this is valid:* The row replacement kept the determinant unchanged, so both matrices have the same determinant.

**Step 4: Connect with noninvertibility.**

Since the determinant is $0$, the matrix is not invertible. Concretely, the rows describe only two independent conditions instead of three, so the equation $Ax=0$ has nonzero solutions. From $R_3$: $x_2+5x_3=0$, and from $R_1$: $x_1+2x_2+3x_3=0$. Choosing $x_3=1$ gives $x_2=-5$ and $x_1=7$:

$$
x=
\begin{pmatrix}
7 \\
-5 \\
1 \\
\end{pmatrix}.
$$

An invertible matrix could send only the zero vector to zero, so this nonzero solution proves that the matrix is not invertible.

---

## Final Answer in Words

The second row is exactly twice the first row, $R_2=2R_1$. Subtracting $2R_1$ from $R_2$ produces a zero row without changing the determinant, so the determinant is $0$. Consequently the matrix is not invertible, and for example the nonzero vector $(7,-5,1)^T$ is mapped to the zero vector.

---

## Quick Verification

Check that $A(7,-5,1)^T=0$ row by row:

- $R_1$: $1\cdot7+2\cdot(-5)+3\cdot1 = 7-10+3 = 0$;
- $R_2$: $2\cdot7+4\cdot(-5)+6\cdot1 = 14-20+6 = 0$;
- $R_3$: $0\cdot7+1\cdot(-5)+5\cdot1 = 0$.

All three products are zero, which confirms the dependence and the noninvertibility.

---

## Common Mistakes

- **Expecting a zero row or column to be visible directly:** a dependence can be hidden as a multiple, as here, and becomes visible only after a row operation.
- **Thinking every zero determinant comes from two proportional rows:** in general one row may be a combination of several others.
- **Calling the matrix invertible because no entry is zero:** invertibility depends on the relations between rows, not on individual entries.

---

## Oral Explanation (3 sentences)

The second row of the matrix is exactly twice the first row, so subtracting twice the first row from the second turns it into a row of zeros without changing the determinant. A matrix with a zero row has determinant zero, because every term of the determinant contains a factor from that row. A zero determinant means the matrix is not invertible, which can also be seen from the nonzero vector $(7,-5,1)^T$ that the matrix sends to zero.

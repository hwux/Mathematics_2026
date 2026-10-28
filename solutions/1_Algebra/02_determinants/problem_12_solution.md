# Exercise 12 — A Parameter Revealed by a Row Operation

## The Problem

For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

---

## What Are We Looking For?

We want the values of $t$ that make $\det A(t)=0$, found with the help of one row operation, and an explanation of what this value means for the rows of the matrix.

---

## Idea and Theorem Before the Calculation

**Invertibility criterion:** $A(t)$ is not invertible exactly when $\det A(t)=0$.

**Row replacement:** $R_2\leftarrow R_2-2R_1$ does not change the determinant.

**Row swap:** interchanging two rows multiplies the determinant by $-1$.

---

## Step-by-Step Solution

**Step 1: Perform $R_2\leftarrow R_2-2R_1$.**

The new second row is

$$
(2,4,t)-2(1,2,3) = (0,0,t-6),
$$

so

$$
\det A(t) = \det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t-6 \\
0 & 1 & 1 \\
\end{pmatrix}.
$$

*Why this is valid:* Adding a multiple of one row to another does not change the determinant.

**Step 2: Make the matrix triangular with a row swap.**

Interchanging $R_2$ and $R_3$ gives an upper-triangular matrix and introduces a factor $-1$:

$$
\det A(t) = -\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & t-6 \\
\end{pmatrix} = -\left(1\cdot1\cdot(t-6)\right) = 6-t.
$$

**Step 3: Solve $\det A(t)=0$.**

$$
6-t=0 \quad\Longleftrightarrow\quad t=6.
$$

**Step 4: What happens to the rows for $t=6$.**

For $t=6$ the second row of $A(6)$ is

$$
(2,4,6) = 2\cdot(1,2,3),
$$

so the second row is exactly twice the first row. The operation $R_2\leftarrow R_2-2R_1$ then produces a complete row of zeros. The rows are linearly dependent, which is precisely why the determinant vanishes.

---

## Final Answer in Words

$\det A(t)=6-t$, so the matrix is not invertible only for $t=6$. For this value the second row becomes twice the first row, the rows are dependent, and the row operation $R_2-2R_1$ turns the second row into zeros.

---

## Quick Verification

Sarrus' rule for general $t$:

$$
\begin{aligned}
\det A(t) &= 1\cdot4\cdot1+2\cdot t\cdot0+3\cdot2\cdot1 \\
&\quad -\left(3\cdot4\cdot0+1\cdot t\cdot1+2\cdot2\cdot1\right) \\
&= 10-(t+4) = 6-t.
\end{aligned}
$$

This is the same expression as above, so $t=6$ is confirmed.

---

## Common Mistakes

- **Forgetting the sign from the row swap:** without the factor $-1$ one obtains $t-6$; the zero $t=6$ is the same, but the determinant itself would be wrong.
- **Expanding first and ignoring the hint:** the row operation makes the role of $t$ visible immediately, because only one entry depends on $t$ afterwards.
- **Claiming the matrix is never invertible because two rows look similar:** the rows are dependent only for the single value $t=6$.

---

## Oral Explanation (3 sentences)

Subtracting twice the first row from the second leaves the second row $(0,0,t-6)$, and after swapping the second and third rows the matrix is triangular with determinant $t-6$, so the original determinant is $6-t$. The matrix is therefore not invertible exactly when $t=6$. For this value the second row $(2,4,6)$ is twice the first row $(1,2,3)$, so the rows are dependent and the row operation produces a zero row.

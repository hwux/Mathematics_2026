# Exercise 3 — When Does the Inverse Not Exist?

## The Problem

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

---

## What Are We Looking For?

We want two separate arguments for the same conclusion, one numerical (the determinant) and one structural (the relation between the rows), and we want to see that they describe the same fact.

---

## Idea and Theorem Before the Calculation

**Determinant criterion:** A square matrix is invertible if and only if its determinant is nonzero.

**Row criterion:** A square matrix is invertible if and only if its rows are linearly independent. If one row is a multiple of another, the rows are dependent.

---

## Step-by-Step Solution

**Method 1: Determinant.**

$$
\det A = 2\cdot2-4\cdot1 = 4-4 = 0.
$$

Since the determinant is zero, $A$ is not invertible. Also the $2\times2$ formula would require division by $\det A=0$, which is impossible.

**Method 2: Dependence between the rows.**

The rows are

$$
R_1=(2,4),\qquad R_2=(1,2).
$$

Every entry of $R_1$ is twice the corresponding entry of $R_2$, so

$$
R_1=2R_2.
$$

The rows are dependent. Consequently $A$ sends some nonzero vector to zero: with $x=(2,-1)^T$,

$$
Ax=
\begin{pmatrix}
2\cdot2+4\cdot(-1) \\
1\cdot2+2\cdot(-1) \\
\end{pmatrix} =
\begin{pmatrix}
0 \\
0 \\
\end{pmatrix}.
$$

If $A^{-1}$ existed, then $x=A^{-1}Ax=A^{-1}0=0$, which contradicts $x\neq0$. Hence $A^{-1}$ does not exist.

*Why this is valid:* An invertible matrix sends only the zero vector to zero, because the inverse would recover the original vector from its image.

**Connection between the two methods.**

The two arguments are not independent facts. For a $2\times2$ matrix, $ad-bc=0$ means exactly that the rows are proportional, so the determinant measures whether the rows are dependent.

---

## Final Answer in Words

$A^{-1}$ does not exist. First, $\det A=0$. Second, the first row is twice the second row, so the rows are dependent and $A$ maps the nonzero vector $(2,-1)^T$ to zero, which an invertible matrix can never do.

---

## Quick Verification

Attempt the Gauss-Jordan method on $[A\mid I]$. The operation $R_1\leftarrow R_1-2R_2$ gives

$$
\begin{pmatrix}
0 & 0 & \mid & 1 & -2 \\
1 & 2 & \mid & 0 & 1 \\
\end{pmatrix}.
$$

The left half now contains a zero row, so it can never be turned into $I$. The method fails exactly as the two arguments predict.

---

## Common Mistakes

- **Looking for a zero entry:** the matrix has no zero entries, yet it is not invertible; what matters is the relation between the rows.
- **Using the $2\times2$ formula anyway:** dividing by $\det A=0$ is not allowed.
- **Treating the two criteria as unrelated:** a zero determinant and dependent rows are two descriptions of the same situation.

---

## Oral Explanation (3 sentences)

The determinant of $A$ is $2\cdot2-4\cdot1=0$, so $A$ has no inverse. The same conclusion follows from the rows: the first row is twice the second, so $A$ sends the nonzero vector $(2,-1)^T$ to zero, and no inverse could bring it back. Both arguments describe the same fact, because a $2\times2$ determinant is zero exactly when the rows are proportional.

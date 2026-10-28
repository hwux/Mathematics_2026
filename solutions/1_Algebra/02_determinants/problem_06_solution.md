# Exercise 6 — Parameter and Invertibility

## The Problem

For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

---

## What Are We Looking For?

$A(t)$ is a whole family of matrices, one for each real number $t$. We want the exceptional values of $t$ for which the matrix has no inverse.

---

## Idea and Theorem Before the Calculation

**Invertibility criterion:** A square matrix is invertible if and only if its determinant is nonzero. Therefore $A(t)$ is not invertible exactly for those $t$ that satisfy

$$
\det A(t) = 0.
$$

The determinant of $A(t)$ is a function of $t$, so the condition becomes an ordinary equation in $t$.

---

## Step-by-Step Solution

**Step 1: Compute the determinant as a function of $t$.**

$$
\det A(t) = t\cdot t-1\cdot2 = t^2-2.
$$

**Step 2: Find the zeros.**

$$
t^2-2=0 \quad\Longleftrightarrow\quad t^2=2 \quad\Longleftrightarrow\quad t=\sqrt2 \ \mathrm{or}\ t=-\sqrt2.
$$

*Why this is valid:* A real number squared equals $2$ exactly when it is $\sqrt2$ or $-\sqrt2$.

**Step 3: Interpret.**

For $t=\pm\sqrt2$ the determinant is zero, so $A(t)$ is not invertible. For every other real $t$ the determinant is nonzero, so $A(t)$ is invertible.

---

## Final Answer in Words

The matrix $A(t)$ is not invertible exactly for $t=\sqrt2$ and $t=-\sqrt2$. These are the values for which $\det A(t)=t^2-2$ equals zero; for all other values of $t$ the matrix is invertible.

---

## Quick Verification

Take $t=\sqrt2$:

$$
A(\sqrt2)=
\begin{pmatrix}
\sqrt2 & 1 \\
2 & \sqrt2 \\
\end{pmatrix}.
$$

Multiplying the first row by $\sqrt2$ gives $(2,\sqrt2)$, which is exactly the second row. The rows are proportional, so the matrix cannot be invertible. The same happens for $t=-\sqrt2$, where the second row is $-\sqrt2$ times the first.

For a value such as $t=0$ the determinant is $-2\neq0$, so $A(0)$ is invertible, as the answer claims.

---

## Common Mistakes

- **Forgetting the negative root:** $t^2=2$ has two solutions, $\sqrt2$ and $-\sqrt2$.
- **Answering the opposite question:** the task asks where the matrix is *not* invertible, which is where the determinant *equals* zero.
- **Writing $\det A(t)=t^2+2$:** the term $bc=1\cdot2$ is subtracted.

---

## Oral Explanation (3 sentences)

A matrix is invertible exactly when its determinant is nonzero, so for the family $A(t)$ the problem reduces to solving $\det A(t)=t^2-2=0$. This equation has the two solutions $t=\sqrt2$ and $t=-\sqrt2$, and for these values the rows of the matrix become proportional. For every other value of $t$ the determinant is nonzero and the matrix has an inverse.

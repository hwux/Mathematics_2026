# Exercise 11 — Parameter and Invertibility

## The Problem

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

---

## What Are We Looking For?

$A(t)$ is a family of matrices depending on a real parameter $t$. We want the values of $t$ for which an inverse exists, one formula for the inverse that works for all these values, and an explanation of how the formula fails at the remaining values.

---

## Idea and Theorem Before the Calculation

**Invertibility criterion:** $A(t)$ is invertible if and only if $\det A(t)\neq0$.

**Inverse of a $2\times2$ matrix:**

$$
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a \\
\end{pmatrix}.
$$

---

## Step-by-Step Solution

**Step 1: Determinant.**

$$
\det A(t) = 1\cdot1-t\cdot t = 1-t^2 = (1-t)(1+t).
$$

**Step 2: Invertibility.**

$\det A(t)=0$ exactly when $t=1$ or $t=-1$. Hence $A(t)$ is invertible for all real $t$ with

$$
t\neq1\qquad\mathrm{and}\qquad t\neq-1.
$$

**Step 3: Inverse formula.**

For $t\neq\pm1$,

$$
A(t)^{-1}=\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix}.
$$

*Why this is valid:* The $2\times2$ formula applies whenever the determinant $1-t^2$ is nonzero.

**Step 4: The excluded values.**

At $t=\pm1$ the factor $\frac{1}{1-t^2}$ requires division by zero, so the formula gives no matrix at all. As $t$ approaches $1$ or $-1$, the entries of $A(t)^{-1}$ grow without bound.

This matches what happens to the matrix itself:

$$
A(1)=
\begin{pmatrix}
1 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad A(-1)=
\begin{pmatrix}
1 & -1 \\
-1 & 1 \\
\end{pmatrix}.
$$

In $A(1)$ the two rows are equal, and in $A(-1)$ the second row is $-1$ times the first. In both cases the rows are dependent, and the matrices send the nonzero vectors $(1,-1)^T$ and $(1,1)^T$, respectively, to zero.

---

## Final Answer in Words

$A(t)$ is invertible exactly for $t\neq\pm1$, and then $A(t)^{-1}$ is $\frac{1}{1-t^2}$ times the matrix with rows $(1,-t)$ and $(-t,1)$. At $t=\pm1$ the determinant is zero, the formula would require division by zero, and the rows of $A(t)$ become dependent.

---

## Quick Verification

Multiply for general $t\neq\pm1$:

$$
A(t)\cdot
\begin{pmatrix}
1 & -t \\
-t & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1-t^2 & -t+t \\
t-t & -t^2+1 \\
\end{pmatrix} =(1-t^2)I.
$$

Dividing by $1-t^2$ gives $I$, so the formula is correct for every allowed $t$. For example, $t=0$ gives $A(0)=I$ and $A(0)^{-1}=I$, as expected.

---

## Common Mistakes

- **Excluding only $t=1$:** the equation $t^2=1$ also has the solution $t=-1$.
- **Writing $\det A(t)=1+t^2$:** the product of the off-diagonal entries is subtracted.
- **Treating the formula as valid everywhere:** the formula is meaningful only where the determinant is nonzero, and this restriction must be stated with it.

---

## Oral Explanation (3 sentences)

The determinant of $A(t)$ is $1-t^2$, which is zero only for $t=1$ and $t=-1$, so the matrix is invertible for all other values of $t$. For those values the $2\times2$ formula gives $A(t)^{-1}=\frac{1}{1-t^2}$ times the matrix with rows $(1,-t)$ and $(-t,1)$. At $t=\pm1$ this formula would divide by zero, which reflects the fact that the rows of $A(t)$ become dependent and the matrix loses its inverse.

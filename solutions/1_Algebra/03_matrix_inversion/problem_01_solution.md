# Exercise 1 — Definition of the Inverse

## The Problem

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

---

## What Are We Looking For?

We want to decide whether $B$ is the inverse of $A$ by checking the definition directly, through two matrix products, without using any formula for the inverse.

---

## Idea and Theorem Before the Calculation

**Definition of the inverse:** A square matrix $B$ is the inverse of a square matrix $A$ of the same size if

$$
AB=I\qquad\mathrm{and}\qquad BA=I.
$$

In that case we write $B=A^{-1}$. Both products must be checked against the definition, because matrix multiplication is in general not commutative.

---

## Step-by-Step Solution

**Step 1: Compute $AB$.**

$$
AB=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
2\cdot1+1\cdot(-1) & 2\cdot(-1)+1\cdot2 \\
1\cdot1+1\cdot(-1) & 1\cdot(-1)+1\cdot2 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 2: Compute $BA$.**

$$
BA=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1\cdot2+(-1)\cdot1 & 1\cdot1+(-1)\cdot1 \\
-1\cdot2+2\cdot1 & -1\cdot1+2\cdot1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 3: Compare with the definition.**

Both products equal the identity matrix $I$. This is exactly the condition in the definition, so

$$
B=A^{-1}.
$$

*Why this is valid:* The definition of the inverse requires nothing more than $AB=I$ and $BA=I$, and both have been verified.

---

## Final Answer in Words

$AB=I$ and $BA=I$, so $B$ is the inverse of $A$. No formula was needed: the definition of the inverse was checked directly by multiplication.

---

## Quick Verification

An inverse must undo the action of $A$ on any vector. Take $x=(1,0)^T$. Then $Ax=(2,1)^T$, and

$$
B
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix} =
\begin{pmatrix}
2-1 \\
-2+2 \\
\end{pmatrix} =
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix},
$$

which returns the original vector, as expected.

---

## Common Mistakes

- **Checking only one product:** for square matrices one product equal to $I$ does in fact imply the other, but this is a theorem; the definition states both conditions, and this exercise asks for both.
- **Inverting entry by entry:** the inverse is not the matrix of reciprocals $\frac12,1,1,1$.
- **Confusing $I$ with a matrix of ones:** the identity has ones on the diagonal and zeros elsewhere.

---

## Oral Explanation (3 sentences)

A matrix $B$ is the inverse of $A$ exactly when multiplying them in either order gives the identity matrix. Computing both products here gives $AB=I$ and $BA=I$, so $B=A^{-1}$ without any formula. In other words, $B$ undoes whatever $A$ does, and $A$ undoes whatever $B$ does.

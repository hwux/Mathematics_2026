# Exercise 8 — Determinant of a Product

## The Problem

Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

---

## What Are We Looking For?

We need three determinants of products, computed from $\det A$ and $\det B$ only, and an explanation of why the order of the factors does not matter for the determinant.

---

## Idea and Theorem Before the Calculation

We assume that $A$ and $B$ have the same size $n\times n$, otherwise the products $AB$ and $BA$ are not both defined.

**Product rule:** $\det(AB)=\det A\cdot\det B$.

**Inverse rule:** If $A$ is invertible, then $\det(A^{-1})=\dfrac{1}{\det A}$.

This follows from the product rule: $A^{-1}A=I$, so $\det(A^{-1})\det A=\det I=1$.

---

## Step-by-Step Solution

**Step 1: $\det(AB)$.**

$$
\det(AB) = \det A\cdot\det B = 3\cdot(-5) = -15.
$$

**Step 2: $\det(BA)$.**

$$
\det(BA) = \det B\cdot\det A = (-5)\cdot3 = -15.
$$

**Step 3: Does $A^{-1}$ exist?**

$\det A=3\neq0$, so $A$ is invertible and $A^{-1}B$ is defined.

**Step 4: $\det(A^{-1}B)$.**

$$
\det(A^{-1}B) = \det(A^{-1})\cdot\det B = \frac{1}{3}\cdot(-5) = -\frac{5}{3}.
$$

*Why this is valid:* The product rule is applied to the factors $A^{-1}$ and $B$, and the inverse rule gives $\det(A^{-1})=\frac13$.

**Step 5: Why $\det(AB)=\det(BA)$.**

The matrices $AB$ and $BA$ are usually different. Their determinants, however, are both products of the two *numbers* $\det A$ and $\det B$. Multiplication of numbers is commutative, so

$$
\det A\cdot\det B = \det B\cdot\det A.
$$

The determinant forgets the order of the factors, even though the matrix product remembers it.

---

## Final Answer in Words

$\det(AB)=-15$, $\det(BA)=-15$ and $\det(A^{-1}B)=-\frac53$. The first two are equal because each is the product of the numbers $3$ and $-5$, and numbers commute even when matrices do not.

---

## Quick Verification

Take

$$
A=
\begin{pmatrix}
3 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
-5 & 0 \\
0 & 1 \\
\end{pmatrix},
$$

so $\det A=3$ and $\det B=-5$. Then

$$
AB=
\begin{pmatrix}
-15 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad BA=
\begin{pmatrix}
-15 & -5 \\
0 & 1 \\
\end{pmatrix}.
$$

The matrices are different, but both determinants equal $-15\cdot1-0=-15$. This illustrates the explanation in Step 5.

---

## Common Mistakes

- **Concluding $AB=BA$ from $\det(AB)=\det(BA)$:** equal determinants do not mean equal matrices.
- **Writing $\det(A^{-1})=-\det A$:** the determinant of the inverse is the reciprocal $\frac{1}{\det A}$, not the opposite number.
- **Skipping the existence check:** $A^{-1}$ exists only because $\det A\neq0$; this must be stated before using it.

---

## Oral Explanation (3 sentences)

The determinant of a product is the product of the determinants, so $\det(AB)=3\cdot(-5)=-15$ and $\det(BA)=(-5)\cdot3=-15$. These are equal because the determinant turns matrices into numbers, and numbers can be multiplied in any order even though matrices usually cannot. Since $\det A\neq0$, the inverse $A^{-1}$ exists, its determinant is $\frac13$, and therefore $\det(A^{-1}B)=-\frac53$.

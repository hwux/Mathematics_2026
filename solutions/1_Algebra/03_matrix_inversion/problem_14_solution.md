# Exercise 14 — A Matrix That Is Its Own Inverse

## The Problem

Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

---

## What Are We Looking For?

We want a short proof, based only on the definition of the inverse, that $A^2=I$ forces $A$ to be its own inverse, and a concrete example other than the obvious $I$ and $-I$.

---

## Idea and Theorem Before the Calculation

**Definition of the inverse:** $B=A^{-1}$ means $AB=I$ and $BA=I$.

**Uniqueness:** An invertible matrix has only one inverse, so any matrix satisfying both conditions is *the* inverse.

---

## Step-by-Step Solution

**Step 1: Proof that $A^{-1}=A$.**

Take $B=A$ in the definition. Both required conditions read

$$
AB=AA=A^2=I,\qquad BA=AA=A^2=I.
$$

They hold by assumption. Therefore $A$ is invertible and its inverse is $A$ itself:

$$
A^{-1}=A.
$$

*Why this is valid:* The definition of the inverse asks only for the two products to equal $I$, and both products here are $A^2$, which equals $I$.

**Step 2: Choose an example.**

Take the matrix that swaps the two coordinates:

$$
A=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

It maps $(x,y)^T$ to $(y,x)^T$, which is the reflection across the line $y=x$. It is clearly different from $I$ and from $-I$.

**Step 3: Verify by multiplication.**

$$
A^2=
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix} =
\begin{pmatrix}
0\cdot0+1\cdot1 & 0\cdot1+1\cdot0 \\
1\cdot0+0\cdot1 & 1\cdot1+0\cdot0 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

So $A^2=I$, and by Step 1 $A^{-1}=A$.

---

## Final Answer in Words

If $A^2=I$, then $A\cdot A=I$ in both orders, so $A$ satisfies the definition of its own inverse and $A^{-1}=A$. An example different from $\pm I$ is the coordinate swap with rows $(0,1)$ and $(1,0)$, which squares to $I$.

---

## Quick Verification

Geometrically, reflecting a point across the line $y=x$ twice brings it back: $(2,5)^T\mapsto(5,2)^T\mapsto(2,5)^T$. Doing the transformation twice is the identity, which is exactly the condition $A^2=I$.

Another example works in the same way: the reflection across the $x$-axis,

$$
\begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix},
$$

also satisfies the condition, since its square has diagonal entries $1^2=1$ and $(-1)^2=1$.

---

## Common Mistakes

- **Concluding that $A=I$ or $A=-I$:** the equation $A^2=I$ has many more solutions among matrices than $x^2=1$ has among numbers.
- **Proving $A^{-1}=A$ by "dividing by $A$":** there is no matrix division; the argument must use the definition of the inverse.
- **Giving an example without verification:** the task explicitly requires computing $A^2$.

---

## Oral Explanation (3 sentences)

If $A^2=I$, then $A$ multiplied by $A$ gives the identity in both orders, which is exactly the definition of $A$ being the inverse of $A$, so $A^{-1}=A$. An example other than $I$ and $-I$ is the matrix that swaps the two coordinates, which reflects the plane across the line $y=x$. Reflecting twice returns every point to its starting position, and indeed multiplying this matrix by itself gives the identity.

# Exercise 12 — Finding Inverses Without Starting from Scratch

## The Problem

It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

---

## What Are We Looking For?

We know $A^{-1}$ but not $A$. We want three new inverses expressed directly through $A^{-1}$, using only properties of the inverse.

---

## Idea and Theorem Before the Calculation

For an invertible matrix $A$ and a number $c\neq0$:

1. **Scalar multiple:** $(cA)^{-1}=\frac1cA^{-1}$, because $(cA)\left(\frac1cA^{-1}\right)=\frac{c}{c}AA^{-1}=I$.
2. **Transpose:** $(A^T)^{-1}=(A^{-1})^T$, because $A^T(A^{-1})^T=(A^{-1}A)^T=I^T=I$.
3. **Power:** $(A^2)^{-1}=(A^{-1})^2$, because $A^2(A^{-1})^2=A(AA^{-1})A^{-1}=AA^{-1}=I$.

---

## Step-by-Step Solution

**Step 1: $(3A)^{-1}$.**

$$
(3A)^{-1}=\frac13A^{-1}=\frac13
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23 \\
\end{pmatrix}.
$$

*Why this is valid:* Scaling $A$ by $3$ is undone by scaling the inverse by $\frac13$.

**Step 2: $(A^T)^{-1}$.**

$$
(A^T)^{-1}=(A^{-1})^T=
\begin{pmatrix}
2 & -3 \\
-1 & 2 \\
\end{pmatrix}.
$$

*Why this is valid:* Transposition and inversion can be performed in either order.

**Step 3: $(A^2)^{-1}$.**

$$
(A^2)^{-1}=(A^{-1})^2=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
4+3 & -2-2 \\
-6-6 & 3+4 \\
\end{pmatrix} =
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix}.
$$

*Why this is valid:* $A^2=AA$, and by the inverse-of-a-product rule $(AA)^{-1}=A^{-1}A^{-1}$.

---

## Final Answer in Words

$(3A)^{-1}=\frac13A^{-1}$ has rows $(\frac23,-\frac13)$ and $(-1,\frac23)$. $(A^T)^{-1}=(A^{-1})^T$ has rows $(2,-3)$ and $(-1,2)$. $(A^2)^{-1}=(A^{-1})^2$ has rows $(7,-4)$ and $(-12,7)$. None of these required finding $A$.

---

## Quick Verification

As an independent check, recover $A$ by inverting $A^{-1}$. Since $\det(A^{-1})=4-3=1$,

$$
A=(A^{-1})^{-1}=
\begin{pmatrix}
2 & 1 \\
3 & 2 \\
\end{pmatrix},\qquad A^2=
\begin{pmatrix}
4+3 & 2+2 \\
6+6 & 3+4 \\
\end{pmatrix} =
\begin{pmatrix}
7 & 4 \\
12 & 7 \\
\end{pmatrix}.
$$

Then

$$
A^2(A^{-1})^2=
\begin{pmatrix}
7 & 4 \\
12 & 7 \\
\end{pmatrix}
\begin{pmatrix}
7 & -4 \\
-12 & 7 \\
\end{pmatrix} =
\begin{pmatrix}
49-48 & -28+28 \\
84-84 & -48+49 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},
$$

which confirms Step 3. Similarly, $(3A)\cdot\frac13A^{-1}=AA^{-1}=I$ confirms Step 1.

---

## Common Mistakes

- **Writing $(3A)^{-1}=3A^{-1}$:** the scalar must also be inverted, giving $\frac13$.
- **Forgetting to transpose:** $(A^T)^{-1}$ is the transpose of $A^{-1}$, not $A^{-1}$ itself.
- **Squaring entry by entry:** $(A^{-1})^2$ is the matrix product $A^{-1}A^{-1}$, not the matrix of squared entries.

---

## Oral Explanation (3 sentences)

Each requested inverse can be expressed through the known matrix $A^{-1}$: scaling $A$ by $3$ scales its inverse by $\frac13$, transposing $A$ transposes its inverse, and squaring $A$ squares its inverse. Applying these rules gives $(3A)^{-1}=\frac13A^{-1}$, $(A^T)^{-1}=(A^{-1})^T$, and $(A^2)^{-1}=(A^{-1})^2$, which has rows $(7,-4)$ and $(-12,7)$. Recovering $A$ and multiplying confirms these results, but the point is that the properties make finding $A$ unnecessary.

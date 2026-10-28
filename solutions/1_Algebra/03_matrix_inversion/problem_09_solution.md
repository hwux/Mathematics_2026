# Exercise 9 — Matrix Equation

## The Problem

Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

---

## What Are We Looking For?

We want an unknown $2\times2$ matrix $X$ with $AX=B$. Because matrix multiplication is not commutative, we must first decide where $A^{-1}$ goes.

---

## Idea and Theorem Before the Calculation

**Isolating $X$:** In $AX=B$ the matrix $A$ stands to the *left* of $X$. To remove it, multiply both sides on the left by $A^{-1}$:

$$
A^{-1}(AX)=A^{-1}B\quad\Longrightarrow\quad (A^{-1}A)X=A^{-1}B\quad\Longrightarrow\quad X=A^{-1}B.
$$

Multiplying on the right instead would give $AXA^{-1}=BA^{-1}$, which does not isolate $X$.

---

## Step-by-Step Solution

**Step 1: Decide the side.**

$A$ multiplies $X$ from the left, so $A^{-1}$ must also be applied from the left on both sides. The solution is $X=A^{-1}B$, not $BA^{-1}$.

**Step 2: Compute $A^{-1}$.**

$\det A=1\cdot1-2\cdot0=1$, so

$$
A^{-1}=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 3: Compute $X=A^{-1}B$.**

$$
X=
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} =
\begin{pmatrix}
3-4 & 1-8 \\
2 & 4 \\
\end{pmatrix} =
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
$$

*Why this is valid:* Associativity allows $A^{-1}(AX)=(A^{-1}A)X=IX=X$.

**Step 4: The wrong side for comparison.**

$$
BA^{-1}=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}
\begin{pmatrix}
1 & -2 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
3 & -5 \\
2 & 0 \\
\end{pmatrix}.
$$

This is a different matrix, so the choice of side really matters.

---

## Final Answer in Words

$A^{-1}$ must be applied from the left, because $A$ stands to the left of $X$. The solution is

$$
X=A^{-1}B=
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix}.
$$

---

## Quick Verification

$$
AX=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4 \\
\end{pmatrix} =
\begin{pmatrix}
-1+4 & -7+8 \\
2 & 4 \\
\end{pmatrix} =
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix} = B.
$$

For comparison, $A(BA^{-1})$ has top row $(3+4,\ -5+0)=(7,-5)$, which is not the top row of $B$, so $BA^{-1}$ does not solve the equation.

---

## Common Mistakes

- **Writing $X=BA^{-1}$:** this solves $XA=B$, a different equation.
- **"Dividing" by $A$:** there is no matrix division; one must state on which side $A^{-1}$ is multiplied.
- **Multiplying the two sides of the equation by $A^{-1}$ on different sides:** the same operation must be applied to both sides.

---

## Oral Explanation (3 sentences)

In the equation $AX=B$ the matrix $A$ stands to the left of $X$, so both sides must be multiplied by $A^{-1}$ from the left, which gives $X=A^{-1}B$. With $A^{-1}$ having rows $(1,-2)$ and $(0,1)$, this produces $X$ with rows $(-1,-7)$ and $(2,4)$, and multiplying by $A$ indeed returns $B$. The matrix $BA^{-1}$ is different and would solve the equation $XA=B$, which shows that the side on which the inverse is applied is essential.

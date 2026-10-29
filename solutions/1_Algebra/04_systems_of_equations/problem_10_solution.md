# Exercise 10 — A Polynomial Through Three Points

## The Problem

Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

---

## What Are We Looking For?

The unknowns are not $x$ and $y$ but the coefficients $a,b,c$ of the polynomial. Each point gives one linear condition on them, and we want the coefficients satisfying all three conditions.

---

## Idea and Theorem Before the Calculation

**Condition from a point:** The graph of $p$ passes through $(x_0,y_0)$ exactly when

$$
p(x_0)=y_0,\qquad\mathrm{that\ is}\qquad ax_0^2+bx_0+c=y_0.
$$

Since $x_0$ and $y_0$ are known numbers, this is a **linear** equation in the unknowns $a,b,c$.

---

## Step-by-Step Solution

**Step 1: Write one equation per point.**

$$
\begin{aligned}
(0,1):&\quad a\cdot0^2+b\cdot0+c=1, \\
(1,3):&\quad a\cdot1^2+b\cdot1+c=3, \\
(2,9):&\quad a\cdot2^2+b\cdot2+c=9.
\end{aligned}
$$

This gives the system

$$
\begin{cases}
c=1, \\
a+b+c=3, \\
4a+2b+c=9.
\end{cases}
$$

**Step 2: Augmented matrix in the order $a,b,c$.**

$$
\begin{pmatrix}
0 & 0 & 1 & \mid & 1 \\
1 & 1 & 1 & \mid & 3 \\
4 & 2 & 1 & \mid & 9 \\
\end{pmatrix}
$$

**Step 3: Eliminate.**

Swap $R_1\leftrightarrow R_2$ so that the first pivot is nonzero, then $R_3\leftarrow R_3-4R_1$:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & 0 & 1 & \mid & 1 \\
0 & -2 & -3 & \mid & -3 \\
\end{pmatrix}
$$

Swap $R_2\leftrightarrow R_3$ to reach row echelon form:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 3 \\
0 & -2 & -3 & \mid & -3 \\
0 & 0 & 1 & \mid & 1 \\
\end{pmatrix}
$$

**Step 4: Back substitution.**

$$
\begin{aligned}
c &= 1, \\
-2b-3c &= -3 \quad\Longrightarrow\quad -2b=0 \quad\Longrightarrow\quad b=0, \\
a+b+c &= 3 \quad\Longrightarrow\quad a=3-0-1=2.
\end{aligned}
$$

*Why this is valid:* There are three pivots for three unknowns, so the solution is unique, and back substitution finds it.

**Step 5: The polynomial.**

$$
p(x)=2x^2+1.
$$

---

## Final Answer in Words

The three points give a linear system in $a,b,c$ with the unique solution $a=2$, $b=0$, $c=1$, so the polynomial is $p(x)=2x^2+1$.

---

## Quick Verification

$$
p(0)=2\cdot0+1=1,\qquad p(1)=2\cdot1+1=3,\qquad p(2)=2\cdot4+1=9.
$$

All three points lie on the graph.

---

## Common Mistakes

- **Treating $x$ and $y$ as the unknowns:** here the coordinates are known numbers and the unknowns are $a,b,c$.
- **Forgetting the squares:** the point $(2,9)$ gives $4a$, not $2a$.
- **Concluding $b$ cannot be zero:** a coefficient of zero is a perfectly valid result, meaning the polynomial has no linear term.

---

## Oral Explanation (3 sentences)

Each point $(x_0,y_0)$ on the graph gives the equation $ax_0^2+bx_0+c=y_0$, which is linear in the unknown coefficients $a,b,c$. The three points produce a system whose first equation immediately gives $c=1$, and elimination with back substitution then gives $b=0$ and $a=2$. The polynomial $p(x)=2x^2+1$ indeed takes the values $1$, $3$, $9$ at $x=0,1,2$.

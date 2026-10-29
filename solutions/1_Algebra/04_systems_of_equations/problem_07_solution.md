# Exercise 7 — Choosing a Method Deliberately

## The Problem

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
$$

2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

---

## What Are We Looking For?

We want to match each situation with the method that exploits its structure, using two criteria: the shape of the coefficient matrix and the number of right-hand sides.

---

## Idea and Theorem Before the Calculation

**Available methods:**

- **Back substitution:** works directly on a triangular system, with no elimination at all.
- **Multiplication by a known inverse:** $x=A^{-1}b$ costs only one matrix-vector product per right-hand side, about $n^2$ multiplications for an $n\times n$ matrix.
- **Gaussian elimination with back substitution:** the standard method for one system with a general matrix.
- **Computing $A^{-1}$:** requires Gauss-Jordan elimination on $[A\mid I]$, which processes $n$ right-hand-side columns instead of one.

---

## Step-by-Step Solution

**Case 1: Triangular system. Method: back substitution.**

The coefficient matrix

$$
\begin{pmatrix}
2 & -1 \\
0 & 4 \\
\end{pmatrix}
$$

is already upper-triangular, so elimination is unnecessary. Solve from the bottom:

$$
\begin{aligned}
4y &= 8 \quad\Longrightarrow\quad y=2, \\
2x-y &= 3 \quad\Longrightarrow\quad 2x=3+2=5 \quad\Longrightarrow\quad x=\frac52.
\end{aligned}
$$

*Why this choice:* The zero below the diagonal means that the last equation already contains only one unknown. Computing an inverse or performing elimination would only repeat work that the structure has already done.

**Case 2: Three right-hand sides, $A^{-1}$ known. Method: multiply by $A^{-1}$.**

Plan:

$$
x_1=A^{-1}b_1,\qquad x_2=A^{-1}b_2,\qquad x_3=A^{-1}b_3.
$$

- **Reusable:** the matrix $A^{-1}$, used for all three systems.
- **Unnecessary:** any elimination on $A$; the expensive part has already been done.
- **Cost:** three matrix-vector products, each about $n^2$ multiplications.

*Why this choice:* Elimination would repeat the same operations on $A$ three times, while the known inverse turns each system into a single product.

**Case 3: One $3\times3$ system, no inverse given. Method: Gaussian elimination on $[A\mid b]$, then back substitution.**

Plan: reduce the $3\times4$ augmented matrix $[A\mid b]$ to row echelon form and solve from the bottom.

- **Unnecessary:** computing $A^{-1}$. Gauss-Jordan on $[A\mid I]$ would carry three extra columns through every row operation, clear the entries above the pivots as well, and still require the product $A^{-1}b$ at the end.
- **Reusable:** nothing needs to be reused, since there is only one right-hand side; elimination handles $b$ at the same time as $A$.

*Why this choice:* For one right-hand side, elimination solves the system directly, and the inverse would be extra work producing information that is never used.

---

## Final Answer in Words

1. The triangular system is solved by back substitution alone: $y=2$, $x=\frac52$.
2. With $A^{-1}$ known and three right-hand sides, the best method is to compute $A^{-1}b_i$ three times; the inverse is the reusable part, and elimination is unnecessary.
3. For a single $3\times3$ system without a given inverse, Gaussian elimination on $[A\mid b]$ is best; computing $A^{-1}$ would be unnecessary extra work.

---

## Quick Verification

Case 1: substitute $(x,y)=(\frac52,2)$:

$$
2\cdot\frac52-2=5-2=3,\qquad 4\cdot2=8.
$$

Both equations hold.

For cases 2 and 3, the plans are consistent with the cost comparison: in case 2 the inverse already exists, so three products are cheaper than three eliminations; in case 3 one elimination on four columns is cheaper than one Gauss-Jordan elimination on six columns followed by a product.

---

## Common Mistakes

- **Always computing the inverse:** for a single system the inverse is more work than elimination.
- **Ignoring a known inverse:** when $A^{-1}$ is given, solving each system by elimination wastes the available information.
- **Eliminating a system that is already triangular:** back substitution can start immediately.

---

## Oral Explanation (3 sentences)

A triangular system needs no elimination at all, so back substitution solves it immediately, giving $y=2$ and $x=\frac52$. When the inverse of $A$ is already known and there are three right-hand sides, each solution is a single product $A^{-1}b_i$, and the inverse is the part that is reused. For one general $3\times3$ system without a given inverse, Gaussian elimination on $[A\mid b]$ is the most economical, because computing $A^{-1}$ would require extra work that a single right-hand side never repays.

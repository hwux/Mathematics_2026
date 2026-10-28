# Exercise 15 — Associativity of Multiplication and Different Calculation Paths

## The Problem

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

---

## What Are We Looking For?

We want to compute the same triple product along two different paths, confirm that the results agree, and count how much work each path requires.

---

## Idea and Theorem Before the Calculation

**Associativity:** For matrices of compatible sizes,

$$
(AB)C=A(BC).
$$

The placement of brackets does not affect the result, but it does affect the sizes of the intermediate matrices and therefore the amount of computation.

**Cost of one product:** Multiplying an $m\times k$ matrix by a $k\times n$ matrix produces $mn$ entries, each requiring $k$ multiplications and $k-1$ additions, so in total $mnk$ multiplications and $mn(k-1)$ additions.

**Sizes here:** $A$ is $2\times3$, $B$ is $3\times2$, $C$ is $2\times2$. The result is $2\times2$ on both paths.

---

## Step-by-Step Solution

**Step 1: Compute $AB$ ($2\times3$ times $3\times2$).**

$$
AB=
\begin{pmatrix}
1\cdot1+2\cdot2+0\cdot(-1) & 1\cdot0+2\cdot1+0\cdot3 \\
0\cdot1+1\cdot2+1\cdot(-1) & 0\cdot0+1\cdot1+1\cdot3 \\
\end{pmatrix} =
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}.
$$

**Step 2: Compute $(AB)C$ ($2\times2$ times $2\times2$).**

$$
(AB)C=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix} =
\begin{pmatrix}
10+0 & 5-2 \\
2+0 & 1-4 \\
\end{pmatrix} =
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

**Step 3: Compute $BC$ ($3\times2$ times $2\times2$).**

$$
BC=
\begin{pmatrix}
1\cdot2+0\cdot0 & 1\cdot1+0\cdot(-1) \\
2\cdot2+1\cdot0 & 2\cdot1+1\cdot(-1) \\
-1\cdot2+3\cdot0 & -1\cdot1+3\cdot(-1) \\
\end{pmatrix} =
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}.
$$

**Step 4: Compute $A(BC)$ ($2\times3$ times $3\times2$).**

$$
A(BC)=
\begin{pmatrix}
1\cdot2+2\cdot4+0\cdot(-2) & 1\cdot1+2\cdot1+0\cdot(-4) \\
0\cdot2+1\cdot4+1\cdot(-2) & 0\cdot1+1\cdot1+1\cdot(-4) \\
\end{pmatrix} =
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

*Why this is valid:* Every product is defined because the inner sizes match at each step, and each entry is a row-times-column sum.

**Step 5: Count the operations.**

| Path | Products | Multiplications | Additions |
|------|----------|-----------------|-----------|
| $(AB)C$ | $AB$: $2\cdot2\cdot3$; then $(AB)C$: $2\cdot2\cdot2$ | $12+8=20$ | $8+4=12$ |
| $A(BC)$ | $BC$: $3\cdot2\cdot2$; then $A(BC)$: $2\cdot2\cdot3$ | $12+12=24$ | $6+8=14$ |

The path $(AB)C$ is cheaper, because its intermediate result $AB$ is only $2\times2$, while $BC$ is $3\times2$.

---

## Final Answer in Words

Both paths give

$$
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

The path $(AB)C$ needs $20$ multiplications and $12$ additions, the path $A(BC)$ needs $24$ multiplications and $14$ additions. Associativity guarantees the same result regardless of the brackets, so one may choose the bracketing that makes the calculation shorter.

---

## Quick Verification

Check one entry by expanding the triple product directly. The entry in position $(2,2)$ of $ABC$ is the sum over all $j,k$ of $a_{2j}b_{jk}c_{k2}$. Using row $2$ of $A$, $(0,1,1)$, and column $2$ of $C$, $(1,-1)^T$:

$$
\sum_{j,k} a_{2j}b_{jk}c_{k2} = 1\cdot\left(b_{21}\cdot1+b_{22}\cdot(-1)\right)+1\cdot\left(b_{31}\cdot1+b_{32}\cdot(-1)\right) = (2-1)+(-1-3) = -3.
$$

This matches the entry $-3$ obtained on both paths.

---

## Common Mistakes

- **Confusing associativity with commutativity:** associativity allows moving the brackets, not changing the order of $A$, $B$, $C$.
- **Assuming both paths cost the same:** the intermediate sizes differ, and so does the amount of work.
- **Arithmetic slips with negative entries:** entries such as $-1\cdot1+3\cdot(-1)=-4$ in $BC$ deserve a second look.

---

## Oral Explanation (3 sentences)

Computing $AB$ first and then multiplying by $C$ gives the same matrix, with rows $(10,3)$ and $(2,-3)$, as computing $BC$ first and then multiplying by $A$, which is what associativity of matrix multiplication guarantees. The brackets do change the intermediate results: $AB$ is a small $2\times2$ matrix, while $BC$ is $3\times2$, so the first path needs $20$ multiplications instead of $24$. Associativity therefore lets us choose the cheapest order of evaluation without changing the answer, as long as the order of the factors themselves stays the same.

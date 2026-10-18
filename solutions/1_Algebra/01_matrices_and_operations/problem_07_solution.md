# Exercise 7 — Identity Matrix, Zero Matrix, and Powers

## The Problem

For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

---

## What Are We Looking For?

We want to see how the identity matrix $I$ and the zero matrix $0$ interact with $A$ (acting as neutral elements), and to discover a pattern in the powers $A^2, A^3, \ldots$.

---

## Idea and Theorem Before the Calculation

**Identity matrix $I$:** The $n\times n$ identity matrix has $1$ on the main diagonal and $0$ everywhere else. It satisfies $AI = IA = A$ for every square matrix $A$ of the same size — it is the neutral element for multiplication.

**Zero matrix $0$:** The matrix with all entries equal to $0$. It satisfies $A + 0 = A$ — it is the neutral element for addition.

**Matrix power:** $A^2 = AA$, $A^3 = A^2 A = AAA$, and so on. Only square matrices can be raised to powers.

For a $2\times2$ matrix we write

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad
0=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}.
$$

---

## Step-by-Step Solution

**Step 1 — Compute $AI$.**

$$
AI=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
2\cdot1+1\cdot0 & 2\cdot0+1\cdot1 \\
0\cdot1+2\cdot0 & 0\cdot0+2\cdot1 \\
\end{pmatrix} =
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
= A.
$$

**Step 2 — Compute $IA$.**

$$
IA=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
1\cdot2+0\cdot0 & 1\cdot1+0\cdot2 \\
0\cdot2+1\cdot0 & 0\cdot1+1\cdot2 \\
\end{pmatrix} =
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
= A.
$$

*Why valid:* $I$ leaves every matrix unchanged because multiplying by it is equivalent to forming a linear combination of the columns of $A$ with weights given by the columns of $I$, which are the standard basis vectors.

**Step 3 — Compute $A + 0$.**

Adding the zero matrix changes nothing:

$$
A+0=
\begin{pmatrix}
2+0 & 1+0 \\
0+0 & 2+0 \\
\end{pmatrix} =
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
= A.
$$

**Step 4 — Compute $A^2$.**

$$
A^2=AA=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
4+0 & 2+2 \\
0+0 & 0+4 \\
\end{pmatrix} =
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}.
$$

**Step 5 — Compute $A^3$.**

$$
A^3=A^2 A=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
8+0 & 4+8 \\
0+0 & 0+8 \\
\end{pmatrix} =
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
$$

*Why valid:* Powers are computed by repeated multiplication, using the result of the previous step as the left factor.

**Step 6 — Observe the pattern.**

Arranging the powers:

$$
A^1=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},\quad
A^2=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix},\quad
A^3=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
$$

The diagonal entries are $2^n$ in $A^n$. The off-diagonal entry (top-right) is $n\cdot 2^{n-1}$: for $n=1$ it is $1$, for $n=2$ it is $4$, for $n=3$ it is $12$. The bottom-left entry stays $0$ because the lower-triangular structure is preserved under multiplication.

The general formula is

$$
A^n=
\begin{pmatrix}
2^n & n\cdot2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
$$

---

## Final Answer in Words

$AI = IA = A$ and $A + 0 = A$, confirming that $I$ is the neutral element for multiplication and $0$ is the neutral element for addition. The powers follow the pattern

$$
A^n=
\begin{pmatrix}
2^n & n\cdot2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
$$

---

## Quick Verification

Check $A^3$ using the formula: diagonal entries $= 2^3 = 8$; top-right entry $= 3\cdot2^2 = 12$; bottom-left $= 0$. This matches the directly computed $A^3$ above.

Also verify $A^2$ from the formula: diagonal $=4$, top-right $= 2\cdot2 = 4$, confirmed.

---

## Common Mistakes

- **Squaring entry by entry:** $A^2$ is not obtained by squaring each entry individually (which would incorrectly yield diagonal entries $4, 4$ and off-diagonal $1, 0$). Matrix powers must always be computed using standard matrix multiplication $AA$.
- **Assuming $AI \neq IA$:** unlike general matrix products, $I$ commutes with every square matrix of the same size.
- **Failing to see the pattern:** compute a few powers before guessing the general formula, and always verify the formula for at least one additional value of $n$.

---

## Oral Explanation (3 sentences)

The identity matrix $I$ plays the same role in matrix multiplication as the number $1$ does in ordinary multiplication: multiplying any square matrix by $I$ on either side leaves it unchanged. Similarly, the zero matrix $0$ is the additive neutral element: adding it to any matrix leaves that matrix unchanged. In this exercise, the successive powers of $A$ reveal a clear pattern — the diagonal entries grow as $2^n$ and the off-diagonal entry grows as $n\cdot2^{n-1}$ — which shows that even simple-looking matrices can produce rich structure when raised to higher powers.


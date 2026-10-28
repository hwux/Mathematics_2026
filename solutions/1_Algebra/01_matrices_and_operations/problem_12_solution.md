# Exercise 12 — Formula for a Matrix Power

## The Problem

Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

---

## What Are We Looking For?

We want a closed formula for every power $A^n$. A few powers suggest the formula; an inductive step then shows that it holds for all $n\ge1$, not only for the cases computed.

---

## Idea and Theorem Before the Calculation

**Powers:** $A^{n+1}=A^nA$.

**Principle of mathematical induction:** A statement $P(n)$ holds for every $n\ge1$ if

1. $P(1)$ is true (base case), and
2. whenever $P(n)$ is true, $P(n+1)$ is also true (inductive step).

---

## Step-by-Step Solution

**Step 1: Compute $A^2$.**

$$
A^2=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 1+1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 2: Compute $A^3$.**

$$
A^3=A^2A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 1+2 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 3: Compute $A^4$.**

$$
A^4=A^3A=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 1+3 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}.
$$

**Step 4: Conjecture.**

The diagonal entries stay $1$, the bottom-left entry stays $0$, and the top-right entry equals the exponent. The conjecture is

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix},\qquad n\ge1.
$$

**Step 5: Base case.**

For $n=1$ the formula gives a matrix with top-right entry $1$, which is exactly $A$, so it is true.

**Step 6: Inductive step.**

Assume the formula holds for some $n$. Then

$$
A^{n+1}=A^nA=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1\cdot1+n\cdot0 & 1\cdot1+n\cdot1 \\
0\cdot1+1\cdot0 & 0\cdot1+1\cdot1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & n+1 \\
0 & 1 \\
\end{pmatrix}.
$$

This is exactly the formula with $n$ replaced by $n+1$.

*Why this is valid:* The base case starts the chain, and the inductive step shows that each case implies the next one, so the formula holds for $n=1,2,3,\ldots$ without exception.

**Why the pattern appears:** Multiplying by $A$ on the right adds the first column to the second column. The first column is always $(1,0)^T$, so each multiplication adds exactly $1$ to the top-right entry and changes nothing else.

---

## Final Answer in Words

$A^2$, $A^3$ and $A^4$ have top-right entries $2$, $3$ and $4$, with all other entries unchanged. This leads to the formula

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix},
$$

which is proved for all $n\ge1$: it holds for $n=1$, and multiplying the formula for $n$ by $A$ gives exactly the formula for $n+1$.

---

## Quick Verification

Compute $A^5$ in a different way, as $A^2A^3$:

$$
A^2A^3=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 3+2 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 5 \\
0 & 1 \\
\end{pmatrix}.
$$

This agrees with the formula for $n=5$. It also shows the rule $A^mA^k=A^{m+k}$ in action: the top-right entries simply add, $2+3=5$.

---

## Common Mistakes

- **Stopping at a conjecture:** checking $n=2,3,4$ makes the formula plausible, but only the inductive step proves it for every $n$.
- **Assuming the formula for $n+1$ inside the inductive step:** the step must start from the case $n$ and *derive* the case $n+1$.
- **Raising entries to the power $n$:** entrywise powers would give top-right entry $1^n=1$, which is wrong.

---

## Oral Explanation (3 sentences)

Computing $A^2$, $A^3$ and $A^4$ shows that only the top-right entry changes, and it equals the exponent, which suggests that $A^n$ has the same form as $A$ with top-right entry $n$. If this formula holds for some $n$, multiplying it by $A$ adds $1$ to the top-right entry and leaves the rest unchanged, so the formula holds for $n+1$ as well. Together with the obvious case $n=1$, induction proves the formula for every positive integer $n$.

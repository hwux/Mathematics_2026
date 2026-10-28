# Exercise 14 — A System of Equations and the Determinant

## The Problem

Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

---

## What Are We Looking For?

We want to separate the values of $k$ into two groups: those for which every right-hand side gives exactly one solution, and the exceptional value, for which the behaviour depends on $b$. For the exceptional value we need two concrete right-hand sides.

---

## Idea and Theorem Before the Calculation

**Determinant and unique solvability:** For a square matrix $A$, the system $Ax=b$ has exactly one solution for every $b$ if and only if $\det A\neq0$. In that case the solution is $x=A^{-1}b$.

**When $\det A=0$:** The system has either no solution or infinitely many, depending on $b$. It never has exactly one solution.

---

## Step-by-Step Solution

**Step 1: Compute the determinant.**

$$
\det A = 1\cdot4-2\cdot k = 4-2k.
$$

**Step 2: Find when it is zero.**

$$
4-2k=0 \quad\Longleftrightarrow\quad k=2.
$$

So for every $k\neq2$ the system has exactly one solution for every $b$.

*Why this is valid:* For $k\neq2$ the determinant is nonzero, $A$ is invertible, and $x=A^{-1}b$ is the only solution.

**Step 3: Study the exceptional value $k=2$.**

For $k=2$, with $b=(b_1,b_2)^T$, the system reads

$$
\begin{cases}
x_1+2x_2=b_1, \\
2x_1+4x_2=b_2.
\end{cases}
$$

The left side of the second equation is exactly twice the left side of the first. The system is therefore consistent only if the right sides have the same relation, $b_2=2b_1$.

**Step 4: A right-hand side with infinitely many solutions.**

Take $b=(1,2)^T$. Then $b_2=2b_1$, and the second equation is just twice the first, so only one condition remains:

$$
x_1+2x_2=1.
$$

Choosing $x_2=s$ freely gives

$$
x=
\begin{pmatrix}
1-2s \\
s \\
\end{pmatrix},\qquad s\in\mathbb{R},
$$

which is infinitely many solutions.

**Step 5: A right-hand side with no solution.**

Take $b=(1,0)^T$. The first equation gives $x_1+2x_2=1$, so $2x_1+4x_2=2$. The second equation demands $2x_1+4x_2=0$. Since $2\neq0$, no vector $x$ satisfies both equations.

---

## Final Answer in Words

The system has exactly one solution for every $b$ precisely when $k\neq2$, because then $\det A=4-2k\neq0$. For $k=2$ the right-hand side $b=(1,2)^T$ gives infinitely many solutions $x=(1-2s,s)^T$, and $b=(1,0)^T$ gives no solution.

---

## Quick Verification

For $k=2$ and $b=(1,2)^T$, take $s=0$ and $s=1$, giving $x=(1,0)^T$ and $x=(-1,1)^T$:

- $(1,0)^T$: $1+0=1$ and $2+0=2$;
- $(-1,1)^T$: $-1+2=1$ and $-2+4=2$.

Both vectors solve the system, so the solution is indeed not unique. For a regular value, for example $k=0$, the determinant is $4\neq0$, and the system $x_1+2x_2=b_1$, $4x_2=b_2$ can be solved uniquely from the bottom up for any $b$.

---

## Common Mistakes

- **Thinking $\det A=0$ always means "no solution":** depending on $b$, there may be infinitely many solutions instead.
- **Choosing an inconsistent $b$ for the infinite case:** the right-hand side must satisfy the same relation as the rows, here $b_2=2b_1$.
- **Answering only $k=2$:** the question asks for the values with a unique solution, which are all $k\neq2$.

---

## Oral Explanation (3 sentences)

The system $Ax=b$ has exactly one solution for every right-hand side precisely when $\det A=4-2k$ is nonzero, that is, for all $k\neq2$. For $k=2$ the second row of $A$ is twice the first, so the system is solvable only when $b_2=2b_1$. With $b=(1,2)^T$ the two equations coincide and give infinitely many solutions, while with $b=(1,0)^T$ they contradict each other and there is no solution.

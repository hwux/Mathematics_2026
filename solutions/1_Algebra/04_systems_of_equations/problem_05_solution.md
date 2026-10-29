# Exercise 5 — Row Echelon Form and Number of Solutions

## The Problem

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

---

## What Are We Looking For?

The matrix is already in row echelon form. We want to read off directly whether the system has solutions, how many variables are free, and the complete solution set.

---

## Idea and Theorem Before the Calculation

For a system in row echelon form with $n$ unknowns:

1. If some row reads $(0\ \cdots\ 0\mid c)$ with $c\neq0$, there is no solution.
2. Otherwise, if $r$ is the number of pivots, then the number of free variables is

$$
n-r.
$$

If $n-r=0$ there is exactly one solution; if $n-r>0$ there are infinitely many.

Call the unknowns $x_1,x_2,x_3$.

---

## Step-by-Step Solution

**Step 1: Check for a contradiction.**

The only zero row on the left is $(0\ 0\ 0\mid0)$, which means $0=0$. There is no row of the form $(0\ 0\ 0\mid c)$ with $c\neq0$, so the system is consistent.

**Step 2: Count the pivots and the free variables.**

The pivots are the leading $1$ in row 1 (column of $x_1$) and the leading $1$ in row 2 (column of $x_2$), so $r=2$. With $n=3$ unknowns,

$$
n-r=3-2=1
$$

variable is free, namely $x_3$, whose column has no pivot. Hence the system has infinitely many solutions.

**Step 3: Back substitution.**

Set $x_3=s$. Then

$$
\begin{aligned}
x_2+2x_3 &= 1 \quad\Longrightarrow\quad x_2=1-2s, \\
x_1+2x_2-x_3 &= 3 \quad\Longrightarrow\quad x_1=3-2(1-2s)+s=1+5s.
\end{aligned}
$$

*Why this is valid:* The pivot variables are expressed through the free variable from the bottom row upward.

**Step 4: Parametric form.**

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
\end{pmatrix} =
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}+s
\begin{pmatrix}
5 \\
-2 \\
1 \\
\end{pmatrix},\qquad s\in\mathbb{R}.
$$

---

## Final Answer in Words

The system has infinitely many solutions, $x_1=1+5s$, $x_2=1-2s$, $x_3=s$ for any real $s$. Exactly one variable is free, because there are $3$ unknowns and $2$ pivots, and the pivot-free column belongs to $x_3$.

---

## Quick Verification

Substitute the general solution into the two nonzero rows:

$$
\begin{aligned}
(1+5s)+2(1-2s)-s &= 1+5s+2-4s-s = 3, \\
(1-2s)+2s &= 1.
\end{aligned}
$$

Both equations hold for every $s$, not just for one chosen value. For example, $s=1$ gives $(6,-1,1)$: $6-2-1=3$ and $-1+2=1$.

---

## Common Mistakes

- **Counting rows instead of pivots:** the matrix has three rows, but only two pivots, because the third row is zero.
- **Choosing a pivot variable as free:** the free variable must be the one whose column has no pivot; choosing $x_1$ free is possible in principle but makes the back substitution harder and is not what the echelon form suggests.
- **Forgetting the sign in back substitution:** $x_1=3-2x_2+x_3$, and the term $-x_3$ moves to the right side as $+x_3$.

---

## Oral Explanation (3 sentences)

The matrix is in row echelon form, and its zero row means $0=0$, so the system is consistent. There are three unknowns but only two pivots, so exactly $3-2=1$ variable is free, namely $x_3$, whose column has no pivot. Setting $x_3=s$ and substituting upward gives $x_2=1-2s$ and $x_1=1+5s$, a whole line of solutions.

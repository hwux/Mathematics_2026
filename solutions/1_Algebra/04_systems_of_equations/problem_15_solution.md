# Exercise 15 — Classifying Three Systems

## The Problem

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

---

## What Are We Looking For?

We want to classify three similar systems with the smallest possible amount of work: one elimination step each, followed by reading off the type from the resulting second row.

---

## Idea and Theorem Before the Calculation

After eliminating $x$ from the second equation of a $2\times2$ system, the second row has one of three forms:

| Second row | Meaning | Type |
|------------|---------|------|
| $(0\ \ d\mid e)$ with $d\neq0$ | $y$ is determined | exactly one solution |
| $(0\ \ 0\mid0)$ | $0=0$, one condition remains | infinitely many solutions |
| $(0\ \ 0\mid e)$ with $e\neq0$ | $0=e$ | no solution |

---

## Step-by-Step Solution

**System 1: $R_2\leftarrow R_2-R_1$.**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -2 & \mid & -2 \\
\end{pmatrix}
$$

The second row has the pivot $-2\neq0$. Both columns have pivots, so there is **exactly one solution**. Completing the calculation: $y=1$, $x=1$.

**System 2: $R_2\leftarrow R_2-2R_1$.**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

The second row is $0=0$. Only the condition $x+y=2$ remains, so $y=s$ is free and there are **infinitely many solutions**, $(2-s,s)$ for $s\in\mathbb{R}$.

**System 3: $R_2\leftarrow R_2-2R_1$.**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

The second row is $0=1$, a contradiction. There is **no solution**.

*Why this is enough:* In each case one elimination step already produced the deciding second row; further calculation is needed only to write down the solutions.

**Comparison.**

Systems 2 and 3 have the same coefficient matrix, whose second row is twice the first, so their left sides are proportional. The type is then decided by the right-hand side: $4=2\cdot2$ gives a redundant equation, while $5\neq2\cdot2$ gives a contradiction. In System 1 the rows $(1,1)$ and $(1,-1)$ are not proportional, so a pivot appears in the second column regardless of the right-hand side.

---

## Final Answer in Words

System 1 has exactly one solution, $(1,1)$, because the second row keeps a nonzero pivot. System 2 has infinitely many solutions, $(2-s,s)$, because its second equation is twice the first and becomes $0=0$. System 3 has no solution, because its left side is twice the first equation but its right side is not, which gives $0=1$.

---

## Quick Verification

- System 1: $(1,1)$ gives $1+1=2$ and $1-1=0$.
- System 2: $(0,2)$ and $(2,0)$ both satisfy $x+y=2$ and $2x+2y=4$, so the solution is not unique.
- System 3: any $(x,y)$ with $x+y=2$ gives $2x+2y=4\neq5$, so no point satisfies both equations.

Geometrically, System 1 describes two crossing lines, System 2 one line written twice, and System 3 two parallel distinct lines.

---

## Common Mistakes

- **Solving completely before classifying:** the type is visible after a single elimination step.
- **Classifying from the coefficients alone:** Systems 2 and 3 have the same coefficients but different types.
- **Treating $0=0$ and $0=1$ alike:** the first removes a condition, the second makes the system impossible.

---

## Oral Explanation (3 sentences)

One elimination step is enough to classify each system: in System 1 the second row keeps a nonzero pivot, so there is exactly one solution, $(1,1)$. In Systems 2 and 3 the left side of the second equation is twice the first, so elimination removes both unknowns from the second row. The right-hand side then decides: System 2 gives $0=0$ and infinitely many solutions, while System 3 gives $0=1$ and no solution.

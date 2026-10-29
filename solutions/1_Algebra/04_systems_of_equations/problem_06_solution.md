# Exercise 6 — A System with a Parameter — Which Cases Actually Occur?

## The Problem

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

---

## What Are We Looking For?

We want to classify the system for every real value of $a$, and we must not assume in advance that all three types of behaviour appear.

---

## Idea and Theorem Before the Calculation

**Classification after elimination:**

- a row $(0\ 0\mid c)$ with $c\neq0$ means no solution;
- a row $(0\ 0\mid0)$ removes one condition, which leaves a free variable;
- a pivot in every column means exactly one solution.

**Determinant test for square systems:** exactly one solution for every right-hand side occurs if and only if $\det A\neq0$.

---

## Step-by-Step Solution

**Step 1: Augmented matrix.**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
a & a & \mid & 4 \\
\end{pmatrix}
$$

**Step 2: $R_2\leftarrow R_2-aR_1$.**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & 0 & \mid & 4-2a \\
\end{pmatrix}
$$

*Why this is valid:* This operation is allowed for every value of $a$, including $a=0$, because it only adds a multiple of the first row.

The left side of the second row is zero for **every** $a$. Only the right-hand side $4-2a$ depends on the parameter.

**Step 3: Case $a=2$.**

The second row becomes $(0\ 0\mid0)$, that is $0=0$. Only the equation $x+y=2$ remains, so $y=s$ is free and

$$
\begin{pmatrix}
x \\
y \\
\end{pmatrix} =
\begin{pmatrix}
2-s \\
s \\
\end{pmatrix},\qquad s\in\mathbb{R}.
$$

There are infinitely many solutions.

**Step 4: Case $a\neq2$.**

The second row reads $0=4-2a$ with $4-2a\neq0$, which is impossible. There is no solution. This includes $a=0$, where the second equation reads $0=4$ directly.

**Step 5: Why exactly one solution never occurs.**

The coefficient matrix

$$
\begin{pmatrix}
1 & 1 \\
a & a \\
\end{pmatrix}
$$

has determinant $a-a=0$ for every $a$. Its second row is always $a$ times the first, so elimination can never produce a second pivot. Without a pivot in the second column, $y$ can never be fixed uniquely, so exactly one solution is impossible.

---

## Final Answer in Words

For $a=2$ the system has infinitely many solutions $(2-s,s)$. For every $a\neq2$ it has no solution. The case of exactly one solution never occurs, because the left sides of the two equations are proportional for every $a$, so the coefficient matrix always has determinant $0$.

---

## Quick Verification

For $a=2$, take $s=0$ and $s=1$: the points $(2,0)$ and $(1,1)$ satisfy $x+y=2$ and $2x+2y=4$, so the system really has more than one solution.

For $a=1$, the system reads $x+y=2$ and $x+y=4$, which cannot both hold: the same sum cannot equal $2$ and $4$. This agrees with the case $a\neq2$.

Geometrically, for $a\neq0$ the second equation is the line $x+y=\frac4a$, which is parallel to $x+y=2$. The lines coincide only for $\frac4a=2$, that is $a=2$, and they can never cross at a single point.

---

## Common Mistakes

- **Assuming all three cases must appear:** the structure of the matrix rules out the unique case for every $a$.
- **Dividing the second equation by $a$:** this step is invalid for $a=0$, and the case $a=0$ would be lost; the row operation $R_2-aR_1$ avoids this problem.
- **Forgetting $a=0$:** it belongs to the case "no solution."

---

## Oral Explanation (3 sentences)

Subtracting $a$ times the first equation from the second gives the row $(0\ 0\mid4-2a)$, whose left side vanishes for every value of $a$. For $a=2$ this row is $0=0$ and the system has infinitely many solutions $(2-s,s)$, while for every other $a$ it is a contradiction and the system has no solution. Exactly one solution never occurs, because the two equations always have proportional left sides and therefore describe parallel or identical lines, never crossing ones.

# Exercise 4 — Infinitely Many Solutions

## The Problem

Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

---

## What Are We Looking For?

We want the complete solution set of a system that turns out to have infinitely many solutions, described with one parameter, and a check on one concrete point of this set.

---

## Idea and Theorem Before the Calculation

**Pivot and free variables:** After elimination, every column containing a pivot belongs to a **pivot variable**, and every other column belongs to a **free variable**. Free variables may take any value; the pivot variables are then determined by back substitution.

**Zero rows:** A row $(0\ 0\ 0\mid0)$ means $0=0$; it carries no information and does not restrict the solution.

---

## Step-by-Step Solution

**Step 1: Augmented matrix.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
2 & 2 & 2 & \mid & 4 \\
1 & -1 & 1 & \mid & 0 \\
\end{pmatrix}
$$

**Step 2: $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-R_1$.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & 0 & 0 & \mid & 0 \\
0 & -2 & 0 & \mid & -2 \\
\end{pmatrix}
$$

The second equation was twice the first, so it became $0=0$.

**Step 3: $R_2\leftrightarrow R_3$.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 2 \\
0 & -2 & 0 & \mid & -2 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

This is a row echelon form. The pivots are in the columns of $x$ and $y$; the column of $z$ has no pivot.

**Step 4: Choose the free variable.**

$z$ is free. Write $z=s$, where $s$ is any real number.

**Step 5: Back substitution.**

$$
\begin{aligned}
-2y &= -2 \quad\Longrightarrow\quad y=1, \\
x+y+z &= 2 \quad\Longrightarrow\quad x=2-1-s=1-s.
\end{aligned}
$$

*Why this is valid:* The two nonzero rows give two independent conditions for three unknowns, so exactly one unknown remains free.

**Step 6: Parametric form.**

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix} =
\begin{pmatrix}
1-s \\
1 \\
s \\
\end{pmatrix} =
\begin{pmatrix}
1 \\
1 \\
0 \\
\end{pmatrix}+s
\begin{pmatrix}
-1 \\
0 \\
1 \\
\end{pmatrix},\qquad s\in\mathbb{R}.
$$

---

## Final Answer in Words

The system has infinitely many solutions $x=1-s$, $y=1$, $z=s$, where $s$ is any real number and $z$ is the free variable. Geometrically, the solution set is a line through the point $(1,1,0)$ in the direction $(-1,0,1)$.

---

## Quick Verification

Choose $s=2$. The parametric form gives the point $(x,y,z)=(-1,1,2)$. Substituting:

$$
\begin{aligned}
-1+1+2 &= 2, \\
2\cdot(-1)+2\cdot1+2\cdot2 &= 4, \\
-1-1+2 &= 0.
\end{aligned}
$$

All three equations hold. The same works for $s=0$, which gives $(1,1,0)$: $1+1+0=2$, $2+2+0=4$, $1-1+0=0$.

---

## Common Mistakes

- **Concluding "no solution" from a zero row:** the row $(0\ 0\ 0\mid0)$ means $0=0$, which is always true.
- **Making $y$ depend on the parameter:** here $y=1$ for every solution, because the second pivot row fixes it.
- **Giving one solution instead of all:** the answer must describe the whole solution set, for every value of $s$.

---

## Oral Explanation (3 sentences)

The second equation is exactly twice the first, so elimination turns it into $0=0$ and only two real conditions remain for three unknowns. The column of $z$ has no pivot, so $z=s$ is free, and back substitution gives $y=1$ and $x=1-s$. Every value of $s$ gives a solution, for example $s=2$ gives $(-1,1,2)$, which satisfies all three equations.

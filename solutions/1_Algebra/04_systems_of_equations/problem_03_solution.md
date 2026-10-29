# Exercise 3 — Inconsistent System

## The Problem

Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

---

## What Are We Looking For?

We want to decide whether the system has a solution, and if not, show exactly where elimination produces an impossible equation.

---

## Idea and Theorem Before the Calculation

**Inconsistency test:** A system is inconsistent (has no solution) exactly when elimination produces a row of the form

$$
\begin{pmatrix}
0 & 0 & \mid & c \\
\end{pmatrix},\qquad c\neq0,
$$

which represents the equation $0=c$.

---

## Step-by-Step Solution

**Step 1: Augmented matrix.**

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
2 & 4 & \mid & 7 \\
\end{pmatrix}
$$

**Step 2: $R_2\leftarrow R_2-2R_1$.**

$$
\begin{pmatrix}
1 & 2 & \mid & 3 \\
0 & 0 & \mid & 1 \\
\end{pmatrix}
$$

*Why:* This removes $x$ from the second equation. The coefficient of $y$ disappears as well, because the left side of the second equation is exactly twice the left side of the first.

**Step 3: Read the second row as an equation.**

$$
0\cdot x+0\cdot y=1,\qquad\mathrm{that\ is}\qquad 0=1.
$$

No values of $x$ and $y$ can make this true, so the system has no solution.

*Why this is valid:* Row operations do not change the solution set. The new system contains an impossible equation, so its solution set is empty, and so is that of the original system.

**Step 4: Interpretation in terms of equations.**

Multiplying the first equation by $2$ gives $2x+4y=6$. The second equation demands $2x+4y=7$. The same expression cannot equal both $6$ and $7$, so the two equations contradict each other. Geometrically, the two equations describe parallel lines that never meet.

---

## Final Answer in Words

The system is inconsistent. After $R_2\leftarrow R_2-2R_1$ the second row becomes $(0\ 0\mid1)$, which means $0=1$. In terms of the equations, the first one forces $2x+4y=6$, while the second one demands $2x+4y=7$.

---

## Quick Verification

Write both equations in the form $y=\ldots$:

$$
y=\frac{3-x}{2},\qquad y=\frac{7-2x}{4}=\frac{3.5-x}{2}.
$$

Both lines have slope $-\frac12$ but different intercepts, $\frac32$ and $\frac74$. Parallel distinct lines have no common point, which confirms that the system has no solution.

---

## Common Mistakes

- **Ignoring the zero row:** a row $(0\ 0\mid1)$ is not "nothing"; it is the equation $0=1$.
- **Confusing $0=1$ with $0=0$:** the first means no solution, the second means the equation was redundant.
- **Trying to solve for $y$ by dividing by zero:** after elimination the coefficient of $y$ is $0$, so there is nothing to divide by.

---

## Oral Explanation (3 sentences)

Subtracting twice the first equation from the second removes both unknowns at once and leaves the equation $0=1$. This is impossible, so the system has no solution. The reason is that the left side of the second equation is exactly twice the left side of the first, but the right side $7$ is not twice $3$, so the equations describe two parallel lines.

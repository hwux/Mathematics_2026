# Exercise 13 — Does Every Equation Add New Information?

## The Problem

Consider the system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

---

## What Are We Looking For?

We want the solution set, and we want to know whether each equation contributes a new condition or whether one of them is already implied by the others.

---

## Idea and Theorem Before the Calculation

**Redundant equation:** An equation is redundant if it can be obtained as a combination of the other equations. Removing it does not change the solution set.

**Detection by elimination:** A redundant equation turns into a zero row $(0\ \cdots\ 0\mid0)$ during elimination.

---

## Step-by-Step Solution

**Step 1: Augmented matrix.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
1 & 0 & -1 & \mid & 2 \\
\end{pmatrix}
$$

**Step 2: $R_3\leftarrow R_3-R_1$.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & -1 & -1 & \mid & -8 \\
\end{pmatrix}
$$

**Step 3: $R_3\leftarrow R_3+R_2$.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 10 \\
0 & 1 & 1 & \mid & 8 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

The third row became $0=0$. The system is consistent, has two pivots and one free variable.

**Step 4: Solve with $x_3=s$.**

$$
\begin{aligned}
x_2+x_3 &= 8 \quad\Longrightarrow\quad x_2=8-s, \\
x_1+x_2 &= 10 \quad\Longrightarrow\quad x_1=10-(8-s)=2+s.
\end{aligned}
$$

$$
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
\end{pmatrix} =
\begin{pmatrix}
2 \\
8 \\
0 \\
\end{pmatrix}+s
\begin{pmatrix}
1 \\
-1 \\
1 \\
\end{pmatrix},\qquad s\in\mathbb{R}.
$$

**Step 5: Show the dependence by calculation.**

The operations in Steps 2 and 3 replaced $R_3$ by $R_3-R_1+R_2$ and obtained zero. Hence the third equation equals the first minus the second:

$$
(x_1+x_2)-(x_2+x_3)=x_1-x_3,\qquad 10-8=2.
$$

The third equation follows from the first two, both on the left side and on the right side.

*Why this is valid:* Any solution of the first two equations satisfies their difference, so it automatically satisfies the third equation.

**Step 6: Which equations are necessary?**

The relation $E_3=E_1-E_2$ can be rearranged as $E_1=E_2+E_3$ or $E_2=E_1-E_3$, so each equation follows from the other two. Exactly one equation is redundant, but any one of the three may be dropped. Two equations cannot be dropped, because the remaining pairs are not proportional; for example, $E_1$ and $E_2$ have coefficient rows $(1,1,0)$ and $(0,1,1)$.

---

## Final Answer in Words

The system has infinitely many solutions $x_1=2+s$, $x_2=8-s$, $x_3=s$. Not all three equations are needed: the third equation is the first minus the second, $x_1-x_3=10-8=2$, so it adds no new information. Any two of the three equations describe the same solution set.

---

## Quick Verification

Substitute the general solution into all three equations:

$$
\begin{aligned}
(2+s)+(8-s) &= 10, \\
(8-s)+s &= 8, \\
(2+s)-s &= 2.
\end{aligned}
$$

All three hold for every $s$. For instance, $s=3$ gives $(5,5,3)$: $5+5=10$, $5+3=8$, $5-3=2$.

---

## Common Mistakes

- **Expecting three equations for three unknowns to give one solution:** if one equation is redundant, only two real conditions remain.
- **Checking only the left sides:** for redundancy the right sides must satisfy the same relation; if the third equation were $x_1-x_3=3$, the system would be inconsistent instead.
- **Calling a specific equation "the" redundant one:** the dependence involves all three, so any one of them can be removed.

---

## Oral Explanation (3 sentences)

Elimination turns the third equation into $0=0$, because the third equation is exactly the first minus the second: $(x_1+x_2)-(x_2+x_3)=x_1-x_3$ and $10-8=2$. So only two independent conditions remain, and with $x_3=s$ free the solutions are $(2+s,\ 8-s,\ s)$. Since each equation follows from the other two, any one of them may be dropped without changing the solution set.

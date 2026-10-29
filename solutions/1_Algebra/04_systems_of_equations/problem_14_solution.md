# Exercise 14 — A Small Change in the Right-Hand Side

## The Problem

Compare the systems

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
$$

and

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

---

## What Are We Looking For?

We want to decide whether each system has a solution, and understand why changing $3$ to $3.1$ in one right-hand side makes such a difference.

---

## Idea and Theorem Before the Calculation

**Overdetermined system:** Three equations in two unknowns. Two non-parallel equations already determine a unique point; the third equation is satisfied only if it passes exactly through that point.

**Consistency test:** Elimination either ends with $0=0$ (consistent) or with $0=c$, $c\neq0$ (inconsistent).

To treat both systems at once, write the third right-hand side as $c$, with $c=3$ or $c=3.1$.

---

## Step-by-Step Solution

**Step 1: Augmented matrix with general $c$.**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
2 & -1 & \mid & 1 \\
3 & 0 & \mid & c \\
\end{pmatrix}
$$

**Step 2: $R_2\leftarrow R_2-2R_1$ and $R_3\leftarrow R_3-3R_1$.**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & -3 & \mid & c-6 \\
\end{pmatrix}
$$

**Step 3: $R_3\leftarrow R_3-R_2$.**

$$
\begin{pmatrix}
1 & 1 & \mid & 2 \\
0 & -3 & \mid & -3 \\
0 & 0 & \mid & c-3 \\
\end{pmatrix}
$$

The last row means $0=c-3$.

**Step 4: First system, $c=3$.**

The last row is $0=0$, so the system is consistent. From $-3y=-3$ we get $y=1$, and from $x+y=2$ we get $x=1$. The system has exactly one solution, $(1,1)$.

**Step 5: Second system, $c=3.1$.**

The last row is $0=0.1$, a contradiction. The system has no solution.

*Why this is valid:* The first two equations alone force $(x,y)=(1,1)$. The third equation then requires $3\cdot1=c$, which holds for $c=3$ and fails for $c=3.1$.

**Step 6: Why a small change matters.**

Each equation is a line in the plane. The first two lines meet at the single point $(1,1)$. The third line, $x=\frac c3$, is vertical:

- for $c=3$ it is the line $x=1$, which passes through $(1,1)$, so all three lines share this point;
- for $c=3.1$ it is the line $x=\frac{31}{30}$, shifted slightly to the right, which misses $(1,1)$.

Consistency of an overdetermined system depends on an exact condition, here $c=3$. It is not a matter of degree: any change in $c$, however small, breaks the condition and makes the system inconsistent.

---

## Final Answer in Words

The first system is consistent with the unique solution $x=1$, $y=1$. The second system is inconsistent: elimination gives $0=0.1$. A small change can change the type because three lines in the plane have a common point only if the third line passes *exactly* through the intersection of the first two, and moving it by any amount destroys this coincidence.

---

## Quick Verification

First system with $(1,1)$:

$$
1+1=2,\qquad 2\cdot1-1=1,\qquad 3\cdot1=3.
$$

All hold. Second system: the first two equations still force $(1,1)$, but then $3x=3\neq3.1$, while the third equation alone requires $x=\frac{31}{30}$, which gives $y=2-\frac{31}{30}=\frac{29}{30}$ in the first equation and $2\cdot\frac{31}{30}-\frac{29}{30}=\frac{33}{30}\neq1$ in the second. No point satisfies all three.

---

## Common Mistakes

- **Solving only two of the three equations:** a solution of two equations must still be checked against the third.
- **Treating $0=0.1$ as "almost true":** a contradiction is a contradiction, no matter how small the number.
- **Concluding that the coefficients changed the type:** the coefficients are identical in both systems; only one right-hand side differs.

---

## Oral Explanation (3 sentences)

Elimination reduces both systems to the same rows plus a last row $0=c-3$, so the first system ($c=3$) is consistent with the unique solution $(1,1)$, while the second ($c=3.1$) gives the contradiction $0=0.1$. The first two equations always meet at $(1,1)$, and the third equation describes the vertical line $x=\frac c3$, which passes through that point only when $c=3$. Because consistency here depends on an exact coincidence of three lines, even a tiny change in one right-hand side turns a solvable system into one with no solution.

# Exercise 2 — Determinant of a 3×3 Matrix

## The Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

---

## What Are We Looking For?

We need the single number $\det A$, obtained with Sarrus' rule, and then an independent short check that the number is correct.

---

## Idea and Theorem Before the Calculation

**Sarrus' rule (only for $3\times3$ matrices):** For

$$
M=
\begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{pmatrix}
$$

the determinant is the sum of the three "downward" diagonal products minus the sum of the three "upward" diagonal products:

$$
\begin{aligned}
\det M &= a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32} \\
&\quad -\left(a_{13}a_{22}a_{31}+a_{11}a_{23}a_{32}+a_{12}a_{21}a_{33}\right).
\end{aligned}
$$

**Property used for the check:** Adding a multiple of one row to another row does not change the determinant.

---

## Step-by-Step Solution

**Step 1: Downward diagonal products.**

$$
\begin{aligned}
a_{11}a_{22}a_{33} &= 1\cdot3\cdot5 = 15, \\
a_{12}a_{23}a_{31} &= 2\cdot4\cdot2 = 16, \\
a_{13}a_{21}a_{32} &= (-1)\cdot0\cdot1 = 0.
\end{aligned}
$$

Their sum is $15+16+0=31$.

**Step 2: Upward diagonal products.**

$$
\begin{aligned}
a_{13}a_{22}a_{31} &= (-1)\cdot3\cdot2 = -6, \\
a_{11}a_{23}a_{32} &= 1\cdot4\cdot1 = 4, \\
a_{12}a_{21}a_{33} &= 2\cdot0\cdot5 = 0.
\end{aligned}
$$

Their sum is $-6+4+0=-2$.

**Step 3: Subtract.**

$$
\det A = 31-(-2) = 33.
$$

*Why this is valid:* Sarrus' rule lists all six products of three entries taken from different rows and different columns, with the correct signs. For a $3\times3$ matrix this is exactly the definition of the determinant.

---

## Final Answer in Words

The determinant of $A$ is $33$. Since it is nonzero, $A$ is invertible.

---

## Quick Verification

Perform $R_3\leftarrow R_3-2R_1$. This operation does not change the determinant:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7 \\
\end{pmatrix}.
$$

The first column now contains only one nonzero entry, so expanding along it leaves a single $2\times2$ determinant:

$$
\det A = 1\cdot\det
\begin{pmatrix}
3 & 4 \\
-3 & 7 \\
\end{pmatrix} = 21-(-12) = 33.
$$

The result agrees with Sarrus' rule.

---

## Common Mistakes

- **Using Sarrus' rule for larger matrices:** the diagonal pattern works only for $3\times3$ matrices; for $4\times4$ it gives a wrong result.
- **Forgetting the bracket around the upward products:** the whole sum of upward products is subtracted, so a negative product such as $-6$ ends up as $+6$.
- **Mixing up which diagonals go down and which go up:** writing the first two columns again to the right of the matrix makes the six diagonals easy to see.

---

## Oral Explanation (3 sentences)

Sarrus' rule computes a $3\times3$ determinant as the three downward diagonal products minus the three upward ones, which here gives $31-(-2)=33$. To check the value, subtracting twice the first row from the third row creates a zero below the first pivot without changing the determinant. Expanding along the first column then reduces the problem to the $2\times2$ determinant $21+12=33$, which confirms the result.

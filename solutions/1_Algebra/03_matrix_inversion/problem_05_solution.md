# Exercise 5 — A 3×3 Matrix

## The Problem

Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

---

## What Are We Looking For?

We want the inverse of a $3\times3$ matrix, for which no simple formula like the $2\times2$ one is available, by reducing $[A\mid I]$ to $[I\mid A^{-1}]$.

---

## Idea and Theorem Before the Calculation

**Gauss-Jordan method:** Apply row operations to $[A\mid I]$ until the left half is $I$. The right half is then $A^{-1}$ (see Exercise 4 for the reason).

**Order of work:** first create zeros below the pivots (forward phase), then scale the pivots to $1$, then create zeros above the pivots (backward phase).

---

## Step-by-Step Solution

**Step 0: Augmented matrix.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
1 & 0 & 1 & \mid & 0 & 0 & 1 \\
\end{pmatrix}
$$

**Step 1: $R_3\leftarrow R_3-R_1$.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & -1 & 1 & \mid & -1 & 0 & 1 \\
\end{pmatrix}
$$

**Step 2: $R_3\leftarrow R_3+R_2$.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 2 & \mid & -1 & 1 & 1 \\
\end{pmatrix}
$$

The left half is now upper-triangular with nonzero pivots $1,1,2$, so $A$ is invertible.

**Step 3: $R_3\leftarrow\frac12R_3$.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 1 & \mid & 0 & 1 & 0 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

**Step 4: $R_2\leftarrow R_2-R_3$.**

$$
\begin{pmatrix}
1 & 1 & 0 & \mid & 1 & 0 & 0 \\
0 & 1 & 0 & \mid & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

**Step 5: $R_1\leftarrow R_1-R_2$.**

$$
\begin{pmatrix}
1 & 0 & 0 & \mid & \frac12 & -\frac12 & \frac12 \\
0 & 1 & 0 & \mid & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & \mid & -\frac12 & \frac12 & \frac12 \\
\end{pmatrix}
$$

*Why this is valid:* Each step is an elementary row operation applied to the whole augmented matrix, so the right half always equals the product of the operations performed so far.

**Step 6: Read off the inverse.**

$$
A^{-1}=\frac12
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix}.
$$

---

## Final Answer in Words

Five row operations reduce $[A\mid I]$ to $[I\mid A^{-1}]$, and the inverse is one half of the matrix with rows $(1,-1,1)$, $(1,1,-1)$ and $(-1,1,1)$.

---

## Quick Verification

$$
AA^{-1}=\frac12
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1 \\
\end{pmatrix} =\frac12
\begin{pmatrix}
1+1 & -1+1 & 1-1 \\
1-1 & 1+1 & -1+1 \\
1-1 & -1+1 & 1+1 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{pmatrix}.
$$

The product is $I$, so the inverse is correct. The factor $\frac12$ also matches $\det A$: the pivots $1,1,2$ give $\det A=2$.

---

## Common Mistakes

- **Dividing a row before it is necessary:** fractions appear early and make every following step harder; here division was postponed until Step 3.
- **Changing the order of the backward phase:** clearing the third column first (Step 4) keeps the first row free of fractions until the very last step.
- **Forgetting to apply an operation to the right half:** this is the most common source of a wrong inverse in a $3\times3$ calculation.

---

## Oral Explanation (3 sentences)

The Gauss-Jordan method works for a $3\times3$ matrix in the same way as for a $2\times2$ matrix: row operations on $[A\mid I]$ turn the left half into $I$ and the right half into $A^{-1}$. Here two subtractions create a triangular left half with pivots $1,1,2$, one division makes the last pivot $1$, and two more subtractions clear the entries above the pivots. The resulting inverse is one half of the matrix with rows $(1,-1,1)$, $(1,1,-1)$, $(-1,1,1)$, and multiplying it by $A$ gives the identity.

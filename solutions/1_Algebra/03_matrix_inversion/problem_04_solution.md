# Exercise 4 — Gauss–Jordan

## The Problem

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

---

## What Are We Looking For?

We want to find $A^{-1}$ by row-reducing the augmented matrix $[A\mid I]$, record every intermediate matrix, and understand why the method works.

---

## Idea and Theorem Before the Calculation

**Gauss-Jordan method:** Write $A$ and $I$ side by side as $[A\mid I]$ and apply row operations to the whole augmented matrix until the left half becomes $I$. The right half is then $A^{-1}$:

$$
[A\mid I]\ \longrightarrow\ [I\mid A^{-1}].
$$

**Why it works:** Every row operation is the same as multiplying on the left by an elementary matrix $E_k$. If $E_m\cdots E_1A=I$, then the product $P=E_m\cdots E_1$ satisfies $PA=I$, so $P=A^{-1}$. The same operations act on the right half, which turns $I$ into $PI=P=A^{-1}$.

---

## Step-by-Step Solution

**Step 0: Write the augmented matrix.**

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
3 & 5 & \mid & 0 & 1 \\
\end{pmatrix}
$$

**Step 1: $R_2\leftarrow R_2-3R_1$.**

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & -1 & \mid & -3 & 1 \\
\end{pmatrix}
$$

*Why:* This creates a zero below the first pivot.

**Step 2: $R_2\leftarrow -R_2$.**

$$
\begin{pmatrix}
1 & 2 & \mid & 1 & 0 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

*Why:* The second pivot must be $1$.

**Step 3: $R_1\leftarrow R_1-2R_2$.**

$$
\begin{pmatrix}
1 & 0 & \mid & -5 & 2 \\
0 & 1 & \mid & 3 & -1 \\
\end{pmatrix}
$$

*Why:* This creates a zero above the second pivot, so the left half is now $I$.

**Step 4: Read off the inverse.**

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

*Why this is valid:* The three operations together form a matrix $P$ with $PA=I$. The right half started as $I$ and received the same operations, so it now equals $P=A^{-1}$.

---

## Final Answer in Words

The Gauss-Jordan method turns $[A\mid I]$ into $[I\mid A^{-1}]$ in three row operations, giving

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix}.
$$

Obtaining $I$ on the left means that the combined row operations act as $A^{-1}$, and the right half records exactly this combination applied to $I$.

---

## Quick Verification

$$
AA^{-1}=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}
\begin{pmatrix}
-5 & 2 \\
3 & -1 \\
\end{pmatrix} =
\begin{pmatrix}
-5+6 & 2-2 \\
-15+15 & 6-5 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}.
$$

The $2\times2$ formula gives the same result: $\det A=5-6=-1$, so the inverse is $-1$ times the matrix with entries $5,-2,-3,1$.

---

## Common Mistakes

- **Applying operations only to the left half:** every operation must be applied to the whole row of the augmented matrix.
- **Stopping at a triangular left half:** the left half must become exactly $I$, including the zeros above the pivots.
- **Reading the answer from the left half:** the inverse appears on the right.

---

## Oral Explanation (3 sentences)

The Gauss-Jordan method writes $A$ and $I$ side by side and applies the same row operations to both until the left half becomes the identity matrix. Since every row operation is a multiplication by an elementary matrix, turning $A$ into $I$ means the combined operations form $A^{-1}$, and applying them to $I$ produces $A^{-1}$ in the right half. Here three operations give $A^{-1}$ with rows $(-5,2)$ and $(3,-1)$, which is confirmed by multiplication.

# Exercise 8 — Inverse of a Transformation

## The Problem

The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

---

## What Are We Looking For?

We want the inverse of a scaling matrix, a geometric description of what it does, and a concrete check that it undoes the original scaling.

---

## Idea and Theorem Before the Calculation

**Diagonal matrices:** A diagonal matrix with nonzero diagonal entries $d_1,d_2$ is invertible, and its inverse is the diagonal matrix with entries $\frac1{d_1},\frac1{d_2}$.

**Geometric meaning:** $S$ maps $(x,y)^T$ to $(2x,\frac12y)^T$: it stretches horizontally by the factor $2$ and compresses vertically by the factor $\frac12$.

---

## Step-by-Step Solution

**Step 1: Check invertibility.**

The diagonal entries $2$ and $\frac12$ are nonzero, and $\det S=2\cdot\frac12=1\neq0$.

**Step 2: Find $S^{-1}$.**

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 2 \\
\end{pmatrix}.
$$

*Why this is valid:*

$$
SS^{-1}=
\begin{pmatrix}
2\cdot\frac12 & 0 \\
0 & \frac12\cdot2 \\
\end{pmatrix} =
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},
$$

and in the same way $S^{-1}S=I$.

**Step 3: Geometric interpretation.**

$S^{-1}$ maps $(x,y)^T$ to $(\frac12x,2y)^T$. It compresses horizontally by the factor $\frac12$ and stretches vertically by the factor $2$, which exactly reverses both effects of $S$. Each direction is scaled back by the reciprocal factor.

---

## Final Answer in Words

$S^{-1}$ is the diagonal matrix with entries $\frac12$ and $2$. Geometrically, $S$ doubles horizontal lengths and halves vertical lengths, and $S^{-1}$ halves horizontal lengths and doubles vertical lengths, bringing every point back to where it started.

---

## Quick Verification

Take $x=(1,1)^T$. Then

$$
Sx=
\begin{pmatrix}
2 \\
\frac12 \\
\end{pmatrix},\qquad S^{-1}(Sx)=
\begin{pmatrix}
\frac12\cdot2 \\
2\cdot\frac12 \\
\end{pmatrix} =
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}.
$$

Applying $S^{-1}$ after $S$ returns the original vector. Also $\det S=1$ means that $S$ preserves area: the unit square becomes a $2\times\frac12$ rectangle, which still has area $1$.

---

## Common Mistakes

- **Taking negatives instead of reciprocals:** the inverse of scaling by $2$ is scaling by $\frac12$, not by $-2$.
- **Inverting the matrix as a whole number:** writing $\frac12S$ gives the diagonal $1,\frac14$, which is not the inverse.
- **Confusing "undo" with "do again":** applying $S$ twice gives scaling by $4$ and $\frac14$, not the identity.

---

## Oral Explanation (3 sentences)

The scaling matrix $S$ stretches the plane horizontally by $2$ and compresses it vertically by $\frac12$. Its inverse is the diagonal matrix with the reciprocal factors $\frac12$ and $2$, which compresses horizontally and stretches vertically. Applying $S$ and then $S^{-1}$ to the vector $(1,1)^T$ gives $(2,\frac12)^T$ and then $(1,1)^T$ again, showing that the inverse undoes the transformation.

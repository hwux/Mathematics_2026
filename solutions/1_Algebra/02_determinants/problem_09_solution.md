# Exercise 9 — Area and the Determinant

## The Problem

The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

---

## What Are We Looking For?

We want the area of the parallelogram with sides $u$ and $v$, computed with a $2\times2$ determinant, and an explanation of the difference between the sign of the determinant and the area itself.

---

## Idea and Theorem Before the Calculation

**Area formula:** If two vectors in the plane are placed as the columns of a $2\times2$ matrix, the area of the parallelogram they span is the absolute value of its determinant:

$$
\mathrm{Area} = \left|\det
\begin{pmatrix}
u & v \\
\end{pmatrix}\right|.
$$

**Meaning of the sign:** The determinant is positive if turning from $u$ to $v$ through the smaller angle is counterclockwise, and negative if it is clockwise. The sign describes orientation, while the absolute value describes size.

---

## Step-by-Step Solution

**Step 1: Determinant with the order $u,v$.**

$$
\det
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix} = 3\cdot4-1\cdot1 = 11.
$$

**Step 2: Area.**

$$
\mathrm{Area} = |11| = 11.
$$

*Why this is valid:* The area of a parallelogram is never negative, and the determinant gives the area up to sign.

**Step 3: Reverse the order.**

$$
\det
\begin{pmatrix}
1 & 3 \\
4 & 1 \\
\end{pmatrix} = 1\cdot1-3\cdot4 = -11.
$$

Swapping the two columns multiplies the determinant by $-1$.

**Step 4: Interpret.**

The parallelogram itself does not change, because it is spanned by the same two vectors, so its area remains

$$
|-11| = 11.
$$

Only the orientation changes. The vector $u$ points slightly above the positive $x$-axis and $v$ points steeply upward, so turning from $u$ to $v$ is counterclockwise (positive determinant), while turning from $v$ to $u$ is clockwise (negative determinant).

---

## Final Answer in Words

The parallelogram has area $11$. With the order $u,v$ the determinant is $11$; with the order $v,u$ it is $-11$. Reversing the order changes the sign of the determinant, which records orientation, but not the area, which is its absolute value.

---

## Quick Verification

Compute the area without determinants. The parallelogram fits into the rectangle $[0,4]\times[0,5]$, whose area is $20$, because its vertices are $(0,0)$, $(3,1)$, $(4,5)$ and $(1,4)$. Outside the parallelogram but inside the rectangle there are:

- two triangles with legs $3$ and $1$, total area $2\cdot\frac{3}{2}=3$;
- two triangles with legs $1$ and $4$, total area $2\cdot2=4$;
- two unit squares in the corners $(3,0)$ to $(4,1)$ and $(0,4)$ to $(1,5)$, total area $2$.

The area of the parallelogram is therefore

$$
20-3-4-2 = 11,
$$

which agrees with the determinant.

---

## Common Mistakes

- **Reporting a negative area:** the area is $|\det|$, never the signed determinant.
- **Thinking that reversing the vectors gives a different parallelogram:** the shape is the same; only the orientation is reversed.
- **Placing $u$ in a column and $v$ in a row:** both vectors must be columns (or both rows) of the matrix.

---

## Oral Explanation (3 sentences)

Placing the vectors $u$ and $v$ as columns of a matrix gives the determinant $3\cdot4-1\cdot1=11$, so the parallelogram they span has area $11$. Reversing the order of the vectors swaps the two columns and therefore changes the determinant to $-11$. The parallelogram is the same, so its area is still $|-11|=11$; the sign only tells whether the turn from the first vector to the second is counterclockwise or clockwise.

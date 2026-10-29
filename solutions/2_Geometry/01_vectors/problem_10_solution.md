# Exercise 10 — Triangle Area from Vectors

## The Problem

The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

---

## What Are We Looking For?

We want the area of a triangle in space, obtained from the area of the parallelogram spanned by two of its sides.

---

## Idea and Theorem Before the Calculation

**Area via the cross product:** The parallelogram spanned by vectors $p$ and $q$ has area

$$
\|p\times q\|.
$$

The triangle with sides $p$ and $q$ from a common vertex is half of this parallelogram.

---

## Step-by-Step Solution

**Step 1: Side vectors from $A$.**

$$
\overrightarrow{AB}=B-A=(2,1,0),\qquad \overrightarrow{AC}=C-A=(1,3,2).
$$

**Step 2: Cross product.**

$$
\begin{aligned}
\overrightarrow{AB}\times\overrightarrow{AC} &= (1\cdot2-0\cdot3,\ 0\cdot1-2\cdot2,\ 2\cdot3-1\cdot1) \\
&= (2,-4,5).
\end{aligned}
$$

**Step 3: Parallelogram area.**

$$
\|(2,-4,5)\|=\sqrt{4+16+25}=\sqrt{45}=3\sqrt5.
$$

**Step 4: Triangle area.**

$$
\mathrm{Area}=\frac12\cdot3\sqrt5=\frac{3\sqrt5}{2}\approx3.35.
$$

**Step 5: The factor $\frac12$.**

The parallelogram with sides $\overrightarrow{AB}$ and $\overrightarrow{AC}$ has vertices $A$, $B$, $C$ and $B+C-A$. Its diagonal $BC$ cuts it into two triangles that are congruent (they have the same three side lengths), and one of them is triangle $ABC$. So the triangle is exactly half of the parallelogram.

*Why this is valid:* Congruent triangles have equal areas, and together they fill the parallelogram.

---

## Final Answer in Words

$\overrightarrow{AB}=(2,1,0)$ and $\overrightarrow{AC}=(1,3,2)$; their cross product is $(2,-4,5)$, so the parallelogram has area $3\sqrt5$ and the triangle has area $\frac{3\sqrt5}{2}$. The factor $\frac12$ appears because a diagonal splits the parallelogram into two congruent triangles.

---

## Quick Verification

Compute the area a second way, with the formula $\frac12\sqrt{\|p\|^2\|q\|^2-(p\cdot q)^2}$:

$$
\|p\|^2=5,\qquad \|q\|^2=14,\qquad p\cdot q=2+3+0=5,
$$

$$
\frac12\sqrt{5\cdot14-25}=\frac12\sqrt{45}=\frac{3\sqrt5}{2}.
$$

The same value is obtained without the cross product.

---

## Common Mistakes

- **Forgetting the factor $\frac12$:** $\|p\times q\|$ is the area of the parallelogram, not of the triangle.
- **Using the points instead of the side vectors:** $B\times C$ gives the right area here only because $A$ is the origin; in general the differences from a common vertex must be used.
- **Simplifying $\sqrt{45}$ incorrectly:** $\sqrt{45}=\sqrt{9\cdot5}=3\sqrt5$.

---

## Oral Explanation (3 sentences)

The sides from $A$ are $\overrightarrow{AB}=(2,1,0)$ and $\overrightarrow{AC}=(1,3,2)$, and their cross product $(2,-4,5)$ has length $3\sqrt5$, which is the area of the parallelogram they span. The triangle $ABC$ is half of this parallelogram, so its area is $\frac{3\sqrt5}{2}$. The factor $\frac12$ comes from the diagonal $BC$, which divides the parallelogram into two congruent triangles.

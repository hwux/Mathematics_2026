# Problem 9 — Definite Integral and Geometric Area

## The Problem

Compute

$$
\int_{-1}^{2}x\,dx.
$$

Then separately compute the areas of the parts of the graph below and above the $x$-axis and explain the difference between the definite integral and geometric area.

---

## What Are We Looking For?

We want the definite integral of $x$ over $[-1,2]$, the areas of the two triangles that the line $y=x$ forms with the $x$-axis, and the relation between these numbers.

---

## Idea and Theorem Before the Calculation

**Fundamental theorem of calculus:** If $F'=f$, then $\int_a^bf(x)\,dx=F(b)-F(a)$.

**Signed area:** The definite integral counts area above the $x$-axis as positive and area below as negative. Geometric area is always nonnegative:

$$
\mathrm{Area}=\int_a^b|f(x)|\,dx.
$$

---

## Step-by-Step Solution

**Step 1: The definite integral.**

$$
\int_{-1}^{2}x\,dx=\left[\frac{x^2}{2}\right]_{-1}^{2}=\frac{4}{2}-\frac{1}{2}=\frac32.
$$

**Step 2: Part below the axis, $[-1,0]$.**

The region is a right triangle with legs $1$ and $1$:

$$
A_-=\frac12\cdot1\cdot1=\frac12,\qquad \int_{-1}^{0}x\,dx=-\frac12.
$$

**Step 3: Part above the axis, $[0,2]$.**

A right triangle with legs $2$ and $2$:

$$
A_+=\frac12\cdot2\cdot2=2,\qquad \int_0^2x\,dx=2.
$$

**Step 4: Compare.**

$$
\int_{-1}^{2}x\,dx=A_+-A_-=2-\frac12=\frac32,\qquad \mathrm{Area}=A_++A_-=2+\frac12=\frac52.
$$

---

## Sketch

![The line y = x on [-1, 2], with a triangle of signed area -1/2 below the axis and +2 above](figures/ex09_signed_area.svg)

---

## Integral Versus Area

The definite integral is a signed accumulation: contributions where $f<0$ are subtracted. It answers questions such as "net change" or "displacement". The geometric area adds the absolute sizes of all pieces. They coincide only when $f\ge0$ on the whole interval; here the small negative triangle makes the integral smaller than the area by $2\cdot\frac12=1$.

---

## Final Answer in Words

$$
\int_{-1}^{2}x\,dx=\frac32.
$$

The area below the axis is $\frac12$ and the area above is $2$. The integral is their difference, $\frac32$, while the total geometric area is their sum, $\frac52$.

---

## Quick Verification

$\int_{-1}^{2}|x|\,dx=\int_{-1}^0(-x)\,dx+\int_0^2x\,dx=\frac12+2=\frac52$, which matches the geometric area. Also, for a linear function the integral equals the length of the interval times the value at its midpoint: $3\cdot\frac12=\frac32$.

---

## Common Mistakes

- **Calling $\frac32$ the area:** it is the signed area.
- **Taking the absolute value of the result:** $\left|\int f\right|$ is not $\int|f|$.
- **Forgetting to split at the zero $x=0$:** area must be computed piece by piece.

---

## Oral Explanation (3 sentences)

The fundamental theorem gives $\int_{-1}^2x\,dx=\frac{4}{2}-\frac{1}{2}=\frac32$. Geometrically the line $y=x$ forms a triangle of area $\frac12$ below the axis on $[-1,0]$ and a triangle of area $2$ above the axis on $[0,2]$. The integral subtracts the part below the axis and gives $\frac32$, while the actual area adds both parts and gives $\frac52$.

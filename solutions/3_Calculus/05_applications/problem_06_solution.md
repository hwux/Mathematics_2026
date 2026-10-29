# Problem 6 — Average Value of a Function

## The Problem

Compute the average value of the function

$$
f(x)=x^2
$$

on the interval $[0,3]$.

Find a point $c\in[0,3]$ for which $f(c)$ is equal to this average value, and interpret the result geometrically.

---

## What Are We Looking For?

We want the average height of the graph of $x^2$ over $[0,3]$, a point where the function attains this height, and its geometric meaning.

---

## Idea and Theorem Before the Calculation

**Average value:**

$$
\bar f=\frac{1}{b-a}\int_a^bf(x)\,dx.
$$

**Mean value theorem for integrals:** If $f$ is continuous on $[a,b]$, there is $c\in[a,b]$ with $f(c)=\bar f$.

---

## Step-by-Step Solution

**Step 1: Integral.**

$$
\int_0^3x^2\,dx=\left[\frac{x^3}{3}\right]_0^3=9.
$$

**Step 2: Average value.**

$$
\bar f=\frac{1}{3-0}\cdot9=3.
$$

**Step 3: Point $c$.**

$$
c^2=3\quad\Longrightarrow\quad c=\sqrt3\approx1.732,
$$

taking the root in $[0,3]$ ($-\sqrt3$ is outside).

---

## Geometric Interpretation

The area under the parabola on $[0,3]$ is $9$. A rectangle with the same base $[0,3]$ and height $\bar f=3$ has the same area $3\cdot3=9$. The horizontal line $y=3$ cuts the parabola at $x=\sqrt3$: to the left of this point the parabola is below the line, to the right it is above, and the area "missing" on the left equals the area "extra" on the right.

---

## Final Answer in Words

The average value of $x^2$ on $[0,3]$ is $3$, and it is attained at $c=\sqrt3\approx1.73$. Geometrically, the rectangle of height $3$ over $[0,3]$ has the same area, $9$, as the region under the parabola.

---

## Quick Verification

$\bar f=3$ lies between the minimum $f(0)=0$ and the maximum $f(3)=9$, as an average must. Also $c=\sqrt3$ is to the right of the midpoint $1.5$, because the parabola grows faster on the right, so its average is larger than its value at the midpoint, $f(1.5)=2.25$.

---

## Common Mistakes

- **Averaging the endpoint values:** $\frac{0+9}{2}=4.5$ is not the average of a nonlinear function.
- **Forgetting to divide by the length:** $9$ is the integral, not the average.
- **Choosing $c=-\sqrt3$:** it is not in $[0,3]$.

---

## Oral Explanation (3 sentences)

The average value of a function on an interval is its integral divided by the length of the interval, here $\frac{1}{3}\int_0^3x^2\,dx=\frac{9}{3}=3$. The function equals this average where $c^2=3$, so at $c=\sqrt3$. Geometrically, a rectangle of height $3$ over $[0,3]$ has the same area as the region under the parabola.

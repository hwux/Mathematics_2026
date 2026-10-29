# Problem 11 — Volume of a Solid of Revolution

## The Problem

The region under the graph

$$
y=\sqrt{x},\qquad x\in[0,4],
$$

is rotated about the $x$-axis.

1. Construct the integral describing the volume using the disk method.
2. Compute the volume.
3. Explain where the factor $\pi y^2$ in the integral comes from.

---

## What Are We Looking For?

We want the volume of the solid obtained by spinning the region under $y=\sqrt{x}$, $0\le x\le4$, around the $x$-axis, built from thin disks.

---

## Idea and Theorem Before the Calculation

**Disk method:** A cross-section of the solid perpendicular to the $x$-axis at position $x$ is a disk of radius $y=f(x)$. Its area is $\pi f(x)^2$, and adding up thin disks of thickness $dx$ gives

$$
V=\int_a^b\pi f(x)^2\,dx.
$$

---

## Step-by-Step Solution

**Part 1: The integral.**

$$
V=\int_0^4\pi\left(\sqrt{x}\right)^2dx=\pi\int_0^4x\,dx.
$$

**Part 2: Compute.**

$$
V=\pi\left[\frac{x^2}{2}\right]_0^4=\pi\cdot8=8\pi\approx25.13.
$$

---

## Where $\pi y^2$ Comes From

Cut the solid by a plane perpendicular to the $x$-axis at position $x$. The point of the graph $(x,\sqrt{x})$ moves around the axis on a circle of radius $y=\sqrt{x}$, so the cross-section is a full disk of that radius, with area $\pi y^2$. A slice of thickness $\Delta x$ is approximately a cylinder of volume $\pi y^2\Delta x$. Adding the slices gives a Riemann sum, and in the limit the integral $\int\pi y^2\,dx$.

---

## Final Answer in Words

The volume is

$$
V=\int_0^4\pi\left(\sqrt{x}\right)^2dx=\pi\int_0^4x\,dx=8\pi.
$$

The factor $\pi y^2$ is the area of the circular cross-section of radius $y=\sqrt{x}$.

---

## Quick Verification

The solid is a paraboloid of revolution (since $x=y^2$) of height $4$ and top radius $2$. A known fact is that such a paraboloid has half the volume of the surrounding cylinder: $\frac12\cdot\pi\cdot2^2\cdot4=8\pi$, which matches.

---

## Common Mistakes

- **Writing $\pi\int\sqrt{x}\,dx$:** the radius must be squared.
- **Forgetting $\pi$:** the cross-section is a disk, not a square.
- **Using $2\pi y$:** that is the circumference, which belongs to surface or shell computations.

---

## Oral Explanation (3 sentences)

Each cross-section of the solid perpendicular to the $x$-axis is a disk whose radius is the height of the graph, $y=\sqrt{x}$, so its area is $\pi y^2=\pi x$. Adding up thin disks gives $V=\pi\int_0^4x\,dx=8\pi$. This agrees with the fact that a paraboloid has half the volume of the cylinder around it, $\frac12\pi\cdot2^2\cdot4=8\pi$.

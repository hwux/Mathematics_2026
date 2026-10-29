# Exercise 9 — Ellipsoid and Its Cross-Sections

## The Problem

Consider

$$
\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.
$$

Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|<4$.

---

## What Are We Looking For?

We want to understand a surface in space by slicing it with horizontal planes and describing the curve obtained in each slice.

---

## Idea and Theorem Before the Calculation

**Ellipsoid:** $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1$ has center $(0,0,0)$ and semiaxes $a,b,c$ along the coordinate axes.

**Horizontal cross-section:** substituting $z=c$ into the equation gives an equation in $x$ and $y$ only, describing the curve in which the plane $z=c$ cuts the surface.

---

## Step-by-Step Solution

**Step 1: Semiaxes.**

$$
a=\sqrt9=3\ (x),\qquad b=\sqrt4=2\ (y),\qquad \sqrt{16}=4\ (z).
$$

The ellipsoid reaches $(\pm3,0,0)$, $(0,\pm2,0)$ and $(0,0,\pm4)$.

**Step 2: Cross-section $z=0$.**

$$
\frac{x^2}{9}+\frac{y^2}{4}=1.
$$

This is an ellipse in the $xy$-plane with semiaxes $3$ and $2$, the largest horizontal slice.

**Step 3: Cross-sections $z=c$ with $|c|<4$.**

Substituting $z=c$:

$$
\frac{x^2}{9}+\frac{y^2}{4}=1-\frac{c^2}{16}.
$$

For $|c|<4$ the right side $k^2=1-\frac{c^2}{16}$ lies between $0$ and $1$. Dividing by it:

$$
\frac{x^2}{9k^2}+\frac{y^2}{4k^2}=1,\qquad k=\sqrt{1-\frac{c^2}{16}}.
$$

This is an ellipse with semiaxes $3k$ and $2k$.

*Why this is valid:* For $|c|<4$ the number $k^2$ is positive, so the division is allowed and the curve is a genuine ellipse.

**Step 4: Describe the change.**

- At $c=0$ we have $k=1$: the largest ellipse, semiaxes $3$ and $2$.
- As $|c|$ grows toward $4$, $k$ decreases toward $0$: the ellipses shrink.
- The ratio of the semiaxes stays $3k:2k=3:2$, so all slices have the same shape and differ only in size.
- At $|c|=4$ the slice is a single point $(0,0,\pm4)$, and for $|c|>4$ there are no points.

---

## Final Answer in Words

The semiaxes are $3$, $2$ and $4$ along the $x$-, $y$- and $z$-axes. The cross-section $z=0$ is the ellipse $\frac{x^2}{9}+\frac{y^2}{4}=1$. For $|c|<4$ the cross-section $z=c$ is an ellipse with semiaxes $3k$ and $2k$, where $k=\sqrt{1-\frac{c^2}{16}}$: all slices have the same $3:2$ shape and shrink from the full size at $c=0$ to a single point at $c=\pm4$.

---

## Quick Verification

Take $c=2$: then $k^2=1-\frac{4}{16}=\frac34$ and $k=\frac{\sqrt3}{2}$, so the semiaxes are $\frac{3\sqrt3}{2}$ and $\sqrt3$. The point $\left(\frac{3\sqrt3}{2},0,2\right)$ should lie on the ellipsoid:

$$
\frac{27/4}{9}+0+\frac{4}{16}=\frac34+\frac14=1.
$$

It does, confirming the formula for the slices.

---

## Common Mistakes

- **Thinking the slices keep the same size:** the right side $1-\frac{c^2}{16}$ decreases, so the slices shrink.
- **Forgetting to divide by $k^2$:** the semiaxes of a slice are $3k$ and $2k$, not $3$ and $2$.
- **Expecting slices for $|c|>4$:** the right side becomes negative, so there are no points.

---

## Oral Explanation (3 sentences)

The ellipsoid has semiaxes $3$, $2$ and $4$ along the three coordinate axes, and its slice $z=0$ is the ellipse $\frac{x^2}{9}+\frac{y^2}{4}=1$. A slice $z=c$ gives $\frac{x^2}{9}+\frac{y^2}{4}=1-\frac{c^2}{16}$, an ellipse with the same $3:2$ shape scaled by $k=\sqrt{1-\frac{c^2}{16}}$. As $|c|$ grows toward $4$, the scale factor shrinks to $0$, so the slices contract to the single points at the top and bottom of the ellipsoid.

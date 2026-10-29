# Exercise 12 — Recognizing a Surface from Cross-Sections

## The Problem

A certain surface has the following properties:
- the cross-section $z=0$ is a point,
- for $z>0$, the cross-sections $z=\mathrm{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

---

## What Are We Looking For?

We reverse the usual direction: instead of slicing a known surface, we are given the slices and must find an equation that produces them.

---

## Idea and Theorem Before the Calculation

**Circular horizontal slices** centered on the $z$-axis mean that the equation depends on $x$ and $y$ only through $x^2+y^2=r^2$, the squared distance from the axis.

**Parabolic profiles:** if the radius $r$ and the height $z$ are related by $z=r^2$, then every vertical slice through the axis is a parabola.

---

## Step-by-Step Solution

**Step 1: Propose the equation.**

$$
z=x^2+y^2.
$$

**Step 2: Check property 1 (slice $z=0$).**

$$
x^2+y^2=0\quad\Longrightarrow\quad x=y=0.
$$

The slice is the single point $(0,0,0)$.

**Step 3: Check property 2 (slices $z=c>0$).**

$$
x^2+y^2=c.
$$

This is a circle centered on the $z$-axis with radius $\sqrt c$, and $\sqrt c$ increases as $c$ increases.

**Step 4: Check property 3 (vertical slices through $Oz$).**

A vertical plane through the $z$-axis contains the points $(r\cos\theta,\ r\sin\theta,\ z)$ for a fixed angle $\theta$, where $r$ is the signed distance along the plane. In this plane

$$
z=r^2\cos^2\theta+r^2\sin^2\theta=r^2,
$$

which is a parabola in the coordinates $(r,z)$. In particular, $x=0$ gives $z=y^2$ and $y=0$ gives $z=x^2$.

*Why this is valid:* All three required properties hold, so the proposed surface has exactly the described cross-sections.

**Step 5: Why other candidates fail.**

- The cone $z^2=x^2+y^2$ has a point at $z=0$ and growing circles, but its vertical slices through the axis are pairs of lines $z=\pm r$, not parabolas.
- The ellipsoid has circles that shrink again, not ones that keep growing.

More generally, $z=k(x^2+y^2)$ with any $k>0$ has all three properties; $k=1$ is the simplest choice.

---

## Final Answer in Words

A suitable surface is the circular paraboloid $z=x^2+y^2$. Its slice $z=0$ is the origin, the slices $z=c>0$ are circles of radius $\sqrt c$ that grow with $c$, and every vertical slice through the $z$-axis is the parabola $z=r^2$. Any $z=k(x^2+y^2)$ with $k>0$ works as well.

---

## Quick Verification

Take the vertical plane $y=x$ through the axis, with $\theta=45^\circ$. Points of the surface in this plane satisfy $z=x^2+x^2=2x^2$; with $r=\sqrt2\,x$ this is $z=r^2$, a parabola. For example $(1,1,2)$ lies on the surface and in the plane $y=x$, at distance $r=\sqrt2$ from the axis and height $z=2=r^2$.

---

## Common Mistakes

- **Choosing the cone $z^2=x^2+y^2$:** its profiles are lines, not parabolas.
- **Choosing $z=x^2+2y^2$:** its horizontal slices are ellipses, not circles.
- **Forgetting the requirement $z>0$:** the surface $z=-(x^2+y^2)$ has its circles below the origin, not above.

---

## Oral Explanation (3 sentences)

Circular horizontal slices around the $z$-axis mean that the equation depends only on $x^2+y^2$, and parabolic vertical profiles mean that the height grows like the square of the distance from the axis. This leads to $z=x^2+y^2$, whose slice $z=0$ is a single point and whose slices $z=c>0$ are circles of radius $\sqrt c$. Every vertical slice through the axis gives $z=r^2$, a parabola, whereas a cone would give straight lines.

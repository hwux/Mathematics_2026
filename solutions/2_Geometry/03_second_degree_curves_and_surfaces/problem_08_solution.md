# Exercise 8 — Sphere

## The Problem

Reduce

$$
x^2+y^2+z^2-4x+2y-6z-2=0
$$

to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

---

## What Are We Looking For?

We want to rewrite the equation as $(x-x_0)^2+(y-y_0)^2+(z-z_0)^2=r^2$, exactly as for a circle but with three coordinates.

---

## Idea and Theorem Before the Calculation

**Canonical form of a sphere:** $(x-x_0)^2+(y-y_0)^2+(z-z_0)^2=r^2$ with $r>0$ describes all points at distance $r$ from the center $(x_0,y_0,z_0)$.

**Completing the square** is done separately for each variable, as for the circle in Exercise 2.

---

## Step-by-Step Solution

**Step 1: Group the terms.**

$$
(x^2-4x)+(y^2+2y)+(z^2-6z)=2.
$$

**Step 2: Complete the squares.**

$$
x^2-4x=(x-2)^2-4,\qquad y^2+2y=(y+1)^2-1,\qquad z^2-6z=(z-3)^2-9.
$$

**Step 3: Substitute.**

$$
(x-2)^2+(y+1)^2+(z-3)^2-14=2\quad\Longrightarrow\quad (x-2)^2+(y+1)^2+(z-3)^2=16.
$$

*Why this is valid:* Each completed square equals the original group of terms, so the equation is unchanged.

**Step 4: Center and radius.**

$$
(x_0,y_0,z_0)=(2,-1,3),\qquad r=4.
$$

**Step 5: Two points on the sphere.**

Move from the center by $4$ along a coordinate axis:

$$
(2+4,-1,3)=(6,-1,3),\qquad (2,-1,3+4)=(2,-1,7).
$$

---

## Final Answer in Words

The canonical form is $(x-2)^2+(y+1)^2+(z-3)^2=16$, a sphere with center $(2,-1,3)$ and radius $4$. Two of its points are $(6,-1,3)$ and $(2,-1,7)$.

---

## Quick Verification

Check both points in the original equation.

**Point $(6,-1,3)$.**

$$
36+1+9-24-2-18-2=0.
$$

**Point $(2,-1,7)$.**

$$
4+1+49-8-2-42-2=0.
$$

Both points satisfy the original equation, which confirms the center and radius.

---

## Common Mistakes

- **Forgetting one of the three subtracted constants:** the constants $4$, $1$ and $9$ all have to be moved to the right side.
- **Wrong signs in the center:** $(y+1)^2$ corresponds to $y_0=-1$.
- **Assuming every such equation is a sphere:** if the right side after completing the squares were negative, there would be no real points, as in Exercise 7.

---

## Oral Explanation (3 sentences)

Completing the square in each variable turns the equation into $(x-2)^2+(y+1)^2+(z-3)^2=16$, which is the canonical form of a sphere. The sphere has center $(2,-1,3)$ and radius $4$, exactly as a circle would, only with one more coordinate. Moving $4$ units from the center along the $x$-axis or the $z$-axis gives the points $(6,-1,3)$ and $(2,-1,7)$, and both satisfy the original equation.

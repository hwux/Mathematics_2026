# Exercise 13 — Intersection of a Sphere and a Plane

## The Problem

Given the sphere

$$
x^2+y^2+z^2=25
$$

and the plane $z=3$, find the equation of the intersection curve and its radius. Then describe what happens for $z=c$ depending on $c$.

---

## What Are We Looking For?

We want the curve in which a horizontal plane cuts a sphere, its radius, and a description of how this curve changes as the plane moves up and down.

---

## Idea and Theorem Before the Calculation

**Intersection:** A point lies on both the sphere and the plane $z=c$ when it satisfies both equations. Substituting $z=c$ into the sphere gives

$$
x^2+y^2=25-c^2,
$$

a circle in the plane $z=c$ if the right side is positive.

**Geometric view:** the center $(0,0,0)$, the center of the slice $(0,0,c)$ and a point of the slice form a right triangle with hypotenuse $5$ and legs $|c|$ and the slice radius $\rho$, so $\rho^2+c^2=25$.

---

## Step-by-Step Solution

**Step 1: The plane $z=3$.**

$$
x^2+y^2+9=25\quad\Longrightarrow\quad x^2+y^2=16.
$$

The intersection curve is

$$
\begin{cases}
x^2+y^2=16, \\
z=3,
\end{cases}
$$

a circle with center $(0,0,3)$ and radius $\rho=4$.

**Step 2: General plane $z=c$.**

$$
x^2+y^2=25-c^2.
$$

- If $|c|<5$: the right side is positive, and the intersection is a circle with center $(0,0,c)$ and radius $\rho=\sqrt{25-c^2}$.
- If $|c|=5$: the right side is $0$, and the intersection is the single point $(0,0,\pm5)$; the plane touches the sphere.
- If $|c|>5$: the right side is negative, and there is no intersection.

*Why this is valid:* The sphere has radius $5$, so a plane at distance $|c|$ from the center cuts it if $|c|<5$, touches it if $|c|=5$, and misses it if $|c|>5$.

**Step 3: How the radius changes.**

The radius $\sqrt{25-c^2}$ is largest, equal to $5$, at $c=0$, where the plane passes through the center and cuts a great circle. As $|c|$ grows the circles shrink, slowly at first and then faster, until they become a point at $|c|=5$.

---

## Final Answer in Words

The plane $z=3$ cuts the sphere in the circle $x^2+y^2=16$, $z=3$, of radius $4$. In general the plane $z=c$ gives a circle of radius $\sqrt{25-c^2}$ for $|c|<5$, a single point for $|c|=5$ (tangent plane), and no intersection for $|c|>5$.

---

## Quick Verification

The point $(4,0,3)$ lies on the circle found in Step 1, and on the sphere: $16+0+9=25$.

Right-triangle check: the distance from the sphere's center to the plane is $3$, the slice radius is $4$, and $3^2+4^2=5^2$ is the squared radius of the sphere.

---

## Common Mistakes

- **Giving the radius as $16$:** the radius of $x^2+y^2=16$ is $4$.
- **Forgetting that the circle lies in the plane $z=3$:** the equation $x^2+y^2=16$ alone describes a cylinder in space; the condition $z=3$ is part of the answer.
- **Assuming every horizontal plane cuts the sphere:** for $|c|>5$ there is no intersection.

---

## Oral Explanation (3 sentences)

Substituting $z=3$ into $x^2+y^2+z^2=25$ gives $x^2+y^2=16$, so the plane cuts the sphere in a circle of radius $4$ centered at $(0,0,3)$. In general the plane $z=c$ gives a circle of radius $\sqrt{25-c^2}$, which is a great circle of radius $5$ at $c=0$ and shrinks as the plane moves away from the center. At $c=\pm5$ the plane only touches the sphere at one point, and for $|c|>5$ it misses the sphere completely.

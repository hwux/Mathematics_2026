# Exercise 7 — A Line Relative to a Plane

## The Problem

For

$$
L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,
$$

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

---

## What Are We Looking For?

We want to classify the position of the line relative to the plane using the direction vector of the line, the normal vector of the plane, and one test point.

---

## Idea and Theorem Before the Calculation

Let $L$ have direction $v$ and point $p$, and let $\Pi$ have normal $n$.

- If $v\cdot n\neq0$, the line crosses the plane in exactly one point.
- If $v\cdot n=0$, the line is parallel to the plane. Then either $p$ lies in $\Pi$, and the whole line lies in $\Pi$, or $p$ does not, and the line has no common point with $\Pi$.

---

## Step-by-Step Solution

**Step 1: Read the vectors.**

$$
v=(1,-1,0),\qquad n=(1,1,1),\qquad p=(1,1,0).
$$

**Step 2: Dot product.**

$$
v\cdot n=1\cdot1+(-1)\cdot1+0\cdot1=0.
$$

The direction is perpendicular to the normal, so the line is parallel to the plane: it either lies in it or misses it completely.

**Step 3: Test the point $p$.**

$$
1+1+0=2.
$$

The point $p$ satisfies the plane equation, so $p\in\Pi$.

**Step 4: Conclude.**

The line is parallel to the plane and has a point in it, so the **whole line lies in the plane**.

*Why this is valid:* Moving along $v$ does not change the value of $x+y+z$, because $v\cdot n=0$; starting at a point where this value is $2$, the line stays in the plane forever.

**Role of the dot product.** Along the line, the left side of the plane equation changes at the rate $n\cdot v$ per unit of $t$. If $n\cdot v\neq0$ it takes every value once, so it equals $2$ exactly once. If $n\cdot v=0$ it is constant, so it equals $2$ either always or never.

---

## Final Answer in Words

The line lies in the plane. The dot product $v\cdot n=0$ shows that the direction of the line is parallel to the plane, and the point $(1,1,0)$ of the line satisfies the plane equation, so every point of the line does.

---

## Quick Verification

Substitute the general point of the line into the plane equation:

$$
(1+t)+(1-t)+0=2\qquad\mathrm{for\ every}\ t.
$$

The equation holds for all $t$, which confirms that the entire line lies in $\Pi$.

---

## Common Mistakes

- **Concluding "parallel, no common point" from $v\cdot n=0$ alone:** a point of the line must be tested as well.
- **Testing the direction vector in the plane equation:** the direction vector is not a point; only $p$ should be substituted.
- **Interpreting $v\cdot n=0$ as "the line is perpendicular to the plane":** it means the line is perpendicular to the *normal*, hence parallel to the plane.

---

## Oral Explanation (3 sentences)

The direction vector $(1,-1,0)$ has dot product $0$ with the normal $(1,1,1)$, so the line runs parallel to the plane and the value of $x+y+z$ does not change along it. The point $(1,1,0)$ of the line gives $x+y+z=2$, so it lies in the plane. Therefore every point of the line lies in the plane, which is confirmed by $(1+t)+(1-t)+0=2$ for all $t$.

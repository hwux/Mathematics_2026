# Exercise 1 — Line Through Two Points

## The Problem

Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

---

## What Are We Looking For?

We want two equivalent descriptions of the same line in the plane: a parametric one built from a point and a direction, and a general one built from a normal vector. Both must contain the given points.

---

## Idea and Theorem Before the Calculation

**Parametric form:** A line through a point $P_0$ with direction vector $v$ consists of all points

$$
(x,y)=P_0+tv,\qquad t\in\mathbb{R}.
$$

**General form:** A line with normal vector $n=(a,b)$ has an equation $ax+by+c=0$. A normal vector is perpendicular to the direction vector, so $n\cdot v=0$.

**From $v$ to $n$ in the plane:** if $v=(p,q)$, then $n=(q,-p)$ is perpendicular to it, because $pq-qp=0$.

---

## Step-by-Step Solution

**Step 1: Direction vector.**

$$
v=B-A=(4-1,\ -1-2)=(3,-3).
$$

Any nonzero multiple also works; the simpler vector $(1,-1)$ points in the same direction.

**Step 2: Parametric form.**

Using the point $A$ and the direction $v$:

$$
(x,y)=(1,2)+t(3,-3),\qquad t\in\mathbb{R},
$$

that is, $x=1+3t$ and $y=2-3t$.

**Step 3: Normal vector.**

From $v=(3,-3)$ we get $(-3,-3)$, or after dividing by $-3$,

$$
n=(1,1).
$$

*Why this is valid:* $n\cdot v=1\cdot3+1\cdot(-3)=0$, so $n$ is perpendicular to the line.

**Step 4: General form.**

The equation has the form $x+y+c=0$. Substituting $A=(1,2)$ gives $1+2+c=0$, so $c=-3$:

$$
x+y-3=0.
$$

The same equation follows from the parametric form: adding $x=1+3t$ and $y=2-3t$ eliminates $t$ and gives $x+y=3$.

---

## Final Answer in Words

The line has parametric form $(x,y)=(1,2)+t(3,-3)$ and general form $x+y-3=0$. A direction vector is $(3,-3)$, or equivalently $(1,-1)$, and a normal vector is $(1,1)$.

---

## Quick Verification

General form:

$$
A:\ 1+2-3=0,\qquad B:\ 4+(-1)-3=0.
$$

Parametric form: $t=0$ gives $(1,2)=A$, and $t=1$ gives $(1+3,\ 2-3)=(4,-1)=B$. Both points satisfy both equations.

---

## Common Mistakes

- **Using a point as the direction vector:** the direction is the difference $B-A$, not one of the points.
- **Confusing direction and normal:** in the general form $ax+by+c=0$ the coefficients $(a,b)$ form a vector *perpendicular* to the line.
- **Thinking the equations are unique:** different points and multiples of $v$ give different but equivalent parametric forms; multiplying the general equation by a nonzero number gives the same line.

---

## Oral Explanation (3 sentences)

The difference $B-A=(3,-3)$ points along the line, so together with the point $A$ it gives the parametric form $(1,2)+t(3,-3)$. A vector perpendicular to this direction, such as $(1,1)$, is a normal vector, and it gives the general form $x+y-3=0$ after substituting $A$ to find the constant. Both $A$ and $B$ satisfy this equation, and in the parametric form they correspond to $t=0$ and $t=1$.

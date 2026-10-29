# Exercise 3 — Plane Through a Point with a Given Normal Vector

## The Problem

Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

---

## What Are We Looking For?

We want the equation of the plane that contains $P$ and is perpendicular to the given vector $n$.

---

## Idea and Theorem Before the Calculation

**Point-normal form:** A point $X=(x,y,z)$ lies in the plane through $P$ with normal $n$ exactly when the vector $X-P$ lies in the plane, that is, when it is perpendicular to $n$:

$$
n\cdot(X-P)=0.
$$

With $n=(a,b,c)$ and $P=(x_0,y_0,z_0)$ this reads

$$
a(x-x_0)+b(y-y_0)+c(z-z_0)=0.
$$

---

## Step-by-Step Solution

**Step 1: Substitute the data.**

$$
2(x-1)+1\cdot(y+2)-1\cdot(z-3)=0.
$$

**Step 2: Expand.**

$$
2x-2+y+2-z+3=0\quad\Longrightarrow\quad 2x+y-z+3=0.
$$

The plane is

$$
2x+y-z=-3.
$$

*Why this is valid:* Every vector from $P$ to a point of the plane is perpendicular to $n$, and the dot product is zero exactly for such vectors.

**Step 3: The role of the normal vector.**

The coefficients of $x,y,z$ in the equation are exactly the entries of $n=(2,1,-1)$. The normal vector fixes the orientation of the plane: it determines which way the plane is tilted. The point $P$ fixes its position, that is, the constant on the right-hand side. Changing only the constant gives a parallel plane with the same normal.

---

## Final Answer in Words

The plane is $2x+y-z=-3$. Its normal vector $(2,1,-1)$ appears as the coefficients of $x,y,z$ and determines the orientation, while the point $P$ determines the constant $-3$.

---

## Quick Verification

Substitute $P=(1,-2,3)$:

$$
2\cdot1+(-2)-3=-3.
$$

The point satisfies the equation. As a second check, the point $Q=(0,0,3)$ also satisfies $2\cdot0+0-3=-3$, and the vector $Q-P=(-1,2,0)$ is perpendicular to $n$: $(2,1,-1)\cdot(-1,2,0)=-2+2+0=0$.

---

## Common Mistakes

- **Sign errors with negative coordinates:** $y-y_0$ with $y_0=-2$ becomes $y+2$.
- **Using $P$ as the coefficients:** the coefficients come from the normal vector, not from the point.
- **Writing $n\cdot X=0$:** this describes a plane through the origin; the point $P$ must be included through $X-P$.

---

## Oral Explanation (3 sentences)

A point $X$ lies in the plane exactly when the vector from $P$ to $X$ is perpendicular to the normal $n$, which is the condition $n\cdot(X-P)=0$. Expanding $2(x-1)+(y+2)-(z-3)=0$ gives the equation $2x+y-z=-3$, which is satisfied by $P$. The normal vector supplies the coefficients and therefore the tilt of the plane, while the point supplies the constant and therefore its position.

# Problem 2 — Maximum Area of a Rectangle

## The Problem

A rectangle has perimeter $40$.

1. Write its area as a function of the length of one side.
2. Determine the domain of this function resulting from the geometry of the problem.
3. Find the dimensions that give the maximum area.
4. Justify that the point found actually gives a maximum.

---

## What Are We Looking For?

Among all rectangles with perimeter $40$, we want the one with the largest area, found by the full optimization scheme.

---

## Idea and Theorem Before the Calculation

**Model:** If one side is $x$, the perimeter condition $2x+2y=40$ gives the other side $y=20-x$.

**Optimization:** find critical points of the area function in the open domain, then confirm the maximum by the sign of the derivative or the second derivative.

---

## Step-by-Step Solution

**Part 1: Area function.**

$$
A(x)=x(20-x)=20x-x^2.
$$

**Part 2: Domain.**

Both sides must be positive: $x>0$ and $20-x>0$. So

$$
D=(0,20).
$$

(The endpoints $0$ and $20$ would give a degenerate rectangle with area $0$.)

**Part 3: Critical point.**

$$
A'(x)=20-2x=0\iff x=10.
$$

Then the other side is $20-10=10$.

**Part 4: Maximum.**

$A'(x)>0$ for $0<x<10$ and $A'(x)<0$ for $10<x<20$, so $A$ increases and then decreases: $x=10$ is the global maximum on $(0,20)$. Also $A''(x)=-2<0$.

$$
A(10)=100.
$$

---

## Final Answer in Words

The area is $A(x)=x(20-x)$ on the domain $0<x<20$. The maximum area is $100$, attained by the square $10\times10$; the derivative changes sign from positive to negative at $x=10$, which confirms the maximum.

---

## Quick Verification

Completing the square: $A(x)=100-(x-10)^2\le100$, with equality only for $x=10$. Nearby rectangles have smaller areas, for example $9\times11=99$ and $8\times12=96$.

---

## Common Mistakes

- **Using $y=40-x$:** the perimeter contains each side twice.
- **Taking the domain $\mathbb{R}$:** lengths must be positive.
- **Stopping at $A'(10)=0$:** the type of the critical point must be justified.

---

## Oral Explanation (3 sentences)

If one side is $x$, the other is $20-x$, so the area is $A(x)=20x-x^2$ for $0<x<20$. The derivative $20-2x$ vanishes at $x=10$ and changes sign from positive to negative, so this is the maximum. The best rectangle is the $10\times10$ square, with area $100$.

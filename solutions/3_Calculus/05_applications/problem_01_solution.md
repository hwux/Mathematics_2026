# Problem 1 — Motion — from Position to Velocity

## The Problem

The position of a point is described by

$$
s(t)=t^3-6t^2+9t+2,\qquad t\ge0.
$$

1. Determine the velocity and acceleration.
2. Find the times at which the point stops.
3. Determine on which intervals the point moves in the positive direction of the axis and on which intervals it moves in the negative direction.

---

## What Are We Looking For?

We want the velocity and acceleration of a point moving on a line, the moments when it is momentarily at rest, and the time intervals of motion in each direction.

---

## Idea and Theorem Before the Calculation

**Velocity** is the rate of change of position, $v(t)=s'(t)$. **Acceleration** is the rate of change of velocity, $a(t)=v'(t)=s''(t)$.

**Direction of motion:** $v(t)>0$ means motion in the positive direction, $v(t)<0$ in the negative direction, and $v(t)=0$ means the point stops (at least momentarily).

---

## Step-by-Step Solution

**Part 1: Velocity and acceleration.**

$$
v(t)=s'(t)=3t^2-12t+9,\qquad a(t)=v'(t)=6t-12.
$$

**Part 2: Stops.**

$$
3t^2-12t+9=3(t^2-4t+3)=3(t-1)(t-3)=0\iff t=1\ \mathrm{or}\ t=3.
$$

Both times satisfy $t\ge0$.

**Part 3: Direction of motion.**

| interval | $[0,1)$ | $(1,3)$ | $(3,\infty)$ |
|---|---|---|---|
| test time | $0$ | $2$ | $4$ |
| $v$ | $9>0$ | $-3<0$ | $9>0$ |
| motion | positive direction | negative direction | positive direction |

Positions at the key times:

$$
s(0)=2,\qquad s(1)=1-6+9+2=6,\qquad s(3)=27-54+27+2=2.
$$

---

## Interpretation

The point starts at $2$ moving forward, slows down and stops at position $6$ at $t=1$, then moves backward and stops again at position $2$ at $t=3$, after which it moves forward for good. The point speeds up when $v$ and $a$ have the same sign and slows down when they have opposite signs. With $a(t)=6t-12$:

| interval | $(0,1)$ | $(1,2)$ | $(2,3)$ | $(3,\infty)$ |
|---|---|---|---|---|
| $v$ | $+$ | $-$ | $-$ | $+$ |
| $a$ | $-$ | $-$ | $+$ | $+$ |
| motion | forward, slowing down | backward, speeding up | backward, slowing down | forward, speeding up |

So the backward speed is greatest at $t=2$, where $v(2)=-3$ and the acceleration changes sign; after that the point brakes until it stops at $t=3$.

---

## Final Answer in Words

$v(t)=3t^2-12t+9$ and $a(t)=6t-12$. The point stops at $t=1$ and $t=3$. It moves in the positive direction for $0\le t<1$ and $t>3$, and in the negative direction for $1<t<3$.

---

## Quick Verification

Displacement between the stops: $s(3)-s(1)=2-6=-4$, negative, consistent with backward motion on $(1,3)$. With the integral: $\int_1^3v(t)\,dt=\left[t^3-6t^2+9t\right]_1^3=0-4=-4$.

---

## Common Mistakes

- **Treating $s$ as the velocity:** the sign of $s$ is the position, not the direction of motion.
- **Missing $t=1$ or $t=3$:** both zeros of $v$ are stops.
- **Confusing a stop with $a=0$:** at $t=2$ the acceleration is zero, but the point is moving.

---

## Oral Explanation (3 sentences)

The velocity is the derivative of the position, $v(t)=3t^2-12t+9=3(t-1)(t-3)$, and the acceleration is $a(t)=6t-12$. The point stops when the velocity is zero, at $t=1$ and $t=3$. Between these times the velocity is negative, so the point moves backward from position $6$ to $2$, while before $t=1$ and after $t=3$ it moves in the positive direction.

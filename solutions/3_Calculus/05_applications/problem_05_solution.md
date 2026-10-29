# Problem 5 — Distance from Velocity

## The Problem

The velocity of a car during the first five seconds is described by the function

$$
v(t)=4t+2\quad [\mathrm{m/s}].
$$

Compute the distance traveled and explain why the integral of velocity gives the change in position.

Then answer what would have to be changed in the reasoning if the velocity also took negative values.

---

## What Are We Looking For?

We want the distance traveled in $5$ seconds, an explanation of why integrating velocity gives the change in position, and the modification needed when velocity can be negative.

---

## Idea and Theorem Before the Calculation

**Position and velocity:** $s'(t)=v(t)$, so $s$ is an antiderivative of $v$.

**Fundamental theorem:**

$$
\int_a^bv(t)\,dt=s(b)-s(a),
$$

the change in position (displacement).

**Distance:** the total length traveled is $\int_a^b|v(t)|\,dt$.

---

## Step-by-Step Solution

**Step 1: Sign of the velocity.** For $0\le t\le5$, $v(t)=4t+2\ge2>0$, so the car moves forward the whole time, and distance equals displacement.

**Step 2: Integral.**

$$
\int_0^5(4t+2)\,dt=\left[2t^2+2t\right]_0^5=50+10=60\ \mathrm{m}.
$$

---

## Why the Integral Gives the Change in Position

Split $[0,5]$ into short time intervals of length $\Delta t$. On each of them the velocity is almost constant, so the car moves about $v(t)\Delta t$ meters. Adding these pieces gives a Riemann sum for $\int_0^5v(t)\,dt$, and refining the partition turns the approximation into the exact integral. Equivalently, since $s'=v$, the fundamental theorem gives $\int_0^5v\,dt=s(5)-s(0)$.

---

## If the Velocity Could Be Negative

A negative velocity means motion backward. Then $\int v\,dt$ still gives the **displacement** $s(b)-s(a)$, in which backward motion is subtracted. The **distance traveled** requires the absolute value:

$$
\mathrm{distance}=\int_a^b|v(t)|\,dt.
$$

In practice one finds the times where $v(t)=0$, splits the interval there, and adds the absolute values of the integrals over the pieces. For example, for $v(t)=2t-4$ on $[0,5]$ the displacement is $\int_0^5(2t-4)\,dt=5$ m, but the distance is $4+9=13$ m.

---

## Final Answer in Words

The car travels $\int_0^5(4t+2)\,dt=60$ m. The integral of velocity gives the change in position because position is an antiderivative of velocity. If the velocity could be negative, the integral would give the displacement, and the distance would be computed as $\int|v(t)|\,dt$, splitting the interval where $v$ changes sign.

---

## Quick Verification

The velocity grows linearly from $2$ to $22$ m/s, so the average velocity is $\frac{2+22}{2}=12$ m/s, and $12\cdot5=60$ m. Geometrically, the area under the graph of $v$ is a trapezoid with parallel sides $2$ and $22$ and height $5$: $\frac{2+22}{2}\cdot5=60$.

---

## Common Mistakes

- **Multiplying $v(5)\cdot5=110$:** the velocity is not constant.
- **Confusing displacement and distance** when $v$ changes sign.
- **Forgetting units:** the result is in meters, since m/s times s gives m.

---

## Oral Explanation (3 sentences)

Since the velocity $4t+2$ is positive on $[0,5]$, the distance equals the displacement, $\int_0^5(4t+2)\,dt=60$ m. The integral of velocity gives the change in position because position is an antiderivative of velocity, or, equivalently, because adding up velocity times small time steps gives the total motion. If the velocity were sometimes negative, the integral would give only the net displacement, and the distance would require integrating the absolute value $|v(t)|$.

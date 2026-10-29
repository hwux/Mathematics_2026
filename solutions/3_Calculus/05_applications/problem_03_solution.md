# Problem 3 — A Box Made from Cardboard

## The Problem

From a $30\,\mathrm{cm}\times40\,\mathrm{cm}$ sheet, squares of side length $x$ are cut from the corners and the edges are folded up to form an open box.

Write the volume as a function of $x$, determine the physically meaningful domain, and find the value of $x$ for which the volume is greatest.

---

## What Are We Looking For?

We want a formula for the volume of the open box in terms of the cut size $x$, the values of $x$ that make physical sense, and the cut that maximizes the volume.

---

## Idea and Theorem Before the Calculation

**Model:** Cutting squares of side $x$ from each corner and folding gives a box with height $x$ and base $(30-2x)\times(40-2x)$.

**Closed-interval method:** the maximum of a continuous function on $[0,15]$ is attained at a critical point or an endpoint; at the endpoints the volume is $0$.

---

## Step-by-Step Solution

**Step 1: Volume.**

$$
V(x)=x(30-2x)(40-2x)=4x^3-140x^2+1200x\quad[\mathrm{cm}^3].
$$

**Step 2: Domain.**

We need $x>0$ and $30-2x>0$ (and $40-2x>0$, which is weaker). So

$$
0<x<15.
$$

**Step 3: Derivative.**

$$
V'(x)=12x^2-280x+1200=4\left(3x^2-70x+300\right).
$$

**Step 4: Critical points.**

$$
x=\frac{70\pm\sqrt{4900-3600}}{6}=\frac{70\pm10\sqrt{13}}{6}=\frac{35\pm5\sqrt{13}}{3}.
$$

Numerically $x_1\approx5.657$ and $x_2\approx17.676$. Only $x_1$ lies in $(0,15)$.

**Step 5: Type of the critical point.**

$V''(x)=24x-280$, and $V''(x_1)\approx-144.2<0$, so $x_1$ is a local maximum. Since $V\to0$ at both ends of the domain and $x_1$ is the only critical point inside, it is the global maximum.

**Step 6: Maximum volume.**

$$
V(x_1)=\frac{1000\left(35+13\sqrt{13}\right)}{27}\approx3032.3\ \mathrm{cm}^3.
$$

The box is about $5.66\,\mathrm{cm}$ high with base about $18.69\,\mathrm{cm}\times28.69\,\mathrm{cm}$.

---

## Final Answer in Words

$V(x)=x(30-2x)(40-2x)$ for $0<x<15$. The volume is greatest for

$$
x=\frac{35-5\sqrt{13}}{3}\approx5.66\ \mathrm{cm},
$$

giving $V\approx3032\ \mathrm{cm}^3$.

---

## Quick Verification

Nearby integer cuts: $V(5)=5\cdot20\cdot30=3000$ and $V(6)=6\cdot18\cdot28=3024$, both slightly less than $3032.3$, consistent with a maximum between $5$ and $6$, closer to $6$.

---

## Common Mistakes

- **Base $(30-x)(40-x)$:** a square is cut from both ends of each side, so $2x$ is subtracted.
- **Keeping the root $x\approx17.68$:** it is outside the physical domain.
- **Forgetting to justify the maximum:** check the second derivative or the endpoint values.

---

## Oral Explanation (3 sentences)

Cutting squares of side $x$ gives a box of height $x$ and base $(30-2x)(40-2x)$, so $V(x)=x(30-2x)(40-2x)$ with $0<x<15$. The derivative $4(3x^2-70x+300)$ vanishes at $x=\frac{35\pm5\sqrt{13}}{3}$, and only the smaller value, about $5.66$, lies in the domain. There the second derivative is negative and the volume vanishes at both ends, so the maximum volume is about $3032\,\mathrm{cm}^3$.

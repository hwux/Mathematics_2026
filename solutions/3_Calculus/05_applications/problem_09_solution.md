# Problem 9 — Minimizing the Material Used for a Can

## The Problem

A closed cylinder has fixed volume $V$.

1. Write the volume constraint.
2. Eliminate one of the variables.
3. Express the surface area as a function of the radius $r$.
4. Find the relation between the height $h$ and the radius $r$ for which the material usage is minimal.

Interpret the obtained relation geometrically.

---

## What Are We Looking For?

Among all closed cylinders with a given volume $V$, we want the shape that uses the least material, that is, has the smallest total surface area.

---

## Idea and Theorem Before the Calculation

**Variables:** radius $r>0$ and height $h>0$.

**Formulas:**

$$
\mathrm{volume}=\pi r^2h,\qquad \mathrm{surface}=2\pi r^2+2\pi rh
$$

(two discs and the side).

**Method:** use the constraint to express $h$ through $r$, obtain a function of one variable, and minimize it on $(0,\infty)$.

---

## Step-by-Step Solution

**Part 1: Constraint.**

$$
\pi r^2h=V.
$$

**Part 2: Eliminate $h$.**

$$
h=\frac{V}{\pi r^2}.
$$

**Part 3: Surface area as a function of $r$.**

$$
S(r)=2\pi r^2+2\pi r\cdot\frac{V}{\pi r^2}=2\pi r^2+\frac{2V}{r},\qquad r>0.
$$

**Part 4: Minimize.**

$$
S'(r)=4\pi r-\frac{2V}{r^2}=0\iff4\pi r^3=2V\iff r^3=\frac{V}{2\pi}.
$$

So the only critical point is $r^*=\sqrt[3]{\frac{V}{2\pi}}$.

$S''(r)=4\pi+\frac{4V}{r^3}>0$ for $r>0$, so $S$ is convex and $r^*$ is the global minimum. Also $S(r)\to\infty$ both as $r\to0^+$ and as $r\to\infty$.

**Relation between $h$ and $r$:**

Using $V=2\pi r^3$ at the optimum,

$$
h=\frac{V}{\pi r^2}=\frac{2\pi r^3}{\pi r^2}=2r.
$$

---

## Geometric Interpretation

At the optimum the height equals the diameter, $h=2r$. The axial cross-section of the can (a cut through its axis) is then a square $2r\times2r$: the can is "as tall as it is wide". A tall thin can wastes material on the side wall, and a flat wide can wastes it on the lids; the square cross-section balances the two.

---

## Final Answer in Words

From $\pi r^2h=V$ we get $h=\frac{V}{\pi r^2}$ and the surface area $S(r)=2\pi r^2+\frac{2V}{r}$. It is minimal for $r=\sqrt[3]{V/(2\pi)}$, which gives

$$
h=2r.
$$

The least material is used when the height equals the diameter, so the axial cross-section is a square.

---

## Quick Verification

For $V=2\pi$ the optimum is $r=1$, $h=2$, $S=2\pi+4\pi=6\pi\approx18.85$. Other shapes with the same volume use more: $r=0.8$ gives $S=2\pi(0.64)+\frac{4\pi}{0.8}\approx4.02+15.71=19.73$, and $r=1.2$ gives $S\approx9.05+10.47=19.52$.

---

## Common Mistakes

- **Forgetting one lid:** a closed can has two discs, $2\pi r^2$.
- **Minimizing with both variables free:** without the constraint the surface can be made arbitrarily small.
- **Answering only $r$:** the problem asks for the relation $h=2r$, which is independent of $V$.

---

## Oral Explanation (3 sentences)

The volume constraint $\pi r^2h=V$ lets us write $h=\frac{V}{\pi r^2}$ and the surface area as $S(r)=2\pi r^2+\frac{2V}{r}$. Setting $S'(r)=4\pi r-\frac{2V}{r^2}$ to zero gives $r^3=\frac{V}{2\pi}$, and since $S$ is convex this is the minimum. Substituting back gives $h=2r$: the optimal can is as tall as its diameter, so its axial cross-section is a square.

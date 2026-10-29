# Exercise 6 — Projection and Perpendicular Component

## The Problem

Find the projection of $u=(4,2)$ onto the direction $v=(1,1)$. Then compute

$$
r=u-\mathrm{proj}_v\,u
$$

and verify that $r\cdot v=0$. Explain this result geometrically.

---

## What Are We Looking For?

We want to split $u$ into a part along $v$ (the projection) and the remaining part $r$, and to see why the remaining part is perpendicular to $v$.

---

## Idea and Theorem Before the Calculation

**Orthogonal projection onto a direction $v\neq0$:**

$$
\mathrm{proj}_v\,u=\frac{u\cdot v}{v\cdot v}\,v.
$$

It is the multiple of $v$ closest to $u$, the "shadow" of $u$ on the line spanned by $v$.

---

## Step-by-Step Solution

**Step 1: Dot products.**

$$
u\cdot v=4\cdot1+2\cdot1=6,\qquad v\cdot v=1+1=2.
$$

**Step 2: Projection.**

$$
\mathrm{proj}_v\,u=\frac62(1,1)=3(1,1)=(3,3).
$$

**Step 3: Perpendicular component.**

$$
r=u-\mathrm{proj}_v\,u=(4,2)-(3,3)=(1,-1).
$$

**Step 4: Verify $r\cdot v=0$.**

$$
r\cdot v=1\cdot1+(-1)\cdot1=0.
$$

*Why this is valid:* In general,

$$
r\cdot v=u\cdot v-\frac{u\cdot v}{v\cdot v}\,v\cdot v=u\cdot v-u\cdot v=0,
$$

so the remainder is always perpendicular to $v$; the coefficient $\frac{u\cdot v}{v\cdot v}$ is chosen exactly to make this happen.

**Step 5: Geometric explanation.**

Drop a perpendicular from the tip of $u$ to the line spanned by $v$. The foot of the perpendicular is the tip of $\mathrm{proj}_v\,u=(3,3)$, and the perpendicular itself is $r=(1,-1)$. So $u$ is the sum of a part along $v$ and a part across $v$, forming a right angle, like the two legs of a right triangle whose hypotenuse is $u$.

---

## Final Answer in Words

The projection of $u$ onto $v$ is $(3,3)$, and the remaining component is $r=(1,-1)$. Since $r\cdot v=0$, the remainder is perpendicular to $v$: the projection keeps the part of $u$ along $v$, and $r$ is the part that points straight across the line of $v$.

---

## Quick Verification

The pieces must add up to $u$:

$$
(3,3)+(1,-1)=(4,2)=u.
$$

They must also satisfy the Pythagorean theorem, since they are perpendicular:

$$
\|(3,3)\|^2+\|(1,-1)\|^2=18+2=20=\|(4,2)\|^2.
$$

Both checks hold.

---

## Common Mistakes

- **Dividing by $\|v\|$ instead of $v\cdot v$:** the formula needs $\|v\|^2=2$, not $\|v\|=\sqrt2$.
- **Reporting the coefficient instead of the vector:** $3$ is the coefficient; the projection is the vector $3v=(3,3)$.
- **Computing $v-\mathrm{proj}$ instead of $u-\mathrm{proj}$:** the perpendicular component is what remains of $u$.

---

## Oral Explanation (3 sentences)

The projection of $u=(4,2)$ onto $v=(1,1)$ is $\frac{u\cdot v}{v\cdot v}v=\frac62(1,1)=(3,3)$, the part of $u$ lying along $v$. Subtracting it leaves $r=(1,-1)$, and $r\cdot v=1-1=0$, so this remaining part is perpendicular to $v$. Geometrically, $u$ is the hypotenuse of a right triangle whose legs are its shadow on the line of $v$ and the perpendicular dropped onto that line.

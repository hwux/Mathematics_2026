# Exercise 11 — Decomposition into Parallel and Perpendicular Components

## The Problem

Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check

$$
u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.
$$

Explain why these are two independent checks of correctness.

---

## What Are We Looking For?

We want to write $u$ as the sum of a vector along $v$ and a vector perpendicular to $v$, and to understand what each of the two checks confirms.

---

## Idea and Theorem Before the Calculation

**Orthogonal decomposition:**

$$
u_{\parallel}=\mathrm{proj}_v\,u=\frac{u\cdot v}{v\cdot v}\,v,\qquad u_{\perp}=u-u_{\parallel}.
$$

---

## Step-by-Step Solution

**Step 1: Dot products.**

$$
u\cdot v=3\cdot1+4\cdot2=11,\qquad v\cdot v=1+4=5.
$$

**Step 2: Parallel component.**

$$
u_{\parallel}=\frac{11}{5}(1,2)=\left(\frac{11}{5},\ \frac{22}{5}\right).
$$

**Step 3: Perpendicular component.**

$$
u_{\perp}=(3,4)-\left(\frac{11}{5},\frac{22}{5}\right)=\left(\frac{15-11}{5},\ \frac{20-22}{5}\right)=\left(\frac45,\ -\frac25\right).
$$

**Step 4: Check 1, reconstruction.**

$$
u_{\parallel}+u_{\perp}=\left(\frac{11+4}{5},\ \frac{22-2}{5}\right)=(3,4)=u.
$$

**Step 5: Check 2, perpendicularity.**

$$
u_{\perp}\cdot v=\frac45\cdot1+\left(-\frac25\right)\cdot2=\frac45-\frac45=0.
$$

**Step 6: Why the checks are independent.**

Each check tests something different:

- The reconstruction check tests that **nothing of $u$ was lost or added**. It holds for *any* split $u=x+(u-x)$, even a wrong choice of $u_{\parallel}$, because $u_{\perp}$ was defined as $u-u_{\parallel}$; so it catches arithmetic slips in the subtraction but not a wrong projection.
- The perpendicularity check tests that the split is the **right one**: among all ways to write $u$ as a multiple of $v$ plus a remainder, only the orthogonal projection leaves a remainder perpendicular to $v$.

For example, the wrong split $x=(2,4)$, $u-x=(1,0)$ passes the first check but fails the second, since $(1,0)\cdot(1,2)=1\neq0$. Only both checks together confirm the decomposition.

---

## Final Answer in Words

$u_{\parallel}=\left(\frac{11}{5},\frac{22}{5}\right)$ and $u_{\perp}=\left(\frac45,-\frac25\right)$. They add up to $u$, and $u_{\perp}\cdot v=0$. The first check confirms that the pieces add up to $u$; the second confirms that the split is the orthogonal one. A wrong parallel part can pass the first check, so both are needed.

---

## Quick Verification

The Pythagorean theorem must hold for perpendicular components:

$$
\|u_{\parallel}\|^2+\|u_{\perp}\|^2=\frac{121+484}{25}+\frac{16+4}{25}=\frac{605+20}{25}=25=\|u\|^2.
$$

Also $u_{\parallel}=\frac{11}{5}v$ is indeed a multiple of $v$, so it is parallel to $v$.

---

## Common Mistakes

- **Dividing by $\|v\|=\sqrt5$ instead of $v\cdot v=5$:** the projection coefficient is $\frac{u\cdot v}{v\cdot v}$.
- **Checking only the sum:** as shown above, a wrong decomposition can still add up to $u$.
- **Sign error in $u_{\perp}$:** $4-\frac{22}{5}=-\frac25$, a negative number.

---

## Oral Explanation (3 sentences)

The parallel component is the projection $\frac{u\cdot v}{v\cdot v}v=\frac{11}{5}(1,2)$, and subtracting it from $u$ leaves the perpendicular component $\left(\frac45,-\frac25\right)$. The two pieces add up to $(3,4)$, and the dot product of the perpendicular piece with $v$ is zero. These checks are independent, because any split into $x$ and $u-x$ adds up to $u$, but only the orthogonal projection leaves a remainder perpendicular to $v$.

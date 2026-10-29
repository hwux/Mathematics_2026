# Exercise 5 — Angle Between Vectors

## The Problem

Given $u=(1,1,0)$ and $v=(1,0,1)$:

1. Use the sign of $u\cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

---

## What Are We Looking For?

We want to predict from the sign of the dot product whether the angle is acute, right or obtuse, then compute the angle exactly and compare.

---

## Idea and Theorem Before the Calculation

**Angle formula:**

$$
\cos\theta=\frac{u\cdot v}{\|u\|\,\|v\|},\qquad 0\le\theta\le\pi.
$$

**Sign rule:** Since the lengths are positive, the sign of $\cos\theta$ is the sign of $u\cdot v$:

- $u\cdot v>0$: acute angle,
- $u\cdot v=0$: right angle,
- $u\cdot v<0$: obtuse angle.

---

## Step-by-Step Solution

**Step 1: Prediction from the sign.**

$$
u\cdot v=1\cdot1+1\cdot0+0\cdot1=1>0.
$$

The dot product is positive, so the angle should be **acute**.

**Step 2: Lengths.**

$$
\|u\|=\sqrt{1+1+0}=\sqrt2,\qquad \|v\|=\sqrt{1+0+1}=\sqrt2.
$$

**Step 3: Cosine and angle.**

$$
\cos\theta=\frac{1}{\sqrt2\cdot\sqrt2}=\frac12\quad\Longrightarrow\quad \theta=\frac{\pi}{3}=60^\circ.
$$

*Why this is valid:* On $[0,\pi]$ the cosine takes each value exactly once, and $\cos60^\circ=\frac12$.

**Step 4: Compare.**

$60^\circ$ is an acute angle, in agreement with the prediction from the sign of the dot product.

---

## Final Answer in Words

The dot product is $1>0$, which predicts an acute angle. The exact computation gives $\cos\theta=\frac12$, so $\theta=60^\circ$, which is indeed acute.

---

## Quick Verification

Check the angle geometrically. The vectors $u$, $v$ and $u-v=(0,1,-1)$ form a triangle with sides

$$
\|u\|=\sqrt2,\qquad \|v\|=\sqrt2,\qquad \|u-v\|=\sqrt{0+1+1}=\sqrt2.
$$

All three sides are equal, so the triangle is equilateral and each of its angles is $60^\circ$; in particular the angle between $u$ and $v$ is $60^\circ$.

---

## Common Mistakes

- **Forgetting to divide by the lengths:** $u\cdot v=1$ is not the cosine; the cosine is $\frac{1}{2}$.
- **Answering in the wrong unit:** $\arccos\frac12$ is $\frac{\pi}{3}$ radians, which is $60^\circ$.
- **Predicting the size of the angle from the sign:** the sign tells only whether the angle is acute, right or obtuse, not its exact value.

---

## Oral Explanation (3 sentences)

The dot product of $u=(1,1,0)$ and $v=(1,0,1)$ is $1$, which is positive, so the angle between them must be acute. Both vectors have length $\sqrt2$, so $\cos\theta=\frac{1}{2}$ and the angle is $60^\circ$. This agrees with the prediction, and it is confirmed by the fact that $u$, $v$ and $u-v$ form an equilateral triangle.

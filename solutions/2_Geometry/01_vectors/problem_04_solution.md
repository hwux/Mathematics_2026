# Exercise 4 — Dot Product and Perpendicularity

## The Problem

For $u=(1,2,-1)$ and $v=(2,-1,3)$ compute $u\cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w=(2,-1,a)$ is perpendicular to $u$, and check the result.

---

## What Are We Looking For?

We want one dot product, a decision about perpendicularity, and a value of the parameter $a$ that makes a second vector perpendicular to $u$.

---

## Idea and Theorem Before the Calculation

**Dot product:**

$$
u\cdot v=u_1v_1+u_2v_2+u_3v_3.
$$

**Perpendicularity criterion:** Two nonzero vectors are perpendicular if and only if their dot product is $0$, because $u\cdot v=\|u\|\,\|v\|\cos\theta$ and $\cos\theta=0$ exactly for $\theta=90^\circ$.

---

## Step-by-Step Solution

**Step 1: Compute $u\cdot v$.**

$$
u\cdot v=1\cdot2+2\cdot(-1)+(-1)\cdot3=2-2-3=-3.
$$

**Step 2: Decide perpendicularity.**

$u\cdot v=-3\neq0$, so $u$ and $v$ are **not** perpendicular. The negative sign means that the angle between them is obtuse.

**Step 3: Condition for $w\perp u$.**

$$
u\cdot w=1\cdot2+2\cdot(-1)+(-1)\cdot a=2-2-a=-a.
$$

Perpendicularity requires

$$
-a=0\quad\Longrightarrow\quad a=0.
$$

*Why this is valid:* The criterion turns the geometric condition "perpendicular" into one linear equation for $a$.

**Step 4: The vector $w$.**

$$
w=(2,-1,0).
$$

---

## Final Answer in Words

$u\cdot v=-3$, so $u$ and $v$ are not perpendicular (the angle between them is obtuse). The vector $w=(2,-1,a)$ is perpendicular to $u$ exactly for $a=0$, that is $w=(2,-1,0)$.

---

## Quick Verification

$$
u\cdot w=1\cdot2+2\cdot(-1)+(-1)\cdot0=2-2+0=0.
$$

The dot product is zero, so $w\perp u$. For any other value, for example $a=1$, the dot product would be $-1\neq0$, confirming that $a=0$ is the only solution.

---

## Common Mistakes

- **Concluding perpendicularity from a small dot product:** only exactly $0$ means perpendicular.
- **Sign errors:** $(-1)\cdot3=-3$ and $2\cdot(-1)=-2$.
- **Making $w$ perpendicular to $v$ instead of $u$:** the condition is $u\cdot w=0$.

---

## Oral Explanation (3 sentences)

The dot product of $u=(1,2,-1)$ and $v=(2,-1,3)$ is $2-2-3=-3$, which is not zero, so the vectors are not perpendicular. For $w=(2,-1,a)$ the dot product with $u$ is $-a$, and it vanishes only for $a=0$. The vector $w=(2,-1,0)$ indeed gives $u\cdot w=2-2+0=0$, so it is perpendicular to $u$.

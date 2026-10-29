# Exercise 8 — Linear Combination and Checking the Result

## The Problem

Check whether $w=(5,1)$ can be written as

$$
w=au+bv,
$$

where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

---

## What Are We Looking For?

We want numbers $a,b$ such that $a$ copies of $u$ plus $b$ copies of $v$ give exactly $w$, and a geometric explanation of why such numbers exist.

---

## Idea and Theorem Before the Calculation

**Linear combination as a system:** Writing $w=au+bv$ coordinate by coordinate gives a linear system for $a$ and $b$.

**Existence and uniqueness in the plane:** If $u$ and $v$ are not parallel, every vector of $\mathbb{R}^2$ can be written as $au+bv$ in exactly one way; $u$ and $v$ then form a basis of the plane.

---

## Step-by-Step Solution

**Step 1: Set up the system.**

$$
a(1,1)+b(2,-1)=(5,1)\quad\Longleftrightarrow\quad
\begin{cases}
a+2b=5, \\
a-b=1.
\end{cases}
$$

**Step 2: Solve.**

Subtract the second equation from the first:

$$
3b=4\quad\Longrightarrow\quad b=\frac43.
$$

Then from $a-b=1$:

$$
a=1+\frac43=\frac73.
$$

*Why this is valid:* The determinant of the system is $1\cdot(-1)-2\cdot1=-3\neq0$, so the solution exists and is unique.

**Step 3: Geometric meaning.**

The vectors $u=(1,1)$ and $v=(2,-1)$ point in different directions, so they are not parallel. Any point of the plane can be reached by moving some amount along $u$ and some amount along $v$, just like walking along two different streets. The numbers $a=\frac73$ and $b=\frac43$ are the coordinates of $w$ in the oblique coordinate system defined by $u$ and $v$.

---

## Final Answer in Words

Yes, $w$ is a linear combination of $u$ and $v$: $w=\frac73u+\frac43v$. Such coefficients exist, and are unique, because $u$ and $v$ are not parallel and therefore span the whole plane.

---

## Quick Verification

Reconstruct $w$:

$$
\frac73(1,1)+\frac43(2,-1)=\left(\frac73+\frac83,\ \frac73-\frac43\right)=\left(\frac{15}{3},\ \frac33\right)=(5,1)=w.
$$

The reconstruction gives exactly $w$.

---

## Common Mistakes

- **Mixing up coordinates and coefficients:** the unknowns are $a$ and $b$, while the coordinates of $u,v,w$ are known numbers.
- **Stopping after finding $b$:** both coefficients are needed.
- **Expecting integer coefficients:** fractional coefficients like $\frac73$ are perfectly valid.

---

## Oral Explanation (3 sentences)

Writing $w=au+bv$ coordinate by coordinate gives the system $a+2b=5$ and $a-b=1$, whose solution is $b=\frac43$ and $a=\frac73$. Substituting back gives $\frac73(1,1)+\frac43(2,-1)=(5,1)$, which confirms the result. Such coefficients exist because $u$ and $v$ are not parallel, so together they can reach every point of the plane, and $a,b$ are the coordinates of $w$ with respect to them.

# Exercise 9 — Cross Product as a Perpendicular Direction

## The Problem

For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

---

## What Are We Looking For?

We want the cross product of two vectors in space, a check that it is perpendicular to both of them, and the effect of reversing the order of the factors.

---

## Idea and Theorem Before the Calculation

**Cross product:**

$$
u\times v=(u_2v_3-u_3v_2,\ u_3v_1-u_1v_3,\ u_1v_2-u_2v_1).
$$

**Properties:**

- $u\times v$ is perpendicular to both $u$ and $v$;
- $v\times u=-(u\times v)$ (anticommutativity).

---

## Step-by-Step Solution

**Step 1: Compute $u\times v$.**

$$
\begin{aligned}
u\times v &= (2\cdot3-0\cdot1,\ 0\cdot0-1\cdot3,\ 1\cdot1-2\cdot0) \\
&= (6,-3,1).
\end{aligned}
$$

**Step 2: Check perpendicularity.**

$$
\begin{aligned}
(u\times v)\cdot u &= 6\cdot1+(-3)\cdot2+1\cdot0=6-6+0=0, \\
(u\times v)\cdot v &= 6\cdot0+(-3)\cdot1+1\cdot3=0-3+3=0.
\end{aligned}
$$

Both dot products are zero, so $u\times v$ is perpendicular to $u$ and to $v$.

**Step 3: Compute $v\times u$.**

$$
\begin{aligned}
v\times u &= (1\cdot0-3\cdot2,\ 3\cdot1-0\cdot0,\ 0\cdot2-1\cdot1) \\
&= (-6,3,-1).
\end{aligned}
$$

**Step 4: Compare.**

$$
v\times u=(-6,3,-1)=-(6,-3,1)=-(u\times v).
$$

The two vectors have the same length and lie on the same line, but point in opposite directions.

*Why this is valid:* Swapping $u$ and $v$ swaps the two products in each component of the formula, which changes the sign of every component.

---

## Final Answer in Words

$u\times v=(6,-3,1)$, and its dot products with $u$ and $v$ are both $0$, so it is perpendicular to both. Reversing the order gives $v\times u=(-6,3,-1)=-(u\times v)$: the same perpendicular line, the same length, the opposite orientation.

---

## Quick Verification

The length of $u\times v$ must equal $\|u\|\,\|v\|\sin\theta$. Here

$$
\|u\times v\|^2=36+9+1=46.
$$

On the other hand, $\|u\|^2\|v\|^2-(u\cdot v)^2=5\cdot10-2^2=46$, which is the same number (Lagrange's identity, equivalent to $\|u\|^2\|v\|^2\sin^2\theta$). The length agrees.

---

## Common Mistakes

- **Sign error in the middle component:** it is $u_3v_1-u_1v_3$, not $u_1v_3-u_3v_1$.
- **Assuming $u\times v=v\times u$:** the cross product changes sign when the factors are swapped.
- **Checking perpendicularity against only one vector:** the cross product must be perpendicular to both.

---

## Oral Explanation (3 sentences)

The cross product of $u=(1,2,0)$ and $v=(0,1,3)$ is $(6,-3,1)$, and its dot products with $u$ and with $v$ are both zero, so it is perpendicular to both vectors. Swapping the factors gives $v\times u=(-6,3,-1)$, which is exactly the negative of $u\times v$. So the cross product determines one perpendicular line, and the order of the factors decides which of the two directions along that line it points to.

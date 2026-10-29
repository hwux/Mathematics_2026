# Exercise 1 — Vector Operations and Their Meaning

## The Problem

For $u=(2,-1,3)$ and $v=(-1,4,2)$ compute

$$
u+v,\qquad u-v,\qquad 3u-2v.
$$

Then verify that $(u+v)-v=u$, and explain geometrically what adding two vectors means.

---

## What Are We Looking For?

We want three new vectors obtained from $u$ and $v$ by addition, subtraction and scalar multiplication, a check of one algebraic identity, and a geometric picture of vector addition.

---

## Idea and Theorem Before the Calculation

**Coordinate rules:** For vectors in $\mathbb{R}^3$ and a number $c$,

$$
(u_1,u_2,u_3)\pm(v_1,v_2,v_3)=(u_1\pm v_1,\ u_2\pm v_2,\ u_3\pm v_3),\qquad c(u_1,u_2,u_3)=(cu_1,\ cu_2,\ cu_3).
$$

Every operation is carried out coordinate by coordinate.

---

## Step-by-Step Solution

**Step 1: $u+v$.**

$$
u+v=(2+(-1),\ -1+4,\ 3+2)=(1,3,5).
$$

**Step 2: $u-v$.**

$$
u-v=(2-(-1),\ -1-4,\ 3-2)=(3,-5,1).
$$

**Step 3: $3u-2v$.**

First the scalar multiples:

$$
3u=(6,-3,9),\qquad 2v=(-2,8,4).
$$

Then the difference:

$$
3u-2v=(6-(-2),\ -3-8,\ 9-4)=(8,-11,5).
$$

**Step 4: Verify $(u+v)-v=u$.**

$$
(u+v)-v=(1,3,5)-(-1,4,2)=(1+1,\ 3-4,\ 5-2)=(2,-1,3)=u.
$$

*Why this is valid:* Subtracting $v$ undoes adding $v$ in every coordinate, so the original vector $u$ returns.

**Step 5: Geometric meaning of addition.**

Draw $u$ as an arrow, then draw $v$ starting at the tip of $u$. The sum $u+v$ is the arrow from the start of $u$ to the tip of $v$: performing the displacement $u$ and then the displacement $v$ has the same effect as the single displacement $u+v$. Equivalently, if $u$ and $v$ start at the same point, $u+v$ is the diagonal of the parallelogram they span.

---

## Final Answer in Words

$u+v=(1,3,5)$, $u-v=(3,-5,1)$ and $3u-2v=(8,-11,5)$. The identity $(u+v)-v=u$ holds, since subtracting $v$ cancels adding $v$ coordinate by coordinate. Adding two vectors means performing one displacement after the other; the sum is the total displacement, the diagonal of the parallelogram spanned by the two vectors.

---

## Quick Verification

Check Step 3 in a different order: $3u-2v=(u-v)+2u-v$, and also $3u-2v=3(u-v)+v$. Using the second form:

$$
3(3,-5,1)+(-1,4,2)=(9-1,\ -15+4,\ 3+2)=(8,-11,5).
$$

This is the same result obtained by a different route.

---

## Common Mistakes

- **Sign errors with negative coordinates:** $2-(-1)=3$, not $1$.
- **Multiplying only one coordinate by the scalar:** $3u$ multiplies all three coordinates by $3$.
- **Thinking $u-v$ points from $u$ to $v$:** $u-v$ points from the tip of $v$ to the tip of $u$ when both start at the same point.

---

## Oral Explanation (3 sentences)

Vectors are added, subtracted and multiplied by numbers coordinate by coordinate, which gives $u+v=(1,3,5)$, $u-v=(3,-5,1)$ and $3u-2v=(8,-11,5)$. Subtracting $v$ from $u+v$ cancels the addition in every coordinate, so $(u+v)-v=u$. Geometrically, adding vectors means following one displacement by the other, and the sum is the diagonal of the parallelogram spanned by the two vectors.

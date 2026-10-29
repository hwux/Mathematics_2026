# Exercise 13 — Do Four Points Lie in One Plane?

## The Problem

Given

$$
A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).
$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

---

## What Are We Looking For?

We want to decide whether the fourth point $D$ lies in the plane through $A$, $B$ and $C$, using a normal vector of that plane.

---

## Idea and Theorem Before the Calculation

**Coplanarity criterion:** If $n$ is a normal vector of the plane through $A,B,C$, then a point $D$ lies in this plane if and only if

$$
\overrightarrow{AD}\cdot n=0.
$$

The value $\overrightarrow{AD}\cdot n=\overrightarrow{AD}\cdot(\overrightarrow{AB}\times\overrightarrow{AC})$ is the scalar triple product, whose absolute value is the volume of the parallelepiped spanned by the three vectors.

---

## Step-by-Step Solution

**Step 1: Vectors from $A$.**

$$
\overrightarrow{AB}=(1,2,0),\qquad \overrightarrow{AC}=(0,1,1).
$$

**Step 2: Normal vector.**

$$
\begin{aligned}
n=\overrightarrow{AB}\times\overrightarrow{AC} &= (2\cdot1-0\cdot1,\ 0\cdot0-1\cdot1,\ 1\cdot1-2\cdot0) \\
&= (2,-1,1).
\end{aligned}
$$

**Step 3: The vector $\overrightarrow{AD}$ and the test.**

$$
\overrightarrow{AD}=(2,5,1),
$$

$$
\overrightarrow{AD}\cdot n=2\cdot2+5\cdot(-1)+1\cdot1=4-5+1=0.
$$

**Step 4: Decide and justify.**

The dot product is $0$, so $D$ **lies in the plane** of $A$, $B$, $C$.

*Justification of the criterion:* $n$ is perpendicular to the plane through $A$. A point $D$ is in this plane exactly when the displacement $\overrightarrow{AD}$ runs within the plane, which is exactly when it has no component along the normal, that is, when $\overrightarrow{AD}\cdot n=0$. Equivalently, the parallelepiped spanned by $\overrightarrow{AB}$, $\overrightarrow{AC}$, $\overrightarrow{AD}$ has volume $0$, so it is flat.

---

## Final Answer in Words

$\overrightarrow{AB}=(1,2,0)$, $\overrightarrow{AC}=(0,1,1)$, $n=(2,-1,1)$ and $\overrightarrow{AD}=(2,5,1)$. Since $\overrightarrow{AD}\cdot n=0$, the point $D$ lies in the plane determined by $A$, $B$ and $C$: the vector from $A$ to $D$ has no component perpendicular to the plane.

---

## Quick Verification

If $D$ is in the plane, $\overrightarrow{AD}$ must be a combination of $\overrightarrow{AB}$ and $\overrightarrow{AC}$. Indeed,

$$
2\overrightarrow{AB}+\overrightarrow{AC}=(2,4,0)+(0,1,1)=(2,5,1)=\overrightarrow{AD}.
$$

So $D=A+2\overrightarrow{AB}+\overrightarrow{AC}$ is reached by moving only along directions of the plane. Also, the plane equation $2x-y+z=0$ (normal $n$, through the origin $A$) holds for $D$: $4-5+1=0$.

---

## Common Mistakes

- **Testing $D$ itself instead of $\overrightarrow{AD}$:** the criterion uses the displacement from a point of the plane; it works with $D$ here only because $A$ is the origin.
- **Concluding "not coplanar" from a nonzero cross product:** the cross product is just the normal; the decision comes from the dot product with $\overrightarrow{AD}$.
- **Sign errors in the cross product:** the middle component is $0\cdot0-1\cdot1=-1$.

---

## Oral Explanation (3 sentences)

The cross product of $\overrightarrow{AB}=(1,2,0)$ and $\overrightarrow{AC}=(0,1,1)$ is the normal vector $n=(2,-1,1)$ of the plane through $A$, $B$, $C$. The vector $\overrightarrow{AD}=(2,5,1)$ has dot product $4-5+1=0$ with this normal, so it lies within the plane and $D$ is a point of the plane. This is confirmed by $\overrightarrow{AD}=2\overrightarrow{AB}+\overrightarrow{AC}$, which shows that $D$ can be reached from $A$ using only directions of the plane.

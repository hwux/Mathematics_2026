# Exercise 14 — Rotation Matrices

## The Problem

The matrix for a rotation through an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{pmatrix}.
$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that

$$
R(\alpha)R(\beta)=R(\alpha+\beta).
$$

Explain the result geometrically.

---

## What Are We Looking For?

We want to multiply two rotation matrices symbolically, recognize the angle-sum formulas in the entries, and connect the algebraic identity with the geometric fact that two successive rotations form one rotation.

---

## Idea and Theorem Before the Calculation

**Angle-sum formulas:**

$$
\begin{aligned}
\cos(\alpha+\beta) &= \cos\alpha\cos\beta-\sin\alpha\sin\beta, \\
\sin(\alpha+\beta) &= \sin\alpha\cos\beta+\cos\alpha\sin\beta.
\end{aligned}
$$

**Composition:** $R(\alpha)R(\beta)x$ means: first rotate $x$ by $\beta$, then rotate the result by $\alpha$.

---

## Step-by-Step Solution

**Step 1: Multiply the matrices.**

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha \\
\end{pmatrix}
\begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta \\
\end{pmatrix}.
$$

Entry by entry:

$$
\begin{aligned}
(1,1):&\quad \cos\alpha\cos\beta-\sin\alpha\sin\beta, \\
(1,2):&\quad -\cos\alpha\sin\beta-\sin\alpha\cos\beta, \\
(2,1):&\quad \sin\alpha\cos\beta+\cos\alpha\sin\beta, \\
(2,2):&\quad -\sin\alpha\sin\beta+\cos\alpha\cos\beta.
\end{aligned}
$$

**Step 2: Apply the angle-sum formulas.**

- Entry $(1,1)$ is exactly $\cos(\alpha+\beta)$.
- Entry $(2,1)$ is exactly $\sin(\alpha+\beta)$.
- Entry $(1,2)$ equals $-\left(\sin\alpha\cos\beta+\cos\alpha\sin\beta\right)=-\sin(\alpha+\beta)$.
- Entry $(2,2)$ equals $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.

*Why this is valid:* Each entry is rearranged only by reordering terms or taking out a common minus sign, and then matched with one of the two angle-sum formulas.

**Step 3: Conclude.**

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta) \\
\end{pmatrix}=R(\alpha+\beta).
$$

**Step 4: Geometric explanation.**

Rotating a vector first by $\beta$ and then by $\alpha$ turns it about the origin by a total angle of $\alpha+\beta$, and this is the same as one rotation by $\alpha+\beta$. The matrix product describes the composition of the two rotations, so it must be the matrix of the total rotation.

A consequence: since $\alpha+\beta=\beta+\alpha$,

$$
R(\alpha)R(\beta)=R(\beta)R(\alpha).
$$

Rotations about the same point commute, even though matrix multiplication is not commutative in general.

---

## Final Answer in Words

Multiplying the two rotation matrices produces entries that are exactly the angle-sum expressions for $\cos(\alpha+\beta)$ and $\sin(\alpha+\beta)$, so $R(\alpha)R(\beta)=R(\alpha+\beta)$. Geometrically, rotating by $\beta$ and then by $\alpha$ is one rotation by $\alpha+\beta$; in particular, rotations about the origin commute.

---

## Quick Verification

Take $\alpha=\beta=90^\circ$. Since $\cos90^\circ=0$ and $\sin90^\circ=1$,

$$
R(90^\circ)R(90^\circ)=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix} =
\begin{pmatrix}
-1 & 0 \\
0 & -1 \\
\end{pmatrix}.
$$

On the other hand, $\cos180^\circ=-1$ and $\sin180^\circ=0$, so $R(180^\circ)$ is the same matrix. Two quarter turns give a half turn, as the formula predicts.

---

## Common Mistakes

- **Sign errors in the top-right entry:** both products in entry $(1,2)$ are negative, which gives $-\sin(\alpha+\beta)$.
- **Mixing up the two angle-sum formulas:** the cosine formula has a minus sign between the products, the sine formula a plus sign.
- **Generalizing commutativity:** rotations about the same point commute, but this does not mean that matrices commute in general (compare Exercise 9).

---

## Oral Explanation (3 sentences)

Multiplying $R(\alpha)$ by $R(\beta)$ gives entries such as $\cos\alpha\cos\beta-\sin\alpha\sin\beta$ and $\sin\alpha\cos\beta+\cos\alpha\sin\beta$, which are exactly $\cos(\alpha+\beta)$ and $\sin(\alpha+\beta)$ by the angle-sum formulas. Therefore the product is the rotation matrix $R(\alpha+\beta)$. Geometrically this says that turning by $\beta$ and then by $\alpha$ is the same as turning once by the total angle, which also explains why two rotations about the origin can be performed in either order.

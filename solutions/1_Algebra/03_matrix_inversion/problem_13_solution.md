# Exercise 13 — Undoing a Composite Transformation

## The Problem

The matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

---

## What Are We Looking For?

We want the inverse of the composite transformation $T=HS$, computed directly and through the product rule, and a comparison with the product of the inverses in the wrong order.

---

## Idea and Theorem Before the Calculation

**Composition:** $Tx=H(Sx)$ means: first scale with $S$, then shear with $H$.

**Inverse of a product:** $(HS)^{-1}=S^{-1}H^{-1}$.

**Inverses of the factors:**

- $S$ doubles the $x$-coordinate, so $S^{-1}$ halves it.
- $H$ maps $(x,y)^T$ to $(x+y,y)^T$, so $H^{-1}$ maps $(x,y)^T$ to $(x-y,y)^T$.

---

## Step-by-Step Solution

**Method 1: Compute $T$, then invert.**

$$
T=HS=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
2 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

$\det T=2\cdot1-1\cdot0=2$, so

$$
T^{-1}=\frac12
\begin{pmatrix}
1 & -1 \\
0 & 2 \\
\end{pmatrix} =
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

**Method 2: Use $(HS)^{-1}=S^{-1}H^{-1}$.**

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

$$
S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

Both methods give the same matrix.

**The incorrect order.**

$$
H^{-1}S^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
\frac12 & -1 \\
0 & 1 \\
\end{pmatrix}.
$$

The top-right entry is $-1$ instead of $-\frac12$, so $H^{-1}S^{-1}\neq T^{-1}$.

**Explaining the rule.**

$T$ first scales and then shears. To return to the starting point, the shear, which was performed last, must be undone first with $H^{-1}$, and only then the scaling with $S^{-1}$. Applied to a vector this is $S^{-1}(H^{-1}x)$, that is, the matrix $S^{-1}H^{-1}$. The order $H^{-1}S^{-1}$ would try to undo the scaling while the shear is still in effect, which does not restore the original vector.

---

## Final Answer in Words

$T=HS$ has rows $(2,1)$ and $(0,1)$, and both methods give

$$
T^{-1}=S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1 \\
\end{pmatrix}.
$$

The wrong order $H^{-1}S^{-1}$ gives a different matrix with top-right entry $-1$. Operations are undone from the end: the last operation, the shear, is undone first.

---

## Quick Verification

Follow the vector $x=(1,1)^T$:

$$
Sx=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\qquad Tx=H(Sx)=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix}.
$$

Undoing in the correct order: $H^{-1}(3,1)^T=(2,1)^T$, then $S^{-1}(2,1)^T=(1,1)^T$. The original vector is recovered.

Undoing in the wrong order: $S^{-1}(3,1)^T=(\frac32,1)^T$, then $H^{-1}(\frac32,1)^T=(\frac12,1)^T\neq(1,1)^T$. The original vector is not recovered.

---

## Common Mistakes

- **Writing $(HS)^{-1}=H^{-1}S^{-1}$:** the factors must appear in reverse order.
- **Confusing which transformation acts first:** in $HSx$ the matrix $S$ acts first, because it stands next to $x$.
- **Inverting the shear incorrectly:** the inverse of adding $y$ to $x$ is subtracting $y$ from $x$, so the off-diagonal entry changes sign.

---

## Oral Explanation (3 sentences)

The composite transformation $T=HS$ first scales and then shears, and its inverse computed directly equals $S^{-1}H^{-1}$, with rows $(\frac12,-\frac12)$ and $(0,1)$. The product in the other order, $H^{-1}S^{-1}$, has a different top-right entry and fails to bring the vector $(3,1)^T$ back to $(1,1)^T$. This illustrates the rule that a sequence of operations is undone from the end: the shear performed last must be undone first.

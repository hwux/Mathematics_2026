# Exercise 9 — Composing Transformations

## The Problem

Let

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For

$$
x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

---

## What Are We Looking For?

We want to apply two geometric transformations to the same vector in two different orders and see whether the final result depends on which transformation is applied first.

---

## Idea and Theorem Before the Calculation

**Composition of transformations:** Applying transformation $S$ and then $R$ corresponds to computing $R(Sx) = (RS)x$. The rightmost matrix acts first on the vector.

**Rotation by $90^\circ$ counterclockwise:** A rotation by $90^\circ$ counterclockwise sends $(a,b)^T$ to $(-b,a)^T$. The matrix $R$ above implements this.

**Nonuniform scaling:** The matrix $S$ doubles the $x$-component and keeps the $y$-component, mapping $(a,b)^T$ to $(2a,b)^T$.

Matrix multiplication is not commutative in general, so $RSx$ and $SRx$ may differ. Whether they differ for this particular pair is decided by computing both.

---

## Step-by-Step Solution

**Step 1 — Compute $RSx$ (scale first, then rotate).**

First apply $S$ to $x$:

$$
Sx=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix} =
\begin{pmatrix}
2\cdot1+0\cdot2 \\
0\cdot1+1\cdot2 \\
\end{pmatrix} =
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}.
$$

The vector is now $(2,2)^T$: the $x$-component was doubled, the $y$-component unchanged.

Then apply $R$ to $Sx$:

$$
RSx=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix} =
\begin{pmatrix}
0\cdot2+(-1)\cdot2 \\
1\cdot2+0\cdot2 \\
\end{pmatrix} =
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}.
$$

*Why valid:* The matrix $RS$ is applied to $x$ by first letting $S$ act, then $R$. The intermediate vector $(2,2)^T$ is the image under scaling before rotation.

**Step 2 — Compute $SRx$ (rotate first, then scale).**

First apply $R$ to $x$:

$$
Rx=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix} =
\begin{pmatrix}
0\cdot1+(-1)\cdot2 \\
1\cdot1+0\cdot2 \\
\end{pmatrix} =
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}.
$$

The vector $(1,2)^T$ has been rotated $90^\circ$ counterclockwise to $(-2,1)^T$.

Then apply $S$ to $Rx$:

$$
SRx=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix} =
\begin{pmatrix}
2\cdot(-2)+0\cdot1 \\
0\cdot(-2)+1\cdot1 \\
\end{pmatrix} =
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}.
$$

**Step 3 — Compare.**

$$
RSx=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
\neq
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
= SRx.
$$

The two results are different.

---

## Geometric Explanation

**$RSx$:** Start with $(1,2)^T$. Scale first: the $x$-component doubles, giving $(2,2)^T$, a vector pointing equally along both axes at $45^\circ$. Rotating $90^\circ$ counterclockwise then yields $(-2,2)^T$.

**$SRx$:** Start with $(1,2)^T$. Rotate first: the vector swings $90^\circ$ counterclockwise, landing at $(-2,1)^T$, which now points mostly in the negative $x$-direction. Then scaling doubles the $x$-component (which is negative), giving $(-4,1)^T$.

The scaling always stretches along the fixed horizontal axis. In $RSx$ it stretches the original horizontal component $1$ of $x$, which becomes $2$. In $SRx$ the rotation has already moved the original vertical component $2$ onto the horizontal axis (as $-2$), so the scaling stretches that component instead, giving $-4$. The two orders stretch different parts of the original vector, which is why the results differ.

---

## Final Answer in Words

$RSx = (-2,2)^T$ (scale then rotate) and $SRx = (-4,1)^T$ (rotate then scale). The two are different, confirming that $RS \neq SR$ and that the composition of geometric transformations is order-dependent.

---

## Quick Verification

Compute $RS$ directly:

$$
RS=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix}.
$$

Apply to $x$: $(0\cdot1+(-1)\cdot2,\;2\cdot1+0\cdot2)^T = (-2,2)^T$. Matches Step 1.

Compute $SR$ directly:

$$
SR=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix} =
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}.
$$

Apply to $x$: $(0\cdot1+(-2)\cdot2,\;1\cdot1+0\cdot2)^T = (-4,1)^T$. Matches Step 2.

---

## Common Mistakes

- **Thinking the rightmost matrix acts last:** in $RSx$, read right to left — $S$ acts first on $x$, then $R$ acts on the result.
- **Assuming geometric transformations always commute:** this example is a direct counterexample. Rotation and scaling along fixed axes generally do not commute.
- **Multiplying the matrices in the wrong order:** computing $SR$ when $RSx$ is required gives the matrix of the other composition and therefore the wrong vector.

---

## Oral Explanation (3 sentences)

Applying two transformations to a vector is like performing two actions in sequence: the matrix written on the right acts first, and the one on the left acts second. In this example, scaling first and then rotating gives $(-2,2)^T$, while rotating first and then scaling gives $(-4,1)^T$ — the results are genuinely different because scaling is tied to fixed coordinate axes, and whether the vector has been rotated before scaling changes which geometric direction gets stretched. This is the geometric meaning of noncommutativity: two transformations that change the shape and orientation of space in different ways generally produce different outcomes depending on which is applied first.


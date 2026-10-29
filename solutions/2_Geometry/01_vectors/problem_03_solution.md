# Exercise 3 — Vector Normalization

## The Problem

For $v=(3,4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ in the form $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

---

## What Are We Looking For?

We want the vector of length $1$ that points exactly the same way as $v$, a check of its length, and a description of what normalization changes.

---

## Idea and Theorem Before the Calculation

**Normalization:** For a nonzero vector $v$,

$$
e=\frac{v}{\|v\|}
$$

has length $1$, because $\|cv\|=|c|\,\|v\|$ and here $c=\frac{1}{\|v\|}>0$. Dividing by a positive number keeps both the direction and the orientation.

---

## Step-by-Step Solution

**Step 1: Length of $v$.**

$$
\|v\|=\sqrt{3^2+4^2}=\sqrt{25}=5.
$$

**Step 2: Divide by the length.**

$$
e=\frac{v}{\|v\|}=\frac15(3,4)=\left(\frac35,\frac45\right).
$$

*Why this is valid:* Dividing by the positive number $5$ shrinks the vector without turning or reversing it.

**Step 3: Check $\|e\|=1$.**

$$
\|e\|=\sqrt{\frac{9}{25}+\frac{16}{25}}=\sqrt{\frac{25}{25}}=1.
$$

**Step 4: Reconstruct $v$.**

$$
\|v\|e=5\left(\frac35,\frac45\right)=(3,4)=v.
$$

**Step 5: What changes and what stays the same.**

- **Changes:** the length, from $5$ to $1$.
- **Unchanged:** the direction (the line along which the vector points) and the orientation (which way along that line it points). Also the ratio of the coordinates stays $3:4$.

---

## Final Answer in Words

The unit vector is $e=\left(\frac35,\frac45\right)$. Its length is $1$, and $v=5e$. Normalization changes only the length of the vector; its direction and orientation remain the same.

---

## Quick Verification

The angle that $e$ makes with the $x$-axis must equal the angle of $v$. For both vectors the ratio of the coordinates is the same:

$$
\frac{4/5}{3/5}=\frac43=\frac{4}{3},
$$

so they have the same slope, and both coordinates are positive, so they point into the same quadrant.

---

## Common Mistakes

- **Dividing by the sum of the coordinates:** dividing by $3+4=7$ gives $\left(\frac37,\frac47\right)$, whose length is not $1$.
- **Dividing by a negative number:** this would reverse the orientation.
- **Forgetting the square root in the length:** $\|v\|=5$, not $25$.

---

## Oral Explanation (3 sentences)

The length of $v=(3,4)$ is $5$, so dividing $v$ by $5$ gives the unit vector $e=\left(\frac35,\frac45\right)$. Its length is $\sqrt{\frac{9}{25}+\frac{16}{25}}=1$, and multiplying it back by $5$ recovers $v$. Normalization only rescales the vector to length $1$; because the scaling factor is positive, the direction and orientation stay exactly the same.

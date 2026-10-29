# Exercise 15 — Comparing Directions Using the Cosine of the Angle

## The Problem

Given

$$
a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).
$$

For each pair, compute

$$
\frac{u\cdot v}{\|u\|\,\|v\|}.
$$

Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

---

## What Are We Looking For?

We want the cosine of the angle for each of the three pairs, the pairs ordered from smallest to largest angle, and an explanation of why two vectors of different lengths can give cosine $1$.

---

## Idea and Theorem Before the Calculation

**Cosine of the angle:**

$$
\cos\theta=\frac{u\cdot v}{\|u\|\,\|v\|},\qquad 0\le\theta\le\pi.
$$

**Ordering:** On $[0,\pi]$ the cosine is decreasing, so a larger cosine means a smaller angle.

---

## Step-by-Step Solution

**Step 1: Lengths.**

$$
\|a\|=\sqrt{1+4+1}=\sqrt6,\qquad \|b\|=\sqrt{4+16+4}=\sqrt{24}=2\sqrt6,\qquad \|c\|=\sqrt{4+0+9}=\sqrt{13}.
$$

**Step 2: Pair $(a,b)$.**

$$
a\cdot b=2+8+2=12,\qquad \frac{12}{\sqrt6\cdot2\sqrt6}=\frac{12}{12}=1.
$$

**Step 3: Pair $(a,c)$.**

$$
a\cdot c=2+0+3=5,\qquad \frac{5}{\sqrt6\cdot\sqrt{13}}=\frac{5}{\sqrt{78}}\approx0.566.
$$

**Step 4: Pair $(b,c)$.**

$$
b\cdot c=4+0+6=10,\qquad \frac{10}{2\sqrt6\cdot\sqrt{13}}=\frac{5}{\sqrt{78}}\approx0.566.
$$

**Step 5: Order by increasing angle.**

| Pair | Cosine | Angle |
|------|--------|-------|
| $(a,b)$ | $1$ | $0^\circ$ |
| $(a,c)$ | $\frac{5}{\sqrt{78}}$ | $\approx55.5^\circ$ |
| $(b,c)$ | $\frac{5}{\sqrt{78}}$ | $\approx55.5^\circ$ |

The pair $(a,b)$ has the smallest angle. The pairs $(a,c)$ and $(b,c)$ are tied, with the same larger angle.

**Step 6: Why the value is $1$ for $a$ and $b$.**

$b=2a$, so $b$ points in exactly the same direction as $a$ and is only twice as long. The formula divides the dot product by both lengths, which removes the effect of length:

$$
\frac{a\cdot(2a)}{\|a\|\cdot\|2a\|}=\frac{2\|a\|^2}{2\|a\|^2}=1.
$$

The cosine measures only direction, so two vectors with the same direction give $\cos\theta=1$, that is $\theta=0^\circ$, whatever their lengths.

*Why this is valid:* The same argument explains the tie: since $b=2a$, the pair $(b,c)$ makes the same angle with $c$ as the pair $(a,c)$.

---

## Final Answer in Words

The cosines are $1$ for $(a,b)$ and $\frac{5}{\sqrt{78}}\approx0.566$ for both $(a,c)$ and $(b,c)$. By increasing angle: first $(a,b)$ with $0^\circ$, then $(a,c)$ and $(b,c)$, tied at about $55.5^\circ$. For $a$ and $b$ the value is $1$ because $b=2a$ points in the same direction, and dividing by the lengths removes the difference in size.

---

## Quick Verification

Scaling one vector by a positive number never changes the cosine, which explains both the value $1$ and the tie. Numerically, $\arccos\frac{5}{\sqrt{78}}$: since $\sqrt{78}\approx8.832$, the cosine is $\approx0.5661$, and $\cos55.5^\circ\approx0.5664$, consistent with the table.

---

## Common Mistakes

- **Ordering by the dot product instead of the cosine:** $b\cdot c=10>a\cdot c=5$, but the angles are equal; lengths must be taken into account.
- **Ordering by increasing cosine:** a larger cosine means a smaller angle.
- **Thinking vectors of different lengths cannot have angle $0^\circ$:** the angle depends only on direction.

---

## Oral Explanation (3 sentences)

The cosine of the angle is $1$ for the pair $(a,b)$ and $\frac{5}{\sqrt{78}}\approx0.566$ for both $(a,c)$ and $(b,c)$, so the smallest angle, $0^\circ$, is between $a$ and $b$, and the other two pairs are tied at about $55.5^\circ$. The value for $a$ and $b$ is exactly $1$ because $b=2a$ points in the same direction, and the formula divides out the lengths. For the same reason, replacing $a$ by $b=2a$ does not change the angle with $c$, which explains the tie.

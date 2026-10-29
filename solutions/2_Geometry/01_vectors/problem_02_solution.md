# Exercise 2 — Distance as the Length of a Vector

## The Problem

The points are $A=(1,2,3)$ and $B=(4,-2,6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

---

## What Are We Looking For?

We want the vector from $A$ to $B$, its length, the distance between the points from the coordinate formula, and an explanation of why these two numbers coincide.

---

## Idea and Theorem Before the Calculation

**Vector between two points:** $\overrightarrow{AB}=B-A$, the displacement that moves $A$ to $B$.

**Length of a vector:**

$$
\|w\|=\sqrt{w_1^2+w_2^2+w_3^2}.
$$

**Distance between points:**

$$
d(A,B)=\sqrt{(b_1-a_1)^2+(b_2-a_2)^2+(b_3-a_3)^2}.
$$

---

## Step-by-Step Solution

**Step 1: Construct $\overrightarrow{AB}$.**

$$
\overrightarrow{AB}=B-A=(4-1,\ -2-2,\ 6-3)=(3,-4,3).
$$

**Step 2: Length of $\overrightarrow{AB}$.**

$$
\|\overrightarrow{AB}\|=\sqrt{3^2+(-4)^2+3^2}=\sqrt{9+16+9}=\sqrt{34}.
$$

**Step 3: Distance from the coordinate formula.**

$$
d(A,B)=\sqrt{(4-1)^2+(-2-2)^2+(6-3)^2}=\sqrt{9+16+9}=\sqrt{34}.
$$

**Step 4: Why the results agree.**

The numbers under the square root in Step 3 are exactly the squared coordinates of $\overrightarrow{AB}$. The distance formula is nothing else than the length of the displacement vector $B-A$ written out in coordinates. Geometrically, the distance between two points is the length of the arrow joining them.

*Why this is valid:* Both formulas come from the Pythagorean theorem applied in three dimensions to the coordinate differences.

---

## Final Answer in Words

$\overrightarrow{AB}=(3,-4,3)$, its length is $\sqrt{34}$, and the distance between $A$ and $B$ is also $\sqrt{34}\approx5.83$. The results agree because the distance formula is the length formula applied to the vector $B-A$.

---

## Quick Verification

Going back from $A$ along $\overrightarrow{AB}$ must reach $B$:

$$
A+\overrightarrow{AB}=(1+3,\ 2-4,\ 3+3)=(4,-2,6)=B.
$$

The vector in the opposite direction, $\overrightarrow{BA}=(-3,4,-3)$, has the same length $\sqrt{34}$, as distance does not depend on the order of the points.

---

## Common Mistakes

- **Computing $A-B$ and calling it $\overrightarrow{AB}$:** the vector from $A$ to $B$ is $B-A$; the opposite vector has the same length but the opposite direction.
- **Forgetting to square the negative coordinate:** $(-4)^2=16$, not $-16$.
- **Forgetting the square root:** $34$ is the squared length; the length is $\sqrt{34}$.

---

## Oral Explanation (3 sentences)

The vector from $A$ to $B$ is the difference $B-A=(3,-4,3)$, and its length is $\sqrt{9+16+9}=\sqrt{34}$. The coordinate distance formula gives exactly the same expression, because it squares the same three coordinate differences. Both calculations measure the length of the arrow from $A$ to $B$, so they must give the same result.

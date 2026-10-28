# Exercise 3 — Swapping Two Rows

## The Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

---

## What Are We Looking For?

We need $\det A$, then a prediction of $\det B$ that uses only a property of the determinant, and finally a direct calculation of $\det B$ that confirms or rejects the prediction.

---

## Idea and Theorem Before the Calculation

**Row swap property:** Interchanging two rows of a square matrix multiplies its determinant by $-1$. The absolute value stays the same; only the sign changes.

**Sarrus' rule** is used for both direct calculations (see Exercise 2).

---

## Step-by-Step Solution

**Step 1: Compute $\det A$ with Sarrus' rule.**

Downward products:

$$
1\cdot3\cdot1+2\cdot1\cdot2+0\cdot0\cdot1 = 3+4+0 = 7.
$$

Upward products:

$$
0\cdot3\cdot2+1\cdot1\cdot1+2\cdot0\cdot1 = 0+1+0 = 1.
$$

Therefore

$$
\det A = 7-1 = 6.
$$

**Step 2: Form $B$.**

Swapping the first and second rows of $A$ gives

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}.
$$

**Step 3: Predict $\det B$.**

$B$ arises from $A$ by one row swap, so

$$
\det B = -\det A = -6.
$$

*Why this is valid:* Every row swap reverses the sign of the determinant, and exactly one swap was performed.

**Step 4: Verify by calculation.**

Downward products for $B$:

$$
0\cdot2\cdot1+3\cdot0\cdot2+1\cdot1\cdot1 = 0+0+1 = 1.
$$

Upward products for $B$:

$$
1\cdot2\cdot2+0\cdot0\cdot1+3\cdot1\cdot1 = 4+0+3 = 7.
$$

Therefore

$$
\det B = 1-7 = -6.
$$

The calculation confirms the prediction.

---

## Final Answer in Words

$\det A=6$. The matrix $B$, obtained by swapping the first two rows, has $\det B=-6$, exactly as predicted by the row swap property.

---

## Quick Verification

Compare the two Sarrus calculations: the downward sum of $B$ equals the upward sum of $A$ (both are $1$), and the upward sum of $B$ equals the downward sum of $A$ (both are $7$). The swap exchanged the roles of the two groups of products, which is precisely why the sign of the difference reversed.

---

## Common Mistakes

- **Thinking a row swap leaves the determinant unchanged:** it changes the sign.
- **Applying the sign change twice by mistake:** one swap gives one factor $-1$; two swaps would restore the original sign.
- **Confusing a swap with a row replacement:** $R_i\leftarrow R_i+cR_j$ does not change the determinant, while $R_i\leftrightarrow R_j$ does.

---

## Oral Explanation (3 sentences)

The determinant of $A$ computed with Sarrus' rule is $7-1=6$. Swapping two rows of a matrix multiplies its determinant by $-1$, so the matrix $B$ with the first two rows interchanged must have determinant $-6$. A direct calculation gives $1-7=-6$, because the swap turns the downward diagonal products of $A$ into the upward ones of $B$ and vice versa.

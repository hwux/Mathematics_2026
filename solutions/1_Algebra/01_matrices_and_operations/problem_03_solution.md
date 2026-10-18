# Exercise 3 — When Can Matrices Be Multiplied?

## The Problem

The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

---

## What Are We Looking For?

We want to know, for each pair of matrices, whether the multiplication can be performed at all, and if yes, what size the resulting matrix has.

---

## Idea and Theorem Before the Calculation

**Dimension compatibility condition:** The product $PQ$ is defined if and only if the number of columns of $P$ equals the number of rows of $Q$. If $P$ is $m\times k$ and $Q$ is $k\times n$, then $PQ$ is $m\times n$.

A helpful way to remember: write the sizes side by side. If the inner numbers match, the product exists; the outer numbers give the result size.

$$
\underbrace{P}_{m\times k}\;\underbrace{Q}_{k\times n} \;\Longrightarrow\; PQ \;\mathrm{is}\; m\times n.
$$

---

## Step-by-Step Solution

For each product, write the sizes of the two factors side by side and check whether the inner numbers agree.

**$AB$:** $A$ is $2\times3$, $B$ is $3\times4$. Inner numbers: $3$ and $3$ — they match. Result: $2\times4$. **Defined.**

*Why:* Each row of $A$ has 3 entries and each column of $B$ has 3 entries, so the dot product that produces each entry of $AB$ is well-formed.

**$BA$:** $B$ is $3\times4$, $A$ is $2\times3$. Inner numbers: $4$ and $2$ — they do not match. **Not defined.**

*Why:* $B$ has 4 columns but $A$ has only 2 rows, so there is no pairing between the entries.

**$BC$:** $B$ is $3\times4$, $C$ is $4\times2$. Inner numbers: $4$ and $4$ — match. Result: $3\times2$. **Defined.**

**$CB$:** $C$ is $4\times2$, $B$ is $3\times4$. Inner numbers: $2$ and $3$ — do not match. **Not defined.**

**$AC$:** $A$ is $2\times3$, $C$ is $4\times2$. Inner numbers: $3$ and $4$ — do not match. **Not defined.**

**$CA$:** $C$ is $4\times2$, $A$ is $2\times3$. Inner numbers: $2$ and $2$ — match. Result: $4\times3$. **Defined.**

**$AD$:** $A$ is $2\times3$, $D$ is $2\times2$. Inner numbers: $3$ and $2$ — do not match. **Not defined.**

**$DA$:** $D$ is $2\times2$, $A$ is $2\times3$. Inner numbers: $2$ and $2$ — match. Result: $2\times3$. **Defined.**

---

## Final Answer in Words

| Product | Inner numbers | Defined? | Result size |
|---------|--------------|----------|-------------|
| $AB$ | $3 = 3$ | Yes | $2\times4$ |
| $BA$ | $4 \neq 2$ | No | — |
| $BC$ | $4 = 4$ | Yes | $3\times2$ |
| $CB$ | $2 \neq 3$ | No | — |
| $AC$ | $3 \neq 4$ | No | — |
| $CA$ | $2 = 2$ | Yes | $4\times3$ |
| $AD$ | $3 \neq 2$ | No | — |
| $DA$ | $2 = 2$ | Yes | $2\times3$ |

Five products are defined and three are not.

---

## Quick Verification

For $AB$: the result is $2\times4$, so it has $2\times4 = 8$ entries. Each entry is computed as a dot product of a row of $A$ (length 3) with a column of $B$ (length 3). The lengths match, confirming the calculation is consistent.

For $BA$: $B$ has 4 columns and $A$ has 2 rows. Since $4\neq2$, no entry of the product can be computed. Not defined — confirmed.

---

## Common Mistakes

- **Checking columns of the second factor against rows of the first:** the rule is columns of the *first* factor must equal rows of the *second* factor.
- **Assuming $AB$ defined implies $BA$ defined:** this example shows directly that $AB$ can be defined while $BA$ is not.
- **Confusing the result size:** the result of an $m\times k$ times $k\times n$ multiplication is $m\times n$, taking the *outer* numbers, not the inner ones.

---

## Oral Explanation (3 sentences)

Matrix multiplication $PQ$ is defined exactly when the number of columns of $P$ equals the number of rows of $Q$, because each entry of the product is a dot product of a row of $P$ with a column of $Q$, and those vectors must have the same length. When the product is defined, the result has as many rows as $P$ and as many columns as $Q$ — the inner dimensions disappear and the outer ones remain. This exercise shows that the order of multiplication matters enormously: $AB$ may be defined while $BA$ is not, which is one of the fundamental differences between matrix algebra and ordinary arithmetic.


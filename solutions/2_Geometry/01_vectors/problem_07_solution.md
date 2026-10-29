# Exercise 7 — Linear Dependence Without Heavy Computation

## The Problem

Given

$$
u=(1,2,3),\qquad v=(2,4,6),\qquad w=(0,1,1).
$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

---

## What Are We Looking For?

We want to find a visible relation between two of the vectors and use it to decide about the whole set, without row reduction or determinants.

---

## Idea and Theorem Before the Calculation

**Linear dependence:** Vectors $u,v,w$ are linearly dependent if there are numbers $\alpha,\beta,\gamma$, not all zero, with

$$
\alpha u+\beta v+\gamma w=0.
$$

**Key fact:** If two vectors of a set are proportional, the set is dependent, whatever the other vectors are.

---

## Step-by-Step Solution

**Step 1: Compare $u$ and $v$.**

Every coordinate of $v$ is twice the corresponding coordinate of $u$:

$$
v=(2\cdot1,\ 2\cdot2,\ 2\cdot3)=2u.
$$

**Step 2: Write a nontrivial relation for all three vectors.**

$$
2u-v+0\cdot w=0.
$$

The coefficients $2,-1,0$ are not all zero.

**Step 3: Conclude.**

A nontrivial combination equals the zero vector, so the vectors $u,v,w$ are **linearly dependent**; they cannot be independent.

*Why this is valid:* The definition of dependence asks for just one nontrivial combination equal to zero, and Step 2 provides it. The vector $w$ is simply given the coefficient $0$.

**Step 4: Why no long calculation is needed.**

A general test (row reduction or a $3\times3$ determinant) would also give "dependent," but the relation $v=2u$ already proves dependence by itself. Once two vectors are proportional, the third vector cannot repair the situation: adding more vectors to a dependent set keeps it dependent.

---

## Final Answer in Words

The relation is $v=2u$, or $2u-v+0w=0$. Therefore $u,v,w$ are linearly dependent and cannot be independent. No long calculation is needed, because a single nontrivial relation between two of the vectors already proves dependence of the whole set.

---

## Quick Verification

Check with a determinant, which is zero exactly for dependent vectors:

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 1 \\
\end{pmatrix}=0,
$$

because the second row is twice the first. Also, the three vectors span only a plane: $u$ and $w$ are not proportional (the first coordinate of $w$ is $0$, that of $u$ is not), so the span is two-dimensional, not three-dimensional.

---

## Common Mistakes

- **Thinking $w$ must be involved in the relation:** a coefficient $0$ for $w$ is allowed, as long as not all coefficients are zero.
- **Using the trivial combination $0u+0v+0w=0$:** it always holds and proves nothing.
- **Concluding independence because $w$ is not a multiple of $u$:** one proportional pair is enough for dependence.

---

## Oral Explanation (3 sentences)

The vector $v=(2,4,6)$ is exactly twice $u=(1,2,3)$, so $2u-v+0w=0$ is a nontrivial combination equal to the zero vector. This means the three vectors are linearly dependent, no matter what $w$ is. No determinant or elimination is needed, because one proportional pair already gives the required dependence relation for the whole set.

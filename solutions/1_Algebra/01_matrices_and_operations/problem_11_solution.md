# Exercise 11 — When Do Matrices Commute?

## The Problem

Given

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

---

## What Are We Looking For?

Matrix multiplication is usually not commutative. Here we fix one matrix $A$ and look for all matrices $B$ that do commute with it, by turning the matrix equation $AB=BA$ into ordinary equations for the entries of $B$.

---

## Idea and Theorem Before the Calculation

**Equality of matrices:** Two matrices of the same size are equal if and only if all corresponding entries are equal. A $2\times2$ matrix equation $AB=BA$ is therefore equivalent to four scalar equations.

**Strategy:** Compute $AB$ and $BA$ with unknown entries, compare them entry by entry, and solve the resulting system.

---

## Step-by-Step Solution

**Step 1: Compute $AB$.**

$$
AB=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix} =
\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix}.
$$

Multiplying by $A$ on the left adds the second row of $B$ to the first row.

**Step 2: Compute $BA$.**

$$
BA=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix} =
\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}.
$$

Multiplying by $A$ on the right adds the first column of $B$ to the second column.

**Step 3: Compare entries.**

$$
\begin{aligned}
(1,1):&\quad a+c=a, \\
(1,2):&\quad b+d=a+b, \\
(2,1):&\quad c=c, \\
(2,2):&\quad d=c+d.
\end{aligned}
$$

**Step 4: Solve.**

- From $(1,1)$: $c=0$.
- From $(1,2)$: $d=a$.
- Equation $(2,1)$ holds always.
- From $(2,2)$: $c=0$ again, which gives nothing new.

The entry $b$ does not appear in any condition, so it is free.

*Why this is valid:* Every condition imposed by $AB=BA$ has been written down, so the solutions of this system are exactly the matrices that commute with $A$.

**Step 5: General form.**

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix} = aI+b
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix},\qquad a,b\in\mathbb{R}.
$$

---

## Final Answer in Words

$AB=BA$ holds if and only if $c=0$ and $d=a$, with $b$ arbitrary. The matrices commuting with $A$ are exactly the upper-triangular matrices with equal diagonal entries, that is, all combinations $aI+bN$ with

$$
N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}.
$$

---

## Quick Verification

Take $a=2$, $b=5$, so

$$
B=
\begin{pmatrix}
2 & 5 \\
0 & 2 \\
\end{pmatrix}.
$$

Then

$$
AB=
\begin{pmatrix}
2 & 7 \\
0 & 2 \\
\end{pmatrix},\qquad BA=
\begin{pmatrix}
2 & 2+5 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 7 \\
0 & 2 \\
\end{pmatrix}.
$$

They are equal. Now break the condition by taking $a=b=d=0$ and $c=1$. Then the formulas from Steps 1 and 2 give

$$
AB=
\begin{pmatrix}
1 & 0 \\
1 & 0 \\
\end{pmatrix},\qquad BA=
\begin{pmatrix}
0 & 0 \\
1 & 1 \\
\end{pmatrix},
$$

which are different, as expected.

---

## Common Mistakes

- **Computing only one product:** both $AB$ and $BA$ must be written out with the unknown entries before comparing.
- **Concluding that $b$ must be $0$:** no equation restricts $b$, so it remains free.
- **Stating only examples:** the task asks for the general form, which must cover every solution.

---

## Oral Explanation (3 sentences)

Writing $B$ with unknown entries and computing both products gives $AB$ with first row $(a+c,\ b+d)$ and $BA$ with second column $(a+b,\ c+d)^T$. Comparing the four entries forces $c=0$ and $d=a$, while $b$ can be any number. Hence the matrices that commute with $A$ are exactly $aI+bN$, the upper-triangular matrices with equal diagonal entries.

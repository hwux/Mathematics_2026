# Exercise 1 — From a System to a Matrix

## The Problem

Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

---

## What Are We Looking For?

We want to rewrite three linear equations as one matrix equation $Ax=b$ and name its three ingredients: the coefficient matrix $A$, the vector of unknowns $x$, and the right-hand side $b$.

---

## Idea and Theorem Before the Calculation

**Matrix form of a linear system:** A system of $m$ linear equations in $n$ unknowns can be written as $Ax=b$, where

- $A$ is the $m\times n$ matrix of coefficients, one row per equation and one column per unknown,
- $x$ is the column vector of unknowns,
- $b$ is the column vector of right-hand sides.

The $i$-th entry of $Ax$ is the dot product of the $i$-th row of $A$ with $x$, which is exactly the left side of the $i$-th equation.

---

## Step-by-Step Solution

**Step 1: Fix the order of the unknowns.**

Use the order $x,y,z$ in every equation. Every column of $A$ will then belong to one unknown: column 1 to $x$, column 2 to $y$, column 3 to $z$.

**Step 2: Read off the coefficients row by row.**

- Equation 1, $2x-y+z=4$: coefficients $2,-1,1$.
- Equation 2, $x+3y-2z=1$: coefficients $1,3,-2$.
- Equation 3, $3x+y+z=7$: coefficients $3,1,1$.

A term written without a number, such as $z$ or $-y$, has coefficient $1$ or $-1$.

**Step 3: Assemble $A$, $x$ and $b$.**

$$
A=
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}.
$$

The system is therefore

$$
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix} =
\begin{pmatrix}
4 \\
1 \\
7 \\
\end{pmatrix}.
$$

*Why this is valid:* Two vectors are equal exactly when all their entries are equal, so this single vector equation states the three original equations at once.

**Step 4: Correspondence between rows and equations.**

Row $i$ of $A$ contains the coefficients of equation $i$, and entry $i$ of $b$ is its right-hand side. Multiplying row $i$ of $A$ by the vector $x$ reproduces the left side of equation $i$.

---

## Final Answer in Words

The coefficient matrix $A$ has rows $(2,-1,1)$, $(1,3,-2)$ and $(3,1,1)$, the vector of unknowns is $x=(x,y,z)^T$, and the right-hand side is $b=(4,1,7)^T$. Each row of $A$ together with the matching entry of $b$ encodes one equation of the system.

---

## Quick Verification

Multiply $A$ by the vector of unknowns:

$$
Ax=
\begin{pmatrix}
2x-y+z \\
x+3y-2z \\
3x+y+z \\
\end{pmatrix}.
$$

These are exactly the three left sides of the original system, and setting them equal to the entries $4,1,7$ of $b$ gives back the original equations.

---

## Common Mistakes

- **Dropping a coefficient $1$ or $-1$:** the term $-y$ contributes $-1$ to the matrix, not $0$.
- **Mixing the order of unknowns:** if one row is written in the order $x,z,y$, the matrix describes a different system.
- **Putting the right-hand sides into $A$:** the numbers $4,1,7$ belong to $b$; they appear in $A$ only in the augmented matrix $[A\mid b]$.

---

## Oral Explanation (3 sentences)

To write the system as $Ax=b$, the coefficients of $x$, $y$, $z$ in each equation are placed in one row of the matrix $A$, the unknowns form the column vector $x$, and the right-hand sides form the column vector $b$. Row $i$ of $A$ multiplied by $x$ gives exactly the left side of equation $i$, so the vector equation $Ax=b$ contains all three equations at once. Here $A$ has rows $(2,-1,1)$, $(1,3,-2)$, $(3,1,1)$ and $b=(4,1,7)^T$.

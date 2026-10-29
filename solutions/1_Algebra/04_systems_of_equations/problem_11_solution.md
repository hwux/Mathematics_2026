# Exercise 11 — A Parameter in a System of Three Equations

## The Problem

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

---

## What Are We Looking For?

We want to know, for every real $t$, whether the system has no solution, exactly one solution, or infinitely many, and we must locate the values of $t$ where an ordinary step of the calculation, such as dividing by a pivot, breaks down.

---

## Idea and Theorem Before the Calculation

**Elimination with a parameter:** Row operations of the form $R_i\leftarrow R_i+cR_j$ are valid for every value of the parameter. Dividing by an expression containing $t$ is valid only where that expression is nonzero, so those values must be treated separately.

**Classification:** a contradiction $0=c\neq0$ means no solution; a pivot in every column means exactly one solution.

---

## Step-by-Step Solution

**Step 1: Augmented matrix.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
1 & t & 1 & \mid & 2 \\
1 & 1 & t & \mid & 3 \\
\end{pmatrix}
$$

**Step 2: $R_2\leftarrow R_2-R_1$ and $R_3\leftarrow R_3-R_1$.**

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & t-1 & 0 & \mid & 1 \\
0 & 0 & t-1 & \mid & 2 \\
\end{pmatrix}
$$

*Why this is valid:* These operations do not involve dividing by anything, so they are valid for every $t$.

The matrix is already in row echelon form, provided $t-1\neq0$. The pivots of rows 2 and 3 are both equal to $t-1$.

**Step 3: The critical step.**

To solve rows 2 and 3, the next step is to divide by $t-1$:

$$
y=\frac{1}{t-1},\qquad z=\frac{2}{t-1}.
$$

This step is valid only for $t\neq1$. The value $t=1$ must be analyzed separately.

**Step 4: Case $t\neq1$: exactly one solution.**

There are three nonzero pivots, $1$, $t-1$, $t-1$, so the solution is unique. Back substitution in row 1:

$$
x=1-y-z=1-\frac{1}{t-1}-\frac{2}{t-1}=1-\frac{3}{t-1}=\frac{t-4}{t-1}.
$$

So for $t\neq1$,

$$
\begin{pmatrix}
x \\
y \\
z \\
\end{pmatrix} =\frac{1}{t-1}
\begin{pmatrix}
t-4 \\
1 \\
2 \\
\end{pmatrix}.
$$

**Step 5: Case $t=1$: no solution.**

Substituting $t=1$ into the matrix from Step 2:

$$
\begin{pmatrix}
1 & 1 & 1 & \mid & 1 \\
0 & 0 & 0 & \mid & 1 \\
0 & 0 & 0 & \mid & 2 \\
\end{pmatrix}
$$

The second row means $0=1$ and the third $0=2$. Both are contradictions, so there is no solution. Directly: for $t=1$ all three equations have the same left side $x+y+z$, which cannot equal $1$, $2$ and $3$ at the same time.

---

## Final Answer in Words

For $t\neq1$ the system has exactly one solution, $x=\frac{t-4}{t-1}$, $y=\frac{1}{t-1}$, $z=\frac{2}{t-1}$. For $t=1$ the step of dividing by the pivot $t-1$ is invalid; at this value the pivots vanish, the right-hand sides do not, and the system has no solution. The case of infinitely many solutions does not occur for any $t$.

---

## Quick Verification

For $t=2$ the formula gives $(x,y,z)=(-2,1,2)$:

$$
\begin{aligned}
-2+1+2 &= 1, \\
-2+2\cdot1+2 &= 2, \\
-2+1+2\cdot2 &= 3.
\end{aligned}
$$

For $t=4$ it gives $(0,\frac13,\frac23)$: $0+\frac13+\frac23=1$, $0+\frac43+\frac23=2$, $0+\frac13+\frac83=3$. Both checks confirm the formula.

---

## Common Mistakes

- **Dividing by $t-1$ without comment:** this hides the value $t=1$, at which the system behaves completely differently.
- **Assuming that a vanishing pivot means infinitely many solutions:** that happens only if the right-hand side vanishes as well; here it does not.
- **Losing the common denominator:** $1-\frac{3}{t-1}=\frac{t-1-3}{t-1}=\frac{t-4}{t-1}$.

---

## Oral Explanation (3 sentences)

Subtracting the first equation from the other two gives the rows $(0,\ t-1,\ 0\mid1)$ and $(0,\ 0,\ t-1\mid2)$, which are valid for every $t$. For $t\neq1$ the pivots $t-1$ are nonzero, so dividing by them gives the unique solution $x=\frac{t-4}{t-1}$, $y=\frac{1}{t-1}$, $z=\frac{2}{t-1}$. For $t=1$ this division is impossible, the rows become $0=1$ and $0=2$, and the system has no solution, because the same expression $x+y+z$ cannot equal three different numbers.

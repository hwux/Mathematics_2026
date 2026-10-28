# Exercise 13 — A Recurrence Written in Matrix Form

## The Problem

Let

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$
0,1,1,2,3,5,8,\ldots
$$

and describe the relationship you observe. Then compute

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

---

## What Are We Looking For?

We want to compute several powers of $F$, recognize the Fibonacci numbers in them, and understand why: multiplication by $F$ is exactly one step of the Fibonacci recurrence.

---

## Idea and Theorem Before the Calculation

**Fibonacci sequence:** $F_0=0$, $F_1=1$, and

$$
F_{n+1}=F_n+F_{n-1}\qquad (n\ge1),
$$

which gives $0,1,1,2,3,5,8,13,\ldots$ Each term is the sum of the two previous terms.

**Powers:** $F^{n+1}=F^nF$, so each power is obtained from the previous one by one multiplication.

---

## Step-by-Step Solution

**Step 1: Compute $F^2$.**

$$
F^2=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} =
\begin{pmatrix}
1+1 & 1+0 \\
1+0 & 1+0 \\
\end{pmatrix} =
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}.
$$

**Step 2: Compute $F^3$.**

$$
F^3=F^2F=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} =
\begin{pmatrix}
2+1 & 2+0 \\
1+1 & 1+0 \\
\end{pmatrix} =
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

**Step 3: Compute $F^4$.**

$$
F^4=F^3F=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} =
\begin{pmatrix}
3+2 & 3+0 \\
2+1 & 2+0 \\
\end{pmatrix} =
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}.
$$

**Step 4: Compute $F^5$.**

$$
F^5=F^4F=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix} =
\begin{pmatrix}
5+3 & 5+0 \\
3+2 & 3+0 \\
\end{pmatrix} =
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

*Why this is valid:* Each power is computed from the previous one by a single multiplication by $F$, using the row-times-column rule.

**Step 5: Compare with the sequence.**

All entries are consecutive Fibonacci numbers. Since $F=F^1$ also has the form

$$
\begin{pmatrix}
F_2 & F_1 \\
F_1 & F_0 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix},
$$

the observed pattern is

$$
F^n=
\begin{pmatrix}
F_{n+1} & F_n \\
F_n & F_{n-1} \\
\end{pmatrix}.
$$

For example, $F^5$ contains $F_6=8$, $F_5=5$ and $F_4=3$.

**Step 6: One recurrence step.**

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix} =
\begin{pmatrix}
1\cdot a+1\cdot b \\
1\cdot a+0\cdot b \\
\end{pmatrix} =
\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}.
$$

The first entry of the result is the sum of the two entries, and the second entry keeps the old first entry. If $(a,b)^T=(F_{n+1},F_n)^T$, then

$$
F
\begin{pmatrix}
F_{n+1} \\
F_n \\
\end{pmatrix} =
\begin{pmatrix}
F_{n+1}+F_n \\
F_{n+1} \\
\end{pmatrix} =
\begin{pmatrix}
F_{n+2} \\
F_{n+1} \\
\end{pmatrix}.
$$

The pair of consecutive terms moves one place forward: the new term is created as a sum, and the newer of the two old terms is kept for the next step, while the older one is dropped.

---

## Final Answer in Words

$$
F^2=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\quad F^3=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix},\quad F^4=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix},\quad F^5=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}.
$$

The entries of $F^n$ are the consecutive Fibonacci numbers $F_{n+1}$, $F_n$, $F_n$, $F_{n-1}$. Multiplication by $F$ turns $(a,b)^T$ into $(a+b,a)^T$, which is exactly one step of the recurrence $F_{n+2}=F_{n+1}+F_n$.

---

## Quick Verification

Start from $(F_1,F_0)^T=(1,0)^T$ and apply $F$ repeatedly using the rule $(a,b)^T\mapsto(a+b,a)^T$:

$$
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}\to
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}\to
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}\to
\begin{pmatrix}
3 \\
2 \\
\end{pmatrix}\to
\begin{pmatrix}
5 \\
3 \\
\end{pmatrix}\to
\begin{pmatrix}
8 \\
5 \\
\end{pmatrix}.
$$

After five steps the vector is $(8,5)^T$, which is the first column of $F^5$, as it must be, because $F^5(1,0)^T$ is the first column of $F^5$.

---

## Common Mistakes

- **Shifting the indices:** the top-left entry of $F^n$ is $F_{n+1}$, not $F_n$; check with $F^1$, whose top-left entry is $F_2=1$.
- **Writing $F(a,b)^T=(a+b,b)^T$:** the second row of $F$ is $(1,0)$, so it keeps $a$, not $b$.
- **Describing only the numbers:** the task also asks why they appear, which is explained by the recurrence step in Step 6.

---

## Oral Explanation (3 sentences)

The powers $F^2$ to $F^5$ contain only consecutive Fibonacci numbers, with $F_{n+1}$ in the top-left corner of $F^n$, $F_n$ in both off-diagonal positions, and $F_{n-1}$ in the bottom-right corner. The reason is that $F$ sends a vector $(a,b)^T$ to $(a+b,a)^T$: it forms the sum of two consecutive terms and keeps the newer of them for the next step. Applying $F$ again and again therefore walks along the Fibonacci sequence, and the powers of $F$ record this walk.

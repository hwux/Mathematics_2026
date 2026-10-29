# Exercise 10 — Continuity of a Piecewise Function

## The Problem

Find $a$ so that

$$
f(x)=
\begin{cases}
ax+1,&x<2, \\
x^2-1,&x\ge2
\end{cases}
$$

is continuous at $x=2$. Explicitly compare the left-hand limit, right-hand limit, and function value.

---

## What Are We Looking For?

We want the value of the parameter $a$ for which the two pieces of the function meet at $x=2$ without a jump.

---

## Idea and Theorem Before the Calculation

**Continuity at a point:** $f$ is continuous at $x=2$ if and only if

$$
\lim_{x\to2^-}f(x)=\lim_{x\to2^+}f(x)=f(2).
$$

All three quantities must exist and be equal.

**Which formula to use:** For $x<2$ the first formula applies, for $x\ge2$ the second, so the left limit uses $ax+1$, while both the right limit and the value $f(2)$ use $x^2-1$.

---

## Step-by-Step Solution

**Step 1: Function value.**

$$
f(2)=2^2-1=3.
$$

**Step 2: Right-hand limit.**

$$
\lim_{x\to2^+}f(x)=\lim_{x\to2^+}(x^2-1)=3.
$$

*Why this is valid:* $x^2-1$ is a polynomial, hence continuous.

**Step 3: Left-hand limit.**

$$
\lim_{x\to2^-}f(x)=\lim_{x\to2^-}(ax+1)=2a+1.
$$

**Step 4: Equate the three quantities.**

The right limit and the value are already equal to $3$. Continuity requires

$$
2a+1=3\quad\Longrightarrow\quad a=1.
$$

**Step 5: Comparison table.**

| Quantity | General $a$ | $a=1$ |
|---|---|---|
| left-hand limit | $2a+1$ | $3$ |
| right-hand limit | $3$ | $3$ |
| $f(2)$ | $3$ | $3$ |

For $a\neq1$ the left limit differs from the other two, and the graph has a jump of size $|2a+1-3|=2|a-1|$ at $x=2$.

---

## Final Answer in Words

The function is continuous at $x=2$ exactly for $a=1$. Then the left-hand limit, the right-hand limit and the value $f(2)$ are all equal to $3$.

---

## Quick Verification

For $a=1$: $f(1.99)=1.99+1=2.99$ and $f(2.01)=2.01^2-1=3.0401$, both close to $f(2)=3$. For a wrong value, say $a=2$: $f(1.99)=4.98$, which is near $5$, not near $3$, so there is a jump.

---

## Common Mistakes

- **Checking only $f(2)$:** a value at a point says nothing about the limit from the other side.
- **Using $ax+1$ at $x=2$:** the condition $x\ge2$ assigns $x=2$ to the second formula.
- **Equating the formulas everywhere:** $ax+1=x^2-1$ only needs to hold at $x=2$, not for all $x$.

---

## Oral Explanation (3 sentences)

Continuity at $x=2$ means that the left-hand limit, the right-hand limit and the value of the function are the same number. The right piece gives $f(2)=3$ and a right-hand limit of $3$, while the left piece gives a left-hand limit of $2a+1$. Setting $2a+1=3$ gives $a=1$, and only for this value do the two pieces meet without a jump.

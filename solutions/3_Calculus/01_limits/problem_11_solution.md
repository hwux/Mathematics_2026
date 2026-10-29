# Exercise 11 — An n-th Root

## The Problem

Compute

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n}.
$$

Explain which term dominates and why the transformation looks different from the case of a quotient of polynomials.

---

## What Are We Looking For?

We want the limit of the $n$-th root of a sum of two exponential terms, and an explanation of which term controls the result.

---

## Idea and Theorem Before the Calculation

**Dominant exponential term:** For $0<q<1$, $q^n\to0$. Since $\frac25<1$, the term $2^n$ is negligible compared with $5^n$: $\frac{2^n}{5^n}\to0$.

**$n$-th root of a constant:** For every constant $c>0$, $\sqrt[n]{c}=c^{1/n}\to1$.

**Squeeze theorem:** If $a_n\le b_n\le c_n$ and $a_n,c_n\to L$, then $b_n\to L$.

---

## Step-by-Step Solution

**Step 1: Factor out the dominant term.**

$$
\sqrt[n]{5^n+2^n}=\sqrt[n]{5^n\left(1+\left(\frac25\right)^n\right)}=5\cdot\sqrt[n]{1+\left(\frac25\right)^n}.
$$

*Why this is valid:* $\sqrt[n]{ab}=\sqrt[n]{a}\,\sqrt[n]{b}$ for positive $a,b$, and $\sqrt[n]{5^n}=5$.

**Step 2: Bound the remaining root.**

Since $0<\left(\frac25\right)^n\le1$,

$$
1\le1+\left(\frac25\right)^n\le2\quad\Longrightarrow\quad1\le\sqrt[n]{1+\left(\frac25\right)^n}\le\sqrt[n]{2}.
$$

**Step 3: Squeeze.**

$$
5\le\sqrt[n]{5^n+2^n}\le5\sqrt[n]{2}.
$$

Since $\sqrt[n]{2}\to1$, both bounds tend to $5$. By the squeeze theorem,

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n}=5.
$$

---

## Why the Transformation Is Different

For a quotient of polynomials we divided by a power $n^k$, and the competing terms differed by powers of $n$. Here the competing terms are exponentials with different bases, and the term with the larger base, $5^n$, dominates: its ratio to $2^n$ grows like $\left(\frac52\right)^n$. We do not divide but factor $5^n$ out from under the root, because the $n$-th root turns $5^n$ into exactly $5$. The leftover factor is squeezed between $1$ and $\sqrt[n]{2}$, and the $n$-th root flattens it to $1$.

---

## Final Answer in Words

$$
\lim_{n\to\infty}\sqrt[n]{5^n+2^n}=5.
$$

The term $5^n$ dominates, and the $n$-th root of $5^n$ is $5$; the contribution of $2^n$ disappears in the limit.

---

## Quick Verification

| $n$ | $1$ | $2$ | $5$ | $10$ |
|---|---|---|---|---|
| $\sqrt[n]{5^n+2^n}$ | $7$ | $5.385$ | $5.010$ | $5.00005$ |

The values decrease towards $5$ and stay above $5$, matching the lower bound in Step 3. In general $\sqrt[n]{a^n+b^n}\to\max(a,b)$ for $a,b>0$.

---

## Common Mistakes

- **Answering $5+2=7$:** that is only the first term; the root does not split over a sum.
- **Writing $\sqrt[n]{5^n+2^n}=5+2$:** $\sqrt[n]{a+b}\neq\sqrt[n]{a}+\sqrt[n]{b}$.
- **Forgetting that $\sqrt[n]{2}\to1$:** this fact is what makes the upper bound converge to $5$.

---

## Oral Explanation (3 sentences)

The term $5^n$ grows much faster than $2^n$, so we factor it out from under the root and get $5\cdot\sqrt[n]{1+(2/5)^n}$. The remaining root lies between $1$ and $\sqrt[n]{2}$, and both of these tend to $1$. By the squeeze theorem the whole expression tends to $5$, the larger of the two bases.

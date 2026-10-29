# Exercise 2 — Different Growth Rates

## The Problem

Compute

$$
\lim_{n\to\infty}\frac{3n+1}{n^2+4},\qquad \lim_{n\to\infty}\frac{2n^3-n}{5n^2+1}.
$$

Compare the two cases and formulate a general observation about the degrees of the polynomials in the numerator and denominator.

---

## What Are We Looking For?

We want two limits of quotients of polynomials in which the degrees of the numerator and denominator differ, and then a general rule describing how the comparison of degrees decides the limit.

---

## Idea and Theorem Before the Calculation

**Divide by the highest power of the denominator.** This keeps the denominator convergent to a nonzero number, so the behavior of the whole fraction is read from the numerator.

**Basic facts:** $\frac{c}{n^k}\to0$ for $k>0$, and $n^k\to+\infty$ for $k>0$.

**Product with a positive limit:** If $a_n\to+\infty$ and $b_n\to b>0$, then $a_nb_n\to+\infty$.

---

## Step-by-Step Solution

**Step 1: First limit, divide by $n^2$.**

$$
\frac{3n+1}{n^2+4}=\frac{\frac{3}{n}+\frac{1}{n^2}}{1+\frac{4}{n^2}}\longrightarrow\frac{0+0}{1+0}=0.
$$

*Why this is valid:* The denominator tends to $1\neq0$, so the quotient rule applies.

**Step 2: Second limit, divide by $n^2$.**

$$
\frac{2n^3-n}{5n^2+1}=\frac{2n-\frac{1}{n}}{5+\frac{1}{n^2}}.
$$

The denominator tends to $5$, while the numerator $2n-\frac1n$ tends to $+\infty$.

**Step 3: Conclude.**

$$
\frac{2n-\frac{1}{n}}{5+\frac{1}{n^2}}=\left(2n-\frac{1}{n}\right)\cdot\frac{1}{5+\frac{1}{n^2}}\longrightarrow+\infty,
$$

because the first factor tends to $+\infty$ and the second tends to $\frac15>0$.

So the first sequence converges to $0$ and the second diverges to $+\infty$.

---

## General Observation

Let the numerator have degree $p$ with leading coefficient $a$, and the denominator degree $q$ with leading coefficient $b$. Then

- if $p<q$, the limit is $0$ (the denominator grows faster),
- if $p=q$, the limit is $\frac{a}{b}$ (Exercise 1),
- if $p>q$, the sequence tends to $+\infty$ or $-\infty$, with the sign of $\frac{a}{b}$.

In short, the fraction behaves like $\frac{a\,n^p}{b\,n^q}=\frac{a}{b}\,n^{p-q}$ for large $n$.

---

## Final Answer in Words

The first limit is $0$, because the denominator has a higher degree than the numerator. The second sequence tends to $+\infty$, because the numerator has the higher degree and the leading coefficients $2$ and $5$ are both positive.

---

## Quick Verification

For $n=1000$:

$$
\frac{3001}{1\,000\,004}\approx0.003,\qquad \frac{2\cdot10^9-1000}{5\cdot10^6+1}\approx400.
$$

The first is small, the second is large and close to $\frac{2}{5}n=400$, which agrees with the dominant-term picture $\frac{2n^3}{5n^2}=\frac{2}{5}n$.

---

## Common Mistakes

- **Answering $\frac{2}{5}$ for the second limit:** the ratio of leading coefficients is the limit only when the degrees are equal.
- **Saying "the limit is $\infty$, so it exists":** a sequence tending to $+\infty$ diverges; we say it has an improper limit.
- **Forgetting the sign:** if the leading coefficients had opposite signs, the second limit would be $-\infty$.

---

## Oral Explanation (3 sentences)

In a quotient of polynomials only the highest powers matter for large $n$, so the fraction behaves like the ratio of its leading terms. In the first case this ratio is $\frac{3n}{n^2}=\frac{3}{n}$, which tends to zero, and in the second it is $\frac{2n^3}{5n^2}=\frac{2}{5}n$, which grows without bound. In general a lower degree on top gives $0$, equal degrees give the ratio of leading coefficients, and a higher degree on top gives an infinite limit.

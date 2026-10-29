# Problem 7 — Exponential Growth

## The Problem

Assume the model

$$
N(t)=N_0e^{kt},\qquad k>0.
$$

1. Verify by differentiation that the model satisfies the relation $N'(t)=kN(t)$.
2. Find the population doubling time.
3. Explain why the doubling time does not depend on $N_0$.

---

## What Are We Looking For?

We want to confirm that exponential growth has a growth rate proportional to the current size, find how long it takes the population to double, and explain why that time is the same for every initial size.

---

## Idea and Theorem Before the Calculation

**Chain rule:** $\left(e^{kt}\right)'=ke^{kt}$.

**Logarithm as inverse:** $e^{a}=b\iff a=\ln b$ for $b>0$.

---

## Step-by-Step Solution

**Part 1: The relation $N'=kN$.**

$$
N'(t)=N_0\cdot ke^{kt}=k\left(N_0e^{kt}\right)=kN(t).
$$

The rate of growth at each moment is proportional to the current population, with proportionality constant $k$.

**Part 2: Doubling time.**

We look for $T>0$ such that $N(t+T)=2N(t)$. Starting from $t=0$:

$$
N_0e^{kT}=2N_0\quad\Longrightarrow\quad e^{kT}=2\quad\Longrightarrow\quad T=\frac{\ln2}{k}.
$$

**Part 3: Independence of $N_0$.**

In Part 2, $N_0$ appears on both sides and cancels. More generally, for any starting time $t$,

$$
\frac{N(t+T)}{N(t)}=\frac{N_0e^{k(t+T)}}{N_0e^{kt}}=e^{kT}=2.
$$

The ratio depends only on the elapsed time, not on $N_0$ or on $t$.

---

## Interpretation

Exponential growth multiplies the population by the same factor over equal time intervals. Doubling is a statement about a ratio, and ratios do not depend on the scale of the population: $100$ bacteria become $200$ in the same time as $10^6$ become $2\cdot10^6$, because each individual contributes to growth at the same per-capita rate $k$.

---

## Final Answer in Words

$N'(t)=kN_0e^{kt}=kN(t)$, so the model has growth rate proportional to its size. The doubling time is

$$
T=\frac{\ln2}{k}.
$$

It does not depend on $N_0$, because doubling compares $N(t+T)$ with $N(t)$, and in this ratio $N_0$ cancels.

---

## Quick Verification

For $k=0.1$ per hour, $T=\frac{\ln2}{0.1}\approx6.93$ hours, and $e^{0.1\cdot6.93}=e^{0.693}\approx2.00$. After two doubling times the factor is $e^{2\ln2}=4$, as expected.

---

## Common Mistakes

- **$\left(N_0e^{kt}\right)'=N_0e^{kt}$:** the factor $k$ from the chain rule is missing.
- **$T=\frac{2}{k}$ or $T=\frac{k}{\ln2}$:** solving $e^{kT}=2$ requires the logarithm.
- **Thinking a bigger population doubles faster:** it grows faster in absolute numbers, but not in ratio.

---

## Oral Explanation (3 sentences)

Differentiating $N_0e^{kt}$ gives $kN_0e^{kt}=kN(t)$, so the growth rate is proportional to the current population. The population doubles when $e^{kT}=2$, which gives $T=\frac{\ln2}{k}$. This time does not depend on $N_0$, because doubling is a comparison of ratios, and in the ratio $\frac{N(t+T)}{N(t)}=e^{kT}$ the initial size cancels.

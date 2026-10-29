# Problem 15 — Recovering a Function from Its Derivative and a Condition

## The Problem

The function $F$ satisfies

$$
F'(x)=2xe^{x^2}
$$

and

$$
F(0)=3.
$$

1. Recognize the method needed to find the function $F$.
2. Determine the entire family of functions with the given derivative.
3. Use the condition $F(0)=3$ to determine the correct constant.
4. Verify the final result by differentiation and substitution of $x=0$.

---

## What Are We Looking For?

We want the unique function whose derivative is $2xe^{x^2}$ and whose value at $0$ is $3$.

---

## Idea and Theorem Before the Calculation

**Antiderivative family:** All functions with derivative $f$ on $\mathbb{R}$ are $G(x)+C$, where $G$ is one antiderivative.

**Initial condition:** One known value selects one member of the family.

**Substitution:** the factor $2x$ is the derivative of the exponent $x^2$, as in Problems 4 and 5.

---

## Step-by-Step Solution

**Part 1: Method.**

The integrand $2xe^{x^2}$ is an exponential of $x^2$ multiplied by the derivative of $x^2$. This is the chain-rule structure, so we use substitution with $u=x^2$.

**Part 2: Family.**

$$
u=x^2,\qquad du=2x\,dx,
$$

$$
\int2xe^{x^2}\,dx=\int e^u\,du=e^u+C=e^{x^2}+C.
$$

So every function with the given derivative has the form

$$
F(x)=e^{x^2}+C,\qquad C\in\mathbb{R}.
$$

**Part 3: Constant.**

$$
F(0)=e^0+C=1+C=3\quad\Longrightarrow\quad C=2.
$$

Hence

$$
F(x)=e^{x^2}+2.
$$

**Part 4: Verification.**

$$
F'(x)=e^{x^2}\cdot2x=2xe^{x^2},\qquad F(0)=e^0+2=3.
$$

Both conditions are satisfied.

---

## Final Answer in Words

The function is recognized as an antiderivative by substitution $u=x^2$, the family is $e^{x^2}+C$, and the condition $F(0)=3$ gives $C=2$. Therefore

$$
F(x)=e^{x^2}+2.
$$

---

## Quick Verification

By the fundamental theorem, $F(x)=F(0)+\int_0^x2te^{t^2}\,dt=3+\left(e^{x^2}-1\right)=e^{x^2}+2$, the same function obtained in a different way.

---

## Common Mistakes

- **Answering $C=3$:** $F(0)=e^0+C=1+C$, and $e^0=1$, not $0$.
- **Forgetting the constant entirely:** then the condition $F(0)=3$ cannot be satisfied.
- **Writing $\frac{e^{x^2}}{2x}$:** dividing by the inner derivative is not a valid method.

---

## Oral Explanation (3 sentences)

The derivative $2xe^{x^2}$ has the chain-rule structure, an exponential of $x^2$ times the derivative of $x^2$, so substitution gives the family $e^{x^2}+C$. The condition $F(0)=3$ means $1+C=3$, so $C=2$ and $F(x)=e^{x^2}+2$. Differentiating gives back $2xe^{x^2}$ and substituting $x=0$ gives $3$, so both requirements hold.

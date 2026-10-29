# Problem 5 — The Same Substitution in a Different Context

## The Problem

Compute

$$
\int xe^{x^2}\,dx.
$$

First compare the structure with Problem 4 and explain what is common despite the different appearance of the function.

---

## What Are We Looking For?

We want an antiderivative of $xe^{x^2}$ and an explanation of why the same substitution as in Problem 4 applies, although the outer function is now an exponential.

---

## Idea and Theorem Before the Calculation

**Common structure:** In Problem 4 the integrand was (outer function of $x^2+1$) times (derivative of $x^2+1$). Here it is (outer function of $x^2$) times (a multiple of the derivative of $x^2$). The type of the outer function does not matter.

**Substitution:** $\int g(u(x))u'(x)\,dx=\int g(u)\,du$.

**Constant factors:** if only $c\cdot u'(x)$ is missing a constant, we can compensate by $\frac{1}{c}$.

---

## Step-by-Step Solution

**Step 1: Choose $u$.**

$$
u=x^2,\qquad du=2x\,dx\quad\Longrightarrow\quad x\,dx=\frac12du.
$$

**Step 2: Substitute.**

$$
\int xe^{x^2}\,dx=\int e^{u}\cdot\frac12\,du=\frac12e^u+C.
$$

*Why this is valid:* the integrand contains $x\,dx$, which is half of $du$; the constant $\frac12$ moves outside the integral.

**Step 3: Return to $x$.**

$$
\int xe^{x^2}\,dx=\frac12e^{x^2}+C.
$$

**Step 4: Verify.**

$$
\left(\frac12e^{x^2}\right)'=\frac12e^{x^2}\cdot2x=xe^{x^2}.
$$

---

## What Is Common with Problem 4

| | Problem 4 | Problem 5 |
|---|---|---|
| inner function $u$ | $x^2+1$ | $x^2$ |
| outer function | $u^4$ | $e^u$ |
| factor present | $2x=u'$ | $x=\frac12u'$ |

In both cases the integrand is the result of a chain rule: an outer function of $u$, multiplied by the derivative of $u$. The substitution is recognized by this structure, not by whether the outer function is a power or an exponential.

---

## Final Answer in Words

$$
\int xe^{x^2}\,dx=\frac12e^{x^2}+C.
$$

As in Problem 4, the derivative of the inner expression appears as a factor (here up to the constant $\frac12$), which makes the substitution $u=x^2$ work.

---

## Quick Verification

Definite check: $\int_0^1xe^{x^2}\,dx=\frac12(e-1)\approx0.859$. On $[0,1]$ the integrand grows from $0$ to $e\approx2.72$ and is convex, so its average should be somewhat below $\frac{0+2.72}{2}=1.36$; the value $0.859$ is plausible.

---

## Common Mistakes

- **Forgetting the factor $\frac12$:** $\left(e^{x^2}\right)'=2xe^{x^2}$, which is twice the integrand.
- **$\int e^{x^2}dx$-type thinking:** without the factor $x$ the substitution would not work.
- **Answering $\frac{e^{x^2}}{2x}$:** dividing by the inner derivative is not a valid rule.

---

## Oral Explanation (3 sentences)

The structure is the same as in Problem 4: an outer function of $x^2$ multiplied by the derivative of $x^2$, up to a constant. With $u=x^2$ we have $x\,dx=\frac12du$, so the integral becomes $\frac12\int e^u\,du=\frac12e^{x^2}+C$. Differentiating gives back $xe^{x^2}$, which shows that substitution is recognized by structure, not by the type of function.

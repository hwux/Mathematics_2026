# Problem 6 — When Does a Logarithm Appear from an Integral?

## The Problem

Compute

$$
\int\frac{2x}{x^2+5}\,dx.
$$

Identify the denominator as a candidate for substitution, compare the numerator with its derivative, and explain the source of the logarithm in the result.

---

## What Are We Looking For?

We want an antiderivative of a fraction whose numerator is the derivative of its denominator, and an explanation of why the answer is a logarithm.

---

## Idea and Theorem Before the Calculation

**Key integral:**

$$
\int\frac{du}{u}=\ln|u|+C,
$$

because $(\ln|u|)'=\frac1u$ for $u\neq0$.

**Pattern "derivative of the denominator over the denominator":**

$$
\int\frac{g'(x)}{g(x)}\,dx=\ln|g(x)|+C.
$$

---

## Step-by-Step Solution

**Step 1: Choose $u$.**

$$
u=x^2+5,\qquad du=2x\,dx.
$$

The numerator $2x\,dx$ is exactly $du$.

**Step 2: Substitute.**

$$
\int\frac{2x}{x^2+5}\,dx=\int\frac{du}{u}=\ln|u|+C.
$$

**Step 3: Return to $x$.**

Since $x^2+5\ge5>0$, the absolute value can be dropped:

$$
\int\frac{2x}{x^2+5}\,dx=\ln(x^2+5)+C.
$$

**Step 4: Verify.**

$$
\left(\ln(x^2+5)\right)'=\frac{2x}{x^2+5}.
$$

---

## Source of the Logarithm

After the substitution the integral becomes $\int u^{-1}\,du$. This is the only power for which the power rule $\frac{u^{n+1}}{n+1}$ fails (it would divide by $0$), and the function whose derivative is $u^{-1}$ is $\ln|u|$. So a logarithm appears whenever the integrand reduces to "something's derivative divided by that something".

---

## Final Answer in Words

$$
\int\frac{2x}{x^2+5}\,dx=\ln(x^2+5)+C.
$$

The numerator $2x$ is the derivative of the denominator $x^2+5$, so the substitution $u=x^2+5$ gives $\int\frac{du}{u}$, which is a logarithm. No absolute value is needed because $x^2+5>0$.

---

## Quick Verification

Definite check: $\int_0^2\frac{2x}{x^2+5}\,dx=\ln9-\ln5=\ln1.8\approx0.588$. The integrand is $0$ at $0$, about $0.333$ at $1$ and $0.444$ at $2$; the trapezoidal rule with step $1$ gives $\frac12(0+0.444)+0.333\approx0.556$, close to $0.588$.

---

## Common Mistakes

- **$\int\frac{2x}{x^2+5}dx=\frac{x^2}{\frac{x^3}{3}+5x}$:** integrals of quotients are not quotients of integrals.
- **Forgetting that the numerator must be the derivative:** for $\int\frac{1}{x^2+5}dx$ this method does not work.
- **Writing $\ln|x^2+5|$ and worrying about the sign:** it is correct, but the absolute value is unnecessary here.

---

## Oral Explanation (3 sentences)

The numerator $2x$ is exactly the derivative of the denominator $x^2+5$, so we substitute $u=x^2+5$ and the integral becomes $\int\frac{du}{u}$. The antiderivative of $\frac1u$ is $\ln|u|$, which is the source of the logarithm. Since $x^2+5$ is always positive, the result is $\ln(x^2+5)+C$.

# Problem 4 — Substitution as Reversing the Chain Rule

## The Problem

Compute

$$
\int 2x(x^2+1)^4\,dx.
$$

Before calculating, identify a candidate for the new variable $u$ and show that its derivative appears in the integral. Finally, verify the result by differentiation.

---

## What Are We Looking For?

We want an antiderivative of a product in which one factor is the derivative of the expression inside a power, using substitution.

---

## Idea and Theorem Before the Calculation

**Chain rule:** $\left(G(u(x))\right)'=G'(u(x))\,u'(x)$.

**Substitution (the chain rule backwards):**

$$
\int g(u(x))\,u'(x)\,dx=\int g(u)\,du\Big|_{u=u(x)}.
$$

**Recognition:** look for an inner expression $u(x)$ whose derivative $u'(x)$ is also a factor of the integrand.

---

## Step-by-Step Solution

**Step 1: Choose $u$.**

The inner expression of the fourth power is $x^2+1$. Let

$$
u=x^2+1,\qquad du=2x\,dx.
$$

The factor $2x\,dx$ is present in the integral, exactly as needed.

**Step 2: Substitute.**

$$
\int2x(x^2+1)^4\,dx=\int u^4\,du=\frac{u^5}{5}+C.
$$

**Step 3: Return to $x$.**

$$
\int2x(x^2+1)^4\,dx=\frac{(x^2+1)^5}{5}+C.
$$

**Step 4: Verify.**

$$
\left(\frac{(x^2+1)^5}{5}\right)'=\frac{5(x^2+1)^4\cdot2x}{5}=2x(x^2+1)^4.
$$

---

## Final Answer in Words

$$
\int2x(x^2+1)^4\,dx=\frac{(x^2+1)^5}{5}+C.
$$

The substitution $u=x^2+1$ works because its derivative $2x$ is already a factor of the integrand; differentiating the result with the chain rule returns the integrand.

---

## Quick Verification

Definite check: $\int_0^1 2x(x^2+1)^4\,dx=\frac{2^5-1^5}{5}=\frac{31}{5}=6.2$. With the substitution directly in limits, $u$ runs from $1$ to $2$ and $\int_1^2u^4\,du=\frac{32-1}{5}=6.2$.

---

## Common Mistakes

- **Expanding $(x^2+1)^4$:** possible but long; substitution is the intended method.
- **Forgetting to replace $dx$:** the factor $2x\,dx$ must become $du$.
- **Leaving the answer in $u$:** the result must be expressed in $x$.

---

## Oral Explanation (3 sentences)

The integrand contains $(x^2+1)^4$ and also the factor $2x$, which is exactly the derivative of $x^2+1$. Setting $u=x^2+1$ turns $2x\,dx$ into $du$ and the integral into $\int u^4\,du=\frac{u^5}{5}+C$. Returning to $x$ gives $\frac{(x^2+1)^5}{5}+C$, and the chain rule confirms that its derivative is the original integrand.

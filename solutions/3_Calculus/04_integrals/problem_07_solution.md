# Problem 7 — Integration by Parts as Reversing the Product Rule

## The Problem

Compute

$$
\int xe^x\,dx.
$$

First write the product differentiation rule and, on that basis, explain the meaning of the integration-by-parts formula. Verify the result by differentiation.

---

## What Are We Looking For?

We want to derive the integration-by-parts formula from the product rule and use it to integrate $xe^x$.

---

## Idea and Theorem Before the Calculation

**Product rule:**

$$
(uv)'=u'v+uv'.
$$

**Integrating both sides:**

$$
uv=\int u'v\,dx+\int uv'\,dx\quad\Longrightarrow\quad\int uv'\,dx=uv-\int u'v\,dx.
$$

**Meaning:** If the integrand is a product $u\cdot v'$, we may move the derivative from $v$ to $u$, at the cost of the boundary term $uv$. This helps when $u'v$ is simpler than $uv'$.

---

## Step-by-Step Solution

**Step 1: Choose the parts.**

$$
u=x,\quad v'=e^x\qquad\Longrightarrow\qquad u'=1,\quad v=e^x.
$$

*Why this choice:* differentiating $x$ makes it simpler (it becomes $1$), while integrating $e^x$ does not make it more complicated.

**Step 2: Apply the formula.**

$$
\int xe^x\,dx=xe^x-\int1\cdot e^x\,dx=xe^x-e^x+C.
$$

**Step 3: Simplify.**

$$
\int xe^x\,dx=(x-1)e^x+C.
$$

**Step 4: Verify.**

$$
\left((x-1)e^x\right)'=1\cdot e^x+(x-1)e^x=xe^x.
$$

---

## Final Answer in Words

$$
\int xe^x\,dx=(x-1)e^x+C.
$$

Integration by parts is the product rule read backwards: the derivative is moved from $e^x$ to $x$, which turns the problem into the easy integral $\int e^x\,dx$.

---

## Quick Verification

Definite check: $\int_0^1xe^x\,dx=\left[(x-1)e^x\right]_0^1=0-(-1)=1$. A rough estimate: on $[0,1]$ the integrand grows from $0$ to $e\approx2.72$; the trapezoidal value $\frac{0+2.72}{2}=1.36$ overestimates a convex function, and Simpson's rule $\frac16(0+4\cdot0.824+2.718)\approx1.002$ is very close to $1$.

---

## Common Mistakes

- **Choosing $u=e^x$, $v'=x$:** this leads to $\int\frac{x^2}{2}e^x\,dx$, which is harder.
- **Sign error:** the formula has $-\int u'v\,dx$.
- **Forgetting the boundary term $uv$:** the answer is not just $-\int u'v\,dx$.

---

## Oral Explanation (3 sentences)

Integrating the product rule $(uv)'=u'v+uv'$ gives the formula $\int uv'\,dx=uv-\int u'v\,dx$, which moves the derivative from one factor to the other. With $u=x$ and $v'=e^x$ we get $xe^x-\int e^x\,dx=(x-1)e^x+C$. Differentiating $(x-1)e^x$ with the product rule returns $xe^x$, which confirms the result.

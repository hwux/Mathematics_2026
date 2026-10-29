# Problem 2 — A Parabola from the Perspective of the Derivative

## The Problem

For $f(x)=x^2-4x+1$, find the minimum using the derivative. Compare the result with the vertex form and explain why both approaches lead to the same point.

---

## What Are We Looking For?

We want the lowest point of the parabola found in two ways, by the derivative and by completing the square, and an explanation of why they agree.

---

## Idea and Theorem Before the Calculation

**Derivative method:** At a minimum of a differentiable function the tangent is horizontal, so $f'(x_0)=0$; a sign change of $f'$ from $-$ to $+$ confirms a minimum.

**Vertex form:** $ax^2+bx+c=a(x-p)^2+q$ with vertex $(p,q)$; for $a>0$ the vertex is the lowest point.

---

## Step-by-Step Solution

**Step 1: Derivative.**

$$
f'(x)=2x-4,\qquad f'(x)=0\iff x=2.
$$

**Step 2: Type of the critical point.**

$f'(x)<0$ for $x<2$ and $f'(x)>0$ for $x>2$, so $f$ decreases and then increases: $x=2$ is a minimum. Equivalently $f''(x)=2>0$.

**Step 3: Minimum value.**

$$
f(2)=4-8+1=-3.
$$

**Step 4: Vertex form.**

$$
x^2-4x+1=(x^2-4x+4)-4+1=(x-2)^2-3.
$$

The vertex is $(2,-3)$. Since $(x-2)^2\ge0$, we have $f(x)\ge-3$ with equality only at $x=2$.

---

## Why Both Methods Agree

The vertex form shows that the parabola is symmetric about the line $x=2$, so its tangent at the vertex must be horizontal: there is no reason for it to tilt either way. Differentiating the vertex form gives $f'(x)=2(x-2)$, which is zero exactly at the vertex. Both methods describe the same geometric fact, the derivative through slopes and the vertex form through a perfect square.

---

## Final Answer in Words

The minimum is at $x=2$ with value $f(2)=-3$. The derivative gives the point where the tangent is horizontal, and the vertex form $(x-2)^2-3$ gives the same point $(2,-3)$ as the vertex of the parabola.

---

## Quick Verification

The zeros of $f$ are $2\pm\sqrt3$, and their midpoint is $2$, which is the axis of symmetry. Also $f(1)=f(3)=-2>-3$, consistent with a minimum at $2$.

---

## Common Mistakes

- **Giving only $x=2$:** the minimum value is $f(2)=-3$.
- **Completing the square incorrectly:** $x^2-4x=(x-2)^2-4$, not $(x-2)^2+4$.
- **Not checking the type:** $f'(x_0)=0$ alone does not distinguish a minimum from a maximum.

---

## Oral Explanation (3 sentences)

The derivative $2x-4$ vanishes at $x=2$ and changes sign from negative to positive, so the function has a minimum there with value $-3$. Completing the square gives $(x-2)^2-3$, which shows directly that the vertex is $(2,-3)$ and that no value is smaller than $-3$. Both methods agree because the tangent at the vertex of a parabola is horizontal by symmetry.

# Problem 15 — Find the Error in the Monotonicity Analysis

## The Problem

For the function

$$
f(x)=x^3-3x
$$

the derivative was correctly computed as

$$
f'(x)=3(x-1)(x+1).
$$

However, a student wrote the following conclusion:

> The derivative is positive between its zeros and negative outside them. Therefore, the function is decreasing on $(-\infty,-1)\cup(1,\infty)$, increasing on $(-1,1)$, has a local minimum at $x=-1$, and a local maximum at $x=1$.

1. Without differentiating again, explain why merely identifying the zeros of the derivative does not justify the stated sign chart, and find the error in the student's reasoning.
2. Construct the correct sign chart for $f'(x)$.
3. Give the correct intervals of monotonicity and the character of the extrema.
4. In each of the three intervals, choose one simple test point and show that the sign of the derivative confirms your classification.

---

## What Are We Looking For?

We want to locate the error in a completed argument, correct the sign chart of $f'$, and give the right monotonicity and extrema, confirmed by test points.

---

## Idea and Theorem Before the Calculation

**Zeros only split the line:** the zeros of $f'$ divide $\mathbb{R}$ into intervals on which $f'$ has a constant sign, but they do not tell which sign. The sign must be determined by a test point or by the shape of $f'$.

**Shape of a quadratic:** $f'(x)=3x^2-3$ has positive leading coefficient $3$, so it is an upward parabola: negative between its zeros and positive outside them.

---

## Step-by-Step Solution

**Part 1: The error.**

The zeros $x=\pm1$ only say where $f'$ may change sign. The student assumed the sign pattern "positive between the zeros", which is the pattern of a downward parabola. But $f'(x)=3(x-1)(x+1)$ has the leading coefficient $3>0$, so it opens upward and is negative between its zeros. The whole conclusion is built on this reversed sign chart.

There is also an internal contradiction that can be seen without any differentiation: $f(-1)=-1+3=2$ and $f(1)=1-3=-2$. If $f$ were increasing on $(-1,1)$, we would need $f(-1)<f(1)$, but $2>-2$. In addition, writing "decreasing on $(-\infty,-1)\cup(1,\infty)$" is incorrect form even for a correct sign, because monotonicity should be stated on each interval separately.

**Part 2: Correct sign chart.**

| interval | $(-\infty,-1)$ | $(-1,1)$ | $(1,\infty)$ |
|---|---|---|---|
| $x-1$ | $-$ | $-$ | $+$ |
| $x+1$ | $-$ | $+$ | $+$ |
| $f'(x)=3(x-1)(x+1)$ | $+$ | $-$ | $+$ |

**Part 3: Monotonicity and extrema.**

- increasing on $(-\infty,-1]$,
- decreasing on $[-1,1]$,
- increasing on $[1,\infty)$,
- local maximum at $x=-1$: $f(-1)=2$,
- local minimum at $x=1$: $f(1)=-2$.

**Part 4: Test points.**

$$
f'(-2)=3(-3)(-1)=9>0,\qquad f'(0)=3(-1)(1)=-3<0,\qquad f'(2)=3(1)(3)=9>0.
$$

The signs $+,-,+$ confirm the classification.

---

## Final Answer in Words

The student reversed the signs: $f'(x)=3(x-1)(x+1)$ is an upward parabola, so it is negative between $-1$ and $1$ and positive outside. Correctly, $f$ is increasing on $(-\infty,-1]$, decreasing on $[-1,1]$, and increasing on $[1,\infty)$, with a local maximum $f(-1)=2$ and a local minimum $f(1)=-2$. The test points $-2$, $0$, $2$ give $f'$ values $9$, $-3$, $9$.

---

## Quick Verification

Direct values: $f(-2)=-2$, $f(-1)=2$, $f(0)=0$, $f(1)=-2$, $f(2)=2$. The values rise from $-2$ to $2$, fall to $-2$, and rise to $2$, exactly the corrected pattern. This agrees with Problem 11 for $a=1$.

---

## Common Mistakes

- **Guessing the sign pattern from the zeros:** always check the leading coefficient or a test point.
- **Swapping maximum and minimum when the signs are reversed:** one error propagates to every conclusion.
- **Writing monotonicity on a union of intervals:** state it on each interval.

---

## Oral Explanation (3 sentences)

The zeros of the derivative only divide the line into intervals; they do not determine the sign on each interval, and the student used the pattern of a downward parabola although $3(x-1)(x+1)$ opens upward. In fact the derivative is positive for $x<-1$, negative on $(-1,1)$ and positive for $x>1$, as the test points $-2$, $0$, $2$ confirm. So the function increases, has a maximum $2$ at $x=-1$, decreases to a minimum $-2$ at $x=1$, and increases again.

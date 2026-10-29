# Exercise 2 — Circle by Completing the Square

## The Problem

Reduce

$$
x^2+y^2-6x+4y-3=0
$$

to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

---

## What Are We Looking For?

We want to rewrite a general second-degree equation as $(x-x_0)^2+(y-y_0)^2=r^2$, which shows the center and radius of the circle directly.

---

## Idea and Theorem Before the Calculation

**Completing the square:**

$$
x^2+bx=\left(x+\frac b2\right)^2-\frac{b^2}{4}.
$$

**Canonical form of a circle:** $(x-x_0)^2+(y-y_0)^2=r^2$ with $r>0$ describes the circle with center $(x_0,y_0)$ and radius $r$.

---

## Step-by-Step Solution

**Step 1: Group the terms.**

$$
(x^2-6x)+(y^2+4y)=3.
$$

**Step 2: Complete each square.**

$$
x^2-6x=(x-3)^2-9,\qquad y^2+4y=(y+2)^2-4.
$$

**Step 3: Substitute and simplify.**

$$
(x-3)^2-9+(y+2)^2-4=3\quad\Longrightarrow\quad (x-3)^2+(y+2)^2=16.
$$

*Why this is valid:* Each completed square equals the original expression, so the equation is unchanged; only its form is different.

**Step 4: Read off center and radius.**

$$
(x_0,y_0)=(3,-2),\qquad r=\sqrt{16}=4.
$$

---

## Final Answer in Words

The canonical form is $(x-3)^2+(y+2)^2=16$. The circle has center $(3,-2)$ and radius $4$.

---

## Quick Verification

Take two points at distance $4$ from the center: $(7,-2)$, to the right, and $(3,2)$, above.

**Point $(7,-2)$.**

$$
\begin{aligned}
\mathrm{canonical}:&\quad (7-3)^2+(-2+2)^2=16, \\
\mathrm{general}:&\quad 49+4-42-8-3=0.
\end{aligned}
$$

**Point $(3,2)$.**

$$
\begin{aligned}
\mathrm{canonical}:&\quad (3-3)^2+(2+2)^2=16, \\
\mathrm{general}:&\quad 9+4-18+8-3=0.
\end{aligned}
$$

Both points satisfy both forms, which confirms that the two equations describe the same circle.

---

## Common Mistakes

- **Forgetting to subtract the added squares:** completing $x^2-6x$ adds $9$, which must be subtracted again (or added to the right side).
- **Reading the center with the wrong signs:** $(x-3)^2+(y+2)^2$ has center $(3,-2)$, not $(-3,2)$.
- **Giving $r=16$:** the right side is $r^2$, so $r=4$.

---

## Oral Explanation (3 sentences)

Grouping the $x$-terms and the $y$-terms and completing the squares turns $x^2-6x$ into $(x-3)^2-9$ and $y^2+4y$ into $(y+2)^2-4$. Moving the constants to the right gives $(x-3)^2+(y+2)^2=16$, a circle with center $(3,-2)$ and radius $4$. The points $(7,-2)$ and $(3,2)$ lie at distance $4$ from the center and satisfy both the general and the canonical equation.

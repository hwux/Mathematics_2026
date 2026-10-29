# Exercise 6 — Shifted Ellipse

## The Problem

Reduce

$$
4x^2+9y^2-16x+18y-11=0
$$

to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

---

## What Are We Looking For?

We want to rewrite the equation as an ellipse with a shifted center, read off the center and the semiaxes, and check the result at the center.

---

## Idea and Theorem Before the Calculation

**Completing the square with a leading coefficient:** factor out the coefficient of the square first:

$$
4x^2-16x=4(x^2-4x)=4\left[(x-2)^2-4\right].
$$

**Shifted ellipse:** $\frac{(x-x_0)^2}{a^2}+\frac{(y-y_0)^2}{b^2}=1$ is an ellipse with center $(x_0,y_0)$ and semiaxes $a$ (horizontal) and $b$ (vertical).

---

## Step-by-Step Solution

**Step 1: Group and factor.**

$$
4(x^2-4x)+9(y^2+2y)=11.
$$

**Step 2: Complete the squares.**

$$
4\left[(x-2)^2-4\right]+9\left[(y+1)^2-1\right]=11.
$$

**Step 3: Expand the constants.**

$$
4(x-2)^2-16+9(y+1)^2-9=11\quad\Longrightarrow\quad 4(x-2)^2+9(y+1)^2=36.
$$

**Step 4: Divide by $36$.**

$$
\frac{(x-2)^2}{9}+\frac{(y+1)^2}{4}=1.
$$

*Why this is valid:* Completing the square and dividing both sides by the positive number $36$ do not change the set of solutions.

**Step 5: Read off the features.**

Center $(2,-1)$, semiaxes $a=3$ (horizontal) and $b=2$ (vertical).

---

## Final Answer in Words

The canonical form is $\frac{(x-2)^2}{9}+\frac{(y+1)^2}{4}=1$: an ellipse with center $(2,-1)$, horizontal semiaxis $3$ and vertical semiaxis $2$.

---

## Quick Verification

Substitute the center $(2,-1)$ into the original left-hand side:

$$
4\cdot4+9\cdot1-16\cdot2+18\cdot(-1)-11=16+9-32-18-11=-36.
$$

From Step 3, the left-hand side equals $4(x-2)^2+9(y+1)^2-36$, which at the center is $0+0-36=-36$. The two values agree.

As a second check, the vertex $(5,-1)$ should lie on the ellipse: $4\cdot25+9\cdot1-80-18-11=100+9-80-18-11=0$.

---

## Common Mistakes

- **Completing the square without factoring out $4$ and $9$:** the square must be completed inside the bracket, and the subtracted constant is then multiplied by the factor.
- **Reading the center as $(-2,1)$:** $(x-2)^2$ and $(y+1)^2$ give the center $(2,-1)$.
- **Reading the semiaxes as $9$ and $4$:** the semiaxes are $\sqrt9=3$ and $\sqrt4=2$.

---

## Oral Explanation (3 sentences)

Factoring out $4$ from the $x$-terms and $9$ from the $y$-terms and completing the squares gives $4(x-2)^2+9(y+1)^2=36$. Dividing by $36$ produces the canonical form $\frac{(x-2)^2}{9}+\frac{(y+1)^2}{4}=1$, an ellipse with center $(2,-1)$ and semiaxes $3$ and $2$. At the center the original left-hand side equals $-36$, which is exactly the value $0+0-36$ predicted by the completed-square form.

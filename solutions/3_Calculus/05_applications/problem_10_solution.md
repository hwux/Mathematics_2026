# Problem 10 — A Cable Through Water and Land

## The Problem

Point $A$ lies on one bank of a river of width $100$ m, and point $B$ lies on the other bank, $500$ m along the bank from the point directly opposite $A$.

The cost per meter of cable underwater is twice the cost per meter of cable on land.

Build a cost function depending on the point where the cable comes out of the water, determine the domain, and find the solution that minimizes the cost.

---

## What Are We Looking For?

We want the point on the far bank where the cable should leave the water so that the total cost of the underwater part plus the land part is as small as possible.

---

## Idea and Theorem Before the Calculation

**Coordinates:** Put $A=(0,0)$ on one bank and the opposite bank on the line $y=100$. The point directly opposite $A$ is $(0,100)$ and $B=(500,100)$.

**Cable route:** straight underwater from $A$ to an exit point $P=(x,100)$ on the far bank, then along the bank from $P$ to $B$.

**Costs:** let $c>0$ be the cost per meter on land, so $2c$ is the cost per meter underwater.

---

## Step-by-Step Solution

**Step 1: Lengths.**

$$
|AP|=\sqrt{x^2+100^2},\qquad |PB|=500-x.
$$

**Step 2: Cost function.**

$$
K(x)=2c\sqrt{x^2+10\,000}+c(500-x).
$$

**Step 3: Domain.**

The exit point must lie between the opposite point and $B$:

$$
0\le x\le500.
$$

(Exiting beyond $B$ or behind the opposite point only lengthens both parts.)

**Step 4: Derivative.**

$$
K'(x)=c\left(\frac{2x}{\sqrt{x^2+10\,000}}-1\right).
$$

**Step 5: Critical point.**

$$
2x=\sqrt{x^2+10\,000}\ \Longrightarrow\ 4x^2=x^2+10\,000\ \Longrightarrow\ x^2=\frac{10\,000}{3}\ \Longrightarrow\ x=\frac{100}{\sqrt3}\approx57.7\ \mathrm{m}.
$$

($x\ge0$, so the positive root is taken.)

**Step 6: Compare with the endpoints.**

At $x=\frac{100}{\sqrt3}$: $\sqrt{x^2+10\,000}=\sqrt{\frac{40\,000}{3}}=\frac{200}{\sqrt3}$, so

$$
K=c\left(\frac{400}{\sqrt3}+500-\frac{100}{\sqrt3}\right)=c\left(500+\frac{300}{\sqrt3}\right)=c\left(500+100\sqrt3\right)\approx673.2\,c.
$$

At the endpoints:

$$
K(0)=c(200+500)=700\,c,\qquad K(500)=2c\sqrt{260\,000}\approx1019.8\,c.
$$

The critical point gives the smallest value. Also $K'<0$ to its left and $K'>0$ to its right, so it is the minimum.

---

## Interpretation

The cable should go underwater to a point about $57.7$ m downstream from the point opposite $A$ and then run $442.3$ m along the bank. At the optimum $\frac{x}{\sqrt{x^2+100^2}}=\frac12$, so the underwater segment makes an angle of $30^\circ$ with the perpendicular to the river. Going straight across ($x=0$) is close but slightly worse; going diagonally all the way to $B$ is much worse because underwater cable is expensive.

---

## Final Answer in Words

The cost function is $K(x)=2c\sqrt{x^2+100^2}+c(500-x)$ for $0\le x\le500$. The minimum is at

$$
x=\frac{100}{\sqrt3}\approx57.7\ \mathrm{m},
$$

with cost $c(500+100\sqrt3)\approx673.2\,c$, compared with $700c$ for crossing straight and $1019.8c$ for going directly to $B$.

---

## Quick Verification

Nearby points: $K(50)=c(2\sqrt{12\,500}+450)\approx673.6\,c$ and $K(65)=c(2\sqrt{14\,225}+435)\approx673.5\,c$, both slightly above $673.2\,c$.

---

## Common Mistakes

- **Using the same cost on land and in water:** then the best route is the straight line from $A$ to $B$.
- **Measuring the land part from $A$:** the land part runs from the exit point $P$ to $B$.
- **Forgetting to compare with the endpoints:** on a closed interval they must be checked.

---

## Oral Explanation (3 sentences)

If the cable leaves the water at distance $x$ from the point opposite $A$, the cost is $2c\sqrt{x^2+100^2}+c(500-x)$ for $0\le x\le500$. The derivative vanishes when $2x=\sqrt{x^2+100^2}$, which gives $x=\frac{100}{\sqrt3}\approx57.7$ m. The cost there is about $673.2c$, lower than at both endpoints, so the cable should exit about $58$ m downstream and run the remaining $442$ m on land.

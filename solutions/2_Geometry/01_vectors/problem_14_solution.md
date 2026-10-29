# Exercise 14 — Closest Point on a Line

## The Problem

Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

---

## What Are We Looking For?

We want the point $Q$ of the line nearest to $P$, the distance $|PQ|$, and a check that the segment $PQ$ meets the line at a right angle.

---

## Idea and Theorem Before the Calculation

**Closest point = projection:** For a line through the origin with direction $v$, the closest point to $P$ is

$$
Q=\mathrm{proj}_v\,P=\frac{P\cdot v}{v\cdot v}\,v,
$$

where $P$ is treated as the vector from the origin. The segment from $Q$ to $P$ is then perpendicular to the line.

---

## Step-by-Step Solution

**Step 1: Dot products.**

$$
P\cdot v=4\cdot1+1\cdot2=6,\qquad v\cdot v=1+4=5.
$$

**Step 2: Closest point.**

$$
Q=\frac65(1,2)=\left(\frac65,\ \frac{12}{5}\right).
$$

**Step 3: Distance.**

$$
P-Q=\left(4-\frac65,\ 1-\frac{12}{5}\right)=\left(\frac{14}{5},\ -\frac75\right),
$$

$$
\|P-Q\|=\sqrt{\frac{196}{25}+\frac{49}{25}}=\sqrt{\frac{245}{25}}=\frac{7}{\sqrt5}=\frac{7\sqrt5}{5}\approx3.13.
$$

**Step 4: Perpendicularity check.**

$$
(P-Q)\cdot v=\frac{14}{5}\cdot1+\left(-\frac75\right)\cdot2=\frac{14}{5}-\frac{14}{5}=0.
$$

*Why this is valid:* For any other point $X$ of the line, the Pythagorean theorem gives $\|P-X\|^2=\|P-Q\|^2+\|Q-X\|^2>\|P-Q\|^2$, because $P-Q$ is perpendicular to $Q-X$. So $Q$ is the closest point.

---

## Final Answer in Words

The closest point of the line to $P$ is $Q=\left(\frac65,\frac{12}{5}\right)$, and the distance from $P$ to the line is $\frac{7}{\sqrt5}=\frac{7\sqrt5}{5}$. The vector $P-Q=\left(\frac{14}{5},-\frac75\right)$ is perpendicular to the direction $v$, since their dot product is $0$.

---

## Quick Verification

The line through the origin with direction $(1,2)$ is $2x-y=0$. The point-to-line distance formula gives

$$
d=\frac{|2\cdot4-1|}{\sqrt{4+1}}=\frac{7}{\sqrt5},
$$

the same value. Also $Q$ lies on the line: $2\cdot\frac65-\frac{12}{5}=0$.

---

## Common Mistakes

- **Reporting the coefficient $\frac65$ as the point:** the closest point is the vector $\frac65v$.
- **Measuring the distance from $P$ to the origin:** $\|P\|=\sqrt{17}$ is larger than the distance to the line.
- **Checking $Q\cdot v=0$ instead of $(P-Q)\cdot v=0$:** the segment from $Q$ to $P$ must be perpendicular to the line, not $Q$ itself.

---

## Oral Explanation (3 sentences)

Projecting $P=(4,1)$ onto the direction $v=(1,2)$ gives the closest point $Q=\frac65(1,2)=\left(\frac65,\frac{12}{5}\right)$. The vector from $Q$ to $P$ is $\left(\frac{14}{5},-\frac75\right)$, whose length $\frac{7}{\sqrt5}$ is the distance from $P$ to the line. Its dot product with $v$ is zero, so the segment meets the line at a right angle, which is exactly why $Q$ is the nearest point.

# Problem 8 — Number of Requests Handled by a Server

## The Problem

The rate at which requests arrive at a server during the first 5 minutes is described by the function

$$
r(t)=100+20t\quad [\mathrm{requests/min}],\qquad 0\le t\le5.
$$

1. Compute the total number of requests that arrived during this time.
2. Compute the average rate of incoming requests over this interval.
3. Compare the average rate with the values $r(0)$ and $r(5)$.

---

## What Are We Looking For?

We want the total number of requests in the first $5$ minutes, the average arrival rate, and a comparison of this average with the rates at the start and at the end.

---

## Idea and Theorem Before the Calculation

**Accumulation:** if $r(t)$ is a rate (requests per minute), the total amount arriving during $[a,b]$ is

$$
\int_a^br(t)\,dt.
$$

**Average rate:** $\bar r=\frac{1}{b-a}\int_a^br(t)\,dt$.

---

## Step-by-Step Solution

**Part 1: Total number of requests.**

$$
\int_0^5(100+20t)\,dt=\left[100t+10t^2\right]_0^5=500+250=750.
$$

**Part 2: Average rate.**

$$
\bar r=\frac{750}{5}=150\ \mathrm{requests/min}.
$$

**Part 3: Comparison.**

$$
r(0)=100,\qquad r(5)=200,\qquad \bar r=150=\frac{100+200}{2}.
$$

The average lies between the initial and final rates, and it is exactly their arithmetic mean. This is because $r$ is linear: its graph is a straight line, and the area under it is a trapezoid, whose average height is the mean of its two parallel sides. It also equals the rate at the middle of the interval, $r(2.5)=150$.

---

## Final Answer in Words

During the first $5$ minutes, $750$ requests arrive. The average arrival rate is $150$ requests per minute, which lies between $r(0)=100$ and $r(5)=200$ and, because the rate grows linearly, equals their mean.

---

## Quick Verification

Trapezoid area under the graph of $r$: parallel sides $100$ and $200$, width $5$, so the area is $\frac{100+200}{2}\cdot5=750$. Units: requests/min times min gives requests.

---

## Common Mistakes

- **$r(5)\cdot5=1000$:** this assumes the final rate for the whole interval.
- **$r(0)\cdot5=500$:** this assumes the initial rate for the whole interval.
- **Thinking the average of a rate is always the mean of the endpoints:** this holds only for linear rates.

---

## Oral Explanation (3 sentences)

The total number of requests is the integral of the arrival rate, $\int_0^5(100+20t)\,dt=750$. Dividing by the length of the interval gives the average rate of $150$ requests per minute. Since the rate grows linearly from $100$ to $200$, the average is exactly the mean of these two values, which the trapezoid picture confirms.

# 📏 Ratio Test

*Test whether an infinite series converges by measuring the long-run ratio of consecutive terms.*

## Core Formula

For a series $\displaystyle\sum_{n=1}^{\infty} a_n$, compute:

$$
L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right|
$$

- **$L < 1$**: the series **converges absolutely**.
- **$L > 1$ (or $L = \infty$)**: the series **diverges**.
- **$L = 1$**: the test is **inconclusive** (you must use another test, such as the $p$-series, Comparison, or Alternating Series Test).

## What It Means

The Ratio Test compares each next term $a_{n+1}$ to the current term $a_n$. It is the go-to test whenever $a_n$ contains **factorials ($n!$), exponentials ($c^n$), or power series terms ($(x-a)^n$)**, because dividing $a_{n+1}$ by $a_n$ causes almost everything to cancel cleanly.

## Intuition

Think of a geometric series $\sum r^n$, where the ratio of consecutive terms is $\left|\frac{r^{n+1}}{r^n}\right| = |r|$. A geometric series converges when $|r| < 1$ and diverges when $|r| > 1$. The Ratio Test asks: *"For large $n$, does our series shrink faster than a convergent geometric series with ratio $L < 1$?"*

## Example

**Problem:** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{n^2}{3^n}$ converges or diverges.

Form $\left|\frac{a_{n+1}}{a_n}\right|$ by multiplying $a_{n+1}$ by the reciprocal of $a_n$:

$$
L = \lim_{n \to \infty} \left|\frac{(n+1)^2}{3^{n+1}} \cdot \frac{3^n}{n^2}\right| = \lim_{n \to \infty} \frac{1}{3}\left(\frac{n+1}{n}\right)^2 = \frac{1}{3}(1)^2 = \frac{1}{3}
$$

Since $L = \frac{1}{3} < 1$, the series **converges** by the Ratio Test.

## Common Mistakes

- **Using the Ratio Test on pure $p$-series or rational functions of $n$**: for $\sum \frac{1}{n^2}$ or $\sum \frac{1}{n}$, the Ratio Test always gives $L = 1$ (inconclusive). Save the Ratio Test for factorials and exponentials!
- **Simplifying $(n+1)!$ incorrectly**: remember $(n+1)! = (n+1) \cdot n!$, so $\frac{n!}{(n+1)!} = \frac{1}{n+1}$.
- **Concluding convergence when $L = 1$**: $L = 1$ gives zero information; for power series $\sum c_n(x-a)^n$, you must plug in the endpoints where $L = 1$ and test them separately.

## Remember

> Spot **$n!$ or $c^n$** $\implies$ run the Ratio Test: **$L < 1$ converges, $L > 1$ diverges, $L = 1$ tells you nothing**.

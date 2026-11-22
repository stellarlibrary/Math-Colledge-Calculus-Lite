# ♾️ Improper Integrals

*Evaluate integrals over infinite intervals or across vertical asymptotes by replacing the trouble spot with a limit.*

## Core Formula

**Type 1 (Infinite Interval):**

$$
\int_a^{\infty} f(x)\,dx = \lim_{t \to \infty} \int_a^t f(x)\,dx
$$

**The Benchmark $p$-Integral on $[1, \infty)$:**

$$
\int_1^{\infty} \frac{1}{x^p}\,dx = \begin{cases} \dfrac{1}{p - 1} \text{ (Converges)}, & \text{if } p > 1 \\[6pt] \infty \text{ (Diverges)}, & \text{if } p \le 1 \end{cases}
$$

- **Converges**: the limit exists and is a **finite number**.
- **Diverges**: the limit is $\pm\infty$ or does not exist.

## What It Means

An integral is **improper** if either:
1. One or both bounds are infinite ($\pm\infty$), or
2. The integrand $f(x)$ has an infinite discontinuity (vertical asymptote) at an endpoint or inside $[a, b]$.

You never plug $\infty$ directly into an antiderivative; instead, you integrate up to a dummy variable $t$ and take the limit as $t$ approaches $\infty$ (or the asymptote).

## Intuition

How can an infinitely long region have a finite area? It depends on **how fast the curve hugs the $x$-axis**:
- For $\frac{1}{x^2}$ ($p = 2 > 1$), the height drops fast enough that the tail area adds up to exactly $1$.
- For $\frac{1}{x}$ ($p = 1$), the curve drops too slowly ($\ln t \to \infty$), so the area grows without bound.

## Example

**Problem:** Determine whether $\displaystyle\int_1^{\infty} \frac{1}{x^3}\,dx$ converges or diverges, and find its value if it converges.

$$
\int_1^{\infty} x^{-3}\,dx = \lim_{t \to \infty} \int_1^t x^{-3}\,dx = \lim_{t \to \infty} \left[-\frac{1}{2x^2}\right]_1^t = \lim_{t \to \infty} \left(-\frac{1}{2t^2} + \frac{1}{2}\right) = 0 + \frac{1}{2} = \frac{1}{2}
$$

Since the limit is finite, the integral **converges to $\frac{1}{2}$** (matching $\frac{1}{p-1} = \frac{1}{3-1} = \frac{1}{2}$).

## Common Mistakes

- **Missing a hidden vertical asymptote inside $[a, b]$**: for $\int_{-1}^1 \frac{1}{x^2}\,dx$, $x = 0$ is a vertical asymptote! You must split it into $\int_{-1}^0 + \int_0^1$ (which diverges)—plugging in $[-1/x]_{-1}^1 = -2$ is completely wrong.
- **Confusing $\int_1^\infty \frac{1}{x^p}\,dx$ with $\int_0^1 \frac{1}{x^p}\,dx$**: on $[1, \infty)$ it converges for $p > 1$, whereas near $0$ on $(0, 1]$ it converges for $p < 1$.

## Remember

> Replace $\infty$ (or an asymptote) with $t$ and take $\lim$; on $[1, \infty)$, **$\int_1^\infty \frac{1}{x^p}\,dx$ converges iff $p > 1$**.

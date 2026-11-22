# 📊 Definite Integral (FTC Part 2)

*Measures the net signed area under a curve—computed by evaluating any antiderivative at the endpoints.*

## Core Formula

$$
\int_a^b f(x)\,dx = \Big[F(x)\Big]_a^b = F(b) - F(a)
$$

- **$[a, b]$**: the interval of integration (from lower bound $a$ to upper bound $b$).
- **$f(x)$**: the continuous integrand (rate of change or height of the curve).
- **$F(x)$**: **any** antiderivative of $f(x)$, meaning $F'(x) = f(x)$.

## What It Means

A definite integral $\int_a^b f(x)\,dx$ represents the **net signed area** between $y = f(x)$ and the $x$-axis from $x = a$ to $x = b$ (area above the $x$-axis counts as positive; area below counts as negative). By the **Evaluation Theorem (FTC Part 2)**, instead of taking a limit of Riemann sums, you simply find an antiderivative $F(x)$ and compute **top bound minus bottom bound**: $F(b) - F(a)$.

## Intuition

If $f(t)$ is your velocity (mph), then the antiderivative $F(t)$ is your mile marker on the highway. The total net displacement between time $t = a$ and time $t = b$ is simply your ending mile marker minus your starting mile marker: $F(b) - F(a)$. All the tiny steps in between telescope into the difference at the endpoints.

## Example

**Problem:** Evaluate $\displaystyle\int_1^3 (3x^2 - 2x)\,dx$.

Find an antiderivative $F(x) = x^3 - x^2$, then evaluate at $b = 3$ and $a = 1$:

$$
\int_1^3 (3x^2 - 2x)\,dx = \Big[x^3 - x^2\Big]_1^3 = \big(3^3 - 3^2\big) - \big(1^3 - 1^2\big) = (27 - 9) - (1 - 1) = 18
$$

## Common Mistakes

- **Subtracting in the wrong order**: it is always $F(\text{upper}) - F(\text{lower})$, i.e., $F(b) - F(a)$, never $F(a) - F(b)$.
- **Assuming $F(0) = 0$**: functions like $e^x$ and $\cos x$ equal $1$ at $x = 0$, not $0$! Always plug in the lower bound carefully.
- **Confusing net area with total area**: if a question asks for *total area* (not net signed area), split the integral where $f(x) = 0$ and integrate $|f(x)|$.

## Remember

> Definite integral returns a **number** (net change): find an antiderivative $F$, then compute **$F(\text{top}) - F(\text{bottom})$**.

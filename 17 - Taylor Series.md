# 🔭 Taylor Series

*Build an infinite polynomial centered at $x = a$ by matching all derivatives of $f$ at that point.*

## Core Formula

$$
f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x - a)^n = f(a) + f'(a)(x - a) + \frac{f''(a)}{2!}(x - a)^2 + \frac{f'''(a)}{3!}(x - a)^3 + \cdots
$$

- **$a$**: the center of the approximation.
- **$f^{(n)}(a)$**: the $n$-th derivative of $f$ evaluated at $x = a$ (a constant number, not a function of $x$).
- **$n!$**: factorial scaling ($0! = 1, 1! = 1, 2! = 2, 3! = 6, \dots$).
- **$(x - a)^n$**: powers of the distance from the center $a$.

## What It Means

A Taylor series represents a smooth function $f(x)$ near $x = a$ as an infinite polynomial. Stopping after degree $N$ gives the **$N$-th degree Taylor polynomial $T_N(x)$**:
- $T_0(x) = f(a)$ matches the **height** at $x = a$.
- $T_1(x) = f(a) + f'(a)(x - a)$ is the **tangent line** (matches height + slope).
- $T_2(x)$ adds $\frac{f''(a)}{2!}(x - a)^2$ to match the **concavity/bending**, and higher terms hug the curve ever more closely.

## Intuition

Why divide by $n!$? Because differentiating $(x - a)^n$ $n$ times brings down $n \cdot (n-1) \cdots 2 \cdot 1 = n!$. Dividing by $n!$ cancels that cascade so the series and $f(x)$ have the exact same $n$-th derivative at $x = a$.

## Example

**Problem:** Find the first four terms of the Taylor series for $f(x) = \ln x$ centered at $a = 1$.

Compute derivatives at $a = 1$:
- $f(x) = \ln x \implies f(1) = 0$
- $f'(x) = x^{-1} \implies f'(1) = 1$
- $f''(x) = -x^{-2} \implies f''(1) = -1$
- $f'''(x) = 2x^{-3} \implies f'''(1) = 2$

$$
\ln x = 0 + 1(x - 1) - \frac{1}{2!}(x - 1)^2 + \frac{2}{3!}(x - 1)^3 - \cdots = (x - 1) - \frac{(x - 1)^2}{2} + \frac{(x - 1)^3}{3} - \cdots
$$

## Common Mistakes

- **Leaving $x$ inside $f^{(n)}(a)$**: the coefficient $\frac{f^{(n)}(a)}{n!}$ must be evaluated at the number $a$, so only $(x - a)^n$ contains $x$.
- **Forgetting $n!$ in the denominator**: notice that in the $\ln x$ example above, $\frac{f'''(1)}{3!} = \frac{2}{6} = \frac{1}{3}$ because $(n-1)!$ cancels with $n!$.

## Remember

> Each term is **$\dfrac{\text{$n$-th derivative at $a$}}{n!} \cdot (x - a)^n$**: match value, slope, concavity, and beyond at $x = a$.

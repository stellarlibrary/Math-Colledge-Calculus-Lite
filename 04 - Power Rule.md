# ⚡ Power Rule

*The workhorse shortcut for differentiating any power of $x$—polynomials, roots, and reciprocals alike.*

## Core Formula

$$
\frac{d}{dx}\left(x^n\right) = n x^{n-1}
$$

- **$x$**: the variable base.
- **$n$**: any fixed real constant exponent (positive, negative, or fractional).

Useful rewrites before applying the rule:

$$
\frac{1}{x^k} = x^{-k}, \qquad \sqrt[m]{x^k} = x^{k/m}, \qquad \frac{d}{dx}(c) = 0
$$

## What It Means

To differentiate $x$ raised to a constant power $n$, **multiply by the old exponent** $n$ in front and **subtract $1$ from the exponent**. Because derivatives are linear, you can differentiate a polynomial term-by-term and pull constants out front: $\frac{d}{dx}[c\,x^n] = c\cdot n x^{n-1}$.

## Intuition

Think of a square of side $x$ (area $x^2$) or a cube of side $x$ (volume $x^3$). When $x$ grows slightly, a square expands along $2$ edges of length $x$ (rate $2x$), and a cube expands along $3$ faces of area $x^2$ (rate $3x^2$). Each derivative drops one dimension: volume ($x^3$) $\to$ surface area ($3x^2$) $\to$ edge length ($6x$).

## Example

**Problem:** Differentiate $f(x) = 4x^3 - \sqrt{x} + \frac{5}{x^2}$.

First rewrite roots and fractions as powers of $x$:

$$
f(x) = 4x^3 - x^{1/2} + 5x^{-2}
$$

Apply the Power Rule to each term:

$$
f'(x) = 12x^2 - \frac{1}{2}x^{-1/2} - 10x^{-3} = 12x^2 - \frac{1}{2\sqrt{x}} - \frac{10}{x^3}
$$

## Common Mistakes

- **Adding instead of subtracting $1$ on negative powers**: the derivative of $x^{-2}$ is $-2x^{-3}$ (since $-2 - 1 = -3$), **not** $-2x^{-1}$.
- **Using the Power Rule when $x$ is in the exponent**: $\frac{d}{dx}(2^x) \neq x\cdot 2^{x-1}$. The Power Rule requires a *variable base* and *constant exponent* ($x^n$).

## Remember

> Rewrite roots and fractions as $x^n$, then **bring the power down and drop the exponent by $1$**.

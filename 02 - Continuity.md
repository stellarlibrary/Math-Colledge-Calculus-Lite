# 🔗 Continuity

*A function has no breaks, jumps, or holes at a point when its limit matches its actual value.*

## Core Formula

$$
\lim_{x \to a} f(x) = f(a)
$$

This single equation packs **three required conditions** at $x = a$:
1. **$f(a)$ is defined** (there is a solid point at $x = a$).
2. **$\lim_{x \to a} f(x)$ exists** (left and right limits match).
3. **The limit equals the function value**: $\lim_{x \to a} f(x) = f(a)$.

## What It Means

Continuity means small changes in the input $x$ produce small, predictable changes in the output $f(x)$. When a function is continuous at $x = a$, you can evaluate the limit simply by **direct substitution**—plugging $a$ straight into $f(x)$. Polynomials, $\sin x$, $\cos x$, and $e^x$ are continuous everywhere; rational functions and $\ln x$ are continuous on their domains.

## Intuition

Think of drawing the curve on paper: if $f$ is continuous on an interval, you can trace the entire graph **without lifting your pen**. Lifting your pen means hitting a **hole** (removable discontinuity), a **step** (jump discontinuity), or a **vertical asymptote** (infinite discontinuity).

## Example

**Problem:** Find $k$ so that $f(x) = \begin{cases} 3x + 1, & x < 2 \\ kx^2 - 1, & x \ge 2 \end{cases}$ is continuous at $x = 2$.

Set the left-hand limit equal to the right-hand limit (and value) at $x = 2$:

$$
\lim_{x \to 2^-} (3x + 1) = 7, \qquad \lim_{x \to 2^+} (kx^2 - 1) = 4k - 1
$$

$$
4k - 1 = 7 \implies 4k = 8 \implies k = 2
$$

## Common Mistakes

- **Checking only that $f(a)$ exists**: a piecewise function can be defined everywhere yet still have a jump if the two pieces don't meet at the boundary.
- **Forgetting domain restrictions**: $f(x) = \frac{1}{x - 3}$ is not continuous at $x = 3$ because $x = 3$ is not in the domain.

## Remember

> Continuous at $a$ means **no holes, no jumps, no asymptotes**: what the function *approaches* is what it *is*.

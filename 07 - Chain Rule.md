# ⛓️ Chain Rule

*How to differentiate nested (composite) functions by peeling them from the outside in.*

## Core Formula

$$
\frac{d}{dx}\big[f(g(x))\big] = f'(g(x)) \cdot g'(x)
$$

In Leibniz notation (where $y = f(u)$ and $u = g(x)$):

$$
\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}
$$

- **$f(\cdot)$**: the **outer** function.
- **$g(x)$**: the **inner** function ("the inside stuff").
- **$f'(g(x))$**: derivative of the outer function, evaluated at the **unchanged** inner function.
- **$g'(x)$**: derivative of the inner function, multiplied on at the end.

## What It Means

Whenever a function is plugged inside another function—like $\sin(x^2)$, $(3x+1)^5$, or $e^{-4x}$—you differentiate the outer shell first while keeping the inside untouched, then **multiply by the derivative of the inside**.

## Intuition

Think of connected gears: if $y$ changes $3$ times as fast as $u$ ($\frac{dy}{du} = 3$), and $u$ changes $2$ times as fast as $x$ ($\frac{du}{dx} = 2$), then $y$ changes $3 \times 2 = 6$ times as fast as $x$. Rates of change **multiply** down a chain of dependencies.

## Example

**Problem:** Differentiate $y = \cos(5x^3 - 2)$.

- Outer function: $\cos(u) \implies$ derivative is $-\sin(u)$
- Inner function: $u = 5x^3 - 2 \implies$ derivative is $u' = 15x^2$

$$
y' = -\sin(5x^3 - 2) \cdot (15x^2) = -15x^2 \sin(5x^3 - 2)
$$

## Common Mistakes

- **Differentiating the inside at the same time as the outside**: $\frac{d}{dx}[\cos(5x^3 - 2)]$ is **not** $-\sin(15x^2)$. The inside stays $5x^3 - 2$ inside $-\sin(\cdot)$.
- **Forgetting to multiply by $g'(x)$**: dropping the "tail" factor $g'(x)$ is the most common mistake on calculus exams.

## Remember

> Peel the onion from the outside in: **derivative of the outside (keep inside same) $\times$ derivative of the inside**.

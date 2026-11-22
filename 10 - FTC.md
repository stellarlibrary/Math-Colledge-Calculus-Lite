# 🌉 Fundamental Theorem of Calculus (Part 1)

*Differentiation and integration are inverse operations: the rate at which area accumulates equals the curve's height.*

## Core Formula

If $f$ is continuous on $[a, b]$, then for $x \in (a, b)$:

$$
\frac{d}{dx} \int_a^x f(t)\,dt = f(x)
$$

With the Chain Rule (when the upper limit is a function $g(x)$):

$$
\frac{d}{dx} \int_a^{g(x)} f(t)\,dt = f(g(x)) \cdot g'(x)
$$

- **$a$**: a fixed constant lower bound.
- **$x$ (or $g(x)$)**: the moving upper bound of accumulation.
- **$t$**: dummy integration variable that disappears once evaluated at the bound.

## What It Means

FTC Part 1 bridges the two halves of calculus. If you define an area-accumulation function $A(x) = \int_a^x f(t)\,dt$ and then take its derivative with respect to $x$, the derivative $\frac{d}{dx}$ directly cancels the integral $\int_a^x$, leaving $f(x)$.

## Intuition

Imagine painting the region under $y = f(t)$ from left to right. At position $x$, the vertical edge of your paintbrush has height $f(x)$. If you move the brush a tiny step $dx$ to the right, the new sliver of area added is $\text{height} \times \text{width} \approx f(x)\,dx$. Dividing by $dx$, the instantaneous rate of area growth is $\frac{dA}{dx} = f(x)$.

## Example

**Problem:** Find $\displaystyle\frac{d}{dx} \int_1^{x^3} \sqrt{1 + t^4}\,dt$.

Here $f(t) = \sqrt{1 + t^4}$ and the upper limit is $g(x) = x^3$ (with $g'(x) = 3x^2$). Do **not** try to antidifferentiate—apply FTC Part 1 with the Chain Rule:

$$
\frac{d}{dx} \int_1^{x^3} \sqrt{1 + t^4}\,dt = \sqrt{1 + (x^3)^4} \cdot (3x^2) = 3x^2\sqrt{1 + x^{12}}
$$

## Common Mistakes

- **Trying to compute the antiderivative first**: functions like $e^{t^2}$ or $\sqrt{1+t^4}$ have no elementary antiderivative—FTC Part 1 lets you bypass antidifferentiation completely.
- **Forgetting $g'(x)$ when the upper bound is not just $x$**: always multiply by the derivative of the upper bound.
- **Variable in the lower bound**: if $x$ is on the bottom, flip the bounds first using $\int_x^a f(t)\,dt = -\int_a^x f(t)\,dt$.

## Remember

> Plug the upper bound into $f(t)$ and **multiply by the upper bound's derivative**: $f(g(x)) \cdot g'(x)$.

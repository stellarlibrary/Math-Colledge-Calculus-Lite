# 🧵 Arc Length

*Measure the exact walking distance along a curve by summing tiny Pythagorean hypotenuse segments.*

## Core Formula

For a smooth curve $y = f(x)$ on $[a, b]$:

$$
L = \int_a^b \sqrt{1 + \big[f'(x)\big]^2}\,dx = \int_a^b \sqrt{1 + \left(\frac{dy}{dx}\right)^2}\,dx
$$

For a curve $x = g(y)$ on $[c, d]$:

$$
L = \int_c^d \sqrt{1 + \left(\frac{dx}{dy}\right)^2}\,dy
$$

- **$ds = \sqrt{1 + (f'(x))^2}\,dx$**: the infinitesimal arc-length element.

## What It Means

While a standard integral $\int_a^b f(x)\,dx$ finds the area *under* a curve, the **Arc Length formula** measures the actual length of the curve itself—as if you laid a piece of string along the graph from $(a, f(a))$ to $(b, f(b))$ and straightened it out against a ruler.

## Intuition

Slice the curve into tiny pieces with horizontal run $dx$ and vertical rise $dy$. By the **Pythagorean Theorem**, the straight-line length $ds$ of each tiny piece is:

$$
ds = \sqrt{(dx)^2 + (dy)^2} = \sqrt{1 + \left(\frac{dy}{dx}\right)^2}\,dx
$$

Integrating $ds$ from $a$ to $b$ adds up all the tiny hypotenuses.

## Example

**Problem:** Find the arc length of $y = \frac{2}{3}x^{3/2}$ from $x = 0$ to $x = 3$.

1. Differentiate and square: $y' = x^{1/2} \implies (y')^2 = x$.
2. Substitute into the arc length integral and use $u = 1 + x$ ($du = dx$):

$$
L = \int_0^3 \sqrt{1 + x}\,dx = \left[\frac{2}{3}(1 + x)^{3/2}\right]_0^3 = \frac{2}{3}\left(4^{3/2} - 1^{3/2}\right) = \frac{2}{3}(8 - 1) = \frac{14}{3}
$$

## Common Mistakes

- **Using $f(x)$ instead of $f'(x)$ inside the square root**: the formula uses the **derivative squared** $[f'(x)]^2$, not $[f(x)]^2$.
- **Forgetting to square $f'(x)$ or dropping the $1 +$**: never simplify $\sqrt{1 + (f'(x))^2}$ as $1 + f'(x)$! Square roots do **not** split across addition.

## Remember

> Arc length is the **Pythagorean Theorem in integral form**: $ds = \sqrt{(dx)^2 + (dy)^2} = \sqrt{1 + (y')^2}\,dx$.

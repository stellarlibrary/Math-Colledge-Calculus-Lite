# ⚖️ Mean Value Theorem (MVT)

*Somewhere on a smooth curve, the instantaneous tangent slope must match the overall average secant slope.*

## Core Formula

If $f$ is:
1. **Continuous** on the closed interval $[a, b]$, and
2. **Differentiable** on the open interval $(a, b)$,

then there exists at least one number $c \in (a, b)$ such that:

$$
f'(c) = \frac{f(b) - f(a)}{b - a}
$$

- **$f'(c)$**: instantaneous rate of change (tangent slope) at $x = c$.
- **$\frac{f(b) - f(a)}{b - a}$**: average rate of change (secant slope) across $[a, b]$.

## What It Means

The Mean Value Theorem guarantees that a smooth, unbroken curve between $(a, f(a))$ and $(b, f(b))$ has at least one interior point $c$ where the **tangent line is parallel to the secant line** connecting the endpoints. (When $f(a) = f(b)$, this special case is **Rolle's Theorem**, giving $f'(c) = 0$.)

## Intuition

Suppose you drive $120$ miles in $2$ hours on a toll road. Your average speed is $\frac{120}{2} = 60\text{ mph}$. Even if you sped up and slowed down along the way, your speedometer **must have read exactly $60\text{ mph}$ at least once** during the trip.

## Example

**Problem:** Verify MVT and find $c$ for $f(x) = x^2$ on $[1, 5]$.

$f(x) = x^2$ is a polynomial, so it is continuous on $[1, 5]$ and differentiable on $(1, 5)$. Set $f'(c) = 2c$ equal to the average slope:

$$
2c = \frac{f(5) - f(1)}{5 - 1} = \frac{25 - 1}{4} = 6 \implies c = 3 \in (1, 5)
$$

## Common Mistakes

- **Skipping the hypothesis check**: MVT fails if there is a discontinuity or sharp corner inside $(a, b)$—for example, $f(x) = |x|$ on $[-1, 1]$ has no point where $f'(c) = 0$ because $f'(0)$ is undefined.
- **Including $c$ values outside $(a, b)$**: if a quadratic gives two roots for $c$, only keep the root strictly inside the open interval $(a, b)$.

## Remember

> On a continuous, smooth trip from $a$ to $b$, **instantaneous slope $=$ average slope** at some $c \in (a, b)$.

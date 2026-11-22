# 🎢 Second Derivative

*The rate of change of the slope—measuring acceleration and providing a quick test for local extrema.*

## Core Formula

$$
f''(x) = \frac{d}{dx}\big[f'(x)\big] = \frac{d^2y}{dx^2}
$$

**Second Derivative Test** (when $f'(c) = 0$):
- **$f''(c) > 0$** (concave up $\cup$) $\implies$ $f(c)$ is a **Local Minimum**.
- **$f''(c) < 0$** (concave down $\cap$) $\implies$ $f(c)$ is a **Local Maximum**.
- **$f''(c) = 0$** $\implies$ **Test is inconclusive** (fall back to the First Derivative Test).

## What It Means

While the first derivative $f'(x)$ tells you whether $f(x)$ is increasing or decreasing (velocity), the **second derivative $f''(x)$** tells you how fast the **slope $f'(x)$ itself is changing** (acceleration). At a flat critical point ($f'(c) = 0$), the sign of $f''(c)$ immediately classifies whether the point sits at the bottom of a bowl or the top of a hill.

## Intuition

Think of driving a car:
- **$f(t)$** is your **position** on the road.
- **$f'(t)$** is your **velocity** (speedometer).
- **$f''(t)$** is your **acceleration** (gas pedal vs. brake pedal).

At a critical point ($f'(c) = 0$), if $f''(c) > 0$, the slope is increasing from negative to positive, curving upward like a smile ($\cup$), so $c$ must be the **bottom of the bowl (local minimum)**.

## Example

**Problem:** Use the Second Derivative Test to classify the critical points of $f(x) = x^3 - 3x^2 + 1$.

We have $f'(x) = 3x^2 - 6x = 0 \implies x = 0, 2$, and $f''(x) = 6x - 6$:
- At $x = 0$: $f''(0) = -6 < 0$ (concave down $\cap$) $\implies$ **Local Maximum** at $x = 0$.
- At $x = 2$: $f''(2) = +6 > 0$ (concave up $\cup$) $\implies$ **Local Minimum** at $x = 2$.

## Common Mistakes

- **Mixing up the signs in the Second Derivative Test**: $f''(c) > 0$ is a **minimum** (not a maximum!), and $f''(c) < 0$ is a **maximum**. Picture $\cup$ ($+$, min at bottom) vs. $\cap$ ($-$, max at top).
- **Concluding "no extremum" when $f''(c) = 0$**: $f''(c) = 0$ is **inconclusive**—for example, $f(x) = x^4$ has $f''(0) = 0$ yet still has a local minimum at $x = 0$.

## Remember

> At $f'(c) = 0$: **$f''(c) > 0$ smiles ($\cup$, Local Min)** and **$f''(c) < 0$ frowns ($\cap$, Local Max)**.

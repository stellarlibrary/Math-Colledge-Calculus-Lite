# 🔀 Inflection Points

*A point on a continuous curve where the bending switches from concave up to concave down (or vice versa).*

## Core Formula

A point $(c, f(c))$ on the graph of a continuous function $f$ is an **inflection point** if:
1. **Candidates:** $f''(c) = 0$ or $f''(c)$ does not exist, **AND**
2. **Sign Change:** $f''(x)$ **changes sign** ($+$ to $-$, or $-$ to $+$) as $x$ passes through $c$.

$$
f''(x) \text{ changes sign at } x = c \quad \Longleftrightarrow \quad (c, f(c)) \text{ is an inflection point}
$$

## What It Means

An inflection point marks the exact transition where a curve stops bending one way ($\cup$ or $\cap$) and starts bending the other way. It is also the point where the **rate of change $f'(x)$ reaches a local maximum or minimum** (the steepest uphill or downhill spot on an S-curve).

## Intuition

Imagine driving along a winding S-shaped road. At first you are turning the steering wheel to the left (concave up), and then you turn the steering wheel to the right (concave down). The exact instant where your **steering wheel passes through straight-ahead**—switching from a left turn to a right turn—is the **inflection point**.

## Example

**Problem:** Find all inflection points of $f(x) = x^4 - 2x^3$.

Differentiate twice:

$$
f'(x) = 4x^3 - 6x^2, \qquad f''(x) = 12x^2 - 12x = 12x(x - 1)
$$

Candidates where $f''(x) = 0$: $x = 0$ and $x = 1$. Check the sign of $f''(x)$:
- On $(-\infty, 0)$: $f''(-1) = 24 > 0$ ($\cup$)
- On $(0, 1)$: $f''(0.5) = -3 < 0$ ($\cap$) $\implies$ sign changes at $x = 0$
- On $(1, \infty)$: $f''(2) = 24 > 0$ ($\cup$) $\implies$ sign changes at $x = 1$

Both $(0, 0)$ and $(1, -1)$ are **inflection points**.

## Common Mistakes

- **Stopping as soon as $f''(c) = 0$ without checking for a sign change**: for $f(x) = x^4$, $f''(x) = 12x^2 = 0$ at $x = 0$, but $f''(x) > 0$ on **both** sides of $0$. Thus $(0, 0)$ is a local minimum, **not** an inflection point!
- **Calling a vertical asymptote an inflection point**: $f(x) = \frac{1}{x}$ changes concavity across $x = 0$, but $x = 0$ is not an inflection point because $f(0)$ is undefined.

## Remember

> $f''(c) = 0$ is only a **candidate**—an inflection point requires $f''(x)$ to **actually change sign** at $x = c$.

# 📍 Critical Points

*The candidate locations for local peaks and valleys—where the slope is zero or undefined.*

## Core Formula

A number $c$ in the **domain** of $f$ is a **critical number** if:

$$
f'(c) = 0 \qquad \text{or} \qquad f'(c) \text{ does not exist (DNE)}
$$

**First Derivative Test at $x = c$:**
- $f'(x)$ changes from **$+$ to $-$** $\implies$ **Local Maximum** at $c$.
- $f'(x)$ changes from **$-$ to $+$** $\implies$ **Local Minimum** at $c$.
- $f'(x)$ does **not** change sign $\implies$ **Neither** (a flat terrace/saddle point).

## What It Means

By **Fermat's Theorem**, every local maximum or minimum of a function *must* occur at a critical point. However, the reverse is not automatic: critical points are **candidates** for local extrema that must be tested by checking whether $f'(x)$ actually changes sign across $x = c$.

## Intuition

Imagine hiking over a mountain range. At the very top of a smooth peak or the very bottom of a valley, the ground beneath your feet is momentarily **flat** ($f'(c) = 0$), or forms a **sharp ridge/corner** ($f'(c)$ undefined). You can never switch from climbing uphill ($f' > 0$) to walking downhill ($f' < 0$) without passing through one of those two states.

## Example

**Problem:** Find and classify the critical points of $f(x) = x^3 - 3x^2 + 1$.

Differentiate and set $f'(x) = 0$ ($f'$ is defined everywhere):

$$
f'(x) = 3x^2 - 6x = 3x(x - 2) = 0 \implies x = 0 \text{ or } x = 2
$$

Test the sign of $f'(x)$ on $(-\infty, 0)$, $(0, 2)$, and $(2, \infty)$:
- On $(-\infty, 0)$: $f'(-1) = 9 > 0$ ($\nearrow$)
- On $(0, 2)$: $f'(1) = -3 < 0$ ($\searrow$) $\implies$ **Local max at $x = 0$**, $f(0) = 1$
- On $(2, \infty)$: $f'(3) = 9 > 0$ ($\nearrow$) $\implies$ **Local min at $x = 2$**, $f(2) = -3$

## Common Mistakes

- **Forgetting where $f'(c)$ is undefined**: for $f(x) = x^{2/3}$, $f'(x) = \frac{2}{3x^{1/3}}$ is never $0$, but $x = 0$ is a critical number (and a local min!) because $f'(0)$ is undefined.
- **Including points outside the domain of $f$**: if $f(x) = \frac{1}{x}$, $f'(0)$ is undefined, but $x = 0$ is **not** a critical number because $f(0)$ is not in the domain.
- **Assuming every $f'(c) = 0$ is a max or min**: for $f(x) = x^3$, $f'(0) = 0$, but $f'(x) = 3x^2 \ge 0$ on both sides, so $x = 0$ is neither a max nor a min.

## Remember

> Critical points live in the **domain of $f$** where **$f'(c) = 0$ or $f'(c)$ DNE**—always check for a sign change in $f'$!

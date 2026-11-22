# 📈 Derivative Definition

*The instantaneous rate of change of a function, found by shrinking a secant interval to zero.*

## Core Formula

$$
f'(x) = \lim_{h \to 0} \frac{f(x + h) - f(x)}{h}
$$

Alternative form at a specific point $x = a$:

$$
f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}
$$

- **$h$**: a tiny step in the input $x$.
- **$f(x+h) - f(x)$**: the resulting change in output ($\Delta y$).
- **$\frac{f(x+h) - f(x)}{h}$**: the difference quotient (average rate of change / secant slope).

## What It Means

The derivative $f'(x)$ (also written $\frac{dy}{dx}$) measures how fast $f(x)$ is changing at a single instant. Geometrically, $f'(a)$ is the **slope of the tangent line** to the graph $y = f(x)$ at $x = a$. Physically, if $s(t)$ is position, then $s'(t)$ is instantaneous velocity.

## Intuition

A secant line connects two points on a curve at $x$ and $x + h$. As you slide the second point closer ($h \to 0$), the secant line pivots until it just kisses the curve at a single point—becoming the **tangent line**. If you zoom in far enough on any smooth curve, it looks like that straight tangent line.

## Example

**Problem:** Use the limit definition to find $f'(x)$ for $f(x) = x^2$.

$$
f'(x) = \lim_{h \to 0} \frac{(x + h)^2 - x^2}{h} = \lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h}
$$

$$
= \lim_{h \to 0} \frac{h(2x + h)}{h} = \lim_{h \to 0} (2x + h) = 2x
$$

At $x = 1$, the tangent slope is $f'(1) = 2(1) = 2$.

## Common Mistakes

- **Dropping $\lim_{h \to 0}$ too early**: keep writing $\lim_{h \to 0}$ on every step until you actually substitute $h = 0$ after canceling $h$.
- **Distributing the minus sign wrong**: in $f(x+h) - f(x)$, always wrap $f(x)$ in parentheses so every term of $f(x)$ is subtracted.
- **Assuming continuity implies differentiability**: sharp corners (like $|x|$ at $x = 0$) and vertical tangents are continuous but **not** differentiable.

## Remember

> Average slope over $[x, x+h]$ becomes **instantaneous slope** when $h \to 0$.

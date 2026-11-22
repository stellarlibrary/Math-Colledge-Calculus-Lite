# ✖️ Product Rule

*How to differentiate two multiplied functions when both factors are changing at the same time.*

## Core Formula

$$
\frac{d}{dx}\big[f(x)\,g(x)\big] = f'(x)\,g(x) + f(x)\,g'(x)
$$

Compact prime notation:

$$
(fg)' = f'g + fg'
$$

- **$f'(x)\,g(x)$**: rate of change from $f$ while $g$ is held fixed.
- **$f(x)\,g'(x)$**: rate of change from $g$ while $f$ is held fixed.

## What It Means

The derivative of a product is **never** just the product of the derivatives. When two functions $f(x)$ and $g(x)$ are multiplied together, each factor takes a turn being differentiated while the other stays unchanged, and then you add the two results together.

## Intuition

Picture a rectangle whose width is $f(x)$ and height is $g(x)$, so its area is $A = f(x)\,g(x)$. When $x$ increases slightly, the rectangle grows in two thin strips:
- A vertical strip of width $df$ and height $g$ $\implies f'g$
- A horizontal strip of width $f$ and height $dg$ $\implies fg'$

The tiny corner where both strips overlap ($df \cdot dg$) vanishes in the limit, leaving $f'g + fg'$.

## Example

**Problem:** Find $h'(x)$ for $h(x) = x^2 e^x$.

Identify $f(x) = x^2$ (so $f'(x) = 2x$) and $g(x) = e^x$ (so $g'(x) = e^x$):

$$
h'(x) = \underbrace{(2x)}_{f'}\underbrace{(e^x)}_{g} + \underbrace{(x^2)}_{f}\underbrace{(e^x)}_{g'} = e^x(2x + x^2)
$$

## Common Mistakes

- **Writing $(fg)' = f'\cdot g'$**: multiplying the derivatives directly is the #1 derivative trap—always form the two-term sum $f'g + fg'$.
- **Using the Product Rule on a constant multiple**: for $5\sin x$, $5$ is a constant, so just pull it out: $(5\sin x)' = 5\cos x$ (no Product Rule needed).

## Remember

> **First times derivative of second, plus second times derivative of first**: $(fg)' = f'g + fg'$.

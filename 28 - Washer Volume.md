# 🍩 Washer Method (Volume)

*Find the volume of a hollow solid of revolution by subtracting the inner hole disk from the outer disk.*

## Core Formula

$$
V = \int_a^b \pi\Big(\big[R(x)\big]^2 - \big[r(x)\big]^2\Big)\,dx
$$

- **$R(x)$ (Outer Radius)**: distance from the axis of rotation to the **farther** boundary curve.
- **$r(x)$ (Inner Radius)**: distance from the axis of rotation to the **closer** boundary curve.
- **$\pi(R^2 - r^2)$**: area of the flat washer (outer circle area $\pi R^2$ minus inner hole area $\pi r^2$).

## What It Means

The **Washer Method** is simply the Disk Method with a hole punched out of the middle. Whenever there is empty space between the region being revolved and the axis of rotation, slicing **perpendicular ($\perp$)** to the axis produces flat rings (washers) instead of solid disks.

## Intuition

Think of a metal hardware washer or a flattened donut: to get the area of the ring, you compute the area of the big circle ($\pi R^2$) and subtract the area of the empty inner hole ($\pi r^2$), then multiply by thickness $dx$.

## Example

**Problem:** Find the volume formed by revolving the region bounded by $y = x$ and $y = x^2$ (on $[0, 1]$) about the $x$-axis.

On $[0, 1]$, the line $y = x$ is farther from the $x$-axis than the parabola $y = x^2$:
- Outer radius: $R(x) = x$
- Inner radius: $r(x) = x^2$

$$
V = \int_0^1 \pi\left[(x)^2 - (x^2)^2\right]dx = \pi \int_0^1 \left(x^2 - x^4\right)dx = \pi\left[\frac{x^3}{3} - \frac{x^5}{5}\right]_0^1 = \pi\left(\frac{1}{3} - \frac{1}{5}\right) = \frac{2\pi}{15}
$$

## Common Mistakes

- **Writing $[R(x) - r(x)]^2$ instead of $[R(x)]^2 - [r(x)]^2$**: this is the #1 volume mistake! You must **square each radius separately** before subtracting: $\pi(R^2 - r^2) \neq \pi(R - r)^2$.
- **Measuring $R$ and $r$ from the $x$-axis when rotating around another line $y = k$**: always measure both $R$ and $r$ **from the axis of rotation**.

## Remember

> **Big circle minus little circle**: square each radius **separately**—$\pi\big(R^2 - r^2\big)$, **never** $\pi(R - r)^2$.

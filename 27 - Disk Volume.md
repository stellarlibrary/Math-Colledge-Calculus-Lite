# 💿 Disk Method (Volume)

*Find the volume of a solid of revolution with no hollow gap by slicing perpendicular to the axis into solid coins.*

## Core Formula

- **Revolved about the $x$-axis** (vertical slices of thickness $dx$, radius $R(x)$):

$$
V = \int_a^b \pi \big[R(x)\big]^2\,dx
$$

- **Revolved about the $y$-axis** (horizontal slices of thickness $dy$, radius $R(y)$):

$$
V = \int_c^d \pi \big[R(y)\big]^2\,dy
$$

- **$R$**: distance from the axis of rotation to the curve.
- **$\pi R^2$**: area of one circular cross-section.

## What It Means

Use the **Disk Method** when a region is flush against the axis of rotation (no gap or hole in the middle) and you slice **perpendicular ($\perp$)** to the axis of rotation. Each cross-section is a solid circular disk of volume $dV = (\text{circle area}) \times (\text{thickness}) = \pi R^2\,dx$.

## Intuition

Picture slicing a loaf of bread or a stack of coins:
- Every coin is a flat cylinder with radius $R = f(x)$ and thickness $dx$.
- One coin has volume $\pi R^2\,dx$.
- The integral $\int_a^b \pi [R(x)]^2\,dx$ stacks infinitely many paper-thin coins from $x = a$ to $x = b$.

## Example

**Problem:** Find the volume of the solid formed by revolving the region under $y = \sqrt{x}$ from $x = 0$ to $x = 4$ about the $x$-axis.

Here the region touches the $x$-axis and $R(x) = \sqrt{x}$:

$$
V = \int_0^4 \pi \left(\sqrt{x}\right)^2 dx = \pi \int_0^4 x\,dx = \pi \left[\frac{x^2}{2}\right]_0^4 = \pi\left(\frac{16}{2} - 0\right) = 8\pi
$$

## Common Mistakes

- **Forgetting to square the radius $R(x)$** or **forgetting the factor of $\pi$**: area of a circle is $\pi R^2$, not $R$ or $2\pi R$.
- **Integrating with the wrong variable**: slicing $\perp$ to the $x$-axis requires $dx$; slicing $\perp$ to the $y$-axis requires $dy$ (so solve for $x = R(y)$ first).
- **Shifted axis of rotation**: if revolving around $y = k$, the radius is $R(x) = |f(x) - k|$, not just $f(x)$.

## Remember

> Slice **perpendicular ($\perp$) to the axis** with no gap $\implies$ stack solid coins of volume **$\pi R^2\,dx$**.

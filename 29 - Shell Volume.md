# 🥫 Cylindrical Shell Method (Volume)

*Find the volume of a solid of revolution by slicing parallel to the axis into nested tin cans.*

## Core Formula

- **Revolved about the $y$-axis** (vertical strips of width $dx$, parallel to the $y$-axis):

$$
V = \int_a^b 2\pi x \, f(x)\,dx
$$

- **General form** (for any axis of rotation):

$$
V = \int_a^b 2\pi \cdot (\text{radius}) \cdot (\text{height}) \cdot (\text{thickness})
$$

- **Radius ($r$)**: distance from the axis of rotation to the slice ($r = x$ for the $y$-axis).
- **Height ($h$)**: length of the slice parallel to the axis ($h = f(x)$ or $f_{\text{top}}(x) - f_{\text{bottom}}(x)$).

## What It Means

Instead of slicing perpendicular to the axis (Disks/Washers), the **Shell Method** slices **parallel ($\parallel$)** to the axis of rotation. Rotating a vertical strip of width $dx$ around the $y$-axis sweeps out a thin cylindrical shell (like a soup can with no lid or bottom).

## Intuition

Cut a thin cylindrical tin can down its side and unroll it flat into a rectangular slab:
- **Width** $=$ circumference of the can $= 2\pi r = 2\pi x$
- **Height** $=$ height of the can $= f(x)$
- **Thickness** $=$ wall thickness $= dx$

Multiplying them gives the shell volume $dV = 2\pi x\,f(x)\,dx$. Integrating sums all the nested cans from the center outward, like Russian nesting dolls.

## Example

**Problem:** Revolve the region under $y = e^{-x^2}$ on $[0, 1]$ about the $y$-axis.

Slicing horizontally for washers would require solving $y = e^{-x^2}$ for $x$, which is hard to integrate. Using vertical shells ($r = x$, $h = e^{-x^2}$) makes it a simple $u$-substitution ($u = -x^2$, $du = -2x\,dx$):

$$
V = \int_0^1 2\pi x e^{-x^2}\,dx = \pi \int_0^{-1} e^u (-du) = \pi\Big[-e^{-x^2}\Big]_0^1 = \pi\left(1 - \frac{1}{e}\right)
$$

## Common Mistakes

- **Confusing when to use $dx$ vs. $dy$**:
  - **Disks/Washers ($\perp$ to axis)**: rotate around $x$-axis $\implies dx$; rotate around $y$-axis $\implies dy$.
  - **Shells ($\parallel$ to axis)**: rotate around $y$-axis $\implies dx$; rotate around $x$-axis $\implies dy$.
- **Squaring the radius**: shells use circumference $2\pi r h$, **not** $\pi r^2$.

## Remember

> Slice **parallel ($\parallel$) to the axis** and unroll the can: **$V = \int 2\pi (\text{radius})(\text{height})\,dx$**.

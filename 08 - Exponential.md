# 🚀 Exponential Derivatives

*The natural exponential $e^x$ is the only non-zero function in calculus that is its own derivative.*

## Core Formula

Natural base $e$:

$$
\frac{d}{dx}\left(e^x\right) = e^x, \qquad \frac{d}{dx}\left(e^{g(x)}\right) = e^{g(x)} \cdot g'(x)
$$

General base $a > 0$:

$$
\frac{d}{dx}\left(a^x\right) = a^x \ln a
$$

- **$e \approx 2.71828$**: Euler's number, the unique base where the slope at $x = 0$ is exactly $1$.
- **$\ln a$**: the scaling factor needed when the base is $a$ instead of $e$.

## What It Means

In an exponential function, the **variable $x$ is in the exponent**. For $y = e^x$, the rate of change at any point equals the current value of the function itself. When the exponent is a function $g(x)$, the Chain Rule keeps $e^{g(x)}$ intact and multiplies by $g'(x)$.

## Intuition

Think of compound interest or population growth: the larger a population $e^x$ already is, the faster it grows. At $x = 0$, the height is $e^0 = 1$ and the slope is $1$; at $x = 2$, the height is $e^2$ and the slope is also $e^2$. Height and slope are always identical.

## Example

**Problem:** Differentiate $f(x) = e^{-3x^2} + 2^x$.

Apply the Chain Rule to $e^{-3x^2}$ (with $g(x) = -3x^2$, $g'(x) = -6x$) and the general base formula to $2^x$:

$$
f'(x) = e^{-3x^2} \cdot (-6x) + 2^x \ln 2 = -6x\,e^{-3x^2} + (\ln 2)\,2^x
$$

## Common Mistakes

- **Treating $e^x$ like a power function**: $\frac{d}{dx}(e^x)$ is **not** $x e^{x-1}$. Use the Power Rule for $x^n$ (variable base) and the Exponential Rule for $e^x$ (variable exponent).
- **Differentiating a constant like $e^3$**: $e^3$ has no $x$ in it—it is just a constant number, so $\frac{d}{dx}(e^3) = 0$.
- **Lowering the exponent in the Chain Rule**: $\frac{d}{dx}(e^{4x}) = 4e^{4x}$, **not** $4e^{4x-1}$.

## Remember

> Copy the exponential $e^{g(x)}$ **exact as is**, then multiply by the derivative of the exponent $g'(x)$.

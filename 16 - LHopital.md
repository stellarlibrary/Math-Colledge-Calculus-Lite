# 🏥 L'Hôpital's Rule

*Resolve $0/0$ or $\infty/\infty$ indeterminate limits by comparing the rates of change of the top and bottom.*

## Core Formula

Suppose $\displaystyle\lim_{x \to a} \frac{f(x)}{g(x)}$ produces the indeterminate form $\frac{0}{0}$ or $\frac{\pm\infty}{\pm\infty}$. Then:

$$
\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}
$$

(provided the limit on the right exists or is $\pm\infty$; also valid as $x \to \pm\infty$).

- **$f'(x)$**: derivative of the numerator **by itself**.
- **$g'(x)$**: derivative of the denominator **by itself**.

## What It Means

When both $f(x)$ and $g(x)$ head toward $0$ (or both head toward $\infty$), a tug-of-war ensues. L'Hôpital's Rule resolves this tug-of-war by replacing the ratio of the functions $\frac{f(x)}{g(x)}$ with the **ratio of their derivatives** $\frac{f'(x)}{g'(x)}$. If the new limit is still $\frac{0}{0}$ or $\frac{\infty}{\infty}$, you can apply L'Hôpital's Rule again.

## Intuition

Near $x = a$ where $f(a) = g(a) = 0$, zoom in on both curves until they look like their tangent lines: $f(x) \approx f'(a)(x - a)$ and $g(x) \approx g'(a)(x - a)$. Dividing the two approximations cancels $(x - a)$ and leaves the ratio of their slopes, $\frac{f'(a)}{g'(a)}$.

## Example

**Problem:** Evaluate $\displaystyle\lim_{x \to 0} \frac{e^{2x} - 1 - 2x}{x^2}$.

1. Check form at $x = 0$: $\frac{e^0 - 1 - 0}{0^2} = \frac{0}{0}$ (L'Hôpital applies).
2. Differentiate top and bottom separately:

$$
\lim_{x \to 0} \frac{2e^{2x} - 2}{2x} \quad \left(\text{still } \frac{0}{0}\right) \stackrel{\text{L'H}}{=} \lim_{x \to 0} \frac{4e^{2x}}{2} = \frac{4(1)}{2} = 2
$$

## Common Mistakes

- **Applying L'Hôpital's Rule when the limit is NOT $\frac{0}{0}$ or $\frac{\infty}{\infty}$**: always check the form first! Applying L'Hôpital to $\lim_{x \to 0} \frac{\cos x}{x + 1} = \frac{1}{1} = 1$ gives the wrong answer $0$.
- **Using the Quotient Rule**: differentiate the numerator and denominator **separately** ($\frac{f'}{g'}$), do **not** compute $\left(\frac{f}{g}\right)'$.
- **Other indeterminate forms ($0 \cdot \infty$, $\infty - \infty$, $1^\infty$, $0^0$, $\infty^0$)**: rewrite them as a fraction $\frac{0}{0}$ or $\frac{\infty}{\infty}$ (or take $\ln$) before using L'Hôpital's Rule.

## Remember

> First verify **$\frac{0}{0}$ or $\frac{\infty}{\infty}$**, then take **derivative of top over derivative of bottom** ($\frac{f'}{g'}$, never Quotient Rule).

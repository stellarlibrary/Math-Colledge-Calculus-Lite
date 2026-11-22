# 🔋 Integral Power Rule

*Reversing the Derivative Power Rule: raise the exponent by $1$ and divide by the new exponent.*

## Core Formula

$$
\int x^n\,dx = \frac{x^{n+1}}{n+1} + C, \qquad n \neq -1
$$

The special case when $n = -1$:

$$
\int x^{-1}\,dx = \int \frac{1}{x}\,dx = \ln|x| + C
$$

- **$n$**: any real constant exponent except $-1$.
- **$C$**: the constant of integration (representing the family of all antiderivatives).

## What It Means

Antidifferentiation runs the Power Rule in reverse. Whereas differentiating $x^n$ *multiplies* by the old power and *subtracts $1$*, integrating $x^n$ **adds $1$ to the power** first and then **divides by the new power** $n + 1$.

## Intuition

Check by differentiating the result: $\frac{d}{dx}\left[\frac{x^{n+1}}{n+1} + C\right] = \frac{(n+1)x^n}{n+1} + 0 = x^n$. The factor $\frac{1}{n+1}$ is placed in front specifically to cancel the $n+1$ that drops down when you take the derivative, and $+C$ accounts for any vertical shift (whose derivative is $0$).

## Example

**Problem:** Evaluate $\displaystyle\int \left(6x^2 - \frac{3}{\sqrt{x}} + \frac{2}{x}\right)dx$.

Rewrite as powers of $x$ first: $\int \left(6x^2 - 3x^{-1/2} + 2\cdot\frac{1}{x}\right)dx$.

$$
= 6\cdot\frac{x^3}{3} - 3\cdot\frac{x^{1/2}}{1/2} + 2\ln|x| + C = 2x^3 - 6\sqrt{x} + 2\ln|x| + C
$$

## Common Mistakes

- **Using the power rule when $n = -1$**: plugging $n = -1$ into $\frac{x^{n+1}}{n+1}$ gives $\frac{x^0}{0}$ (division by zero!). Always integrate $\frac{1}{x}$ as $\ln|x| + C$.
- **Forgetting $+C$ on indefinite integrals**: without bounds, an integral represents an entire family of curves, so $+C$ is mandatory.
- **Integrating a fraction by integrating top and bottom separately**: rewrite $\frac{x^3 + 1}{x^2}$ by splitting into $x + x^{-2}$ first.

## Remember

> **Add $1$ to the exponent, divide by the new exponent, and never forget $+C$** (unless $n = -1 \implies \ln|x| + C$).

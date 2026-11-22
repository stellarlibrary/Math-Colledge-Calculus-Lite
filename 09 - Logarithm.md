# 🪵 Logarithmic Derivatives

*Differentiating $\ln x$ turns a logarithm into a simple reciprocal—and log properties make hard derivatives easy.*

## Core Formula

Natural logarithm ($x > 0$):

$$
\frac{d}{dx}(\ln x) = \frac{1}{x}, \qquad \frac{d}{dx}\big(\ln|g(x)|\big) = \frac{g'(x)}{g(x)}
$$

General base $a > 0, a \neq 1$:

$$
\frac{d}{dx}(\log_a x) = \frac{1}{x \ln a}
$$

- **$\frac{g'(x)}{g(x)}$**: "derivative of the inside over the inside" (the logarithmic derivative).

## What It Means

The derivative of $\ln x$ is $\frac{1}{x}$. When differentiating $\ln(g(x))$, the Chain Rule gives $\frac{1}{g(x)} \cdot g'(x) = \frac{g'(x)}{g(x)}$. Even better, you can use **log laws** ($\ln(AB) = \ln A + \ln B$, $\ln(A/B) = \ln A - \ln B$, $\ln(A^k) = k\ln A$) *before* differentiating to avoid messy Product, Quotient, or Chain Rules.

## Intuition

As $x$ grows larger, $\ln x$ still increases, but more and more slowly. Its slope $\frac{1}{x}$ reflects this: steep near $x = 0^+$ (for instance, slope $10$ at $x = 0.1$) and nearly flat for large $x$ (slope $0.01$ at $x = 100$).

## Example

**Problem:** Find $\frac{d}{dx} \ln\left(\frac{x^4}{\sin x}\right)$ for $x \in (0, \pi)$.

First expand using logarithm properties, then differentiate term by term:

$$
\ln\left(\frac{x^4}{\sin x}\right) = 4\ln x - \ln(\sin x)
$$

$$
\frac{d}{dx}\big[4\ln x - \ln(\sin x)\big] = \frac{4}{x} - \frac{\cos x}{\sin x} = \frac{4}{x} - \cot x
$$

## Common Mistakes

- **Forgetting the Chain Rule on $\ln(g(x))$**: $\frac{d}{dx}[\ln(x^2 + 1)] = \frac{2x}{x^2 + 1}$, **not** $\frac{1}{x^2 + 1}$.
- **Confusing $\ln(A + B)$ with $\ln A + \ln B$**: logarithms split products and quotients, **never** sums! $\ln(x^2 + 1)$ cannot be simplified.
- **Missing the $\ln a$ factor for base $a$**: $\frac{d}{dx}(\log_{10} x) = \frac{1}{x \ln 10}$, not $\frac{1}{x}$.

## Remember

> For $\ln(\text{inside})$, the derivative is simply **$\dfrac{\text{derivative of inside}}{\text{inside}}$**: $\dfrac{g'(x)}{g(x)}$.

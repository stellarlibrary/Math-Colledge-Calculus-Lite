# 🌐 Maclaurin Series

*A Taylor series centered at $a = 0$—giving the four essential power series expansions every calculus student should know.*

## Core Formula

$$
f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + \frac{f'''(0)}{3!}x^3 + \cdots
$$

**The Big Four Maclaurin Series to Memorize:**

$$
\begin{aligned}
\frac{1}{1 - x} &= \sum_{n=0}^{\infty} x^n = 1 + x + x^2 + x^3 + \cdots && (|x| < 1) \\
e^x &= \sum_{n=0}^{\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots && (\text{all } x) \\
\sin x &= \sum_{n=0}^{\infty} (-1)^n\frac{x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots && (\text{all } x) \\
\cos x &= \sum_{n=0}^{\infty} (-1)^n\frac{x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots && (\text{all } x)
\end{aligned}
$$

## What It Means

A Maclaurin series is simply a Taylor series with center $a = 0$. Rather than taking derivatives from scratch every time, you can build new Maclaurin series almost instantly by **substituting, multiplying, differentiating, or integrating** the Big Four series above.

## Intuition

Notice the symmetry:
- **$\sin x$ is an odd function** ($\sin(-x) = -\sin x$), so its Maclaurin series has only **odd powers** ($x, x^3, x^5, \dots$) with alternating signs.
- **$\cos x$ is an even function** ($\cos(-x) = \cos x$), so its Maclaurin series has only **even powers** ($1, x^2, x^4, \dots$) with alternating signs—and differentiating the series for $\sin x$ term-by-term gives the series for $\cos x$!

## Example

**Problem:** Find the Maclaurin series for $f(x) = x\cos(x^2)$.

Replace $x$ with $x^2$ in the known Maclaurin series for $\cos x$, then multiply by $x$:

$$
\cos(x^2) = 1 - \frac{(x^2)^2}{2!} + \frac{(x^2)^4}{4!} - \cdots = 1 - \frac{x^4}{2!} + \frac{x^8}{4!} - \cdots
$$

$$
x\cos(x^2) = x - \frac{x^5}{2!} + \frac{x^9}{4!} - \cdots = \sum_{n=0}^{\infty} (-1)^n \frac{x^{4n+1}}{(2n)!}
$$

## Common Mistakes

- **Differentiating $x\cos(x^2)$ repeatedly at $x = 0$**: never take higher derivatives when you can substitute $x^2$ into a known Maclaurin series in two lines!
- **Mixing up $\sin x$ and $\cos x$**: remember $\sin(0) = 0$ (starts with $x$, odd powers) and $\cos(0) = 1$ (starts with $1$, even powers).

## Remember

> Maclaurin $=$ **Taylor centered at $0$**; memorize $\frac{1}{1-x}, e^x, \sin x, \cos x$ and substitute to build the rest.

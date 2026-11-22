# 🥣 Concavity

*How a graph bends: curving upward like a cup ($f'' > 0$) or downward like a cap ($f'' < 0$).*

## Core Formula

On an open interval $I$:

$$
\begin{aligned}
f''(x) > 0 \quad &\implies \quad f \text{ is \textbf{Concave Up} } (\cup) \text{ on } I \\
f''(x) < 0 \quad &\implies \quad f \text{ is \textbf{Concave Down} } (\cap) \text{ on } I
\end{aligned}
$$

- **Concave Up ($\cup$)**: the slope $f'(x)$ is **increasing**; the graph lies **above** its tangent lines.
- **Concave Down ($\cap$)**: the slope $f'(x)$ is **decreasing**; the graph lies **below** its tangent lines.

## What It Means

Concavity describes the **bending direction** of a curve, independent of whether the function is going uphill or downhill. For instance, $f(x) = e^{-x}$ is decreasing everywhere ($f' < 0$), yet it is concave up everywhere ($f'' > 0$) because its downward slope is flattening out.

## Intuition

Use the **Cup and Tangent Rule**:
- **Concave Up ($f'' > 0$)**: shaped like a upright bowl $\cup$ that **holds water**. Tangent lines sit *underneath* the curve, so linear approximations **underestimate** $f(x)$.
- **Concave Down ($f'' < 0$)**: shaped like an umbrella $\cap$ that **spills water**. Tangent lines sit *on top of* the curve, so linear approximations **overestimate** $f(x)$.

## Example

**Problem:** Find the intervals of concavity for $f(x) = x^3 - 6x^2 + 9x + 1$.

Compute the first and second derivatives:

$$
f'(x) = 3x^2 - 12x + 9, \qquad f''(x) = 6x - 12 = 6(x - 2)
$$

Set $f''(x) = 0 \implies x = 2$:
- For $x < 2$: $f''(x) < 0 \implies$ **Concave Down** on $(-\infty, 2)$.
- For $x > 2$: $f''(x) > 0 \implies$ **Concave Up** on $(2, \infty)$.

## Common Mistakes

- **Confusing "increasing" ($f' > 0$) with "concave up" ($f'' > 0$)**: a function can be decreasing and concave up at the same time (like the left half of $y = x^2$).
- **Plugging test points into $f(x)$ or $f'(x)$ instead of $f''(x)$**: when testing concavity intervals, always evaluate the sign of **$f''(x)$**.

## Remember

> **$f'' > 0$ holds water ($\cup$, tangent below)**; **$f'' < 0$ spills water ($\cap$, tangent above)**.

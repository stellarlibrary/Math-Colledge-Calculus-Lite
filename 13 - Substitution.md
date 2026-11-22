# 🔄 Substitution Rule ($u$-Substitution)

*The reverse of the Chain Rule: simplify a composite integral by replacing the inside function with $u$.*

## Core Formula

Indefinite integral:

$$
\int f(g(x))\,g'(x)\,dx = \int f(u)\,du = F(u) + C = F(g(x)) + C
$$

Definite integral (changing bounds to $u$):

$$
\int_a^b f(g(x))\,g'(x)\,dx = \int_{g(a)}^{g(b)} f(u)\,du
$$

- **$u = g(x)$**: the inner function chosen to simplify the integrand.
- **$du = g'(x)\,dx$**: the differential linking $dx$ to $du$.

## What It Means

Use $u$-substitution when an integral contains **both an inner function $g(x)$ and a constant multiple of its derivative $g'(x)$**. By setting $u = g(x)$ and $du = g'(x)\,dx$, you absorb the complicated inner expression and its derivative into a clean integral in terms of $u$.

## Intuition

When the Chain Rule differentiates $F(g(x))$, it spits out an extra factor of $g'(x)$ on the outside: $F'(g(x))\cdot g'(x)$. $u$-substitution spots that extra $g'(x)\,dx$ sitting in the integral and folds it back into $du$, undoing the Chain Rule in one step.

## Example

**Problem:** Evaluate $\displaystyle\int_0^2 x e^{x^2}\,dx$.

Let $u = x^2$. Then $du = 2x\,dx \implies x\,dx = \frac{1}{2}\,du$.
Update the bounds: when $x = 0 \implies u = 0$; when $x = 2 \implies u = 2^2 = 4$.

$$
\int_0^2 x e^{x^2}\,dx = \frac{1}{2}\int_0^4 e^u\,du = \frac{1}{2}\Big[e^u\Big]_0^4 = \frac{1}{2}(e^4 - e^0) = \frac{e^4 - 1}{2}
$$

## Common Mistakes

- **Leaving mixed $x$ and $u$ variables**: every $x$ and $dx$ must be converted to $u$ and $du$ before integrating.
- **Plugging $x$-bounds into the $u$-antiderivative**: for definite integrals, either convert the bounds to $u = g(a), g(b)$ right away, or switch back to $x$ before plugging in $a$ and $b$.
- **Forgetting to back-substitute $u = g(x)$** at the end of an indefinite integral.

## Remember

> Pick **$u = \text{inside function}$** whose derivative $du = g'(x)\,dx$ is already waiting in the integral.

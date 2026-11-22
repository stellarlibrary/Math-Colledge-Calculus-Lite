# 🧩 Integration by Parts

*The reverse of the Product Rule: trade a hard product integral $\int u\,dv$ for an easier one $\int v\,du$.*

## Core Formula

$$
\int u\,dv = u v - \int v\,du
$$

For definite integrals:

$$
\int_a^b u\,dv = \Big[u v\Big]_a^b - \int_a^b v\,du
$$

- **$u$**: factor you choose to **differentiate** ($u \to du$), chosen so $du$ becomes simpler.
- **$dv$**: factor you choose to **integrate** ($dv \to v$), chosen so it is easy to antidifferentiate.

## What It Means

When an integral is a product of two unrelated function types (such as $x e^x$, $x \sin x$, or $\ln x$) and $u$-substitution does not work, Integration by Parts lets you differentiate one part ($u$) while integrating the other ($dv$).

## Intuition

Start from the Product Rule: $(uv)' = u'v + uv'$. Integrate both sides: $uv = \int v\,du + \int u\,dv$, and rearrange to get $\int u\,dv = uv - \int v\,du$.
To choose $u$, follow the **LIATE priority** (pick whichever appears first as $u$):
1. **L**ogarithmic ($\ln x$)
2. **I**nverse trig ($\arctan x, \arcsin x$)
3. **A**lgebraic ($x^2, 3x$)
4. **T**rigonometric ($\sin x, \cos x$)
5. **E**xponential ($e^x, 2^x$)

## Example

**Problem:** Evaluate $\displaystyle\int x e^x\,dx$.

By LIATE, Algebraic ($x$) comes before Exponential ($e^x$):
- Let $u = x \implies du = dx$
- Let $dv = e^x\,dx \implies v = e^x$

$$
\int x e^x\,dx = x e^x - \int e^x\,dx = x e^x - e^x + C = e^x(x - 1) + C
$$

## Common Mistakes

- **Picking $u$ and $dv$ backwards**: if you set $u = e^x$ and $dv = x\,dx$ in $\int x e^x\,dx$, you get $\int \frac{1}{2}x^2 e^x\,dx$, which is *worse* than what you started with.
- **Sign errors when repeating by parts**: wrap the second $\int v\,du$ in brackets so the minus sign distributes properly.
- **Overlooking $\int \ln x\,dx$**: write it as $\int (\ln x)\cdot 1\,dx$ with $u = \ln x$ and $dv = 1\,dx$, giving $x\ln x - x + C$.

## Remember

> Use **LIATE** to pick $u$ (gets simpler when differentiated) and apply **$\int u\,dv = uv - \int v\,du$**.

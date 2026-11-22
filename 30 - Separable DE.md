# 🧪 Separable Differential Equations

*Solve a first-order differential equation by moving all $y$'s to one side, all $x$'s to the other, and integrating.*

## Core Formula

If a differential equation can be factored as a product of a function of $x$ and a function of $y$:

$$
\frac{dy}{dx} = g(x)\,h(y)
$$

Separate variables (for $h(y) \neq 0$) and integrate both sides:

$$
\int \frac{1}{h(y)}\,dy = \int g(x)\,dx + C
$$

- **General Solution**: the family of solutions containing the arbitrary constant $C$.
- **Particular Solution**: the specific function found by plugging in an initial condition $y(x_0) = y_0$ to solve for $C$.

## What It Means

A differential equation relates an unknown function $y(x)$ to its derivative $\frac{dy}{dx}$. It is **separable** if you can use multiplication and division to isolate every $y$ with $dy$ on the left and every $x$ with $dx$ on the right. Once separated, antidifferentiating both sides recovers the function $y(x)$.

## Intuition

Although $\frac{dy}{dx}$ is a limit of a ratio, the Chain Rule guarantees that treating $dy$ and $dx$ as separate differentials works: since $\int \frac{1}{h(y)}\frac{dy}{dx}\,dx = \int \frac{1}{h(y)}\,dy$, splitting $\frac{dy}{dx}$ across the equals sign is a valid shortcut for reverse-Chain-Rule integration.

## Example

**Problem:** Solve the initial value problem $\dfrac{dy}{dx} = 2xy^2$ with $y(0) = 1$.

1. **Separate** variables (divide by $y^2$, multiply by $dx$):

$$
y^{-2}\,dy = 2x\,dx
$$

2. **Integrate** both sides:

$$
\int y^{-2}\,dy = \int 2x\,dx \implies -\frac{1}{y} = x^2 + C
$$

3. **Apply initial condition** $y(0) = 1$: $-\frac{1}{1} = 0^2 + C \implies C = -1$.
4. **Solve for $y$**: $-\frac{1}{y} = x^2 - 1 \implies y(x) = \frac{1}{1 - x^2}$.

## Common Mistakes

- **Separating by addition or subtraction**: $\frac{dy}{dx} = x + y$ is **not** separable! You can only move $y$ across via multiplication or division.
- **Tacking $+C$ on after solving for $y$**: add $+C$ **immediately** after integrating—for instance, $\ln|y| = x + C$ gives $y = Ae^x$, **not** $y = e^x + C$.
- **Forgetting constant (equilibrium) solutions**: if $h(y_0) = 0$, dividing by $h(y)$ can lose the constant solution $y = y_0$.

## Remember

> **1. Separate** ($\frac{dy}{h(y)} = g(x)\,dx$) $\to$ **2. Integrate** (add $+C$ right away!) $\to$ **3. Plug in $y(x_0) = y_0$ & solve for $y$**.

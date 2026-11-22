# ➗ Quotient Rule

*How to differentiate a fraction of two functions—where numerator growth helps and denominator growth opposes.*

## Core Formula

$$
\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right] = \frac{f'(x)\,g(x) - f(x)\,g'(x)}{\big[g(x)\big]^2}, \qquad g(x) \neq 0
$$

Compact prime notation:

$$
\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}
$$

- **$f(x)$ ("High")**: numerator function.
- **$g(x)$ ("Low")**: denominator function.

## What It Means

To differentiate a ratio $\frac{f(x)}{g(x)}$, take the derivative of the top times the bottom, **subtract** the top times the derivative of the bottom, and divide the entire expression by the **bottom squared**. Unlike the Product Rule, subtraction means the **order of terms in the numerator strictly matters**.

## Intuition

Think about what changes the size of a fraction $\frac{f}{g}$:
- If the numerator $f$ grows ($f' > 0$), the fraction gets **bigger** $\implies +f'g$.
- If the denominator $g$ grows ($g' > 0$), the fraction gets **smaller** $\implies -fg'$.
- Dividing by $g^2$ properly scales both effects.

## Example

**Problem:** Differentiate $y = \frac{3x - 1}{x^2 + 1}$.

Let $f(x) = 3x - 1$ ($f'(x) = 3$) and $g(x) = x^2 + 1$ ($g'(x) = 2x$):

$$
y' = \frac{(3)(x^2 + 1) - (3x - 1)(2x)}{(x^2 + 1)^2} = \frac{3x^2 + 3 - 6x^2 + 2x}{(x^2 + 1)^2} = \frac{-3x^2 + 2x + 3}{(x^2 + 1)^2}
$$

## Common Mistakes

- **Reversing the subtraction order**: writing $fg' - f'g$ flips the sign of your entire answer. Differentiate the **top** first!
- **Canceling $g(x)$ prematurely** or expanding $(g(x))^2$ unnecessarily—usually it is best to leave the denominator factored as $[g(x)]^2$.
- **Overusing the Quotient Rule**: if the numerator is a constant, like $\frac{4}{x^3}$, rewrite it as $4x^{-3}$ and use the simpler Power Rule.

## Remember

> *"Low d-High minus High d-Low, over the square of what's below"*: $\dfrac{g f' - f g'}{g^2}$.

# 🎯 Limit Definition

*Where a function is heading as the input gets arbitrarily close to a point.*

## Core Formula

$$
\lim_{x \to a} f(x) = L
$$

- **$x \to a$**: the input $x$ approaches $a$ from both the left ($x < a$) and the right ($x > a$), without necessarily equaling $a$.
- **$L$**: the single finite number that the output $f(x)$ gets closer and closer to.

## What It Means

A limit describes the **nearby behavior** of a function around $x = a$, not what happens at $x = a$ itself. Even if $f(a)$ is undefined (a hole in the graph) or defined to be a completely different value, the limit $L$ still exists as long as the left-hand limit and right-hand limit agree:

$$
\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = L
$$

## Intuition

Imagine two friends walking along the graph toward $x = a$, one from the left and one from the right. If both friends point to the same height $L$ as they close in on $x = a$, then the limit is $L$—even if the bridge is missing a plank right at $x = a$.

## Example

**Problem:** Evaluate $\displaystyle\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$.

Direct substitution gives $\frac{0}{0}$ (undefined at $x = 2$). Factoring reveals the nearby behavior for $x \neq 2$:

$$
\lim_{x \to 2} \frac{(x - 2)(x + 2)}{x - 2} = \lim_{x \to 2} (x + 2) = 2 + 2 = 4
$$

## Common Mistakes

- **Confusing $\lim_{x \to a} f(x)$ with $f(a)$**: a limit can exist even when $f(a)$ is undefined.
- **Stopping at $\frac{0}{0}$**: getting $\frac{0}{0}$ means "keep simplifying" (factor, rationalize, or use common denominators), not "limit does not exist."
- **Only checking one side**: if $\lim_{x \to a^-} f(x) \neq \lim_{x \to a^+} f(x)$, the two-sided limit does not exist (DNE).

## Remember

> A limit cares about the **journey** toward $x = a$, never the destination at $x = a$.

# College Calculus Lite Cards — Requirements Document

## 1. Project Overview

This repository provides a **30-card Lite knowledge deck** for college-level Calculus I and Calculus II students.

Unlike full textbook notes, **Lite cards** are built for fast, one-screen mobile review and intuitive understanding. Every card replaces generic boilerplate with clear explanations, properly rendered LaTeX formulas, concrete visual/geometric intuition, a worked step-by-step example, common student pitfalls, and a memorable one-line takeaway.

---

## 2. Target Audience & Learning Goals

### Primary Audience
College students taking Calculus I and Calculus II who want a rapid, high-clarity reference to grasp and retain the 30 most essential formulas and theorems.

### Learning Goals
1. **Grasp the core formula immediately** with clean, properly rendered Markdown LaTeX (`$...$` and `$$...$$`) and symbol breakdowns.
2. **Understand what the concept actually means** in plain, student-friendly English before getting lost in notation.
3. **Build geometric or physical intuition** so formulas make sense rather than feeling like arbitrary rules to memorize.
4. **Follow a concrete worked example** showing exactly how the rule or theorem works in practice.
5. **Avoid common pitfalls** by highlighting the specific mistakes students make on homework and exams.
6. **Retain a quick memory hook** for instant recall.

---

## 3. Card Design & Formatting Standards

### 3.1 Clean Section Headings (No Redundant Section Emojis)
- **Do not** clutter every section header (`## Core Formula`, `## What It Means`, etc.) with the same repeated emojis (`📌`, `🧠`, `💡`, `🔍`, `⚠️`) across all 30 cards.
- Instead, give **each card its own topic-relevant emoji in the `#` title** (e.g., `# 🎯 Limit Definition`, `# ⛓️ Chain Rule`, `# 💿 Disk Volume`) to give each concept a distinct visual identity, while keeping `##` section headings clean and distraction-free.

### 3.2 Standard Card Structure
Every card follows a consistent, scannable layout:

```markdown
# <Topic Emoji> <Card Title>

*<One-line subtitle summarizing the card's role in calculus>*

## Core Formula

$$
<Main LaTeX Formula>
$$

- **<Symbol / Term 1>**: plain-English meaning
- **<Symbol / Term 2>**: plain-English meaning

## What It Means

Clear, plain-English explanation of the concept, when it applies, and why it matters.

## Intuition

Visual, geometric, or physical mental model that makes the formula click.

## Example

**Problem:** <Concrete calculus problem>

$$
<Step-by-step worked solution>
$$

## Common Mistakes

- **<Mistake 1>**: why it happens and how to avoid it.
- **<Mistake 2>**: why it happens and how to avoid it.

## Remember

> <One short, memorable takeaway sentence or mnemonic.>
```

### 3.3 Equation Formatting Rules
- Use standard GitHub-compatible Markdown LaTeX:
  - Inline math: `$...$`
  - Display math: `$$...$$`
- Do **not** use ```latex code blocks (which render as raw source code instead of formatted math on GitHub and Markdown viewers).
- Always include differentials (`\,dx`, `\,dt`, `\,du`), proper fractions (`\frac{a}{b}`), limits (`\lim_{x \to a}`), and explicit conditions (such as $n \neq -1$ or continuity/differentiability requirements).

### 3.4 Length & Tone
- **Length**: ~250–450 words per card — concise enough to read on a phone screen in 1–2 minutes, yet complete enough for genuine conceptual understanding.
- **Tone**: Clear, direct, encouraging, and student-centered. Explain the idea in plain language alongside the math.

---

## 4. Scope of the 30 Lite Cards

### Part I: Limits & Continuity
| # | File | Topic | Concept Emoji |
|---|------|-------|---------------|
| 01 | `01 - Limit Definition.md` | Approaching a value near a point | 🎯 |
| 02 | `02 - Continuity.md` | Unbroken graphs and the three continuity conditions | 🔗 |

### Part II: Derivatives & Differentiation Rules
| # | File | Topic | Concept Emoji |
|---|------|-------|---------------|
| 03 | `03 - Derivative Definition.md` | Instantaneous rate of change via limit of secant slopes | 📈 |
| 04 | `04 - Power Rule.md` | Differentiating $x^n$ for any real exponent | ⚡ |
| 05 | `05 - Product Rule.md` | Differentiating a product of two functions | ✖️ |
| 06 | `06 - Quotient Rule.md` | Differentiating a ratio of two functions | ➗ |
| 07 | `07 - Chain Rule.md` | Differentiating composite (nested) functions | ⛓️ |
| 08 | `08 - Exponential.md` | Derivatives of $e^x$ and general base $a^x$ | 🚀 |
| 09 | `09 - Logarithm.md` | Derivatives of $\ln x$ and $\log_a x$ | 🪵 |

### Part III: Integration & Core Theorems
| # | File | Topic | Concept Emoji |
|---|------|-------|---------------|
| 10 | `10 - FTC.md` | Fundamental Theorem of Calculus (Part 1: Derivative of an integral) | 🌉 |
| 11 | `11 - Integral Power.md` | Antiderivative power rule and the $n = -1$ exception | 🔋 |
| 12 | `12 - Definite Integral.md` | Net signed area and FTC Part 2 evaluation $F(b) - F(a)$ | 📊 |
| 13 | `13 - Substitution.md` | $u$-substitution (reversing the Chain Rule) | 🔄 |
| 14 | `14 - Integration by Parts.md` | Reversing the Product Rule ($\int u\,dv = uv - \int v\,du$) | 🧩 |

### Part IV: Mean Value Theorem, Indeterminate Forms & Series
| # | File | Topic | Concept Emoji |
|---|------|-------|---------------|
| 15 | `15 - MVT.md` | Mean Value Theorem (instantaneous slope matches average slope) | ⚖️ |
| 16 | `16 - LHopital.md` | L'Hôpital's Rule for $0/0$ and $\infty/\infty$ indeterminate forms | 🏥 |
| 17 | `17 - Taylor Series.md` | Infinite polynomial expansion centered at $x = a$ | 🔭 |
| 18 | `18 - Maclaurin.md` | Taylor series centered at $x = 0$ and classic expansions | 🌐 |
| 19 | `19 - Ratio Test.md` | Testing series convergence via the ratio $\lvert a_{n+1}/a_n \rvert$ | 📏 |
| 20 | `20 - Improper Integral.md` | Infinite bounds, discontinuities, and the $p$-integral test | ♾️ |

### Part V: Curve Analysis & Optimization
| # | File | Topic | Concept Emoji |
|---|------|-------|---------------|
| 21 | `21 - Critical Points.md` | Finding where $f'(c) = 0$ or $f'(c)$ is undefined | 📍 |
| 22 | `22 - Second Derivative.md` | Acceleration of a function and the Second Derivative Test | 🎢 |
| 23 | `23 - Concavity.md` | Concave up ($f'' > 0$) vs. concave down ($f'' < 0$) | 🥣 |
| 24 | `24 - Inflection.md` | Points where concavity changes sign | 🔀 |

### Part VI: Geometric Applications & Differential Equations
| # | File | Topic | Concept Emoji |
|---|------|-------|---------------|
| 25 | `25 - Arc Length.md` | Measuring distance along a smooth curve | 🧵 |
| 26 | `26 - Surface Area.md` | Area of a surface formed by revolving a curve | 🏺 |
| 27 | `27 - Disk Volume.md` | Solid of revolution with solid circular cross-sections | 💿 |
| 28 | `28 - Washer Volume.md` | Solid of revolution with hollow ring cross-sections | 🍩 |
| 29 | `29 - Shell Volume.md` | Volume by nested cylindrical shells | 🥫 |
| 30 | `30 - Separable DE.md` | Solving first-order differential equations by separating variables | 🧪 |

---

## 5. Quality Checklist

Before a card is considered complete, verify that:
- [ ] It contains **no generic placeholder text** (such as *"Key calculus concept frequently tested"* or *"Typical exam-style application"*).
- [ ] All math is rendered with `$...$` or `$$...$$` rather than fenced code blocks.
- [ ] Conditions and hypotheses (e.g., continuity on $[a,b]$, $n \neq -1$, indeterminate forms) are explicitly stated.
- [ ] The example is fully worked out with concrete numbers and functions.
- [ ] The common mistakes reflect real student errors specific to that topic.

# 04. Differential Calculus

Comprehensive guide to differential calculus: difference quotients, differentiation rules, standard derivatives table, tangent/normal lines, fundamental theorems, curve sketching (extrema, concavity, inflection), asymptotic equivalences, orders of infinitesimals/infinites, little-o algebra, and Taylor/Maclaurin series expansions.

---

## Table of Contents

1. [Difference Quotient and Definition of Derivative](#1-difference-quotient-and-definition-of-derivative)
2. [Tangent and Normal Lines](#2-tangent-and-normal-lines)
3. [Table of Standard Derivatives](#3-table-of-standard-derivatives)
4. [Differentiation Rules and Algebra](#4-differentiation-rules-and-algebra)
5. [Derivative of Inverse Functions](#5-derivative-of-inverse-functions)
6. [Fundamental Differential Theorems](#6-fundamental-differential-theorems)
7. [Monotonicity, Extrema, and Fermat's Theorem](#7-monotonicity-extrema-and-fermats-theorem)
8. [Concavity, Convexity, and Inflection Points](#8-concavity-convexity-and-inflection-points)
9. [Asymptotic Equivalences, Infinitesimals, and Little-o Algebra](#9-asymptotic-equivalences-infinitesimals-and-little-o-algebra)
10. [Taylor and Maclaurin Expansions](#10-taylor-and-maclaurin-expansions)

---

## 1. Difference Quotient and Definition of Derivative

Let $f: (a, b) \to \mathbb{R}$ and $x_0 \in (a, b)$.

### 1.1 Difference Quotient (Rapporto Incrementale)
For an increment $h \neq 0$ such that $x_0 + h \in (a, b)$:

$$\frac{\Delta f}{\Delta x} = \frac{f(x_0 + h) - f(x_0)}{h}$$

### 1.2 Definition of Derivative
The derivative $f'(x_0)$ is the limit of the difference quotient as $h \to 0$:

$$f'(x_0) = \lim_{h \to 0} \frac{f(x_0 + h) - f(x_0)}{h} = \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0}$$

* **Geometric Meaning:** $f'(x_0)$ is the angular coefficient (slope $m$) of the tangent line to the curve at $(x_0, f(x_0))$.
* **Differentiability $\implies$ Continuity:** If $f$ is differentiable at $x_0$, then $f$ is continuous at $x_0$.

---

## 2. Tangent and Normal Lines

Let $f$ be differentiable at $x_0$:

### 2.1 Tangent Line (Retta Tangente)

$$y - f(x_0) = f'(x_0)(x - x_0) \implies y = f'(x_0)(x - x_0) + f(x_0)$$

### 2.2 Normal Line (Retta Normale)
The normal line is perpendicular to the tangent line at $(x_0, f(x_0))$ (provided $f'(x_0) \neq 0$):

$$y - f(x_0) = -\frac{1}{f'(x_0)}(x - x_0)$$

---

## 3. Table of Standard Derivatives

| Function $f(x)$ | Derivative $f'(x)$ | Domain / Conditions |
| :--- | :--- | :--- |
| $c$ (constant) | $0$ | $x \in \mathbb{R}$ |
| $x^\alpha$ | $\alpha x^{\alpha - 1}$ | $\alpha \in \mathbb{R}, x > 0$ |
| $\sqrt{x}$ | $\frac{1}{2\sqrt{x}}$ | $x > 0$ |
| $e^x$ | $e^x$ | $x \in \mathbb{R}$ |
| $a^x$ | $a^x \ln(a)$ | $a > 0, a \neq 1$ |
| $\ln(x)$ | $\frac{1}{x}$ | $x > 0$ |
| $\log_a(x)$ | $\frac{1}{x \ln(a)}$ | $x > 0, a > 0, a \neq 1$ |
| $\sin(x)$ | $\cos(x)$ | $x \in \mathbb{R}$ |
| $\cos(x)$ | $-\sin(x)$ | $x \in \mathbb{R}$ |
| $\tan(x)$ | $1 + \tan^2(x) = \frac{1}{\cos^2(x)}$ | $x \neq \frac{\pi}{2} + k\pi$ |
| $\cot(x)$ | $-(1 + \cot^2(x)) = -\frac{1}{\sin^2(x)}$ | $x \neq k\pi$ |
| $\arcsin(x)$ | $\frac{1}{\sqrt{1 - x^2}}$ | $x \in (-1, 1)$ |
| $\arccos(x)$ | $-\frac{1}{\sqrt{1 - x^2}}$ | $x \in (-1, 1)$ |
| $\arctan(x)$ | $\frac{1}{1 + x^2}$ | $x \in \mathbb{R}$ |
| $\text{arccot}(x)$ | $-\frac{1}{1 + x^2}$ | $x \in \mathbb{R}$ |

---

## 4. Differentiation Rules and Algebra

Let $f, g$ be differentiable functions and $k \in \mathbb{R}$ a constant:

### 4.1 Basic Rules
* **Scalar Multiplication:** $(k \cdot f)'(x) = k \cdot f'(x)$
* **Sum / Difference:** $(f \pm g)'(x) = f'(x) \pm g'(x)$

### 4.2 Product and Quotient Rules
* **Product Rule (Leibniz):**

$$(f \cdot g)'(x) = f'(x)g(x) + f(x)g'(x)$$

* **Quotient Rule:**

$$\left(\frac{f}{g}\right)'(x) = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2} \quad (g(x) \neq 0)$$

### 4.3 Chain Rule (Composite Functions)

$$(f \circ g)'(x) = [f(g(x))]' = f'(g(x)) \cdot g'(x)$$

### 4.4 Generalized Power Function ($f(x)^{g(x)}$)
Using logarithmic differentiation ($f(x)^{g(x)} = e^{g(x)\ln(f(x))}$ with $f(x) > 0$):

$$[f(x)^{g(x)}]' = f(x)^{g(x)} \left[ g'(x)\ln(f(x)) + g(x)\frac{f'(x)}{f(x)} \right]$$

---

## 5. Derivative of Inverse Functions

Let $f: I \to J$ be strictly monotonic and differentiable at $x_0 \in I$, with $f'(x_0) \neq 0$.
The inverse function $f^{-1}: J \to I$ is differentiable at $y_0 = f(x_0)$, and:

$$(f^{-1})'(y_0) = \frac{1}{f'(f^{-1}(y_0))} = \frac{1}{f'(x_0)}$$

---

## 6. Fundamental Differential Theorems

### 6.1 Rolle's Theorem
Let $f: [a, b] \to \mathbb{R}$ be continuous on $[a, b]$, differentiable on $(a, b)$, and $f(a) = f(b)$.
Then there exists at least one $c \in (a, b)$ such that:

$$f'(c) = 0$$

### 6.2 Mean Value Theorem (Teorema di Lagrange)
Let $f: [a, b] \to \mathbb{R}$ be continuous on $[a, b]$ and differentiable on $(a, b)$.
Then there exists at least one $c \in (a, b)$ such that:

$$f'(c) = \frac{f(b) - f(a)}{b - a}$$

### 6.3 Cauchy's Generalized Mean Value Theorem
Let $f, g: [a, b] \to \mathbb{R}$ be continuous on $[a, b]$ and differentiable on $(a, b)$.
Then there exists at least one $c \in (a, b)$ such that:

$$[f(b) - f(a)] g'(c) = [g(b) - g(a)] f'(c)$$

### 6.4 L'Hôpital's Rule
For indeterminate forms $[0/0]$ or $[\infty/\infty]$:
If $\lim_{x \to x_0} \frac{f'(x)}{g'(x)} = L \in \mathbb{R} \cup \{\pm\infty\}$, then:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)}$$

### 6.5 Limit of the Derivative Theorem
Let $f$ be continuous on $[x_0, x_0 + \delta)$ and differentiable on $(x_0, x_0 + \delta)$.
If $\lim_{x \to x_0^+} f'(x) = L$, then the right-hand derivative exists and $f'_+(x_0) = L$.

---

## 7. Monotonicity, Extrema, and Fermat's Theorem

### 7.1 Fermat's Theorem on Stationary Points
Let $f: (a, b) \to \mathbb{R}$ and $x_0 \in (a, b)$ be a local extremum (maximum or minimum).
If $f$ is differentiable at $x_0$, then:

$$f'(x_0) = 0$$

### 7.2 Monotonicity Tests
Let $f$ be differentiable on $(a, b)$:
* $f'(x) \ge 0, \, \forall x \in (a, b) \iff f$ is monotonically increasing.
* $f'(x) > 0, \, \forall x \in (a, b) \implies f$ is strictly increasing.
* $f'(x) \le 0, \, \forall x \in (a, b) \iff f$ is monotonically decreasing.
* $f'(x) < 0, \, \forall x \in (a, b) \implies f$ is strictly decreasing.

### 7.3 First Derivative Test for Local Extrema
Around a critical point $x_0$ ($f'(x_0) = 0$):
* **Local Maximum:** $f'(x) > 0$ for $x < x_0$, and $f'(x) < 0$ for $x > x_0$ ($+ \to -$).
* **Local Minimum:** $f'(x) < 0$ for $x < x_0$, and $f'(x) > 0$ for $x > x_0$ ($- \to +$).

---

## 8. Concavity, Convexity, and Inflection Points

Let $f$ be twice differentiable on $(a, b)$:

### 8.1 Tests for Concavity and Convexity
* **Convex (Concave Upwards / Convessa $\cup$):** Tangent lines lie below the curve:

$$f''(x) \ge 0, \quad \forall x \in (a, b)$$

* **Concave (Concave Downwards / Concava $\cap$):** Tangent lines lie above the curve:

$$f''(x) \le 0, \quad \forall x \in (a, b)$$

### 8.2 Points of Inflection (Punti di Flesso)
A point $x_0$ is an inflection point if the concavity changes sign ($+ \to -$ or $- \to +$).
* **Necessary Condition:** If $x_0$ is an inflection point and $f''(x_0)$ exists $\implies f''(x_0) = 0$.
* **Second Derivative Test for Extrema:**
  * $f'(x_0) = 0 \land f''(x_0) > 0 \implies x_0$ is a **local minimum**.
  * $f'(x_0) = 0 \land f''(x_0) < 0 \implies x_0$ is a **local maximum**.

---

## 9. Asymptotic Equivalences, Infinitesimals, and Little-o Algebra

### 9.1 Asymptotic Equivalence Definition ($\sim$)
Two functions $f$ and $g$ are asymptotically equivalent as $x \to x_0$ ($f \sim g$) if:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = 1$$

### 9.2 Fundamental Asymptotic Equivalences (as $x \to 0$)

$$\sin(x) \sim x$$

$$1 - \cos(x) \sim \frac{x^2}{2}$$

$$\tan(x) \sim x$$

$$\arcsin(x) \sim x$$

$$\arctan(x) \sim x$$

$$e^x - 1 \sim x$$

$$a^x - 1 \sim x \ln(a) \quad (a > 0)$$

$$\ln(1 + x) \sim x$$

$$(1 + x)^\alpha - 1 \sim \alpha x \quad (\forall \alpha \in \mathbb{R})$$

### 9.3 Hierarchy of Growth Rates (Scala degli Infiniti, as $x \to +\infty$)
For $\beta > 0, \, \alpha > 0, \, a > 1$:

$$[\ln(x)]^\beta \ll x^\alpha \ll a^x \ll x^x$$

* **Limit Comparisons:**

$$\lim_{x \to +\infty} \frac{[\ln(x)]^\beta}{x^\alpha} = 0, \quad \lim_{x \to +\infty} \frac{x^\alpha}{a^x} = 0, \quad \lim_{x \to +\infty} \frac{a^x}{x^x} = 0$$

### 9.4 Orders of Infinitesimals and Principal Part (Scala degli Infinitesimi)
Let $f(x) \to 0$ and $g(x) \to 0$ as $x \to x_0$. If:

$$\lim_{x \to x_0} \frac{f(x)}{[g(x)]^\alpha} = L \neq 0 \quad (L \in \mathbb{R}, \, \alpha > 0)$$

* **Order of Infinitesimal:** $f(x)$ is an infinitesimal of **order $\alpha$** with respect to the test infinitesimal $g(x)$ (typically $g(x) = x - x_0$ or $g(x) = 1/x$).
* **Principal Part (Parte Principale):** $P(x) = L [g(x)]^\alpha$.

### 9.5 Little-o Definition and Algebra (O-piccolo)
We write $f(x) = o(g(x))$ as $x \to x_0$ if:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = 0$$

* **Algebraic Rules (as $x \to 0$):**
  * $o(x^n) \pm o(x^n) = o(x^n)$
  * $c \cdot o(x^n) = o(x^n) \quad (c \neq 0)$
  * $x^m \cdot o(x^n) = o(x^{n+m})$
  * $o(x^n) \cdot o(x^m) = o(x^{n+m})$
  * $[o(x^n)]^m = o(x^{n \cdot m})$
  * $o(x^n + o(x^n)) = o(x^n)$
  * $x^m + o(x^n) = x^m + o(x^m)$ for $n \ge m$ (lower powers dominate).

---

## 10. Taylor and Maclaurin Expansions

### 10.1 Taylor Formula with Peano Remainder
If $f$ is $n$-times differentiable at $x_0$:

$$f(x) = \sum_{k=0}^n \frac{f^{(k)}(x_0)}{k!} (x - x_0)^k + o((x - x_0)^n)$$

### 10.2 Standard Maclaurin Series (Centered at $x_0 = 0$)

$$\begin{aligned}
e^x &= 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots + \frac{x^n}{n!} + o(x^n) \\
\sin(x) &= x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots + (-1)^n \frac{x^{2n+1}}{(2n+1)!} + o(x^{2n+2}) \\
\cos(x) &= 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots + (-1)^n \frac{x^{2n}}{(2n)!} + o(x^{2n+1}) \\
\tan(x) &= x + \frac{x^3}{3} + \frac{2x^5}{15} + o(x^5) \\
\ln(1 + x) &= x - \frac{x^2}{2} + \frac{x^3}{3} - \dots + (-1)^{n-1} \frac{x^n}{n} + o(x^n) \\
\arctan(x) &= x - \frac{x^3}{3} + \frac{x^5}{5} - \dots + (-1)^n \frac{x^{2n+1}}{2n+1} + o(x^{2n+2}) \\
\arcsin(x) &= x + \frac{x^3}{6} + \frac{3x^5}{40} + o(x^5) \\
(1 + x)^\alpha &= 1 + \alpha x + \frac{\alpha(\alpha - 1)}{2!}x^2 + \dots + \binom{\alpha}{n}x^n + o(x^n)
\end{aligned}$$

---

[Back to Main README](../README.md)

# 05. Integral Calculus

Comprehensive guide to integral calculus: antiderivatives, fundamental properties of the Riemann integral, integral mean value theorems, the Fundamental Theorem of Calculus, standard integration methods, partial fraction decomposition, Weierstrass substitutions, operational shortcuts, and improper integrals with convergence criteria.

---

## Table of Contents

1. [Indefinite Integrals and Standard Antiderivatives](#1-indefinite-integrals-and-standard-antiderivatives)
2. [Riemann Definite Integral and Fundamental Properties](#2-riemann-definite-integral-and-fundamental-properties)
3. [Integral Mean Value Theorems](#3-integral-mean-value-theorems)
4. [Fundamental Theorem of Calculus (Torricelli-Barrow)](#4-fundamental-theorem-of-calculus-torricelli-barrow)
5. [Integration by Parts (Standard and DI Method)](#5-integration-by-parts-standard-and-di-method)
6. [Integration by Substitution](#6-integration-by-substitution)
7. [Rational Functions and Partial Fraction Decomposition](#7-rational-functions-and-partial-fraction-decomposition)
8. [Advanced Substitutions, Taylor Series, and Operational Shortcuts](#8-advanced-substitutions-taylor-series-and-operational-shortcuts)
9. [Improper Integrals and Convergence Criteria](#9-improper-integrals-and-convergence-criteria)

---

## 1. Indefinite Integrals and Standard Antiderivatives

An antiderivative (primitiva) of a function $f(x)$ on an interval $I$ is any differentiable function $F(x)$ such that $F'(x) = f(x), \, \forall x \in I$.
The indefinite integral represents the family of all antiderivatives:

$$\int f(x) \, dx = F(x) + C \quad (C \in \mathbb{R})$$

### 1.1 Table of Immediate Generalized Antiderivatives

| Integrand Form | Antiderivative | Conditions |
| :--- | :--- | :--- |
| $\int f'(x) [f(x)]^\alpha \, dx$ | $\frac{[f(x)]^{\alpha+1}}{\alpha+1} + C$ | $\alpha \neq -1$ |
| $\int \frac{f'(x)}{f(x)} \, dx$ | $\ln|f(x)| + C$ | $f(x) \neq 0$ |
| $\int f'(x) e^{f(x)} \, dx$ | $e^{f(x)} + C$ | $x \in \mathbb{R}$ |
| $\int f'(x) a^{f(x)} \, dx$ | $\frac{a^{f(x)}}{\ln(a)} + C$ | $a > 0, a \neq 1$ |
| $\int f'(x) \cos(f(x)) \, dx$ | $\sin(f(x)) + C$ | $x \in \mathbb{R}$ |
| $\int f'(x) \sin(f(x)) \, dx$ | $-\cos(f(x)) + C$ | $x \in \mathbb{R}$ |
| $\int \frac{f'(x)}{\cos^2(f(x))} \, dx$ | $\tan(f(x)) + C$ | $f(x) \neq \frac{\pi}{2} + k\pi$ |
| $\int \frac{f'(x)}{1 + [f(x)]^2} \, dx$ | $\arctan(f(x)) + C$ | $x \in \mathbb{R}$ |
| $\int \frac{f'(x)}{\sqrt{1 - [f(x)]^2}} \, dx$ | $\arcsin(f(x)) + C$ | $|f(x)| < 1$ |

---

## 2. Riemann Definite Integral and Fundamental Properties

Let $f, g: [a, b] \to \mathbb{R}$ be Riemann-integrable functions:

### 2.1 Boundary Conventions
* **Null Interval:**

$$\int_a^a f(x) \, dx = 0$$

* **Reversal of Integration Limits:**

$$\int_b^a f(x) \, dx = -\int_a^b f(x) \, dx$$

### 2.2 Fundamental Operational Properties
* **Linearity:**

$$\int_a^b [\alpha f(x) + \beta g(x)] \, dx = \alpha \int_a^b f(x) \, dx + \beta \int_a^b g(x) \, dx \quad (\forall \alpha, \beta \in \mathbb{R})$$

* **Interval Additivity:** For any $c \in [a, b]$:

$$\int_a^b f(x) \, dx = \int_a^c f(x) \, dx + \int_c^b f(x) \, dx$$

* **Monotonicity (Preservation of Order):**

$$\text{If } f(x) \le g(x), \, \forall x \in [a, b] \implies \int_a^b f(x) \, dx \le \int_a^b g(x) \, dx$$

* **Triangle Inequality for Integrals:**

$$\left| \int_a^b f(x) \, dx \right| \le \int_a^b |f(x)| \, dx$$

---

## 3. Integral Mean Value Theorems

### 3.1 Mean Value Theorem for Integrals (Teorema della Media Integrale)
If $f: [a, b] \to \mathbb{R}$ is continuous, then there exists at least one point $c \in [a, b]$ such that:

$$\frac{1}{b - a} \int_a^b f(x) \, dx = f(c)$$

* The quantity $\mu = \frac{1}{b-a} \int_a^b f(x) \, dx$ is called the **integral average value** of $f$ on $[a, b]$.

### 3.2 Weighted Mean Value Theorem (Media Integrale Pesata)
Let $f, g: [a, b] \to \mathbb{R}$ be continuous, with a non-negative weight function $g(x) \ge 0, \, \forall x \in [a, b]$. Then there exists $c \in [a, b]$ such that:

$$\int_a^b f(x) g(x) \, dx = f(c) \int_a^b g(x) \, dx$$

---

## 4. Fundamental Theorem of Calculus (Torricelli-Barrow)

### 4.1 First Fundamental Theorem (Integral Function & Torricelli's Theorem)
Let $f: [a, b] \to \mathbb{R}$ be continuous. The **integral function** $F: [a, b] \to \mathbb{R}$ defined by:

$$F(x) = \int_a^x f(t) \, dt$$

is continuous on $[a, b]$, differentiable on $(a, b)$, and its derivative satisfies:

$$F'(x) = \frac{d}{dx} \left[ \int_a^x f(t) \, dt \right] = f(x), \quad \forall x \in (a, b)$$

* **Chain Rule Extension (Leibniz Integral Rule):**

$$\frac{d}{dx} \left[ \int_{u(x)}^{v(x)} f(t) \, dt \right] = f(v(x)) \cdot v'(x) - f(u(x)) \cdot u'(x)$$

### 4.2 Second Fundamental Theorem (Newton-Leibniz Formula)
If $f$ is continuous on $[a, b]$ and $G(x)$ is any antiderivative of $f$ ($G'(x) = f(x)$):

$$\int_a^b f(x) \, dx = [G(x)]_a^b = G(b) - G(a)$$

---

## 5. Integration by Parts (Standard and DI Method)

### 5.1 Standard Formula

$$\int u(x) v'(x) \, dx = u(x)v(x) - \int u'(x)v(x) \, dx$$

For definite integrals:

$$\int_a^b u(x) v'(x) \, dx = [u(x)v(x)]_a^b - \int_a^b u'(x)v(x) \, dx$$

### 5.2 The DI Method (Tabular Integration Shortcut)
Used for repeated integration by parts, such as $\int P(x) e^{ax} \, dx$, $\int P(x) \sin(ax) \, dx$, or $\int P(x) \cos(ax) \, dx$:

1. Create two columns: **D** (Differentiate) and **I** (Integrate).
2. Differentiate the polynomial $P(x)$ down to $0$.
3. Integrate the transcendental function repeatedly.
4. Multiply terms along diagonals with alternating signs ($+, -, +, \dots$).

---

## 6. Integration by Substitution

### 6.1 Indefinite Substitution
Let $x = g(t)$, where $g$ is continuously differentiable:

$$\int f(g(t)) g'(t) \, dt = \int f(u) \, du \quad (\text{with } u = g(t), \, du = g'(t)dt) \text{}$$

### 6.2 Definite Substitution
When applying substitution to a definite integral, transform the integration boundaries accordingly:

$$\int_a^b f(g(x)) g'(x) \, dx = \int_{g(a)}^{g(b)} f(u) \, du$$

---

## 7. Rational Functions and Partial Fraction Decomposition

To integrate rational functions $\frac{P(x)}{Q(x)}$:
* If $\deg(P) \ge \deg(Q)$, perform polynomial division first: $\frac{P(x)}{Q(x)} = S(x) + \frac{R(x)}{Q(x)}$ with $\deg(R) < \deg(Q)$.
* Factorize $Q(x)$ into linear factors $(x - r)$ and irreducible quadratic factors $(x^2 + px + q)$.

### 7.1 Decomposition Cases

* **Distinct Linear Factors $(x - a)(x - b)$:**

$$\frac{R(x)}{(x - a)(x - b)} = \frac{A}{x - a} + \frac{B}{x - b} \text{}$$

* **Repeated Linear Factors $(x - a)^k$:**

$$\frac{R(x)}{(x - a)^k} = \frac{A_1}{x - a} + \frac{A_2}{(x - a)^2} + \dots + \frac{A_k}{(x - a)^k} \text{}$$

* **Irreducible Quadratic Factor $(x^2 + px + q)$ with $\Delta < 0$:**

$$\frac{R(x)}{x^2 + px + q} \implies \text{Split into a logarithmic derivative part } \frac{f'(x)}{f(x)} \text{ and an arctangent part } \frac{1}{1 + u^2} \text{}$$

---

## 8. Advanced Substitutions, Taylor Series, and Operational Shortcuts

### 8.1 Universal Weierstrass Parametric Substitution
For integrals containing rational expressions of sine and cosine $R(\sin x, \cos x)$, set $t = \tan(x/2)$:

$$\sin(x) = \frac{2t}{1 + t^2}, \quad \cos(x) = \frac{1 - t^2}{1 + t^2}, \quad dx = \frac{2}{1 + t^2} \, dt \text{}$$

### 8.2 Symmetry Shortcuts on Symmetric Intervals $[-a, a]$
* **Even Function ($f(-x) = f(x)$):**

$$\int_{-a}^a f(x) \, dx = 2 \int_0^a f(x) \, dx \text{}$$

* **Odd Function ($f(-x) = -f(x)$):**

$$\int_{-a}^a f(x) \, dx = 0 \text{}$$

### 8.3 Integration via Taylor / Maclaurin Series
For functions without elementary antiderivatives (e.g., $e^{-x^2}, \frac{\sin x}{x}$):

$$f(x) = \sum_{k=0}^n \frac{f^{(k)}(0)}{k!} x^k + R_n(x) \implies \int f(x) \, dx = \sum_{k=0}^n \frac{f^{(k)}(0)}{k!(k+1)} x^{k+1} + \dots$$

---

## 9. Improper Integrals and Convergence Criteria

### 9.1 Classification of Improper Integrals
* **Type I (Unbounded Intervals $[a, +\infty)$):**

$$\int_a^{+\infty} f(x) \, dx = \lim_{t \to +\infty} \int_a^t f(x) \, dx \text{}$$

* **Type II (Singularities / Vertical Asymptotes near $b^-$):**

$$\int_a^b f(x) \, dx = \lim_{t \to b^-} \int_a^t f(x) \, dx \text{}$$

### 9.2 Reference $p$-Integrals (Integrali Campione)

* **At Infinity ($[a, +\infty)$ with $a > 0$):**

$$\int_a^{+\infty} \frac{1}{x^p} \, dx \quad \begin{cases} \text{Converges} & \text{if } p > 1 \\ \text{Diverges to } +\infty & \text{if } p \le 1 \end{cases} \text{}$$

* **Near Singularities ($(0, a]$ with $a > 0$):**

$$\int_0^a \frac{1}{x^p} \, dx \quad \begin{cases} \text{Converges} & \text{if } p < 1 \\ \text{Diverges to } +\infty & \text{if } p \ge 1 \end{cases}$$

### 9.3 Convergence Criteria for Non-Negative Integrands ($f(x) \ge 0$)

* **Direct Comparison Test (Criterio del Confronto):**
  If $0 \le f(x) \le g(x)$ for all $x \ge a$:
  * $\int_a^{+\infty} g(x) \, dx \text{ converges} \implies \int_a^{+\infty} f(x) \, dx \text{ converges}$
  * $\int_a^{+\infty} f(x) \, dx \text{ diverges} \implies \int_a^{+\infty} g(x) \, dx \text{ diverges}$

* **Asymptotic Comparison Test (Criterio del Confronto Asintotico):**
  If $f(x) \sim \frac{L}{x^p}$ as $x \to +\infty$ ($L > 0$):

$$\int_a^{+\infty} f(x) \, dx \text{ converges} \iff p > 1$$

---

[Back to Main README](../README.md)

# 03. Limits of Functions & Continuity

Formal analysis of real function limits, limit computation laws, standard notable limits, indeterminate forms, continuity criteria, discontinuity classifications, and fundamental theorems on continuous functions.

---

## Table of Contents

1. [Definition and Classification of Limits](#1-definition-and-classification-of-limits)
2. [Limit Laws and Algebraic Operations](#2-limit-laws-and-algebraic-operations)
3. [Comparison and Squeeze Theorems](#3-comparison-and-squeeze-theorems)
4. [Composite Function Limits and Change of Variable](#4-composite-function-limits-and-change-of-variable)
5. [Indeterminate Forms](#5-indeterminate-forms)
6. [List of Standard and Notable Limits](#6-list-of-standard-and-notable-limits)
7. [Continuity of Real Functions](#7-continuity-of-real-functions)
8. [Classification of Discontinuities](#8-classification-of-discontinuities)
9. [Fundamental Theorems on Continuous Functions](#9-fundamental-theorems-on-continuous-functions)

---

## 1. Definition and Classification of Limits

Let $f: X \to \mathbb{R}$ be a function and $x_0 \in \mathbb{R}$ an accumulation point for $X$.

### 1.1 Formal Classifications

* **Convergent (Finite Limit $L \in \mathbb{R}$):**

$$\lim_{x \to x_0} f(x) = L \iff \forall \varepsilon > 0, \, \exists \delta > 0 : \forall x \in X, \, 0 < |x - x_0| < \delta \implies |f(x) - L| < \varepsilon$$

* **Divergent to $+\infty$:**

$$\lim_{x \to x_0} f(x) = +\infty \iff \forall M > 0, \, \exists \delta > 0 : \forall x \in X, \, 0 < |x - x_0| < \delta \implies f(x) > M$$

* **Divergent to $-\infty$:**

$$\lim_{x \to x_0} f(x) = -\infty \iff \forall M > 0, \, \exists \delta > 0 : \forall x \in X, \, 0 < |x - x_0| < \delta \implies f(x) < -M$$

* **Irregular / Oscillating (Limit Does Not Exist):**
  The function oscillates indefinitely near $x_0$ without approaching any single value or infinity (e.g., $\lim_{x \to 0} \sin(1/x)$ ).

### 1.2 One-Sided Limits (Destro e Sinistro)
* **Right-hand Limit ( $x \to x_0^+$):** Evaluated for $x \in (x_0, x_0 + \delta)$.
* **Left-hand Limit ( $x \to x_0^-$):** Evaluated for $x \in (x_0 - \delta, x_0)$.
* *Theorem:* The two-sided limit exists if and only if both one-sided limits exist and are equal:

$$\lim_{x \to x_0} f(x) = L \iff \lim_{x \to x_0^+} f(x) = \lim_{x \to x_0^-} f(x) = L$$

---

## 2. Limit Laws and Algebraic Operations

Assuming $\lim_{x \to x_0} f(x) = L_1 \in \mathbb{R}$ and $\lim_{x \to x_0} g(x) = L_2 \in \mathbb{R}$:

* **Linear Combinations:**

$$\lim_{x \to x_0} [\alpha f(x) + \beta g(x)] = \alpha L_1 + \beta L_2 \quad (\forall \alpha, \beta \in \mathbb{R})$$

* **Product Law:**

$$\lim_{x \to x_0} [f(x) \cdot g(x)] = L_1 \cdot L_2$$

* **Quotient Law:**

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \frac{L_1}{L_2} \quad (\text{provided } L_2 \neq 0)$$

* **Power Law:**

$$\lim_{x \to x_0} [f(x)]^{g(x)} = L_1^{L_2} \quad (\text{provided } L_1 > 0)$$

---

## 3. Comparison and Squeeze Theorems

* **Order Preservation:** If $f(x) \le g(x)$ in a punctured neighborhood of $x_0$, then:

$$\lim_{x \to x_0} f(x) \le \lim_{x \to x_0} g(x)$$

* **Squeeze Theorem (Teorema dei Carabinieri):** If $g(x) \le f(x) \le h(x)$ near $x_0$, and $\lim_{x \to x_0} g(x) = \lim_{x \to x_0} h(x) = L$, then:

$$\lim_{x \to x_0} f(x) = L$$

* **Bounded $\times$ Infinitesimal:** If $|f(x)| \le M$ (bounded) and $\lim_{x \to x_0} g(x) = 0$, then:

$$\lim_{x \to x_0} [f(x) \cdot g(x)] = 0$$

---

## 4. Composite Function Limits and Change of Variable

### 4.1 Limit of Composite Functions
Let $\lim_{x \to x_0} g(x) = y_0$. If $f(y)$ is continuous at $y = y_0$ (or if $g(x) \neq y_0$ for $x \neq x_0$), then:

$$\lim_{x \to x_0} f(g(x)) = f\left( \lim_{x \to x_0} g(x) \right) = f(y_0)$$

### 4.2 Substitution Technique (Cambio di Variabile)
To evaluate $\lim_{x \to x_0} f(g(x))$, set $t = g(x)$. As $x \to x_0 \implies t \to y_0$:

$$\lim_{x \to x_0} f(g(x)) = \lim_{t \to y_0} f(t)$$

---

## 5. Indeterminate Forms

Algebraic limit operations can result in indeterminate forms that require algebraic manipulation, Taylor expansions, or L'Hôpital's Rule:

$$\left[ \frac{0}{0} \right], \quad \left[ \frac{\infty}{\infty} \right], \quad [0 \cdot \infty], \quad [+\infty - \infty], \quad [1^\infty], \quad [0^0], \quad [\infty^0]$$

---

## 6. List of Standard and Notable Limits

All limits below assume $x \to 0$ unless specified otherwise.

### 6.1 Trigonometric Limits

$$\lim_{x \to 0} \frac{\sin(x)}{x} = 1$$

$$\lim_{x \to 0} \frac{1 - \cos(x)}{x^2} = \frac{1}{2}$$

$$\lim_{x \to 0} \frac{\tan(x)}{x} = 1$$

$$\lim_{x \to 0} \frac{\arcsin(x)}{x} = 1$$

$$\lim_{x \to 0} \frac{\arctan(x)}{x} = 1$$

### 6.2 Exponential and Logarithmic Limits

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

$$\lim_{x \to 0} \frac{a^x - 1}{x} = \ln(a) \quad (a > 0)$$

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

$$\lim_{x \to 0} \frac{\log_a(1 + x)}{x} = \frac{1}{\ln(a)} = \log_a(e)$$

### 6.3 Generalized Binomial and Base $e$ Limits

$$\lim_{x \to 0} \frac{(1 + x)^\alpha - 1}{x} = \alpha \quad (\forall \alpha \in \mathbb{R})$$

$$\lim_{x \to \pm\infty} \left(1 + \frac{1}{x}\right)^x = e$$

$$\lim_{x \to 0} (1 + x)^{1/x} = e$$

---

## 7. Continuity of Real Functions

### 7.1 Definition at a Point
A function $f$ is continuous at $x_0 \in \text{dom}(f)$ if:

$$\lim_{x \to x_0} f(x) = f(x_0) \iff \lim_{x \to x_0^+} f(x) = \lim_{x \to x_0^-} f(x) = f(x_0)$$

### 7.2 Continuity of Elementary Functions
All standard elementary functions are **continuous on their entire domain of definition**:
* Polynomials and rational functions
* Power and root functions ($x^\alpha, \sqrt[n]{x}$)
* Exponential and logarithmic functions ( $a^x, \log_a(x)$ )
* Trigonometric and inverse trigonometric functions ($\sin x, \cos x, \tan x, \arcsin x, \arctan x$)

---

## 8. Classification of Discontinuities

Let $x_0$ be a point where $f(x)$ fails to be continuous:

### 8.1 First Kind: Jump Discontinuity (Discontinuità di Salto)
Left and right limits exist and are finite, but are unequal:

$$\lim_{x \to x_0^-} f(x) = L_1, \quad \lim_{x \to x_0^+} f(x) = L_2 \quad \text{with } L_1 \neq L_2$$

* **Jump Height:** $J = |L_2 - L_1|$

### 8.2 Second Kind: Essential Discontinuity (Seconda Specie)
At least one of the one-sided limits does not exist or is infinite ($\pm\infty$):

$$\lim_{x \to x_0^-} f(x) = \pm\infty \quad \text{or} \quad \lim_{x \to x_0^+} f(x) = \pm\infty \quad \text{(or does not exist)}$$

### 8.3 Third Kind: Removable Discontinuity (Terza Specie / Eliminabile)
The two-sided limit exists and is finite ($L \in \mathbb{R}$), but either $x_0 \notin \text{dom}(f)$ or $L \neq f(x_0)$:

$$\lim_{x \to x_0} f(x) = L \neq f(x_0)$$

* Can be made continuous by extending the definition: $\tilde{f}(x_0) = L$.

---

## 9. Fundamental Theorems on Continuous Functions

### 9.1 Zero-Point Theorem (Teorema di Esistenza degli Zeri / Bolzano)
Let $f: [a, b] \to \mathbb{R}$ be continuous on a closed bounded interval $[a, b]$. If:

$$f(a) \cdot f(b) < 0$$

Then there exists at least one point $c \in (a, b)$ such that:

$$f(c) = 0$$

### 9.2 Intermediate Value Theorem (Teorema dei Valori Intermedi)
Let $f: [a, b] \to \mathbb{R}$ be continuous on $[a, b]$. Then $f$ attains every value between $f(a)$ and $f(b)$:

$$\forall y_0 \in (\min(f(a), f(b)), \max(f(a), f(b))), \quad \exists c \in (a, b) : f(c) = y_0$$

### 9.3 Weierstrass Extreme Value Theorem (Teorema di Weierstrass)
Let $f: [a, b] \to \mathbb{R}$ be continuous on a closed and bounded (compact) interval $[a, b]$. Then $f$ attains an absolute maximum ($M$) and an absolute minimum ($m$):

$$\exists x_{\min}, x_{\max} \in [a, b] : \forall x \in [a, b], \quad m = f(x_{\min}) \le f(x) \le f(x_{\max}) = M$$

---

[Back to Main README](../README.md)

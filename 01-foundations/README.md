# 01. Foundations & Preliminaries

This directory covers the foundational mathematical structures, axiomatic foundations of real numbers, essential topology of the real line, fundamental algebraic and logarithmic identities, trigonometry, and function classifications required for Calculus 1.

---

## Table of Contents

1. [Axiomatic Structure of Real Numbers](#1-axiomatic-structure-of-real-numbers)
2. [Bounds, Supremum, and Infimum](#2-bounds-supremum-and-infimum)
3. [Topology of Real Numbers: Intervals and Neighborhoods](#3-topology-of-real-numbers-intervals-and-neighborhoods)
4. [Mathematical Induction and Bernoulli's Inequality](#4-mathematical-induction-and-bernoullis-inequality)
5. [Special Products and Binomial Theorem](#5-special-products-and-binomial-theorem)
6. [Powers, Exponentials, and Logarithms](#6-powers-exponentials-and-logarithms)
7. [Trigonometric Identities and Methods](#7-trigonometric-identities-and-methods)
8. [Functions: Properties, Monotonicity, and Compositions](#8-functions-properties-monotonicity-and-compositions)

---

## 1. Axiomatic Structure of Real Numbers

The set of real numbers $\mathbb{R}$ is defined as a complete ordered field.

### 1.1 Field Axioms
For all $a, b, c \in \mathbb{R}$:
* Associativity: $(a + b) + c = a + (b + c)$ and $(a \cdot b) \cdot c = a \cdot (b \cdot c)$
* Commutativity: $a + b = b + a$ and $a \cdot b = b \cdot a$
* Additive Identity: $a + 0 = a$
* Multiplicative Identity: $a \cdot 1 = a$
* Opposite: $\forall a \in \mathbb{R}, \exists (-a) : a + (-a) = 0$
* Reciprocal: $\forall a \in \mathbb{R} \setminus \{0\}, \exists a^{-1} = \frac{1}{a} : a \cdot \frac{1}{a} = 1$
* Distributivity: $a \cdot (b + c) = a \cdot b + a \cdot c$

### 1.2 Order Axioms
* Total Order: $\forall a, b \in \mathbb{R}$, either $a \le b$ or $b \le a$
* Transitivity: $a \le b \land b \le c \implies a \le c$
* Compatibility with Addition: $a \le b \implies a + c \le b + c$
* Compatibility with Multiplication: $(a \le b \land c > 0) \implies a \cdot c \le b \cdot c$

### 1.3 Cardinality, Density, and Completeness
* Hierarchy: $\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$
* Cardinality: $\mathbb{N}, \mathbb{Z}, \mathbb{Q}$ are countable ($|\mathbb{N}| = \aleph_0$), while $\mathbb{R}$ is uncountable ($|\mathbb{R}| = \mathfrak{c} = 2^{\aleph_0}$)
* Density of $\mathbb{Q}$ and $\mathbb{R} \setminus \mathbb{Q}$:

$$\forall a, b \in \mathbb{R} \text{ with } a < b, \quad \exists q \in \mathbb{Q}, \, \exists r \in \mathbb{R} \setminus \mathbb{Q} : a < q < b \land a < r < b$$

* Completeness Axiom (Dedekind): Every non-empty subset $A \subset \mathbb{R}$ bounded above has a least upper bound ($\sup A \in \mathbb{R}$).

---

## 2. Bounds, Supremum, and Infimum

Let $A \subseteq \mathbb{R}$ be a non-empty set:

* Bounded Above: $\exists M \in \mathbb{R} : \forall x \in A, \, x \le M$
* Bounded Below: $\exists m \in \mathbb{R} : \forall x \in A, \, x \ge m$
* Bounded Set: A set bounded both above and below.

### Epsilon Characterization

Supremum ($L = \sup A$):

$$L = \sup A \iff \begin{cases} \forall x \in A, & x \le L \\ \forall \varepsilon > 0, \, \exists x \in A : & x > L - \varepsilon \end{cases}$$

Infimum ($l = \inf A$):

$$l = \inf A \iff \begin{cases} \forall x \in A, & x \ge l \\ \forall \varepsilon > 0, \, \exists x \in A : & x < l + \varepsilon \end{cases}$$

* Maximum: If $\sup A \in A$, then $\max A = \sup A$
* Minimum: If $\inf A \in A$, then $\min A = \inf A$

---

## 3. Topology of Real Numbers: Intervals and Neighborhoods

### 3.1 Intervals
* Bounded: $(a, b)$, $[a, b]$, $[a, b)$, $(a, b]$
* Unbounded: $(-\infty, b)$, $[a, +\infty)$, $(-\infty, +\infty) = \mathbb{R}$

### 3.2 Neighborhoods
* Open ball centered at $x_0$ with radius $r > 0$:

$$I_r(x_0) = (x_0 - r, x_0 + r) = \{x \in \mathbb{R} : |x - x_0| < r\}$$

* Punctured neighborhood:

$$\dot{I}_r(x_0) = I_r(x_0) \setminus \{x_0\} = \{x \in \mathbb{R} : 0 < |x - x_0| < r\}$$

### 3.3 Point Classifications
Let $A \subseteq \mathbb{R}$ and $x_0 \in \mathbb{R}$:
* Interior Point: $\exists r > 0 : I_r(x_0) \subseteq A$
* Accumulation Point: $\forall r > 0, \, \dot{I}_r(x_0) \cap A \neq \emptyset$
* Isolated Point: $x_0 \in A$ and $\exists r > 0 : I_r(x_0) \cap A = \{x_0\}$

---

## 4. Mathematical Induction and Bernoulli's Inequality

### 4.1 Principle of Mathematical Induction
To prove that $P(n)$ holds $\forall n \ge n_0$ ($n, n_0 \in \mathbb{N}$):
1. Base Step: Prove $P(n_0)$ is true.
2. Inductive Step: Assume $P(k)$ is true, then prove $P(k+1)$ is true.

$$P(k) \implies P(k+1)$$

### 4.2 Bernoulli's Inequality

$$\forall x \ge -1, \quad \forall n \in \mathbb{N} \implies (1 + x)^n \ge 1 + nx$$

---

## 5. Special Products and Binomial Theorem

* Difference of Squares: $a^2 - b^2 = (a - b)(a + b)$
* Square of Binomial: $(a \pm b)^2 = a^2 \pm 2ab + b^2$
* Square of Trinomial: $(a + b + c)^2 = a^2 + b^2 + c^2 + 2ab + 2ac + 2bc$
* Cubes:
  * $(a \pm b)^3 = a^3 \pm 3a^2b + 3ab^2 \pm b^3$
  * $a^3 \pm b^3 = (a \pm b)(a^2 \mp ab + b^2)$
* Difference of $n$-th Powers:

$$a^n - b^n = (a - b)(a^{n-1} + a^{n-2}b + \dots + ab^{n-2} + b^{n-1})$$

* Binomial Theorem:

$$(a + b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k} b^k, \quad \binom{n}{k} = \frac{n!}{k!(n-k)!}$$

---

## 6. Powers, Exponentials, and Logarithms

### 6.1 Exponent Rules ($a, b > 0$)

$$x^a \cdot x^b = x^{a+b}, \quad \frac{x^a}{x^b} = x^{a-b}, \quad (x^a)^b = x^{ab}, \quad x^{-a} = \frac{1}{x^a}, \quad x^{p/q} = \sqrt[q]{x^p}$$

### 6.2 Logarithm Properties ($x, y > 0, \, a > 0, \, a \neq 1$)

$$\log_a(x) = y \iff a^y = x$$

* Product: $\ln(x \cdot y) = \ln(x) + \ln(y)$
* Quotient: $\ln\left(\frac{x}{y}\right) = \ln(x) - \ln(y)$
* Power: $\ln(x^k) = k \ln(x)$
* Base Change: $\log_a(x) = \frac{\ln(x)}{\ln(a)}$

---

## 7. Trigonometric Identities and Methods

### 7.1 Fundamentals
* Angle Conversion: $\alpha_{\text{rad}} = \alpha_{\text{deg}} \cdot \frac{\pi}{180}$
* Fundamental Identity: $\sin^2(x) + \cos^2(x) = 1$
* Reciprocal and Tangent:

$$\tan(x) = \frac{\sin(x)}{\cos(x)}, \quad \cot(x) = \frac{\cos(x)}{\sin(x)}, \quad \sec(x) = \frac{1}{\cos(x)}, \quad \csc(x) = \frac{1}{\sin(x)}$$

### 7.2 Addition and Subtraction
* $\sin(\alpha \pm \beta) = \sin(\alpha)\cos(\beta) \pm \cos(\alpha)\sin(\beta)$
* $\cos(\alpha \pm \beta) = \cos(\alpha)\cos(\beta) \mp \sin(\alpha)\sin(\beta)$
* $\tan(\alpha \pm \beta) = \frac{\tan(\alpha) \pm \tan(\beta)}{1 \mp \tan(\alpha)\tan(\beta)}$

### 7.3 Double-Angle and Power Reduction
* Double-Angle:

$$\sin(2x) = 2\sin(x)\cos(x)$$

$$\cos(2x) = \cos^2(x) - \sin^2(x) = 2\cos^2(x) - 1 = 1 - 2\sin^2(x)$$

* Power Reduction:

$$\sin^2(x) = \frac{1 - \cos(2x)}{2}, \quad \cos^2(x) = \frac{1 + \cos(2x)}{2}$$

### 7.4 Half-Angle Formulas

$$\sin\left(\frac{x}{2}\right) = \pm\sqrt{\frac{1 - \cos(x)}{2}}, \quad \cos\left(\frac{x}{2}\right) = \pm\sqrt{\frac{1 + \cos(x)}{2}}, \quad \tan\left(\frac{x}{2}\right) = \frac{1 - \cos(x)}{\sin(x)} = \frac{\sin(x)}{1 + \cos(x)}$$

### 7.5 Universal Parametric Substitution (t = tan(x/2))

$$\sin(x) = \frac{2t}{1 + t^2}, \quad \cos(x) = \frac{1 - t^2}{1 + t^2}, \quad \tan(x) = \frac{2t}{1 - t^2}$$

### 7.6 Harmonic Addition Form
To combine $a\sin(x) + b\cos(x)$ into a single sinusoidal term:

$$a\sin(x) + b\cos(x) = R\sin(x + \varphi)$$

$$\text{where } R = \sqrt{a^2 + b^2}, \quad \cos(\varphi) = \frac{a}{R}, \quad \sin(\varphi) = \frac{b}{R}$$

### 7.7 Prosthaphaeresis and Werner
* Prosthaphaeresis:

$$\sin(p) \pm \sin(q) = 2\sin\left(\frac{p \pm q}{2}\right)\cos\left(\frac{p \mp q}{2}\right)$$

$$\cos(p) + \cos(q) = 2\cos\left(\frac{p + q}{2}\right)\cos\left(\frac{p - q}{2}\right)$$

$$\cos(p) - \cos(q) = -2\sin\left(\frac{p + q}{2}\right)\sin\left(\frac{p - q}{2}\right)$$

* Werner:

$$\sin(\alpha)\cos(\beta) = \frac{1}{2}[\sin(\alpha + \beta) + \sin(\alpha - \beta)]$$

$$\cos(\alpha)\cos(\beta) = \frac{1}{2}[\cos(\alpha + \beta) + \cos(\alpha - \beta)]$$

$$\sin(\alpha)\sin(\beta) = \frac{1}{2}[\cos(\alpha - \beta) - \cos(\alpha + \beta)]$$

---

## 8. Functions: Properties, Monotonicity, and Compositions

Let $f: X \to Y$ be a real-valued function ($X, Y \subseteq \mathbb{R}$).

### 8.1 Basic Properties
* Domain: Set of $x \in \mathbb{R}$ where $f(x)$ is well-defined
* Even Function: $f(-x) = f(x)$
* Odd Function: $f(-x) = -f(x)$
* Periodic Function: $\exists T > 0 : f(x + T) = f(x), \, \forall x \in X$

### 8.2 Injectivity, Surjectivity, and Bijectivity
* Injective (One-to-One): $f(x_1) = f(x_2) \implies x_1 = x_2$
* Surjective (Onto): $\forall y \in Y, \, \exists x \in X : f(x) = y$
* Bijective: Injective and Surjective $\implies$ Invertible ($f^{-1}: Y \to X$)

### 8.3 Monotonicity
Let $I \subseteq X$ be an interval:
* Strictly Increasing: $\forall x_1, x_2 \in I, \, x_1 < x_2 \implies f(x_1) < f(x_2)$
* Strictly Decreasing: $\forall x_1, x_2 \in I, \, x_1 < x_2 \implies f(x_1) > f(x_2)$
* Property: Strictly monotonic functions are always injective.

### 8.4 Operations and Compositions
* Linear Combination: $(af + bg)(x) = af(x) + bg(x)$
* Product and Quotient: $(f \cdot g)(x) = f(x)g(x), \quad (f / g)(x) = f(x) / g(x)$
* Generalized Exponential Base:

$$[f(x)]^{g(x)} = e^{g(x)\ln(f(x))} \quad (\text{for } f(x) > 0)$$

* Function Composition:

$$(f \circ g)(x) = f(g(x)) \quad \text{with } \text{dom}(f \circ g) = \{x \in \text{dom}(g) : g(x) \in \text{dom}(f)\}$$

---

[Back to Main README](../README.md)

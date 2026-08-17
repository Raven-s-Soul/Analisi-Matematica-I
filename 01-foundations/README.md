# 01. Foundations & Preliminaries

This directory covers the foundational mathematical logic, axiomatic structures of the real number system, topology of the real line, essential algebra, and general function classifications.

---

## Table of Contents

1. [Axiomatic Structure of Real Numbers](#1-axiomatic-structure-of-real-numbers)
2. [Bounds, Extremums, Supremum, and Infimum](#2-bounds-extremums-supremum-and-infimum)
3. [Topology of the Real Line](#3-topology-of-the-real-line)
4. [Mathematical Induction and Bernoulli's Inequality](#4-mathematical-induction-and-bernoullis-inequality)
5. [Special Products and Binomial Theorem](#5-special-products-and-binomial-theorem)
6. [Powers, Exponentials, and Logarithms](#6-powers-exponentials-and-logarithms)
7. [Functions: Properties, Monotonicity, and Compositions](#7-functions-properties-monotonicity-and-compositions)

---

## 1. Axiomatic Structure of Real Numbers

The real number system $\mathbb{R}$ is defined as a **complete ordered field**.

### 1.1 Field Axioms (Addition and Multiplication)
For all $a, b, c \in \mathbb{R}$:
* **Associativity:** $(a + b) + c = a + (b + c)$ and $(a \cdot b) \cdot c = a \cdot (b \cdot c)$
* **Commutativity:** $a + b = b + a$ and $a \cdot b = b \cdot a$
* **Identities:** Neutral elements $0$ ($a + 0 = a$) and $1$ ($a \cdot 1 = a$)
* **Inverses:** 
  * Additive inverse (Opposite): $\forall a \in \mathbb{R}, \, \exists (-a) : a + (-a) = 0$
  * Multiplicative inverse (Reciprocal): $\forall a \in \mathbb{R} \setminus \{0\}, \, \exists a^{-1} = \frac{1}{a} : a \cdot \frac{1}{a} = 1$
* **Distributivity:** $a \cdot (b + c) = a \cdot b + a \cdot c$

### 1.2 Order Axioms
* **Total Order:** $\forall a, b \in \mathbb{R}$, either $a \le b$ or $b \le a$
* **Transitivity:** $a \le b \land b \le c \implies a \le c$
* **Operation Compatibility:**
  * $a \le b \implies a + c \le b + c$
  * $(a \le b \land c > 0) \implies a \cdot c \le b \cdot c$

### 1.3 Cardinality, Density, and Completeness
* **Number Sets Hierarchy:** $\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$
* **Cardinality:** $\mathbb{N}, \mathbb{Z}, \mathbb{Q}$ are countable ($|\mathbb{N}| = \aleph_0$). $\mathbb{R}$ is uncountable ($|\mathbb{R}| = \mathfrak{c} = 2^{\aleph_0}$).
* **Density:** Between any two real numbers $a < b$, there exist infinitely many rational and irrational numbers:

$$\forall a, b \in \mathbb{R} \text{ with } a < b, \quad \exists q \in \mathbb{Q}, \, \exists r \in \mathbb{R} \setminus \mathbb{Q} : a < q < b \land a < r < b$$

* **Completeness Axiom (Dedekind):** Every non-empty subset $A \subset \mathbb{R}$ bounded above has a least upper bound ($\sup A \in \mathbb{R}$).

---

## 2. Bounds, Extremums, Supremum, and Infimum

Let $A \subseteq \mathbb{R}$ be a non-empty set:

* **Bounded Above:** $\exists M \in \mathbb{R} : \forall x \in A, \, x \le M$ ($M$ is an upper bound / maggiorante)
* **Bounded Below:** $\exists m \in \mathbb{R} : \forall x \in A, \, x \ge m$ ($m$ is a lower bound / minorante)
* **Bounded Set:** Bounded both above and below.

### Epsilon Characterization

**Supremum ($L = \sup A$):**

$$L = \sup A \iff \begin{cases} \forall x \in A, & x \le L \\ \forall \varepsilon > 0, \, \exists x \in A : & x > L - \varepsilon \end{cases}$$

**Infimum ($l = \inf A$):**

$$l = \inf A \iff \begin{cases} \forall x \in A, & x \ge l \\ \forall \varepsilon > 0, \, \exists x \in A : & x < l + \varepsilon \end{cases}$$

* **Maximum ($\max A$):** If $\sup A \in A \implies \max A = \sup A$
* **Minimum ($\min A$):** If $\inf A \in A \implies \min A = \inf A$

---

## 3. Topology of the Real Line

### 3.1 Intervals
* **Bounded:** Open $(a, b)$, Closed $[a, b]$, Half-open $[a, b)$ or $(a, b]$
* **Unbounded:** $(-\infty, b)$, $[a, +\infty)$, $(-\infty, +\infty) = \mathbb{R}$

### 3.2 Neighborhoods (Intorni)
* **Spherical Open Neighborhood (Radius $r > 0$ centered at $x_0$):**

$$I_r(x_0) = (x_0 - r, x_0 + r) = \{x \in \mathbb{R} : |x - x_0| < r\}$$

* **Punctured Neighborhood (Intorno Bucato):**

$$\dot{I}_r(x_0) = I_r(x_0) \setminus \{x_0\} = \{x \in \mathbb{R} : 0 < |x - x_0| < r\}$$

### 3.3 Point Classifications
Let $A \subseteq \mathbb{R}$ and $x_0 \in \mathbb{R}$:
* **Interior Point (Punto Interno):** $\exists r > 0 : I_r(x_0) \subseteq A$
* **Accumulation Point (Punto di Accumulazione):** $\forall r > 0, \, \dot{I}_r(x_0) \cap A \neq \emptyset$
* **Isolated Point (Punto Isolato):** $x_0 \in A$ and $\exists r > 0 : I_r(x_0) \cap A = \{x_0\}$

---

## 4. Mathematical Induction and Bernoulli's Inequality

### 4.1 Principle of Mathematical Induction
To prove that $P(n)$ holds $\forall n \ge n_0$ ($n, n_0 \in \mathbb{N}$):
1. **Base Step:** Verify that $P(n_0)$ is true.
2. **Inductive Step:** Prove $P(k) \implies P(k+1)$ for $k \ge n_0$.

### 4.2 Bernoulli's Inequality

$$\forall x \ge -1, \quad \forall n \in \mathbb{N} \implies (1 + x)^n \ge 1 + nx$$

---

## 5. Special Products and Binomial Theorem

* **Difference of Squares:** $a^2 - b^2 = (a - b)(a + b)$
* **Square of Binomial:** $(a \pm b)^2 = a^2 \pm 2ab + b^2$
* **Square of Trinomial:** $(a + b + c)^2 = a^2 + b^2 + c^2 + 2ab + 2ac + 2bc$
* **Cubes:**
  * $(a \pm b)^3 = a^3 \pm 3a^2b + 3ab^2 \pm b^3$
  * $a^3 \pm b^3 = (a \pm b)(a^2 \mp ab + b^2)$
* **Difference of $n$-th Powers:**

$$a^n - b^n = (a - b)(a^{n-1} + a^{n-2}b + \dots + ab^{n-2} + b^{n-1})$$

* **Binomial Theorem:**

$$(a + b)^n = \sum_{k=0}^n \binom{n}{k} a^{n-k} b^k, \quad \text{where } \binom{n}{k} = \frac{n!}{k!(n-k)!}$$

---

## 6. Powers, Exponentials, and Logarithms

### 6.1 Exponent Properties ($a, b > 0$)

$$x^a \cdot x^b = x^{a+b}, \quad \frac{x^a}{x^b} = x^{a-b}, \quad (x^a)^b = x^{ab}, \quad x^{-a} = \frac{1}{x^a}, \quad x^{p/q} = \sqrt[q]{x^p}$$

### 6.2 Logarithm Properties ($x, y > 0, \, a > 0, \, a \neq 1$)

$$\log_a(x) = y \iff a^y = x$$

* **Product Rule:** $\ln(x \cdot y) = \ln(x) + \ln(y)$
* **Quotient Rule:** $\ln\left(\frac{x}{y}\right) = \ln(x) - \ln(y)$
* **Power Rule:** $\ln(x^k) = k \ln(x)$
* **Change of Base:** $\log_a(x) = \frac{\ln(x)}{\ln(a)}$

---

## 7. Functions: Properties, Monotonicity, and Compositions

Let $f: X \to Y$ be a real-valued function ($X, Y \subseteq \mathbb{R}$).

### 7.1 Basic Properties
* **Domain ($\text{dom}(f)$):** The set of all real numbers for which $f(x)$ is mathematically defined.
* **Even Function:** $f(-x) = f(x)$ (Symmetric with respect to the $y$-axis).
* **Odd Function:** $f(-x) = -f(x)$ (Symmetric with respect to the origin).
* **Periodic Function:** $\exists T > 0 : f(x + T) = f(x), \, \forall x \in X$.

### 7.2 Injectivity, Surjectivity, and Bijectivity
* **Injective (One-to-One):** $f(x_1) = f(x_2) \implies x_1 = x_2$
* **Surjective (Onto):** $\forall y \in Y, \, \exists x \in X : f(x) = y$
* **Bijective:** Invertible ($f^{-1}: Y \to X$)

### 7.3 Monotonicity
Let $I \subseteq X$ be an interval:
* **Strictly Increasing:** $\forall x_1, x_2 \in I, \, x_1 < x_2 \implies f(x_1) < f(x_2)$
* **Strictly Decreasing:** $\forall x_1, x_2 \in I, \, x_1 < x_2 \implies f(x_1) > f(x_2)$
* *Property:* Every strictly monotonic function is **injective**.

### 7.4 Operations and Compositions
* **Linear Combination:** $(af + bg)(x) = af(x) + bg(x)$
* **Product and Quotient:**

$$(f \cdot g)(x) = f(x)g(x), \quad \left(\frac{f}{g}\right)(x) = \frac{f(x)}{g(x)} \quad (g(x) \neq 0)$$

* **Generalized Exponential Base:**

$$[f(x)]^{g(x)} = e^{g(x)\ln(f(x))} \quad (\text{defined for } f(x) > 0)$$

* **Function Composition:**

$$(f \circ g)(x) = f(g(x)) \quad \text{with } \text{dom}(f \circ g) = \{x \in \text{dom}(g) : g(x) \in \text{dom}(f)\}$$

---

[Back to Main README](../README.md)

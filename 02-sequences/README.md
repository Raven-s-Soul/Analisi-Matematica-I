# 02. Pre-Calculus, Trigonometry & Sequences

This directory combines essential trigonometric tools, algebraic pre-calculus methods, and the formal study of real sequences $(a_n)_{n \in \mathbb{N}}$ with fundamental convergence theorems.

---

## Table of Contents

### Part I: Pre-Calculus & Trigonometry
1. [Angles and Fundamental Functions](#1-angles-and-fundamental-functions)
2. [Fundamental Pythagorean Identities](#2-fundamental-pythagorean-identities)
3. [Angle Addition, Subtraction, and Double-Angle](#3-angle-addition-subtraction-and-double-angle)
4. [Linearization and Half-Angle Formulas](#4-linearization-and-half-angle-formulas)
5. [Universal Parametric Substitution](#5-universal-parametric-substitution)
6. [Harmonic Addition, Prosthaphaeresis, and Werner](#6-harmonic-addition-prosthaphaeresis-and-werner)
7. [Geometry and Triangle Theorems](#7-geometry-and-triangle-theorems)

### Part II: Sequences of Real Numbers
8. [Definition of Sequence Limits](#8-definition-of-sequence-limits)
9. [Fundamental Convergence Theorems](#9-fundamental-convergence-theorems)
10. [Hierarchy of Growth Rates and Indeterminate Forms](#10-hierarchy-of-growth-rates-and-indeterminate-forms)
11. [Notable Sequence Limits and Euler's Number](#11-notable-sequence-limits-and-eulers-number)
12. [Recursive Sequences and Stirling's Approximation](#12-recursive-sequences-and-stirlings-approximation)

---

# Part I: Pre-Calculus & Trigonometry

## 1. Angles and Fundamental Functions

* **Angle Conversion:** $180^\circ = \pi \text{ rad} \implies \alpha_{\text{rad}} = \alpha_{\text{deg}} \cdot \frac{\pi}{180}$
* **Definitions on the Unit Circle ($x^2 + y^2 = 1$):**
  * $\cos(\alpha) = x$-coordinate
  * $\sin(\alpha) = y$-coordinate
* **Reciprocal and Ratio Functions:**

$$\tan(x) = \frac{\sin(x)}{\cos(x)}, \quad \cot(x) = \frac{\cos(x)}{\sin(x)} = \frac{1}{\tan(x)}$$

$$\sec(x) = \frac{1}{\cos(x)}, \quad \csc(x) = \frac{1}{\sin(x)}$$

---

## 2. Fundamental Pythagorean Identities

$$\sin^2(x) + \cos^2(x) = 1$$

$$1 + \tan^2(x) = \sec^2(x) = \frac{1}{\cos^2(x)}$$

$$1 + \cot^2(x) = \csc^2(x) = \frac{1}{\sin^2(x)}$$

---

## 3. Angle Addition, Subtraction, and Double-Angle

### 3.1 Addition and Subtraction
* **Sine:** $\sin(\alpha \pm \beta) = \sin(\alpha)\cos(\beta) \pm \cos(\alpha)\sin(\beta)$
* **Cosine:** $\cos(\alpha \pm \beta) = \cos(\alpha)\cos(\beta) \mp \sin(\alpha)\sin(\beta)$
* **Tangent:** $\tan(\alpha \pm \beta) = \frac{\tan(\alpha) \pm \tan(\beta)}{1 \mp \tan(\alpha)\tan(\beta)}$

### 3.2 Double-Angle Formulas

$$\sin(2x) = 2\sin(x)\cos(x)$$

$$\cos(2x) = \cos^2(x) - \sin^2(x) = 2\cos^2(x) - 1 = 1 - 2\sin^2(x)$$

$$\tan(2x) = \frac{2\tan(x)}{1 - \tan^2(x)}$$

---

## 4. Linearization and Half-Angle Formulas

### 4.1 Linearization (Power Reduction)
Essential for integrating powers of trigonometric functions:

$$\sin^2(x) = \frac{1 - \cos(2x)}{2}, \quad \cos^2(x) = \frac{1 + \cos(2x)}{2}$$

### 4.2 Half-Angle Formulas

$$\sin\left(\frac{x}{2}\right) = \pm\sqrt{\frac{1 - \cos(x)}{2}}, \quad \cos\left(\frac{x}{2}\right) = \pm\sqrt{\frac{1 + \cos(x)}{2}}, \quad \tan\left(\frac{x}{2}\right) = \frac{1 - \cos(x)}{\sin(x)} = \frac{\sin(x)}{1 + \cos(x)}$$

---

## 5. Universal Parametric Substitution

Used to convert trigonometric expressions into rational algebraic functions using $t = \tan(x/2)$:

$$\sin(x) = \frac{2t}{1 + t^2}, \quad \cos(x) = \frac{1 - t^2}{1 + t^2}, \quad \tan(x) = \frac{2t}{1 - t^2}, \quad dx = \frac{2}{1 + t^2} \, dt$$

---

## 6. Harmonic Addition, Prosthaphaeresis, and Werner

### 6.1 Harmonic Addition Form (Metodo dell'Angolo Aggiunto)
To combine $a\sin(x) + b\cos(x)$ into a single sinusoidal wave:

$$a\sin(x) + b\cos(x) = R\sin(x + \varphi)$$

$$\text{where } R = \sqrt{a^2 + b^2}, \quad \cos(\varphi) = \frac{a}{R}, \quad \sin(\varphi) = \frac{b}{R}$$

### 6.2 Prosthaphaeresis (Sum-to-Product)

$$\sin(p) \pm \sin(q) = 2\sin\left(\frac{p \pm q}{2}\right)\cos\left(\frac{p \mp q}{2}\right)$$

$$\cos(p) + \cos(q) = 2\cos\left(\frac{p + q}{2}\right)\cos\left(\frac{p - q}{2}\right)$$

$$\cos(p) - \cos(q) = -2\sin\left(\frac{p + q}{2}\right)\sin\left(\frac{p - q}{2}\right)$$

### 6.3 Werner (Product-to-Sum)

$$\sin(\alpha)\cos(\beta) = \frac{1}{2}[\sin(\alpha + \beta) + \sin(\alpha - \beta)]$$

$$\cos(\alpha)\cos(\beta) = \frac{1}{2}[\cos(\alpha + \beta) + \cos(\alpha - \beta)]$$

$$\sin(\alpha)\sin(\beta) = \frac{1}{2}[\cos(\alpha - \beta) - \cos(\alpha + \beta)]$$

---

## 7. Geometry and Triangle Theorems

* **Triangle Angle Sum:** $\alpha + \beta + \gamma = 180^\circ = \pi \text{ rad}$
* **Law of Sines:**

$$\frac{a}{\sin(\alpha)} = \frac{b}{\sin(\beta)} = \frac{c}{\sin(\gamma)} = 2R$$

---

# Part II: Sequences of Real Numbers

## 8. Definition of Sequence Limits

A sequence is a function $a: \mathbb{N} \to \mathbb{R}$, denoted as $(a_n)_{n \in \mathbb{N}}$.

* **Finite Limit ($L \in \mathbb{R}$):**

$$\lim_{n \to \infty} a_n = L \iff \forall \varepsilon > 0, \, \exists N \in \mathbb{N} : \forall n > N, \, |a_n - L| < \varepsilon$$

* **Divergent to $+\infty$:**

$$\lim_{n \to \infty} a_n = +\infty \iff \forall M > 0, \, \exists N \in \mathbb{N} : \forall n > N, \, a_n > M$$

* **Divergent to $-\infty$:**

$$\lim_{n \to \infty} a_n = -\infty \iff \forall M > 0, \, \exists N \in \mathbb{N} : \forall n > N, \, a_n < -M$$

---

## 9. Fundamental Convergence Theorems

* **Uniqueness:** If a sequence converges, its limit is unique.
* **Sign Permanence:** If $\lim a_n = L > 0 \implies \exists N : \forall n > N, \, a_n > 0$.
* **Squeeze Theorem (Carabinieri):**

$$\text{If } a_n \le b_n \le c_n \text{ and } \lim_{n \to \infty} a_n = \lim_{n \to \infty} c_n = L \implies \lim_{n \to \infty} b_n = L$$

* **Bounded $\times$ Infinitesimal:**

$$\text{If } |a_n| \le M \text{ and } \lim_{n \to \infty} b_n = 0 \implies \lim_{n \to \infty} (a_n \cdot b_n) = 0$$

* **Monotone Convergence Theorem:** Every bounded monotone sequence converges:

$$\text{Increasing and bounded above} \implies \lim_{n \to \infty} a_n = \sup\{a_n\}$$

$$\text{Decreasing and bounded below} \implies \lim_{n \to \infty} a_n = \inf\{a_n\}$$

---

## 10. Hierarchy of Growth Rates and Indeterminate Forms

### 10.1 Hierarchy Scale (as $n \to \infty$)

$$\ln(n) \ll n^a \ll b^n \ll n! \ll n^n \quad (\text{where } a > 0, \, b > 1)$$

### 10.2 Fundamental Growth Ratios

$$\lim_{n \to \infty} \frac{\ln(n)}{n^a} = 0, \quad \lim_{n \to \infty} \frac{n^a}{b^n} = 0, \quad \lim_{n \to \infty} \frac{b^n}{n!} = 0, \quad \lim_{n \to \infty} \frac{n!}{n^n} = 0$$

### 10.3 Indeterminate Forms

$$\left[ \frac{0}{0} \right], \quad \left[ \frac{\infty}{\infty} \right], \quad [0 \cdot \infty], \quad [+\infty - \infty], \quad [1^\infty], \quad [0^0], \quad [\infty^0]$$

---

## 11. Notable Sequence Limits and Euler's Number

* **Euler's Constant:**

$$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n$$

* **Generalized Power:**

$$\lim_{n \to \infty} \left(1 + \frac{a}{n}\right)^{b n} = e^{a b} \quad (\forall a, b \in \mathbb{R})$$

* **Geometric Limit:**

$$\lim_{n \to \infty} q^n = \begin{cases} 0 & \text{if } |q| < 1 \\ 1 & \text{if } q = 1 \\ +\infty & \text{if } q > 1 \\ \text{undefined} & \text{if } q \le -1 \end{cases}$$

* **Standard Roots:**

$$\lim_{n \to \infty} \sqrt[n]{n} = 1, \quad \lim_{n \to \infty} \sqrt[n]{c} = 1 \quad (c > 0)$$

---

## 12. Recursive Sequences and Stirling's Approximation

### 12.1 Recursive Sequences ( $a_{n+1} = f(a_n)$ )
1. **Candidate Limits:** Find solutions to the fixed-point equation $L = f(L)$.
2. **Bounds by Induction:** Verify that $a_n \ge m$ or $a_n \le M, \, \forall n \in \mathbb{N}$.
3. **Monotonicity:** Test $a_{n+1} - a_n = f(a_n) - a_n \ge 0$ (or $\le 0$).
4. **Conclusion:** Apply the Monotone Convergence Theorem to confirm $\lim a_n = L$.

### 12.2 Stirling's Approximation
Used for computing limits with factorials as $n \to \infty$:

$$n! \sim \sqrt{2\pi n} \left(\frac{n}{e}\right)^n$$

---

[Back to Main README](../README.md)

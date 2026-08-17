# 06. Numerical Series

Infinite numerical series analysis, sum properties, classic reference series (Geometric, Harmonic, Telescopic), necessary convergence conditions, and convergence tests for positive and alternating series.

---

## Table of Contents

1. [Definitions and Sum Properties](#1-definitions-and-sum-properties)
2. [Necessary Condition for Convergence](#2-necessary-condition-for-convergence)
3. [Reference and Notable Series](#3-reference-and-notable-series)
4. [Convergence Tests for Non-Negative Series](#4-convergence-tests-for-non-negative-series)
5. [Alternating Series and Absolute Convergence](#5-alternating-series-and-absolute-convergence)

---

## 1. Definitions and Sum Properties

Given a sequence of real numbers $(a_n)_{n \in \mathbb{N}}$, the sequence of partial sums $(S_k)$ is defined as:

$$S_k = \sum_{n=0}^k a_n = a_0 + a_1 + a_2 + \dots + a_k$$

The infinite numerical series is the limit of its partial sums as $k \to \infty$:

$$\sum_{n=0}^\infty a_n = \lim_{k \to \infty} S_k$$

* **Convergent:** $\lim_{k \to \infty} S_k = S \in \mathbb{R}$ ($S$ is the sum of the series).
* **Divergent:** $\lim_{k \to \infty} S_k = \pm\infty$.
* **Indeterminate / Oscillating:** The limit of partial sums does not exist.

### 1.1 Linearity of Series
If $\sum a_n = A$ and $\sum b_n = B$ are convergent series, then $\forall \alpha, \beta \in \mathbb{R}$:

$$\sum_{n=0}^\infty (\alpha a_n + \beta b_n) = \alpha \sum_{n=0}^\infty a_n + \beta \sum_{n=0}^\infty b_n = \alpha A + \beta B$$

---

## 2. Necessary Condition for Convergence

* **Test for Divergence (TFD):**

$$\text{If } \sum_{n=0}^\infty a_n \text{ converges} \implies \lim_{n \to \infty} a_n = 0$$

* **Divergence Criterion:** If $\lim_{n \to \infty} a_n \neq 0$ (or does not exist), then the series **diverges**.
* *Note:* $\lim_{n \to \infty} a_n = 0$ is a **necessary but not sufficient** condition for convergence (e.g., the harmonic series).

---

## 3. Reference and Notable Series

### 3.1 Geometric Series

$$\sum_{n=0}^\infty q^n = \begin{cases} \frac{1}{1 - q} & \text{if } |q| < 1 \quad (\text{Converges}) \\ +\infty & \text{if } q \ge 1 \quad (\text{Diverges}) \\ \text{oscillating} & \text{if } q \le -1 \quad (\text{Indeterminate}) \end{cases}$$

### 3.2 Harmonic and Generalized $p$-Series

$$\sum_{n=1}^\infty \frac{1}{n^p} \quad \begin{cases} \text{Converges} & \text{if } p > 1 \\ \text{Diverges to } +\infty & \text{if } p \le 1 \end{cases}$$

* **Standard Harmonic Series ($p = 1$):** $\sum_{n=1}^\infty \frac{1}{n} = +\infty$.

### 3.3 Generalized Harmonic Series with Logarithms

$$\sum_{n=2}^\infty \frac{1}{n^p [\ln(n)]^q} \quad \begin{cases} \text{Converges} & \text{if } p > 1, \, \forall q \\ \text{Converges} & \text{if } p = 1 \text{ and } q > 1 \\ \text{Diverges} & \text{if } p < 1 \text{ or } (p = 1 \text{ and } q \le 1) \end{cases}$$

### 3.4 Telescoping Series (Mengoli Series)
A series where terms cancel out in adjacent pairs: $a_n = b_n - b_{n+1}$:

$$S_k = \sum_{n=1}^k (b_n - b_{n+1}) = b_1 - b_{k+1} \implies \sum_{n=1}^\infty a_n = b_1 - \lim_{k \to \infty} b_{k+1}$$

* **Classic Example (Mengoli):**

$$\sum_{n=1}^\infty \frac{1}{n(n+1)} = \sum_{n=1}^\infty \left( \frac{1}{n} - \frac{1}{n+1} \right) = 1 - \lim_{k \to \infty} \frac{1}{k+1} = 1$$

---

## 4. Convergence Tests for Non-Negative Series 
> ($a_n \ge 0$)
### 4.1 Direct Comparison Test (Criterio del Confronto)
Let $0 \le a_n \le b_n$ for all $n \ge n_0$:
* If $\sum b_n$ converges $\implies \sum a_n$ converges.
* If $\sum a_n$ diverges $\implies \sum b_n$ diverges.

### 4.2 Asymptotic Comparison Test (Criterio del Confronto Asintotico)
Let $a_n > 0, b_n > 0$. If $\lim_{n \to \infty} \frac{a_n}{b_n} = L \in (0, +\infty)$:

$$\sum a_n \text{ and } \sum b_n \text{ have the exact same convergence behavior (both converge or both diverge)}$$

* If $L = 0$ and $\sum b_n$ converges $\implies \sum a_n$ converges.
* If $L = +\infty$ and $\sum b_n$ diverges $\implies \sum a_n$ diverges.

### 4.3 Ratio Test (Criterio del Rapporto / D'Alembert)
Let $a_n > 0$, and assume the limit exists:

$$\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = L$$

* **$L < 1$:** The series **converges**.
* **$L > 1$:** The series **diverges**.
* **$L = 1$:** The test is **inconclusive** (use comparison or integral tests).

### 4.4 Root Test (Criterio della Radice / Cauchy)
Let $a_n \ge 0$, and assume the limit exists:

$$\lim_{n \to \infty} \sqrt[n]{a_n} = L$$

* **$L < 1$:** The series **converges**.
* **$L > 1$:** The series **diverges**.
* **$L = 1$:** The test is **inconclusive**.

### 4.5 Integral Test (Criterio Integrale)
Let $f: [1, +\infty) \to [0, +\infty)$ be a continuous, positive, and monotonically decreasing function such that $f(n) = a_n$:

$$\sum_{n=1}^\infty a_n \text{ converges} \iff \int_1^{+\infty} f(x) \, dx \text{ converges}$$

---

## 5. Alternating Series and Absolute Convergence

### 5.1 Absolute Convergence
A series $\sum a_n$ is **absolutely convergent** if the series of absolute values converges:

$$\sum_{n=0}^\infty |a_n| < +\infty \implies \sum_{n=0}^\infty a_n \text{ converges}$$

* *Note:* Absolute convergence implies simple convergence, but the converse is not generally true.

### 5.2 Leibniz's Test for Alternating Series
An alternating series $\sum_{n=0}^\infty (-1)^n b_n$ with $b_n \ge 0$ converges if:
1. **Monotonically Decreasing:** $b_{n+1} \le b_n, \, \forall n \ge n_0$
2. **Infinitesimal:** $\lim_{n \to \infty} b_n = 0$

* **Error Estimate for Alternating Series:**

$$|S - S_k| \le b_{k+1}$$

---

[Back to Main README](../README.md)

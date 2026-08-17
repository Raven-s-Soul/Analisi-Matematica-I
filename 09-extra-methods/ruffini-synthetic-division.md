# Synthetic Division (Ruffini's Rule)

A fast algorithmic method to divide, evaluate, and factor polynomials when dividing by a linear binomial of the form $(x - r)$ or $(ax - b)$.

---

## Table of Contents

1. [The Remainder and Factor Theorem](#1-the-remainder-and-factor-theorem)
2. [Finding Candidate Roots (Rational Root Theorem)](#2-finding-candidate-roots-rational-root-theorem)
3. [Step-by-Step Worked Example](#3-step-by-step-worked-example)
4. [Ruffini Tableau](#4-ruffini-tableau)
5. [Dividing by (ax - b) with a != 1](#5-dividing-by-ax---b-with-a--1)

---

## 1. The Remainder and Factor Theorem

Let $P(x)$ be a polynomial of degree $n \ge 1$:
* **Remainder Theorem:** The remainder of the division of $P(x)$ by $(x - r)$ is equal to $P(r)$.
* **Factor Theorem:** If $P(r) = 0$, then $r$ is a root of $P(x)$, and $(x - r)$ divides $P(x)$ with zero remainder:

$$P(x) = (x - r) Q(x)$$

Where $\deg(Q) = \deg(P) - 1$.

---

## 2. Finding Candidate Roots (Rational Root Theorem)

For a polynomial with integer coefficients:

$$P(x) = a_n x^n + a_{n-1} x^{n-1} + \dots + a_1 x + a_0$$

Every rational root $r = \frac{p}{q}$ (in lowest terms) satisfies:
* $p$ is an integer divisor of the constant term $a_0$.
* $q$ is an integer divisor of the leading coefficient $a_n$.

* **Monic Polynomials ($a_n = 1$):** Candidate roots are simply the integer divisors of $a_0$:

$$\text{Candidates } r \in \{ \text{divisors of } a_0 \}$$

---

## 3. Step-by-Step Worked Example

Factorize the polynomial:

$$P(x) = x^3 - 4x^2 + x + 6$$

### Step 1: List Candidate Roots
The constant term is $a_0 = 6$. Its integer divisors are:

$$\text{Candidates } r \in \{\pm 1, \pm 2, \pm 3, \pm 6\}$$

### Step 2: Test Candidates
* $P(1) = (1)^3 - 4(1)^2 + (1) + 6 = 4 \neq 0$
* $P(-1) = (-1)^3 - 4(-1)^2 + (-1) + 6 = -1 - 4 - 1 + 6 = 0 \implies r = -1 \text{ is a root}$
* $P(2) = (2)^3 - 4(2)^2 + (2) + 6 = 8 - 16 + 2 + 6 = 0 \implies r = 2 \text{ is a root}$

---

## 4. Ruffini Tableau

Using root $r = 2$ on the coefficient array $[1, -4, 1, 6]$:

| | $x^3$ | $x^2$ | $x^1$ | Constant |
| :---: | :---: | :---: | :---: | :---: |
| | **1** | **-4** | **1** | **6** |
| **r = 2** | | 2 | -4 | -6 |
| | **1** ($x^2$) | **-2** ($x$) | **-3** (const) | **0** (Remainder) |

### Execution Steps:
1. Bring down the leading coefficient ($1$).
2. Multiply $1 \times 2 = 2$, place it below $-4$, and add: $-4 + 2 = -2$.
3. Multiply $-2 \times 2 = -4$, place it below $1$, and add: $1 + (-4) = -3$.
4. Multiply $-3 \times 2 = -6$, place it below $6$, and add: $6 + (-6) = 0$ (Remainder).

### Resulting Quotient Polynomial:

$$Q(x) = x^2 - 2x - 3$$

Factorizing the remaining quadratic quotient:

$$x^2 - 2x - 3 = (x - 3)(x + 1)$$

### Complete Factorization:

$$P(x) = (x - 2)(x^2 - 2x - 3) = (x - 2)(x - 3)(x + 1)$$

---

## 5. Dividing by (ax - b) with a != 1

When dividing $P(x)$ by $(ax - b)$, rewrite the divisor as $a\left(x - \frac{b}{a}\right)$:

1. Perform synthetic division using root $r = \frac{b}{a}$.
2. Divide the resulting quotient coefficients by $a$:

$$P(x) = (ax - b) \cdot \left(\frac{Q(x)}{a}\right) + R$$

---

[Back to Extra Methods](./) | [Back to Main README](../README.md)

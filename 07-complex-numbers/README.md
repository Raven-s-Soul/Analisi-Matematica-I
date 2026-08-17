# 07. Complex Numbers

Algebraic structures, geometric representation on the Argand-Gauss plane, polar and exponential notations, Euler's formulas, De Moivre's theorem, n-th complex roots, and complex polynomials with real coefficients.

---

## Table of Contents

1. [Definition and the Argand-Gauss Plane](#1-definition-and-the-argand-gauss-plane)
2. [Algebraic Form, Conjugate, and Modulus](#2-algebraic-form-conjugate-and-modulus)
3. [Trigonometric and Polar Representation](#3-trigonometric-and-polar-representation)
4. [Exponential Form and Euler's Formulas](#4-exponential-form-and-eulers-formulas)
5. [Powers of Complex Numbers and De Moivre's Formula](#5-powers-of-complex-numbers-and-de-moivres-formula)
6. [n-th Roots of Complex Numbers](#6-n-th-roots-of-complex-numbers)
7. [Polynomials in the Complex Domain and Real Coefficients](#7-polynomials-in-the-complex-domain-and-real-coefficients)

---

## 1. Definition and the Argand-Gauss Plane

The set of complex numbers $\mathbb{C}$ consists of pairs $(a, b) \in \mathbb{R}^2$ with an imaginary unit $i$ satisfying:

$$i^2 = -1 \implies i = \sqrt{-1}$$

### 1.1 The Argand-Gauss Plane
Every complex number $z = a + ib$ is represented as a point $(a, b)$ in the Cartesian plane:
* Real Axis ($\text{Re}$): The horizontal axis representing $\text{Re}(z) = a$.
* Imaginary Axis ($\text{Im}$): The vertical axis representing $\text{Im}(z) = b$.

---

## 2. Algebraic Form, Conjugate, and Modulus

### 2.1 Algebraic Representation
Every $z \in \mathbb{C}$ is written as:

$$z = a + ib \quad (a, b \in \mathbb{R})$$

* Real Part: $\text{Re}(z) = a = \frac{z + \bar{z}}{2}$
* Imaginary Part: $\text{Im}(z) = b = \frac{z - \bar{z}}{2i}$

### 2.2 Complex Conjugate
The complex conjugate of $z = a + ib$ is:

$$\bar{z} = a - ib$$

Properties:
* $\overline{z_1 \pm z_2} = \bar{z}_1 \pm \bar{z}_2$
* $\overline{z_1 \cdot z_2} = \bar{z}_1 \cdot \bar{z}_2$
* $\overline{(z_1 / z_2)} = \bar{z}_1 / \bar{z}_2 \quad (z_2 \neq 0)$
* $\overline{(\bar{z})} = z$
* $z \in \mathbb{R} \iff z = \bar{z}$
* $z \in i\mathbb{R} \iff z = -\bar{z}$

### 2.3 Modulus
The modulus of $z = a + ib$ represents distance from the origin:

$$|z| = \sqrt{a^2 + b^2} = \sqrt{z \bar{z}}$$

Properties:
* $|z| \ge 0$, and $|z| = 0 \iff z = 0$
* $|z| = |\bar{z}| = |-z|$
* $|z_1 \cdot z_2| = |z_1| \cdot |z_2|$
* $|z_1 / z_2| = |z_1| / |z_2| \quad (z_2 \neq 0)$
* Triangle Inequality: $|z_1 + z_2| \le |z_1| + |z_2|$

### 2.4 Multiplicative Inverse
For $z \neq 0$:

$$\frac{1}{z} = \frac{\bar{z}}{|z|^2} = \frac{a - ib}{a^2 + b^2} = \frac{a}{a^2 + b^2} - i \frac{b}{a^2 + b^2}$$

---

## 3. Trigonometric and Polar Representation

Converting Cartesian coordinates $(a, b)$ to polar coordinates $(r, \theta)$:

$$z = r(\cos\theta + i\sin\theta)$$

Where:
* Modulus: $r = |z| = \sqrt{a^2 + b^2} \ge 0$
* Argument ($\theta = \arg(z)$):

$$\theta = \begin{cases} \arctan(b/a) & \text{if } a > 0 \\ \arctan(b/a) + \pi & \text{if } a < 0 \land b \ge 0 \\ \arctan(b/a) - \pi & \text{if } a < 0 \land b < 0 \\ +\pi/2 & \text{if } a = 0 \land b > 0 \\ -\pi/2 & \text{if } a = 0 \land b < 0 \end{cases}$$

### 3.1 Polar Operations
* Product:

$$z_1 \cdot z_2 = r_1 r_2 [\cos(\theta_1 + \theta_2) + i\sin(\theta_1 + \theta_2)]$$

* Quotient:

$$\frac{z_1}{z_2} = \frac{r_1}{r_2} [\cos(\theta_1 - \theta_2) + i\sin(\theta_1 - \theta_2)]$$

---

## 4. Exponential Form and Euler's Formulas

### 4.1 Euler's Formula

$$e^{i\theta} = \cos\theta + i\sin\theta$$

* Exponential Representation:

$$z = r e^{i\theta} \quad (r = |z|, \, \theta = \arg(z))$$

* Euler's Identity ($\theta = \pi$):

$$e^{i\pi} + 1 = 0$$

### 4.2 Sine and Cosine via Exponentials

$$\cos\theta = \frac{e^{i\theta} + e^{-i\theta}}{2}$$

$$\sin\theta = \frac{e^{i\theta} - e^{-i\theta}}{2i}$$

---

## 5. Powers of Complex Numbers and De Moivre's Formula

### 5.1 De Moivre's Formula
For any integer $n \in \mathbb{Z}$:

$$(\cos\theta + i\sin\theta)^n = \cos(n\theta) + i\sin(n\theta)$$

### 5.2 Powers in Exponential Form

$$z^n = (r e^{i\theta})^n = r^n e^{i n\theta} = r^n [\cos(n\theta) + i\sin(n\theta)]$$

---

## 6. n-th Roots of Complex Numbers

For $z = r e^{i\theta} \neq 0$ and an integer $n \ge 1$, the equation $w^n = z$ has $n$ distinct roots $w_0, w_1, \dots, w_{n-1}$:

$$w_k = \sqrt[n]{r} \left[ \cos\left(\frac{\theta + 2k\pi}{n}\right) + i\sin\left(\frac{\theta + 2k\pi}{n}\right) \right], \quad k = 0, 1, \dots, n-1$$

### 6.1 Geometric Properties
* The $n$ roots lie on a circle centered at the origin with radius $R = \sqrt[n]{r}$.
* The roots form the vertices of a regular $n$-sided polygon.
* The sum of all $n$-th roots is zero:

$$\sum_{k=0}^{n-1} w_k = 0$$

---

## 7. Polynomials in the Complex Domain and Real Coefficients

### 7.1 Fundamental Theorem of Algebra
Every non-constant polynomial $P(z) = a_n z^n + \dots + a_0 \in \mathbb{C}[z]$ ($a_n \neq 0$) has exactly $n$ complex roots counted with multiplicity:

$$P(z) = a_n (z - z_1)^{m_1} \dots (z - z_k)^{m_k}, \quad \sum_{j=1}^k m_j = n$$

### 7.2 Polynomials with Real Coefficients ($a_i \in \mathbb{R}$)
* Conjugate Root Theorem: If $z_0 \in \mathbb{C}$ is a root of $P(z) = 0$, its conjugate $\bar{z}_0$ is also a root with the same multiplicity.
* Quadratic Factorization:

$$(z - z_0)(z - \bar{z}_0) = z^2 - 2\text{Re}(z_0)z + |z_0|^2 \in \mathbb{R}[z]$$

---

[Back to Main README](../README.md)

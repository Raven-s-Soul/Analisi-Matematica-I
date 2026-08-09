# 04. Differential Calculus

Derivatives, differential theorems, curve sketching, and polynomial approximations.

---

## 📌 Key Topics & Formulas

### 1. Definition of Derivative
$$f'(x_0) = \lim_{h \to 0} \frac{f(x_0 + h) - f(x_0)}{h}$$

### 2. Core Differential Theorems
* **Fermat's Theorem:** If $x_0$ is a local extremum and $f$ is differentiable at $x_0$, then $f'(x_0) = 0$.
* **Rolle's Theorem:** $f$ continuous on $[a,b]$, differentiable on $(a,b)$, $f(a) = f(b) \implies \exists c \in (a,b) : f'(c) = 0$.
* **Mean Value Theorem (Lagrange):** $\exists c \in (a,b) : f'(c) = \frac{f(b) - f(a)}{b - a}$.
* **L'Hôpital's Rule:** For $\frac{0}{0}$ or $\frac{\infty}{\infty}$, $\lim \frac{f(x)}{g(x)} = \lim \frac{f'(x)}{g'(x)}$.

### 3. Taylor Series Expansion (around $x_0 = 0$, Maclaurin)
$$f(x) = \sum_{k=0}^n \frac{f^{(k)}(0)}{k!} x^k + o(x^n)$$

---

[⬅️ Back to Main README](../README.md)

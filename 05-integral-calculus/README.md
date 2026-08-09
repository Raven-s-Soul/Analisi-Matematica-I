# 05. Integral Calculus

Antiderivatives, integration techniques, Riemann integration, and improper integrals.

---

## 📌 Key Topics & Formulas

### 1. Integration Techniques
* **By Parts:** $\int u \, dv = uv - \int v \, du$
* **Substitution:** $\int f(g(x)) g'(x) \, dx = \int f(u) \, du \quad (u = g(x))$

### 2. Fundamental Theorem of Calculus
If $F(x) = \int_a^x f(t) \, dt$, then $F'(x) = f(x)$ and:
$$\int_a^b f(x) \, dx = F(b) - F(a)$$

### 3. Improper Integrals
* **Unbounded Domain:** $\int_a^\infty f(x) \, dx = \lim_{t \to \infty} \int_a^t f(x) \, dx$
* **p-Integral Convergence:** $\int_1^\infty \frac{1}{x^p} \, dx$ converges $\iff p > 1$.

---

[⬅️ Back to Main README](../README.md)

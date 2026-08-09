# 08. Ordinary Differential Equations (ODEs)

First-order and second-order ordinary differential equations and Initial Value Problems (Cauchy Problem).

---

## 📌 Key Types & Solution Methods

### 1. First-Order Separable
$$y' = g(x)h(y) \implies \int \frac{1}{h(y)} \, dy = \int g(x) \, dx$$

### 2. First-Order Linear
$$y' + a(x)y = b(x) \implies y(x) = e^{-A(x)} \left( \int b(x) e^{A(x)} \, dx + C \right), \quad A(x) = \int a(x) \, dx$$

### 3. Second-Order Linear Homogeneous (Constant Coefficients)
$$ay'' + by' + cy = 0 \implies \text{Characteristic equation: } ar^2 + br + c = 0$$
* $\Delta > 0$: $y(x) = C_1 e^{r_1 x} + C_2 e^{r_2 x}$
* $\Delta = 0$: $y(x) = (C_1 + C_2 x) e^{r x}$
* $\Delta < 0$: $y(x) = e^{\alpha x} (C_1 \cos(\beta x) + C_2 \sin(\beta x)) \quad (r = \alpha \pm i\beta)$

---

[⬅️ Back to Main README](../README.md)

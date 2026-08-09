# 03. Limits of Functions & Continuity

Formal analysis of function limits, asymptotic behavior, and continuity properties on intervals.

---

## 📌 Key Topics & Formulas

### 1. Limit Definition ($\varepsilon - \delta$)
$$\lim_{x \to x_0} f(x) = L \iff \forall \varepsilon > 0, \exists \delta > 0 : 0 < |x - x_0| < \delta \implies |f(x) - L| < \varepsilon$$

### 2. Standard Limits (Notable Limits)
$$\lim_{x \to 0} \frac{\sin x}{x} = 1, \quad \lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}, \quad \lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1, \quad \lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

### 3. Classification of Discontinuities
* **Removable (I Kind / Eliminabile):** $\lim_{x \to x_0} f(x)$ exists but $\neq f(x_0)$.
* **Jump (II Kind / Salto):** Left and right limits exist but are unequal ($\lim_{x \to x_0^-} \neq \lim_{x \to x_0^+}$).
* **Essential (III Kind / Seconda Specie):** At least one one-sided limit is infinite or does not exist.

### 4. Core Theorems on Continuous Functions
* **Weierstrass Theorem:** A continuous function on a closed bounded interval $[a, b]$ attains an absolute maximum and minimum.
* **Intermediate Value Theorem:** A continuous function on $[a, b]$ takes all values between $f(a)$ and $f(b)$.

---

[⬅️ Back to Main README](../README.md)

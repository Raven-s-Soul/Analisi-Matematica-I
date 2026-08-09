# 02. Sequences of Real Numbers

Study of real sequences $(a_n)_{n \in \mathbb{N}}$, limit evaluations as $n \to \infty$, and fundamental convergence theorems.

---

## 📌 Key Topics & Formulas

### 1. Definition of Sequence Limit
$$\lim_{n \to \infty} a_n = L \iff \forall \varepsilon > 0, \exists N \in \mathbb{N} : \forall n > N, |a_n - L| < \varepsilon$$

### 2. Fundamental Theorems
* **Squeeze Theorem (Carabinieri):** If $a_n \le b_n \le c_n$ and $\lim a_n = \lim c_n = L$, then $\lim b_n = L$.
* **Monotone Convergence Theorem:** Every bounded monotone sequence converges.

### 3. Asymptotic Growth Rates (Hierarchy of Infinites)
As $n \to \infty$:
$$\ln(n) \ll n^a \ll b^n \ll n! \ll n^n \quad (a>0, b>1)$$

### 4. Euler's Number
$$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n$$

---

[⬅️ Back to Main README](../README.md)

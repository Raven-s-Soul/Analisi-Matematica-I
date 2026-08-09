# 06. Numerical Series

Infinite series analysis, convergence tests for non-negative series, and alternating series.

---

## 📌 Key Topics & Tests

### 1. Necessary Condition for Convergence
$$\text{If } \sum_{n=1}^\infty a_n \text{ converges} \implies \lim_{n \to \infty} a_n = 0$$

### 2. Notable Series
* **Geometric Series:** $\sum_{n=0}^\infty q^n = \frac{1}{1-q}$ for $|q| < 1$.
* **p-Series (Harmonic):** $\sum_{n=1}^\infty \frac{1}{n^p}$ converges $\iff p > 1$.

### 3. Convergence Tests ($a_n \ge 0$)
* **Ratio Test:** $\lim \frac{a_{n+1}}{a_n} = L \implies L < 1 \text{ (conv)}, L > 1 \text{ (div)}$.
* **Root Test:** $\lim \sqrt[n]{a_n} = L \implies L < 1 \text{ (conv)}, L > 1 \text{ (div)}$.

### 4. Alternating Series (Leibniz Criterion)
For $\sum (-1)^n b_n$ with $b_n \ge 0$:
If $b_n$ is monotonically decreasing and $\lim b_n = 0$, the series converges.

---

[⬅️ Back to Main README](../README.md)

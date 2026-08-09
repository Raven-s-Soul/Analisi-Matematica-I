# Synthetic Division (Ruffini's Rule)

A fast method to divide and factor polynomials when dividing by a linear factor of the form $(x - r)$.

---

## 💡 The Principle

Given a polynomial $P(x)$, if $P(r) = 0$, then $r$ is a root, and $(x - r)$ divides $P(x)$ perfectly without remainder:
$$P(x) = (x - r) Q(x)$$

---

## 📐 Step-by-Step Procedure

To factor $P(x) = x^3 - 4x^2 + x + 6$:

1. **Find potential roots $r$:** Integer roots must divide the constant term ($6$). Test $\pm 1, \pm 2, \pm 3, \pm 6$.
2. **Test root:** $P(2) = 2^3 - 4(2)^2 + 2 + 6 = 8 - 16 + 2 + 6 = 0$. So $r = 2$ is a root.
3. **Set up table:** Align coefficients $[1, -4, 1, 6]$ and place $r = 2$ on the left.
4. **Perform synthetic steps:**
   * Drop the first coefficient ($1$).
   * Multiply by $r=2$ and add to the next coefficient.

The resulting quotient polynomial is $Q(x) = x^2 - 2x - 3$.

Thus, $x^3 - 4x^2 + x + 6 = (x - 2)(x^2 - 2x - 3) = (x - 2)(x - 3)(x + 1)$.

---

[⬅️ Back to Extra Methods](./) | [⬅️ Back to Main README](../README.md)

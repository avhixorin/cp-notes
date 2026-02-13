# 🔹 GCD Properties

---

## 1. Euclidean Algorithm

gcd(a, b) = gcd(b, a % b)

Time Complexity: O(log(min(a, b)))

Worst case: Consecutive Fibonacci numbers.

---

## 2. Subtraction Property

gcd(a, b) = gcd(a, b - a)

More generally:
gcd(a, b) = gcd(a, b + ka)

Use Case:

- Reducing large numbers
- Removing common shifts

---

## 3. Adding Same Value

gcd(a + x, b + x)

Reduction:
gcd(a + x, b + x)
= gcd(a + x, (b + x) - (a + x))
= gcd(a + x, b - a)

Important:
The variable x disappears from differences.

---

## 4. Multiple Elements With +x

gcd(a1 + x, a2 + x, ..., an + x)

Let:
G = gcd(a2 - a1, a3 - a1, ..., an - a1)

Then:
Answer = gcd(a1 + x, G)

Edge Case:
If n = 1 → answer = |a1 + x|

---

## 5. Base Cases

gcd(x, 0) = |x|

gcd(0, x) = |x|

gcd(0, 0) = 0

---

## 6. Multiplication Rule

gcd(ka, kb) = k * gcd(a, b)

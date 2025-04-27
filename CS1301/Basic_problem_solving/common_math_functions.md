# 🧮 Commonly Used Functions in Python's `math` Module

The `math` module in Python provides access to many standard mathematical functions and constants. Below is a curated list of the most **commonly used functions**, including `math.e`.

---

## 📌 Constants

| Constant | Description | Example |
|----------|-------------|---------|
| `math.e` | Euler's number (≈ 2.718) | `math.exp(1)` → 2.718... |
| `math.pi` | Pi (≈ 3.14159) | `math.sin(math.pi)` → ~0 |
| `math.tau` | 2 × π (≈ 6.28318) | Circle in radians |
| `math.inf` | Infinity | `math.inf > 1e308` |
| `math.nan` | Not a Number | Used in undefined math results |

---

## 🔢 Exponentials & Logarithms

| Function | Description | Example |
|----------|-------------|---------|
| `math.exp(x)` | e^x | `math.exp(2)` → 7.389 |
| `math.log(x)` | Natural logarithm (base e) | `math.log(math.e)` → 1 |
| `math.log(x, base)` | Logarithm to any base | `math.log(100, 10)` → 2 |
| `math.log10(x)` | Base-10 log | `math.log10(1000)` → 3 |
| `math.log2(x)` | Base-2 log | `math.log2(8)` → 3 |
| `math.pow(x, y)` | x^y (float result) | `math.pow(2, 3)` → 8.0 |

---

## 🧮 Trigonometry

| Function | Description | Example |
|----------|-------------|---------|
| `math.sin(x)` | Sine (radians) | `math.sin(math.pi / 2)` → 1 |
| `math.cos(x)` | Cosine | `math.cos(0)` → 1 |
| `math.tan(x)` | Tangent | `math.tan(math.pi / 4)` → 1 |
| `math.asin(x)` | Arc sine (returns radians) | `math.asin(1)` → π/2 |
| `math.acos(x)` | Arc cosine | `math.acos(1)` → 0 |
| `math.atan(x)` | Arc tangent | `math.atan(1)` → π/4 |
| `math.degrees(x)` | Radians → Degrees | `math.degrees(math.pi)` → 180 |
| `math.radians(x)` | Degrees → Radians | `math.radians(180)` → π |

---

## 🧱 Rounding and Integer Functions

| Function | Description | Example |
|----------|-------------|---------|
| `math.floor(x)` | Round down | `math.floor(3.7)` → 3 |
| `math.ceil(x)` | Round up | `math.ceil(3.1)` → 4 |
| `math.trunc(x)` | Truncate decimal | `math.trunc(3.9)` → 3 |
| `math.fabs(x)` | Absolute value (float) | `math.fabs(-4.2)` → 4.2 |
| `math.factorial(n)` | n! | `math.factorial(5)` → 120 |
| `math.gcd(a, b)` | Greatest common divisor | `math.gcd(8, 12)` → 4 |

---

## 📌 Summary

The `math` module is essential for:
- Scientific and financial calculations
- Geometry and trigonometry
- Statistical and logarithmic modeling
- Clean and precise rounding or absolute operations

To use any of these:

```python
import math
result = math.sqrt(16)
```

---

> Tip: Use `help(math)` in Python to see everything available in the module.

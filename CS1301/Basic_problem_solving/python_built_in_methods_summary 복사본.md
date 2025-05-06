
# Python Built-in String and Float Methods Summary

This document summarizes important Python built-in methods you asked about, including how they work and when to use them.

---

## 1. String Methods for Character-Type Checking

| Method | Purpose | Example |
|:------|:--------|:--------|
| `isdigit()` | Checks if all characters are digits (0–9 and some Unicode digits) | `"123".isdigit()` → True |
| `isdecimal()` | Checks if all characters are strict decimal digits (0–9 only) | `"123".isdecimal()` → True |
| `isnumeric()` | Checks if all characters are numeric (digits, superscripts, Roman numerals) | `"Ⅻ".isnumeric()` → True |
| `isalpha()` | Checks if all characters are letters (a–z, A–Z) | `"Hello".isalpha()` → True |
| `isalnum()` | Checks if all characters are letters or digits (no spaces/symbols) | `"abc123".isalnum()` → True |
| `isspace()` | Checks if all characters are whitespace (spaces, tabs, etc.) | `"   ".isspace()` → True |
| `isupper()` | Checks if all letters are uppercase | `"HELLO".isupper()` → True |
| `islower()` | Checks if all letters are lowercase | `"hello".islower()` → True |
| `startswith(substring)` | Checks if a string starts with a specific substring | `"hello".startswith("he")` → True |
| `endswith(substring)` | Checks if a string ends with a specific substring | `"hello.txt".endswith(".txt")` → True |

---

## 2. Float Method: `is_integer()`

| Method | Purpose | Example |
|:------|:--------|:--------|
| `is_integer()` | Checks if a float value is numerically an integer (no decimal part) | `(5.0).is_integer()` → True |

### Important Notes:
- `is_integer()` only works on `float` types, **not** on `int` types.
- Example: `5.is_integer()` → ❌ Error

---

## 3. Differences Between `isdecimal()`, `isdigit()`, and `isnumeric()`

| Method | Strictness | Accepts | Example |
|:-------|:-----------|:--------|:--------|
| `isdecimal()` | Strictest | Only 0–9 digits | `"123".isdecimal()` → True |
| `isdigit()` | Medium | 0–9 digits + Unicode digits like "²" | `"²".isdigit()` → True |
| `isnumeric()` | Most flexible | Any numeric-looking character (Roman numerals, fractions, etc.) | `"Ⅻ".isnumeric()` → True |

---

## 4. How to Check if a String is a Float

You cannot use `isdigit()` or `isdecimal()` to check decimal numbers like `"3.14"`.  
Instead, use a `try-except` block:

```python
def is_float(s):
    try:
        float(s)
        return True
    except ValueError:
        return False
```

This will correctly recognize strings like `"3.14"`, `"123"`, or `"-5.2"` as valid numbers.

---

## 5. How to Distinguish Integers vs Floats

```python
def check_number_type(s):
    try:
        num = float(s)
        if num.is_integer():
            return "integer"
        else:
            return "float"
    except ValueError:
        return "not a number"
```

- `"123"` → "integer"
- `"3.14"` → "float"
- `"hello"` → "not a number"

---

# ✨ Summary

- Use `isXXX()` methods for **string character type checking**.
- Use `float()` + `.is_integer()` for **numeric type checking (integer vs float)**.
- `isdecimal()` is the strictest; `isnumeric()` is the most flexible.

# 🕒 Time Comparison Without `if` – AM/PM Safe Logic

This document explains a concise and robust Python approach to comparing times (in 12-hour format with AM/PM) **without using `if` statements or function definitions**, while **safely handling edge cases like 12 AM / 12 PM**.

---

## ✅ Problem

Determine if the **current time** is **before** the **deadline time**, using:

```python
current_hour, current_minute, current_section = 12, 37, "PM"
due_hour, due_minute, due_section = 9, 0, "PM"
```

Time is given in 12-hour format with `"AM"` or `"PM"` strings.

---

## 🔥 The User's Logic (Elegant & Correct)

```python
am_pm = current_section < due_section
current_hour = current_hour % 12
due_hour = due_hour % 12

print(
    am_pm or
    (
        current_section == due_section and
        (due_hour, due_minute) > (current_hour, current_minute)
    )
)
```

---

## 💡 How It Works

### 🔹 1. AM/PM Section Comparison

```python
am_pm = current_section < due_section
```

- `"AM" < "PM"` returns `True` if current time is in the morning and due is in the afternoon
- If this is the case, the current time is guaranteed to be earlier → `True`

---

### 🔹 2. Hour Normalization

```python
current_hour = current_hour % 12
due_hour = due_hour % 12
```

- Converts `12` → `0` for both AM and PM
- Safe because this normalization is only used when **both sections match**
- Ensures that 12 AM and 12 PM don't mistakenly appear “later” than expected

---

### 🔹 3. Tuple Comparison

```python
(due_hour, due_minute) > (current_hour, current_minute)
```

- Only runs when `current_section == due_section`
- Tuple comparison automatically handles hour/minute ordering
- Works perfectly even if hour = 0 (i.e., 12 AM or 12 PM after normalization)

---

## ✅ Why This Is Great

| Feature | Status |
|--------|--------|
| Handles 12 AM/PM correctly | ✅ |
| No `if` statements | ✅ |
| Concise, readable logic | ✅ |
| Works for all AM/PM combinations | ✅ |
| Efficient (no unnecessary conversion) | ✅ |

---

## 🧠 Summary

- The logic works because it **isolates AM vs PM cases first**, and only compares hour/minute when both are in the same section.
- By normalizing 12 → 0 and using Python's tuple comparison, it stays safe and intuitive.
- This is a great example of how **boolean math + tuple comparison** can replace control flow.

> A minimal, robust solution that handles time logic with elegance. 👏


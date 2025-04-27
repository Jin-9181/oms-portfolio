# 📘 Understanding `dict.items()` in Python

`dict.items()` is one of the most commonly used methods when working with dictionaries in Python. This guide explains what it does, how it works, and why it’s useful.

---

## 🔹 What is `items()`?

```python
dict.items()
```

Returns a view object that displays a list of a dictionary's **(key, value)** tuple pairs.

---

## 🧾 Example

```python
person = {
    "name": "Alice",
    "age": 30,
    "city": "Seoul"
}

for k, v in person.items():
    print(f"Key: {k}, Value: {v}")
```

### ✅ Output:

```
Key: name, Value: Alice
Key: age, Value: 30
Key: city, Value: Seoul
```

---

## 🧠 Why Use `items()`?

| Situation | Method | Description |
|----------|--------|-------------|
| You want only keys | `for key in dict:` | Default iteration gives keys |
| You want only values | `for value in dict.values()` | `.values()` gives just the values |
| ✅ You want both keys and values | `for key, value in dict.items()` | Best practice and most common usage |

---

## 🧱 What Does It Return?

```python
person.items()
# Output: dict_items([('name', 'Alice'), ('age', 30), ('city', 'Seoul')])
```

This is essentially an iterable of tuples, so it can be unpacked in a loop:

```python
for key, value in person.items():
    ...
```

---

## 💡 Applied Example

```python
fruits = {"apple": 3, "banana": 5, "orange": 2}

total = 0
for fruit, count in fruits.items():
    print(f"{fruit}: {count}개")
    total += count

print("총합:", total)
```

---

## 🧠 Related Methods

| Method | Description | Example |
|--------|-------------|---------|
| `.items()` | Returns (key, value) pairs | `for k, v in d.items()` |
| `.keys()` | Returns keys | `for k in d.keys()` |
| `.values()` | Returns values | `for v in d.values()` |

---

## ✅ Summary

- `.items()` returns each (key, value) pair from a dictionary.
- You can use `for key, value in dict.items()` to loop through both.
- It supports tuple unpacking, which makes it powerful and clean for iteration.
- Best choice when both keys and values are needed during a loop.


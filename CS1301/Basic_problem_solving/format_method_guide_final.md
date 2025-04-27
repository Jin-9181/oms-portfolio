
# 🧠 Python `.format()` String Method - Quick Reference

The `.format()` method in Python is used to insert values into a string in a clean and readable way. It replaces placeholders (`{}`) in a string with values provided via the `.format()` function.

---

## ✅ Basic Syntax

```python
"Your text here {}".format(value)
```

---

## 🔹 Example 1: Basic usage

```python
name = "Jin"
greeting = "Hello, {}!".format(name)
print(greeting)
# Output: Hello, Jin!
```

---

## 🔹 Example 2: Multiple values

```python
a = 3
b = 5
result = "{} + {} = {}".format(a, b, a + b)
print(result)
# Output: 3 + 5 = 8
```

---

## 🔹 Example 3: Using index positions

```python
sentence = "{1} is after {0}".format("one", "two")
print(sentence)
# Output: two is after one
```

---

## 🔹 Example 4: Using values from a list

```python
info = ["Alice", 30]
message = "Name: {}, Age: {}".format(info[0], info[1])
print(message)
# Output: Name: Alice, Age: 30
```

---

## 🔹 Example 5: Unpacking a list directly

```python
data = [10, 20, 30]
print("A: {}, B: {}, C: {}".format(*data))
# Output: A: 10, B: 20, C: 30
```

---

## 🔹 Example 6: Formatting decimals and numbers

```python
pi = 3.14159
print("Pi: {:.2f}".format(pi))
# Output: Pi: 3.14
```

---

## 📌 Bonus: f-strings (Python 3.6+)

A more modern way to format strings:

```python
name = "Jin"
print(f"Hello, {name}!")
# Output: Hello, Jin!
```

---

## ✅ Summary Table

| Pattern | Description |
|---------|-------------|
| `"{}".format(x)` | Insert a single value |
| `"{0} {1}".format(a, b)` | Specify order with index |
| `"{}".format(my_list[0])` | Use list values |
| `"{}".format(*my_list)` | Unpack list values |
| `"{:.2f}".format(num)` | Format decimal to 2 places |

---

💡 Use `.format()` for readable, flexible string formatting. For more concise syntax in Python 3.6+, consider using **f-strings**!

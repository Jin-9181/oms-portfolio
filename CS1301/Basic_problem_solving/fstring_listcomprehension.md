# Python Basics: f-string and List Comprehension

## 📌 f-string (Formatted String Literals)

**f-strings** are a concise and readable way to include the values of variables or expressions inside strings. They were introduced in Python 3.6.

### ✅ Syntax

```python
f"some text {variable_or_expression}"
```

- Any variable or expression inside `{}` is evaluated and inserted into the string.
- You must prefix the string with `f` or `F`.

### ✅ Examples

```python
name = "Alice"
age = 30
print(f"My name is {name} and I am {age} years old.")
# Output: My name is Alice and I am 30 years old.

print(f"The sum of 2 and 3 is {2 + 3}.")
# Output: The sum of 2 and 3 is 5.
```

### ✅ Notes

- Without the `f` prefix, variables inside `{}` are treated as normal text:
  
```python
name = "Alice"
print("Hello, {name}")  # Output: Hello, {name}
```

- With `f`:
  
```python
print(f"Hello, {name}")  # Output: Hello, Alice
```

---

## 📌 List Comprehension

**List comprehension** is a concise way to create lists from existing iterables. It combines `for` loops and optional conditions into a single line.

### ✅ Syntax

```python
new_list = [expression for item in iterable]
```

- `expression` is the value to include in the new list.
- `item` is the loop variable.
- `iterable` is the original list or sequence you're iterating over.

### ✅ Examples

```python
numbers = [1, 2, 3, 4]
squares = [n**2 for n in numbers]
print(squares)  # Output: [1, 4, 9, 16]
```

```python
names = [" Alice ", " Bob", "Charlie "]
cleaned_names = [name.strip() for name in names]
print(cleaned_names)  # Output: ['Alice', 'Bob', 'Charlie']
```

### ✅ With Condition

```python
evens = [n for n in range(10) if n % 2 == 0]
print(evens)  # Output: [0, 2, 4, 6, 8]
```

---

## ✅ Summary

| Feature             | Use Case                                      |
|---------------------|-----------------------------------------------|
| `f"{variable}"`     | Insert variables/expressions inside strings   |
| `[x for x in list]` | Create or transform lists in one line         |

Both are Pythonic tools that help write cleaner, shorter, and more expressive code.
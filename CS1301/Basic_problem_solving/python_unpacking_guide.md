
# 🧩 Python Unpacking: Complete Guide

This guide covers how unpacking works in Python using `*` and `**`, including for lists, tuples, and dictionaries—both in assignments and function definitions or calls.

---

## 📦 1. List Unpacking

### ✅ Basic usage
```python
my_list = [1, 2, 3]
a, b, c = my_list
# a = 1, b = 2, c = 3
```

- The number of variables must match the number of elements.

### ✅ Using `*` to capture the rest
```python
a, *b = [1, 2, 3, 4]      # a = 1, b = [2, 3, 4]
*a, b = [1, 2, 3, 4]      # a = [1, 2, 3], b = 4
a, b, *c = [1, 2, 3, 4, 5]# a = 1, b = 2, c = [3, 4, 5]
```

---

## 🧷 2. Tuple Unpacking

- Works the same as list unpacking.
```python
my_tuple = (10, 20, 30)
x, y, z = my_tuple
# x = 10, y = 20, z = 30
```

- Also supports `*`:
```python
a, *b = (1, 2, 3, 4)  # a = 1, b = [2, 3, 4]
```

---

## 🗃 3. Dictionary Unpacking (`**`)

### ✅ Function arguments
```python
def greet(name, age):
    print(f"Hello, I'm {name}, {age} years old.")

info = {"name": "Alice", "age": 30}
greet(**info)
```

### ✅ Merging dictionaries
```python
a = {"x": 1, "y": 2}
b = {"y": 3, "z": 4}
merged = {**a, **b}
# merged = {'x': 1, 'y': 3, 'z': 4}
```

---

## 🧰 4. Unpacking in Functions

### ✅ `*args` (positional arguments)
```python
def add_all(*args):
    return sum(args)

add_all(1, 2, 3)  # Returns 6
```

- `args` is a tuple containing all additional positional arguments.

### ✅ `**kwargs` (keyword arguments)
```python
def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", job="Engineer")
```

- `kwargs` is a dictionary of all additional keyword arguments.

### ✅ Mixed example
```python
def show(a, *args, **kwargs):
    print("a:", a)
    print("args:", args)
    print("kwargs:", kwargs)

show(1, 2, 3, x=10, y=20)
```

---

## 🧨 5. Unpacking in Function Calls

```python
nums = [1, 2, 3]
add_all(*nums)  # Same as add_all(1, 2, 3)

info = {"name": "Bob", "age": 25}
greet(**info)   # Same as greet(name="Bob", age=25)
```

---

## 🧠 Summary

| Unpacking Type | Syntax     | Resulting Type | Common Use                   |
|----------------|------------|----------------|------------------------------|
| List unpacking | `a, b = [...]` | variables | Variable assignment          |
| Tuple unpacking| `a, b = (...)` | variables | Same as list                |
| *args          | `*args`    | tuple          | Accept variable-length positional args |
| **kwargs       | `**kwargs` | dict           | Accept variable-length keyword args    |
| Call unpacking | `*list`, `**dict` | depends | Spread arguments into functions        |

---

## 🔚 Notes

- Unpacking is a powerful and elegant way to deal with flexible data structures and argument passing.
- Use `*` for sequences, and `**` for mappings.

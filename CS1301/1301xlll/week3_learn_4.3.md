# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 4.3: Lists

---

## 📚 Key Concepts Summary

### Concept 1: [List]
- List: a data structure that contains ordered number of values that are accessed by numberice indicies. 
- List-like Structures: Also referred to as sequences and collections, a data structure that holds multiple individual values gathered together under one variable name, accessed via indices. Includes to lists, arrays, and tuples. Lists are simultaneously a type of data structure and a specific type in some languages.
- characterisrics of list can be defied differently on each language
    - immutability of value : can we edit the value of inside the list
    - immutability of the size of the list : can we addd additional value to the list
    - Homogeneity: A property of lists determining whether they can accept multiple types of variables. A homogenous list can only accept one type of variable; a nonhomogenous or heterogenous list can accept multiple types.
- exmaples
    - list, arrays, tuples, vectors, tables, and etc

### Concpet 2: [Tuples in Python]
- Tuple: An immutable form of a list-like structure in Python.
- Lists: A mutable form of a list-like structure in Python.
- To declare a tuple, we set a variable equal to a comma separated series of values or variables.
    - example_tuple = (value1, value2, value3)
    - example_tuple2 = (var1, var2, var3)  - variables has to have the value assigned(declared) - but it's not assigning the variable it self. it's giving the value of variable
- we can mix up the data types of values insdie tuples
    - if a string is in a tuple, then the print() will print out the quotation mark together
    -
- use tauple[#] to access the values insdie the tauple(tauple is basically a list)
- unpacking, we mean taking the list of values contained within the tuple, and assigning each one to a distinct variable.
    - x = 123
    - tauple = (x)
    - y = tauple
    = y = 123
- You can't chagne the tauple itself. Which mean tauple is immutable. so you can' change a (1,2,3) to (3,2,3)
     - but you can assign a different tauple to a variable that is tauple like my_tauple = (1,2,3) and assiging my_tauple = (3,4,5)
- Tuaple can have only one value but needs a , behind it
- True value of tuaple comes when writing function, function can only return one value but by using tauple we can use tauple and unpack it then we can use it usefully. 
- Tauples can be nested, which mean we can make tuaples made of tauples
     - superTauple = ((1,2,3,), (4,5,6), (7,8,9))
     - How to access : tauple[x][y] : x is the index number of the tauple and y is the ord insde that sub tauple 
     - This can be used like a row / column
     - t1 = (1,2,3)
     - t2 = (4,5,6)
     - t3 = (7,8,9)
     - t4 = (t1, t2, t3) 
     - t4[1][2] is like access the 2nd row on 3rd column

### Concept 3: [List in Python]
- Anything you can do with tauple then you can do list
- lists are mutable unlike tauples
- common ground with tauple:
    - most of the thing we learn 
- Difference between list and tauple
    - list.sort() 
        - Python's list will preserve the order of the items
        - for integer : lowest to highest
            - this means list is mutable. the value actually changed
        - the index changs but the id of value will remain
    - 
    - list.append(x)
    - list.extend(otherlist_name)
    - list.insert(index#, value) 
    - list.remove(value)
    - list.reverse() : reversed the current order of the list
    - list.pop() : removes the last value of the list and returns it
        - 'returns' means it can be assigned to a variable and also act as a method.
        - i = list.pop() : will remove the last item of the list and return the value which will assign it to variable i here. 
        - 
    - del mylist[index:index] : slicing + indicies work here
    - list.index(value) = returns the index of the value
    - list.count(value) = returns the count of value in the list
    - value in list : a boolean oeprator to check whether a value is insde the list.
    ## 🔄 In-Place vs New Object Behavior in Python

| Operation / Method            | Data Type        | Behavior        | Description |
|------------------------------|------------------|-----------------|-------------|
| `list.sort()`                | `list`           | ✅ In-place     | Sorts the list itself; returns `None`. |
| `sorted(list)`               | `list` / iterable| ❌ New object   | Returns a new sorted list; original remains unchanged. |
| `list.reverse()`             | `list`           | ✅ In-place     | Reverses the list order directly. |
| `reversed(list)`             | `list` / iterable| ❌ New object   | Returns a new reverse iterator; original unchanged. |
| `list.append(x)`             | `list`           | ✅ In-place     | Adds element to the end of the list. |
| `list + list2`               | `list`           | ❌ New object   | Concatenates two lists into a new one. |
| `list += list2`              | `list`           | ✅ In-place     | Extends the list with elements from list2. |
| `str.upper()`                | `str`            | ❌ New object   | Returns an uppercase copy of the string. |
| `str.replace()`              | `str`            | ❌ New object   | Returns a modified string; original is untouched. |
| `x *= 2` (`list`, `set`)     | `mutable types`  | ✅ In-place     | Modifies the object directly, if applicable. |
| `x *= 2` (`str`, `tuple`)    | `immutable types`| ❌ New object   | Creates a new object due to immutability. |
| `dict.update({...})`         | `dict`           | ✅ In-place     | Updates the dictionary directly. |
| `a = a + b` (`list`, etc.)   | any              | ❌ New object   | Always creates a new object and rebinds the variable. |

### Notes:
- `In-place` means the operation modifies the original object.
- `New object` means a fresh object is created and assigned; original remains unchanged.
- For mutable types (`list`, `dict`, `set`), in-place operations affect all references.
- For immutable types (`str`, `tuple`, `int`), any change results in a new object.


### Concept 4: [iteration over a list]
- for x in list: 
    - x will run for each items in the list 
### Concept 5: [Function and list] 
- since lists are mutable, if a list is inside a function the list can be changed

### Concept 6: [list vs tauple]
- We often use tuples when we're definitely dealing with a pre-determined number of items.
- We use lists when the ability to add or remove from the list would actually be useful and relevant.
- We usually use lists when the individual things on the list are qualitatively similar. We use tuples if they're qualitatively different.
- List : usually for same data types. For iteration

### Concpet 7: [Advanced list- like structure]
- Stack: A list-like structure that follows the “Last-In-First-Out” paradigm, where we can only access the most recently-added item on the list and can only access it by removing it from the list.
    - we can only add to the top of stack, we can only access the top data while removing it
    - LIFO = Last in First out
- Queue: A list-like structure that follows the “First-In-First-Out” paradigm, where we can only access the least recently-added item on the list  and can only access it by removing it from the list.
    - FIFO = First in First Out
    - But like our stacks, generally queues will only let you see the data if you actually remove the data from the list.
- Linked List: A list-like structure where the location of each item in the list is contained in the previous item in the list.
    - 
## 💻 Code Practice Summary

- [`filename.py`](./filename.py): Description of this coding task
- [`filename.ipynb`](./filename.ipynb): Jupyter notebook summary

- 
- 
---

## 🧠 How I Understand It (In My Own Words)
- 



---

## ❓ Unclear Points / To Revisit
-  
---

## 🗂 Reference Links

- [Official docs / lecture video]()
- [Helpful blog post]()
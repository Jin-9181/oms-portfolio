# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 4.1: Data Structure

---

## 📚 Key Concepts Summary

### Concept 1: [Data Structure]
- Data Structures: Approaches to organizing abstract data types, such that the data can be accessed efficiently.
- List : 
- list-like structure (sqeuences): List-Like Structures: Also referred to as sequences and collections, a data structure that holds multiple individual values gathered together under one variable name, accessed via indices. This includes structures like lists, arrays, and tuples. Lists are simultaneously a general type of data structure and a specific data type in some languages.
- Index: A number used to access a particular element from a list-like data structure. Traditionally, most programming languages assign the first item of a list-like data structure the index 0.
- String: A data structure that holds a list, or a string, of characters.
- Lists: A data structure that holds multiple individual values gathered together under one variable name, accessed via indices. Similar to arrays and tuples.
- File Input and Output: The complementary processes of saving data to a file and loading data from a file, generally such that the state of the memory of the program is the same after saving and loading have occurred.
- Dictionaries: A data structure comprised of key-value pairs, where a key is entered into the dictionary to get out a value. Similar to or synonymous with Maps, Associative Arrays, HashMaps, and Hashtables.

### Concept 2:[Passing by Value vs Passing by Reference]
- Passing by Value : No access to the variables themeselves. handing over the value to the function and the function returning the value. No variables are exchanged.
- Passing by reference : Having access to the variables themselves. Handing over the variables themeselves, which means the function can edit the variables if it wants to
    - Python won't do this with integers. Integers are always effectively passed by value. But in some languages like C++, you can choose whether to pass a variable by value or reference. 
    - when we input a name, the name will point to a memory address, a reference. It points to a location in memory. The location then stores the actual value we care about. 
- Python deals with passing-by-value and passing-by-reference a little strangely. In reality, everything is passed by reference, but because of some details we'll cover next lesson, it often appears to be passing by value.
    - Even if you have a variabled defined before the function and the variable's value has changed inside the function. The value won't change outside of the function. It's as if python treating the primitive data types as if it's passing by value. 
        - Data types : integer, string
    - Python passes by reference for most of the data types. 
- Variable assignment 
    - One is just that we can refer to the same data by different names-- we can have multiple variables that point to the same data and if you access and modify the data via one variable name, it also modifies the data for any other variable names
    - variable name is a way of just finding the value. 
    - mutability

### Concept 3: [Mutability]
- Mutability: Whether or not a variable can have its value changed after being declared.
- Mutable Variable: A variable whose value can change after it has been declared.
- Immutable Variable: A variable whose value cannot change after it has been declared.
- All variables in Python are passed by reference. However, we saw some appear to act as if they're passed by value. The reason they acted this way is because they were immutable. Keep watching and we'll explore that more
    - 실제로 무슨 일이 일어나나? 3이란 값 + 자리에 해당 변수를 할당하지만... 새로운 값이 할당되면 기존 자리에 해당 값을 넣는게 아니라 새로운 자리에 그 데이터를 놓고 그데이터에 변수를 할당하는 느낌...
    - 
- So the fundamental takeaway for immutable data types is if for immutable data types, like integers and strings, when Python is asked to change the value of an existing variable, it does not actually change the value stored in memory. In this case, it doesn't erase the 5 and replace it with a 6. Instead, it creates a new place in memory,
puts the new value there, and tells the variable name to point to that instead. So it no longer points to the old value, and instead it points to the new value. This is the way Python handles immutable data types.
- There's a memory address : print(id(variable_name)) will print the memory address. 
- print(id(immutable_variable_with_A) == id(immutable_variable_with_B))
- list will act differently assigning [1, 2, 3] to variable A and B. These two variables will have different momory address. 
- For mutable datas, you can change the data but the id won't change. 
- everytime you create a mutable data, you create new ones with new id

### Concept 4: [Method]
- Methods: Functions that are contained within data types.
    - calling the variable  and then call the methods
        - so method is a function that is contained in a data structure
- Boolean method : returning T and False
    - .isdigit(), 
        - .isdigit() is build inside the string data type, which means any strings will have the access to isdigit()
            - "." means that the one before . has the access to the method the follows
    - mystring.startswith("string")
        - Method can also have inputs like that. 
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
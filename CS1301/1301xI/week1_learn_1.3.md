# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 1.3: 

---

## 📚 Key Concepts Summary

### Concept 1: [Debugging]
- the goal of debugging is to get the information necessary to locate and fix the error.
- Don't just stare at the codes but maybe add some codes and try to make the problems clearer
- print debugging
    - A form of debugging where print statements are added throughout the code to check how the program is flowing.
    - simply printing out a text that a certain flow is finished will help to locate the error
- scope debugging
    - A form of debugging where print statements are added to check the status of the variables in the program at different  stages to see how they are changing.
    - Scoping down a code to review whether a code in working as intended within that scope. 
    - Printing out results of each loop to see where's going wrong

- rubber duck debugging
    - A form of debugging where the programmer explains the logic, goals, and operations to an inanimate listener to methodically step through the code.


### Coencept 2: [Errors]
- compilation error:  error that occurs while compiling a code. errors that occur during the computer's read through the code 
    - syntax error: code that doesn't work with current programming language. violating Python's internal grammer
    - name error: code that tries to use something that doesn't exist
        - using unassigned variables
    - type errors: code taht doesn't make sense
        - smell of True, color of number 5
        - pring(leng(5)) : there's no length in integer so it's a type error
    - Attribute error: 
        - a = "Hello, World" b = 5
        - print(a.endswith("d")) : true 
        - print(b.endswith("d")) : attribute error
- runtime errors: errors that only will be found out while runing the code
    - exampels
        - dividing by zero : dividing number by number won't be found until the number is zero when it runs
        - null errors : code containing a variable that has no value
        - memory erros: code that surpasses the computer's power

### Concept 3: [advanced_debugging]
- step-by-step execution: Some development environments will let you run your code one line at a time, instead of all at once.
- variable visualization: looking into the brain of computer while it's running the code.
- in-line debugging: 

 

## 💻 Code Practice Summary

- [`filename.py`](./filename.py): Description of this coding task
- [`filename.ipynb`](./filename.ipynb): Jupyter notebook summary

---

## 🧠 How I Understand It (In My Own Words)

- We might need to write codes that helps debugging in the first place, even if the code doesn't help the program to achieve it's original goal. 
- when encountering a name error, try to find misspellings. 
---

## ❓ Unclear Points / To Revisit

- complie time error vs run time error
---

## 🗂 Reference Links

- [Official docs / lecture video]()
- [Helpful blog post]()
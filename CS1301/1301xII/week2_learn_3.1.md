# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 3.1: controlled structures

---

## 📚 Key Concepts Summary

### Concept 1: [control structures]
- Control Structures: Statements that control the flow of execution of the program. Or, more simply, lines of code that control when other lines of code run.
- It allows us to loop over certain lines of code multiple times, changing tha data they act on each time
- Conditional Statements: Programming statements that control what code is executed based on certain conditions; usually of the form “if”, “else if”, and “else”.
- Loop: A programming control structure that executes a segment of code multiple times.
- Function: A segment of code that performs a specific task, sometimes taking some input and sometimes returning some output.
- Exception: An error that a program might want to anticipate and catch instead of outright avoiding.
- Exception Handling: A control structure that catches certain anticipated errors and reacts to them accordingly.

### Concept 2: [indentation]
- Indentation: Spaces at the beginning of a line that are used to group together blocks of code. All consecutive lines of code at the same level of indentation are in a single code block.
- line that sets so condition controls all the lines of code that are indented under the initial code before indentation
- nested indentation :  putting one control structure inside the code controlled by another control structure. the entire indented code won't run if the condition is false

### Concept 3: [scope] 
- Scope: The portion of a program’s execution during which a variable can be seen and accessed.
- similar to computer's short term memory
-  refers to which parts of a program can see the variables that you've created.
- Scope can work pretty differently from language to language, so when you start to learn another programming language, be prepared to investigate how scope works in the new language. Generally, it works very differently between scripting languages (like Python) and compiled languages (like Java).
- Most languages use controlled structure to define scope
- Scope of a variable is often limited by the control structure
    - The program after the conditiona cannot see the variables created inside the conditionals because programs outside the conditionals can't know whether the conditionals were true and if the variables were every created. 
- Scope in Python is actually a little bit more straightforward to understand than in many languages, but it also carries its own challenges. Generally, every variable or function we create has a line on which it is created. If that line has already run, then the scope for that variable or function has begun. If it hasn't, then that variable's or function's scope has not yet begun.
- because of the scope of varaibles in python's nature, it can be dangerous to create a variable inside the condionals, a solution can be creating a variable outside the conditionals (before) 
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
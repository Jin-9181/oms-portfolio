# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 2.4: matchmatical operators

---

## 📚 Key Concepts Summary

### Concept 1: [Assignment operator]
- Assignment Operator: An operator that takes the output of an expression and assigns it to a variable.
- Operator
- '=' assigns a value ' x = 5' 
- '+=' adds to the current value and assing s0 . x += 3	is equal to x = x + 3
- -=	Subtract and assign	
- *=	Multiply and assign	
- /=	Divide and assign	
- //=	Floor divide and assign	
- %=	Modulus and assign	
- **=	Exponent and assign	

### Concept 2: [Mathmatical operator]
- +, -, * , / , %
    - Division: Even if you divide an integer by integer and it's even. The data type will be a float. output is always an float.
    - % Modulus : giving the result of division as remainder instead of quotient. 
    - divmod(a,b) = (quotient,remainder) = (a/b,a//b)
    - math.floor(a) = round down to the nearest integer and converting the type to integer. 
        - math.floor is almost as if floor dividing by 1 and converting to int. but this doesn't apply to negative numbers because int() will not round down but get rid of the remainder. For -5.1 math.floor() will return -6 but floor dividing by 1 and converting to in will give -5.

- % can be used for desinging pages like showing only 10 contents to the page and creating new one. Using modulus will give me the idea whetehr the number of content is divided evenly by 10 
- len(): A function that takes as input a variable with a length, such as a string of characters or a list of items, and returns its length.
- Floor division, represented by a double-slash (//), which is division that rounds down to the nearest whole number. For example, 5 // 2 would be 2, because 5 divided by 2 is 2.5, which is rounded down to the nearest integer, 2.
- Exponentiation, represented by a double-asterisk (**), which raises the first number to the second number. For example, 5 ** 2 would be 25, because 5 raised to the 2nd power is 25.
- If ther's a float in mathmatical operator : always the ouput is float. 

### Concept 3: [self assignment]
- Self-Assignment: A common programming pattern where a variable is assigned to the output of an expression that included the variable itself.
- Self-assignment reveals something very important about the assignment operator: Python (and most other programming languages) will evaluate everything on the right side of the assignment before attempting to assign the result to the variable on the left. That's why self-assignment works: Python initially replaces the variables with their values, so by the time we assign a new value to a variable, Python doesn't remember that the variable receiving a new value was used in the calculation.
- word count in a paragraph. wordcount = wordcount + 1 
- Increment: Repeatedly adding a constant, typically one, to a variable.
    - example
        lettercount = 0 
        for character in "Hello, world" : 
            lettercount = lettercount + 1
        print(lettercount) 

        Outcome : 12 
- first assigns the value of the variable on the right side of assignement. Then it evaluates everythign on the right side and finally assigns the value to the variable(left isde) 

### Concept 4: [Logical + mathmatical operator]
- Generally speaking, it's reasonable to assume that if you mix logical and mathematical operators, Python will evaluate all the mathematical operators before trying to move on to logical ones. For example, given the expression 2 + 5 > 3, Python will evaluate 2 + 5 before trying to evaluate 5 > 3.





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
-  usually if a programming questions asks you to get the quotient just divide it. Don't approach it like math. 
- import.
---

## 🗂 Reference Links

- [Official docs / lecture video]()
- [Helpful blog post]()
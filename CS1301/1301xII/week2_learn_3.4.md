# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 3.4: Function

---

## 📚 Key Concepts Summary

### Concept 1: [function]
- A segment of code that performs a specific task, sometimes taking some input and somties returning some output
- Functions let us package code  into mini-programs to reuse.
- Function Call : a place where a function is actually used in some code. Once this happens The execution of code then goes into that function runs the function's code, and then returns to the main code. 
- function definition : creates a function, including its name, parameters, and code, to be used by other portions of a program
    - funtion header: names the function and states what input it will expect. input is shows as list of parameters. The name and list of parameters a function expects, provided as reference to the res of the programs to use when calling the function
    - parameters: a variable for which a function expects to receive a value when called, whose scope is the function's own execution
    - function body: The code that a functions ruens when called. Lines of code that dictate what shouldb done when the function is called
    - Return statement: The line of code that defines what output will be sent back at the end of a function
    - Argument : input passed into the parameters during a function call
- Scope is also working same in function too.
- Not all function have need output or input
- end="" : not to move over to next line 
    - print("$", end="")
      print(5) will print $5

### Concept 2: [defining function]
- Once we define function, the actual body doesn't run at that moment. 
- once we call the function, the program goes back to the line we defined the fuction and runs the body from there

### Concept 3: [parameter and return]
- parameters are the pieces of input the functions expects, while arguments are the actual pieces of input a specific functions call receives. So multiply functions will expect two numbers which are parameters and if I call 'multiply' with the number 7 and 2 the 7 and 2 are arguments. And then return the output 14
- when there's a return. we are replacing the function call with return for the call.
    from datetime import date
    def get_today_date():
        x = date.today().year
        y = date.today().month
        z = date.today().day
        return str(x) + "/" + str(y) + "/" + str(z)
- we can set a variable as a parameter and if we do that the variables value will be used as the argument when the function is called. 
- multiple parameter
    functionName(parameter1, parameter2):

### Concept 4: [Mistakes in function]
- Parameter mismatch: we gave a function more or fewer parameters than it expectd
- Scope Error: we tried to use a variable in a function that was created outside the function, or similaryly, we tried to use a variable outside a function that was created inside the function. Variables created inside the function exist inside the function and only until the function is done running. 
- NoneType
    - If you're returning inside a conditional, ensure every branch of conditional has a return statement
    - Even inside nexted conditionals, we still want to make sure every lower branch also has an else that returns something. 
    - 

### Concept 5: [Keyword parameter]
- a special kind of optional parameter to which the program amy choose to assign an argument during a function call or may ignore. Typically, keyword parameters have a default value that is used if it is not overridden by a function call
    - inside the print() function 
        - sep = "string" is a keyword parameter that tells Python what character or what string to use to separate individual strings in one print
            - so sep = "" will make 'no space' as an separator which makes print("A", "B", "C", sep = "") to print  ABC
            - before this sep already had a value of " ".
        - end = "string" is a keyword parameter that tells Python what character to put at the end of the print statement. 
            - so end = "" will make no space, or new line character to come at the end of the print so making the next line(print) to come right after the current line(print)
            -  befor this end already had a value of the next line character
- keyworld parameters should go after all the positional parameters
- How to create keyword parameters
    - putting a value of something to the parameters. If no arguments has been input then the parameter will hold the preassigned value which is hte keyword parameter's value. but if it's overridden by an argument then the functiol called will run with the overridden value. But if no other value were input, the function will run with the predetermined keyword, parameter. 
    
    def currency_amount(currency, amount):
        if currency == "JPY"
            return "J" + amount
        elif currency == "USD"
            return "$" + amount 
        else: 
            return amount 
    print(currency_amount(5)) -> this is an error 
    print(currency)

    def currency_amount(amount, currency = USD):
    - with this currency now became a keyword parameter so even if we don't input currency when we call the function it will run without error assuming currency == "USD". If some argument is put , for example ' currency == "JPY" ' then it will be overridden. 
    - 
- also called optional parameter. 





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
# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 2.2: Variables 

---

## 📚 Key Concepts Summary

### Concept 1: [variable]
- a name that holds value
- the value can always change
- If you're ever confused about what a variable means, treat it as a question. num_cats becomes "Number of cats?" name becomes "Name?" The value, then, is the answer to the question. How many kids do I have? 'kid' is variable and 0 is the value
- an assignment statment is always formatted this way 'variable = value'
- naming the variable in a logical way is a good example of self-documented code
- Each programming language has it own way of designing variable names
    - python uses _(underscore)
    - languages like Java, C# uses camel cases (thisIsMyvaRiables)
- Typical vairables 
    - Boolean : True or False
    - an integer : 1,2,3 ... 
    - a decimal number : -7.1...
    - a date
    - a string of charater : "Hello, world"
- In python, the type of variable is only decided by the value assigned to it
- Variables name can only hold letters, numbers and underscore 
- Null: The “value” a variable has when it doesn’t actually have a value.
- literals (pure value in python) cannnot be assiged a value
- None : good for creating variables that will receive values later in your program because it lets you check to make sure they've received a value when needed.

### Concept 2: [Type of variables]
- integer, real number, character, string, boolean
- variables can hold any type of data (type of person)
- type of variables matters. 3 can't be logically compared with blue 
- types are assigend by the value. So variables hold only value and type are assigned by the value.(Pythong)
- tpye function : type() 
    - type(variable) -> type (value) -> some sort of type : <class 'int'>, <class 'int'>, 
    - Takes as input some variable or value directly and returns the type of the variable such as an integer or string of characters.
- mixing types: 
    - string(a sequence) can't be multiplied by float
    - but string(sequence) multiplied by string will work
    - boolean is interpreted as 1, 0 when mixed with operators ! True = 1, False = 0

### Concept 3: [NoneType]
- variable None
- This example's result 
    a = "Hello"
    b = "world"
    c = a + b
    d = print(c)
    print(d)
        is :
        Helloworld
        None
    - d = print(c) That does two things: it prints c, and it sets d to the result of printing c. So, we see "Helloworld" printed because it printed c.
    - What about d though? You might be tempted to think that d should now have the value "Helloworld", too. Isn't "Helloworld" the result of print(c)? Not exactly: the result of print(c) was "Helloworld" being printed to the console. It did something rather than just resolving to a value. So, there was no actual value for d to be assigned to. As a result, its value is None.
- You should never assign a variable to a print statement. You should never do something like a = print("Hi!").

### Concept 4: [Type Conversion]
- Converting to string : str(variable)
- implicit conversion
    - print(variable) inheritently holds the str() function inside becasue in order to print it it should be a string
        - implicit conversion doesn't work when you have other data types in the parenthesis it won't implicitly convert. And show a type error
        - using plus + won't automatically to implicit coversion because if there's a plus sign, Python will tries to add the two thing and then print. which means it assumes that they are same type of data. 
            - print("Today's date: " + date.today()) will return a type error

        - on the other hand, when if there's ',' in the parenthesis, python will treat these as seperate types so, it implicitly converts each data to string value and then puts the together. Also it naturally adds a space between two values
            - print("Today's date:", date.today()) will return data without problem 
        
- each data types all holds a string version of it any data can be changed to strings but not all datas are inter-covertable. 
-  a str(integer) will can be converted to float right away. Python will automatically assume there's a .0 behind the integer
- but str(float) can't be converted to integer right away. Phython doesn't know what to do with the number under decimal point.
- so what is convetable ?  Boolean and integer? let's test
- int(variable): Takes as input some variable (usually a string) and attempts to convert it to an integer, returning the integer if successful or raising a ValueError if unsuccessful. This function will work if variable is a string made up only of digits and, optionally, the negative sign.

- bool(variable): Takes as input some variable (usually a string) and attempts to convert it to a boolean, returning the boolean value if successful or raising a ValueError if unsuccessful. Generally, this function returns False if variable is 0 or an empty string, True if variable is anything else.

- float(variable): Takes as input some variable (usually a string) and attempts to convert it to a float, returning the float if successful or raising a ValueError if unsuccessful. This function will work if variable is a string made up only of digits and, optionally, a negative sign and a decimal point.

### Concept 5: [Input] 
- User inputs have automatically have the value type of string

### Concept 6: [Reserved keywords]
- You can tell the reserved words by "import keyword" and "print(keyword.kwlist)
- Importing Libraries. import, from. Not covered explicitly, but you'll see these in a few places throughout our material, especially when we're dealing with dates, turtles, or random numbers.
- Logical Operators. and, is, not, or, False, True, None. Covered in Chapter 2.3.
- Control Structures. as, break, continue, if, elif, else, for, in, while, pass, with. Covered throughout Unit 3. if, elif, and else are covered in 3.2; for, while, pass, continue, and break are covered in 3.3. as and with are not covered explicitly. in comes up in Chapters 2.3, 3.2, 3.3, and other places.
- Functions. def, return. Covered in Chapter 3.4.
- Object-Oriented Programming Syntax. class. Covered in Chapter 5.1.
- Error Handling. except, finally, raise, try. Covered in Chapter 3.5. else also comes up here.)
- if we misuse a reserved keyword then we'll see syntax letter
- using a function's name as a variable's name. it will conflict. 

### Concept 7: [Dot notation]
- When you see dot notation, the majority of the time you can think of them kind of like 's in English. For example, person.name would become "person's name". person.name.firstname would become "person's name's firstname".
- You might also sometimes see a function on the other side of the dot. For example, we could say my_string.isdigit(). This is like asking a question about my_string: my_string's a digit? Or, we could say my_string.upper(), which is like requesting some information: my_string's uppercase form?
- Date is a library we use like a fucntion
- There are variables with lots of data
    - datetime.datetime.now() = wil hold hour, minute, second
    - date.today() = will hold year, month, day
- overall structure is "variableName.partOfVariable"


## 💻 Code Practice Summary

- [`filename.py`](./filename.py): Description of this coding task
- [`filename.ipynb`](./filename.ipynb): Jupyter notebook summary

---

## 🧠 How I Understand It (In My Own Words)
- If there's mutliple parenthesis, the most inner one will run
- date.today(): After importing date from datetime, returns a date object representing the current date.
    - To have access to date.today(), the line from datetime import date must appear first.
- print(int("2.1")) won't work.  print(int(float("2.1"))) will work. 
- print(float("2")) will work. 
- print(bool("")) = False 
- print(bool(2)) = True
- print(flaot(Fasle)) = 0.0 
- 

---

## ❓ Unclear Points / To Revisit
-  What will this code print?
    1| a = 5
    2| b = a
    3| a = "Hello!"
    4| print(b)
    -  The answer is 5. b gets a's value on line 2, but if a's value changes afterward, it doesn't change what b's value was... at least not when we're dealing with integers, strings, or floats.
---

## 🗂 Reference Links

- [Official docs / lecture video]()
- [Helpful blog post]()
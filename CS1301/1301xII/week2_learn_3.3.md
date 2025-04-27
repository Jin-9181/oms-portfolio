# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 3.3: Loops

---

## 📚 Key Concepts Summary

### Concept 1: [conditional statement]
- Loop: A programming control structure that repeats lines of code until a certain condition is met 
- For loops: repeats some code a specified number of times
    - iteration : a single execution of a repeated task or block of code
    -  for-each loop : 
- While loops: Runs a block of code until a certain logical expression is satisfied (when it's true)
    - do while loops

- All loops can b ewritten into a while loop, not necessarily a for loop.
- Not all loops are interchangeable, and for loops use predetermined amount of iterations(not while loops)

### Concept 2: [Traditional Loop]
- Loop control variable : a variable whose value is the number of times a loop has run. It is used to check if the loop should keep running(if it has run as many itmes as it's supposed to) 
- for i in range (1, 11): 
    - range is a function that returns a list of numbers, starting with the first number, given in the parentheses, and ending before the last number. 
    - so in this case from 1 to 10
    - all of these formats are correct
        - range (x): start from zero and count up to x-1
        - range (x, y) : start from x and up to y-1
        - range (x, y, z): start from x and up to y-1 uping by z
        - range (x, y, -z) : (only when x> y) start from x and go down to y by z
- example
    sum = 0
    for i in range(1,11):
        next_number = int (input("input your score #"+ str(i) + ":")
        sum += next_number
    print(sum/i) 
    - input don't implicitly converts to string. 

- string[#] 
    - pulls the value according to the index number(#) 
- x_range = range(x, y)
    - x_range[3] == x + 3
- x_list = ["x", "Y", "Z", -----, "0"]
    - x_list[2] == "Z"
- for i in range(0, len("some sort of string"))
    - print(i, "some sort of string"[i])

### Concpet 3: [For-each loops]
- For-Each Loop: A loop control strcture that runs a block of code a predetermined number of times, where the number of times comes from the length of some list and the items in the list are automatically loaded in to variable for usage in the block of code
- example 
- list_nubmer = [10, 11, 12]
    sum = 0

    for loop_number in list_nubmer:
        sum += loop_number
    print(sum / len(list_number))
    will be print(33 / 3) 

- for x in list: -> x will have the value in the list 
- for x in string: -> x will have the each character of string 
- for x in range: -> x will have the number in range 
- Python does not iterate over boolean or numbers if we want to iterate a number we have to convert it into string

### Concept 4: [While loops]
- Any for loop can be written as a while loop, but oftentimes for loops more accurately represent the way we think about the way the code needs to work.
- python will allow 
    - while 0: , while 1: , while "x", while "hello" because it will automatically treat it as True or False ( 1 for true, some value for true)
- random.randint(x, y) : returns a random number greater or eqault to x and less than or eqaul to y
- infinite loop 

### Concept 5: [nested for loops]
- for i in range(2,10)
    for j in range(2, 10)
        print(i, "multiplied by", j, "is", i*j)
- len(list) = number of items in the list 
- outer loop vs inner loop
    - inner loop: indented loop inside the outer loop
- you can compare two list by doing a nested for loop with two list and comparing the exat match of two lists

### Concept 6: [Keywords and scope] 
- "continue" : Skip the rest of the current iteration of the loop and continue with the next iteration of the loop (if there is a next iteration) 
    for i in rage(1,21)
        if i % 2 ==0:
            continue
        print(i, "is odd")
    print("Done!") 
    - this will print only odd numbers
- "break" : skip the rest of the current iteration of the loop and break out of the loop altogether, skpping any later iterations too
    - break will just move on to next line of the code
- "pass": designate an "empty' body for a control structure
    - if you want to design the control structrure but haven't wrote down the body in side the control structure, "pass" will let you have an empty line of code without causing error
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
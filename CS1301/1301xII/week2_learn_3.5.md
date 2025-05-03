# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 3.5: Error handling 

---

## 📚 Key Concepts Summary

### Concept 1: [Error]
- catching errors: using error handling to prevent a pgogram from crashing when an error is encountered.
- uncaught errors: an error that is not handled by error handling ocde, and thus usually forces the program to crash. 
- Benefits of error catching
    - program design thought process: it helps you focus on designing the program for its original purpose
    - Organized code
    - Preventing unanticipated errors from crashing the program

### Concept 2: [Try - Catch - Finally]
- The Try statement marks a block of code to attempt, but in which we anticipate an error might arise. 
    - A contorl structure that sets aside a block of code in which an error might occur so that the computer will look error handling capabilities. 
    - 
- The Catch statement names the errors to anticipate, and marks a block of code to run if an anticipated error arises. (Python often refers to this as the Except block as 
well)
    - Contains the code the computer should run if an expected error was encounter in Try block
    - a control structure that designates what error it anticipates in a try block and provides the code to execute if that error arrises. 
    - declares the type of error that should be expected
- The Finally statement marks a block of code to run after the above two blocks no matter what.
    - Contains code that should be exectured after the code in the 'try' block whether it succeeded or not. 
    - a control structure that designates some code to run after a try and catch structure regardless of whether or not an error arose. 
- In python, there is also an Else block for exception handling: it runs some code only if no errors arose in the Try block. 

### Concept 3: [Try and Except]
- try: if an error is encountered, it will jump to catch block (except)
    - try tells the computer it's okay to fail
- except : the execution will run the this except block if some error happens in try block
    - a good place to put some error message.
- Catching a specific error
    - except type of error: the except will run only when the catch body have the type of error that was input on except body. 
    - example
        except ValueError as error: 
            print(error)
            output: the error message but the program doesn't crash. 
- Catching multiple specific errors
    - You can have multiple except 
        try:
            code
        except TypeError as error:
            print(error)
        except ValueError as error:
            print(error)
        except (ValueError or TypeError) as error:
            print(error)
        except ValueError, TypeError, ZeroDivisionError: 
            print(error)
        except Exception as error:   -> handling all other errors that wasnt specified. 
            print("Some other type error occurred") 
        print("Done!")
- Finally block and else
    - else block is code that runs only when try 
    - example 
        try:
        except TypeError as error: 
        except Exception as error: 
        else: 
            print("Yay")
        print("done")
    - else block measn : if there were no errors occured then (else) run the block
- File input
    - open(filename): Takes as input a filename and returns the file. Once returned, the file can be read line by line or wrtten to. depending on the mode. Mode is set with the keyword parameter "mode", "r" for rea, "w" for write, "a"for append.
    - close() : a method that closes the file of which it's a member
- Fiannly block
    - for codes that needs to run regardless of whetehr an error was detected or not. So withi this block, we can cover every possible situdations
    - holds instruction whether we encounter a error or not
    - Except : holds instructions for when we encounter error <> Else: instructions for no error encountered. 
    - example
        filename.close() - we always want to close a file so.. 
    - we can put some error message in case we didn't type the right error on our except code
- Exception as e: 
    print(type(e))
    print(str(e))
- good practice
    - except (error1, error2)
    - class "newname"(Exception): 
        pass
    (insde the try:)
        if xxxxx :
            raise "newname"("error message")
        except "newname" as e: 
            
### Concept 4: [Nested Try-Catch-Else-Fiannly]
- example
    try:
        inputfile = open(filename, mode = "r") 
        try: 
            do something
        except ValueError:
            print(xx)
        else:
            print(yy)
        finally:
            inputfile.close()
    except IOError as error:
        print(something)
### Concept 5: [Early Function Terminations]
- Common idioms in writing functions
    - Go trhough a process of checking for some condition (typically in a loop), and return the moment that condition is met. If the loop ends without that condition being met, return the oppsite result. 

### Concept 6: [Error Handling]
- Error handling in for loops 
    - if we put a loop inside the try body then once we hit one error the loop will stop to run. 
    - so we would rather put the try body inside the loop so the loop will run even afrer we try, catch
-  Error handling in functions
    - handling in side the function
        - having try: except: inside the function
    - handling in the code that calls the function
        - ??? 
## 💻 Code Practice Summary

- [`filename.py`](./filename.py): Description of this coding task
- [`filename.ipynb`](./filename.ipynb): Jupyter notebook summary

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
# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 4.4: File input and output

---

## 📚 Key Concepts Summary

### Concept 1: [File]
- File Input and Output: The complementary processes of saving data to a file and loading data from a file, generally such that the state of the memory of the program is the same after saving and loading have occurred.
- File types
    - how the program should read the files.  set of rules for how to interpret a file, and a program can only correctly interpret the file if it knows those rules.
    - Files can have very specific encoding and this encoding can be read only by 
### Concept 2: [Open and Clsoe]
- file open -> assign to a variable for that open file -> modify -> close file(letting other programs to access/moidfy)
    - file open should be carefully handled because if can crash the program. So handlie with Try can be required
    - Most of the case, when a file is opened it's locked in the OS that doesn't allow other programs to access it. (reason why we have to close the filed at end)
- Opening and closing files often mirror each other: when we're done saving to and loading from a file, the goal is for the program to have the same data stored in memory as if it was never saved in the first place.
- read / write / apending
    - read: we're looking at the file's contents and reading it into our program. We're not changing the contents, just inputting it into our own code.
    - write: writing, we assume the file is a snapshot of the current state of our data, not a running log of the history of all of its changes. When we write to a file, we by default, erase it and rewrite it completely from scratch.
    - appending: starts at the last line of the file. 

### Concept 3: [Writing files in Python]
- How to open file:   variable_name = open("filename_string", "command")
    - command : "w", "r", ""a"  (stands for write, read-only, append)
- How to write to a file:   file_assigned_variable.write("string")
    - .write() can only take strings as input so if we are not inputing strings then we have to explicitly convert it to string
    - .write() doesn't automatically change lines. to do that we have to include + "\n" to add line breaks.
    - write() method cannot take multiple arguments
- How to close a file: variable_name.close()
- How to write a list 
    - use for loop and iterate the items in the list and write each items on the file. 
        - filename.write(listname + "\n")
    - use  ' .writelines(listname)
    - smart way to do it
        - filename.write("\n".join(listname)) : this will change the list into a looong string with multiple breakline character. so this will print the items of list on different lines
        - print(variable, file = file_name_variable) : this will automatically add line break.

- Appending the fiels: use "a" instaed of "w"
    - after opening the file with "a"
    - and then use .write()
    - good for keeping log

### Concept 4: [Reading files in Python]
- how to read : 
    - reading mode :  variable = open("filename", "r")
    - print(variable.readline()) 
    - print(variable.readline())
        - thing to note: readline() is a way to read a file line by line and itself actslike it contains a newline character. so if we put a newline character when writing the file. we will get double line spcaes 
- how to read without dobule line spaces
    - print(variable.readline().strip())
        - strip() basically get rid of anything that doesn't print out visibally. so this will get rid of the \n we put in the string
        - varaible.readline().strip() -> "12\n".strip() -> "12"
    - if we are handling integer, int() will remove newline characters automatically. 
- how to read in one line: read()
    - variable_name = file_variable.read() : will assign the entire content into the variable name
- how to read file into list 
    - create a empty list 
    - open the file in raed mode
    - for i in file_variable: 
    -   list_name.append(i.strip())
    - use strip to get rid of the line break at the end of each lines in a file
- we can read each line and assign it to variables 
    - variable_name = file_variable.readline().strip()
    - vraiable_int = int(file_variable.readline())


### Concept 5: [Save and Load Functions]
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
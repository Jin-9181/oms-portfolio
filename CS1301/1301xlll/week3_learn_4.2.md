# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 4.2: Strings

---

## 📚 Key Concepts Summary

### Concept 1: [string]
- String: A data structure that holds a list, or a string, of characters.
- Character: A single letter, number, symbol, or special character.
- What we naturally understand isn't obvious to computer. We have to make sure they understand our intent
- Unicode: A computing industry standard that sets what hexadecimal codes correspond to what characters, so that text appears consistent across platforms.
    - This unicode is how computer understands our language, file. If a file is input the A in side the character will be broken in to unicodes and then get understand by computer as A
    - Hexadecimal: A short-hand expression of the ones and zeroes that comprise computer data, comprised of 16 characters, 0 through 9 and A through F.
- Charater represents only characters... how do we know when to start a new line? a space?
    - There's a 'new line character'
    - Newline Character: A Unicode character, either LF (line feed) or CR (carriage return), that is rendered as the beginning of a new line of text.
- Three way to declare string:
    - Quotation mark : "", '' 
        - How do we declare quotation mark as part of string? :  Apostrophe
    - Apostrophe: '' for quotation marks 
    - Triple Apostrophe: ''' "I" 'Hi' ''' <- this works. 
- Special Character
    - \n : Line break
    - \ : Python interprets this as escape. So with the following sequence (e.g. n) it will do certain actions
    - \t : Tab
    - \" : not ending the quotation mark. just trying to print quotation mark
    - \\ : telling python to igore the following \. so lets us print thisn such as ' \n ' without breaking the line
    - we can do line break by using ''' because '''(triple apostrophe) will force Python to take everything insdie the string until it meets its pair. so having ''' and actualy enter will make a line break

### Concpet 2: [String Concatenation]
- String Concatenation: The process of putting two or more strings together in order to form one string made of the individual strings. For example, concatenating “A” with “B” would give “AB”.
- Assignment Concatenation: Concatenate by assiging the +  of two strings
- self assignment also works in string concatenation
- \ will let you write code on the next line without breaking the line

### Concept 3: [Slicing] 
- String Slicing: The Python term for obtaining substrings from within a string based on character indices.
- Zero-Indexing: A convention in most programming languages where the first item of a list of items is considered the “0th” item, not the 1st item.
    - why zero indexing? originally indexing meanth, skip x items to access the character inside a string. so the first item becasme index 0 since you have skip 0 item to access the first item. 
- [#] : a.k.a bracket is a way to access the single charater of string
- substring
    - we can use for loop for this. 
    - using[n1:n2] : start from n1 index up to n2 - 1 index
        - we can skip the first number then the Python will assume it is 0
        - we can skpi the second number then the Pytho will assume it is the last character
        - we can still exceed the index of the string with n2 (although we can't pick the index that is at/over n2)
            - it will automtatically stop at the end of the string
            - 
        - If the starting character is after the ending character, the result will be an empty string.
    - using[n1:n2:n3] : start from n1 up to n2(not includign n2) with the gap of n3
        - if  n1 and n2 is empty it's starting from beginning or ending at end
- Negative indices
    -  '-2' index will mean the second last letter ( index -2 for "ABCDE" is "D")
    -  if the idex is over the actual string: it will return empty value
- Remember, string slicing just gives us new strings. We can use those new strings in all the ways we can use normal strings. For example, we can concatenate with them: 
    - "Hello, world!"[:6] + "Hi, CS1301!"[4:] → "Hello, CS1301!"
- And we can also loop over them:
    - for character in "Hi, CS1301!"[4:]:
        - print(character, end = "")
            - ...will output "CS1301!". So, we could loop over every fourth character in a string by using:
            - for character in "Hi, CS1301! Let's loop over every fourth character!"[::4]:
                - print(character, end = "")
                    - ...which will output "HC0Lsoveyu re". 
    - You could even take the slice of a slice: "Hello, world!"[4:][:3] will give you the first three characters (the second slice) of all but the first four characters (the first slice) of that string.

### Concept 4: [String search in Python]
- in operator: Check whetehr a substring is in the string
    - if "BC" in "ABCDE":  == True
    - not in also works. just the other way around
        - if "GH" not in "ABCDE" == True 
- find():
    - how it works: string.find(substring)
    - it returns the index where it is found when the substring is excatly there
    - it returns -1 if the exact match isn't found.
    - re can replace in method by using this. Just compare the result with zero if the result is >= 0, it means it's found and < 0 then not found.
    - find will only return the first index the substring is found(even if there's more than one)
    - find(text, start, end): A method of the string data type that will find the first instance of the value of text within the string calling the method. Optionally, also takes parameters start and end to mark where to search in the string. Returns -1 if text cannot be found.
- rfind(): looking for the last place where it showed.
- startswith(prefix, start, end): True if the string starts with the prefix string
- count(substring, start, end): returns the number of sumbstring found within the start and end. 
- you can't put end without start

### Concept 5: [ String Method]
- split([separator]): A method of the string data type that will split a string up into a list of smaller strings. If a separator string is given, that string will be used to determine where to split; if not, the string will be split by spaces.
    - if you don't put anything for separator it will use space as separater
    - outcome will be ["str1", "str2", "str3", ...] - the separator will be gone
- counting number of words(splited by space) in a string
    - string.count(" ") + 1
    - len(string.split(" ")) <- len(list) will count the values insdie the list
- string.capitalize() : capitalizing the first string character of the entire string into upper case and changing the rest o lower case.
- string.lower() : making all the string character lower case
- string.upper() : making all the string character upper case
- string.title() : capitalizes any character found after the space/special character/tab/linebreak. and then changes all the rest of the letter inside that substring into lower case
- string.strip() : strips out all the whitespaces before and after the string
- string.replace("substring", "replacing string")
- string.split() = list of substruings
- adding_string.join(list of string) = joining the list inside the string using the 'adding_string' as a separator
- all these method won't change the value of a string but it shows the result what if we did chage it.
- split is opposite of join

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
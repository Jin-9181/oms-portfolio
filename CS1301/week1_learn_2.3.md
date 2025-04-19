# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 2.3: Logical Operators 

---

## 📚 Key Concepts Summary

### Concept 1: [operators]
- simplest way to act on data
- Specific, simple functions that act on primitive data types, like integers and strings.

### Concept 2: [mathmatical operator]
- Addition +, subtraction -, multiplication *, division /, modulous %(remainder)

### Concept 3: [logical operator]
- Logical Operators: Operators that perform logical operations, such as comparing relative values, checking equality, checking set membership, or evaluating combinations of other logical operators.
- has only the value of True or False
- Relational operator : Operators that check the relationships between multiple variables, such as checking if they are equal or if one is greater than another.
- Boolean operator : operators check the combination of multiple relational operators.
- Numeric Comparison Operators: Operators that facilitate numeric comparison between values. Typically, these are 'greater than' (>), 'greater than or equal to' (>=), 'equal to' (==), 'less than' (<), and 'less than or equal to' (<=).
    - A string of characters is 'less' than another string if it comes earlier alphabetically. "Apple" would be 'less' than "Banana".
    - A date is 'less' than another date if it comes earlier in time. January 1st, 2017 would be 'less' than January 15th, 2017.
- Non-Numeric Equality Comparisons: Nearly any kind of data can compare for equality, even if it isn't numeric. We can't ask if an apple is greater than an orange, but we can ask if apples and oranges are 'equal', or the same thing.

- Set Operators: Check to see if a value is a member of a set of multiple values. Most often this comes up in strings and lists.
    - With strings, we can check to see if a certain smaller string occurs inside a larger string. For example, "cde" is in the string "abcdefg", but "ijk" is not.
    - With lists, we can check to see if a certain item is on our list. For example, if we had a list containing "grapes", "apples", and "oranges", then "apples" would be in that set, but "papaya" would not.
    - using 'in' as the operator : checks to see if something is contained within a list of other things.
    - 

### Concept 4: [boolean operator]
- Boolean Operators: Operators like “and” and “or” that act on pairs of boolean (true or false) values, or that act on single boolean values, like “not”
- And: An operator that acts on two boolean (true or false) values and evaluates to “true” if and only if both are true.
- Or: An operator that acts on two boolean (true or false) values and evaluates to “true” if and only if at least one is true.
- Not: An operator that acts on one boolean (true or false) value and evaluates to the opposite value (false becomes true, true becomes false). It alternates the value
-  Python evaluates and first, then or.

### Concept 5: [truth table]
- Truth Tables: Tables that map out the results of a statement in boolean logic (that is, using boolean operators) depending on the values of the individual variables.
- 



## 💻 Code Practice Summary

- [`filename.py`](./filename.py): Description of this coding task
- [`filename.ipynb`](./filename.ipynb): Jupyter notebook summary

- print(5 < 3) will be False
- 
---

## 🧠 How I Understand It (In My Own Words)
- all capital letters are sorted before lower lettercase lettes so Z will come before a
- "" are always found in 'in' operator
- computer reads left to right. And parenthesis is a good way to organize long codes. 
- Simplifying Conditionals
- commutative property of boolean operator : with the same operator the order doesn't matter but if you mix operators (and + or) the order starts to matter. pythong evaluates and first then or
    - not is evaluated first.
    - and is evaluated second.
    - or is evaluated third.
- distibutive property : A and (B or c) is same as (A and b) or (A and c) 
- de Morgan's law : 
    - and -> or 
    - not (A and B) = not A or not B
    - not (A or B ) = not A and not B
- Don't try to compare one variable to multiple values.
-  != is the opposite of ==



---

## ❓ Unclear Points / To Revisit
-  
---

## 🗂 Reference Links

- [Official docs / lecture video]()
- [Helpful blog post]()
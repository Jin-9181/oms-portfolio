# 📘 Week [1] Learning Summary

## ✅ Topics Covered
- Chapter 4.5: Dictionary

---

## 📚 Key Concepts Summary

### Concept 1: [Dictionary]
- Dictionaries: A data structure comprised of key-value pairs, where a key is entered into the dictionary to get out a value. Similar to or synonymous with Maps, Associative Arrays, HashMaps, and Hashtables.
- Dictionary Key: A value then, when passed into a dictionary, returns a corresponding value, like a word and its definition. Similar to a variable.
- Dictionary Value: A value returned in response to a key in a dictionary. Similar to a value of a variable outside a dictionary.
- key difference with a list is that unlike list, which we use numeric indices to access the item stored in a list, we can use a key(which can be a non-numeric value) to access the data
- Dictionary in python, doesn't guarantee to preserve order (unlike list) 
- Map (Jave, C) , Associative array (PHP, JavaScript), hashmap hash table..

### Concept 2: [Creating and Accessing Dictionaries]
- using {}
- we need keys and value 
    - key : value
    - new_dic = {"mango" : 5, "apple" : 3}
- keys must be immutable values : string, integer, float, tauple ( can't use list)
    - if the key changes, we won't be able to match it with values 
- Values can change. 
- how to change/access the value 
    - dictionary_name[key_name] += 1 , *= 3, = 5
    - works like assigning new value to a variable
### Concept 3: [Adding to and removing from a dictionary]
- how to add:
    - dictionary_name[new_key_name] = new_value
- hot to remove:
    - del dictionary_name[key_name_to_delete] 
- In other language, if we try to create a new key that already exist, this will triger an error. In python, this will just overwrite
- how to update multiple values
    - .update(key : value, key : value) : this will update, overwrite, create new keys and values
- how to not overwrite 
    - .setdefault(key_name, new_value) : this doesn't overwrite if the key already exisit, it only created key : value when the key already doesn't exist. 
- how to check whether the key exist
    - key_name in dictionary : this is a boolean statement
- dict_name.get()
    - .get(key_name) : returns the value if it exist, returns none if no key
    - .get(key_name, value) : if the key : value already exist it returns the value and if it doesn't exist, creates it.
- defaultdict
    - how to use: from collections import defualtdict
    - dictionary_name = defualtdict(data_type)
        - int, list, dict, etc
        - this will set up a defautl value for keys that doesn't exist. 
        - unlike dict which will cause KeyError when calling a non-exisitng keys

### Concept 4: [Traversing Dictionaries]
- values(): A method of the dictionary type that returns a list of all the values of that dictionary.
- keys(): A method of a dictionary type that returns a list of all the keys in that dictionary.
- items(): A method of a dictionary type that returns a list of (key, value) tuples in that dictionary.
- searching key, value
    - for key in dict.keys():  + if key ==, key < , etc
    - for value in dict.values(): + if value < 5 or something
    - for key in dict.keys(): + value = dict[key]
    - for (key, value) in dict.items():
        - if value < 5: 
            print(key, "is less than", value)

### Concept 5: [Dictionaries and lists]
- we can store lists or tauples as a value in dictionary
- lists for multiplees values with same qualatative charaterirstisc.
- tauples for different qualitative values
- dictionaries of dictionaries
    - creating a dictionary as a value to a name (key) : and that sub-dictionary will hold address, phone number, emails as key with a corresponding value
- we can trea lists as value in dictionary as normal list
    - dict_name[list_as_key_name].append[value] works
    - accessing values : dict_name[key_name][index]

- the first value we create for a key in dictionary will determine the data type of the value. so we have to explicitly assign the right data type. int, str, list, tauple 
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
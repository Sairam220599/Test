# Basic Python
## 1. Data Types:-
### i. Containers
Containers are any object that holds an arbitrary number of other objects. Generally, containers provide a way to access the contained objects and to iterate over them.

In the collections there are some container datatypes, which are alternatives to python’s general purpose built-in containers like dict, list, set etc.

**Some of the containers are-**

**1) namedtuple():**
Used to create tuple subclass with the name field

**2) deque:**
Queue using list type data

**3) Counter:**
Subclass of dict to count the hash-table objects

**4) ChainMap:**
Used to create single view of multiple mappings

**5) OrderedDict:**
Subclass of dict, where data are added in ordered manner

**6) UserList:**
Wrapper for list to easier access.

### ii. Lists
A list is a collection which is **ordered** and **changeable**. In Python lists are written with square brackets.

It can store many data types such as integers,characters, strings, lists(nested list), dict etc and it is not necessary that all elements are of same type.

**Syntax of initialization-**

my_list = [1,2,3]

**or**

my_list = list()

**Some useful method used with Lists-**

**1) append():** 
Adds an element at the end of the list

**2) index():**
Returns the index of the first element with the specified value

**3) insert():**
Adds an element at the specified position

**4) pop():**
Removes the element at the specified position

**5) remove():**
Removes the item with the specified value

**6) reverse():**
Reverses the order of the list

**7) sort():**
Sort the list.

### iii.Dictionaries ###

A dictionary is a collection which is unordered, changeable and indexed.

In Python dictionaries are written with curly brackets, and they have keys and values.

**Example of a Dictionary-**

```
my_dict = {
  "Sport": "Football",
  "tournment": "UEFA",
  "Venue": "Madrid" 
}
```



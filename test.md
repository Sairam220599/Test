# Basic Python
## 1. Data Types:-
### i. Containers
* Containers are any object that holds an arbitrary number of other objects. Generally, containers provide a way to access the contained objects and to iterate over them.

* In the collections there are some container datatypes, which are alternatives to python’s general purpose built-in containers like dict, list, set etc.

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
* A list is a collection which is ordered and changeable. In Python lists are written with square brackets.

* It can store many data types such as integers,characters, strings, lists(nested list), dict etc and it is not necessary that all elements are of same type.

**Syntax of initialization-**

```my_list = [1,2,3]```

**or**

```my_list = list()```

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

### iii. Dictionaries ###

* A dictionary is a collection which is unordered, changeable and indexed.

* In Python dictionaries are written with curly brackets, and they have keys and values.

**Example of a Dictionary-**

```
my_dict = {
  "Sport": "Football",
  "tournment": "UEFA",
  "Venue": "Madrid" 
}
```

* We can access elements/values using the keys of the dictionary instead of index.

* You can change the value of a specific item by referring to its key name-

``` my_dict["Venue"] = "Berlin" ```


### iv. Sets ###
* A set is a collection which is unordered and unindexed. 

* In Python sets are written with curly brackets.

**Example of a Set-**

``` my_set = {Cricket, Football, Tennis, Hockey} ```

* The major advantage of using a set, as opposed to a list, is that it has a highly optimized method for checking whether a specific element is contained in the set.

**Some useful method used with Sets-**

**1) difference:():**
Returns a set containing the difference between two or more sets.

**2) intersection():**
Returns a set, that is the intersection of two other sets.

**3) union():**
Return a set containing the union of sets

**4) issubset():**
Returns whether another set contains this set or not

**5) symmetric_difference():**
Returns a set with the symmetric differences of two sets

### v. Tuples ###

* A tuple is a collection which is ordered and unchangeable.

* In Python tuples are written with round brackets.

* The sequence of values stored in a tuple can be of any type, and they are indexed by integers.

**Example of a Tuple-**

``` my_tuple = ('python', 'C++', 'Java') ```


## 2. Functions ##

* A function is a set of statements that take inputs, do some specific computation and produces output.

* The idea behind is to not to repeat the same thing which is also called **Don't Repeat Yourself**(DRY) Principle.

* In Python a function is defined using the def keyword:

``` 
def my_function():
    print("Hello World!")
```

* To call we just need to write the function name with open and close parenthesis.

``` my_function() ```

* We can pass arugments to a function and return a value from the function.

``` 
def add(a,b):
    return a+b
```

* Now to call the function we need to pass arguement to it and assign it to a variable.

``` sum = add(5,10) ```


## 3. Claases ##

* Almost everything in Python is an object, with its properties and methods.

* A Class is like an object constructor, or a _blueprint_ for creating objects.

* Classes are created by keyword class-

``` 
class my_class:
    x = 10
    y = 5
```

* Now, we can create object of the class my_class and access the atrributes(x and y) of the class-

```
obj = my_class()
print(obj.x)
```

* All classes have a function called __init__(), which is always executed when the class is being initiated.

```
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)
```


## 4. Numpy ##

* NumPy is a Python package. It stands for 'Numerical Python'. It is a library consisting of multidimensional array objects and a collection of routines for processing of array.

* The conventional way of importing the NumPy package is as follows-

``` import numpy as np ```

### i. Arrays ###

* The most important object defined in NumPy is an N-dimensional array type called ndarray.

* It describes the collection of items of the same type. Items in the collection can be accessed using a zero-based index.

**Example**

```
Live Demo
import numpy as np 
a = np.array([1,2,3]) 
print a
```

* The shape attribute returns a 

 














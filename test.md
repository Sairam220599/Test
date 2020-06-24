# Basic Python
## 1. Data Types
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


## 3. Classes ##

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
print (a)
```

* The shape attribute returns a tuple consisting of array dimensions. It can also be used to resize the array.

```
import numpy as np 
a = np.array([[1,2,3],[4,5,6]]) 
print (a.shape)
```

* Resizing-

```
import numpy as np 

a = np.array([[1,2,3],[4,5,6]]) 
a.shape = (3,2) 
print a 
```

### ii. Array Indexing ###

*  Items in ndarray object follows zero-based index.

* Three types of indexing methods are available − field access, basic slicing and advanced indexing.

*  A Python slice object is constructed by giving start, stop, and step parameters to the built-in slice function. This slice object is passed to the array to extract a part of array.

**Example**

```
import numpy as np 
a = np.arange(10) 
s = slice(2,7,2) 
print (a[s])
```

* If only one parameter is put, a single item corresponding to the index will be returned.

* If a : is inserted in front of it, all items from that index onwards will be extracted.

* If two parameters (with : between them) is used, items between the two indexes (not including the stop index) with default step one are sliced.

```
import numpy as np 
a = np.arange(10) 
b = a[5] 
print (b)          # slice single item 
print(a[2:])       # slice items starting from index 
print(a[2:5])      # slice items between indexes
```

**Boolean Array Indexing**

* This type of advanced indexing is used when the resultant object is meant to be the result of Boolean operations, such as comparison operators.

**Example**

```
import numpy as np 
x = np.array([[ 0,  1,  2],[ 3,  4,  5],[ 6,  7,  8],[ 9, 10, 11]]) 
print 'The items greater than 5 are:' 
print x[x > 5]      # Now we will print the items greater than 5 
```

### iii. Data Types ###

* NumPy supports a much greater variety of numerical types than Python does.

* Some of the data types defined in NumPy are bool_ , int_ , float_ , complex , and many more.

**Data Type Objects(dtype)**

* A data type object describes interpretation of fixed block of memory corresponding to an array, depending on the following aspects −
  
  * Type of data (integer, float or Python object)
  
  * Size of data
  
  * Byte order (little-endian or big-endian)
  
  * In case of structured type, the names of fields, data type of each field and part of the memory block taken by each field
  
  * If data type is a subarray, its shape and data type
  
* A dtype object is constructed using the following syntax −

``` numpy.dtype(object, align, copy) ```

* The parameters are −

  * Object − To be converted to data type object

  * Align − If true, adds padding to the field to make it similar to C-struct

  * Copy − Makes a new copy of dtype object. If false, the result is reference to builtin data type object

**Example**

```
import numpy as np 
dt = np.dtype(np.int32) 
print dt
```
  
### iv. Array Math ###

*  NumPy contains a large number of various mathematical operations.

* NumPy provides standard trigonometric functions, functions for arithmetic operations, handling complex numbers, etc.

**1. Trignometric Functions**

* NumPy has standard trigonometric functions which return trigonometric ratios for a given angle in radians.

```
import numpy as np 
a = np.array([0,30,45,60,90]) 

# Convert to radians by multiplying with pi/180 
print (np.sin(a*np.pi/180))   

print (np.cos(a*np.pi/180)) 

print (np.tan(a*np.pi/180))
```

**2. Arithmetic Functions**

* Input arrays for performing arithmetic operations such as add(), subtract(), multiply(), and divide() must be either of the same shape or should conform to array broadcasting rules.

**Example**

```
import numpy as np 
a = np.arange(9, dtype = np.float_).reshape(3,3) 
b = np.array([10,10,10]) 
print (np.add(a,b))       # addition of two arrays

print (np.subtract(a,b))  # subtraction of two arrays

print (np.multiply(a,b))  # multiplication of two arrays

print (np.divide(a,b))    # Division of two arrays
```

**3. Statistical Functions**

* NumPy has quite a few useful statistical functions for finding minimum, maximum, percentile standard deviation and variance, etc. from the given elements in the array.

**Examples of some statistical functions-**

```
import numpy as np 
a = np.array([[3,7,5],[8,4,3],[2,4,9]]) 

print (np.amax(a))      # returns smallest value in array
print (np.amin(a))      # returns largest value in array

print(np.mean(a))       # mean of the array
print(np.median(a))     # median of the array
print(np.std(a))        # standard deviation of the array
```

### v. Broadcasting ###

* The term broadcasting refers to the ability of NumPy to treat arrays of different shapes during arithmetic operations.

* Arithmetic operations on arrays are usually done on corresponding elements. If two arrays are of exactly the same shape, then these operations are smoothly performed.

**Example**

```
import numpy as np 

a = np.array([1,2,3,4]) 
b = np.array([10,20,30,40]) 
c = a * b             # broadcasting for element wise multiplication.
print (c)    
```

## 5. Matplotlib ##

* Matplotlib is one of the most popular Python packages used for data visualization.

* Matplotlib is written in Python and makes use of NumPy, the numerical mathematics extension of Python.

* It is a cross-platform library for making 2D plots from data in arrays.

### i. Plotting ###

* To begin with, the Pyplot module from Matplotlib package is imported, with an alias plt as a matter of convention.

``` import matplotlib.pyplot as plt ```

* Now we can create arrays to be plotted on the x axis and y axis.

```
x = np.arange(0, math.pi*2, 0.05)
y = np.sin(x)
```

* The values from two arrays are plotted using the plot() function.

``` plt.plot(x,y) ```

* You can set the plot title, and labels for x and y axes.

``` 
plt.xlabel("angle")
plt.ylabel("sine")
plt.title('sine wave')
```

* The Plot viewer window is invoked by the show() function −

``` plt.show() ```

### ii. Subplots ###

* Matplotlib’spyplot API has a convenience function called subplots() which acts as a utility wrapper and helps in creating common layouts of subplots, including the enclosing figure object, in a single call.

``` plt.subplots(nrows, ncols) ```

* The two integer arguments to this function specify the number of rows and columns of the subplot grid.

* The function returns a figure object and a tuple containing axes objects equal to nrows*ncols. Each axes object is accessible by its index.

**Example for creating a 2x2 subplots**

```
import matplotlib.pyplot as plt
fig,a =  plt.subplots(2,2)
import numpy as np
x = np.arange(1,5)
a[0][0].plot(x,x*x)
a[0][0].set_title('square')
a[0][1].plot(x,np.sqrt(x))
a[0][1].set_title('square root')
a[1][0].plot(x,np.exp(x))
a[1][0].set_title('exp')
a[1][1].plot(x,np.log10(x))
a[1][1].set_title('log')
plt.show()
```

### iii. Images ###

* The image module in Matplotlib package provides functionalities required for loading, rescaling and displaying image.

* The imread() function is used to read image data in an ndarray object of float32 dtype.

```
import matplotlib.pyplot as plt
import matplotlib.image as mpimg
import numpy as np
img = mpimg.imread('mtplogo.png')
```

* Any array containing image data can be saved to a disk file by executing the imsave() function. Here a vertically flipped version of the original png file is saved by giving origin parameter as lower.

``` plt.imsave("logo.png", img, cmap = 'gray', origin = 'lower') ```

* To draw the image on Matplotlib viewer, execute the imshow() function.

``` imgplot = plt.imshow(img) ```


## 5. Jupyter Notebook ##

* Jupyter Notebooks are a powerful way to write and iterate on your Python code for data analysis. Rather than writing and re-writing an entire program, you can write lines of code and run them one at a time.

* Then, if you need to make a change, you can go back and make your edit and rerun the program again, all in the same window.

* 








 














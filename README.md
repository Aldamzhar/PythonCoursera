# PythonCoursera

## This is the repo for the Coursera course on Python and everything I learned from it


Python Interpreter = it is the program that runs behind the scenes, which takes 
			the input and transforms it into the output in Python
			 Language

Even if we write the 100 into the source code and run through the interpreter,
it will evaulate the expression and take the output for it. In this case,
100 has nothing to output, so there is no output


Expressions are building blocks of programming


print(some_exp1 +-*/ some_exp2) ===> evaluates the expression and then prints it

print(10//3) ---> 3, because the // is division to get the integer part

print(10 ** 2) ---> 100, ** is the math degree operator 

print(10%3) ---> 1, modulo operator, to get the remainder

Order of completion of operations: 

	1) Parentheses
	2) Exponentiation
	3) Multiplication and Division
	4) Subtraction and Addition
	5) Comparison
	6) Not
	7) And Or

print(18.0 // 4) ---> prints out 4.0, because 18.0 is float and result would be float too

"#" represents comment 

functions are objects in Python 

print(square) ---> <function square>

## Data Types

print(type("Hello World")) ---> <class 'str'>
print(type(17)) ---> <class 'int'> 
print(type(3.2)) ---> <class 'float'>

To create a string use: '', "", """ """, ''' '''

print(42, 500) ---> 42 500

## Type Conversion Functions

during the conversion of float to int, it just cuts off the decimal part and then 
makes, for example, 3.9999 to 3

Function Call                  |   Output
			      
print(3.14, int(3.14))         |   3.14 3 
print(3.9999, int(3.9999))         3.9999 3
print(3.0, int(3.0))	       |   3.0 3 
print(-3.999, int(-3.999))         -3.9999 -3
                               |
print("2345", int("2345"))     	   2345 2345 	
print(17, int(17))             |   17 17
print(int("23bottles"))            ValueError 


print(float("123.45"))             123.45
print(type(float(123.45)))         <class 'float'>


print(str(17))                     17
print(str(123.45))                 123.45
print(type(str(123.45)))           <class 'str'>

## Variables 

1) Setting Variables

	message = "Hi"
	n = 17
	pi = 3.14159

2) Reference variables
 
	print(message) --> Hi
	print(n)       --> 17
	print(pi)      --> 3.14159

## Statements and Expressions

Statement is a complete instruction that the Python Program executes

x = 1 + 2 + 3 is a statement
1 + 2 + 3 is an expression 

len(string) prints out the length of string (number)

Python Evaluates the expression in steps:
	
	1) Evals function itself
	2) Evals args (left-right) 
	3) Call function 

add(square(y), square(x))

1) add
2) square(y), square(x)
3) does call them (add(y^2, square(x)), add(y^2, x^2), y^2 + x^2)


## Updating the variables 

x = 6  (output is 6)

x = x+1 (output is 7)


x+=3 or x-=3 (x plus 3 or minus 3 on itself)


## Input

n = input("Please enter your name: ")
print("Hello", n)     

[if the n = "Steve"] --> Output: Hello Steve 

## Turtle Graphics 

	import turtle                # make turtle Graphics Library available
	wn = turtle.Screen()	     # make a screen
	alex = turtle.Turtle()	     # makes a turtle (arrow), name is alex
	alex.forward(150)            # forward method, . is access to this method
	alex.left(90)                # left by 90 pixels
	alex.forward(75)	     # forward by 75 pixels
	alex.salary = 50000          # attribute of alex salary is 50000
	print(alex.salary) 	     # in output console there is 50000

alex is instance of Turtle Class
wn is instance of Screen Class

forward, left are methods


## Herd of Turtles 

	import turtle 
	wn = turtle.Screen()    # Set up the window and its attribute
	wn.bgcolor("lightgreen") # The background color of the window is lightgreen
	
	tess = turtle.Turtle()  # create a tess and set its pen width with 5 pixels
	tess.pensize(5)

	alex = turtle.Turtle()  # create alex
	alex.color("hotpink")  # set his color as a hotpink

	tess.forward(80)
	tess.left(120)
	tess.forward(80)
	tess.left(120)
	tess.forward(80)
	tess.left(120)           # tess goes full triangle

	tess.right(180)
	tess.forward(80)          # turns 180 and goes from the origin away

	alex.forward(50)
	alex.left(90)
	alex.forward(50)
	alex.left(90)
	alex.forward(50)
	alex.left(90)
	alex.forward(50)          # full square by pink alex

	wn.exitonclick()           # if somebody clicks on window, it disappears


## For loop

	for var_name in range(3):      # executes this code 3 times, var_name is variable name    
		[somecode]

	


## More Turtle Methods

	import turtle 
	wn = turtle.Screen()
	wn.bgcolor("lightgreen")
	tess = turtle.Turtle()
	tess.color("blue")
	tess.shape("turtle") # shape is turtle

	dist = 5
	tess.up()   # lift the pen up, so line is not drawn behind the turtle        

	for _ in range(30):
		tess.stamp()  # stamps turtle impression on the window
		tess.forward(dist)
		tess.right(24)
		dist = dist + 2 # makes a spiral in the end

	wn.exitonclick()

	
alex.speed(10) # 1 is slowest, 10 is highest animation speed, 0 is turn of animation and move as fast as possible


## Importing modules

	import random    # randomizer library 
	
	prob = random.random() # returns floating point number between 0 and 1 

	diceThrow = random.randrange(1,7) # return an int, one of 1,2,3,4,5,6


random.name_of_function() # invoke the function of random library


	from random import randrange, random # now we don't have to mention library in the function calls in below 2 invocations  
	
	prob = random()

	diceThrow = randrange(1,7)


## Debugging (Syntax, Runtime and Semantic Errors)

Syntax error == statements aren't well formed, interpreter can't parse it

Runtime error == illegal operation happened (3/0 or 5/0)

Semantic error == produces output that is not intended 

## Know your Error Messages 

NameError == you have used a variable before it has a value

 
## Incremental Programming 

Program and check, program and check each time (one-two steps at a time)

## Common Errors 


NameError, SyntaxError, TypeError ==> expression tries to combine 2 objects of types that should not be combined


## Sequence mutation

There are 2 ways to change the value of the object you've created:

	1) You can make a modified copy of it
	2) Modify the original

2) is called mutation


## String, Lists and Tuples

All these are the types of sequences

Sequence is an ordered collection, has an order, length

## Strings

String is the sequence of characters

	s = "Hello World"


## Lists 

List is a sequence of any type of value 


	myList = ["one", 5, "three"]

	print(myList) # prints everything there in square brackets

	List = [] # empty one


## Tuples

Tuples are just like lists, but they are immutable (cannot be changed after they have been created)

	myList = ["one", 5, "three"]	# list
	myTuple = ("one", 5, "three")   # tuple
		
	myTuple = (100)  # confused with type int
	myTuple = (100, ) # class tuple
	
	myTuple = () # empty tuple


## Index Operator

Indexing allows us access the certain element in the sequence

	s = "Python"

	s[0] # first element

	s[-1] # last element 
	s[-2] # prelast, same with lists and tuples

## Slice operator

	julia = ("Julia", "Roberts", 1967, "Actress")

	julia[2]  # 1967
	julia[2:4] # [1967, "Actress"]

	julia[:3] # from beginning to the 3rd, 3rd not included

	julia[5:] # from 5th to the end

## Concatenation and repetition operator

	[1,2] + [3,4]  # [1,2,3,4]

	[0]*4 # [0,0,0,0]


## Count and Index

	a = "I have had an apple on my desk before!"

	print(a.count("e"))  # number of e's in a, is 5
	print(a.count("ha"))  #  ha's are 2


works for list too

Index gives the position where the instance met for the first time

	music = "Pull out your music and dancing can begin"
	bio = ["Metatarsal", "Metatarsal", "Fibula", [], "Tibia", "Tibia", 43, "Femur", "Occipital", "Metatarsal"]

	music.index("m") # 14
	music.index("your") # 9

	bio.index("Metatarsal") # 0 
	bio.index([]) # 3
	bio.index(43) # 6


if not in the list, index() gives runtime Error


## Split and Join

Split == turns string into list of substrings


	song = "The rain in Spain..."
	wds = song.split() 
	print(wds) # ["The", "rain", "in", "Spain..."]

	'leaders and best'.split("e") # ["l", "ad", "rs and b", "st"]

Join == takes a list of strings and joins it into one long string

	"/".join(["leaders", "and", "best"])   # "leaders/and/best"
			
Append == adds element to the list

	lst.append(elem)

Remove == removing an element inside the list, list is changed but not creating new one

	lst.remove(elem)

## For loop

	List (name is name of loop variable)

	for name in ["1st", "2nd", "3rd"]:
		print(name)     # prints 1st 
					 2nd
					 3rd

	Strings (achar is name of loop variable)

	for achar in "Go Spot Go":
		print(achar)   # G
				 o 
				
				S and so on

	
In loops, list or string elements are assigned to loop variables each iteration

## Range function 

	for i in range(0,5):
		print(i) # prints numbers from 0 to 4, newlined

range(5) ---> [0,1,2,3,4]


 
## Boolean Expressions

Booleans == truth values: true or false

## Logical Operators 

	expr1 and expr2
	expr1 or expr2
	not expr1


## In and not in operator 

	'p' in 'apple'  # checks whether thing on the left is part of thing on the right (True)
	't' not in 'apple' # true

'in' works with lists


## Conditional Execution

	if something:
		somecode
	else:
		some other code

OR

	if some:
		something
	elif someother:
		someothercode
	else:
		somefinalthing


## Mutability 

Lists are mutable (values of it can be changed, it can be prolonged, shortened and so on)

	alist[1:3] = ['x','y'] # replaced 1st and 2nd with x and y


Strings aren't mutable (can't change the characters or strings themselves)


Can create new string and take a slice of old one

## List element deletion

	a = [1,2,3]
	del a[1] # now a is [1,3]


	alist = [1,2,3,4,5,6]
	del alist[1:5] # a is [1]


## Objects and references

	a = "banana"
	b = "banana"

	a is b # true

is asks whether a and b are pointing or referencing the same object (string banana)

it works that way with strings 


But with lists 

	a = [1,2,3]
	b = [1,2,3]

	a is b # false, a points to one, b points to another but with same contents

	a == b # true, cause contents are the same 

	id(a) # ids of objects 
	id(b) #	


# Aliases

if you change one of two aliases bound to the same object, then second one is also changed 

	a = [1,2,3]
	b = [1,2,3]  # different objects

	a is b # false

	b = a # now point to the same object

	a == b # true
	a is b # true

	b[0] = 5 # b is [5,2,3], and a is [5,2,3] too


## Cloning lists

Cloning list makes entirely new copy of older list, but objects are not connected, it is just a copy

	a = [1,2,3]

	b = a[:] # cloning, making exact copy

	b[0] = 5 # b is [5,2,3], but a is [1,2,3]



When concatenating list to older one, it just extends older one, but not affecting aliases


## Methods on Lists

.append() # adds to the end of the list

.insert(position_to_insert_to, the_element_to_insert) # goes there, insert the element even if between existing elements

.count(value) # how many of the elements in list equal to value?  

.index(value) # at which position value can be found

.reverse() # reverse the list, same list 

.sort() # from smallest to biggest

.remove(element) # element is removed from the list

.pop() # removes the last element from the list


## Append VS Concatenate

.append() # adds to the end of the list, same list remains

lst = lst + some_list # makes a copy of the same list but with addition from the some_lis

	origlist = [1,2,3] 
	aliaslist = origlist  # aliaslist ---- (both point to the list)
				origlist ----|--> [1,2,3]
	
	origlist += ["cat"] # now, origlist ----> [1,2,3,"cat"]--
				   aliaslist -------------------| same changes applied to aliaslist 
	origlist = origlist + ["cow"]

## Non-mutating methods on Strings

These are the methods that produce a new one based on the old one

.upper() # all capital letters in new str

.lower() # all letters are lowered 

.count("Some_string") # number for occurences of some_string in the string itself

.strip() # gets rid of the whitespaces in beginning and at the end

.replace("old_substring", "new_substring") # creates a new string but replaced the old chunk with new chunk, but original remain the same

str() # typecast into the string type

"String {}. This is {}".format(name1, name2) # String name1. This is name2

"{:.2f} ...".format(somestr) # :.2f is floating point number, 2 digits after decimal point, more precise, default is 3 decimal places

 
## Reading a file 

Open the file:

	fileref = open("file.txt", "r") # r for read, returns the file object

After some manipulation and actions, close the file

	contents = fileref.read() # read function returns all contents of a file, in one string



	lines = fileref.readlines() # returns a list of strings, one string for each line in the file 

	print(lines[:4]) # returns first 4 lines of file as a list


	for line in fileref: # go over the whole file 
		print(line.strip()) # and extract line by line without newlines (strip gets rid of whitespaces, newlines)



	print(contents[:100]) # first 100 characters of these contents

	fileref.close() # closing the file 

	
## Finding a file in FileSystem 

If you have a Python Program in a directory and you have to access the file in a parent one, then you have to get up a level

	somefile = open('../somefiledir/somefile.txt')  # relative path

.. means go up a level in a parent directory

	somefile = open('/user/adminname/files/projs/data.txt') # absolute path (not preferable)


## Writing to a file

	file_obj = open("squares.txt", "w")

	for number in range(13):
		square = number**2
		file_obj.write(str(square)) # writing to a file 13 squared numbers from 0 to 12 
		file_obj.write('\n')	

	file_obj.close()


We still can access the file even if it's closed for reading when didn't reload the page 

	new_file_obj = open("squares.txt", "r")
	print(new_file_obj.read()[:10]) # prints first 10 characters inside the file


## Using 'with' for Files

	with open('mydata.txt', 'r') as md:     # equivalent of 'md = open('mydata.txt', 'r')'
		for line in md:
			print(line)             # after that line, 'md.close()' occurs behind the scenes, we don't have to explicitly write that line, because with does it for us


## .csv format 

'csv' stands for Comma Separated Values 

just a text file that follows some conventions, values are going to be separated by a comma, 
every line of the file will have the same structure  

						
## Reading a .csv file 

	fileconnection = open("olymics.txt","r")
	lines = fileconnection.readlines() # list of lines
	for lin in lines[:6]:
		print(lin.strip()) # printing individual line without newlines

	header = lines[0]
	field_names = header.strip().split(',') # take the 0th element of the list, which is string  and split it, which means create a list of its substrings of that string
	print(field_names) # ['1st','2nd', '3rd']

	
## Writing to a .csv file 

	outfile = open("reduced_olympics.csv", "w")

	outfile.write('name,age,sport')
	outfile.write('\n')

	outfile.close()

Use format to then input it to csv file

Can use join method too, but confusing

Concatenation but not recommended


## Dictionaries

Dictionaries are unordered collection of items, bag of key/value pairs

	eng2sp = {} # Creating a dictionary

	eng2sp['one'] = 'uno' # one key and one value, key = 'one', value = 'uno'
	eng2sp['two'] = 'dos' # Create another key value pair
	eng2sp['three'] = 'tres'

Keys can be almost any type of object and values can be any type of object


Also can declare dictionary like this:

	eng2sp = {'one':'uno', 'two':'dos', 'three':'tres'}

Access the value of the key:

	eng2sp['one'] # will be 'uno'


	
## Dictionary Operations

	inventory = {'apples':430, 'bananas':312, 'oranges':525, 'pears':217}

	del inventory['pears'] # Get rid of key value pair (pears 217)

	inventory['pears'] = 0 # Update the value of key 'pears', now 0 

	numItems = len(inventory) # Returns number of key-value pairs in this dictionary, it is 4

## Dictionary Methods

	inventory = {'apples':430, 'bananas':312, 'oranges':525, 'pears':217}

	for key in inventory.keys(): # .keys() method gets all the keys from dictionary, doesn't matter in which order
		print(key, "has the value", inventory[key]) # and then access all the values associated with each key

	key = list(inventory.keys()) # make the list of keys a list by list() method

	
	for key in inventory: # also returns just keys
		print(key)

	
	inventory.values() # all values of keys
	inventory.items() # items of key-value pairs written in tuples

	
	'apples' in inventory # boolean value, True as the key is in dictionary


	inventory.get('apples') # same as inventory['apples'] = 312 as output

But if the key was not in dictionary, say 'cherries'

	inventory['cherries'] # will get the KeyError
	inventory.get('cherries') # will be output: None

Also, if the key is not here, and there is a second parameter added in get() function, such as 0,  then make the output value associated with this key 0, instead of None
	
	inventory.get('cherries',0) # Output will be 0, but key-value pair of this is not added 


## Aliasing and copying with Dictionaries

	opposites = {'up':'down', 'right':'wrong', 'true':'false'}
	alias = opposites # points to exact same object as opposites

	print(alias is opposites) #  True

	alias['right'] = 'left' 
 	print(opposites['right']) # now it is left, because they are connected 



## Packages 

Packages = directory of Python Scripts

Each script = module 

Specify functions, methods and types

Thousands of packages available: numpy, matplotlib, Scikit-learn

pip = package management system on python

importing package to use

```python
import numpy as np

np.array([1,2,3])
```

## Numpy

Numeric Python = Alternative to Python List

Calculations over entire arrays

Easy and fast


```python
import numpy as np

np_height = np.array(height)

np_weight = np.array(weight)

bmi = np_weight/np_height**2 # works fine in numpy but errors with list
```

Numpy arrays contain only one type!


## 2D numpy arrays

Just create a list of lists in numpy arrays

.shape # (2,5) 2 rows, 5 columns

np_2d[0][2] # 3rd element of 1st list

np_2d[0,2] # same


np_2d[:, 1:3] # take elements from 1st to 3rd index not included, in all lists

np_2d[1, :] # take everything from 2nd list


## Basic Statistics with numpy

.mean() # mean value 

.median() # median

.corrcoef() # correlation between values

.std() # standard deviation

.sum(), .sort() # others, but fast! Because in numpy array, every element is of the one type

.normal() # normalize

.column_stack() 


## Object Oriented Programming

OOP = Flexible, powerful paradim where classes represent and define concepts, while objects are instances of classes

Attributes = characteristics associated with the type

Methods = functions associated with the type

Example:

Apple = class

Flavor and color = attributes

Cut, eat = methods 


```python
dir("") # will show all attributes and methods related to a class<string> ("")
help("") # will show all documentation to the corresponding class of an object 
```

__methodname__ methods are usually not called explicitly but called internally in Python

for example, __len__ is called by len() function which we may call in a program


## Defining new classes

```python
class Apple: # class keyword for defining class
    flavor = "" # defining attributes flavor and color for apple class
    color = ""  
	

jonagold = Apple() # create a new object of class Apple 

jonagold.flavor = "sweet"
jonagold.color = "red"

print(jonagold.color.upper()) # RED
print(jonagold.flavor) # sweet

```

"." Dot notation = lets access to any of the methods and attributes object has


## Instance Methods

```python
Class Piglet:
  name = "piglet"
  def speak(self): # self represents the instance that the method is being executed on
    print("oink! I'm {}!".format(self.name)) # This means that it accesses the attribute name from the current instance of Piglet

hamlet = Piglet()

```

## Constructors and Other special methods

Constructor = method that is called when you call the name of the class

```python
class Apple:
  def __init__(self, color,flavor): # always named "init"
    self.color = color
    self.flavor = flavor
  def __str__(self):
    return "This apple is {} and {}".format(self.color, self.flavor)

jonagold = Apple("red", "sweet") 
print(jonagold) # prints now the message cleaner than bunch of numbers saying position at a computer's memory, str special method helped us
```

## Documenting Functions, Classes and Methods

Docstring = brief text explains what something does

```python
help(Apple) # Shows documentation on what methods there are in our defined class

def to_seconds(hours, minutes, seconds):
  """Returns the amount of seconds in given hours, minutes and seconds"""
  return hours*3600 + minutes*60 + seconds

help(to_seconds) # shows the comment in function that briefly explains it	
```

## Inheritance

Inheritance = lets programmer build relationships between concepts and group them together

This allows us to reduce code duplication by generalizing our code

```python
class Fruit:
  def __init__(self, color, flavor):
    self.color = color
    self.flavor = flavor

class Apple(Fruit):
  pass

class Grape(Fruit): # Apple and Grape classes inherit from Fruit class, they are called siblings
  pass 

g_smith = Apple("green", "tart")
carnelian = Grape("purple", "sweet")
```

Inheriting classes will have the same attributes and methods in children classes 

We can make them behave differently

```python
class Animal:
  sound = ""
  def __init__(self,name):
    self.name = name
  def speak(self):
    print("{sound} I'm {name}! {sound}".format(name = self.name, sound=self.sound))

class Piglet(Animal):
  sound = "Oink!"

hamlet = Piglet("Hamlet")
hamlet.speak() # Oink! I'm Hamlet! Oink!

class Cow(Animal):
  sound = "Moooo"

milky = Cow("Milky White")
milky.speak() # Moooo I'm Milky White! Moooo
```


## Composition

Composition = use of the code in the other classes by calling their methods

Always initialize mutable attributes in a constructor!!!

```python
class Repository:
  def __init__(self):
    self.packages = {}
  def add_package(self, package):
    self.packages[package.name] = package
  def total_size(self):
    result = 0
    for package in self.packages.values():
      result += package.size
    return result
```

## Python Modules 

Modules = used to organize functions,classes and other data together in a structured way

Python Standard Library

```python
import random
import datetime

now = datetime.datetime.now() # date and time right now
now.year # 2020
random.randint(1,10) # generate random number between 1 and 10
```


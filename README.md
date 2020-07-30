# Python3 Programming course on Coursera

## This is the repo for the Coursera courses on Python and everything I learned from them


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


Namespace is an environment where all names are unique

In Python, there was one global or top-level namespace, then each invocation of a function creates a new namespace

Implicit tuple packing is when Python automatically packs the values written by comma into one tuple without explicitly marking parentheses

Unpacking tuple conveniently:

```python
name, age = julia # julia is tuple of ("Zane", 23) for example
```
Passing tuple to a function:

```python
def add(x,y)
  return x + y

print(add(3,4))
z = (5,4)
print(add(*z)) # unpacking the tuple by sending as a parameter with asterisk to a function
print(add(z)) # without it, there will be TypeError of 1 given argument instead of 2
```

Listener loop is the while loop which terminates if the input variable in condition is met

Listens to the input() from the user 

## Optional parameters

```python
def f(a, L=[]):
  L.append(a)
  return L

f(1) # After this, list is [1]
f(2) # [1,2]
f(3) # [1,2,3] When we mutate the default parameter, it can affect the future function calls
f(4,["Hello"]) # Separate list, separate object ["Hello", 4]
f(5,["Hello"]) # ["Hello", 5]
```

## Keyword parameters

```python
def f(x, y=3, z=7):
  code

f(x=1, z=5) # y is 3, and x and z are specified, keyword parameters

f(z=5, x=4) # order is not important
```
keyword parameter should always come after positional arguments like this:

f(10,z=4)

## Lambda expressions

Lambda expressions are alternative ways to define function

```python
def func(args): #usual way
  return ret_val

func = lambda args: ret_val # lambda expression

lambda args:ret_val # return is implicit, anonymous lambda function 
```

## Sorting

We do sorting in Python by sort() and sorted() functions

### Sort function

```python
L1 = [1,7,4,2,-3]
L2 = ["Cherry", "Apple", "Blueberry"]

L1.sort() # Usually from lowest to highest
print(L1) # [-2,1,3,4,7]
L2.sort() # Usually alphabetically from a to z
print(L2) # ["Apple", "Blueberry", "Cherry"]
```

### Sorted function

There are definite differences between sorted and sort methods

1) Here, we use function syntax instead of method syntax
2) We are getting the value back here and assign in to variable
3) When we invoke sorted() on a list, it doesn't change original one, produces new list with different order

```python
L2 = ["Cherry", "Apple", "Blueberry"]

L3 = sorted(L2)
print(L3)  # ["Apple", "Blueberry", "Cherry"]
print(sorted(L2)) # ["Apple", "Blueberry", "Cherry"]
print(L2) # unchanged, same as before


L2.sort()
print(L2) # ["Apple", "Blueberry", "Cherry"]
print(L2.sort()) # return value is None

print(sorted("Apple")) # ['A', 'e', 'l', 'p', 'p']
```

## Optional Reverse Parameter

```python
L2 = ["Cherry", "Apple", "Blueberry"]
print(sorted(L2, reverse=True)) # ["Cherry", "Blueberry", "Apple"] reverse alphabetical order
```

## Optional Key Parameter

```python
L1 = [1,7,4,-2,3]

def absolute(x):
  if x >= 0:
    return x
  else:
    return -x

L2 = sorted(L1, key=absolute) # here we pass the function as parameter in another function
print(L2) # [1,-2,3,4,7]
L2 = sorted(L1, key=lambda x: absolute(x))
print(L2) # [1,-2,3,4,7]

print(sorted(L1, reverse = True, key = absolute)) # [7,4,3,-2,1]
```
Behind the scenes, when sorted() function is called, it subsequently calls the function absolute for each of the items in the list, and then sorts them based on what they turn into as the result of function absolute for example

## Advanced Sorting (Dictionaries, Breaking Ties)

### Sorting Dictionary's keys

```python
L = ['E', 'F', 'B', 'A', 'D', 'I', 'I', 'C', 'B', 'A', 'D', 'D', 'E', 'D']

d = {}
for x in L:
  if x in d:
    d[x] = d[x] + 1
  else:
    d[x] = 1


for x in sorted(d.keys()): # will be A appears .., B appears .. , C appears, sorting by keys
  print("{} appears {} times".format(x,d[k])) 

for x in sorted(d.keys(), key=lambda k: d[k]) # will be .. appears 1, .. appears 1 , .. 2, .. 2, .. 4, sorting by values


for x in sorted(d.keys(), key=lambda k: d[k], reverse = True) # will be .. 4, ..2 , ..1 and so on, sorting by values from highest to lowest
```

### Breaking Ties

When we sort tuples we sort them by their first value

But if they are comparing first values and they are equal, they are going to compare second ones, and so on  (Breaking Ties)

We can make a tie breaking property to sort lists for example

```python
fruits = ['peach', 'kiwi', 'apple', 'blueberry', 'papaya', 'mango', 'pear']
new_order = sorted(fruits, key=lambda fruit_name: (len(fruit_name), fruit_name))
for fruit in new_order:
  print(fruit) # kiwi, pear, apple, mango, peach, papaya, blueberry (first small length words, then big length words in the end, and if there is a tie between same lengthed , we will compare them by alphabetical order) 

new_order = sorted(fruits, key=lambda fruit_name: (-len(fruit_name), fruit_name))
for fruit in new_order:
  print(fruit) # blueberry, papaya, apple, mango, peach, kiwi, pear (Reverse order of list but the alphabetical order is preserved, and we changed the property of longest to shortest words)

```

## When to use a lambda expression

When the function is easy to write and simple, then make lambda expression, otherwise use name functions



## JSON Format and JSON Module

JSON = JavaScript Object Notation = standard format defined that makes it easy to share that data (nested lists and dictionaries)

Python makes it pretty easy to both read in and write out data in JSON format

JSON format looks exactly like the printout of a Python list or dictionary

There are 2 powerful methods of JSON module in Python: 

1) json.loads(string)
2) json.dumps(list or dictionary)

```python
import json

a_string = '\n\n\n{\n "resultCount":25,\n "results": [\n{"wrapperType":"track", "kind":"podcast", "collectionId":10892}]}'

d = json.loads(a_string) # takes string as input and returns a dictionary or a list

print(type(d)) # because in the string, first symbol among whitespace and newlines was { curly brace, then the return value will be <class 'dict'>
print(d.keys()) # ['resultCount', 'results']
print(d['resultCount']) # 25



def pretty(obj):
  return json.dumps(obj, sort_keys=True, indent=2) # takes list or dictionary and converts it into a string that's in the JSON format, obj is list or dict, sort_keys = True means output in alphabetical order, indent = 2 means 2 character indents that will prettify the string
     
d = {'key1': {'c':5, 'a':90, 5:50}, 'key2': {'b':3, 'c':'yes'}}

print(d) # same inline
print(pretty(d)) # 

{
  "key1":{
    "5":50,
    "a":90,
    "c":5
  },
  "key2":{
    "b":3,
    "c":"yes"  
  }	
}  prettifying the output
```

## Shallow copies

If we take some list and make it as a full slice:

```python
original = [[some1], [some2]]
copied_version = original[:] # it will take same contents as original, but will point to different objects
```
However when we mutate the list in the list of original as example, changes will affect copy too (CONFUSION!)

## Deep Copies

Deep copy is when you will go through the nested loops and fulfill the list one by one

Create an empty list, then go and fill, therefore, if changes in original happen, it has no impact on copied one

There is a module called 'copy' that performs the recursion behind the scenes

```python
import copy 

original = [[some, [s1,s2]], [some2, [s3,s4]]]

shallow = original[:]
deep = copy.deepcopy(original) # takes a sequence as value, produces the deep copy of nested levels
```

## Extracting from Nested Data

JSON Online Editor

Use it to deduce what to index and what to access in order to retrieve data you want to have

## Map

Map function makes a new list where each item in original list is transformed in some way

Map = function that takes sequence as 2nd input and function as 1st input

```python
def triple(value):
  return 3*value

def tripleStuff(a_list):
  new_list = map(triple, a_list)
  return new_list

def quadrupleStuff(a_list):
  new_list = map(lambda value: 4*value, a_list)
  return new_list

things = [2,5,9]
things3 = tripleStuff(things)
print(things3) # [6,15,27]

things4 = quadrupleStuff(things)
print(things4) # [8,20,36]
```

## Filter

Filter = start with some items and end up with fewer of them

Filter function takes two parameters, first is expression (lambda) and second is sequence (list)

Filter returns True if item should be kept and False if it should be filtered out 

```python
def keep_evens(nums):
  new_seq = filter(lambda num: num % 2 == 0, nums) # normally returns iterators in Python just like .keys() method
  return list(new_seq)  # therefore it is better to convert it into list

print(keep_evens([3,4,6,7,0,1])) # [4,6,0]
```

## List Comprehensions

```python
things = [2,5,9]

yourlist = [value*2 for value in things] # creating a list (square brackets, transformer expression (value*2) )

print(yourlist) # [4,10,18]
```
General template for list comprehension:  [<transformer_expression> for <varname> in <seq> if <filtration_expression>]

## Zip

Zip = takes two sequences and zips them together matching their 1st,2nd and so on items together

Useful for pairwise comparisons and combinations

Zip function takes two or more sequences and makes a list of tuples
Each tuple gathers together the items from the corresponding position in the list


```python
L1 = [3,4,5]
L2 = [1,2,3]
L4 = list(zip(L1,L2)) # returns actually an iterator; list like object
print(L4) # It is still going to have 3 elements but each of them is a pair of numbers (3,1), (4,2), (5,3)
L3 = [x1+x2 for (x1,x2) in list(zip(L1,L2))] # makes a list of tuples and makes them add each other and create a list of those results of additions
```

## Requesting Data From the Internet

### REST API

API = Application Programming Interface = interface that lets one computer program interact with another computer program.

REST = Representation State Transfer

REST API means website that produces data intended for another computer program to consume rather than something intended to be displayed to people in a browser

REST API will respond to requests in particular format 


### URLs, Domain Names, and IP addresses

The template of website URL: {protocol}://{server}/{arguments}

Server says where to fetch something from and arguments say what to fetch from that remote server

Protocol says how to communicate with that remote server

__Host(Server) names__ (Domain name)

__Host name__ is a name for specific computer you're communicating with

Every computer that's attached to the internet has a unique identifier, an address called __IP (Internet Protocol) address__
 
No two computers connected to the internet can have the same IP address at the same time

When the computer disconnects, you might get another computer to reuse that IP address

When we have a domain name like google.com, that's of a more permanent name but the actual server that is responding to that name may change over time and each server will have an IP address 

Internet has something called __DNS (Domain Name System)__ = the setup to resolve the names like google.com and turn them to these unique identifiers, the IP addresses

IP address will look like 159.89.239.247 (3 dots just to divide the 4 chunks) 

Each of these chunks should have a number between 0 and 255

You can represent that with eight bits, eight zeros and ones

We got 4 sets of 8 bits, total of 32 bits, therefore sometimes these are called 32-bit addresses 

There's a distributed lookups system, the DNS and you can go to various sites that will let you do this lookup

My computer has a way of doing that lookup, it has a server that it talks to in the background

### Routing

When the browser talks to some remote server, say google.com, it establishes connection and then it sends some data, pieces of text or some other formatting data, and each of those pieces of content gets chopped up into a bunch of packets

Each of those small packets gets sent out onto this big routing system that consists of a whole bunch of routers

Routers = computers whose sole purpose is to receive these data packets and pass them on

Each packet goes from one router to next

Each of those routers has a big lookup table that says "If this packet that i've received is destined for some particular address, what's the next hop? What's the next router I should send it to?"

Magically all of these routers have managed to coordinate their routing tables, so that when a packet gets sent here, it evenrually makes its way to the destination 

As an example: for diagnostics about if i'm trying to send data packets from computer to google.com

```
traceroute google.com

1 100.68.0.5 (100.68.0.5)  71.102 ms 36.587 ms 58.474 ms
2 143.24.43.5 (same here)   some speeds
3 10.255.255.254 (same here) some speeds
...
```

1st line here tells me where does that packet go first, and it goes to computer that has the IP address 100.68.0.5 and it took 71.102 ms to get it there first time, 2nd time is 36, 3rd time is 58ms

2nd line here tells me that if packets successfully went to 1st, where does it go next. It went from 100.68.0.5 to computer with 143.24.43.5. Same with first  
 
and so on

### HTTP: Behind the scenes

What happens behind the scenes when the browser fetches the data from a remote server?

(1) One way is by having an http protocol

First, it is going to take the domain name after http:// and convert it into an IP address 

Then the computer makes a connection to the remote computer 

(2) Second way is using https, which is more secure version of http protocol

First thing that it is going to do is computer would send some info back and forth to the google.com server as example that would establish the encryption keys so that all of the rest of the communication would be encrypted and nobody who intercepted that communication would be able to figure out what we were saying to each other 

After the setup, the browser will start to send messages and it will actually send text, it'll send the word "GET" and then whatever arguments were after the slash 

It will say what path we're looking for and also it will send some headers saying things like, "It is Chrome Browser, current time stamp and other headers"

Then we will receive back from that server some response headers

And it will say "I'm sending HTML and other headers, timestamp" 

Most importantly, google.com is going to send me some HTML, and that HTML my browser is going to take and turn it into a webpage in a browser

So, browser renders HTML

### URL Query Parameters

After the slash, there is a very commom path name, for example, 'list' and then question mark, and after it we got query parameters

Example: 'https://google.com/list?filter=tags:Art,&range=2018-10-01'

These query parameters are very often formatted in these key=value 

We have in example two of these keys: filter and range 

Value of filter is tags: Art
Value of range is October 1st, 2018

The server is going to interpret this request as a request to search on the server to find out these events that are happening on 2018 or beginning in October 1st, and that somehow are tagged with the word Art

If we go to that website, the server is interpreting the request as a query and it is returning info just about artistic activities that are happening starting on October 1st

### REST API URLs 

Request to an API is made by visiting an URL

Some APIs use a different part of the HTTP protocol, called the POST mechanism, in which case not all of the requests is encoded right into the URL

In HTTP, the entire request is encoded in URL

For example, we got URL: https://itunes.apple.com/search?term=Ann+Arbor&entity=podcast

If we copy the URL in the browser, it is either going to put the contents into a file attachment which will be downloaded, or it may just show the contents in a browser window

What we get is a text in JSON format, and it can easily be converted into a Python dictionary using the json.loads() function

If we break the URL apart:

1) domain name in the base URL: `https://itunes.apple.com/search`
2) character `?`
3) key=value pairs. In this case, there are two pairs. Term and Entity, & separates two pairs

We encoded in URL that we were making request to iTunes server, hence itunes.apple.com

Slash search part --> we are searching something (?)

We want to search for Ann Arbor --> term=Ann+Arbor
and we wanted the podcast --> entity=podcast

All the information on the website is encoded in URL and it is pretty useful for debigging 

### The Requests Module

requests module provide a function get and lets Python Program fetch the content of web page

There are __cross site scripting restrictions__ = There can be security considerations built into most web browsers

```python
import requests
import json

page = requests.get('https://api.datamuse.com/words?rel_rhy=funny') # pass the URL get back the response object that includes the text, source of the page that lives at that URL
print(type(page))
print(page.text[:150]) # print first 150 characters, gives us the text attribute, content
print(page.url) # print the url that was fetched


x = page.json() # turn page.txt into a python object, short for json.loads(page.txt)
print(type(x)) # list
print(x[0]) # first element in the list
print(json.dumps(x, indent=2)) # pretty print the results, the list
```
 
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

## Final Project

Problem statement:

We need to process a list of Event objects using their attributes to generate a report that lists all users currently logged in to the machines.


Research:

We need to know how we can sort the stuff in Python

```python
numbers = [4,6,2,7,1]
numbers.sort() 
print(numbers) # [1,2,4,6,7]

names = ["Carlos", "Ray", "Alex", "Kelly"]
print(sorted(names)) # ["Alex", "Carlos", "Kelly", "Ray"]
print(names) # ["Carlos", "Ray", "Alex", "Kelly"]

print(sorted(names, key=len)) # output will be ["Ray", "Alex", "Kelly", "Carlos"], here, ascending order of lengths of names
```

So, sort() function changes the list itself, but sorted() method creates a new list sorted, without changing the original

However, sorted() method can take second parameter as for the criteria for which to sort


```python
def get_event_date(event):
  return event.date

def current_users(events):
  events.sort(key = get_event_date)
  machines = {}
  for event in events:
    if event.machine not in machines:
      machines[event.machine] = set()
    if event.type = "login":
      machines[event.machine].add(event.user)
    elif event.type = "logout":
      machines[event.machine].remove(event.user)
  return machines


def generate_report(machines):
  for machine, users in machine.items():
    if len(users) > 0:
      user_list = ", ".join(users)
      print("{}: {}".format(machine, user_list))
```




# Using Python to Interact with Operating System course

Operating system = software that manages everything that goes on the computer

There are 2 main parts of operating system:

1) Kernel = main core of OS, it talks directly to our hardware and manages our system's resources. Users don't interact with Kernel directly

2) User space = everything outside of kernel, users interact directly with it, like system programs and user interface

Linux is the name of the kernel developed originally by Linus Torvalds

Because Linux is open source OS, many organizations package their own versions of it = called distributions

Some common are Ubuntu, Debian and Red Hat. Also Chrome OS but is usually considered an OS in its own right

Android OS also runs on Linux Kernel

Unix is OS developed back in 70's by Bell Labs

Linus created Linux which is based on Unix

MacOS kernel and some of its user space are also based on kernel and user space of the Unix family known as BSD


## Interpreted vs Compiled Languages

Compiler = software, which translates the source code into machine level language

It can make compiled program super fast to run, but compilation process itself can take time

Compiled languages: C, C++, Go, Rust


Interpreter = program to execute the instructions specified in the code

Interpreted languages generally run slower than compiled ones

Interpreted languages: Python, Ruby, JavaScript, Bash, PowerShell


Mixed approach languages: Java, C#

The code needs to be compiled first but it gets compiled into intermediate code, that can execute on different platforms

We execute the code using a program that's OS specific: Java Virtual Machine for Java, and Common Language Runtime for C#



Python Interpreter itself is a compiled executable that's platform specific, but I can run my scripts everywhere once I have it installed


`cat _filename_` = command on terminal, shows the contents of file on Linux


To avoid writing python3 line to execute the code in terminal, we can add the extra line to our file called 'shebang' which tells the OS which command we want to use to execute that script

Open the editor --> here, can use 'nano' filename.py --> `#!/usr/bin/env python3` type this into the beginning of script --> save it --> make the script file executable --> chmod +x filename.py --> ./filename.py --> Done

We need to add './' when executing the script, because the script isn't located in any of the directories listed in PATH variable.

PATH variable = tells OS where to find programs to execute

. in './' expression represents the current directory


## Own Python Modules 

import filename 

If I have a module that split into separate files, and I want to recognize the directory has a module, i need to create init.py file

In order for interpreter to recognize the directory as a Python module, we need to create init.py

## IDE

IDE = Integrated Development Environment = code editor with handy extra capabilities that make writing scripts a lot easier 

One of the features in IDEs is __Syntax Higlighting__ = means the editor recognizes the language of code and makes up syntax of language 

Code completion feature 

Vim, Atom, VS Code = editors 



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

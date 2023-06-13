# Variables
- variables in computer programming are like buckets or envelopes where the information you put inside one can be accessed later
- each variables is given a name, which is like a word you write on the outside of the bucket so you know what it represents
- when referring to a variable we use the name of the variable, not the data within
```Python
x = 5
# printing a integer variable outputs the integer to the command line
print(x)
# we can also modify the value before it is printed by the print function
print(x + 10)

x = "cucumber"
# printing a string variable outputs the string to the command line
print(x)

x = 5
y = 7
# similarly to above we can modify the value printed by writing an
# expression in the function parameter area
print(x+y)

x = 10
x = 5
# what happens when you redefine a variable before printing?
print(x)

x = "cat"
y = "dog"
# you can print two strings apart
print(x, y)
# or you can print the strings together by adding them together
print(x + y)
```

---
## Naming Variables
- note that variables names have to follow some rules
	- variables names MUST
		- start with a letter
	- variable names MUST NOT
		- contain a space
	- variable names SHOULD
		- start with a lower case (unless is a constant variable)
		- use underscores between worlds
```
Great Variable Names
	first_name
	distance
	ds9              # unclear what the variable represents 
Allowed Variables Names (Not Properly Formatted)
	FirstName        # stats with an upper case letter
	firstName        # does not use a underscore between words
	X                # starts with a upper case letter
Not allowed; code will not run
	first name       # contains a space
	9ds              # starts with a number
	%correct         # starts with a symbol
```

### Check For Understanding
- Create three variables. 
	- The first must be a string
	- The second must be an integer
	- The third must be a float
- Create a variable that contains your name.
	- Create a print statement that says hello to you.
	- `print("Hello " + your_name)`
- Create three variable names that are not valid. Explain to your counselor why they are not valid variable names

***Before you move on, make sure you show your counselor your progress.***

---
## Input and Type Changing
- the `input()` function (similar to the `print()` function) calls for the user to input a value
- the value is initially takes as a string but we can change the variable's type
	- to make an integer use `int(input())`
	- to make a string use `str(input())`
	- to make a float use `float(input())`

```Python
# take the user's input as a string and then print it out
x = input()
print("Hello", x)

# get the user's age and they type cast it to an integer with int()
# then we add one (to prove it became an integer) and then we print it
x = input("Age: ")
y = int(x)
y = y + 1
print(y)

# take the user's input twice and print them after adding them together
x = input("Input a number: ")
y = input("Input a number: ")
print(x + y)
# why doesn't this add the two numbers together?
```

### Check For Understanding
- Write a program that asks for two inputs and adds them together.
	- Make sure to use type casting so the variables are integers.
- Write three more programs that can do subtraction, multiplication, and division.
	- Be sure to use type casting.
- Write a program that takes user input to two string variables. These two variables should be the first and last name of the user.
	- Print out the values by saying hello to the user.

***Before you move on, make sure you show your counselor your progress.***

---
## If Statements and Conditional Operators
- if is a conditional statement
- conditional statements let computers make decisions, based on if the condition is true or not
```Python
# play around with these numbers and see what changes in the function
a = 1
b = 2
c = 1

if a == 1:
	print("a is equal to 1")

if b > 1:
	print("b is greater than 1")

if c >= 1:
	print("c is greater than or equal to 1")

```

***Without running the code, tell your counselor what this code would print:***
```Python
a = 4
b = 5

if a < b:
	print("a is less than b")

if a > b:
	print("a is greater than b")

print("Done")
```

- Python has 6 comparison operators:
	- remember that the double equal sign (\=\=) is the comparison operator for equal and the single equal sign (\=) is just for setting values like variables
	- `x = 10 (x is 10)` versus `x == 10 (x is equal to 10)`

 Operator | Name | Example 
 --- | --- | --- 
  ==       | Equal                    | x == y  
 !=       | Not Equal                | x != y  
 \>        | Greater than             | x > y   
 <        | Less than                | x < y   
 \>=       | Greater than or equal to | x >= y  
 <=       | Less than or equal to    | x <= y  

- code after a conditional (like if statements) is only run if the condition is met and the code is properly indented (generally with a tab). also, conditional statements must end in a colon (:)
```Python
# play around with these variables to see what happens
a = 2
b = 2

# note the colon at the end and the indentation of the code
if a == b:
	print("As long as the two numbers are the same, this will print.")
	print("So will this.")
	print("And this.")
# note how the next line is not indented. this will print even if the
# if statement is not true
print("This will always print.")
```

### Check For Understanding
- Write a program that takes the user input and makes two integer variables
	- Compare these variables with all 6 of the conditional operators.
	- Make sure to print out a statement telling the user what worked
		- If the equals conditional works tell the user that the numbers are equal
		- If the greater than or equal conditional works tell the user that the first number is either greater than or equal to the second number.
	- More than one conditional operator may be true at the same time. Print out a different statement for each conditional operator that is true.

***Before you move on, make sure you show your counselor your progress.***

---
# Logic
## Boolean Operators
- an if statement can check multiple conditions by chaining together comparisons with `and` and `or`. these are considered operators like `+` or `-`, but they are not interchangeable with each other

```Python
# Play with these values and see what happens
a = 1
b = 2
c = 3

# these next two methods operate similarly
# this method uses nested if statements to make sure both conditions are met
if a < b:
	if a < c:
		print("a is less than b and c")

# this method uses a boolean operator to remove the nested if statement
if a < b and a < c:
	print("a is less than b and c")

# the or operator makes the condition true if either part of the conditional
# is true (or both are true)
if a < b or a < c:
	print("a is less than either b or c (or both)")

# we can also use a boolean operator to help evaluate when we want
# a conditional to be true even though the condition is not true
if not a == b:
	print("a does not equal b")
```


### Check For Understanding
***Think of an example of where the not operator could be user. Talk to your counselor about why the not operator is helpful.***

---
## Boolean Values
- we can set variables to a Boolean value (either `True` or `False`). these are generally referred to as Booleans
```Python
# make sure to capitalize True and False. they will not work in lower case
# Play with these values and see what happens
a = True
b = False

if (a and b):
	print("a and b are true")

if (a != b):
	print("a is not equal to b")
	
if (a == b or a != b):
	print("a is equal to b or a is not equal to b")

if not (a == b):
	print("a and b are not equal")
```

---
## Everything is a Boolean?
- did you know that a lot of things are considered Booleans? if something exists, it returns `True`. if it does not exits (i.e. it is 0) then it returns false
```Python
if "cat":
	print("cat exists")

if 9:
	print("9 exists")

if 0:
	print("0 exists")

# Play with this value and see what happens
a = 0

if a:
	print("your a value exists")
```

---
## Else Statements
- if statements tell the computer what to do based on whether a condition is `True` or `False`. 
- if the condition is not met, and `else` statement can be used. 
- If several different conditions must be met, an `elif` (stands for else if) statement can be used
  - note that if an if or `elif` statement evaluates `True` no other `elif` statements in the block with try to evaluate
  - this is because the rest are considered only if the previous `if` and `elif` statements are false
```Python
if 4 != 4:
	print("4 is not equal to 4")
else:
	print("4 is equal to 4")

if 9 == 9:
	print("9 is equal to 9")
else:
	print("9 is not equal to 9")

# Play with these values and see what happens
a = 0
b = 0

if a == b:
	print("a is equal to b")
elif a != b:
	print("a is not equal to b")
elif a > b:
	print("a is greater than b")
elif a < b:
	print("a is less than b")
elif a >= b:
	print("a is greater than or equal to b")
elif a <= b:
	print("a is less than or equal to b")
```

### Check For Understanding
***When a and b are equal why do we only print that they are equal and not that they are greater than or equal to or less than or equal to? Talk to your counselor about why this happens.***

---
## Comparing Strings
- when you compare two strings remember the quotes
```Python
# remember we can use the escape character (\") to have quotes in our strings
if "Dave" == "Dave":
	print("\"Dave\" is equal to \"Dave\")

if "Dave" == Dave:
	print("\"Dave\" is equal to Dave")
```

### Check For Understanding
***Why does the second if statement evaluate to False? Talk to your counselor about why you think this is.***

---
## Manipulating Strings
- sometimes it's helpful to convert a string to all uppercase or all lowercase
- in the next example by converting the input to all lowercase we can check the input string to a string in all lower case.
	- if the input was "NORTH", "North", or "nOrTh" it all becomes "north" so we can properly check it in our conditional

```Python
direction = input("What direction do you want to go? ")

if direction.lower() == "north":
	print("Lets go north")
else:
	print("I don't know where to go")
```

### Check For Understanding
- Write a program that takes in the users name.
	- Write an if statement that checks that the user's name is equal to the name you provide.
		- If `True` print out something saying they have a great name
		- If `False` print out something saying they have a nice name
		- Remember to make the input all lowercase so you can easily check the value

***Before you move on, make sure you show your counselor your progress.***

---
# Loops
## For Loops
- the for loop in python can be created by using the range function. we give the range function a number and it create a loop that starts a 0 and goes to the inputted number minus 1
```Python
# try playing with the value in range() to make the loops longer or shorter
for i in range(10):
	print(i)

for i in range(7):
	print(i + 1)

for x in range(7):
	print(x * 2)
```

---
## Advanced Range For Loops
- the range function has more than one parameter that it can take
- if actually has the ability to have three parameters
	- `range(starting_number, ending_number, increment)`
	- `ending_number` is the only required value
	- if not supplied, `starting_number` = 0 and `increment` = 1
```Python
for i in range(10, 0, -1):
	print(i)

for i in range(2,12,2):
	print(i)
	
# since we only have two parameters, what parameters are they?
# Try identifying them with your counselor
for i in range(2,5):
	print((i + 1) * 2)
```

---
## While Loops
- a `while` loop will repeat continuously until the given condition is `False`
```Python
quit = "n"

while quit == "n":
	quit = input("Do you want to quit? ")
```
- after the condition becomes `False` we can continue the program
```Python
x = True
while x:
	print("Do this while x is true")
	x = False
	print("Now that x is false, this loop will end")
print("The program continues when the loop ends!")
```
- we can also make a while loop into something like a for loop
	- this might be helpful if we increment `i` by different amounts through the program
```Python
i = 0
while i < 10:
	print(i)
	i = i + 1
```

### Check For Understanding
- Get two inputs from the user (one is a string and one is a integer)
	- Create for loop that prints out the string for as many times as the integer

- Recreate the previous problem with a while loop instead of a for loop

***Before you move on, make sure you show your counselor your progress.***

---

# Lists
## Creating Lists
- lists are a type of variable that holds elements at different indexes
	- a list has different values 
	- these values are stored at a position called an index
	- note that a list's index starts at 0

![[Pasted image 20230613111524.png]]

```Python
# This list has only two integer values
x = [1, 3]
print(x)

# This list has three string values
x = ["a","b","c"]
print(x)

# These list contains other lists that contain strings
# List 1 = ["a","b"]
# List 2 = ["c"]
# List 3 = [["a","b"],["c"]]
x = [["a","b"],["c"]]
print(x)
```

---
## Editing a List
- you can access the value at a specific index value by:
	- `list_name[index]`
```Python
x = [1, 2, 3]
print(x[0])
print(x[1])
print(x[2])

print(x)

# What happens if I multiply it?
print(x[2] * 2)
```
- you can also use the same strategy to change a value in a list
```Python
x = [1, 2, 3]
print(x)

x[2] = 4
print(x)

x[0] = 0
print(x)
```
- if you want to add to the array and not just change you can use `append()`
```Python
x = [1, 2, 3]
print(x)

x.append(4)
print(x)

x = ["a", "b"]
print(x)

x.append("c")
print(x)
```
- if you want to remove the first occurrence of the supplied parameter use `remove()`
	- if this finds nothing if will remove nothing
```Python
x = ["a","b"]
print(x)

x.remove("a")
print(x)

x = [1, 2, 3, 1]
print(x)

# note that this only removes the first value of 1
x.remove(1)
print(x)
```

### Check For Understanding
- Make an list with the user's input then print that list
	- Create an empty list `x = []`
	- Create a for loop that runs 5 times
	- Each time the loop runs
		- Ask the user for a new string input
		- Append it to the list
	- Print the list after the for loop is over

---
## Looping Through List
- you can loop through a list to get each item in them
- note that `item_variable` stores a copy of the value in the list (not the actual value)
	- therefore, you cannot change the array simply by changing `item_variable`
```Python
list_name = [1, 2, 3, 4, 5]
for item_variable in list_name:
	print(item_variable)

# Another example with more common variable names
my_list = ["cat", "dog", "man"]
for item in my_list:
	print(item)
```
- we can also use the value we get from the array
```Python
my_list = [5, 76, 8, 5, 3, 3, 56, 5, 23]
list_total = 0

for item in my_list:
	list_total = list_total + item
	
print(list_total)
```

---
## Looping Lists with Range
- list can also be looped through using a regular `for` loop
- generally you use the length of the list and the range
	- you can find the length of the list with `len()`
```Python
my_list = [1, 2, 3, 4, 5]
for i in range(len(my_list)):
	print(my_list[i])

my_list = ["cat", "dog", "man"]  
for i in range(len(my_list)):  
    print(my_list[i])

# we can now update in the list by using their index
my_list = [1, 2, 3, 4, 5]
for i in range(len(my_list)):
	my_list[i] = my_list[i] + 1
print(my_list)
```

### Check For Understanding
- Make an list with the user's input then print that list
	- Create an empty list `x = []`
	- Create a for loop that runs 5 times
	- Each time the loop runs
		- Ask the user for a new integer input
		- Make sure to type cast it with `int()`
		- Append it to the list
	- Create a for loop that has a range equal to the length of the list
		- Add one to each value 
	- Print out the list to check your work

---
## Strings are Lists
- strings are actually just lists of characters
- `"word" = ['w','o','r','d']`
```Python
a = "Hi There"  
print(len(a))  
for i in range(len(a)):  
    print(a[i])  
a += 'a'  
print(a)
```

---
# Time for Adventure

***Talk to your counselor about starting work on the adventure game***

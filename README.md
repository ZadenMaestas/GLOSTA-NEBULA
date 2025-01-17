# GLOSTA-NEBULA

---

# About
Really simple programming language I made to test out features regarding a different type of syntax for GLOSTA BYE.

Turned out to be bigger when I added 1.2k more lines to it !!



# Documentation

## Basic Hello, World! Program

Writing our first program in GN is simple, lets write a print function:

```cpp
print "Hello World!"
```

#### Note: Spaces between each token are vital, as the interpreter tokenizes based on spaces.

## Basic Math:

The interpreter reads backwards, but we can do order of operations by using quickscopes, or parentheses.
Items inside parentheses are scanned and interpreted before the rest.

```cpp
print (1 + 1) * 2
```

-----^~~~~~~ <- interpreted and set to "2" before the rest

So, the interpreter reads that as this:

```cpp
print 2 * 2
```

## Types

While types are not necessary, if you want to have spaces you need to use a string.
print "Hello world."
print 'Hello world.'

## Mathematical Operators

#### + is used for addition and string concatenation

#### - is used for subtraction

####  * is used for multiplication

#### / is used for division

#### ^ is used for power to

#### % is used for modulus

## Variables

Variables are easy to define, set, and use.
To define one, you write something like this:

```js
var lemon
5
```

No equals needed, just three tokens

"var" <- signifies we're defining a variable

"lemon" <- tells the interpreter the name of the variable

"5" <- tells the interpreter the value of the variable

To redefine a variable, we just do it simply as if we were defining another variable with the same name.

```js
var lemon
lemon + 2
$$
Our
lemon
variable
becomes
7
```

Yes, you can call a variable inside its own definition as long as the variable already exists!

## For Loops

To run a simple forloop, we would write code like this:

```cpp
for 5
print "Hello!"
endloop
```

Output: prints "Hello!" five times.

And to access the loop index, we can call "idx"

```cpp
for 5
print idx
endloop
```

Output prints 0 -> 4 on first iteration

idx is a variable automatically declared by the interpreter. The variable is NOT deleted and can be accessed after,
but if another loop is ran it will be overwritten.

## User stacks

User stacks are like C++ vectors made easy. They have three commands which allows almost full control:

```cpp
newstack strawberry -> define a new stack

pushstack strawberry 4 -> push 4 to the stack
pushstack strawberry 5 -> push 5 to the stack

print indexstack strawberry top -> prints 5
print indexstack strawberry size -> prints 5
print indexstack strawberry 0 -> prints 4
print indexstack strawberry 1 -> prints 5
```

## If statements

GLOSTA NEBULA has 2 binary operators and 2 unary operators meant for if statements:

#### == -> equal to

#### != -> not equal to

#### > -> greater than

#### < -> less than

These operators can also be used to print

```cpp
print 5 == 5 <- prints "true"
print 5 > 6 <- prints "false"
print 5 < 6 <- prints "true"
print 5 != 5 <- prints "false"

if 5 == 5
print "true"
endif
```

^^ that runs because 5 is equal to 5

```cpp
if 5 != 5
print "true"
endif
```

^^ this does not run, 5 is equal to 5.

```cpp
if 6 > 5
print "true"
endif
```

^^ this runs, 6 is greater than 5

```cpp
if 6 < 5
print "true"
endif
```

^^ this does not run, 6 is not less than 5.

## User Keycalls/Functions

While functions do not have a explicitly reserved return function, manipulating the GLOSTA stack top is easily
performed.

```js
function blueberry

1 + 4 < -final
value
is
pushed
top
closefunction

print
blueberry < -prints
5
```

# Finish early

Writing @FINISH will complete the program and collect all garbage, meaning if you put it inside the function, the
function
will not end up registering.

# Comments

Comments are written as such

```
$$ This is a comment
$$This is also a comment
```

## C++ Accessible Functions -

```cpp
print arg1
```

We all know what print does, right? It prints the value to the screen.

```cpp
getinput arg1
```

Requests user input and writes it to the variable given. i.e.

```cpp
var raspberry ""
getinput raspberry
```

If the user inputs "hello", the value of raspberry would be set to "hello"

```cpp
rand arg1
```

Generates a random number from 0 to arg1, which must be an integer.

```cpp
import arg1
```

- Imports a file with GLOSTA NEBULA code. The file is executed.
- arg1 is a file name, "filename.glo"

```cpp
strlen arg1
```

Returns the length of the string given

## Enabling and Using the GLOSTA Stack

To give yourself access to the GLOSTA Stack (gstack), you need to write the following:
```
@ENABLEGSTACKACCESS
```
which will allow the rest of your code to access the features.

Here are the functions which become available

```cpp
indexgstack arg1
```

arg1 can be a number or "top"/"size" which indexes the top of the gstack

```cpp
printgstack
```

prints the entire stack along with the indexes

```cpp
setgindex arg1 arg2
```
arg1 is the index aka "top"/"size" or any available index integer

arg2 is the new value, which can be anything

```cpp
cleargstack
```
erases the entire stack, not including: variables, userstacks, functions/keycalls

[It's strongly recommended that you check out the included examples too](https://github.com/AwesomeMc101/GLOSTA-NEBULA/tree/main/examples)


# Description
Some basic concepts of scripting in Lua Programing Language.
This guide is for experienced programmer who need to write some script but have no idea about the syntax of Lua Prigramming.
This just given an overall idea of Lua Programming.


## Introduction to Lua
Lua is a powerful and intuitive general-purpose programming language developed in 1993 by a team of scrappy professors at Pontifical Catholic University of Rio de Janeiro, in Brazil. Much of the inspiration for Lua came from the languages SOL (Simple Object Language) and DEL (data-entry language). In Portuguese, Sol means “sun” and Lua means “moon”.

Lua has an easy-to-read, Python-like syntax, it takes up very little space on your machine, and it can interoperate with any C code.

Despite its humble beginnings, Lua is now used for:
1. Building games, such as Roblox, World of Warcraft, and Angry Birds
2. Building web apps, such as Venmo and Adobe
3. Building developer tools within companies such as Redis

### Single Line Comment
A single line comment will comment out a single line and is denoted by two dashes -- preceding it.

### Multi Line Comment
A multi-line comment will comment out multiple lines and is denoted by --[[ (to begin the comment, and ]] to end the comment:
  ``` function sumdigits(n) 
     local sum = 0
     while n > 0 do
        sum = sum + n%10
        n = math.floor(n/10)
     end
     return sum
  end
```
### Data Types in Lua
In Lua, data can be organized into four basic data types, each with distinct behavior and purposes.
![image](https://github.com/manzar2525/Lua/assets/107947502/1a8423b1-ee17-4d0c-b9ef-95dc2946d640)


**Note:** There are also an additional four complex data types that we won’t go into now. They are: 
1.  Tables
2.  Functions
3.  Userdata
4.  Threads.


## Operators

![image](https://github.com/manzar2525/Lua/assets/107947502/1d7f74cc-e0c3-460e-b88f-e5f7fdfa5707)

![image](https://github.com/manzar2525/Lua/assets/107947502/20c0048b-57b8-4242-9a69-25e6eb698b66)

## Comparision Operators
1. **A > B:** A Greater than B
2. **A >= B:** A Greater than or Equal to B
3. **A < B:** A Less than B
4. **A <= B:** A Less than or Equal to B
5. **A == B:** A Equals B
6. **A ~= B:** A doesn’t Equal B
</br>





===========Conditionals and Logic
The if Statement
The foundation of every control structure starts with an if statement. if statements require two parts:

a boolean expression — a variable or some code that evaluates to a true or false value.
a code block — the code that is executed if the boolean expression is true (and is skipped otherwise).

isHungry = true
if isHungry then
  print("I need food")
end 

Let’s break down the code in this example:

if: the keyword telling Lua to create an if statement.
isHungry: the boolean expression to be evaluated.
then: signals the end of the boolean expression and the start of the code block
print("I need food"): the code that only runs if the boolean expression is true.
end: marks the end of the code block.

The else Statement
Next, let’s talk about a common scenario: We want something to happen if our condition is true OR we want something else to happen if our condition is false. We could write this:

The elseif Statement
Imagine we are in the kitchen making a delicious sandwich, but when we check the fridge, we notice that we don’t have ham. We don’t just throw out the sandwich because we don’t have ham. We first will check if we have another option. Luckily we had turkey and can continue to make a sandwich.

peopleInRoom = 10
chairsInRoom = 5
if peopleInRoom == 0 then
  print("No one showed up!")
elseif peopleInRoom <= chairsInRoom then
  print("We have enough chairs")
else    
  print("We don't have enough chairs")
end


============Order of Operatros=====

Given a boolean expression, it will evaluate certain operators before others. The table below shows what operators are evaluated first from top to bottom.
()
^
not
*, /
+, -
<, >, <=, >=, ~=, ==
and
or
Note: If an operator is repeated or multiple operators of the same level are in the same expression, the computer moves left to right through a line of code in execution.

















========================Functions=========

If we want to create a function for our code then we have to make a function declaration.

Most of the code is the same but we’ve added some things before and after. Let’s look at what each part of this code is doing:

function — This marks the start of our function.
getTravelTime — The function’s name. A function’s name should describe what the function does to increase our code’s readability.
() — Parentheses are used to indicate any inputs. For now, there are none (indicated by the empty parentheses) but we’ll add some later.
The code of the function goes between the parentheses and end and is indented for improved readability.
end — This marks the end of our function.


function printShoppingCartTotal()
  subtotal = 100
  taxRate = 1.2
  total = subtotal * taxRate
  print(total)
end

printShoppingCartTotal()
printShoppingCartTotal()
printShoppingCartTotal()


We need to set up our function to take inputs (called arguments) that change how the function behaves. For our own functions to do this, they need parameters. Parameters are variables that are declared with the function but aren’t assigned a value until they are called:

Returns
As we have seen, our functions can receive outside information from the rest of the program. Our functions can also send information back. This is done through a return.

One more important note about returns is that any code after a return statement will never be executed.


function printShoppingCartTotal(subtotal, taxRate)
  total = subtotal * taxRate
  print(total)
end

printShoppingCartTotal(100,1.2)
printShoppingCartTotal(200,1.1)
printShoppingCartTotal(500,1)



function getShoppingCartTotal(subtotal, taxRate)
  total = subtotal * taxRate
  return total
end

total1=getShoppingCartTotal(200,1.2)
total2=getShoppingCartTotal(300,1.1)
total3=getShoppingCartTotal(50,1.5)
finalTotal=total1 + total2 + total3
print(finalTotal)
print(total3)
print(total1,total2)


Built-In Lua Functions
We’ve been using print this whole time, but Lua comes with a lot more functions built in. For example, Lua has an entire collection of functions for using and manipulating strings. The documentation for these functions can be found on Lua’s Official Website. Additional examples for the string and other libraries can be found in the user-maintained wiki


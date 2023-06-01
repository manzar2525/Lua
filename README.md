# Description
Some basic concepts of scripting in Lua Programing Language.
This guide is for experienced programmer who need to write some script but have no idea about the syntax of Lua Prigramming.
This guide just give an overall idea of Lua Programming.


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
     local sum = 0          --here we are putting a sinle line comment
     while n > 0 do
        sum = sum + n%10
        n = math.floor(n/10)
     --[[ here we are putting
          multiple lines of comment
        ]]
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



## Comparision Operators
1. **A > B:** A Greater than B
2. **A >= B:** A Greater than or Equal to B
3. **A < B:** A Less than B
4. **A <= B:** A Less than or Equal to B
5. **A == B:** A Equals B
6. **A ~= B:** A doesn’t Equal B

![image](https://github.com/manzar2525/Lua/assets/107947502/0b05dc5d-2e16-4eaf-b2f4-baf564a13c96)

## Conditionals and Logic
**The if Statement**
The foundation of every control structure starts with an if statement. 
if statements require two parts:
1. **boolean expression** — a variable or some code that evaluates to a true or false value.
2. **a code block** — the code that is executed if the boolean expression is true (and is skipped otherwise).

```
score=80
if score >=90 then
  print("you got A+")
elseif score >=80 and score <90 then
  print("you just passed")
else
  print("you failed")
```
Let’s break down the code in this example:<br>

1. **if:** the keyword telling Lua to create an if statement.
2. **score >=90:** the boolean expression to be evaluated.
3. **then:** signals the end of the boolean expression and the start of the code block
4. **print("you got A+")** the code that only runs if the boolean expression is true
5. **elseif:** evaluate this ecpression if first expression is evaluated to be false.
6. **print("you just passed")** the code that only runs if the first boolean expression is false and second is true.
7. **else:** the keyword tell that all the above experssions are false then execute the below code
8. **print("you failed"):** the code that only runs if all the boolean expression are false.
9. **end:** marks the end of the code block.

## Order of Operatros

Given a boolean expression, it will evaluate certain operators before others. 
The priority of evaluation of operators is mentioned below:
1. ()
2. ^
3. not
4. *, /
5. +, -
6. <, >, <=, >=, ~=, ==
7. and
8. or


**Note:** If an operator is repeated or multiple operators of the same level are in the same expression, the computer moves left to right through a line of code in execution.


## Functions

If we want to create a function for our code then we have to make a function declaration.
```
function getShoppingCartTotal(subTotal,taxRate)
  total = subTotal * taxRate
  return total
end

print(getShoppingCartTotal(100,1.5))
print(getShoppingCartTotal(200,2))
print(getShoppingCartTotal(50,1.3))
```
Let’s look at what each part of this code is doing:

1. **function** — This marks the start of our function.
2. **getShoppingCartTotal** — The function’s name. A function’s name should describe what the function does to increase our code’s readability.
3. **(subTotal,taxRate)** — Parentheses are used to indicate any inputs. For now, there are two *subTotal* and *taxRate*.
4. **total = subTotal * taxRate** - body of the function and we can add as many as lines of code required.
5.  **return total** - This line is returning the execution control back to the statement which callled this function. any code as part of this function will not be executed.
6.  **end** — This marks the end of our function.end and is indented for improved readability.
7.  **getShoppingCartTotal(100,1.5)** writing a function won't get executed until and unless we call that function. here the function is being called.

## Built-In Lua Functions
We’ve been using print this whole time, but Lua comes with a lot more functions built in. 
For example, Lua has an entire collection of functions for using and manipulating strings. The documentation for these functions can be found on Lua’s Official Website. 
1. [Officle Lua website for Inbuilt Modules](http://lua-users.org/wiki/StringLibraryTutorial)
2. [user-maintained wiki](http://lua-users.org/wiki/TutorialDirectory)

**I have used the content from Codecademy as i learned from there itself**<br></br>
[Codecademy Learn Lua](https://www.codecademy.com/learn/learn-lua)


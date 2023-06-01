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


1. **Number:**  A numeric value including positive values, negative values, and decimal values.	  </br></emsp>**Examples**: 10, 3.5, -4	
2. **String:**	A sequence of individual characters inside quotations. It can be letters, spaces, numbers, or symbols. </br></emsp> **Example:** "This is a string".'I have 5 cats!'	To store your username on a website.
3. **Boolean:** A value that only has two possible values: true or false.	
4. **Nil:** A representation for the absence of a value. If there is no value, it is nil.

**Note:** There are also an additional four complex data types that we won’t go into now. They are: 
1.  Tables
2.  Functions
3.  Userdata
4.  Threads.


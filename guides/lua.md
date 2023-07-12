# 🌟 The Programmer's Treasure Trove 🌟

<span style="font-size: 10px;">(*A note for people coming to learn for Roblox development. While this is close to the same language as Roblox's (Luau), this __DOES NOT__ provide a full guide for Roblox scripting. Sorry!*)</span>
### Introduction to Lua

Lua <span style="font-size: 10px;">(*Not to be confused with <span style="color: lightcyan;">[Luau](https://luau-lang.org/)</span>*)</span> is a programming language known for its unique and straightforward syntax. It keeps things simple, making it easier to learn and understand. With Lua, you'll find a clean and intuitive approach that allows you to express your ideas concisely. Its focus on readability and minimalism promotes writing clear and maintainable code.


> Remember! Before learning any programming language... "<u>**Successful programming requires a combination of dedication, continuous learning, and honing of skills.**</u> and almost always dedication is greater than skill! As long as you persevere you will grow!"

## Table of Contents:
- [Introduction](#introduction-to-lua) 
- [Table of Contents](#table-of-contents) 
- [Resources](#resources)
- [Variables](#variables)
- [Tables](#tables)
- [Functions](#functions)
- [Misc. Topics](#misc-topics)
    - [Object-Oriented Programming](#object-oriented-programming-oop)

## Resources

Here are some things you might need for development in Lua! (Note: Before you install from their website, check if your package manager has it, it makes installing easy! :D)

- [Lua](https://www.lua.org/) is needed.. Duh 
    - [Install the latest version of Lua](https://www.lua.org/download.html)
- [Luarocks](https://luarocks.org/) contains a ton of libraries and frameworks for Lua. (Luarocks usage is not covered in this)
    - [Install Luarocks!](https://github.com/luarocks/luarocks/wiki/Download)
- [LuaJIT](https://luajit.org/) is a Just-In-Time compiler, meaning it compiles your code before running, making it super-fast! (Some Lua built functions do not work in LuaJIT. But for the most part, it maintains 95% of Lua's functionality, with [7x the speed](https://staff.fnwi.uva.nl/h.vandermeer/docs/lua/luajit/luajit_performance.html))
    - [Install LuaJIT](https://luajit.org/download.html) 

- Libraries (LuaRocks)
    - [LuaSocket](https://lunarmodules.github.io/luasocket/) <br>
        -   Network support for the Lua language <br>
            ```luarocks install luasocket``` <br>
            ```local socket = require('socket')```
    - [Lpeg](https://www.inf.puc-rio.br/~roberto/lpeg/) ([View on LuaRocks](https://luarocks.org/modules/gvvaughan/lpeg)) <br>
        -   LPeg is a new pattern-matching library for Lua, based on Parsing Expression Grammars (PEGs). <br>
            ```luarocks install lpeg``` <br>
            ```local lpeg = require('lpeg')```
    - [LFS or Lua File System](https://lunarmodules.github.io/luafilesystem/) ([View on LuaRocks](https://luarocks.org/modules/hisham/luafilesystem))<br>
        -   LuaFileSystem is a Lua library developed to complement the set of functions related to file systems offered by the standard Lua distribution. <br>
            ```luarocks install lfs``` <br>
            ```local lfs = require('lfs')```

## Variables

In Lua, variables are used to store and manipulate data. They are like containers that hold values of different types such as numbers, strings, and more. Here's a simple explanation of variables in Lua:

-   Variable Declaration:
    To create a variable, you simply assign a value to it using the assignment operator (=). Lua is dynamically typed, which means you don't need to explicitly declare the type of the variable. For example:

```
myVariable = 10
```

#### Variable Naming:
Variable names in Lua can consist of letters, digits, and underscores (_), but they must start with a letter or an underscore. Lua is case-sensitive, so myVariable and myvariable are considered different variables.

#### Variable Types:
Lua supports multiple data types, and the type of a variable is determined by the value it holds. Some common types include:

- Numbers: Represented as integers or floating-point values.
- Strings: Sequences of characters enclosed in single or double quotes.
- Booleans: Represented as either true or false.
- Tables: A versatile data structure that can hold multiple values.
- Functions: Blocks of reusable code.
---
-   Variable Assignment and Manipulation:
    You can assign new values to a variable at any time. For example:

```
myVariable = 20  -- Assigning a new value
myVariable = myVariable + 5  -- Modifying the value
```

-   Variable Scope:
    Variables in Lua have a scope, which determines their visibility and lifetime. A variable declared outside any code block has global scope and can be accessed from anywhere. Variables declared within a code block, such as a function, have local scope and are only accessible within that block.

-   Nil Value:
    If a variable doesn't have a value assigned, it is nil by default. nil represents the absence of a value.

You can also assign function values and what functions return, but more on that later. But just for this context, one of these functions returns a value.
```
myVariable = myFunction -- Doesn't execute the function
myVariable = myFunction() -- This does execute the function, and this is assigned the return values of the function
```

If you don't understand all this fancy *function* and *return* stuff, don't worry. You will understand it later :).


Oh and also, if you have seen me putting text in my examples above, it's called commenting. Comments don't affect your code, and are like notes. You can start comments by putting '--' and then your comment:
```
-- Your comment here
-- or
--[[
    Your comment here
]]
```


## Tables

In Lua, tables are a fundamental data structure that can be used to create arrays, dictionaries, objects, and more. They are highly flexible and can store different types of values as key-value pairs. Here's an explanation of tables in Lua:

-   Table Creation:
    Tables in Lua can be created using curly braces {} or the table library functions. For example:

```
-- Using curly braces
local myTable = {}

-- Using table library function
local myTable = table.create()
```

-   Key-Value Pairs:
    Tables store data as key-value pairs, where the keys can be of any type (except nil) and the values can be any valid Lua value. Keys are used to access the corresponding values. For example:

    (**Important note for tables: Remember to put the commas on your tables! You don't need a comma on your last table entry, but it doesnt hurt to have it.**)

```
local person = {
  name = "John",
  age = 25, -- Comma needed
  isStudent = true -- Comma not needed
}
print(person.name)  -- Output: John
print(person.age)   -- Output: 25
print(person.isStudent)  -- Output: true
```
-   Table Access:
    You can access table values using square brackets [] or dot notation .. For example:

```
local person = {
  name = "John",
  age = 25
}
print(person["name"])  -- Output: John
print(person.age)      -- Output: 25
```

-   Adding and Modifying Table Elements:
    You can add new key-value pairs or modify existing ones by assigning values to them. For example:

```
local person = {
  name = "John",
  age = 25
}
person.isStudent = true  -- Adding a new key-value pair
person.age = 26         -- Modifying an existing value
```

-   Iterating Over Tables:
    Lua provides different ways to iterate over the elements of a table. The pairs() function can be used to iterate over all key-value pairs, while the ipairs() function is specifically used for iterating over array-like tables. For example:

```
local fruits = {"apple", "banana", "orange"}
for key, value in pairs(fruits) do
  print(key, value)
end
-- Output:
-- 1   apple
-- 2   banana
-- 3   orange
```

Table Length:
You can get the length of an array-like table (the number of elements) using the # operator. However, note that this doesn't work for tables with mixed key types or non-consecutive numeric keys. For example:

```
local fruits = {"apple", "banana", "orange"}
print(#fruits)  -- Output: 3
```

-   Table Methods:
    Lua provides several useful methods to manipulate tables, such as table.insert(), table.remove(), and table.sort(). These methods allow you to insert elements, remove elements, and sort arrays, respectively.

Tables are a powerful feature in Lua and are widely used for organizing and manipulating data. They offer flexibility and can be used in various ways depending on your program's needs.


## Functions

 In Lua, functions are blocks of reusable code that can be called and executed multiple times. They allow you to encapsulate logic, improve code organization, and promote the concept of "Don't Repeat Yourself" (DRY), which encourages reusing code instead of duplicating it. Here's an explanation of functions and how they relate to the DRY principle:

-   Function Declaration:
    In Lua, you can declare a function using the function keyword, followed by the function name, parentheses for parameters (optional), and a block of code enclosed in end. For example:

```
function greet()
  print("Hello, world!")
end
```

-   Function Parameters:
    Functions can take input values called parameters or arguments. Parameters are specified within the parentheses during function declaration. For example:

```
function greet(name)
  print("Hello, " .. name .. "!")
end

greet("John")  -- Output: Hello, John!
``` 
    
-   Function Return Values: (Referenced briefly in Variable assignment)
    Functions can also return values using the return keyword. This allows functions to compute a result and pass it back to the caller. For example:

```
function add(a, b)
  return a + b
end

local result = add(3, 5)
print(result)  -- Output: 8
```

-   Function Reusability and DRY:
    The concept of DRY encourages avoiding code duplication by writing reusable functions. When you encounter a task that needs to be performed multiple times, you can define a function for that task and call it whenever needed. This improves code maintainability and reduces the chances of introducing errors. For example:

```
    function greet(name)
      print("Hello, " .. name .. "!")
    end

    greet("John")
    greet("Jane")
    greet("Alice")
```

In this example, instead of writing the greeting code multiple times, we define a greet() function once and call it with different names. This adheres to the DRY principle and avoids repetition.

-   Function Scope:
    Variables declared within a function have local scope, which means they are only accessible within that function. This allows functions to have their own set of variables without interfering with other parts of the program.

Functions are a fundamental building block in Lua programming. They enable code reuse, promote modularity, and play a crucial role in adhering to the DRY principle by avoiding code duplication. By defining functions for common tasks, you can write more efficient and maintainable code.

## Usage of Libraries and Frameworks

Libraries (Libs) and Frameworks can be used to enhance the Lua langauge.

### What is the difference between Libs and Frameworks?

-   Libraries:
    Libraries in Lua are collections of reusable code that provide specific functionality. They are typically designed to solve specific problems or provide utility functions. Lua libraries are often distributed as standalone modules or files that can be included in your Lua scripts. Libraries can be developed by the Lua community or by individuals and organizations to extend Lua's capabilities. They provide ready-to-use functions and modules that you can incorporate into your Lua code. Examples of Lua libraries include lpeg (for pattern matching and parsing), luasocket (for networking), and luafilesystem (for file system operations).

-   Frameworks:
    Frameworks, on the other hand, are more comprehensive software structures that provide a foundation or a set of tools to build applications. Frameworks often impose a specific architecture or design pattern to structure your code and provide a framework-specific way of solving problems. They are more opinionated and offer a higher-level abstraction compared to libraries. Frameworks in Lua typically provide a complete set of tools, modules, and conventions to develop specific types of applications, such as web frameworks or game frameworks. Examples of Lua frameworks include LÖVE (for game development), OpenResty (for web development with Nginx), and Sailor (a web framework).

## Misc. Topics

These are miscellaneous topics and sections that could be useful for later in your programming career!

Table of Contents for Misc. Topics:
- [Object Oriented Programming (OOP)](#object-oriented-programming-oop)


### Object Oriented Programming (OOP)

In Lua, you can implement object-oriented programming (OOP) concepts using tables and metatables. While Lua doesn't have built-in classes like some other programming languages, you can create objects and define their behavior using metatables. Here's a simplified explanation of OOP in Lua:

-   Objects and Tables:
    In Lua, objects can be represented using tables. Tables can store data and functions, making them suitable for constructing objects. Each object is an instance of a table.

-   Metatables:
    Metatables are special tables in Lua that define the behavior of other tables (objects). By assigning a metatable to a table, you can specify how operations like indexing, assignment, and arithmetic should be handled. Metatables allow you to define custom methods and control the behavior of objects.

-   Creating Objects:
    To create an object, you typically start by creating a table and setting its metatable to define its behavior. You can define methods as functions inside the metatable. For example:

```
-- Define a metatable with methods
local myClass = {
  value = 0,
  increment = function(self, amount)
    self.value = self.value + amount
  end
}

-- Create an object and set its metatable
local myObject = {}
setmetatable(myObject, { __index = myClass })

-- Use the object and its methods
print(myObject.value)      -- Output: 0
myObject:increment(5)
print(myObject.value)      -- Output: 5
```

In this example, myClass is the metatable defining the behavior of the objects. increment is a method defined inside the metatable. By setting the metatable of myObject to myClass, myObject inherits the methods and properties defined in myClass.

-   Method Invocation:
-   When calling a method on an object, Lua provides a shorthand syntax using the colon (:) operator. The colon automatically passes the object as the first argument (self) to the method. For example:

```
myObject:increment(5)
```
    This is equivalent to myObject.increment(myObject, 5), where myObject is explicitly passed as the first argument.

-   Inheritance and Polymorphism:
    In Lua, you can achieve inheritance by creating a child table with its own metatable and setting the parent table as its metatable. This allows the child object to inherit methods and properties from the parent object. Polymorphism can be achieved by overriding methods in the child metatable or by adding additional methods specific to the child object.

-   Garbage Collection:
    Lua handles memory management through garbage collection. When an object is no longer referenced, it becomes eligible for garbage collection, and Lua automatically frees the associated memory.

It's important to note that Lua's approach to OOP using tables and metatables is flexible but requires careful design and manual management of object behavior. Several Lua libraries and frameworks provide additional abstractions and conventions to simplify and enhance object-oriented programming in Lua, such as middleclass, Penlight, and LÖVE.
# 🌟 The Programmer's Treasure Trove 🌟

<span style="font-size: 10px;">(*A note for people coming to learn for Roblox development. While this is close to the same language as Roblox's (Luau), this __DOES NOT__ provide a full guide for Roblox scripting. Sorry!*)</span>
### Introduction to Lua

Lua <span style="font-size: 10px;">(*Not to be confused with <span style="color: lightcyan;">[Luau](https://luau-lang.org/)</span>*)</span> is a programming language known for its unique and straightforward syntax. It keeps things simple, making it easier to learn and understand. With Lua, you'll find a clean and intuitive approach that allows you to express your ideas concisely. Its focus on readability and minimalism promotes writing clear and maintainable code.


> Remember! Before learning any programming language... "<u>**Successful programming requires a combination of dedication, continuous learning, and honing of skills.**</u> and almost always dedication is greater than skill! As long as you persevere you will grow!"

## Table of Contents:
- [Introduction](#introduction-to-lua) 
- [Table of Contents](#table-of-contents) 
- [Variables](#variables)
- [Tables](#tables)
- [Functions](#functions)


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

#### Variable Assignment and Manipulation:
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

### Tables

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

```
local person = {
  name = "John",
  age = 25,
  isStudent = true
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

### Functions

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
    
-   Function Return Values: (Referenced briefly in [Variable assignment](#variable-assignment-and-manipulation))
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
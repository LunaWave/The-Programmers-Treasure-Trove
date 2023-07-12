# 🌟 The Programmer's Treasure Trove 🌟

<span style="font-size: 10px;">(*A note for people coming to learn for Roblox development. While this is close to the same language as Roblox's (Luau), this __DOES NOT__ provide a full guide for Roblox scripting. Sorry!*)</span>
### Introduction to Lua

Lua <span style="font-size: 10px;">(*Not to be confused with <span style="color: lightcyan;">[Luau](https://luau-lang.org/)</span>*)</span> is a programming language known for its unique and straightforward syntax. It keeps things simple, making it easier to learn and understand. With Lua, you'll find a clean and intuitive approach that allows you to express your ideas concisely. Its focus on readability and minimalism promotes writing clear and maintainable code.


> Remember! Before learning any programming language... "<u>**Successful programming requires a combination of dedication, continuous learning, and honing of skills.**</u> and almost always dedication is greater than skill! As long as you perservere you will grow!"

## Table of Contents:
- [Introduction](#introduction-to-lua) 
- [Table of Contents](#table-of-contents) 
- [Variables](#variables)
- [Tables](#tables)


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
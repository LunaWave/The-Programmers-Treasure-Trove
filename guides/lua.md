# 🌟 The Programmer's Treasure Trove 🌟

<span style="font-size: 10px;">(*A note for people coming to learn for Roblox development. While this is close to the same language as Roblox's (Luau), this __DOES NOT__ provide a full guide for Roblox scripting. Sorry!*)</span>
### Introduction to Lua

Lua <span style="font-size: 10px;">(*Not to be confused with <span style="color: lightcyan;">[Luau](https://luau-lang.org/)</span>*)</span> is a programming language known for its unique and straightforward syntax. It keeps things simple, making it easier to learn and understand. With Lua, you'll find a clean and intuitive approach that allows you to express your ideas concisely. Its focus on readability and minimalism promotes writing clear and maintainable code.

## Table of Contents:
- [Introduction](#introduction-to-lua) 
- [Table of Contents](#table-of-contents) 
- [Variables](#variables)


### Variables

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

That's a simple overview of variables in Lua. They are fundamental for storing and manipulating data in Lua programs.
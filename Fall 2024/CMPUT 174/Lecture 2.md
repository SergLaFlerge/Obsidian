The real goal of the course is learning computational problem solving *before* the programming.

The biggest skill to learn is *problem decomposition*. This is where we break a problem down into smaller tasks that are manageable.

We need to be able to represent the essential information about a problem (abstraction), and then a way to be stored in a computer (modeling.)

We need to learn how to make effective plans and procedures to solve the problem (algorithm design).

# What is programming?

It's the process of writing computer programs; a way to translate our algorithms into machine instructions.

## Low Level VS High Level Programming

Low level programming is not very human readable, with little to no abstraction, whereas high level programming is very human readable, with more abstraction.

It is easier to write complex programs in high level languages.

### What is Python?

Python is a high level, object oriented programming language. In about python, we have different types of objects, each of different types, identities, and values.

- ID is simply the location in the memory of the object.
- The type of object determines how much space it takes, as well as the types of operations you can do on it.
- The value of the object is simply what the object is representing.

```python
import time
age = input("Enter legal driving age: ")
time.sleep (0.5)
print("The legal driving age is" + age)
```

How do you know the ID of an object? Python has a built-in function called id that tells you exactly that. There is a similar function for the type of object (type).

These objects are how we represent the essential properties of our task/problem. We can for example give data objects names:

```python
number = 174
```

The python language has many types of statements, which help with different types of tasks. These can be conditionals (if, elif, else), or tasks that need to be repeated continuously (while loops, for loops).

# Tokenization

What is a token? It is the smallest unit of meaning, much like how punctuation, verbs, adjectives, etc. are tokens of language. There are five tokens we care about, following the acronym KILOD:

- Keyword.
- Identifier.
- Literal.
- Operator.
- Delimiter.

# Parsing Statements

This is the process of interpreting the tokens. Python reads statements left-to-right and top-to-bottom.

#flashcards174

The ID of an object is ==where in the memory it is located.==
<!--SR:!2024-09-22,10,250-->

The type of object determines  two things: ==how much space it takes, as well as the types of operators that can be used on it.==
<!--SR:!2024-09-28,11,230-->

The acronym KILOD stands for::keyword, identifier, literal, operator, delimiter.
<!--SR:!2024-10-14,23,250-->

A ==token== is smallest meaningful unit in a program.
<!--SR:!2024-10-03,15,250-->

Words reserved for a specific purpose are called::keywords.
<!--SR:!2024-09-23,10,270-->

==Identifiers== are used to refer to objects in memory (built-in or user made.)
<!--SR:!2024-09-25,8,210-->

==Literals== are used to represent constant, fixed values.
<!--SR:!2024-09-22,10,250-->

There are three kinds of literals: ::Integer literals, floating point literals, and string literals.
<!--SR:!2024-10-11,20,250-->

 Integer literals are composed of ==only digits (whole numbers.)==
<!--SR:!2024-10-14,23,250-->

Floating point literals are composed of ==only digits and a single decimal point.==
<!--SR:!2024-10-03,15,250-->

String literals are composed of ==any characters surrounded by single or double quotes.==
<!--SR:!2024-10-11,20,250-->

Operators are used to refer to ==operations on objects.==
<!--SR:!2024-10-07,18,250-->

T/F: There are operators in python that are not represented by operator tokens. :: True.
<!--SR:!2024-10-07,18,250-->

Special characters with varying functions are called ==delimiters.==
<!--SR:!2024-10-11,20,250-->
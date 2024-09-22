 ```python
 result = True == ('5'*4)
 ```

Here, from left to right, we have an identifier, delimiter, keyword, operator, delimiter, string literal, operator, integer literal, and delimiter.

# Mutablity

You can't change the ID are the type of object, but you can change the value of an object. This is called mutablity. Things that can be changed are called mutable, and things that can't are called immutable. To e

# Types

Int, float, and string objects are immutable. They have a literal representation that can't be changed. We may assign a variable to represent any of these objects, but if we change what the variable represents, we are accessing another object entirely. If

```python
a = 4
a = a + 1
```

And we check the id of $a$, we will get two different ids, meaning we are accessing different objects.

In a string, we can specify a single character to access using a process called *subscription*. When we look for a specific character, we start counting (indexing) from 0, therefore, in the string

```Python
'CMPUT174'[1]
```

We will obtain the character "M" as opposed to "C". We can also use a negative index to take from the back, for example,

```Python
'CMPUT174'[-1]
```

Will return "4".

We can also take chunks (called "slicing") of a string using [n:m], where n is the starting position and m is *one more* than where we want to stop. For example

```python
'CMPUT174'[0:5]
```

Will return "CMPUT". We can also leave either n or m blank, which will slice starting from 0 or ending at -1 respectively. Slicing a string will also give you a string.

We can also find the length of a string by using 

```Python
len()
```

Another immutable type is called bool. Booleans are simply True or False in python. Operations are not usually done on operators, but they are often the results of certain questions. For example,

```Python
1 == 1
```

Will return "True". True and False are the only bools in python.

We have another type called "None", which represents nothing. Its class is "NoneType". Confusing at first but useful, probably.

Yet type is called a list. It is a container that can hold many other objects, including other lists. Lists *are mutable*, so you can change the contents of the list while keeping the same id. Just like strings, we can also do subscription, slicing, and len, with the same 0-based indexing. Slicing a list also gives a list.

A very similar object to a list is a tuple. The one difference is that a tuple is immutable.

```Python
list = [1,'a', None, 64]
tuple = (1,'a', None, 64)
```

Lists use "[]" and tuples use "()".

## Function Type

All python functions are bound to objects in memory. Objects that represent functions can have different types base the on how and where they are defined. Python has built-in functions, but we can make our own as well, and even imported from libraries that people have already made.

## Module Type

A module is simply a collection of functions. These can be imported and they provide specific functionality for certain tasks.
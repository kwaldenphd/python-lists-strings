# Lists and Strings in Python

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

## Lab Objectives
- Practice utilizing lists and strings in the Python programming language
  * For strings, this includes creation, length and access, basic list operations, and basic method arguments
  * For lists, this includes creation, access, iteration, nesting, searching, concatenating, growing, deleting, sorting, and reversing
- Understand and articulate the differences between lists and strings
- Use Python methods and functions to work with strings and numbers

## Acknowledgements

Elements of this lab procedure were adapted from materials developed by [Dr. Peter Bui](http://www3.nd.edu/~pbui/) for the [CSE 10101 "Elements of Computing I" course](https://www3.nd.edu/~pbui/teaching/cdt.30010.fa16/).
- [Reading 05: Lists, Strings](https://www3.nd.edu/~pbui/teaching/cdt.30010.fa16/reading05.html)
- [Notebook 05: Lists, Strings](https://www3.nd.edu/~pbui/teaching/cdt.30010.fa16/notebook05.html)

Elements of this lab procedure were adapted from materials developed by [Dr. Janet Davis](https://cs.whitman.edu/~davisj/) for the the [CSC 105 "The Digital Age" course](https://www.cs.grinnell.edu/~davisjan/csc/105/2012S/). 
- [Laboratory: Programming in Python](http://www.cs.grinnell.edu/~davisjan/csc/105/labs/python1.html)

Elements of this lab procedure were adapted from materials developed by [Dr. Corey Pennycuff](https://www3.nd.edu/~cpennycu/) for the [CSE 10101 Elements of Computing (Fall 2019)](https://www3.nd.edu/~cpennycu/2019/fa-CSE10101-CDT30010.html).

Elements of this lab procedure were adapted from materials developed by [Lindsay K. Mattock](http://lindsaymattock.net/) for the the [SLIS 5020 Computing Foundations course](http://lindsaymattock.net/computingfoundations.html). 

# Table of Contents
- [Python Syntax: Methods and Functions](#python-syntax-methods-and-functions)
- [Working With Strings and Variables](#working-with-strings-and-variables)
- [Combining Variable Types](#combining-variable-types)
- [Working With Lists](#working-with-lists)
  * [A List of Strings](#a-list-of-strings)
    * [A few additional functions that can be useful when working with lists](#a-few-additional-functions-that-can-be-useful-when-working-with-lists)
  * [A List of Numbers](#a-list-of-numbers)
- [How to submit this lab (and show your work)](#how-to-submit-this-lab-and-show-your-work)
- [Lab Notebook Questions](#lab-notebook-questions)
  

# Python Syntax: Methods and Functions

1. Python has some specific terminology used to describe elements of code.

2. Syntax: Programming languages have their own syntax, which are a set of rules that determine how programs (commands, lines of code) are written and interpreted. The language syntax includes both elements of the code visible to human readers as well as elements of the code executed by the machine.

3. Function: We have a whole lab coming up on functions. For now, we can think of functions as a group of statements that perform a specific task. Python includes built-in functions like `print()`, `dict()`, `input()`, `int()`, and `len()`, but also allows you to create your own functions. Data, parameters, or arguments can be passed into a function, and a function can also return data.

4. Parameters and arguments can be used interchangeably in Python.

5. Method: In Python, a method is something that is applied to an object. That object could be a variable, string, number, or other type of data. A method is a function that is available for objects based on their type. For example `append()`, `extend()`, `sort()`, and `reverse()` are all methods that can be used with `list` object types. `capitalize()`, `upper()`, `lower()`, and `title()` are all methods that can be used with `string` object types.

6. Function vs. Method: Functions are generic, while a method is called on an object. A method is associated with an object (and can access/interact with the data or information that is part of that object). Functions do not alter the state of an object, while a method can alter an object state.

# Variables

7. We worked with variables in our first Python lab. A variable is a placeholder for a piece of information. You can think of it as a basket or container. 

8. Python has a few rules for variables:
- Variable names can only include letter, numbers, or underscores, but cannot start with a number.
- Spaces are not permitted.
- The names of Python methods and functions are reserved, meaning that they cannot be used as variable names. So, `print` cannot be used as a variable name.
- As a rule, variable names should be short and descriptive.

<blockquote>Q1: In your own words, explain the difference between <code>print(hello)</code> and <code>print(“hello”)</code>.</blockquote>

# Strings

9. Refresh: What are strings? A string is a sequence of characters. Although we can have list of characters, often times we want to access and manipulate the sequence as an aggregate set of text rather than individual letters. Strings are identified by the <code>“ ”</code> or alternatively by <code>‘ ’</code>.

```Python
# example that creates a new string variable
first_name = 'Katherine'

# check variable type
type(first_name)

# view value of first_name variable
first_name
```

```Python
# example that converts integer to string
str(10)

# example that converts float to string
str(15.0)

# example that converts boolean to string
str(True)
```

10. Because certain operations on strings are so common, Python includes a variety of built-in methods that you can apply to a string object:

## Title Methods

11. Let's look at an example that uses different title methods.

```Python
# example using my name
name = "katherine walden"
```

11. Next, we’ll use the `print` function with the method `title`. Python functions and methods always end with a `()`. Methods define an additional action that can be applied to the data.
```Python
# example using my name, printed in title case
name = "katherine walden"
print(name.title())
```

12. Your program should output your data with a leading capital letter.

13. We can also change the case using the `upper()` method and `lower()` method: `print(name.upper())` outputs your string with all capital letters, while `print(name.lower())` outputs your string in all lower case.

`Katherine Walden`
`KATHERINE WALDEN`
`katherine walden`

14. Try adding two additional `print()` functions calling the `name` variable with each of these methods.  

<blockquote>Q2: Describe the syntax of the three commands that we just used (steps 10-14) in your own words. What is this code doing? Define the function and method for each example.</blockquote>

```Python
first_name = "katherine"
last_name = "walden"
full_name = first_name + " " + last name
```
## Concatenation

15. Let’s modify our code a bit and create two new variables `first_name` for your first name and `last_name` for your last name. We can then combine these two string variables (called concatenation) in a third variable called `full_name`.

16. If we want our first and last name to be separated by a space, we need to tell Python to add one in by including the `“ “`, otherwise, each string will be printed back-to-back.
```Python
first_name = "katherine"
last_name = "walden"
full_name = first_name + " " + last name

print(full_name)
```

17. We can then use the `print()` function as we did before to output `full_name` in title case.
```Python
first_name = "katherine"
last_name = "walden"
full_name = first_name + " " + last name

print("Hello, " + full_name.title() + "!")
```

18. We could combine strings and variables in the same `print()` function to output a full sentence to the screen.
```Python
first_name = "katherine"
last_name = "walden"
full_name = first_name + " " + last name

sentence="Hello, " + full_name.title() + "!"

print(sentence)
```

19. We could also assign this whole sentence to a variable and return the same output.

<blockquote>Q3: Explain how each of these two programs (steps 15-18) work in your own words.</blockquote>

### Combining Variable Types

20. Python works with integers (whole numbers) and floats (any number with a decimal point). Python uses the basic mathematic symbols to perform functions: `+` (add), `-` (subtract), `*` (multiply), `/` (divide). 

21. Try this program:
```Python
print(2+3)
print(2-3)
print(2*3)
print(2/3)
```
<blockquote>Q4: Why does <code>print(2//3)</code> return 0? How would you modify your code to return the decimal number? Why?</blockquote>

22. Hint: Try `print(2.0//3.0)` using the floating point integers (numbers with decimal points).

23. Let’s write a new program with an integer variable and a string variable. Feel free to modify course number and department if taking this as something other than CSE 10101.
```Python
course_name="Elements of Computing I"
course_number = 10101

print("Welcome to " + course_name.title() + " CSE:" + course_number)
```
24. When you run the program, you will receive an error.

<p align="center"><a href="https://github.com/kwaldenphd/Python/blob/master/images/Image_8.png?raw=true"><img class="aligncenter" src="https://github.com/kwaldenphd/Python/blob/master/images/Image_8.png?raw=true" /></a></p>

25. The `type` error is telling us that we cannot use these two different variable types in the same function. 

26. When we want numbers to be read as characters rather than numeric digits, we have to use the string method `str()` to convert the integer into a string of characters.
```Python
print("Welcome to " + course_name.title() + " CSE:" + str(course_number))
```
<blockquote>Q5: Explain concatenation in your own words. Why must we convert numbers to strings in the program above? Refer to this example and the previous example.</blockquote>

<blockquote>Q6: Write a program that converts integer, float, or boolean values to a string, using the <code>str</code> function.</code></blockquote>

## String Length and Access

We can get the length or size of a string by using the `len` function.

```Python
len(first_name)
```

27. We can also extract (or modify) individual characters within a string. To do so, we need a way to specify which character we mean. 

28. This is done by giving each position in the string an `index number` or `index operator`, which is determined by simply counting off (starting at 0) from left to right. 

29. We then use the index number as a subscript into the string. 

```Python
# access first character in string
first_name[0]

# access last character in string
first_name[-1]
```

30. In Python there is no notion of a character type as there is in languages such as Java or C. So when we check the type for a character in a string, we get back another string.

```Python
type(first_name[0])
```

30. Another example: let's say we have a variable `color` that includes the string `"turquoise"`.

32. Then...
- `color[0]` holds the letter `t`
- `color[1]` holds the letter `u`
- `color[2]` holds the letter `r`
- etc

<blockquote>Q7: Write a program that prompts the user to enter a 6-letter word, and then prints the first, third, and fifth letters of that word.</blockquote>
 
31. A sample output for your program might look like this:
```
Please enter a 6-letter word: joyful
The first, third, and fifth letters are: j y u
```
NOTE: Strings in Python are immutable, which means that you cannot change the elements of a string once it is set.

The following program will result in a `TypeError`.

```Python
first_name[0] = 'k'
```
So what do you do when you want to update a string? You simply construct a new one!

```Python
first_name = 'k' + first_name[1:]
first_name
```
## Other String Operations

Since a string is a sequence of characters, there are a few other operations that work on strings.

### Length

We've already seen the `len` function in action, but to refresh:

```Python
len(first_name)
```

### Properties

We can check the properties of characters in a string.
- `.isalpha()` checks if all string values are letters
- `.isalnum()` checks if string includes only letters and numbers
- `.isdigit()` checks if all string values are numbers
- `.islower()` checks if all string includes any lower-case characters
- `.isspace()` checks if the string includes any whitespace characters
- `.istitle()` checks if the string includes any title-case characters
- `.isupper()` checks if the string includes any upper-case characters

To see these string property methods in action in Python syntax:

```Python
# checks if all string values are letters
'abc123'.isalpha()

# checks if string values are letters and numbers
'abc123'.isalnum()

# checks if all string values are numbers
'abc123'.isdigit()

# checks if string includes any lower-case characters
'abc123'.islower()

# checks if string includes any whitespace characters
'abc123'.isspace()

# checks if string includes any title-case characters
'abc123'.istitle()

# checks if string includes any upper-case characters
'abc123'.isupper()
```

These commands return Boolean `True` or `False` values.

### Sort

We can sort characters in a string alphabetically or reverse alphabetically.

```Python
# sort alphabetically
sorted(first_name)

# reverse sort
reversed(first_name)
```

These commands output the characters in the string in alphabetical or reverse alphabetical order.

### Max and Min

We can also get the maximum or minimum value in the string. For strings that are sequences of characters, the minimum value is the character that appears first in the English-language alphabet, and the maximum is the character that appears last in the English-language alphabet.

```Python
# get max string letter
max(first_name)

# get min string letter
min(first_name)
```

### In Operator

We can also use the `in` operator to check if a character or substring (combination of characters) is present in another string.

```Python
# checks is 'a' is in 'abcd' string
'a' in 'abcd'

# checks if 'e' is in 'abcd' string
'e' in 'abcd'

# checks if 'bc' is in 'abcd' string
'bc' in 'abcd'
```

Each of these `in` operator examples returns a Boolean value, `True` or `False`.


### Search

32. We can also instruct the computer to search for a given character within a string.

34. There are a few different search methods we can use with strings:
 - `.startswith()` checks if the string starts with a character or substring
 - `.endswith()` checks if the string ends with a character or substring
 - `.find()` locates the index position for a specific character or substring
 - `.index()` also locates the index position for a specific character or substring
 
 NOTE: The `.find()` method returns `-1` if the character or substring is not found. The `.index()` method will throw an error if the character or substring is not found.
 
 To see these methods in action using Python syntax:
 
 ```Python
 # checks if string starts with 'the' substring
'the boy who blocked his own shot'.startswith('the')

# checks if string ends with 'shot' substring
the boy who blocked his own shot'.endswith('shot')

# locates index position for 'who' substring
# note .find() outputs the index position for the first character in the substring
'the boy who blocked his own shot'.find('who') 

# checks if 'who' substring is located at index position 10
# note -1 return means the substring was not located at that position
'the boy who blocked his own shot'.find('who', 10)

# locates index position for 'who' substring
'the boy who blocked his own shot'.index('who') 

# checks if 'who' substring is located at index position 10
# unlike .find(), .index() will return a ValueError if the substring is located at that position
'the boy who blocked his own shot'.index('who', 10)
```

33. Let's look at another example.

Say we have a variable `color` holds the string `"turquoise"`. 

We can retrieve the index of the letter `q` (which is 3) as follows:
```python
color = "turquoise"
index_number = color.index("q")
print ("The index number for the letter u within the word " + color + " is", index_number)
```

<blockquote>Q8: Modify the program to have it search for other characters in the string. Does it always return the index number you expect? What index is returned if you ask for the index of the letter u (i.e., what happens when the desired character appears more than once in the string)?</blockquote>

# Working With Lists

34. Python allows us to store information in a few different ways. 

36. In this lab, we're focusing on lists, which are an ordered collection of items.

The individual values in a list are called elements or items. 

Lists have a type and are also considered values themselves.

```Python
# create a list containing 4 numbers
[0, 1, 2, 3]

# assign that list to a variable
numbers = [0, 1, 2, 3]

# check types of numbers variable
type(numbers)
```

Although this is rare, list elements do not need to be the same type.

```Python
[0, 1.0, 'a']
```

## List Length and Access

We can use the `len` function to get the length of a list.

```Python
len(numbers)
```

We can also use the index operator and index position to access and manipulate elements in a list.

```Python
# access first item in a list
numbers[0]

# access last item in a list
numbers[-1]
```

```Python
# modify first item in a list
numbers[0] = 'zero'
numbers
```

A few other notes on index operators:

Indeces can be any integer expression.

A few examples:

```Python
# `numbers[0+1]` is the same as `numbers[1]`
numbers[0+1]
numbers[1]

# index position stored as a variable
index = 1
numbers[index]
numbers[1]

# index position as a multiplication product
numbers[index * 2]
numbers[2]
```

An invalid index will yield an IndexError.

```Python
numbers[1000]
```

And as covered with strings, a negative index will start at the end of the list and count right to left.

```Python
# access last item in list
numbers[-1]

# access next to last item in list
numbers[-2]
```

## Modifying Lists

While strings are immutable, items in a list can be modified.

An example we've seen before that modifies a single list item.

```Python
# modify first item in a list
numbers[0] = 'zero'
numbers
```

We can also grow an existing list using the `.append()` or `.extend()` methods.

```Python
# add integer 4 to end of numbers list
numbers.append(4)
numbers

# add [5,6,7] to end of numbers list
numbers.extend(range(5, 8))
numbers
```

To unpack what happened in that last bit of code- the `range()` function returns a sequence of numbers.

The default `range()` function starts at `0`, but in this example we start at `5`. 

The default `range()` function moves by increments of `1` and stops before a specified number. In our example, `range()` stops before 8.

The core syntax for range:
`range(start, stop, step)`

We can delete items from a list using the `pop()` method or the `del` statement.

```Python
# remove an item at index 0 and return just that item
numbers.pop(0)

# remove an item at index 0
del numbers[0]
```

## Empty Lists

A list with no items is called an empty list.

We can also use the `list()` argument to create an empty list.

Examples in Python syntax:

```Python
# create empty list
[]

# create empty list using list()
list()
```

## Nesting and Sublists

Lists can also contain other lists- this is referred to as nested lists or sub-lists.

```Python
# create list with two sub-lists
points = [[0, 1], [2, 3]]
points

# access first item on list, which is a sublist
points[0]

# access first item WITHIN second item on list; 
# core syntax: list_name[list_item_number][sublist_item_number]
points[1][0]
```

## Lists and the In Operator

Like with strings, we can use the `in` operator to test if a list contains a specific value.

```Python
# checks if 0 is i numbers
0 in numbers

# checks if 5 is in numbers
5 in numbers
```

Both of these commands return Boolean `True` or `False` statements.

## Concatenation

We can concatenate (or join) two lists using the `+` operator.

```Python
[0, 1, 2,] + [3, 4, 5]
```

## Copying

We can copy a list using the `*` (multiplication) operator.

```Python
[0, 1, 2] * 3
```

## Sorting

As with strings, we can sort the items in our list.

We have two options when sorting items in a list.

Sorting a list **in-place** changes the underlying order of items in the list.

Generating a sorted version of a list **does not** change the underlying order of items in the list.

Let's look at a few examples using Python syntax.

```Python
# create numbers list
numbers = [2, 4, 1, 3]

# sort list in place to update list order
numbers.sort()

# show updated list
numbers
```

```Python
# generate sorted version of list; DOES NOT change underlying order
sorted(numbers)

# will return original list order
numbers

# assign results of sorted() to new variable
sorted_numbers = sorted(numbers)

# show new variable with sorted list
sorted_numbers
```

### Reverse

We can reverse a list using the `.reverse()` method of the `reversed()` function.

As with `.sort()` and `sorted()`, we have the option to reverse in-place or generate a reversed version of the original list.

To demonstrate using Python syntax:

```Python
# create list using range()
numbers = range(0, 7)

# reverse list in-place
numbers.reverse()

# show reversed list
numbers
```

```Python
# generate reversed version of list
reversed(numbers)

# show original list
numbers

# create new variable with reversed list
reversed_numbers = reversed(numbers)

# show new varaible with reversed list
reversed_numbers
```

## Utility Functions

A few other functions that come in handy when working with lists that contain numbers.
- `sum()` calculates the sum of items in a list
- `max()` identifies the highest value in a list
- `min()` identifies the lowest value in a list
- `random.choice()` selects a list item at random
- `random.shuffle()` shuffles items in a list in-place
- `random.sample()` samples a select number of items from a list

Examples for each in Python syntax:

```Python
# compute the sum of a list
sum([0, 1, 2, 3])

# assign list to variable 
list = ([0, 1, 2, 3])

# compute sum of list using variable name
sum(list)
```

```Python
# find max value of list
max([0, 1, 2, 3])

# find max value of list using variable name
max(list)
```

```Python
# find min value of list
min([0, 1, 2, 3])

# find min value using list variable
min(list)
```

```Python
# select element at random
random.choice(list)
```

```Python
# shuffle a list in-place
random.shuffle(list)
```

```Python
# sample 2 elements from a list
# core syntax: random.sample(list_name, number_of_elements)
random.sample(list, 2)
```

## Looking Ahead

In the next lab, we'll talk all about conditional statements.

But for now, let's take a step back and think about how Python interacts with or treats the items in our list.

For example, when we're using the `in` operator, how does Python test for membership (i.e. see if the value we're looking for is located in the list)?

Python accomplishes this via **iteration**, which involves iterating over each item in the list. 

So Python starts at the first item in the list (index position `0`), and goes through each item on the list (left to right) until it reaches the end of the list.

Again, we will have a whole lab on conditional statements, but a few quick examples for now just to illustrate the concept of iteration.

We can use a **`for` loop** to iterate over the items in a list.

```Python
for number in numbers:
 print(number)
```

We can iterate over just the indeces in the list.

```Python
for i in range(len(numbers)):
 print(number[i])
```

We can retrieve the item and the index position using the `enumerate()` function.

```Python
for i, number in enumerate(numbers):
 print(i, number)
```

Again, more to come on conditional statements.

<blockquote>Q9: Create your own list of numbers. Include your list code as part of this question answer. What is the length of your list? What is the number position for each of the items in your list? How would you return the value of the first item? How would you return the value of the last item?</blockquote>

<blockquote>Q10: Using the same list from the previous question, write a program that includes the following steps or components:
<ol type="a">
 <li>Adds a new item to your list</li>
 <li>Deletes an item from your list</li>
 <li>Sorts your list in-place</li>
 <li>Generates a sorted version of your list</li>
 <li>Reverse sorts your list in-place</li>
 <li>Generates a reverse sorted version of your list</li>
 <li>Determines the <code>min</code> and <code>max</code> values for your list</li>
 <li>Selects an list element at random</li>
 <li>Shuffles your list</li>
</ol>
</blockquote>

## Lists of Strings

We 

37. Write a list of a few of your favorite things.
```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
```

38. We can print this list with a print function `print(cookies)`, but Python returns a representation of the list, just as we entered it.
`['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']`

39. This isn’t particularly useful by itself; however, we can use the position of each item (the `index`) to perform different functions.

40. Add a `print()` function calling a specific item on your list.
```Python
print(cookies[0].title())
```

41. This command returns the first item on my list. This is the item in the `0` position on my list.
```Python
Chocolate Chip
```

42. Items in a list are indexed with a number, **beginning with 0 NOT 1.**

43. A `print` function that outputs the last item on my list of four items would look like this.
```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print(cookies[3].title())
```

44. We can also work backwards (left-to-right) on our list using negative numbers. For example, to call the last item on the list we could also use the index position `-1`.
```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print(cookies[-1].title())
```

45. To return the second to last item, we could use `-2`. For the third to last `-3`, etc.

46. We can concatenate our list items in strings.
```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
print("My favorite cookie to bake is " + cookies[1].title() + ".")
```
47. Which outputs `My favorite cookie to bake is snickerdoodle.`

48. We can also change the items in a list. 

49. Maybe I have a friend who is allergic to peanut butter. I can change the `peanut butter` entry.
```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
cookies[2] = 'oatmeal'
print(cookies)
```
50. The `print()` function outputs the modified list.
`['chocolate chip', 'snickerdoodle', 'oatmeal', 'sugar']`

51. We can also add data to our list using the append function.
```Python
cookies = ['chocolate chip', 'snickerdoodle', 'peanut butter', 'sugar']
cookies.append('oatmeal')
print(cookies)
```

52. The `print()` function now returns a list of five items `[chocolate chip, snickerdoodle, peanut butter, sugar, oatmeal]`

53. We can also use `append()` to create new lists.
```Python
my_pets = []
my_pets.append('Christy Mathewson')
my_pets.append('Smoky Jo Wood')
my_pets.append('Sandy Koufax')
print(my_pets)
```

54. In this block of code, we started with an empty list `[]`. Then the next two lines with `append()` add new items to the list.

55. With `append()`, items are added to the end of the list. 

56. The `insert()` function allows us to add items to any position in the list.
```Python
fruit = ['apple', 'pear', 'banana']
fruit.insert(1, 'orange')
print(fruit)
```
57. This block of code adds orange to the second position on the list (index position 1).

58. The output is `['apple', 'orange', 'kiwi', 'banana']`

59. Conversely, the `del` statement allows you to delete items from your list using the index number.

60. The following code will remove `orange` from the list.
```Python
fruit = ['apple', 'orange', 'pear', 'banana']
del fruit[1]
print(fruit)
```

61. We can also delete items by value (instead of position) using `remove()`.
```Python
fruit = ['apple', 'orange', 'pear', 'banana']
fruit.remove('orange')
print(fruit)
```

<blockquote><code>remove</code> only removes the first instance of the value in the list. So, if in the previous example orange appeared on the list a second time, only the first instance would be removed. To remove all instances, you would need to perform a loop (we’ll talk about loops later in the semester).</blockquote>

## A few additional functions that can be useful when working with lists

### `Reverse`

62. To print in reverse order, use `reverse()`.
```Python
fruit = ['apple', 'orange', 'pear', 'banana']
fruit.reverse()
print(fruit)
```

### `Sort`

63. To alphabetize your list, use the `sort()` method.
```Python
fruit = ['apple', 'orange', 'pear', 'banana']
fruit.sort()
print(fruit)
```

### `Len`

64. To find the length of your list, use the `len()` function.
```Python
fruit = ['apple', 'orange', 'pear', 'banana']
length = len(fruit)
print(length)
```
35. To recap: Lists are an ordered collection of items. Lists can be numbers or strings. They are declared with a variable name, but the information is contained within `[ ]` and the individual items are separated by a comma. 

<blockquote>Q11: Create your own list of strings. Include your list code as part of this question answer. What is the length of your list? What is the number position for each of the items in your list? How would you return the value of the first item? How would you return the value of the last item?</blockquote>

<blockquote>Q12: Using the same list from the previous question, write a program that includes the following steps or components:
<ol type="a">
 <li>Adds a new item to your list</li>
 <li>Deletes an item from your list</li>
 <li>Sorts your list in-place</li>
 <li>Generates a sorted version of your list</li>
 <li>Reverse sorts your list in-place</li>
 <li>Generates a reverse sorted version of your list</li>
 <li>Determines the <code>min</code> and <code>max</code> values for your list</li>
 <li>Selects an list element at random</li>
 <li>Shuffles your list</li>
</ol>
</blockquote>

## A List of Numbers

65. We can also work with numbers in lists. 

66. We can create a list in the same way that we did in the previous example, or we can use the `range()` function.
```Python
# in this example we'll wrap the list() function around the range() function to create a list of numbers

numbers = list(range(1,10))
print(numbers)
```

67. This outputs `[1, 2, 3, 4, 5, 6, 7, 8, 9]`

68. You may have expected to see the numbers one to ten printed. This is yet another example of the quirks of working with programming languages. 

69. Python starts with the first number and quits when it reaches the last number of your range. Because it stops at 10, it doesn’t include the 10.

<blockquote>Q8: How would you modify this code to output the full range 1-10?</blockquote>

70. What if we just wanted the odd numbers in this range? We could add an additional value to the `range` function to tell the computer to count by two.
```Python
numbers = list(range(1,11,2))
print(numbers)
```
<blockquote>Q11: How would you rewrite the code to include only the even numbers from 1 to 10?</blockquote>

71. Can you write a program that creates a list that represents all of the different patterns we could represent from 1 bit to 8 bits, like our chart from binary math lab?

- 1 bit - 2 patterns
- 2 bits - 4
- 3 bits - 8
- 4 bits - 16
- 5 bits - 32
- 6 bits - 64
- 7 bits - 128
- 8 bits - 256
- n bits -2<sup>n</sup> patterns

72. Try to write a program that outputs the list: `[2, 4, 8, 16, 32, 64, 128, 256]`.

<blockquote>Hint: a double * represents exponents in Python. So 2<sup>2</sup> would be <code>2**2</code>.</blockquote>

73. There are multiple ways to achieve this output.
```Python
patterns = []
for bit in range(1,9):
  patterns.append(2**bit)
print(patterns)
```

74. Python also allows us to return the minimum value, maximum value, and sum of the numbers in a list.
```Python
patterns = []
for bit in range(1,9):
  patterns.append(2**bit)

print(min(patterns))
print(max(patterns))
print(sum(patterns))
```

75. This program outputs
`2`
`256`
`510`

76. Lists nested within lists are called sub-lists.

77. We can check if something is in a list using the `in` operator.

<blockquote>Q12: Create the list <code>numbers</code> with the following values: <code>[[0, 1], [2, 3], [4, 5]]</code>. 
<ol type="a">
  <li>What is the second element?</li>
  <li>How would you change 4 to 'four'?</li>
  <li>How would you change 1 to 'one'?</li>
  <li>How would you print out each sub-list (one sub-list per line)?</li>
  <li>How would you print out each number (one number per line)?</li>
 </ol>
 </blockquote>
 
# How to submit this lab (and show your work)

80. Moving forward, we'll submit lab notebooks as `.py` files. 

81. One option is to have a `.py` file that you use to run code and test programs while working through the lab. When ready to submit the lab notebook, you add comments and remove extraneous materials.

82. Another option is to have an "official" `.py` file that you are using as a lab notebook (separate from your working/testing file). Use comments in Python to note when you are starting a new question (as well as answering a question).
  * Example: `Lab5_Notebook_Walden.py`

83. What gets submitted as the lab notebook is the `Lab5_Notebook_Walden.py` file.
- When in doubt, use comments
- Be sure you are using comments to note what question you're responding to
 
# Lab Notebook Questions

Q1: In your own words, explain the difference between `print(hello)` and `print(“hello”)`.

Q2: Describe the syntax of the three commands that we just used (steps 10-14) in your own words. What is this code doing? Define the function and method for each example.

Q3: Explain how each of these two programs (steps 15-18) work in your own words.

Q4: Why does `print(2/3)` return `0`? How would you modify your code to return the decimal number? Why?

Q5: Explain concatenation in your own words. Why must we convert numbers to strings in the program above? Refer to this example and the previous example.

Q6: Write a program that converts integer, float, or boolean values to a string, using the `str()` function.

Q7: Write a program that prompts the user to enter a 6-letter word, and then prints the first, third, and fifth letters of that word.

Q8: Modify the program to have it search for other characters in the string. Does it always return the index number you expect? What index is returned if you ask for the index of the letter u (i.e., what happens when the desired character appears more than once in the string)?

Q9: Create your own list of strings. Include your list code as part of this question answer. What is the length of your list? What is the number position for each of the items in your list? How would you return the value of the first item? How would you return the value of the last item?

Q10: Using the same list from the previous question, write a program that includes the following steps or components:
<ol type="a">
 <li>Adds a new item to your list</li>
 <li>Deletes an item from your list</li>
 <li>Sorts your list in-place</li>
 <li>Generates a sorted version of your list</li>
 <li>Reverse sorts your list in-place</li>
 <li>Generates a reverse sorted version of your list</li>
 <li>Determines the <code>min</code> and <code>max</code> values for your list</li>
 <li>Selects an list element at random</li>
 <li>Shuffles your list</li>
</ol>

Q11: How would you rewrite the code to include only the even numbers from 1 to 10?

Q12: Create the list `numbers` with the following values: `[[0, 1], [2, 3], [4, 5]]`
<ol type="a">
  <li>What is the second element?</li>
  <li>How would you change 4 to 'four'?</li>
  <li>How would you change 1 to 'one'?</li>
  <li>How would you print out each sub-list (one sub-list per line)?</li>
  <li>How would you print out each number (one number per line)?</li>
 </ol>

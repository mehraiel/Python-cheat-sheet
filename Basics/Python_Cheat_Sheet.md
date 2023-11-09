## 1- Variables and Data Types


```python
# this called comment : use "#" then write explain or any text (this not run or included as code)

# Variables and Data Types
name = "Alice"          # String
age = 30                # Integer
height = 5.8            # Float
is_student = True       # Boolean (take 2 values only True and False)

print("this to print the name :" , name)
print(f"another way to print age : {age} and the height {height}")
print(is_student) # to print variable only without text
```

    this to print the name : Alice
    another way to print age : 30 and the height 5.8
    True
    

## 2- Basic Operations


```python
# Basic Operations
result_add = 5 + 3          # Addition
result_sub = 7 - 2          # Subtraction
result_mul = 4 * 6          # Multiplication
result_div = 10 / 2         # Division
result_int_div = 11 // 3        # Integer Division
result_rem = 11 % 3      # Modulus (Remainder)

print(result_add , "\t", result_sub) # to make tab between values use this symbol --> \t
print(result_mul , "\n" , result_div) #to make new line use this symbol --> \n
print(result_int_div , result_rem)  # can use "," between variable
```

    8 	 5
    24 
     5.0
    3 2
    

## 3- Strings


```python
# String Operations "TEXT"
greeting = "Hello, " + name     # Concatenation
length = len(name)              # Length of a string
uppercase_name = name.upper()   # Uppercase
lowercase_name = name.lower()   # Lowercase

print(greeting)
print(length)
print(uppercase_name)
print(lowercase_name)
```

    Hello, Alice
    5
    ALICE
    alice
    

## 4- Lists
*  list is a commonly used data structure that allows you to store and manage a collection of items. Lists are ordered, mutable, and can contain elements of different data types. You can access and manipulate the elements in a list using indexing

* fruits = ["apple", "banana", "cherry"]

* Characteristics of Lists:
  * Ordered: Lists maintain the order of elements. The order in which you add elements is the order in which they are stored in the list.

  * Mutable: Lists are mutable, meaning you can change, add, or remove elements from them after they are created.

  * Heterogeneous: Lists can contain elements of different data types, including strings, numbers, other lists, and more.







```python
# Lists
fruits = ["apple", "banana", "cherry"]
print(fruits)

fruits.append("orange")        # Add an item to the end
print("after append", fruits)
```

    ['apple', 'banana', 'cherry']
    after append ['apple', 'banana', 'cherry', 'orange']
    

* Indexing is the process of accessing individual elements within a list by their position or index. In Python, lists are zero-based, which means the first element is at index 0, the second element is at index 1, and so on. You can use square brackets [] to access elements by their index and can also use negative indexing to access elements from the end of the list.
  * fruits[0] will give you "apple."
fruits[1] will give you "banana."

  * fruits[-1] gives you the last element, "cherry."

   fruits[-2] gives you the second-to-last element, "banana."


lst = ['apple', 'banana', 'cherry']

         0          1        2         
        -3         -2       -1


can access apple lst[0] or lst[-3] and so on


```python
fruits[1] = "kiwi"              # Modify an item
print(fruits)

print(fruits[0])
print(fruits[-1])

fruits.remove("cherry")        # Remove an item
num_fruits = len(fruits)       # Length of a list : to get length of list


print(fruits)
print(num_fruits)
```

    ['apple', 'kiwi', 'cherry', 'orange']
    apple
    orange
    ['apple', 'kiwi', 'orange']
    3
    

* Slicing can also access a range of elements within a list using slicing. Slicing is done by specifying a start index, an end index, and an optional step

  * fruits = ["apple", "banana", "cherry", "date", "fig"]

  * Get elements from index 1 (inclusive) to 4 (exclusive)
  selected_fruits = fruits[1:4]
 selected_fruits will be ["banana", "cherry", "date"]


```python
fruits = ["apple", "banana", "cherry", "date", "fig"]

# Get elements from index 1 (inclusive) to 4 (exclusive)
selected_fruits = fruits[1:4]

# Get every second element
every_second_fruit = fruits[::2]


print(selected_fruits)
print(every_second_fruit)
```

    ['banana', 'cherry', 'date']
    ['apple', 'cherry', 'fig']
    

## 5- Tuples
* A tuple is an ordered, immutable collection of elements. Tuples are defined using parentheses () and can also contain items of various data types. Once you create a tuple, you cannot change its elements.



```python
point = (3, 5)
x, y = point  # Unpacking a tuple
print(x)
print(y)
```

    3
    5
    

## 6- Dictionaries
A dictionary is an unordered collection of key-value pairs. Dictionaries are defined using curly braces {} and consist of keys and their associated values. Keys must be unique, and they are used to access the corresponding values.


```python
person = {"name": "Alice", "age": 30, "is_student": True}
print(person)

name = person["name"]  # Access a value by key
print(name)


person["height"] = 5.8  # Add a new key-value pair
print(person)

```

    {'name': 'Alice', 'age': 30, 'is_student': True}
    Alice
    {'name': 'Alice', 'age': 30, 'is_student': True, 'height': 5.8}
    

## 7- Sets

A set is an unordered collection of unique elements. Sets are defined using curly braces {} or the set() constructor. They do not allow duplicate values and are commonly used for performing mathematical set operations.


```python
fruits = {"apple", "banana", "cherry"}
print(fruits )

fruits.add("date")  # Add an element to the set
print(fruits)

fruits.remove("banana")  # Remove an element
print(fruits)  # Output: {'cherry', 'date', 'apple'}


fruits.add("apple")  # will not add apple again
print(fruits)
```

    {'cherry', 'apple', 'banana'}
    {'cherry', 'apple', 'banana', 'date'}
    {'cherry', 'apple', 'date'}
    {'cherry', 'apple', 'date'}
    

###  Differences between lists, tuples, dictionaries, and sets



#### 1- Lists:

Ordered: Lists maintain the order of elements, and you can access elements by index.
Mutable: You can add, remove, or modify elements in a list.
Syntax: Defined using square brackets [].


#### 2- Tuples:

Ordered: Like lists, tuples also maintain the order of elements, and you can access elements by index.
Immutable: Once created, tuples cannot be modified, which means you can't add, remove, or change elements.
Syntax: Defined using parentheses ().


#### 3- Dictionaries:

Unordered: Dictionaries do not have a specific order for their elements. Instead, they use keys to access values.
Key-Value Pairs: Dictionaries consist of key-value pairs, where each key is unique and associated with a value.
Syntax: Defined using curly braces {} with key-value pairs separated by colons (key: value).


#### 4- Sets:

Unordered: Sets are unordered collections of unique elements. The order of elements is not guaranteed.
Unique Values: Sets do not allow duplicate elements. If you add a duplicate, it will be ignored.
Syntax: Defined using curly braces {} or the set() constructor.

## 8- Control Structures : Conditional Statements (if, elif, else)

* allow you to execute different code blocks based on whether a certain condition is true or false

  * if: It tests a condition and, if true, executes the code inside the block.
  * elif (optional): You can have multiple elif clauses to check additional conditions.
  * else (optional): If none of the conditions in the if and elif blocks are true, the code in the else block is executed.


```python
# Control Structures
age = 20 # change value of age will change the printed text

if age >= 18:
    print("You are an adult")
elif age >= 13:
    print("You are a teenager")
else:
    print("You are a child")



```

    You are an adult
    


```python
grade = 85

if grade >= 90:
    print("A")
elif grade >= 80:
    print("B")
elif grade >= 70:
    print("C")
else:
    print("D")

```

    B
    

- Nested if Statements

  - can also nest if statements inside other if or elif blocks to create more intricate conditional logic


```python
age = 20
is_student = True

if age >= 18:
    if is_student:
        print("You are an adult student")
    else:
        print("You are an adult non-student")
else:
    print("You are a child")

```

    You are an adult student
    

## 9- Control Structures : Loops
repeating a block of code multiple times

for variable in iterable:
    
    Code to execute for each item in the iterable

  - variable is a variable that takes on the value of each item in the iterable during each iteration.
  - iterable is a sequence of items (e.g., a list, string, or range) over which the loop iterates.


```python
# for loop iterates over the fruits list and prints each fruit.

fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

    apple
    banana
    cherry
    

- range


```python
# loop uses the range function to generate numbers from 0 to 4, and it prints each number.
for i in range(5):
    print(i)


```

    0
    1
    2
    3
    4
    

- while


```python
# while loop repeats a block of code as long as a specified condition is True

count = 0
while count < 5:
    print(count)
    count += 1     # increment value of count by 1 each iteration in loop

```

    0
    1
    2
    3
    4
    

- break


```python
# break statement is used to exit a loop prematurely, regardless of whether the loop's condition is satisfied.

for number in range(10):
    if number == 5:
        break
    print(number)

#   loop prints numbers from 0 to 4 and then exits when number becomes 5

```

    0
    1
    2
    3
    4
    

- continue


```python
# continue statement is used to skip the rest of the current iteration and move to the next iteration of the loop

for number in range(6):
    if number == 3:
        continue
    print(number)

# This loop prints numbers from 0 to 5 but skips printing 3.
```

    0
    1
    2
    4
    5
    

#### Nested Loop
- loops inside other loops, creating nested loops. This is useful for handling complex scenarios where you need to iterate over multiple sequences or grids.


```python
for i in range(3):
    for j in range(2):
        print(f"({i}, {j})")

```

    (0, 0)
    (0, 1)
    (1, 0)
    (1, 1)
    (2, 0)
    (2, 1)
    

## 10- Function
- Functions  are blocks of reusable code that perform specific tasks or operations. They allow you to organize and modularize your code, making it more readable, maintainable, and efficient
- functions are defined using the def keyword, followed by the function name, parameters, and a code block




```
def function_name(parameter1, parameter2, ...):
    # Code to perform a specific task
    return result

```

    - function_name: The name of the function.
    - parameters: Input values or arguments that the function accepts.
    - code block: The sequence of statements that define what the function does.
    - return: An optional statement used to specify the value that the function should return when it's called.




```python
def greet(person):
    return "Hello, " + person

message = greet("Bob")
print(message)
```

    Hello, Bob
    


```python
def add_numbers(a, b):
    result = a + b
    return result

sum_result = add_numbers(3, 5)
print(sum_result)

```

    8
    

#### Function with Default Parameters


```python
def greet(name, greeting="Hello"):
    message = f"{greeting}, {name}!"
    return message

print(greet("Alice"))  # Output: "Hello, Alice!"
print(greet("Bob", "Hi"))  # Output: "Hi, Bob!"

```

    Hello, Alice!
    Hi, Bob!
    

#### Function with Multiple Return Values


```python
def get_name_and_age():
    name = "Alice"
    age = 30
    return name, age

result = get_name_and_age()
print(result)  # Output: ("Alice", 30)
name, age = get_name_and_age()
print(name, age)  # Output: "Alice 30"

# get_name_and_age function returns two values, which can be unpacked into separate variables when calling the function.

```

    ('Alice', 30)
    Alice 30
    

## 11- File Operations

* Read from file

read the content of the file






```python
# File Operations
file = open("example.txt", "r")  # Open file for reading
content = file.read()            # Read the entire file
file.close()
print(content)
```

    Line 1
    Line 2
    Line 3
    

* write to file
To write to a text file, you can use the open() function
   - to open the file in write mode ('w')  "replace any text in file : delete old text and write the given text"
   - or append mode ('a'). "append after the old text"


```python
# Open the file in write mode
with open("output.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a second line.\n")
    file.close()

```


```python
# want to add content to an existing file without overwriting its contents, you can open the file in append mode ('a')
with open("output.txt", "a") as file:
    file.write("append another line")

```


```python

```

# Assignment 06:-

### Functions

### 1. Write a function named add_numbers that takes two parameters and returns their sum.


```python
def add_numbers(k,i):
    a = k+i
    return a
sum = add_numbers(1,2)
print("Sum of add_numbers is:", sum)
    
```

    Sum of add_numbers is: 3
    

### 2. Define a function calculate_area to compute the area of a rectangle given its length and width.


```python
def calculate_area(length,width):
    area = length*width
    return area
computed = calculate_area(6,9)
print("Computed area of rectangle is:", computed)
```

    Computed area of rectangle is: 54
    

### 3. Add a docstring to the calculate_area function explaining its purpose.


```python
def calculated_area(length):
     """
     It is the area which is calculated by specific formula of rectange shape.
     It has 2 parameters
     """
    area = length*2
    return area
print(calculated_area)
```


      File <tokenize>:6
        area = length*2
        ^
    IndentationError: unindent does not match any outer indentation level
    


### 4. Create a function print_greeting that takes a name as an argument and prints a personalized greeting.


```python
def print_greeting(name):
    greeting = "Hello! This is Kinza Ishaq greeting you warmly"
    print(greeting)
print_greeting("KINZA")
```

    Hello! This is Kinza Ishaq greeting you warmly
    

### 5. Write a function is_prime that checks if a given number is prime.


```python
def is_prime(number):
    if number<2:
        return False
    for i in range(2, int(number**0.5) + 1):
        if number % i == 0:
            return False
    return True
result = is_prime(19)
print(result)
```

    True
    

### 6. Implement a function factorial to calculate the factorial of a given number.


```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n-1)

number = 9
result = factorial(number)
print("The factorial of 9 is", result)


```

    The factorial of 9 is 362880
    

### 7. Create a function print_pattern to print a specific pattern of stars.


```python
def print_pattern(rows):
    for i in range(1, rows + 1):
        for j in range(1, i + 1):
            print("*", end=" ")
        print()
print_pattern(5)

```

    * 
    * * 
    * * * 
    * * * * 
    * * * * * 
    

### 8. Write a function multiply_numbers with default values for its parameters.


```python
def multiply_numbers(k=1, i=1):
    return k * i
default = multiply_numbers()  
values = multiply_numbers(5, 3)  

print("Default Multiply is", default)
print("Values multiply is", values)

```

    Default Multiply is 1
    Values multiply is 15
    

### 9. Define a function print_info that takes a variable number of arguments and prints them.


```python
def print_info(*args):
    for arg in args:
        print(arg)
print_info("Name: Kinza", "Age: 24")


```

    Name: Kinza
    Age: 24
    

### 10. Create a function power_of_two that accepts a number and returns its square.


```python
def power_of_two(number):
    return number ** 2
result = power_of_two(5)
print("The square of 5 is", result)

```

    The square of 5 is 25
    

### 11. Define a variable inside a function and try to access it outside the function.


```python
def new_function():
    local_variable = "I am inside the function"
new_function()
try:
    print(local_variable)
except NameError as e:
    print(f"Error: {e}")

```

    Error: name 'local_variable' is not defined
    


```python
global_variable = None 
def set_global_variable():
    global global_variable
    global_variable = "I am inside the function"
set_global_variable()
print(global_variable)

```

    I am inside the function
    

### 12. Write a function that uses a variable from the enclosing scope.


```python
def outer_function():
    outer_variable = "I am from the outer function"

    def inner_function():
        print("Inside inner function:", outer_variable)

    # Call the nested function
    inner_function()

# Call the outer function
outer_function()

```

    Inside inner function: I am from the outer function
    

### 13. Create a global variable and modify it inside a function.


```python
global_variable = 10
def modify_global_variable():
    global global_variable
    global_variable += 5
print("Before:", global_variable)
modify_global_variable()
print("After:", global_variable)

```

    Before: 10
    After: 15
    

### 14. Write a lambda function to calculate the cube of a number.


```python
cube = lambda x: x**3
result = cube(4)
print("The cube of 4 is", result)

```

    The cube of 4 is 64
    

### 15. Use a lambda function as an argument with the map function.


```python
numbers = [1, 2, 3, 4, 5]
cubes = list(map(lambda x: x**3, numbers))
print("Original numbers:", numbers)
print("Cubes of numbers:", cubes)

```

    Original numbers: [1, 2, 3, 4, 5]
    Cubes of numbers: [1, 8, 27, 64, 125]
    

### 16. Use a lambda function with the filter function to filter even numbers from a list.


```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print("Original numbers:", numbers)
print("Even numbers:", even_numbers)

```

    Original numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    Even numbers: [2, 4, 6, 8, 10]
    

### 17. Apply a lambda function with the reduce function to find the product of a list.


```python
from functools import reduce
numbers = [1, 2, 3, 4, 5]
product = reduce(lambda x, y: x * y, numbers)
print("Original numbers:", numbers)
print("Product of numbers:", product)

```

    Original numbers: [1, 2, 3, 4, 5]
    Product of numbers: 120
    

### 18. Sort a list of tuples based on the second element using a lambda function.


```python
tuple_list = [(1, 5), (3, 2), (7, 8), (2, 4), (5, 1)]
sorted_list = sorted(tuple_list, key=lambda x: x[1])
print("Original list:", tuple_list)
print("Sorted list based on the second element:", sorted_list)

```

    Original list: [(1, 5), (3, 2), (7, 8), (2, 4), (5, 1)]
    Sorted list based on the second element: [(5, 1), (3, 2), (2, 4), (1, 5), (7, 8)]
    

### 19. Demonstrate the use of the zip function with two lists.


```python
names = ['Kinza', 'Eman', 'Fateeha']
ages = [24, 22, 23]
zipped_data = zip(names, ages)
zipped_list = list(zipped_data)

print("Original lists:")
print("Names:", names)
print("Ages:", ages)
print("\nCombined using zip:")
print("Zipped list:", zipped_list)

```

    Original lists:
    Names: ['Kinza', 'Eman', 'Fateeha']
    Ages: [24, 22, 23]
    
    Combined using zip:
    Zipped list: [('Kinza', 24), ('Eman', 22), ('Fateeha', 23)]
    

### 20. Implement a generator function that generates Fibonacci numbers.


```python
def fibonacci_generator():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b
fibonacci = fibonacci_generator()
for _ in range(10):
    print(next(fibonacci))

```

    0
    1
    1
    2
    3
    5
    8
    13
    21
    34
    

### 21. Use a generator expression to create a sequence of squares.


```python
squares = (x**2 for x in range(1, 6))
print("Sequence of squares:", list(squares))

```

    Sequence of squares: [1, 4, 9, 16, 25]
    

### 22. Write a function that uses the yield statement to produce a generator.


```python
def square_generator(n):
    for i in range(1, n + 1):
        yield i**2
squares = square_generator(5)
for square in squares:
    print(square)

```

    1
    4
    9
    16
    25
    

### 23. Explain the difference between iterators and generators in Python.

### Iterator: 
An iterator is an object that implements the __iter__() and __next__() methods. The __iter__() method returns the iterator object itself, and the __next__() method returns the next value from the iterator. Iterators can be manually created by implementing these methods.

### Generator: 
A generator is a special type of iterator created using a function with the yield statement. The yield statement allows a function to produce a series of values over multiple calls without losing its state. Generators are more concise and convenient than manually implementing iterators.

### 24. Write a Python program that includes a nested function. Inside the nested function, access a variable from the enclosing function's scope, and explain how the scope resolution works in this case.


```python
def outer_function():
    outer_variable = "I am from the outer function"

    def nested_function():
        print("Inside nested function:", outer_variable)
    nested_function()
outer_function()

```

    Inside nested function: I am from the outer function
    

### 25. Create a list of strings containing both uppercase and lowercase words. Use a lambda function with the sorted() function to sort the list in a case-insensitive manner.


```python
word_list = ["Apple", "banana", "Orange", "grape", "Cherry"]
sorted_words = sorted(word_list, key=lambda x: x.lower())
print("Original list:", word_list)
print("Sorted list (case-insensitive):", sorted_words)

```

    Original list: ['Apple', 'banana', 'Orange', 'grape', 'Cherry']
    Sorted list (case-insensitive): ['Apple', 'banana', 'Cherry', 'grape', 'Orange']
    

### 26. Implement a generator function that yields prime numbers indefinitely. Use this generator to print the first 10 prime numbers.


```python
def is_prime(num):
    """Check if a number is prime."""
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

def prime_generator():
    """Generate prime numbers indefinitely."""
    num = 2
    while True:
        if is_prime(num):
            yield num
        num += 1
primes = prime_generator()
for _ in range(10):
    print(next(primes))

```

    2
    3
    5
    7
    11
    13
    17
    19
    23
    29
    

### 27. Write a decorator function that measures the execution time of another function. Apply this decorator to a function of your choice and print the execution time.


```python
import time

def execution_time_decorator(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        elapsed_time = end_time - start_time
        print(f"Execution time for {func.__name__}: {elapsed_time:.6f} seconds")
        return result
    return wrapper
def sample_function():
    time.sleep(2)
    print("Function executed!")
sample_function()

```

    Function executed!
    


```python

```

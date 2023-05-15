# Class-07
Reading Questions:

1-Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.
```
In Python, variable scope refers to the portion of the code where a variable is accessible and can be referenced. The scope determines the visibility and lifetime of a variable within a program.

Local Scopes are a variables defined within a function have local scope, meaning they are only accessible within that specific function.

Ex: 
```
```py
def my_function():
    x = 10  # Local variable
    print(x)

my_function()  # Output: 10

print(x)  # NameError: name 'x' is not defined
```

Global Scopes are variables defined outside of any function or block have global scope, meaning they can be accessed from anywhere within the program.

Ex:
```py
# Global variable
x = 10

def my_function():
    print(x)

my_function()  # Output: 10

x = 20

def another_function():
    print(x)

another_function()  # Output: 20
```




2-How do the global and nonlocal keywords work in Python, and in what situations might you use them?
```
In Python, the global and nonlocal keywords are used to access variables that are outside the current scope of a function.

global keyword:

When you use the global keyword inside a function, it allows you to modify or assign a value to a variable that is in the global scope (outside any function).
```

Ex:
```py
x = 10  # Global variable

def my_function():
    global x 
    x = 20 
    print(x)

my_function()  # Output: 20

# The global variable has been modified outside the function
print(x)  # Output: 20
```

nonlocal keyword:

The nonlocal keyword is used to access variables from the immediate outer scope, specifically in nested functions.

Ex:
```py
def outer_function():
    x = 10  # Outer variable

    def inner_function():
        nonlocal x  # Indicate that we want to use the variable from the outer scope
        x = 20  
        print(x)

    inner_function()  # Output: 20

    # The variable has been modified in the inner function
    print(x)  # Output: 20

outer_function()
```




3-In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.
```
The purpose of Big O notation in algorithm analysis is to quantify the worst-case time complexity or space complexity of an algorithm. It allows us to understand how the algorithm's runtime or memory usage grows as the input size increases. By analyzing the Big O complexity of different algorithms, we can make informed decisions about which algorithm to choose for a specific problem based on its efficiency.

```


4-Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.
```
To simulate a dice roll using Python, you can make use of the random module, which provides functions for generating random numbers. 
```
Ex:

import random
```py
def roll_dice():
    return random.randint(1, 6)  # Generate a random integer between 1 and 6 inclusive

# Simulating a dice roll
result = roll_dice()
print("Dice roll result:", result)
```

to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials. To do this, you would perform multiple dice rolls and count the number of times the specific number (6 in this case) appears. The probability can be calculated by dividing the count of successful outcomes by the total number of trials.

Ex:
```py
import random

def roll_dice():
    return random.randint(1, 6)

def calculate_probability(target_number, num_trials):
    count = 0

    for _ in range(num_trials):
        if roll_dice() == target_number:
            count += 1

    probability = count / num_trials
    return probability

target_number = 6
num_trials = 100000  # Number of dice rolls to perform

probability = calculate_probability(target_number, num_trials)
print(f"Probability of rolling a {target_number}: {probability}")
```

By adjusting the value of num_trials, you can simulate a larger or smaller number of dice rolls to get a more accurate probability estimate.




## sources:
```
https://realpython.com/python-scope-legb-rule/

 https://www.youtube.com/watch?v=dNorFNlDbX0
```


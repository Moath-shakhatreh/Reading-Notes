## Classes, Objects and Recursive

Classes and objects are important because we used them to decompose a large system into real-world abstractions that can form the basis for analysis and design.


## Reading Questions

1-What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?

In Python, a class is a blueprint for creating objects, while an object is an instance of a class. The key differences between classes and objects lie in their behavior and functionality.

classes and objects are essential concepts in Python's object-oriented programming paradigm. Classes define the attributes and methods that objects of that class can have, while objects are specific instances of a class that inherit those attributes and methods. You can create instances of a class using the constructor method, and you can access and modify the attributes and methods of an object using the dot notation.


2-Explain the concept of recursion and provide an example of how it can be used to solve a problem in Python. What are some best practices to follow when implementing a recursive function?

Recursion is a programming technique that involves a function calling itself to solve a problem. The process continues until a base case is reached, where the function does not call itself again, and the solution is obtained by combining the results of the previous calls.

A common example of a recursive function is the factorial function. The factorial of a non-negative integer n, denoted by n!, is the product of all positive integers less than or equal to n. For example, 5! = 5 x 4 x 3 x 2 x 1 = 120.

Here's an example implementation of the factorial function using recursion in Python:

def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)


Some best practices to follow when implementing a recursive function include:

Ensuring that the function has a base case to terminate the recursion.
Ensuring that the function moves towards the base case in each recursive call, such that it eventually reaches the base case.
Avoiding infinite recursion by checking that the inputs to the function are valid.





3-What is the purpose of pytest fixtures and code coverage in testing Python code? Explain how they can be used together to improve the quality and maintainability of a project.

Pytest fixtures and code coverage are two important tools in testing Python code. Pytest fixtures provide a way to set up and tear down resources for tests, while code coverage measures how much of the code is being exercised by the tests.

Fixtures are functions that provide a set of preconditions for tests to run. They can be used to create and initialize objects, configure settings, or establish connections to databases, among other things. By using fixtures, tests can be made more modular and reusable, and they can avoid code duplication.

By combining fixtures and code coverage, tests can be made more comprehensive and effective. Fixtures can be used to set up preconditions for specific tests, and code coverage can be used to measure how much of the code is being exercised by those tests. This can help identify areas of the code that are not being tested and can be used to write additional tests to improve the coverage.


## Things I want to know more about:

how to use except for other problems

## Sources :

https://www.learnpython.org/en/Classes_and_Objects
https://www.guru99.com/difference-between-object-and-class.html
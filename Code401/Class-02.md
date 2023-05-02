## Class-02

reading these topics helped me with:

understanding TDD and how it help in the quality of the code ,know more information a bout Recursion,Understanding new topics(Python Modules and Packages) and finally knowing the benefites of using ( if __name__ == '__main__': )statement.

### Reading Questions

1-What are the key principles of Test-Driven Development (TDD) in Python, and how do they contribute to the overall quality of code?

Test Driven Development (TDD) is software development approach in which test cases are developed to specify and validate what the code will do. In simple terms, test cases for each functionality are created and tested first and if the test fails then the new code is written in order to pass the test and making code simple and bug-free.


2-Explain the purpose of the if __name__ == '__main__': statement in Python scripts. 
What are some use cases for including this conditional in your code?

A Python programme uses the condition if __name__ == '__main__' to only run the code inside the if statement when the program is run directly by the Python interpreter. The code inside the if statement is not executed when the file's code is imported as a module.


3-Describe the concept of recursion in Python.

A recursive function is a function defined in terms of itself via self-referential expressions. This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result.

4-What is the difference between Python modules and packages?

In simple terms, a module is a single file containing python code, whereas a package is a collection of modules that are organized in a directory hierarchy.

### Explain how to create, import, and use them in your Python programs.


To create a module just save the code you want in a file with the file extension .py

Save this code in a file named mymodule.py

def greeting(name):
  print("Hello, " + name)

Use a Module

Now we can use the module we just created, by using the import statement:

Example
Import the module named mymodule, and call the greeting function:

import mymodule

mymodule.greeting("Jonathan")
## FileIO & Exceptions

Reading these topics helped me knowing how to deal with python files (reading, writing ,opening ,closing and doing some tricks with the files) , knowing that are there two types of errors (syntax and an exception ) and how they are differ , raising exceptions ,making assertions and demonstration of the try and except block.

## Reading Questions


1-What is the purpose of the ‘with’ statement when opening a file in Python, and how does it help manage resources while reading and writing files?

 shorthand. More significantly, it ensures that resources are closed immediately after processing. Reading or writing to a file is a common use of the with statement. A context manager is a function or class that supports the with statement.


2-Explain the difference between the ‘read()’ and ‘readline()’ methods for file objects in Python. Provide examples of when to use each method.

The read() and readline() methods are both used to read data from a file object in Python. However, they have different behaviors and are useful in different situations.

The read() method reads the entire contents of a file object and returns them as a string. It takes an optional argument that specifies the maximum number of bytes to read. If no argument is provided, it will read the entire file. For example:

with open('file.txt', 'r') as f:
    data = f.read()


In this example, the read() method is used to read the entire contents of the file.txt file and store them in the data variable.

On the other hand, the readline() method reads a single line from a file object and returns it as a string. It reads up to and including the newline character (\n) at the end of the line. If the end of the file is reached and there are no more lines to read, it will return an empty string (''). For example:

with open('file.txt', 'r') as f:

line = f.readline()

In this example, the readline() method is used to read the first line of the file.txt file and store it in the line variable.


3-Briefly describe the concept of exception handling in Python. How can the ‘try’, ‘except’, and ‘finally’ blocks be used to handle exceptions and ensure proper execution of code? Provide a simple example.

Exception handling is a mechanism in Python that allows the detection and resolution of errors or exceptional situations that may occur during the execution of a program. When an exception is raised, the program stops its normal flow and looks for a handler that can catch the exception and perform some actions based on it.

In Python, exception handling is achieved using the try, except, and finally blocks. The try block is used to enclose the code that may raise an exception. The except block is used to handle the exception that is raised by the try block. The finally block is used to execute some code that should always be executed, regardless of whether an exception was raised or not.

Here is an example of how to use these blocks to handle exceptions in Python:

try:
    x = int(input("Enter a number: "))
    y = int(input("Enter another number: "))
    result = x / y
    print(f"The result is {result}")
except ValueError:
    print("Invalid input. Please enter a number.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
finally:
    print("Program executed successfully.")


## Things I want to know more about:

Is Exception handling can be used for every error 

## Sources :


https://www.tutorialspoint.com/what-is-the-use-of-the-with-statement-in-python

https://realpython.com/python-exceptions/
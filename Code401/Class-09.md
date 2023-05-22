# Clas-09


>1-What is the purpose of dunder methods in Python? Provide an example of a commonly used dunder method.
```
In Python, "dunder" stands for "double underscore," and dunder methods (also called magic methods or special methods) are predefined methods with a specific naming convention that allows you to define how objects of a class behave in various contexts. These methods are surrounded by double underscores on both sides of their names.

Dunder methods are used to provide functionality for operator overloading, object representation, attribute access, and more. They allow you to customize the behavior of your objects, making them act like built-in types or respond to specific operations

One commonly used dunder method is __str__. It is used to define a string representation of an object and is automatically called when you use the built-in str() function or the print() function on an object. It should return a human-readable string that represents the object's state.

Ex:

class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __str__(self):
        return f"Point({self.x}, {self.y})"

point = Point(3, 5)
print(point)  # Output: Point(3, 5)
```




>2-In the video “AI Guru makes $238,800 with misleading paid course,” what was the main ethical issue raised concerning the use of developers’ work, and how might this have been avoided?
```
the main ethical issue was that the course wasn't as expected to be and plagiarism or unauthorized use of developers' work without proper attribution or compensation.

we can avoid this by checking if the developers respect the intellectual property rights of others and not use their work without proper authorization or permission before taking any courses.
```




> 3-Describe the Python statistics module and give an example of a function within the module that can be used to perform a common statistical operation
```
statistics module is a built-in module that provides functions for statistical operations. It offers a set of functions to calculate various statistical measures such as mean, median, mode, standard deviation, variance, and more. These functions operate on sequences of numeric data.

Ex:

import statistics

data = [4, 6, 2, 8, 5, 2, 8, 9, 3, 5]

mean_value = statistics.mean(data)
print(mean_value)  # Output: 5.2
```




 



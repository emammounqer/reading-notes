# Class 09

## What is the purpose of dunder methods in Python? Provide an example of a commonly used dunder method

Dunder methods are special methods in Python that have two underscores before and after their name. They are also known as magic methods. Dunder methods let you emulate the behavior of built-in types.

commonly used dunder method is :

- __init__ method, which is used to initialize a newly created object.
- __str__ method, which is used to return a string representation of an object.
- __repr__ method, which is used to return a printable representation of an object.
- __len__ method, which is used to return the length of a sequence.

```python
class StrSupport:
    def __str__(self):
        return "this class support str method"

obj = str(StrSupport()) #output: this class support str method
```

## In the video “AI Guru makes $238,800 with misleading paid course,” what was the main ethical issue raised concerning the use of developers’ work, and how might this have been avoided?

The main ethical issue raised concerning the use of developers’ work is that the developer's work was used without his permission and without giving him credit. This could have been avoided by giving the developer credit for his work and asking for his permission to use it.

## Describe the Python statistics module and give an example of a function within the module that can be used to perform a common statistical operation

The Python statistics module provides functions to perform mathematical statistics on numeric data. It is available in Python 3.4 and above. The statistics module provides functions to calculate mathematical statistics of numeric data. It has functions for calculating the mean, median, mode, standard deviation, variance, and other statistical quantities.

```python
import statistics

data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

print(statistics.mean(data)) #output: 5.5
print(statistics.median(data)) #output: 5.5
print(statistics.mode(data)) #output: 1
print(statistics.stdev(data)) #output: 3.0276503540974917
print(statistics.variance(data)) #output: 9.166666666666666
```

# Class 04

## What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?

Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. ***Classes** are essentially a template to create your objects*.

## Explain the concept of recursion and provide an example of how it can be used to solve a problem in Python. What are some best practices to follow when implementing a recursive function?

A recursive function is a function defined in terms of itself via self-referential expressions. This means that the function will continue to call itself until some condition is met to return a result.

example:

```python
def factorial(n):
    if n == 1:
        return 1
    else:
        return n * factorial(n-1)
```

Each recursive call has its own execution context, so to maintain state during recursion you have to either:

- Thread the state through each recursive call so that the current state is part of the current call’s execution context
- Keep the state in global scope

some best practices:

- function have a base case
- function change his state and move toward the base case when calling itself
- if we unnecessarily recomputing values. try to improve the function by caching the results
- Keep stack overflow limitation in mind if you have a program that requires deep recursion.

## What is the purpose of pytest fixtures and code coverage in testing Python code? Explain how they can be used together to improve the quality and maintainability of a project

fixtures are functions, which will run some code before each test ,You'll want to have some objects available to all of your tests. Those objects might contain data you want to share across tests, or they might involve the network or filesystem.

In pytest, you define fixtures using a combination of the pytest.fixture decorator, along with a function definition.

```python
@pytest.fixture
def some_data():
    return 42
```

At the same time, fixtures are used differently from global variables. For example, let's say you want to include this fixture in one of your tests. You then can mention it in the test's parameter list.

```python
def test_some_data(some_data):
    assert some_data == 42
```

coverage measures the amount of testing performed by a set of test. It will include gathering information about which parts of a program are executed when running the test suite to determine which branches of conditional statements have been taken.

100% code coverage doesn't mean that your code is perfect or that it lacks bugs. But it does give you a greater degree of confidence in the code and the fact that it has been run at least once.

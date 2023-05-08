# Class 12 - Pandas

## Explain the purpose and basic functionality of the Pandas library. What are some common operations that can be performed on data using Pandas, and how do they contribute to data analysis and manipulation?

panda is a library that is used for data analysis and manipulation, it is used to read data from different sources, and to manipulate it, and to analyze it, it is used to read data from csv files, excel files, json files, and many other sources.

Common operations:

- Stats - mean, median, mode, standard deviation, variance, etc.
- Apply : DataFrame.apply() applies a user defined function to the data.
- Histogramming : creates a histogram to visualize the frequency distribution of numerical data. It is done using the hist() method on a DataFrame or Series. It helps in understanding the data distribution and is useful in data analysis and exploratory data analysis.
- String Methods : Series is equipped with a set of string processing methods in the str attribute that make it easy to operate on each element of the array

## What are the primary data structures in Pandas, and how do they differ in terms of use cases?

Pandas is a popular data analysis library in Python that provides a rich set of data structures for working with structured data. The primary data structures in Pandas are:

- Series: is a one-dimensional array-like object containing a sequence of values and an associated array of data labels, called its index.
- DataFrame: is a 2-dimensional labeled data structure with columns of potentially different types. You can think of it like a spreadsheet or SQL table, or a dict of Series objects.

## Describe the process of loading a dataset into a Pandas DataFrame. What are some common file formats that can be used, and which Pandas functions are utilized to read these formats?

To load a dataset into a Pandas DataFrame, it depends on the file format. For example, to load a CSV file, we use the `read_csv()` function and to load an Excel file, we use the `read_excel()` function, etc. these This function takes in a file path file as input and returns a pandas.DataFrame object.

Some common file formats that can be used to load data into a Pandas DataFrame are:

- CSV: Comma-separated values file format, used for storing tabular data.
- Excel: Microsoft Excel file format, used for storing tabular data.
- SQL databases: Used for storing and retrieving data in a relational database.
- JSON: JavaScript Object Notation, used for storing and exchanging data.
- HTML: Hypertext Markup Language, used for creating web pages.

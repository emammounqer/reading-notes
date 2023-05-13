# Class 13 - Linear Regressions

## Can you explain the basic concept of linear regression and its purpose in the context of machine learning and data analysis?

Regression searches for relationships among variables. For example, you can observe several employees of some company and try to understand how their salaries depend on their features, such as experience, education level, role, city of employment, and so on.

This is a regression problem where data related to each employee represents one observation. The presumption is that the experience, education, role, and city are the independent features, while the salary depends on them.

Linear regression can be thought of as finding the straight line that best fits a set of scattered data points:

![Linear Regression](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Linear_regression.svg/1200px-Linear_regression.svg.png)

## Describe the process of implementing a linear regression model using Python’s Scikit Learn library, including the necessary steps and functions

The process of implementing a linear regression model using Python’s Scikit Learn library is as follows:

1. Import the required libraries.

    ```python
    from sklearn.linear_model import LinearRegression
    sklearn.linear_model.LinearRegression()
    ```

2. Create a numpy array of data

    ```python
    x = np.array([6, 16, 26, 36, 46, 56]).reshape((-1, 1))
    y = np.array([4, 23, 10, 12, 22, 35])
    ```

3. Create a linear regression model.

    ```python
    model = LinearRegression().fit(x, y)
    ```

4. Obtain the coefficient of determination by calling the model with the score() function, then print the coefficientز

    ```python
    r_sq = model.score(x, y)
    print('coefficient of determination:', r_sq)
    ```

5. Print the Intercept and the Slope

    ```python
    print('intercept:', model.intercept_)
    print('slope:', model.coef_)
    ```

6. Predict a Response and print it:

    ```python
    y_pred = model.predict(x)
    print('predicted response:', y_pred, sep='\n')
    ```

## What is the purpose of splitting the dataset into train and test sets, and how does this contribute to the evaluation of a machine learning model’s performance?

The purpose of splitting the dataset into train and test sets is to evaluate the performance of the model on unseen data. The model is trained on the training set and then evaluated on the test set. This helps us to understand how well the model generalizes to unseen data.

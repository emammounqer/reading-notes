# Class 14 : Data Visualization

## What are the key differences between Matplotlib, Seaborn, and Bokeh libraries in terms of their features and use cases? Provide an example of a specific visualization that is more suitable for each library

| Library    | Features                                    | Use Cases                                                                 | Example Visualization                                      |
|------------|---------------------------------------------|---------------------------------------------------------------------------|------------------------------------------------------------|
| Matplotlib | Low-level interface, detailed customization | Static and interactive visualizations, wide range of plot types           | Line plot showing a variable's trend over time             |
| Seaborn    | High-level interface, predefined themes     | Statistical data visualization, exploring relationships between variables | Scatter plot showing the correlation between two variables |
| Bokeh      | Interactive, web-based visualizations       | Data exploration, interactive dashboards and web applications             | Interactive bar chart with filtering and tooltips          |

Matplotlib: line plot showing a variable's trend over time
Seaborn: scatter plot showing the correlation between two variables
Bokeh: interactive bar chart with filtering and tooltips

## In the Seaborn library, what are the main functions to create relational, categorical, and distribution plots? Briefly explain the purpose of each type of plot and provide an example use case

Relational plots: `scatterplot()`, `lineplot()`, `relplot()`
purpose: show the relationship between two variables
example use case: scatter plot showing the correlation between two variables

Categorical plots: `catplot()`, `boxplot()`, `violinplot()`
purpose: show the distribution of a variable within categories
example use case: box plot showing the distribution of a variable within categories

Distribution plots: `histplot()`, `kdeplot()`, `displot()`
purpose: show the distribution of a variable
example use case: histogram showing the distribution of a variable

## Discuss the role of the Seaborn Cheat Sheet in a Python developer’s workflow. What are some key sections or elements featured in the cheat sheet that can help a developer quickly reference Seaborn functionalities?

The Seaborn Cheat Sheet is a quick reference guide for Seaborn's most commonly used functions. It is organized into sections based on the type of plot, and each section contains a brief description of the plot type and a code snippet for creating the plot. The cheat sheet also includes a list of Seaborn's color palettes and a section on customizing plots.

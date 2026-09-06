# ECE-2112-PA-3

**Made by: Alijah B. Lazaga | 2ECE-B**

The content of this repository contains the Programming Assignment 3 for "Advanced Computer Programming" this S.Y. 2026-2027.

Note: Before coding, put 'import pandas as pd` in order to import the PANDAS library and rename it to pd. This way, pd will act as an acronym, shortening it so that we don't have to code pandas before every function. We also have to import a .csv file that was uploaded in canvas by your professor. We can use `pd.read_csv()` to read the file and rename it to `cars`.

# **A. Positional and Label-Based Slicing**

**a. Display the shape and complete list of column names cars.**

The following functions were used:

• `.columns` - A built-in function that displays the columns of a dataframe.

• `.shape` - A built-in function that checks the number of rows and columns of an array or dataframe.

**b. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where the first data row is row 1.**

The following functions were used:

• `.iloc[5:10]` - A built-in function that select specific rows. We also used a slicing statement inside the bracket in order to remove rows 0 to 5. We used `[5:10]` instead of `[6:11]` because the assignment asks us to use the first data row (0) as row 1. 

We then rename the dataframe to `cars_6_to_10` using `cars_6_to_10 = cars.iloc[5:10]`.

**c. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.**

The following function was used:

• `.loc[:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]` - A built-in function that selects specific columns. We used a colon before the comma to select every row while we indicated only select column names to be displayed after the comma. The structure of the function is like this -> `.iloc[row, column]`.

By combining all of the functions shown above, the final code for this problem is as follows:

```python
cars.column
cars.shape

cars_6_to_10 = cars.iloc[5:10]
cars_6_to_10.loc[:, ['Model', 'mpg', 'cyl', 'hp', 'gear']]
```
Note: You can place the name of the dataframe in the second line after each code to display/print the function.

# **B. Model Lookup**

Use Boolean indexing on the Model column to answer both requests.

**a. Display the complete row for Toyota Corolla.**

The following method was used:

• `toyota = cars[cars['Model'] == 'Toyota Corolla']` - A python statement that uses boolean indexing to locate a row using the Model column.

**b. For Pontiac Firebird, display only Model, mpg, hp, and wt.**

The following method was used:

• `pontiac = cars[cars['Model'] == 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]` - A  python statement that uses boolean indexing to locate a row using the Model column whist selecting only Model, mpg, hp, wt as the columns.

By combining all of the code shown above, the final code for this problem is as follows:

```python
toyota = cars[cars['Model'] ==  'Toyota Corolla']
toyota

pontiac = cars[cars['Model'] == 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]
pontiac
```

# **C. Multi-Model Subsetting**

Create a DataFrame named selected cars containing only the records for three models: Datsun 710, Lotus Europa, and Ferrari Dino. Retain only Model, mpg, cyl, hp, and gear.

The following function and method were used in this problem:

• `cars.loc[(cars['Model'] == "Datsun 710") | (cars['Model'] == "Lotus Europa") | (cars['Model'] == "Ferrari Dino"),['Model', 'mpg', 'cyl', 'hp', 'gear']]` - A built-in function that locates specific rows through a specified column and selects columns that are only indicated which is model, mpg, cyl, hp, and gear. The line of code uses the OR statement `|` to select rows Datsun 710, Lotus Europa, and Ferrari Dino. If we used the AND statement `&`, it will not work because the rows we want are seperate; They will conjoin if we used the AND statement.

• `.shape` - A built-in function that checks the number of rows and columns of a dataframe.

By combining all of the code shown above, the final code for this problem is as follows:

```python
selected_cars = cars.loc[(cars['Model'] == "Datsun 710") | (cars['Model'] == "Lotus Europa") | (cars['Model'] == "Ferrari Dino"),['Model', 'mpg', 'cyl', 'hp', 'gear']]
selected_cars

selected_cars.shape
```

Thank you for reading!!!

To fully see the main python program, please visit the link provided below:
https://github.com/alijahlazaga/ECE-2112-PA-3/blob/935a30f68ad44eabb147d1ba31d3437379175cd7/ProgrammingAssignment3.ipynb

### **README file Version History:**

September 3, 2026 - Initial README content uploaded

September 6, 2026 - Final README content uploaded










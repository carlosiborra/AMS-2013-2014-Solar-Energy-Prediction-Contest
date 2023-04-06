# Práctica 1. Aprendizaje Automático

Grado en Ingeniería Informática, Curso 2022/2023. Universidad Carlos III de Madrid.

## 0. Table of Contents

- [Práctica 1. Aprendizaje Automático](#práctica-1-aprendizaje-automático)
  - [0. Table of Contents](#0-table-of-contents)
  - [1. Authors](#1-authors)
  - [2. Requirements](#2-requirements)
    - [Recommended - Notice](#recommended---notice)
  - [3. Remarks](#3-remarks)
    - [In order to open the conda environment, you must run the following command](#in-order-to-open-the-conda-environment-you-must-run-the-following-command)
  - [4. Resources](#4-resources)

## 1. Authors

- Carlos Iborra Llopis - 100451170
- Alejandra Galán Arrospide - 100451273

## 2. Requirements

- pandas
- numpy
- matplotlib.pyplot
- missingno: needs to be used within the requirements, it can throw errors easily with any other versions of the libraries
- seaborn
- sklearn

### Recommended - Notice

- **Important**, if missigno library is throwing the following error (ValueError: keyword grid_b is not recognized), please change in missigno.py (lib file):<br>
    from grid(b=False) to grid(visible=False). This error is due to the version of matplotlib in the conda environment.
- jinja2=3.0.3
- nbconvert=6.4.4
- We recommend using the **Better Comments** extension for VSCode to see the comments in a more readable way.

## 3. Remarks

### In order to open the conda environment, you must run the following command

```
conda activate "path to the environment"
```

- EDA (Exploratory Data Analysis) is a crucial step in the data science process. It is the process of analyzing the data to summarize their main characteristics, often with visual methods. It is used to see what the data can tell us beyond the formal modeling or hypothesis testing task. Link in resources.
- **We need to focus on the correlation between the target and input variables.** We can use a correlation matrix to see the correlation between the variables. We can also use a heatmap to visualize the correlation matrix. **This will be useful to make the reduction of the dimensionality of the data** (see below PCAs).
- **Reduce the dimensionality of the data using PCA** (Principal Component Analysis) and compare the results with the original data. *Not compulsory*.
- Divide the data of 12 years into training and test sets in the following way (beware of the time series nature of the data):
  - **10 years for training**
  - **2 years for test/validation**
- The folds must respect the time series nature of the data: the first fold must contain the firsts years of the data, and the second fold the last years as if we were doing a real prediction, since otherwise we would be changing the time series nature of the data.
- **DO NOT USE** time_series_split from sklearn which is a cross-validation object that splits the data into training and test sets in a time series manner (i.e. the test set is always larger than the training set). Best to use the predefined_split from sklearn (use a split of the years in training for hyperparameter tuning and the rest for testing).
- **Create graphs** in order to understand the relation between execution time (tranining and test) and the results (accuracy, precision, recall, F1, AUC, etc.).
- Advanced methods: **SVMs** (Support Vector Machines which are a type of linear classifier. They are based on the idea of finding a hyperplane that separates the data into two classes. The hyperplane is chosen in such a way that the distance between the hyperplane and the nearest data points from both the classes is maximized. The data points that are closest to the hyperplane are called support vectors), **Random Forests** (they create a lot of random trees and then combine them to get the mean prediction, when better the tree, better the attributes its composed of. See CARTs, 1996), **Gradient Boosting** (they create a lot of trees and then combine them to get the mean prediction, but they do it in a sequential way, so the next tree is created to correct the errors of the previous tree).

## 4. Resources

- [AMS 2013-2014 Solar Energy Prediction Contest](https://www.kaggle.com/competitions/ams-2014-solar-energy-prediction-contest/data)

- [A Simple Tutorial on Exploratory Data Analysis](https://www.kaggle.com/code/spscientist/a-simple-tutorial-on-exploratory-data-analysis/notebook)

- [Using the missingno Python library to Identify and Visualise Missing Data](https://towardsdatascience.com/using-the-missingno-python-library-to-identify-and-visualise-missing-data-prior-to-machine-learning-34c8c5b5f009)

- [] (<https://aulaglobal.uc3m.es/mod/resource/view.php?id=4378737>)
- [] (<https://aulaglobal.uc3m.es/mod/resource/view.php?id=4378744>)
- [] (https://aulaglobal.uc3m.es/mod/resource/view.php?id=4386772)
- 

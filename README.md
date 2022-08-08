# Software-developer-salary-prediction
Developing a Machine Learning model to predict software developer salaries, then creating a web app to using Streamlit to explore the dataset and make predictions.

# About this project.
This project is all about cleaning the software developer salary dataset, from Stack overflow, for the year 2020, applying various machine learning models to the data (Mainly regression) to make the predictions about the salaries of software developers, and finally using Streamlit to build a web app to enable a user explore the dataset and make predictions of developer salaries.

# Goal of this project
* To apply data cleaning on the dataset
* To apply several Machine Learning Algorithms on the dataset and find out the best model that can be used to predict developer salaries (Regression Model)

# Libraries Used
* Pandas.
* Numpy.
* Scikit-learn
* Pickle

# Data cleaning
The dataset was downloaded from Stacjk Overflow. With over 70,000 responses fielded from over 180 countries, the Annual Developer Survey examines all aspects of the developer experience from learning to code to their favorite technologies to version control and the workplace experience of professional developers. The most important variables used for data analysis, which in my view contribute to changes in salary amounts are Education level, Country, Years of experience and age.
All rows containing null values (missing observations) were dropped as here is enough data even after dropping the rows with missing data. Countries with counts of less than 400 were also dropped.
The outliers (salaries greater than $250,000) were also removed from the dataset.

# Machine Learning Algorithms used.
* Linear Regression
This was the first model applied to the dataset to see if the age, years of experience, country and education level can be used to predict developer salary. The model had a mean squared error of 38707.10276261793

* Decision tree regression.
This followed Linear Regression, and the model had a mean squared error of 23097.990800603697. This was better compared to the liner regression model.

* Random Forest Regressor.
This model had a mean squared error of 23971.29743334671, which was not any better than the decision tree regressor.

* Grid search CV
The mdel had a mean absolute error of 147.70274636907232, which was better off compared to the previous three models, so this was the model used for predictiong developer salary based on age, education levcel, years of experience and country the developer was from.


The model was saved using Pickle and will be used for creating a user interface to predict developer salary using Streamlit.

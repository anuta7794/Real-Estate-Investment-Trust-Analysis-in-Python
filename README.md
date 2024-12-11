# Real Estate Investment Trust Analysis and Data Modeling in Python

### Overview:

This Project is a part of the "Data Analysis with Python" IBM course and aims to showcase data analysis skills in Python such as:

+ Developing Python code for cleaning and preparing data for analysis - including handling missing values, formatting, normalizing, and binning data;

+ Manipulating data using dataframes, summarizing data, understanding data distribution, performing correlation and creating data pipelines;

+ Performing exploratory data analysis and applying analytical techniques to a real-word dataset using libraries such as **_Pandas_**, **_Numpy_** and **_Scipy_**;

+ Building and evaluating regression models using machine learning **_scikit-learn library_** and using them for prediction and decision making.

I used **_Jupyter Notebook_** to Complete this Project (http://localhost:8888/notebooks/Desktop/IBM%20Data%20Analyst/Data%20Analysis%20with%20Python/Final%20Project%20-%20Data%20Analytics%20for%20House%20Pricing/House%20Sales%20in%20King%20County%20USA%20Analysis.ipynb).

### Scenario:

For this project, I assumed the role of a Data Analyst working at a Real Estate Investment Trust. The Trust would like to start investing in Residential real estate. I am tasked with determining the market price of a house given a set of features. I will analyze and predict housing prices using attributes or features such as square footage, number of bedrooms, number of floors, and so on. 

### Dataset:

The dataset contains house sale prices for King County, which includes Seattle. It includes homes sold between May 2014 and May 2015. It was taken from (https://www.kaggle.com/datasets/harlfoxem/housesalesprediction).

### Steps:

1. Importing Data Sets:

   + Displaying the data types of each column using the function **_dtypes_**.

2. Data Wrangling:

   + Dropping the columns "id" and "Unnamed: 0" from axis 1 using the method **_drop()_**, then use the method **_describe()_** to obtain a statistical summary of the data;
   + Replacing the missing values with the mean of the column using the method **_replace()_**.

3. Exploratory Data Analysis:

   + Using the method **_value_counts_** to count the number of houses with unique floor values, use the method **_.to_frame()_** to convert it to a dataframe;

   + Use the function **_boxplot_** in the seaborn library to determine whether houses with a waterfront view or without a waterfront view have more price outliers;
  
   ![Boxplot](https://github.com/user-attachments/assets/840b2820-1a81-4605-bd52-acec8055f69f)

   + Using the function **_regplot_** in the seaborn library to determine if the feature sqft_above is negatively or positively correlated with price.
    
   ![Scatterplot](https://github.com/user-attachments/assets/0b15c214-4a7a-4057-83e5-c39f9c24f2d4)

4. Model Development:

   + Fitting a **_linear regression model_** to predict the 'price' using the feature 'sqft_living', then calculating the **_R^2_**;
  
   + Fiting a **_linear regression model_** to predict the 'price' using the list of features;
  
   + Creating a list of tuples, the first element in the tuple contains the name of the estimator; the second element in the tuple contains the model constructor;
  
   + Using the list to create a **_pipeline object_** to predict the 'price', fitting the object using the features in the list features, and calculating the **_R^2_**.

5. Model Evaluation and Refinment:

   + Splitting the data into training and testing sets;
  
   + Creating and fit a **_Ridge regression object_** using the training data, setting the regularization parameter to 0.1, and calculating the R^2 using the test data;
  
   + Performing a **_second order polynomial transform_** on both the training data and testing data. Creating and fitting a **_Ridge regression object_** using the training data, setting the regularisation parameter to 0.1, and calculating the **_R^2_** utilising the test data provided. 

    

  

   


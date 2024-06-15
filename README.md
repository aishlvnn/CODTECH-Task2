# CODTECH-Task2
Name: Aaishah Sheikh

Company: CODTECH IT SOLUTIONS

ID: CT08PP700

Domain: Data Science

Duration: May to June 2024

Mentor: G. Sravani

Task 2: Exploratory Data Analysis
Importing Libraries
The necessary libraries for data manipulation, visualization, and machine learning are imported. This includes:

numpy for numerical operations.
pandas for data manipulation and analysis.
matplotlib and seaborn for data visualization.
warnings to suppress warnings during the execution.

Loading and Exploring Data
The dataset is loaded using pd.read_csv(). Initial exploration involves:

Displaying the first 10 rows to get an overview of the data.
Checking the shape of the dataset to understand its dimensions.
Using info() to get detailed information about the data types and non-null counts of each column.
Identifying missing values in each column using isnull().sum().
Cleaning Data
Functions are defined to clean and preprocess the data:

clean_size(): Converts the Size column values from strings with 'M' and 'k' suffixes to numerical values in bytes.
clean_size_mb(): Converts the Size column values to numerical values in megabytes.
clean_install(): Cleans the Installs column by removing commas and the '+' sign, converting the values to floats.
clean_price(): Cleans the Price column by removing the '$' sign, converting the values to floats.
These functions are applied to the relevant columns, and missing values are handled:

For the Size column, missing values are filled with the mean size of the respective category.
Rows with missing sizes and ratings are removed.
Exploratory Data Analysis (EDA)
Descriptive statistics and visualizations are performed to understand the dataset better:

Summary statistics of the dataset are displayed using describe().
Distribution plots for Rating, Size, and Reviews are created using seaborn's kdeplot() to visualize their spreads.
Count plots for categorical variables such as Type, Content Rating, and Category are created to visualize the frequency of each category.
Bar plots are created to show the mean ratings of apps per category.
Regression plots are created to explore relationships between variables like Reviews, Ratings, Price, and Size.
Data Preparation for Machine Learning
The data is prepared for machine learning by:

Dropping columns that do not contribute numerically to the regression model (Current Ver, Android Ver, App, and Last Updated).
Encoding categorical variables using pd.get_dummies().
Splitting the data into features (X) and target (y) variables.
Splitting the data into training and test sets using train_test_split().
Scaling the data using StandardScaler() to normalize the features for better performance of the machine learning model.
Building and Evaluating the Model
A Random Forest Regressor is used for predicting the Rating of apps:

The RandomForestRegressor model is instantiated and fitted to the training data without hyperparameter tuning.
Predictions are made on the test data.
Scatter plots and residual plots are created to visualize the model's predictions against the actual values.
The performance of the model is evaluated using metrics like Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).
The model's accuracy is calculated based on the Mean Absolute Percentage Error (MAPE).
This process involves thorough data cleaning, exploration, visualization, and preparation to build a machine learning model that can predict app ratings on the Google Play Store. Each step is crucial for ensuring the quality and reliability of the predictions made by the model.

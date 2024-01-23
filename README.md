# READ ME
This read me file contains a short explanation of the files in this folder and a short introduction to the topic, project description, and the way we conducted our work.
___
## Authors
- `Sander van Duin`
- `Ali Kalantari Khandani`
- `Owen Alberts`
- `Patrick Nasr-Alla`
___
## Files

- Jupyter Notebooks
    - EDA
        - Final EDA.ipynb
    - Models
        - Final Model with all Variables.ipynb
        - Final Model with all Variables except MMR.ipynb
        - Final Model with MMR and Categorical Features.ipynb
        - Final Model with MMR and Numerical Features.ipynb
        - Final Model with only MMR.ipynb
- CSV files
    - EDA
        - car_prices.csv
    - Models
        - cleaned_car_data_Final_EDA1.csv
- Results
    - Results.ipynb

___
## Installation
Before opening and running the files in this folder, please be aware that setting up your `path` name in every file is necessary in order for it to fully run. Here is a demonstration:
```python
# Set the path to the directory containing the dataset 
path = r"Your Pathname" 

# Change the current working directory to the specified path
os.chdir(path)

# List files in the 'car' subdirectory to verify the presence of the dataset
os.listdir(os.path.join('car'))

# Construct the file path for the car prices dataset
car_path = os.path.join("car" , "car_prices.csv")
# Load the dataset from the specified path into a pandas DataFrame
# 'on_bad_lines="skip"' is used to handle any problematic lines during loading
car_df = pd.read_csv(car_path, on_bad_lines="skip")
# Display the first few rows of the DataFrame for a preliminary look at the data
car_df.head()
```
Also make sure you have the right name for your subdirectory file. In this case it is car, but it can be different for you.

___
## TOPIC
The topic of this project is how a car dealership can use advanced predictive modeling techniques to enhance a car dealership's decision-making process in inventory selection and pricing to maximize profitability.

***`The results of this project can be found in the "Results.ipynb" file. A comprehensive explanation of the results is shown there`***

___
## Project Description



#### Introduction
This project harnesses `advanced predictive modeling to revolutionize decision-making in car dealerships`, focusing on enhancing inventory selection and pricing strategies. `The goal` is to leverage data-driven insights for boosting profitability in the competitive automotive market.

#### Objectives
- Implement predictive models for accurate car price prediction.
- Analyze the impact of car features on selling prices to optimize inventory.
- Develop dynamic pricing strategies based on market trends and car characteristics.
- Enhance customer experience and resource allocation efficiency through data analysis.

#### Methodology

- Data Collection and Preprocessing
    - Gathered and cleansed data on used car auction prices and relevant features.

- Model Development
    - Developed and compared various models: Random Forest, Neural Networks, KNN, XGBoost, and Linear Regression.
    - Trained and tested these models on different feature subsets to evaluate their price prediction accuracy.

- Key Techniques and Concepts
    - **Feature Analysis**: Investigating how features like body type, color, region, and MMR data affect car prices.
    - **Predictive Analytics**: Using machine learning to forecast car selling prices and identify profitable inventory.
    - **Dynamic Pricing**: Adjusting pricing in response to market trends and vehicle specifics.
    - **Risk Assessment**: Identifying and mitigating potential inventory risks.

___
## Project Workflow of EDA and the Models
By using an `used car auction prices dataset`, a workflow was created as follows:

##### *EDA*
1. `Exploratory Data Analysis and Data Cleaning`
    - **Techniques Used**: Correlation analysis, descriptive statistics, distribution visualizations.
    - **Tasks**: Outlier removal, missing values imputation.
2. `Feature Engineering`
    - **Process**: Create a feature dataset from clean data.
    - **Tasks**: Feature scaling/normalization, feature selection, categorical variable encoding, feature transformation, new feature creation.
##### *Models*
3. `Datasets Generation`
    - **Details**: Generate train, validation, and test datasets.
4. `Model Fitting`
    - **Models**: Random Forest and Neural Network.
    - **Tasks**: Fitting, hyperparameter tuning using grid-search.
    - **Analysis**: Investigate loss function evolution over epochs for Neural Network.
5. `Model Evaluation`
    - **Metrics**: Choose appropriate performance metrics.
    - **Analysis**: Actual vs. predicted plots, confusion matrix.
6. `Model Selection`
    - **Objective**: Compare the performance of the Neural Network and Random Forest models.
7. `Explainability`
    - **Focus**: Explain the best performing model’s predictions using feature importance methods.
8. `Additional Models`
    - **Models**: Linear/Logistic Regression, KNN, XGBoost.
    - **Comparison**: Evaluate these models against Random Forest and Neural Network.





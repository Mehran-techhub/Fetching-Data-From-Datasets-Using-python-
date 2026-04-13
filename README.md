# Fetching-Data-From-Datasets-Using-python-


Project Overview

This project focuses on fetching, importing, and analyzing datasets using Python. The workflow includes downloading real-world datasets from Kaggle, loading them into Python, and performing data extraction and manipulation for further analysis and model development. It demonstrates practical experience in handling structured data for data science and machine learning tasks.

Objective

The main objective is to learn how to access real-world datasets from Kaggle, import them into Python environments, and efficiently extract meaningful information for analysis, visualization, or machine learning model training.

Tools & Technologies
Python
Pandas (data manipulation)
NumPy (numerical operations)
Matplotlib / Seaborn (visualization)
Kaggle Dataset Platform
Jupyter Notebook / VS Code
Step 1: Getting Dataset from Kaggle
Create an account on Kaggle: https://www.kaggle.com
Go to the dataset section and search for a relevant dataset (e.g., sales, health, finance, etc.).
Download dataset manually OR use Kaggle API.
Using Kaggle API (Professional Method):
Install Kaggle library:
pip install kaggle
Download API token from Kaggle account settings
Place kaggle.json file in .kaggle folder
Run command to download dataset:
kaggle datasets download -d <dataset-name>
Extract ZIP file:
import zipfile

with zipfile.ZipFile("dataset.zip", "r") as file:
    file.extractall("data")
Step 2: Loading Dataset into Python

Once dataset is downloaded:

import pandas as pd

df = pd.read_csv("data/dataset.csv")
Step 3: Data Exploration (Fetching Data)

After loading dataset, data is explored using Pandas:

df.head()        # First 5 rows
df.tail()        # Last 5 rows
df.info()        # Dataset structure
df.describe()    # Statistical summary
df.columns       # Column names
Step 4: Data Fetching & Filtering

Extracting specific data based on conditions:

df['column_name']               # Single column
df[df['age'] > 25]             # Conditional filtering
df.loc[0:10, ['col1','col2']]  # Specific rows & columns
Step 5: Data Cleaning

Handling missing or incorrect data:

df.isnull().sum()        # Check missing values
df.dropna()              # Remove null values
df.fillna(0)             # Replace missing values
Step 6: Data Analysis

Performing analysis on dataset:

df.groupby('category').mean()
df['sales'].sum()
df['profit'].max()
Step 7: Visualization (Optional)
import matplotlib.pyplot as plt

df['sales'].plot(kind='bar')
plt.show()
Key Features of Work
Real-world dataset handling from Kaggle
API-based dataset downloading
Structured data cleaning and preprocessing
Efficient data extraction and filtering
Basic data analysis and visualization
Learning Outcomes

Through this project, I gained practical experience in:

Working with real-world datasets
Using Kaggle as a data source
Python-based data manipulation using Pandas
Data cleaning and preprocessing techniques
Extracting insights from raw data

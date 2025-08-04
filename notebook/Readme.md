Nigeria Malaria Data Analysis
Cleaning, Exploration, and Predictive Modeling

Project Structure
text
├── data/  
│ └── Nigerian_malaria.csv # Raw dataset (NMIS 2016)  
├── notebooks/  
│ └── dataclean.ipynb # Data cleaning & EDA (Jupyter Notebook)  
├── outputs/  
│ ├── cleaned_data/ # Processed CSV files  
│ └── visualizations/ # Graphs/plots  
└── README.md  
Dataset Overview
File: Nigerian_malaria.csv

Source: Nigeria Malaria Indicator Survey (NMIS 2016)

Variables:

hhid: Household ID

hv024, hv025: State/Region codes

hv201, hv205: Water source & sanitation

hv206, hv213: Mosquito net usage

hv210, hv211: Malaria testing results

Notebook: dataclean.ipynb

1. Setup
   python
   import pandas as pd
   import matplotlib.pyplot as plt
   import seaborn as sns
   import numpy as np
2. Load Data
   python
   malaria = pd.read_csv('../data/Nigerian_malaria.csv')
   malaria.head(10) # Preview first 10 rows
3. Data Cleaning
   Tasks:

Handle missing values (hv213, hv214).

Recode categorical variables (e.g., hv025: Urban/Rural → 0/1).

Filter relevant columns:

python
cols = ['hv024', 'hv025', 'hv206', 'hv213', 'hv210']
malaria_clean = malaria[cols].dropna() 4. Exploratory Analysis

Next Steps
Merge Climate Data: Add CHIRPS/NOAA datasets for predictive modeling.

Machine Learning: Train a classifier (e.g., Logistic Regression) in a new notebook.

Fatime Dadi Wardougou , 25858

My github link: https://github.com/Fatime-Dadi/Malaria_25858

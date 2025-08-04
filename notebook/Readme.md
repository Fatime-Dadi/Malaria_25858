# Nigeria Malaria Data Analysis

## Project Overview

This project analyzes malaria data from the Nigeria Malaria Indicator Survey (NMIS 2016) to explore household and environmental factors, clean and preprocess the data, and build predictive models for malaria risk. The workflow includes data cleaning, exploratory data analysis (EDA), and machine learning.

## Project Structure

### Data Description

- **Raw Data**: `Nigerian_malaria.csv` contains household-level survey data.
- **Key Variables**:
  - `hhid`: Household ID
  - `hv024`, `hv025`: State/Region codes
  - `hv201`, `hv205`: Water source & sanitation
  - `hv206`, `hv213`: Mosquito net usage
  - `hv210`, `hv211`: Malaria testing results

## Workflow

### 1. Data Cleaning (`dataclean.ipynb`)

- Handle missing values: Especially in columns like hv213 (mosquito net usage) and hv214
- Recode categorical variables: For example, convert hv025 (Urban/Rural) to binary (0/1)
- Filter relevant columns
- Save cleaned data: Output to `cleaned_data.csv` and `Nigerian_malaria_dashboard.csv`

### 2. Exploratory Data Analysis (`data_visualization.ipynb`)

- Visualize distributions, correlations, and trends in the cleaned data
- Analyze asset ownership, wealth, and malaria prevalence by region and household characteristics

### 3. Predictive Modeling (`Appl_machinelearnig.ipynb`)

- Feature selection: Use cleaned and encoded variables
- Modeling: Train classifiers (e.g., Logistic Regression, Random Forest) to predict malaria risk
- Evaluation: Assess accuracy, confusion matrix, and classification report

### 4. Dashboarding (PowerBI)

- Visualize key findings and predictions using PowerBI (`Dashbord.pbix`)

## Next Steps

- Merge Climate Data: Integrate external climate datasets (e.g., CHIRPS/NOAA) for enhanced predictive modeling
- Model Improvement: Experiment with additional features and advanced machine learning algorithms

## Usage

# 1. Clone the repository

# 2. Ensure you have the required Python libraries:

```bash
pandas numpy matplotlib seaborn scikit-learn
```

Run notebooks in order:

dataclean.ipynb → data_visualization.ipynb → Appl_machinelearnig.ipynb

Explore the PowerBI dashboard for interactive visualizations

Author
Fatime Dadi Wardougou
GitHub: Fatime-Dadi/Malaria_25858

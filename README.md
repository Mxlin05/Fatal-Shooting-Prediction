# Predictive Analysis of Police Killings

## Overview

This project performs a comprehensive data analysis and machine learning study on fatal police shootings in the United States between 2015 and 2017. By integrating demographic datasets from the US Census Bureau with incident reports, the project explores socioeconomic factors—such as poverty rates, educational attainment, and racial demographics—to understand patterns and develop predictive models.

## Repository Structure

The repository contains the primary analysis notebook and several datasets required for the study:

* **`351_Project_Team_14_William_Chen_Nelson_Chan_Matthew_Lin.ipynb`**: The main Jupyter Notebook containing data cleaning, exploratory data analysis (EDA), and machine learning implementations.
* **`police_killings_train.csv` / `police_killings_test.csv**`: Core datasets detailing individual fatal shooting incidents.
* **`poverty.csv`**: Poverty rate data by geographic area and city.
* **`education.csv`**: Data indicating high school completion percentages.
* **`income.csv`**: Median household income data.
* **`share_race_by_city.csv`**: Racial breakdown of populations within specific cities.

## Machine Learning & Modeling

The project evaluated several algorithms to determine if socioeconomic and geographic features could effectively predict the race of an individual involved in a fatal shooting.

* **Baseline Model**: Established as a performance benchmark for comparison.
* **Logistic Regression**: Implemented as a linear approach to classification. By calculating the probability of a class through the logistic function, this model attempted to find linear decision boundaries between different demographic features.
* **Random Forest**: Employed to handle non-linear relationships through a collection of decision trees. While powerful, this model faced challenges with overfitting due to the high density of shared racial percentage features.
* **K-Nearest Neighbors (KNN)**: Tested on the premise that similar socioeconomic backgrounds (income, poverty) correlate with demographic groups. However, because socioeconomic factors often affect all races within a specific area similarly, the results remained ambiguous and struggled to outperform the baseline.

## Key Findings

The study revealed that while socioeconomic indicators like income and poverty rates are influential, they often overlap across racial boundaries in high-crime areas. This creates a "feature overlap" that makes it difficult for standard classification algorithms to achieve high precision without more granular, individual-level data.

## Contributions

* **Nelson Chan**: Conducted the **Exploratory Data Analysis (EDA)**, including data cleaning, merging the Census datasets with incident reports, and creating visualizations to identify initial trends.
* **Matthew Lin**: Led the **Machine Learning** phase, responsible for feature engineering, model selection (Logistic Regression, Random Forest, KNN), and evaluating model performance.
* **William Chen**: Handled the **Presentation** and documentation, synthesizing technical findings into a cohesive narrative and ensuring the project objectives were clearly communicated.

## How to Run

1. Ensure you have `python 3.x` installed.
2. Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn`.
3. Launch the notebook: `jupyter notebook 351_Project_Team_14_William_Chen_Nelson_Chan_Matthew_Lin.ipynb`.

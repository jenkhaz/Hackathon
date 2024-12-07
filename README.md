# EECE 490 Hackathon
# Personality Traits and Smoking Behavior Analysis

This repository explores the relationship between personality traits, sociodemographic factors, lifestyle variables, and smoking behaviors in a dataset of approximately 200 participants. The primary focus is on predicting outcomes such as the number of cigarettes smoked per day (CigsPerDay), time to first cigarette (TimeToFirstCig), and social media hours (SocialMediaHours).

## Project Overview

The analysis includes:
- **Data Preprocessing:**  
  - Translation of Arabic responses to English.  
  - Dropping columns that are not suitable for encoding (free-text comment fields).  
  - Renaming columns for clarity and convenience.
  - Label encoding categorical features and ensuring numeric columns remain as is.

- **Feature Selection:**  
  Using simple correlation thresholds (e.g., `abs(corr) >= 0.1` or `0.2`) to select features related to the target variables.

- **Modeling Approaches:**  
  Experiments with several models, including:
  - Logistic Regression  
  - XGBoost Classifier  
  - Attempts at hyperparameter tuning using `GridSearchCV`.

- **Targets Modeled:**
  - **CigsPerDay:** Categories of cigarettes smoked daily.
  - **TimeToFirstCig:** An indicator of nicotine dependence, measured by how soon after waking a participant smokes their first cigarette.
  - **Social Media Usage:** Attempts to predict the extent of social media usage.

- **Evaluation Metrics:**
  - Accuracy, Confusion Matrices, and Classification Reports to assess model performance.
  - Cross-validation to evaluate model stability.

## Key Findings

- **Modest Accuracy (~50-56%)**:  
  Despite using advanced models like XGBoost and performing hyperparameter tuning, the predictive performance remained modest.

- **Small Dataset (~200 Data Points)**:  
  The dataset’s limited size likely hinders model generalizability and stability, as complex human behaviors like smoking patterns are difficult to capture with so few samples.

- **Complex, Multifaceted Behaviors:**  
  The complexity of human behavior around smoking, influenced by personality, socioeconomic factors, and lifestyle, cannot be easily captured by a limited set of features and samples.

## Recommendations & Future Work

- **More Data:**  
  Increasing the sample size is crucial to improve statistical power and capture a broader range of behaviors.

- **Feature Engineering & Domain Expertise:**  
  Incorporating domain knowledge, creating more informative features, or collecting additional variables could yield stronger predictive signals.

- **Advanced Modeling Techniques:**  
  Exploring ordinal models for TimeToFirstCig or trying different machine learning algorithms, ensembles, or deep learning approaches may uncover improvements.

## Repository Structure

- **Data:**  
  Contains the original and processed CSV files (if publicly shareable).

- **Notebooks:**  
  Jupyter notebooks detailing the data preprocessing steps, model training, tuning, and evaluations.

- **Scripts:**  
  Python scripts for cleaning data, encoding columns, running models, and generating reports.

- **Results:**  
  Saved confusion matrices, classification reports, and summary tables for reference.


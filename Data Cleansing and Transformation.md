# NLP Resume Extraction - Project Document

## Team Member Details
- **Group Name:** Lone Data Enthusiast
- **Team Members:**
  1. Name: Ritu Kukreja<br>
     Email: rk977@drexel.edu<br>
     Country: United States<br>
     College/Company: Drexel University<br>
     Specialization: Data Science, NLP, Data Analyst<br>

## Problem Description

The goal of this analysis is to process and analyze a dataset containing resume information. The dataset is provided in JSON format and includes details such as name, designation, companies worked at, skills, graduation year, college name, degree, location, and years of experience.

# Data Cleansing and Transformation

## Imputing Missing Values
### Technique 1: Mean/Median/Mode Imputation
In this technique, missing values in the numerical columns ('Graduation Year' and 'Years of Experience') are imputed using the mean. Categorical columns ('Location', 'Designation', 'Companies', 'Skills', 'College Name', 'Degree') with None values are replaced with a consistent placeholder value ('Unknown'). This approach ensures a standardized and comprehensive handling of missing data using mean imputation in numerical columns and placeholder values in categorical columns.

### Technique 2: Model-Based Imputation

## Handling Outliers
This code segment involves handling outliers in the dataset using the Interquartile Range (IQR) method. The lower and upper bounds of the IQR are calculated using the first quartile (Q1) and third quartile (Q3). Data points outside the range defined by these bounds are considered outliers and subsequently removed from the dataset. This outlier-handling technique ensures a more robust and accurate dataset, free from extreme values that could impact the analysis and modeling processes.

# NLP Featurization

1. Defined a function to calculate years of experience by considering both "Years of Experience" and "Graduation Year" columns.
2. Applied the function to the DataFrame, updating the 'Years of Experience' column.
3. Detected outliers using Z-scores and removed them based on a threshold of 3 standard deviations.
4. Calculated skewness and visualized the distribution for numeric columns.

## Clean the Data using Regex
1. Utilized regex patterns to extract information on total IT experience from the text.
2. Iterated through the DataFrame, updating 'Years of Experience' based on extracted information.

# Code Reviews
Given that I am the sole contributor to this project, I conducted comprehensive code reviews, meticulously reviewing and refining my code on two separate occasions.

Lone Data Enthusiast<br>
10/26/2023

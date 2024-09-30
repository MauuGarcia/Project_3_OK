# Project 3: WHO World Health Statistics 2020 Analysis

#### Team: Nallely González, David Girma, David Flores, Elena Zamudio, Francisco García and Mauricio García.

## Overview

This project aims to analyze global health statistics from the World Health Organization (WHO) to uncover patterns, trends, and insights related to cancer, cardiovascular diseases, diabetes, and chronic respiratory diseases. The dataset used in this analysis is sourced from the WHO World Health Statistics 2020 and provides an in-depth look into the health status of countries worldwide.

## Purpose.

The purpose of this project is to undertake a comprehensive analysis of global health statistics with a particular emphasis on non-communicable diseases (NCDs) such as cardiovascular diseases, cancer, diabetes, and chronic respiratory diseases. Using the World Health Organization's (WHO) 2020 health statistics dataset, we aim to explore various factors that contribute to mortality rates and overall life expectancy across different countries. By examining these variables, we seek to uncover patterns, identify correlations, and ultimately provide insights that could guide global health policy and intervention strategies.

A critical component of this project is the relationship between environmental factors, specifically air pollution, and mortality rates attributed to NCDs. Air pollution is a well-known risk factor for many respiratory and cardiovascular conditions. Therefore, one of the project's key questions is to explore how mortality rates from diseases like cardiovascular conditions, cancer, diabetes, and respiratory illnesses are linked to air pollution-related deaths. By understanding the strength of this relationship, we can assess the potential impact of environmental health interventions on reducing NCD-related mortality rates. This exploration is crucial, given that air quality is a modifiable factor that can be improved through policy and public health initiatives.

Additionally, we aim to investigate the connection between life expectancy and mortality rates from NCDs. Life expectancy is a fundamental indicator of a country's overall health, and it is often affected by the prevalence and management of chronic diseases. In this analysis, we seek to identify trends that show how higher mortality rates from cardiovascular diseases, cancer, diabetes, and respiratory diseases correlate with a decrease in life expectancy. Understanding this relationship can help highlight the profound impact that these diseases have on populations' health and longevity, underscoring the importance of comprehensive health policies aimed at managing NCDs.

The project also delves into the influence of lifestyle choices, such as tobacco and alcohol consumption, on health outcomes. Specifically, we explore the correlation between tobacco consumption and mortality rates associated with cardiovascular diseases, cancer, diabetes, and respiratory diseases. Tobacco use is widely recognized as a major risk factor for these conditions. Therefore, our analysis will provide insights into how strongly tobacco use is linked to increased mortality, potentially informing public health policies and smoking cessation programs. Similarly, we examine the relationship between alcohol consumption rates and cancer mortality. Alcohol is another modifiable risk factor, and this analysis seeks to determine whether higher alcohol consumption correlates with increased cancer mortality rates, thereby contributing to the body of evidence on lifestyle-related risk factors.

Healthcare system coverage and resource allocation are additional focal points in our project. We investigate how the mortality rate from NCDs is related to health service coverage across various countries. Specifically, we aim to assess whether higher coverage rates correlate with lower mortality rates, thereby evaluating the effectiveness of healthcare accessibility. This examination extends to identifying which countries with high mortality rates suffer from a lack of healthcare professionals, particularly doctors, available per 10,000 inhabitants. By analyzing the distribution of healthcare resources, we seek to understand whether the availability of medical professionals significantly impacts mortality rates. This information can be crucial for policymakers and healthcare planners, as it may highlight regions that need increased healthcare workforce capacity.

Environmental health determinants, such as reliance on clean fuels, are also examined in this project. We assess how the use of clean fuels correlates with mortality rates from cardiovascular diseases, cancer, diabetes, and respiratory diseases. The use of clean fuels for cooking and heating is an important factor in reducing indoor air pollution, which is known to contribute to respiratory diseases. This part of the analysis will help identify whether countries relying on clean energy experience lower mortality rates, providing evidence for environmental interventions as a means to improve health outcomes.

Lastly, we explore the relationship between health service coverage and infant mortality rates. Infant mortality is a critical indicator of a country's healthcare quality and access. In this analysis, we identify which countries with high infant mortality rates suffer from low health service coverage. This investigation seeks to reveal whether insufficient healthcare services significantly impact infant mortality, thereby emphasizing the importance of improving health coverage to protect vulnerable populations. 

By addressing these comprehensive research questions, this project aims to provide a holistic view of global health challenges related to NCDs. It seeks to identify key risk factors, healthcare disparities, and areas for targeted interventions. The insights derived from this analysis can support public health officials, policymakers, healthcare providers, and researchers in their efforts to develop effective strategies and allocate resources efficiently to improve health outcomes and reduce mortality worldwide. Ultimately, the project endeavors to contribute to a greater understanding of the complex interplay between environmental, lifestyle, and healthcare factors in shaping global health trends.

## Project Workflow

### Overview
This section outlines the workflow of the project, including how data is processed, transformed, and stored in an SQL database. It also provides instructions on how to use and interact with the project effectively.

### 1. Extract, Transform, Load (ETL) Workflow
The project employs an ETL process to ingest, transform, and store data in an SQL database. Below is a step-by-step breakdown of the workflow:

1. **Extract:**
   - The project begins by extracting data from the WHO World Health Statistics 2020 dataset, which is available in CSV format. This dataset contains comprehensive information about global health statistics, including mortality rates, healthcare resources, and lifestyle factors.
   
2. **Transform:**
   - Before loading the data into the database, the raw dataset undergoes a transformation process. During this phase, unnecessary columns are removed, data types are standardized, and null or missing values are handled to ensure data consistency and accuracy. The transformed data is then organized into tables that facilitate structured storage in the SQL database.
   
3. **Load:**
   - The transformed data is loaded into an SQL database. For this project, SQL was chosen because of its robust capabilities in handling structured data and performing complex queries efficiently.
   
4. **Database Documentation:**
   - SQL was chosen for this project due to its strengths in handling structured datasets, performing data analysis, and facilitating complex queries. The tabular format of the data fits well into an SQL schema, making it easier to organize and query the information.
   - The project includes an **Entity Relationship Diagram (ERD)** to visually represent the database schema and relationships between the tables. This diagram is provided to help users understand the database structure and how different data points are connected.

### 2. Database Interaction
The project provides a method for reading data from the SQL database and displaying it for further analysis:

1. **Pandas DataFrame:**
   - Data can be retrieved from the SQL database using SQL queries and converted into a Pandas DataFrame. This allows for flexible data manipulation and analysis using Python's extensive data science libraries.
   - The `pandas` and `sqlite3` libraries are used to connect to the SQL database, execute queries, and convert the resulting data into a format that is easy to work with for analysis.

2. **Future Use:**
   - The data retrieval method can be extended or modified to suit different analytical needs, such as exporting data for visualization in Jupyter Notebooks or creating dashboards for real-time data analysis.

### 3. How to Use the Project
To use and interact with this project, follow these steps:

1. **Clone the Repository:**
   - Clone the repository to your local machine using the following command:
     ```bash
     git clone https://github.com/MauuGarcia/Project_3_OK.git
     ```

2. **Install Required Libraries:**
   - Ensure you have all necessary Python libraries installed, including:
     - `pandas` (for data manipulation)
     - `sqlite3` (for database interactions)
     - `matplotlib` (for visualizations)
   - You can install the required libraries using:
     ```bash
     pip install pandas sqlite3 matplotlib
     ```

3. **Set Up the Database:**
   - The repository includes a script to create the SQL database and populate it with the transformed data. This script will automatically create the necessary tables (`HealthStatistics` and `RiskFactors`) and insert the data into these tables.
   - Run the provided script to set up the SQL database:
     ```bash
     python setup_database.py
     ```

4. **Run the Data Processing Script:**
   - The repository contains Jupyter Notebooks that demonstrate how to extract, transform, and load data into the SQL database. Open these notebooks in Jupyter and execute the cells to perform the ETL process.
   - The script will connect to your SQL database, create the necessary tables, and insert the transformed data.

5. **Interact with the Data:**
   - Once the data is stored in the SQL database, you can use the provided Python scripts or notebooks to query and analyze the data. Examples include:
     - Executing SQL queries to retrieve data from the `HealthStatistics` and `RiskFactors` tables.
     - Converting data from SQL queries into a Pandas DataFrame for further analysis and visualization.

### 4. Additional Features
- The project includes methods for extracting data from the database, transforming it into a usable format, and visualizing it, offering a comprehensive approach to data analysis.

By following this workflow, users can successfully extract, transform, and analyze global health data using an SQL database. This project serves as a valuable tool for exploring key health statistics and their relationships, providing insights into global health challenges.

### 4. Ethical Considerations
In conducting this project, we have taken several steps to ensure the ethical use of health data. The dataset used is publicly available and does not contain personally identifiable information, thereby minimizing privacy concerns. All analyses are performed in aggregate form to highlight general trends and insights rather than targeting specific individuals or groups. Additionally, we acknowledge the limitations of this dataset, as it provides a snapshot of health statistics from specific years and may not reflect the most current global health conditions. Our goal is to use this information responsibly, presenting findings that can aid in understanding global health challenges without causing harm or misinterpretation.

### 5. References
- **Data Source:** The data for this project was obtained from the following Kaggle dataset: [WHO World Health Statistics 2020 Complete](https://www.kaggle.com/datasets/utkarshxy/who-worldhealth-statistics-2020-complete).
- **Code References:** This project makes use of standard data analysis and visualization libraries in Python, such as `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scipy`. Any external code used has been appropriately adapted and cited within the project documentation.
- **Bootcamp references:** © 2024 edX Boot Camps LLC
By following this workflow, you can effectively extract, transform, and interact with global health data using this project. This provides a solid framework for understanding global health trends and insights, supporting further research and analysis.

# Telecom_Customer_Churn_individual_project
Title: Customer Churn Analysis

Data Cleaning and Preprocessing
1. I imported the raw dataset in csv to python environment using import pandas
  The dataset contained 7043 rows and 21 columns

2. The dataset was examined for missing values, duplicates and outliers.
  - The isna().sum code was ran for the missing values
  - Empty strings were replaced with NaN values for TotalCharges Column and they were removed.
  - Duplicates were checked for and also removed.
  - Outliers were calculated IQR method for numeric columns which are MonthlyCharges and TotalCharges
  - The remove outliers function was used to remove them from the dataframe

3. Missing data were handled through mean and median imputation techniques
  The missing value columns were filled with the mean value and median value respectively.

4. Some unneccesary columns(SeniorCitizen, Partner, dependents, streamingtv, streamingmovies, paperlessbilling) were dropped with the .drop code

5. Encode Categorical Variables with one-hot encoding
  The categorical variables were encoded to 'True' = 1 or 'False' = 0

6. The numeric columns were scaled with StandardScaler technique

Data Exploration
7. The describe() method was used to perform descriptive statistics on the dataset

8. Distribution of key variables like gender, monthlycharges, totalcharges and churn status were visualized using count plot for gender and churn status, then histogram for monthlycharges and totalcharges.

9. Heatmap was used to visualize correlations between; gender and monthlycharges, churn and monthlycharges, tenure and totalcharges, and Techsupport and churn.

10. The t-test hypothesis was conducted to compare the difference between churned and non-churned customers with the 'scipy' method

11. - Summary tables and statistics was created for 'contract type' and 'paymentmethod' columns 

Data Visualization
12. Insightful visualizations were generated to communicate findings:
    - Barplots for categorical columns: gender, churn, TechSupport, MultipleLines and PhoneService
    - Histograms was used for the numeric variables: Monthlycharges, Totalcharges and tenure.
    - Box plots to identify outliers in tenure, monthlycharges and totalcharges columns.
    - Scatter plots were created for numeric columns such as tenure, monthlycharges and totalcharges.
    - Pie chart was created to visualize the proportion of churned vs non-churned customers.
    - A count was made first, then it returned 73.4% for non-churned customers and 26.6% for churned customers.



Insights and Recommendation:
The factors influencing Churn form my analysis are MonthlyCharges for month-to-month contract type.
I will recommend that longer contracts are offered with incentives such as discounted monthlycharges. This will provide stability and reduce the likelihood of customers churning.

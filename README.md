# Bank-customer-churn-prediction
End-to-end data analysis  project to predict customer churn using Python and Power BI


🏦 Bank Customer Churn Prediction
Prepared By: Mrs. Tina Chaudhari
Project Date: April 2026
Dataset Source: Kaggle 
	EXECUTIVE SUMMARY:
Customer churn is one of the most critical challenges in the banking industry as it directly impacts revenue, profitability, and customer lifetime value. This project focuses on analyzing customer behavior to identify patterns and key drivers behind churn using a dataset of 10,000 bank customers.
The analysis reveals that approximately 20.4% of customers have churned, indicating that nearly 1 in every 5 customers is leaving the bank. Through deep exploratory data analysis (EDA) and dashboard visualization, the study identifies high-risk segments such as inactive customers, customers aged 45–60, high-balance individuals, and customers from Germany.
The Power BI dashboard provides an interactive view of churn patterns, enabling business users to filter and analyze customer segments dynamically. The insights generated from this project can help banks design targeted retention strategies, improve customer engagement, and reduce revenue loss.
This project demonstrates strong capabilities in data analysis, business understanding, and visualization, making it highly relevant for real-world business decision-making.

	BUSINESS PROBLEM:
Customer retention is a major concern for banks because acquiring new customers is significantly more expensive than retaining existing ones. High churn rates lead to:
•	Loss of revenue
•	Increased marketing and acquisition costs
•	Reduced customer lifetime value
The bank currently lacks a clear understanding of:
•	Which customers are most likely to churn
•	What factors drive customer attrition
•	How to proactively reduce churn
This project aims to solve these problems by identifying churn drivers and suggesting data-driven strategies for customer retention.
	WHY THIS DATASET WAS SELECTED:
•	Real Work Experience:
Worked at ICICI Bank   for 3 years   there I saw every day that loyal customers are suddenly leaving the bank. The bank tries very hard to retain them but sometimes it’s possible but most of the time it’s not.
•	Observed First-Hand: 
In the banking industry, customer churn is a billion-dollar domain. Acquiring a new customer is 5 times more expensive than retaining an existing one and the most interesting thing is what the bank assumes that for example: senior customers are loyal but the data told something different to me.
The Gap: Bank could not predict churn in advance. So, for identifying this issue in banking sector I choose this dataset.
	This dataset was selected because it closely represents a real-world banking scenario and contains key variables required to analyze customer churn effectively.
•	Reasons for selection:
•	Contains 10,000 customer records, which is sufficient for meaningful analysis
•	Includes important behavioral and financial features such as balance, credit score, and activity status
•	Covers multiple geographic regions (France, Germany, Spain) for comparative analysis
•	Clean dataset with no missing values and no duplicates, making it ideal for analysis
•	Widely used in industry and available on Kaggle, making it relevant for portfolio projects
This dataset allows for both exploratory analysis and predictive modeling, making it a strong choice for demonstrating end-to-end data analytics skills.
	Project Objective:
	The objective aims to understand:
	Behavior patterns of customers across different segments
	High-risk customer groups
	Business impact of churn on revenue and profit
	Early warning signs to catch at-risk customers
 
	Dataset Structure & Features:
The dataset has 10,000 customer records with 14 columns, including ID columns. Each column shows a different customer detail that helps us understand why customers leave. It shows customer information and money habits.
Feature Name	Data Type
	Description

Credit Score
	Numerical
	Number that shows credit history
Geography
	Categorical
	Country or region where the customer is located
Gender
	Categorical
	Binary category for customer gender
Age
	Numerical
	Customer age, an important factor
Tenure	Numerical	How long the customer has been with the bank

Balance	Numerical	Shows how much money they have
Num Of Products	Numerical	How many products they use

Has Credit Card
	Binary	Indicates whether the customer has a credit card
Is Active Member	Binary	Indicates whether the customer actively uses their account
Estimated Salary	Numerical	Estimated salary of the customer
Churn	Binary/Target	Target variable where 1 = churn and 0 = retained
	Tools & Libraries Used:
           Programming language → Python
Libraries: 
•	Pandas
•	NumPy
•	Matplotlib
•	seaborn
•	sklearn
Platform Used :- Jupyter Notebook.
For visualization – Power BI 
	Data Understanding: - Initially, I explore the dataset to understand its structure & features. Firstly, I imported the libraries and then upload the “BANK CUSTOMER CHURN PREDICTION” Dataset in my jupyter notebook using pandas.  
	Then I used the following functions to understand the datatypes & missing values, column names  and overall data structure.  
SL. NO.	FUNCTIONS	DESCRIPTIONS
1.	data. columns() 
	Gives  all column names in the dataset . 
2.	data. shape()	Gives number of rows and columns in the dataset(10000,12)
3.	data. info()	Gives summary of the dataset includes column names , dtype, non-null count
4.	data. dtypes
	It gives specifically info regarding  dtypes
5.	data. describe()	Generates statistical summary (count, mean, std, min, |
| | 25%, 50%, 75%, max) for numerical columns.
6.	.isnull().sum()	Gives column names with missing values . I  found that there are no missing values in any column. This means the dataset is clean and does not require any imputation techniques like mean, median, or mode filling
7.	data.duplicated().sum()	Its for duplicate records and the result was 0, which means there are no duplicate rows in the dataset. This ensures data quality and prevents bias in analysis or model training
8.	data.nunique()	This helps in understanding feature diversity, identifying categorical variables, and detecting columns that may not be useful for modeling.
9.	Heatmap 	 This graph also helps to visualizes the missing values in the dataset so I can easily decide which column I have to drop and which columns I have to fill 
<Axes: >
	Observations:  checked through the heatmap also and found that there are no missing values in any column. This means the dataset is clean and does not require any imputation techniques like mean, median, or mode filling. Having no missing values helps ensure better model performance and simplifies preprocessing.

	Exploratory Data Analysis (EDA)
The EDA process follows a systematic approach from basic exploration to advanced feature engineering. The analysis employs Python functions to understand data structure, check data quality, and identify patterns in customer behavior
Step 1: Target Analysis (Distribution of Target)
  
 
OBSERVATIONS: I plotted a bar chart of the target variable churn to understand its distribution. The graph shows that the number of non-churned customers is significantly higher than churned customers. This indicates a class imbalance in the dataset, where approximately 80% customers stayed and 20% churned.
Categorical vs Churn analysis
  

OBSERVATIONS  :  I used a count plot to analyze the relationship between gender and churn. The plot shows the number of churned and non-churned customers for each gender. From the visualization, we can compare whether churn behavior differs between males and females.
NOTE : Female customers tend to have a slightly higher churn rate compared to male customers
  
OBSERVATION: I created a count plot to analyze churn distribution across different countries. The visualization shows the number of churned and non-churned customers for each country, with values displayed on top of each bar for better clarity. This helps identify geographical patterns in customer churn. NOTE: The plot shows that Germany has a higher churn rate compared to France and Spain.

 
OBSERVATION: I used a cross-tabulation to calculate the percentage of churn within each country. This helps compare churn rates across countries independent of their population size. I observed that Germany has a higher churn rate compared to France and Spain.

Numerical vs Target Analysis
 
OBSERVATIONS: I used a boxplot to compare the distribution of account balance between churned and non-churned customers. The plot shows that customers who churned generally have higher account balances compared to those who did not churn
  
OBSERVATIONS: I divided the balance into different ranges and checked how many customers churn in each range. I found that customers with higher balance are more likely to churn.
AGE DISTRIBUTION BY CHURN

 
OBSERVATION: I used a boxplot to compare the age of customers who churned and those who didn’t. I found that customers who churned are generally older

  
OBSERVATION: I divided age into different groups and checked churn in each group. I found that older age groups have higher churn. Binning helps us see trends clearly, and here it shows a strong relationship between age and churn

Binary columns vs Target variable analysis
OBSERVATION: I used a count plot to compare churn between customers who have a credit card and those who don’t. The result shows that there is no major difference in churn based on credit card ownership.
  
OBSERVATIONS: I used crosstab with normalization to compare churn percentage across credit card ownership. I found that both groups have almost similar churn rates, so credit card ownership does not significantly impact churn 

Churn by Active Membership
OBSERVATION: I analyzed churn based on active membership and found that inactive customers have a much higher churn rate compared to active customers. This indicates that customer engagement plays an important role in retention.

 

OBSERVATION: I compared churn percentage between active and inactive customers. I found that inactive customers have significantly higher churn (27%) compared to active customers (14%). This shows that active membership strongly impacts customer retention

	COLUMN TYPE SEGREGATION
I segregated the columns into categorical, binary, and numerical features to apply appropriate preprocessing techniques. Categorical columns like country and gender require encoding, binary columns are already in 0/1 format, and numerical columns can be used for scaling and modeling
OBSERVATIONS : I printed value counts for categorical columns to understand the distribution of categories. This helps identify dominant categories and check for imbalance

	Feature Segregation
  OBSERVATIONS: I used a loop to create count plots for all categorical variables against churn. This helps analyze how different categories impact customer churn and I found that country has stronger impact than gender.
I plotted histograms with KDE for all numerical features to understand their distribution, skewness, and presence of outliers.
OBSERVATIONS:
Distribution almost normal (bell-shaped)
Most values range is 600–700 
 OBSERVATIONS:
Right-skewed (positive skew)
Young customers are more
Older customers are less
 
OBSERVATIONS:
Uniform distribution (0–10 years) ,in every range customers are almost equal 
 
OBSERVATIONS:
Highly skewed , many customers having zero balance

OBSERVATIONS:
Discrete distribution
Most customers → 1 or 2 products
OBSERVATIONS:
Uniform distribution
Salary spread evenly
 obSERVATIONS:  I used boxplots to compare numerical features across churn categories to identify differences in distributions and detect key patterns
1.	Credit Score Churned customers having slightly lower score
2.	Age Churned customers are older Its showing strong relationship with churn
3.	Tenure not more difference Weak feature
4.	Balance Churned customers haing higher balance Strong indicator
5.	Products Number Most customers having one or two products Important feature
6.	Estimated Salary Almost same distribution Weak impact

	Age Binning (Feature Engineering)

OBSERVATIONS: I checked sample values and datatype of the age column to ensure data consistency and confirm that it is a numerical feature and I checked the minimum and maximum values of the age column to ensure there are no unrealistic or incorrect values . I created an AgeGroup feature by binning the age variable into meaningful categories to capture behavioral patterns across different age segments.

 

 OBSERVATIONS: I analyzed churn across different age groups using count plot and found that churn increases with age, especially in mid-age and senior customers.

	Balance Binning
I created Balance Group by binning the balance feature into four categories to better analyze customer segments based on account balance Most customers fall under the low balance category
 

 
OBSERVATIONS: I found that customers with higher account balances are more likely to churn, especially in the high and very high balance groups High balance customers are valuable, so their churn is a major business concern

	Salary Binning
I created Salary Group by binning estimated salary into four categories to analyze customer segments based on income levels Salary does not show strong variation across customers

  OBSERVATIONS : I analyzed churn across salary groups and found that churn distribution is fairly consistent across all salary levels, indicating that salary does not have a strong impact on churn

	Correlation Heatmap

•	A correlation function was used for the computation of numerical features.  
A heatmap was used to visualize relationship between variables
 
OBSERVATIONS: I used a correlation heatmap to understand relationships between features. I found that age and balance have positive correlation with churn, while active membership has a negative correlation. Most other features show weak correlation, indicating they have less impact on churn.

	Encoding 
I applied one-hot encoding to categorical variables and used drop_ first=True to avoid multicollinearity. I converted categorical data into numerical using one-hot encoding. Encoding ensures categorical features are properly used in machine learning models.
	Feature Scaling: Imported sklearn librar
For scaling, feature scaling standardization was applied
 StandardScaler from sklearn  
       Reason:  
•	To convert data into equal weightage  
•	To prepare data for machine learning algorithms  
•	To prevent large value features from dominating the model  
- Standardization dataset was converted back into Dataframe format.
OBSERVATIONS: I applied StandardScaler to normalize numerical features so that all variables are on the same scale, which helps in better comparison and prepares the data for future modeling. :After applying StandardScaler, the output was a NumPy array. So I converted it back into a DataFrame to retain column names and make the data easier to interpret.
Power BI Dashboard Architecture
		The Power BI dashboard transforms raw data into interactive, business-ready visualizations. The architecture follows best practices for data modeling, DAX measure creation, and user experience design.
	Data Loading
		Imported CSV file into Power BI using Power Query for transformation and data shaping operations
	Power Query Steps
Removed Customer Id columns, changed data types for accuracy, added calculated columns including Age Group and Balance Category bins
	Data Modeling
Created single table model with no relationships required since only one dataset is used for analysis
	DAX Measures
  Developed key measures including Total Customers, Churned Customers, Churn Rate using DIVIDE function, and Active Customers calculations.
1. Churn Rate = DIVIDE ([Churned Customers], [Total Customers])
2. Churned Customers = CALCULATCOUNTROWS ('Bank Customer Churn Prediction'),'Bank Customer Churn Prediction'[churn] = 1)
3. Active % = DIVIDE (CALCULATE (COUNTROWS ('Bank Customer Churn Prediction'),'Bank Customer Churn Prediction'[active_member] = 1, [Total Customers])
4. Avg Balance = AVERAGE ('Bank Customer Churn Prediction'[balance])
5. Avg Salary = AVERAGE ('Bank Customer Churn Prediction'[estimated_salary])
6. Total Customers = COUNTROWS ('Bank Customer Churn Prediction')
7. Active Status = IF([active_member]=1,"Active","Inactive")
8. Age Group = SWITCH(TRUE(), 'Bank Customer Churn Prediction'[age] < 30, "Young",'Bank Customer Churn Prediction'[age] < 50, "Middle","Senior”)
9. CreditGroup = SWITCH(TRUE(),'BankCustomerChurnPrediction'[credit_score] < 500, "Low",'Bank Customer Churn Prediction'[credit_score] < 700, "Medium",
"High”)
10. Risk Level DAX = SWITCH(TRUE(),'BankCustomerChurnPrediction'[active_member] = 1 && 'Bank Customer Churn Prediction'[balance] > 50000, "Low Risk", 'Bank Customer Churn Prediction'[active_member] = 1 &&'BankCustomer Churn Prediction'[balance] <= 50000, "Medium Risk", 'Bank Customer Churn Prediction'[active_member] = 0 && 'Bank Customer Churn Prediction'[balance] > 50000, "Medium Risk", 'Bank Customer Churn Prediction'[active_member] = 0 && 'Bank Customer Churn Prediction'[balance] <= 50000, "High Risk", "High Risk"
	Create KPI Visuals (Card Visuals)
KPI 1: Total Customers
•	Visual: Card
•	Value: [Total Customers]
•	Format: Whole number, no decimals
•	Value: 10000
KPI 2: Churn Customers
•	Visual: Card
•	Value: [Churn Customers]
•	Format: Whole number
•	Value: 2037
KPI 3: Churn Rate
•	Visual: Card
•	Value: [Churn Rate %]
•	Format: Percentage, 2 decimalsaqq1
•	Value: 20.37%
KPI 4: Average Balance
•	Visual: Card
•	Value: [Avg Balance]
•	Format: Currency / Whole number
•	Value: 76486
•	KPI 5: Active Customers %

	Create Charts & Visuals
	Churn Rate by Geography
•	Visual: map
•	Location: Country
•	Bubble size : [Churn Rate %]
•	Values: Germany = 32.44% , France =16.13%  , Spain =16.67%
	Churn Rate by Age Group
•	Visual: Clustered column chart
•	X-Axis: Age Group (Senior, Middle, Young)
•	Y-Axis : Count Of Customer_id
•	Legend: Churn Rate
•	Values: Senior = 45.45%, Middle = 18.37%, Young = 7.56%
	Churn Rate by Gender
      Visual: Donut Chart 
•	Legend: Gender
•	Values: Count of customer_id
•	Tool tips: Churn Rate
•	Values: Female= 25.07% , Male=16.46%
	Churn Rate by Tenure
•	Visual: Line Chart or Column Chart
•	Axis: tenure (0 to 10)
•	Y-Axis: [Churn Rate %]
•	Values: 0=23.3%, 1=18.95%, 2=16.04%, 3=13.85%, 4=9.24%
	Products vs Churn
•	Visual: Clustered Column Chart
•	X-Axis: products_number (1,2,3,4+)
•	Y-Axis :Count of Customer_id
•	Legend = Churn 
•	Insight: 1 product = highest churn
	Age vs Credit Score
•	Visual: Clustered Column Chart
•	X-axis: Credit group
•	Y-axis: Churn Rate
•	Values = Low =18.80%  , High = 16.73% ,Medium=16.47%
	Risk Level Distribution
•	Visual: Donut Chart 
•	Legend: Risk Level DAX
•	Values: Count of Customer_id
•	Values: Medium Risk  having customers= 48%, Low Risk = 27.98%, High Risk = 24.02%
	Active vs Inactive Members
•	Legend : Active Status
•	Values: count of customer_id
•	Labels: Active = 51.51%, Inactive = 48.49%
•	 Create Slicers (Filters)
Added these slicers for interactivity:
•	Geography (Germany / France /Spain)
•	Gender (Female / Male)
•	Age Group (Senior / Middle / Young)
•	Active Status (Active / Inactive)
•	Risk Level (High / Medium / Low)
________________________________________
	Visual Titles
•	CHURN RATE BY GEOGRAPHY
•	CHURN RATE BY AGE GROUP
•	PRODUCTS vs CHURN
•	CHURN RATE BY TENURE
•	ACTIVE VS INACTIVE MEMBERS
•	HIGH AND LOW RISK CUSTOMERS
 


	KEY INSIGHTS :
1.	Overall Churn Situation Around 20% customers left the bank Simple meaning: Out of every 5 customers, 1 customer is leaving Insight: This is not very high, but still a serious business problem Company needs to focus on customer retention
2.	Age is a Strong Factor Older customers have higher churn Simple meaning: Young people stay, older people leave more Why this happens: Older customers compare banks more They expect better service They may shift for better offers
3.	High Balance Customers Are Leaving Customers with more money in account having more churn Simple meaning: Rich customers are leaving more Why this is important: These are valuable customers Losing them = big financial loss.
4.	Active Member is the MOST IMPORTANT Factor Inactive customers churn a lot Active customers rarely leave Simple meaning: those customers are not using the bank servuces they are leaving the bank.
5.	Country One country has higher churn Simple meaning: customer behaviour is different in every country Why this happens: Competition Service quality Local market conditions.
6.	Gender Has Very Little Impact Male & Female churn almost same Simple meaning: Gender doesn’t matter much here.
7.	Credit Card Has No Major Impact
8.	Correlation Insight
		Most values are close to 0 Simple meaning: Features are not strongly connected Insight: No strong linear relationship No multicollinearity problem.Deep meaning: Churn depends on multiple factors together, not one single factor.
RECOMMENDATIONS:
1. Target inactive users with special offers.
2. Focus on Germany – run Germany-specific retention campaigns.
3. Increase product cross selling (1 product → 2+ products).
4. Implement loyalty programs for high balance customers.
5. Provide extra support to first-year customers (calls, offers, check-ins).
________________________________________
	MACHINE LEARNING (IF APPLIED) :
Models:
•	Logistic Regression
•	Random Forest
Steps:
•	Train-test split
•	Model training
•	Accuracy evaluation
Conclusion:
From the analysis, I found that customer churn is mainly influenced by customer engagement, age, and account balance. The most important factor is whether the customer is active or not, as inactive customers are much more likely to leave. Additionally, older customers and those with higher account balances show higher churn, indicating dissatisfaction among valuable customers. On the other hand, features like gender, salary, and credit card ownership have minimal impact. Overall, the key driver of churn is lack of engagement, and improving customer interaction can significantly reduce churn.

# Colony Event Analysis
The housing society has provided us with a comprehensive dataset named "Final_Data.csv," which contains essential information about its residents, flats, 
confirmed member and donation details. Lets begin with loading the data and getting the basic overview of data. Also, perform data quality checks by identifying missing values, 
checking the data types, finding the unique values and the descriptive statistics.

## Objective:
Our primary objective is to analyse the data that empowers the housing society to make data-driven decisions, optimize event planning, 
and ensure the efficient utilisation of resources.  By leveraging the decorator and caterer data, we aim to enhance the event experience, 
minimise costs, and maximise resident satisfaction. The selection of the best caterer and decorator based on customer satisfaction and cost-effectiveness 
will play a crucial role in achieving these goals and ensuring the success of the grand event. 
Analyze the data and gain insights for organizing the grand event find out following information with your analysis:

- Demographic Analysis
- Flat Information
- Resident Participation
​​- Owner and Tenant Information
- Donations Analysis
- Event Planning
- Decorator and Caterer Analysis

## Implementation Steps :
1. Data Loading and Overview: 
   We begin by loading the dataset, named "Final_Data.csv," into a Pandas DataFrame. We display the first few rows of the DataFrame to provide an initial
   overview of the data's structure and content.
   
2. Getting a Summary of the Dataset:
   To ensure data integrity, we perform a thorough data quality check. We examine data types to confirm that each column is assigned the appropriate data
   type (e.g., numeric, string, date).
   
3. Descriptive Statistics:
   In this step, To gain insights into the dataset's numerical features, we calculate summary statistics for numeric columns.
   
4. Count Number of Unique Values:
   Understanding the diversity and uniqueness of categorical variables is essential for event planning and engagement strategies.
   Analyze the results to understand the variety of responses and preferences among residents.
   
5. Checking for Unique Values:
   Identify the unique set of variables in the dataframe inorder to identify the unique values if any kind of discrepancy present in the data.
   
6. Checking for Missing Values:
   Identify and report missing values in the dataset, which may require data imputation or further data collection strategies.

7. Check for Duplicate Values:
   One important aspect of data quality is identifying and handling duplicated data. We utilise the duplicated() method in pandas to check
   for duplicated rows within the dataset. The sum() function is then applied to count the total number of duplicated rows. Duplicated data can
   introduce bias and inaccuracies into our analysis, so it's essential to address it appropriately.


## Building the code 
 

1. Replace "_" with NaN in the entire DataFrame

We begin by addressing missing data. In our dataset, missing values are represented as underscores. 
We'll replace these underscores with NaN (Not-a-Number) values using the replace function to facilitate further data processing.

2. Handling Missing Values: 

We identify and remove two columns, 'Unnamed: 0' and 'Owner's Spouse Name,' as they are not relevant to our analysis. Dropping unnecessary columns helps simplify the dataset.

3. Data Type Conversion: 

We ensure that relevant columns are of the correct data types for analysis. Specifically, we convert 'No of Resident' and 'Confirmed Members' 
columns to numeric data types while handling any conversion errors by setting them to NaN.

4. Impute Missing Values in 'Maintenance Amt' , ‘Flat Vacancy’, 'Donation', ‘No of Resident' , 'Confirmed Members', 'Availability of owner' and 'Origin of Owner' 

- To address missing values in the 'Maintenance Amt' column, we iteratively go through the DataFrame. For each missing value, we impute it based on the corresponding 'Flat Area (sq.mt)' 
  value. We reference a previously calculated dictionary, 'avg_maintenance_amt,' to fill in these values
- We handle missing values in the 'Flat Vacancy' column by using a conditional approach. If 'Availability of owner' is 'Yes,' we assume the flat is owned ('Flat Vacancy' is 'Owned'), and 
  if 'Availability of owner' is not 'Yes,' we consider the flat as vacant ('Flat Vacancy' is 'Vacant').
- For missing values in the 'Donation', ‘No of Resident' , 'Confirmed Members' column, we impute them with the median value of the respective column.
- Finally, we handle missing values in the 'Availability of owner' and 'Origin of Owner' columns by imputing them with the mode (most frequent value) of their respective columns.

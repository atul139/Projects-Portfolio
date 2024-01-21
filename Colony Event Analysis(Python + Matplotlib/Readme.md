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

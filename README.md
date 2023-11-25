
# Sales-RFM Analysis

The purpose of this project is to conduct a Customer Segmentation Analysis for an Automobile bike Company. Customer segmentation is performed by developing a RFM Model. RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions. In this analysis the customer segment was divided into 11 groups. The analysis will help in determining which customers segments should be targeted in order to enhance sales revenue for the company. A Sales Dashboard for Customer Segmentation is developed using Power BI and the data quality assessment and analysis is done using Python.

## PowerBI
![Uploading Customer RFM.PNG…]()

## Analysis Approach

[Analysis Approach](https://linktodocumentation)
**1. Data Quality Assessment and Data Cleaning**

The first step towards generating useful insights from the data was the data prepartion, quality assessment and data cleaning step. After the cleaning process exploratory data analysis on the dataset and identification customer purchasing behaviours to generate insights can be performed.

In the data cleaning step the data quality of the following datasets were first assesed. After a data quality assessment the following data quality issues was observed and the necessary process to mitigate the issue was followed :

**1.CustomerDemographics.xlsx :**
1 Irrelevent column was present and such columns were dropped from the dataset.

There were 5 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values

For gender column there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.

The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discripency of age distribution. An outlier was observed and the record was removed.

Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

**2.NewCustomerList.xlsx :**
5 Irrelevent column was present and such columns were dropped from the dataset.

There were 4 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values

The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discripency of age distribution.

There was no data inconsistency.

Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

**3.Transaction_data.xlsx :**
The product_first_sold_date column is not in datetime format. The data type of this column was changed from int64 to datetime format.

There were 7 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values

A new feature column 'Profit' was created which is basically the difference between list price and standard price.

There was no data inconsistency.

Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

**4.CustomerAddress.xlsx :**
For states column there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.

There were certain customer IDs from Customer Dempgraphics table which were getting dropped in the Address table.

**2. Exploratory Data Analysis on Customer Segments**

After the data cleaning process, exploratory analysis on the dataset is performed and the following insights are obtained :

**New vs Old Customers Age Distribution**

Most New customers are aged between 40-49 also for Old Customers the most of them are aged between 40-49

The lowest number of customers for both the types of customers is present in the age bracket under 20 and above 80 age groups.

The automobile company is popular among New Customers among the age groups 20-29 and 40-49.

A steep drop in customers is observed in the 30-39 age group among the New Customers

![Old Age Distribution](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/79fb1e63-e2eb-49bc-86a0-7bc5eece0047)
![Age distribution](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/1bc8bf1e-15f2-4b7f-8dc6-3b7a1d954488)

**Bike purchases over last 3 years by Gender**

Most bike puechases are done by Feamale over the last 3 years. 

Approximately 51% of the bike purchases are done by Female compared to 49% of the purchases being done by Male.

The Female purchases are 10,000 more than that of Male purchases (numerically).

![Male Vs Female](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/29fc5dee-5e59-474b-8ea6-283f6af9e558)

**New vs Old Customers Job Industry Distribution**

Most New customers are from the Manufacturing and Financial Services sector (approx 20% of the New Customers).

The lowest number of customers are from the Agriculture and Telecom sector approx 3%.

Similar trend is observed among Old Customers as well

![Industry distribution](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/e9491060-7f3f-47e6-b624-d95eb85615be)

**Wealth Segmentation by Age Category**

Across all age categories the largest number of customers are from 'Mass Customer' Segment

The next category comes from the 'High Net Worth' customers.

In the age group 40-49, Affluent segment out performs the High Net Worth customers in terms of number of customers.

![wealth by age group](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/58206107-5553-42e5-93ce-83fb535a5ff2)


**Cars owned by States**

New South Wales has the largest number of people who donot own a car.

In Victoria the proportion is quite even.

In Queensland the number of people owning a car is greater than who donot have a car.

![Car owners](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/3f8feaf7-c676-4f05-8db5-e85a2d6cd2f9)


**3. RFM Analysis and Customer Segmentation**
In this stage of analysis the customer segmentation was done by developing an RFM Model. The RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions.

In this analysis the customer segment was divided into 11 groups. The groups being :

Platinum Customers
Very Loyal Customers
Recent Customers
Potential Customers
Lost Customers
Losing Customers
Late Bloomer
High Risk Customers
Evasive Customers
Becoming Loyal
Almost lost Customers
As of the current state of the Automobile business the current distribution of customers segments is depicted below:

![Customer Segment](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/b479382f-badc-4f70-a34e-d4e5c925a7f0)


**4. RFM Analysis: Scatter Plots**
Recency vs Monetary :

The visualization shows that recent customers have purchased more products and generated relatively more revenue than the customers who visited a while ago.

![Recency VS Monetary](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/8d3aa58b-10a5-4453-bf2f-f5dcfec52c09)

Frequency vs Monetary :

The visualization shows that customers belonging to Platinum/ Very Loyal/ Becoming Loyal Customer Segments have a greater frequency and generate greater monetary for the business

![Frequency vs Monetary](https://github.com/Ahshamali/Sales-RFM-Analysis/assets/96016885/63590850-a402-4dea-93dd-5dc79861c98b)







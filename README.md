# Cafe Sales Data Cleaning Project

## Introduction
This project focuses on cleaning and preparing a transactional cafe sales dataset for data management and analysis. The data contains information about customer purchases, including transaction ID's, items, quantities, prices, total spending, payment methods, locations, and transaction dates. This raw dataset also contains many common data-quality issues, such as missing values, "ERROR" and blank entries, "UNKOWN values", inconsistent records, and incorrect or incomplete information. These issues can reduce data accuracy and lead to unreliable insights.

## The Goal
The goal of this project is to identify, clean, and standardize the dataset while preserving the integrity and validity of the original information. The clean dataset can then be used for further analysis, visualization, and business insights to uncover purchasing patterns, product popularity, spending habits, and payment preferences. 

## Tools Used
- Microsoft Excel

## Raw Dataset Preview
<img width="800" height="500" alt="Screenshot 2026-09-09 152553" src="https://github.com/user-attachments/assets/2e510848-3ed9-4c90-89bb-97e4db87a926" />

## My Approach
### 1. Formatting the Data and Identifying the Issues
First and foremost, it is important to format the dataset as a table, as this allows me to organize the data clearly, making it easier to sort, filter, and identify inconsistencies without disrupting the existing structure.  In addition to the obvious "ERROR", "UNKNOWN", and blank entries, I also noticed that the Price Per Unit and Total Spent columns are not formatted as currency. I further noticed that the Price Per Unit column contains values of 0, which is not possible and should be reviewed for accuracy. To make the missing information more noticeable, I highlighted all blank entries in yellow. 

<img width="800" height="500" alt="image" src="https://github.com/user-attachments/assets/48fad8cf-94ad-4415-be6a-2b67745baad4" />



### 2. Standardizing the Data
I replaced all "ERROR", "UNKNOWN", and blank entries with "NA" to ensure that the data is presented more consistently and clearly, making it easier to interpret. I also replaced all "0" entries entries in the Price Per Unit column with "NA", since a price of $0.00 is not possible and would be considered invalid data. Secondly, I converted the Price Per Unit and Total Spent columns into currency format because they represent monetary amounts. Using a consistent currency format makes the financial information more professional and easier to understand. 

<img width="800" height="500" alt="image" src="https://github.com/user-attachments/assets/9af71147-0d61-4dd3-a562-70c731e825bc" />




### 3. Handling the NA Entries
Now, it is important to note that all "NA" entries in each column should not be treated the same way. Guessing missing values could reduce the accuracy and quality of the dataset. Instead, each blank "NA" should be evaluated and based on the column and whether the missing information can be reliably determined from the other available data.

For the Transaction ID, Item, Payment Method, Location, and Transaction Date columns, it would be best to leave the "NA" entries unchanged to preserve the integrity and accuracy of the dataset. For the Quantity, Price Per Unit, and Total Spent columns, I created Clean columns to correct the missing entries when they could be calculated from the available information. For example, if Quantity and Price Per Unit were available but Total Spent was "NA", I calculated Total Spent by multiplying Quantity x Price Per Unit. Similarly, if Quantity and Total Spent were available but Price Per Unit was "NA", I calculated Price Per Unit by dividing Total Spent / Quantity. The same approach was applied to the Quantity column when the other two values were available.

<img width="1526" height="736" alt="image" src="https://github.com/user-attachments/assets/84a9619e-9fba-4a0c-9f42-6f97c9024dab" />







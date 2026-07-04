# HR ANALYTICS #
## Data Cleaning ##
### What I Observed ###

I noticed the data was so rough, the columns are not in the right data type, there were duplicates, there were extra spaces and some of the data were not consistent.
### What I did ###
I started with duplicating the dataset,removed duplicates, Changed the whole data type,create a table and named it.

For the Department Code, I created another column and I used the UPPERTRIM Function to trim and also change everything to capital Letters, I renamed it and I hid the previous Dept code

Hire Date: I used Text to Column to change it to Date, I formatted it to Month-Day-year, after that, I changed the data type to short date. 

Salary: I used Text to Columns to change it to General and change the date type to Currency, I removed it from decimal points and make it a whole number. I also removed the blank spaces in the column.

Employment Status: I used the TRIM function to trim the extra spaces and used Find and replace to replace to standardize it.

## The transformation I applied ###
From the project, I was asked to create some columns like Full name, Department Name, Year of service, Performance Band, and Eligible Bonus amount. 

Full Name: I inserted a column beside Last name and I named it full name, I merged both first name and the last name together using the Trim Function, after merging it togther, I copied the full name and I pasted it again as values so as to delete the first name and the last name. 

Department Name: I created another column and named it as Department name, I used Vlookup Function to merge the departmment
 
Year of service: I was asked to calculate duration from hire date to today, I used the DATEDIF function to calculate the year of service, i changed the data type to numbers.

Performance band: I used IFS function to get the performance band. There is a performance score in the dataset, so if the Performance score is higher then 95, it should be outstanding, if the performance score is  higher than 85, it should be Exceeding, if the performance score is above 70, it should be Achieving, it it is  higher than 50, it should be Developing but if it is lesser than 49 then it should be less improvement.

Eligiblle bonus amount: There is a bonus amount that 


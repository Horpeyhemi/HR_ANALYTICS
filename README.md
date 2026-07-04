# HR ANALYTICS #
## Data Cleaning ##
### What I Observed ###

I noticed the data was so rough, the columns are not in the right data type, there were duplicates, there were extra spaces and some of the data were not consistent.
### What I did ###
I started with duplicating the dataset,removed duplicates, Changed the whole data type,create a table and named it.

For the Department Code, I created another column and I used the UPPERTRIM Function to trim and also change everything to capital Letters, I renamed it and I hid the previous Dept code

Hire Date: I used Text to Column to change it to Date, I formatted it to Month-Day-year, after that, I changed the data type to short date. 

Salary: I used Text to Columns to change it to General and change the dat type to Currency, I removed it from decimal points and make it a whole number. I also removed the blank spaces in the column.

Employment Status: I used the TRIM function to trim the extra spaces and used Find and replace to replace to standardize it.

## The transformation I applied ###
From the project, I was asked to create some columns like Full name, Department Name, Year or service, Performance Band, and Eligible Bonus amount. 

Full Name: I inserted a column beside Last name and I Names it full name, I merged both first name and the last name together using the Trim Function, after merging it togther, I copied the full name and I pasted it again as values so as to delete the first name and the last name. 



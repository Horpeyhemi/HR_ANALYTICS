# HR ANALYTICS #
## Data Cleaning ##
### What I Observed ###

The raw Data was messy:
1) Wrong data types in Columns
2) Duplicates Records
3) Extra Spaces
4) Inconsistent data entries
### What I did ###
I cleaned the dataset by:
Duplicated the dataset, removed duplicates, converted to Table and named it.

Department Code: Created another column and I used the UPPERTRIM Function to trim and also change everything to capital Letters, renamed it and hid the previous Dept code.

Hire Date: Used Text to Column to change it to Date, formatted it to Month-Day-year and changed the data type to short date. 

Salary: Used Text to Columns to change it to General, change the date type to Currency,removed it from decimal points,and used IF and Median to fill the blanks spaces in the column and names it "Estimated Median Salary"

Employment Status: Used the TRIM function to trim the extra spaces and used Find and replace to standardize it.

## The transformation I applied ###
From the project, I was asked to create some columns and name them Full name, Department Name, Year of service, Performance Band, and Eligible Bonus amount. 

Full Name: Inserted a column beside Last name and named it full name, merged both first name and the last name together using the Trim Function, after merging it togther, I copied the full name and pasted it again as values so as to delete the first name and the last name. 

Department Name: Created another column and named it as Department name, used Vlookup Function to merge the departmment
 
Year of service: I was asked to calculate duration from hire date to today,used the DATEDIF function to calculate the year of service and change the data type to numbers.

Performance band: Used IFS function to Categorize base on performance score.
> 95= Outstanding
> 85= Exceeding
> 70= Achieving
> 50= Developing
< 49= Needs Improvement.

Eligible bonus amount: There is a bonus amount that is for people that have a particular performing score, Used IFS Function to Assign bonus based on score:
> 95= 0.12
> 85= 0.08
> 70= 0.05
> 50= 0.02
< 49= 0

Created another column and named it Left/Resigned Band:Used If(OR) Function,0 IF employee left, 1 if employee is still active.

Another Column named Left Band:Used the column to track those that resigned, I classified Terminated, resigned or Retired as Left because they are no longer a staff in the company. I used IF Function to sort it, so that resigned staff will also be classified as "Left" instead of not appearing in the analysis.

Bonus Paid: Estimated Median Salary * Eligible Bonus Amount 

## Issue Encountered ##
After Merging the first name and the last name, I deleted the first and the last name but I noticed the full name that I merged vanished so I had to undo it, I copied and pasted it as Formula and deleted the first and the last name, it was still the same, I ended pasting it as values.  

For Department Code; After creating another columnn and using the UPPER(TRIM) Function, I deleted the previous dept code but the second one I did vanished too and I didnt want to paste it as values because we were asked to show our formulas, so,I hid the previous Department Code. 

After inserting another column while doing the pivot tables, my pivot table didnt bring the new column I added, it took a while before I knew that I could refresh the pivot table

## Insight ##
![image alt](https://github.com/Horpeyhemi/HR_ANALYTICS/blob/8df276dae6d19dc545c08eb08e22953b9170434e/ANALYTIC%20DASHBOARD.png)


 The performance and the Eligible bonus Amount shows those that have high performing score are rewarded excellently. Employee in the Outstanding band collected the highest bonus Amount.

 Attrition Analysis: Using the Left band column, It is easier for us to know the number of staff that left each department.

 With the year of service calculated, we can see the year of experience; majority of staff have more than 2 years of experience.

 The IT (Information Technology) department has the highest paying average salary, followed by Finance, this suggest that the company invested well im technical and financial roles than other departments.

 The Sales department has the highest headcount but not the highest average salary.



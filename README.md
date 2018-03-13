Before beginning to work on any of the following questions first exclude all rows where:
•	The school is designated as a foreign institution or a proprietary institution.
•	Answer:  To consider these conditions I first set a Data filter for Row 6.  I’m interested in filtering Column E “School Type” to exclude all options only leaving Private-Nonprofit and Public selected.  
•	The school's zip code does not contain 0.
•	Answer: I created a new column to figure our whether Column D “Zip Code” contains 0 or not. I performed a google search to how I can search for a string in a cell and found out we can use ISNUMBER function.  I created a new column and created the following formula: =ISNUMBER(SEARCH(0,D7)).  If the zip code contains a 0 then my formula will yield a “False” result and if the zip code contains the number 0 my formula will yield a “True” result.  I drag my formula down through the entire column to yield the results.    Once we have the results we can filter for True to give us all the schools whose zip code does not contain 0. 
QUESTION 1
Please provide your answer as a number.
How many schools had disbursed a total of greater than or equal to $707,300 and less than $800,895 in loans for the time period reported on the spreadsheet provided (“Quarterly Activity” only)?
•	Answer: 55
Explanation:
Before finding number of schools I will have to find total $ of Disbursements by each school.  To do that I need to write a formula to calculate the following. 
1.	DL SUBSIDIZED: $ of Disbursements
2.	DL UNSUBSIDIZED: $ of Disbursements
3.	DL UNSUBSIDIZED- GRADUATE :  $ of Disbursements
4.	DL PARENT PLUS : $ of Disbursements
5.	DL GRAD PLUS: $ of Disbursements
I inserted a new column for calculating this and write a formula for getting sum of all disbursements.
=SUM(L265,Q265,V265,AA265,AF265).
I pasted this formula in each cell of the column.  To filter out the range for this question I used a custom filter (Click on Number Filter->Custom Filter).  My selection is as follows:
 “is greater than or equal to” = 707300 And “is less than” = 800895
This filter returns 55 results.




QUESTION 2
Please provide your answer as a number.
Consider the sum of expected total loan amount if the loans were fully disbursed for each school in this Quarter. For how many schools was this amount greater than $20,000,000?
Answer: 67
•	I use the same Column which I created for Question 1.  This time we’ll set the custom filter to “Greater Than..” to 20000000.  This filter returns 67 results.

QUESTION 3
Please provide your answer as a number.
Amongst the schools that are considered part of Bellevue, WA (according to zip codes on http://zipcode.org), what was the largest number of recipients within a school for either DL Unsubsidized Undergraduate or DL Unsubsidized Graduate loans? Ignore unavailable data i.e. data with ‘-’ value.
Answer : 219
1.	For Bellevue School we’ll set filter ZIP code to starting with 98007 which is 980076484.
2.	Comparing Unsubsidized Undergraduate (219 recipients) and DL Unsubsidized Graduate loans recipients (not available), Largest number of recipients is 219.

QUESTION 4
Please provide your answer as a number.
Consider the state in which the last Olympics was hosted in the USA. What is the sum of the expected total loan amount if the loan is fully disbursed for DL Subsidized loans in the public schools in this state in Q4 of 2016-2017, based on the data provided?
Answer: UT $10291063
This question does not specify which Olympics to consider (Summer Games or Winter Games).   If Summer Olympic is considered, then it’s GA State. If Winter Olympic is considered the it’s UT State.  My answer will be given for UT because by date (2002) it is the most recent.  
Explanation:
1.	First Filter for Public Schools. 
2.	Then Filter for State: UT.
3.	For Total amount for DL subsidized loans we’ll take a sum of Column L ‘$ of Disbursements’.



QUESTION 5
Please provide your answer as a number.
Consider all the private nonprofit schools in WA state where the name of the school starts with either “s”, “u”, “v” or “w”. For these schools, consider the expected total loan amount if the loan is fully disbursed for unsubsidized undergraduate studies. Exclude all schools where the unsubsidized undergraduate loan amount is not available i.e. “-” or 0. What was the median value?
Answer: $925,329.29 
1.	First Filter for state as WA then filter for private nonprofit schools.
2.	Then select the school starts with either “s”, “u”, “v” or “w”.
3.	We need median which is average of total unsubsidized undergraduate loan amount.
4.	We use AVG formula to get median.

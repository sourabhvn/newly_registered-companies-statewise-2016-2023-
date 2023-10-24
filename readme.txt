Hi, I am Sourabh Navaratna. I am a data enthusiast who loves to analyse the data.Below is my own case study using the dataset number of new companies registered from 2016-17 to 2021-22 from the Government of India Open dataset source.

-- Problem statement

Analysing the distribution and growth trend of registered companies across different states in India over the years 2016-17 to 2021-22 and the beginning of the year 2022 till April

1)Identify which states have the highest cumulative number of registered companies by 2021-22.
2)Analyze the yearly growth trend of registered companies in major states.




Tools used- Spreadsheets/Googlesheets

--Data Processing
Importing the dataset into the google sheets.

Using the COUNTA() function in a new column to ensure there are values for each year in each state.
=COUNTA(B2:H2)(Drag the formula to all rows in the column). This formula counts the number of non-blank cells in the range B2 to H2 which corresponds to the data for one state across all the mentioned years.
Since we have 7 different columns for each state our result should be 7 for each state else we have null values in our column.

We can also use conditional formatting to highlight blanks visually.
If any blank cells are found, AVERAGE() can be used if you decide to fill them with an average.

Adding a new column which will hold the data of total number of registered companies from 2016-17 to 1.4.22 to till date
Using the sum() function to calculate total number of registered companies for each state,



-- Analysis phase

Calculating the yearly growth rate each each from 2016-17 to till date we use the formula:
 =((Current Year - Previous Year)/Previous Year)*100

Now creating a new column with header Rank to rank all the states based on the sum of registered companies from 2016-till date.
use the =RANK.EQ(I2,I2:I38,0) formula and apply to the whole column.

Now based on the rank highlight the top 5 and bottom 5 states using conditional formatting.

select the states column and go to condtional formatting select custom formula and enter
=$J2<=5. this will check all the ranks less than or equal to 5 and highlight green.
Similarly highlight the bottom 5 states with red.

Now we visualise the data using charts.
We use the line chart to Observe the trend of registrations for a specific state or a set of states over the years.
Next we use a pie chart to visualise the percentage share of newly registered comapnies bewteen the states.

From the Data Analysis we found out that Maharashtra,Delhi,Uttar Pradesh,Karnataka and Tamil Nadu are the top 5 states having the number of newly registred companies.
Maharashtra achieved its highest yearly growth rate of newly registred companies of 23.69% in the year 2020-21.
Himachal Pradesh registred highest yearly growth rate of whooping 66% in the year 2020-21.




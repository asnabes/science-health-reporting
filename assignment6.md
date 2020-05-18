# <div align="center">Assignment 6</div>
**Questions**
1. Which racial or ethnic group saw the largest change in unemployment rate from February to April?<br />
Hispanic and Latino U.S. residents saw the biggest increase in their unemployment rate (a 14.5 percentage point change) from February to April. White (11.1 percentage point), black (10.9 percentage point) and Asian (12.0 percentage point) U.S. residents had similar increases in their unemployment rates. 
<br />Attribution: [A Reuters article](https://www.reuters.com/article/us-health-coronavirus-usa-jobs/how-the-coronavirus-job-cuts-played-out-by-sector-and-demographics-idUSKBN21M0EL) that talks about “job losses” inspired me to think of the change in unemployment rate and not just the unemployment rate itself. 
1. What was the change in the teenage unemployment rate from February to April, and how does it compare to the changes in the adult men and adult women unemployment rates from February to April? (I would compare the change in the teenage unemployment rate to the change in the overall adult unemployment rate, but the table in the PDF split up the data for women and men.)<br />
The change in the teenage unemployment rate was 20.9 percentage points. The change in the adult men unemployment rate was 9.7 percentage points, and the change in the adult women unemployment rate was 12.4 percentage points. Therefore, the teenage unemployment rate increased more than the adult women and men unemployment rates. 
1. How would one rank different education levels by unemployment rate in April?
    1. People without a high school diploma (21.2%)
    1. High school graduates who did not attend college (17.3%)
    1. People who have an associate degree or who attended college, but did not graduate (15.0%)
    1. People with a bachelor’s degree or more (8.4%)

**Data cleaning**
1. In Excel, I deleted a row that described the table and said how the numbers were in thousands, except for the unemployment rates (I wrote the “except for the unemployment rates" part). I also deleted a row that explained how Hispanics and Latinos could belong to any race. 
1. In R, I ran library(readr) and library(dplyr). I also imported the csv file and saved it as a dataframe called unemployment.
1. I deleted the “Employment status,” “Unemployment rates,” “Reason for unemployment,” “Duration of unemployment,” “Employed persons at work part time,” and “persons not in the labor force” rows, as they contained NA in most of their columns. These rows just contain titles for different parts of the table. I used the na.omit() function to delete these rows. 
1. I deleted the “……..” in each of the category names in the csv file in Excel. 
1. I changed the names of rows 12 through 24 and 31 through 34 of the original table. Since I deleted the titles of these sections, the names of the rows were not specific enough. For example, “White” is not a good row name. I changed it to “White unemployment rate.” There were other sections of the table where I did not change the row names. These rows (such as row 26 in the original table) have pretty straightforward names, so it’s not necessary to include the title of the section in those row names. 
1. There was a weird symbol that appeared in the place of the apostrophe in “bachelor’s," but when I re-wrote the row name, “bachelor’s degree and higher,” in step 5, the symbol was replaced with an apostrophe. 
1. I created a new column with values that are equal to the Apr. 2020 column minus the Feb. 2020 column. To do this, I used the mutate() function, which I learned from Codecademy. Specifically, I wrote this:
unemploymentv3 <- unemploymentv2 %>% <br />
	mutate(‘April 2020 – February 2020’ = ‘Apr. 2020’ – ‘Feb. 2020’)
1. I created a new dataframe called unemploymentv4, which contains rows 18 to 21 of unemploymentv3. unemploymentv4 shows the unemployment rates for different education levels and the changes in unemployment rates from March to April and from February to April for different education levels. 

**Headline and nutgraph**<br />
Headline: **Hispanic and Latino unemployment rate increases by 14.5 percentage points from Feb. to April**
Nutgraph:<br /> 
The unemployment rate for Hispanic and Latino U.S. residents reached 18.9% in April, which is the highest unemployment rate of the ethnic and racial groups listed in [a Bureau of Labor Statistics table](https://www.bls.gov/news.release/pdf/empsit.pdf). 14.5% of Asians, 16.7% of black or African Americans and 14.2% of white people were unemployed in April, according to the Bureau of Labor Statistics data. Hispanics and Latinos saw the largest increase in their unemployment rate from February to April — a 14.5 percentage point rise. 

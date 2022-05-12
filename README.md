# kickstarter-analysis
Performing an analysis on Kickstarter Data to uncover trends 

## Overview of Project
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Crowdfunding has become an increasingly popular method of raising capital for projects amongst entrepreneurs, this project aims to examine global kickstarter campaigns utilizing captured data (2009-2017) to uncover trends related to the preforming arts, more specifcally plays.

### Purpose

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; To employ the use of excel visualization tools and formulae to organise the data into a 
user friendly format that is easy for the customer (Louise) to extract information at a glance based on the relationship they hold specific to individualized parameters (e.g. launch dates and funding goals) and provide insights into trends that may be of beneficial use within future projects.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The focus of this analysis was to examine the count of theatre outcomes as related to their launch dates, in order to do so the following steps were taken: 
   1. Firstly, the Kickstarter dataset needed to be organized. This was accomplished by creating a “Years” column and extracting its data from the "Date_created" column. This in turn was derived from the "launched_at" column that had to be converted from Unix format to a readable date, providing further clarity into the individual campaigns' launch date
   2. Next, a pivot table was created utilizing the entire data set. Filtering by “parent category” and “years”, rows to represent “date_created" and populating the columns and values alike with “outcomes”.
   3. The pivot chart was then ammended to discard the outcomes of all current live campaigns, and filtered to show data feilds pertaining solely to "theaters" and lastly altered to display the information monthly instead of quarterly.
   4. Finally, after the data was sorted, a line graph was created to visualize the data from the created pivot table, so the relationship between theater campaign outcomes based on their launch month could be presented and understood at a glance.


![](resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The focus of this analysis is to view the percentage of successful, failed and canceled plays based on the funding goal amount. TO accomplish the aformentioned, the following steps were taken:
   1. A new table created on a new sheet aims to capture the outcomes in relation to the campaign funding goals, which were subdivided into 12 groupings, ranging from < $1,000 up to > $50,000. 
   2. The COUNTIFS function was then utilized to capture the outcome and goal data specifically for the “plays” subcategory in order to illustrate "the count" of successful/failed/cancelled outcomes
   3. The "SUM" function was then employed on the basis of the count to capture a total where then a simple percentage formula was calculated and line chart created to visualise the numerical data.

An analysis of outcomes based on goals was charted using a line graph (as seen below) and examined to reveal some interesting facts:

1. the lower the target goal the higher the chance of success 

2. as target goals increased the chances of faliure did too indicating an inverse relationship between the two
 
3. chances of faliure and success coincided at 3 distinct points implying a 50% likelihood of eaither faliure or success

4. Interestingly enough there was a far higher chance of success when fundraising for a kickstarter in the range of $35,000-$44,999 as compared to faliure though the total number of projects sampled in that range were quite minimal and so this sample subset examined may not be accurately indicative of what may actually happen if applied to the population, if everyone were to start fundraising with that goal in mind.

![](resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Most of the formulae and scripting used within this project were items that ive had a great deal of personal experience in, thoughh I'm able to understand how some of my peers had troubles in the following:
- typing/using the correct formulae in order to achieve desired goals whether it be the function use itself or the syntax of the formula
- Not fixing reference tables and receiving #N/A result errors
- pivot tables not being assigned their correct headers/values 

Personally two "errors" I encountered were with regards to the Vlookup function as well as nested if formulas:
- When using Vlookup/nested "if"/COUNTIFS to fill in subcategory statistics as well as relavent feilds within the master data set and Ouctomes based on Goals sheet, unfamiliarity of the sytax in which it should have been written led me through a couple iterations of troubleshooting


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;An analysis of outcomes as determined relative to the theatres launch date, revealed that there was a relatively low likelihood of cancellation thorough out the year (as depicted by the yellow line at the bottom of the graph). Examination of the blue and red line graphs (indicating chances of success and failure respectively) appeared to move together with the highest chnace of success compared to failure seeming to be present during the spring/summer months. While this relationship maybe causal due to the effect of a more pleasant climate, we cannot assume so as a correlative link might also exist since the spring/summer months indicated a general higher average of hosted events and so inherently presents with a higer average of successful/failed outcomes.

- What can you conclude about the Outcomes based on Goals?

An analysis of outcomes based on goals was charted using a line graph (as seen below) and examined to reveal a few interesting facts as below:

   1. the lower the target goal the higher the chance of success 

   2. as target goals increased the chances of faliure did too, indicating an inverse relationship between the two
 
   3. chances of faliure and success coincided at 3 distinct points implying a 50% likelihood of eaither faliure or success

   4. Interestingly enough there was a far higher chance of success when fundraising for a kickstarter in the range of $35,000-$44,999 as compared to    faliure though the total number of projects sampled in that range were quite minimal and so this sample subset examined may not be accurately indicative of what may actually happen if applied to the population should everyone start fundraising with that goal in mind.

- What are some limitations of this dataset?
  - not enough data points amongst higher set goals to be able to apply what we see in this data set to the greater population in order to gain a greater understanding of the nature of success specifically pertaining to plays, it would be advantageous to gather data from a variety of other sources to draw a far more accurate conclusion.
  
- What are some other possible tables and/or graphs that we could create?
  - A boxplot would be efficient to see any outliers in the data set so that they maybe ommitted when making our final conclusions
  - Outcomes by country could be an alternative table that maybe used for kickstartes that are region specific and could help provide more insights in terms of geographical disparities
  - Outcomes in relation to number of backers (i.e. a greater number of backers would likely imply a greter chance of success) would be insightful

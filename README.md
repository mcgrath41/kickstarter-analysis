# Kickstarting with Excel

## Overview of Project

### Purpose

Statistical analysis of 4,000 kickstarter campaigns via Excel to put into perspective the failed kickstarter campaign for Louise's play, Fever.  

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

After filtering the dataset to include only theater-related campaigns, we can better understand if a theater campaign's launch date has any impact on its perfomrance. This was completed by grouping these campaigns by the month in which they were launched and by outcome via PivotTable. The following Line Chart was then created to better visualize this tabular data:

![](/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

Next, we filtered down a step further to only include "plays" within the parent category "theater" to analyze how campaigns directly-related to that of Louise's play, Fever, have fared. These campaigns were grouped by Goal amount and by outcome which allowed us to calculate the success-rate of kickstarter campaigns for plays of similar sizes/expectations. To visualize this analysis, a second Line Chart was then created which can be found below:

![](/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

The only significant challenge pertained to the Theater Outcomes by Launch Date analysis. The launch dates provided in the dataset were in Unix timestamps. To complete the analysis, these timestamps had to be converted into a day-month-year format via the formula:

`=(((J2/60)/60)/24)+DATE(1970,1,1)` 

where J2 was the first cell in the Launched_at column. This enabled us to interpret the outcomes by month and include a filter for Years (via the `Year()` function) in the PivotTable.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  1. Overall, the launch date of theater kickstarter campaigns does not appear to have any impact on the outcome. As evidenced in the screen shot, the ratio of successful to failed campaigns is relatively the same throughout the year. 
  2. However, if we filter the "Years" to 2016 only, we can see that in the month of June there were nearly the same amount of successful & failed campaigns. Given that the campaign for Louise's play, Fever, was launched in June of 2016, the chance of success based on time frame alone could be assumed to be as low as 50%.  

- What can you conclude about the Outcomes based on Goals? 

  1. As one would expect, campaigns with lower goal amounts are more successful campaigns than those with higher goal amounts. 73% of campaigns with goal amounts similar to that of Louise's play, Fever ($2,885), were successful. 

- What are some limitations of this dataset?

  1. Some limitations of the dataset include different currencies, lack of recent data (post-2017), and existence of outliers. 

- What are some other possible tables and/or graphs that we could create?

  1. Other possible tables and/or graphs we could create include average donation vs. category, a box plot of Percentage Funded, and/or length of time of each campaign.  

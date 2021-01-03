# Kickstarting with Excel

## Overview of Project
Louise is an up-and-coming playwright looking to start a crowdfunding campaign to fund her play Fever. She has estimated a budget of over $10,000. I will be using excel to organize, sort, and analyze crowdfunding data to determine if there are specific factors that can make a campaign successful. Analyzing this data, will allow Louise to mirror other successful campaigns to thereby, increase the success of her own crowdfunding campaign.  

### Purpose
Louise’s play Fever came close to its fundraising goal in a short amount of time. The purpose of this analysis is to determine how different campaigns fared in relation to their launch dates and their funding goals. This analysis will in turn provide insight as to what to expect in regards to Louise’s play Fever and the direction Louise should follow to increase her odds at a successful campaign. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
In Deliverable 1, to visualize the campaign outcomes (successful, failed, and canceled) against the launch date, I used a pivot table. I filtered the column labels to show only the three “successful”, “failed”, and “canceled” outcomes. I filtered by Parent Category (to select “Theater”) and Years (extracted through the Year() function). I set my columns to be the outcomes and rows to be the Date Created Conversion (showing only the month of the Launch Date). The values of the pivot table were the count of the outcomes. Using this data, I created a line chart (as seen below) to visualize the correlation between the Launch date seen on the x-axis and the Outcome count seen on the y-axis. Looking at the chart, there is a significant peak of 111 successful theater campaigns in May. 

![image1](https://github.com/Soniaprogram/kickstarter-analysis/blob/main/resources/Theater_Outcomes_vs_Launch.png?raw=true)

### Analysis of Outcomes Based on Goals
In Deliverable 2, I visualized the percentage of successful, failed, and canceled plays based on the funding goal amount in the form of a line chart. In order to do this, I first created a table of the Funding Goal, Number of Successful, Failed, and Canceled projects, Total Projects, and Percentage of Successful, Failed, and Canceled projects. I used the COUNTIFS() function to specify “successful”, “failed”, and “canceled” outcomes, the goal amount, and the subcategory of “plays”.
I used the SUM() function to populate the Total Projects column and calculated the percentage by dividing the Number Successful, Failed, and Canceled by the Total Projects. I was then able to select the percentage columns and Goal column to plot the relationship between goal amount ranges on the x-axis and the percentage of successful, failed, or canceled projects on the y-axis. Based on the line chart (as seen below), the highest percentage of successful plays occurred with a goal of less than $1000. On the contrary, the highest percentage of failed plays was 100% which occurred with a funding goal of $45,000-$49,999.

![image2](https://github.com/Soniaprogram/kickstarter-analysis/blob/main/resources/Outcomes_vs_Goals.png?raw=true)

### Challenges and Difficulties Encountered
A challenge I faced during my analysis, was correctly implementing the COUNTIFS() function in the second deliverable. I found this function to be a bit of a challenge as syntax is very important. Firstly, it is important to specify the correct range for the goal amount, the correct subcategory, and outcome. Secondly, it is important to add the ‘$’ if copying the formula to other cells to keep the cells constant. If you do not pay attention, it could be very easy to miswrite the formula which could lead to flawed data. 
For example to set the COUNTIFS() function for Number Successful with a Goal of less than 1000, and the subcategory of “plays”, it would look like: =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"=successful",Kickstarter!$R:$R,"=plays")

## Results

###### What are two conclusions you can draw about the Outcomes based on Launch Date?
- Looking at the line chart, there is a significant peak of 111 successful theater campaigns in May. I can draw the conclusion that it would be most beneficial to launch a campaign in May. Furthermore, the second conclusion is that the failed plays do not vary much based on launch date, implying that there is another factor that affects this outcome more. 

###### What can you conclude about the Outcomes based on Goals?
- Based on the line chart, the highest percentage of successful plays occurred with a goal of less than $1000. On the contrary, the highest percentage of failed plays was 100% which occurred with a funding goal of $45,000-$49,999. It would be beneficial to aim for a goal less than $1000 and not within the $45,000-49,999 range.

###### What are some limitations of this dataset?
- This dataset does not specify the genre of plays which would also allow us to see why some plays were successful or more popular over others. It would also be beneficial to see the publicity methods adopted by successful campaigns versus failed campaigns to see if there is a correlation there. 

###### What are some other possible tables and/or graphs that we could create?
- With the current data set, we can create a table and line graph to show the duration of the campaign and its correlation with the Outcome (success or failure) of the campaign. It would also be interesting to see the correlation of spotlight and the Outcome of the campaign. 

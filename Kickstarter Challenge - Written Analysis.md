# Kickstarting with Excel

## Overview of Project
In this analysis I have examined data from Kickstarter campaigns in order to determine which factors result in the most favorable campaign outcomes.  My analysis focuses on criteria such as launch date, campaign goal, category of the campaign, and location of the campaign.  I have compared these criteria to the outcomes of the Kickstarter campaigns to best illustrate what factors make a campaign successful.

### Purpose
The purpose of this project is to provide the client, Louise, with an analysis of successful theater-related Kickstarter campaigns.  Louise is interested in launching a Kickstarter campaign to fund a theater project, and our goal is to provide her with the insights necessary to oversee the most successful campaign possible.  The insights gleamed from this analysis will allow Louise to make informed decisions regarding launch date, campaign goal, and location of the campaign. 

## Analysis and Challenges
My analysis began with an examination of the data to determine which information needed to be converted in order to be read easily by humans.  Once I had formatted the data so that it was easily readable, I added conditional formatting in order to quickly identify trends in the data.  I then noted that launch date and campaign goal were two criteria that warranted further analysis.  Next I used Pivot Charts to visualize the relationships between these criteria and the outcome of the campaign. 

### Analysis of Outcomes Based on Launch Date
I began my analysis of Outcomes Based on Launch Date by creating a new column in my worksheet corresponding to the year the campaign was launched.  Then I created a line chart that illustrated which months yielded the most successful campaigns each year.  In order to view the outcomes of campaigns based on their launch date, I filtered my chart to display only theater campaigns for all years. With those filters in place, I used this line chart to visualize the relationship between month launched on the x-axis and number of outcomes on the y-axis.  Through an analysis of this line chart I was able to determine that May and June are statistically the best months to launch a campaign, while December and January are the worst.  I also noted that theater campaigns are more likley to succeed than fail regardless of when they are launched. 

![Theater_Outcomes_vs_Launch](/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
In order to perform an analysis of Outcomes Based on Goals, I first determined the range of goals I wanted to examine.  With my ranges in place, I then used the COUNTIFS function to calculate the number of successful campaigns, failed campaigns, and canceled campaigns.  I noticed here that my values were higher than expected and began to add more filters to my formula.  Once I added a criterion for the subcategory "plays", I was able to get the correct result.  Next I calculated the total projects in order to determine the percentage of successful, failed, and canceled campaigns.  Using these values, I created a line chart in order to visualize the relationship between successful, failed and canceled campaigns in each range of goals. Upon initial examination of the chart I deduced that campaigns are more successful when the goal is low, and campaigns failed more often when the goal is high.  I also noted that goal ranges that contained many Kickstarter campaigns tended to have a lower variance than goal ranges which contained very few Kickstarter campaigns.  For example, Kickstarter campaings that have a goal range of $45000-$49999 appear to fail 100% of the time.  However further investigation shows that only 1 campaign was launched with a goal in this range.  Additional analysis of outliers may be required in order to provide a more accurate assessment for our client. 

![Outcomes_vs_Goals](/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
I ran into several obstacles during my analysis.  I frequently encountered errors when trying to create any formula which required several arguments.  I had a particularly hard time using the COUNTIFS function to analyze the relationship between campaign goal and the success of a campaign.  I was able to successfully execute the function for the first data range, which is "less than 1000".  Once the function required two integers in the data range, my formula no longer functioned correctly.  I was able to identify the error because my PivotChart did not match the example included in our module.  I then began to work backwards and rearranged my formula to see how it affected the chart.  After some trial and error, I realized that I had not included "greater than or equal to" in my formula.  With the cause of my error identified, I was able to edit my formulas in the rest of the chart to achieve the correct result. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  - The first conclusion I was able to draw is that campaigns launched in May are most likely to succeed, while campaigns launched in December are least likely to succeed.  Another important conclusion is that theater campaigns are more likley to succeed than fail regardless of when they are launched.  Campaigns launched in December have the smallest variance, meaning these campaigns are almost as likely to fail as they are to succeed.

- What can you conclude about the Outcomes based on Goals?
  - I have concluded that campaigns with a low goal are more likely to succeed, while campaigns with high goals are more likely to fail.  I also noted that there are very few campaigns with goals ranged $25000-$49999, therefore the variance between percentage successful and percentage failed is larger. 

- What are some limitations of this dataset?
  - One limitation of this dataset is that the data does not include efforts made by the entity or individual to promote their campaign.  I would be interested to see data on the size of the audience each campaign was shared with.  Another interesting metric would be to see if any of these entities promoted their campaigns using paid advertisements.  This would allow me to determine if a campaign failed because their goal was too high, or if it failed because the entity did not share the campaign with a large enough audience. 

- What are some other possible tables and/or graphs that we could create?
  - One table we could create is a bar chart which illustrates the relationship between successful campaigns and the percentage funded.  This would allow us to not only provide Louise with insights on successful campaigns, we can also provide her with suggestions that would help her exceed her goal.  Another table we could create is a line chart which illustrates the relationship between the length of a campaign and the campaign outcome.  In order to build this table, we would first have to determine the length of time between the launch date and the campaign deadline.  Then we could compare the lenghths of the campaigns with their outcomes to determine if short campaigns or long campaigns are more successful.

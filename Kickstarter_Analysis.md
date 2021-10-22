# Kickstarting Analysis

## Overview of Project
Louise's play, Fever, had reached its goal in a short amount of time. In order to determine how different campaigns fared in relation to their launch dates and their funding goals, Louise wants to assemble and observe whether the launch dates and the funding goals affect the outcome of other theater productions.

### Purpose
The purpose of this project is to analyze the outcomes of theater kickstarters based on the relationships between launch dates and goals. The goal of this analysis is to determine if the launch dates and goal affect the outcomes of the kickstarter. 

## Analysis and Challenges
The biggest challenge of this analysis is filtering the needed data. Even though Louise wants to focus on data pertaining to theater productions and plays, the raw data also includes data for every Kickstarter between 2009 and 2017. This meant that Louise would have to use filters or write an Excel formula that could pick out Louise's criteria.  

### Analysis of Outcomes Based on Launch Date
According to data, the highest point for total projects launched was in May with 166 projects. The lowest point for total projects launched was in December with 75 projects. The high point for sucessful, failed, and canceled projects respectively was May with 111 sucesses, July and October with 50 failures, and January with 7 cancellations. The low point for sucessful, failed, and canceled projects respectively was December with 37 sucesses, November with 31 failures, and October with 0 cancellations.  

### Analysis of Outcomes Based on Goals
According to data, the highest point for goals was 534 projects that needed $1000 to $4999. The lowest point for goals was 1 project that needed $45000 to $49999. The high point for sucessful, failed, and canceled projects respectively was 388 successes that needed $1000 to $4999, 146 failures that needed $1000 to $4999, and 0 cancellations. The low point for sucessful, failed, and canceled projects respectively was 0 successes that needed $25000 to $29999 and $45000 to $49999, 1 failure that needed $40000 to $44000 and $45000 to $49999 each, and 0 cancellations.

### Challenges and Difficulties Encountered
The biggest challenge was figuring out the syntax for the nested Countif formula. In order to find the count of outcomes based on the range of the goals, a nested Coutif formula had to be used to account for the multiple criteria used to sort the data. However, it was difficult to figure out the syntax, especially for the criteria for the goal ranges. I tried to use nested greater or less than statements for the criteria, only to run into issue of Excel not recognizing them. I had to break up the formuls into multiple statements to allow for multiple criteria. I ended up using a formula that looks like this to populate the Outcomes Based on Goals chart: =COUNTIFS(Kickstarter!$F:$F, "outcome", Kickstarter!$D:$D, ">=start of goal", Kickstarter!$D:$D, "<=end of goal", Kickstarter!$R:$R, "plays")

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
* Successes, failures, and cancelations peaked around May, with a slight drop between January and March, and then would drop after May until December. A conclusion that can be drawn is that the best time to launch a sucessful campaign is between March and May.
* The only time the number of successes and failures came close to meeting was in December; for the rest of the year, the number of successes would remain higher than the number of failures. A conclusion that can be reached is that it is more likely for a campaign to be successful than to fail, no matter the month it was launched.

- What can you conclude about the Outcomes based on Goals?
* Unlike with the launch dates, whether the goals affected the outcome varied wildly from datapoint to datapoint. For campaigns with goals that were less than $1000, the number of successes outnumbered the number of failures, but for goals that were $25000-$29999 and $45000-$49999, the number of successes dropped to zero. Also, for goals between less than $1000 to $25000-$29000 and $40000-$44999 to greater $45000-$49999, the number of successes fell while the number of failures went up. The only times when successes went up were when the goals were between $25000-$29999 to $40000-$44999. The conclusion that can be drawn from this to to either have a goal less than $1000 or have it between $25000 to $40000-$44999 in order to make it a success.  

- What are some limitations of this dataset?
* While the dataset has the start and end-dates of the campaigns, it lacks data for the actual length of the campaigns. Also, neither of the pivot tables have data that measures length of campaigns versus outcomes.

- What are some other possible tables and/or graphs that we could create?
* I would like to have a column that calculates the legnth of each campaign. I would then create a table and graph that eould compare lengths of campaigns versus their goals and outcomes. It would be interesting to see if the lengths of the campaigns affect whether or not they reach their goals. 
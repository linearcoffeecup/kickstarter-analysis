# Kickstarting with Excel

## Overview of Project

Data is gathered from Kickstarter programs over a number of years and compiled in Excel. The task of the project is to gain insights on a particular subcategory, plays, out of a parent category, theatre.  In this analysis, the project (1) uses data on play status as “successful”, “failed”, or “canceled” over the months of the year, and (2) bins data on funding goals and the percent of the total number of plays that were “successful”, “failed”, or “canceled” in each bin.  The insights analysis use Excel capabilities to search, filter, and graph data of interest.  

### Purpose

These insights gained from visualization of the data may be useful for future program planning.  The presentation of the data relates the status of plays both by time in terms of launch date, and by bins of funding goals in separate graphs.  Visual analysis of the relations can help find insights for timing of play starts or for expectations and improvement of goals for a successful play.

## Analysis and Challenges

The analysis uses the database KickStarter_Challenge.xls.  It presents results of outcomes (i.e., the play status) based on launch date as well as funding goals.  In this analysis the following Excel features were used:

- Moving data from one column to another using the text-to-column feature,

- Converting unix time to readable format,

- Functions such as Year(), COUNTIFS(),

- Pivot Tables, and,

- Line Charts

### Analysis of Outcomes Based on Launch Date

The analysis of outcomes based on launch date rely on the following [graph](https://github.com/linearcoffeecup/kickstarter-analysis/blob/main/Resources/Theatre_Outcomes_vs_Launch.png):

￼Theatre_Outcomes_vs_Launch.png![Theatre_Outcomes_vs_Launch](https://user-images.githubusercontent.com/85037467/123554439-98ba6600-d745-11eb-88e4-a39fa73f597f.png)

It is clear that almost all plays have been launched at some time in a given year because very few have been cancelled.  However, not every play launched was “successful”.  Insights for plays launched are:

- Plays should be started around mid-year based on the peak of “successful” plays, and 
  
- The plays with a status of “failed” hover around 40 throughout the months of the year.

### Analysis of Outcomes Based on Goals

The analysis of outcomes based on goals rely on the following [graph](https://github.com/linearcoffeecup/kickstarter-analysis/blob/main/Resources/Outcome_vs_Goals.png):

￼Outcome_vs_Goals.png![Outcome_vs_Goals](https://user-images.githubusercontent.com/85037467/123554448-a66feb80-d745-11eb-8f9c-f904adb593b3.png)


This graph has the difference in play outcome from the previous graph in that there are no “canceled” plays in any of the bins.  Based on the graph the following insight are clear:

- The best chances for a “successful” play are those with goals met in the range of less than or equal to $5,000.00.  It can be observed that in this range “successful” plays are above the median while “failed” plays are relatively low in comparison.  It appears for larger goals that “successful” and “failed” plays are mixed. However, in the interval $35,000.00 to $40,000.00 the plays are “successful” and this range could be explored further, programmatically, to understand this observation and determine if future planning can enhance the underlying reason for success.

- Another insight is that “canceled” plays are those that did not reach a funding goal versus being canceled due to other reasons.  Since the number of canceled plays is very low, resources should not be spent to understand why these plays did not reach goals. 

### Challenges and Difficulties Encountered

During the analysis, I had been seeing a different graph than that shown in the Challenge for one of the analyses.  Upon consideration, I realized that I had not included a filter on plays.  Thus, it is important to clearly know the filters for the data which will be used for graphing.  From this experience, it would be useful to have a way to “double check” the results plotted in a graph.  Since these datasets are very large this double-check method would have to be (1) reviewing graph requirements, or (2) using Excel features to perform “sensibility” checks.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  - Plan to launch plays in summer months, and
  
  - There is a need to understand the reason that the number of “failed” plays does not change too much from 40 and to see if this number can be reduced.

- What can you conclude about the Outcomes based on Goals?

  - Plan to launch plays that have goals around $5,000.00 or less
  
  - Determine why the range of $35,000.00 to $40,000.00 is successful and see it the reason can be improved upon.

- What are some limitations of this dataset?

  Some limitations of this dataset are:

    - Outcome terms are not defined which makes it difficult to know whether success or failure is a financial reason or otherwise,
  
    - The data requires preparation prior to being useful:  examples include the need to split a column into parent and subgroups and also the need to convert time into a readable format.

- What are some other possible tables and/or graphs that we could create?

  - It would be useful to explore the relation between the time from when the play was launched to when it was sunset; however, this data does not appear to be available.  The only “length of time” perspective would be between the “deadline” and “launch date”.  This relation with respect to time could be explored on the time-scale of months.

  - The graph of outcome versus goal was based on an arbitrary binning of the outcomes.  A histogram would provide a more natural binning for visual analysis.

  - Simply drawing conclusions between the two graphs is not justifiable without doing further analysis.  If relations between the two graphs are to be explored further tables and graphs would be needed which use data in the two graphs.



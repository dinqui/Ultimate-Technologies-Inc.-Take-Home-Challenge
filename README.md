# Ultimate Technologies Inc. Take-Home Challenge

## Part 1 ‐ Exploratory data analysis
[Code](https://github.com/dinqui/Ultimate-Technologies-Inc.-Take-Home-Challenge/blob/main/Ultimate%20Technologies%20Inc.%20Take-Home%20Challenge%20-%20Part%201.ipynb)

The daily cycle of log-ins shows that the time of day greatly affects the number of user log-ins. The number of log-ins is highest at the very end, beginning, and middle of the day, with a large dip around 7:30 and a smaller dip around 17:00, as shown in the graph below. 

![Plot of daily cycle of log-ins](https://github.com/dinqui/Ultimate-Technologies-Inc.-Take-Home-Challenge/blob/main/images/time_of_day.png)

The weekly cycle of log-ins shows that the day of the week also affects the number of user log-ins. The number of log-ins increases throughout the work week, but peaks on Saturday and Sunday close behind. 

![Plot of weekly cycle of log-ins](https://github.com/dinqui/Ultimate-Technologies-Inc.-Take-Home-Challenge/blob/main/images/day_of_week.png)

## Part 2 ‐ Experiment and metrics design

For the experiment to encourage driver partners to serve both cities, I would choose the number of times that driver partners pass through the tolls as the measure of success. I would choose this metric because it would need to be tracked in order to reimburse tolls, and indicates whether driver partners are driving in both cities. 

An experiment that I would propose to compare the effectiveness of the proposed change would be to pick a set of driver partners at random to be reimbursed for toll costs while the remaining drivers are not. Then track how often each partner driver from both groups goes through the tolls. I would use the Chi Square Test to verify the signifigance of the difference between driver partners who were reimbursed and those who were not. If the p-value was determined to be small enough that we could reject the null hypothesis that reimbursing partner drivers does not increase the number serving both cities, then I would recommend implementing the toll reimbursement system. One caveat is that it is possible that some driver partners are not crossing through the toll because they are working in both cities but because they live in one city but are driving in the other one. 

## Part 3 ‐ Predictive modeling
1. Perform any cleaning, exploratory analysis, and/or visualizations to use the provided data for this analysis (a few sentences/plots describing your approach will suffice). What fraction of the observed users were retained?
2. Build a predictive model to help Ultimate determine whether or not a user will be active in their 6th month on the system. Discuss why you chose your approach, what alternatives you considered, and any concerns you have. How valid is your model? Include any key indicators of model performance.
3. Briefly discuss how Ultimate might leverage the insights gained from the model to improve its long­term rider retention (again, a few sentences will suffice).

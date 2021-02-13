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
[Code](https://github.com/dinqui/Ultimate-Technologies-Inc.-Take-Home-Challenge/blob/main/Ultimate%20Technologies%20Inc.%20Take-Home%20Challenge%20-%20Part%203.ipynb)

I explored the statistical summary of the numerical categories and created histograms and boxplots as shown below. The boxplots showed that some categorieshad outliers, especially average distance, percent of surge rides, and number of tripes in first 30 days. The histogram for the percentage of weekday trips showed that most users took trips mostly during the week. I also imputed the average of the average rating by drivers and average rating of drivers to fill missing values. 37% of the observed users were retained. 

To create a predictive model to determine whether or not a user will be active in their 6th month on the system I used the following features: city user signed up in, average distance of trips taken in first 30 days, number of trips taken in first 30 days, average rating of driver, average rating by driver, percent of trips taken with surge >1, average surge multiplier over all trips, if ultimate black user, and percent of trips occurring during a weekday. I applied three models to the data, logistic regression, decision tree, and random forest. The best model was the Random Fores with a depth of 4. This model was the best because it minimized the number of type 1 errors. It is more important to minimize how many users are predicted as being retained but actually will not because then they will not be accurately targeted to increase ridership. This model had both an accuracy score and a precision score of 75% and a balanced accuracy score of 70%. The confusion matrix is shown below. Futhermore, the model identified 5 key features for predicting long-term rider retention: average rating by driver, percent surge, city is King's Landing, average surge, and percent weekday trips. Ultimate can use this model to target users who are predicted to not be retained and offer additional marketing or incentives to keep them on board. 

![confusion_matrix](https://github.com/dinqui/Ultimate-Technologies-Inc.-Take-Home-Challenge/blob/main/images/confusion_matrix.png)


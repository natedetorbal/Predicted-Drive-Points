# Predicted-Drive-Points
College Football Predicted Drive Points
by Nate DeTorbal
February, 2021


## Introduction
In Sports, fans always try and justify their teams losses. They say things like "The other team got lucky", or "we lost the game, the other team didn't win it", or even "we really deserved to win that game." While luck is very hard to quantify, we can take a better look at what a team 'deserved' to output in a certain game. Predicting Drive Points is a way that we can look at a possession in football and say on average, this is what should have happened on this possession given how we performed on the given drive. For example, if an offensive possession starts on their own 25 yard-line and the offense manages to get down to the opposing teams 5 yard-line, you would expect them to most likely score a touchdown. However, on the next play, the team turns the ball over, resulting in zero points. The overall success of the drive 'deserved' to score some points, and on average a drive with the same drive statistics do score points. In short, Predicted Drive Points is a descriptive metric that attempts to account for the predicted points a team should score on a drive based on their total offensive performance. You could say that Predicted Drive Points attempts to look at how a team scores on average, and takes out less likely and unusual plays. 


## Data Acquisition
All data is acquired in the 'Get Data.ipynb' notebook. I downloaded and used the CFBD custom library for python to get the data. Here is a link to the library documentation: https://github.com/CFBD/cfbd-python
The data used is play-by-play data for each play in college football. Data from the 2018 Season was used to initially train the model. Data from the 2019 and 2020 seasons were used to validate and view results. More information on what statistics are pulled from the play-by-play data are found in the model variables below. 


## Model Variables
#### Which statistics from a drive are used to find the Predicted Drive Points?
**Start Period (start_period)
:** The Quarter the drive starts
**End Period (end_period)
:** The Quarter the drive ends
**Start Yards-To-Goal (start_ytg)
:** The Yards-To-Goal at the start of the drive
**Success Rate (sr)
:** The Proportion of time the offense gains 40% of yards to go on first down, 60% of yards to go on second down, or gains a first-down on third or fourth down. This is used to measure the efficiency of the offense. This is used in the model as the average success rate for the whole drive. 
**Predicted Points Added per Play (ppa_per_play)
:** The Average Predicted Points Added per Play from the drive. This is similar to the purpose of success rate, but ppa also captures the magnitude of how successful or unsuccessful a given play was. 
**Number of Plays (num_plays)
:** The number of plays that occured on the drive
**Reduced Result (reduced_result)
:** The response variable in the model, in other words this is the result we are hoping to predict. The result of the drive, simplified to any of these four categories: Touchdown (TD), Field Goal (FG), Turnover (TO), Non-Score (NON_SCORE). 


## More Information
The specifics of the project are found in the 'Predicted Drive Points.ipynb' notebook file. I tested a few different classification model types and settled on using a Gradient Boosting Classifier. The results of the model are displayed in the aforementioned notebook. 


## Credits
#### Conor McQuiston (@ConorMcQ5 on Twitter)
This Predicted Drive Points Project is Conor's original idea. I took his idea and attempted to make it my own. I added upon Conor's project by using a Multinominal Classification Model, where Conor used a series of Logistic Regression Models. I also did this project in Python where Conor did it in R.



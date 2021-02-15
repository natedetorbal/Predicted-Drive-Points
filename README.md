# Predicted-Drive-Points
College Football Predicted Drive Points

## Introduction




## Data Acquisition
All data is acquired in the 'Get Data.ipynb' notebook. I downloaded and used the CFBD custom library for python to get the data. Here is a link to the library documentation: https://github.com/CFBD/cfbd-python


## Model Variables
Predicted Points Added (ppa)
: definition

Start Period (start_period)
: The Quarter the drive starts

End Period (end_period)
: The Quarter the drive ends

Start Yards-To-Goal (start_ytg)
: The Yards-To-Goal at the start of the drive

Success Rate (sr)
 :The Proportion of time the offense gains 40% of yards to go on first down, 60% of yards to go on second down, or gains a first-down on third or fourth down. This is used to measure the efficiency of the offense.

Predicted Points Added per Play (ppa_per_play)
: The Average Predicted Points Added per Play from the drive. This, unlike Success Rate, also captures how successful or unsuccessful a given play was.

Number of Plays (num_plays)
: The number of plays that occured on the drive

Reduced Result (reduced_result)
: The response variable in the model, in other words this is the result we are hoping to predict. The result of the drive, simplified to any of these four categories: Touchdown (TD), Field Goal (FG), Turnover (TO), Non-Score (NON_SCORE). 


## Use of the Model



## Credits
#### Conor McQuiston (@ConorMcQ5 on Twitter)
This Predicted Drive Points Project is Conor's original idea. I took his idea and attempted to make it my own. I added upon Conor's project by using a Multinominal Classification Model, where Conor used a series of Logistic Regression Models. I also did this project in Python where Conor did it in R.



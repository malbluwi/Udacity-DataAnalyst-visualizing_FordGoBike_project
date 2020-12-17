# Ford GoBike Data Visualization
## by Mohammed Albluwi



## Introduction:

In this Ford Go Bike Data Analysis, We want to look at what affects the biking system's usage. This leads us 
to investigate several features that we think has a relationship with our investigation. These interesting 
features are ages, user typer, time, and locations. The investigation can be summarized in the following question:

what is the most gender like to bike?
What are their ages?
What time do we have more trips? In the morning, afternoon, or evening?
What is the status of bike usage during months and weekdays?
What is the number of bike usage per location?
Which location has the most trip?
Where, when, and what day do unsubscribed customers bike compared to subscribed customers?


## About Dataset:

The data consists of approximately 2,619,577 records for public bike rides from Jun 2017 to Septemper 2018 and from 
Jan 2019 to the end of Feb 2019. 9936 records were removed as they are null data. There were no duplicate rows and 
what we found was duplicate indexes as a result of merging several data frames. The data consists of 16 features, 
and we added 15 more features, which are calculated or split from the 16 features. The following are the 16 new columns split 
from 'start_time' and 'end_time':

 1- Start_Date
 2- Start_Year
 3- Start_Month
 4- Start_Day_of_Week
 5- Start_Time
 6- Start_Hour
 7- Start_Min

 8- End_Date
 9- End_Year
10- End_Month
11- End_Day_of_Week
12- Start_Time
13- End_Hour
14- End_Min

The new calacluted column that derived from 'duration_sec' is 'duration_min'. 

## Dataset Source

11 datasets were taken from different source. 10 datatsets are from kaggle website, https://www.kaggle.com/franckjay/ford-gobike-data,
and the other is from Udacity's soucre uploaded on the project page. All the data were merged into file named df_goBike_clean.





## Summary of Findings:

The use of bicycles for Ford GoBikes is a more popular activity in the summer season. Usually, 
tourists or occasional riders who want to enjoy summer use the bike system. Subscribers seem
 most of them are workers as their ages fall between 20-45, and their usage in the morning is 
more than in the afternoon. The month of February is the highest usage of the system, and we 
suggest more investigation for the source of data to confirm credibility. The ratio of 
customers biking for age interval 19-30 is more significant than the subscriber's ratio. Also,
 the subscriber's ratio for age interval 31 – 60 is bigger than customers'.  The top 10 stations 
in the number of users count are all in the same area where the distance between any two stations 
won't exceed 1.2 miles! See the map below. We guess that it is crowded area and users use the 
system to beat traffic and the stress of commuting.





## Presentation:

'output-toggle.tpl' file is used to make slides look nicer. The following is the command:

jupyter nbconvert slide_deck_template.ipynb --to slides --template output-toggle.tpl--post serve








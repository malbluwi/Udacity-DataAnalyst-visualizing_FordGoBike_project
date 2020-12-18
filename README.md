# Ford GoBike Data Visualization
## by Mohammed Albluwi




## About Data set:

The data set contains information about bicycle riders made in a bike-sharing system covering the greater San Francisco Bay area.



## Data Source

11 datasets were taken from different sources. 10 datasets are from the kaggle website, https://www.kaggle.com/franckjay/ford-gobike-data,
and the other is from Udacity's source uploaded on the project's page. All the data were merged into a file named: df_goBike_clean.



### Features :

The features included in the data set are the following:

 1- Duration Sec                     
 2- Start Time                       
 3- End Time                         
 4- Start Station Id              
 5- Start Station Name            
 6- Start Station Latitude           
 7- Start Station_Longitude          
 8- End Station Id                
 9- End Station Name              
10- End Stationl Latitude             
12- End Station Longitude            
13- Bike Id                          
14- User Type (Subscriber or Customer)                    
15- Member Birth Year           
16- Member Gender (Male, Female or Other)               
17- Bike Share For All Trip   

9936 records were removed as they are null data.

The data consists of approximately 2,619,577 records for public riders from Jun 2017 to September 2018 and from 
Jan 2019 to the end of Feb 2019.  There were no duplicate rows and what we found was duplicate indexes as a result of merging several data frames.



## Data Cleaning

There was some cleaning needed to the data set. This included: 

 1- Duplicate index 
     there were no duplicate rows and what we found was duplicate indexes as a result of merging several data frames.

 2- Duplicate rows

 3- Many null values for several columns 
     9936 records were removed as they are null data

 4- Data types of some columns are inappropriate
     The type of columns were changed are as follow:
       a- 'start_station_id' and 'end_station_id' to the int format.
       b- 'bike_id', 'start_station_id', and 'end_station_id' to object format.
       c- 'user_type', 'member_gender', and 'bike_share_for_all_trip' to category format.
       d- 'start_time', 'end_time' to the timestamp format.
       e- 'member_birth_year' to int format.</b>

 5- Some values violate the rule of accuracy
      any member who is over 100 year old was removed

 6- Split 'start_time' and 'end time' into 7 new columns each and calcuate minutes from 'duration_sec' 
     The following are the 14 new columns:

	a- split from 'start_time':
          1- Start_Date
          2- Start_Year
          3- Start_Month
          4- Start_Day_of_Week
          5- Start_Time
          6- Start_Hour
          7- Start_Min

       b- split from 'end_time':
          1- End_Date
          2- End_Year
          3- End_Month
          4- End_Day_of_Week
          5- Start_Time
          6- End_Hour
          7- End_Min

       c- calcuate from 'duration_sec'
          1- duration_min


 7- Add age and duration_min columns
    age calculated from	'Member Birth Year'
    duration_mne calcuated from 'duration_sec'



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



## Key Insights for Presentation:

For a presentation, We want to look at what affects the biking system's usage. This leads us to 
investigate several features that we think they have relationships with what we are looking for. 
These interesting features are ages, ender and user type, time, and locations. The investigation 
process is divided into 3 explorations. In each one, we try to investigate our features of 
interest by plotting and analyzing. 

 a- Univariate Exploration
    1- The usage of the system by month and weekday 
    2- Ten top stations with most trips. 


 b- Bivariate Exploration
    1- The propostion of the user type


c- Multivariate Exploration
   1- The weekley usage of bikes per user type and trip duration per user type. 
   2- Riding count based on user typer and member gender on top 10 Stations. 
   3- Weekly Usage as per gender and user typer.Top 10 trip stations by time (Morning, Afternoon, Night)
   4- How many FordGoBike users weekly, and what their ages?



## Presentation of Slides withoud Code:

'output-toggle.tpl' file is used to make slides look nicer. The following is the command:

jupyter nbconvert slide_deck_template.ipynb --to slides --template output-toggle.tpl--post serve








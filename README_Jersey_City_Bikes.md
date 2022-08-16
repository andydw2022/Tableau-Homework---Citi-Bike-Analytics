# Tableau Homework - Citi Bike Analytics

Please note I was not able to save to my local drive in .twbx format using save as...
because I am using the public version. The only options to save on my copy of Tableau are:

Save to Tableau Public...
Save to Tableau Public As ...

Just to be on the safe side I have taken screen shots and uploaded them in the folder Images.
There are 3 main visualisations I have submitted for this homework:

## Story Board City Bike usage in 2019 in Jersey City
url : https://public.tableau.com/shared/QWZTJSQWD?:display_count=n&:origin=viz_share_link

## Dashboard : Usage by age, gender, trip  & user types
url : https://public.tableau.com/views/DashboardUsagebyagegendertripusertypes/DashboardofBikeusagebyagegendertriptotalsandusertypes?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link

## Dashboard : Usage by Start and End Stations
url : https://public.tableau.com/views/DashboardUsagebyStartandEndStations_16606140386380/DashboardUsagebyStartandEndStations?:language=en-GB&:display_count=n&:origin=viz_share_link


## Background

![Citi-Bikes](Images/citi-bike-station-bikes.jpg)

The [New York Citi Bike](https://en.wikipedia.org/wiki/Citi_Bike) Program is largest bike sharing program in the United States. Since 2013, the Citi Bike Program has implemented a robust infrastructure for collecting data on the program's utilisation. Through the team's efforts, each month bike data is collected, organised, and made public on the [Citi Bike Data](https://www.citibikenyc.com/system-data) webpage.

However, while the data has been regularly updated, the team has yet to implement a dashboard or sophisticated reporting process. City officials have a number of questions on the program, so your first task on the job is to build a set of data reports to provide the answers. The following visualisations are based on 12 months data from Jersey City for the year 2019 (pre-pandemic). Their data has more demograhic information that the New York City dataset. For example:

JC : Headings are:

tripduration	        266	               1543
starttime    	        03:35.5	           23:32.9
stoptime	            08:01.8	           49:16.1
start station id	    3273	           3681
start station name	    Manila & 1st	   Grand St
start station latitude	40.72165072	       40.71517768
start station longitude	-74.04288411	   -74.03768331
end station id	        3209	           3213
end station name	    Brunswick St	   Van Vorst Park
end station latitude	40.7241765	       40.71848892
end station longitude	-74.0506564	       -74.04772663
bikeid	                42494	           45343
usertype	            Subscriber	       Customer
birth year	            1988	           1996
gender	                1                  2

NYC : Headings are:

ride_id	                    55262E4365A955A2		    D272F1B15D841EC0
rideable_type	            classic_bike		        classic_bike
started_at	                18/01/2022 8:23		        21/01/2022 9:03
ended_at	                18/01/2022 8:28		        21/01/2022 9:05
start_station_name	        Boerum Pl\t& Pacific St		E 12 St & Ave C
start_station_id	        4488.09		                5616.08
end_station_name	        Clinton St & Joralemon St	E 10 St & Avenue A
end_station_id	            4605.04		                5659.05
start_lat	                40.68848906		            40.727243
start_lng	                -73.99116039		        -73.976831
end_lat	                    40.69239502		            40.72740794
end_lng	                    -73.99337909		        -73.98142006
member_casual	            member		                member

Jersey City(JC) data has age and gender which gives more scope for analysis of the demographics.
But JC data start and stop times are not actual time of day unlike NYC, that's an anomaly and also JC data has a large number of unknown genders and also age anomalies. Like there are birth years in the 19th century or very early 20th century. I have chosen to not filter them out to highlight them as an anomaly.

## Data Preparation
-------------------
The data set chosen for visualtion is 12 months of 2019 (pre-pandemic) for Jersey City.

User Type (Customer = 24-hour pass or 3-day pass user; Subscriber = Annual Member)
Gender (Zero=unknown; 1=male; 2=female)

A new column for month was added and all 12 files were then aggreagated into 1 file.
A new column for Gender name was added  with values of 'Female', 'Male', 'Unknown'
A another new column for Age calculated using 2019 - year of birth.

## Tableau Public Visualisations for Jersey City in 2019

Dashboard : Usage by age, gender, trip totals & user types
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

*Access this Tableau DashBoard visualisations by using this url:
https://public.tableau.com/views/DashboardUsagebyagegendertripusertypes/DashboardofBikeusagebyagegendertriptotalsandusertypes?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link

This dashboard contains 4 visualisations of bike patronage for 2019 for Jersey City

    1. Trip counts by gender per month
    2. Total Trip counts per month
    3. User Types per month
    4. Average Distance covered by riders by age (5 yearly brackets). Contains age anomalies. The reason could be data entry error, privacy concerns or weird sense of humour.

Dashboard : Usage by Start and End Stations
+++++++++++++++++++++++++++++++++++++++++++

*Access this Tableau DashBoard visualisations by using this url:
https://public.tableau.com/views/DashboardUsagebyStartandEndStations_16606140386380/DashboardUsagebyStartandEndStations?:language=en-GB&:display_count=n&:origin=viz_share_link


This dashboard contains 4 visualisations of bike patronage for 2019 for Jersey City

    1. Trip counts by gender per month
    2. Total Trip counts per month
    3. User Types per month
    4. Average Distance covered by riders by age (5 yearly brackets). Contains age anomalies. Some ages over 100! The reason could be data entry error, privacy concerns or weird sense of humour.


Story Board City Bike usage in 2019 in Jersey City
+++++++++++++++++++++++++++++++++++++++++++++++++++

*Access this Tableau StoryBoard visualisations by using this url:
https://public.tableau.com/shared/QWZTJSQWD?:display_count=n&:origin=viz_share_link

This StoryBoard contains 13 visualisations of bike patronage for 2019 for Jersey City


1. Total Trips taken by month. 
--------------------------------------
This gives an overall picture of usage of bike
trips taken regardless of age, gender or user type.
Most trips were undertaken in the warmer months of July, August and September

2. Trips taken per month by gender.
---------------------------------------------- 
Males account for the overall majority of usage across all months.
However there are quite a few riders who either did not or chose to not reveal
their gender.

3. Comparison between Subscribers and Casual Customers
---------------------------------------------------------------------------------
Here we see that the main users of the system 
are Subscribers well ahead of casual customer.
Usage split into months. Subscribers are most likely daily commuters

4. Trips by age in 5 year groups
-----------------------------
In this chart we see the ages in 5 year brackets of riders
and the average distance covered in km. 
Notice the ages above 80.
Something not quite right with the data recorded here. 
30-35 year olds ride on average further than any other age group

5. Trips by individual age
-----------------------
In this chart we see the ages ungrouped. 
There is a statistic that really stands out and
that is the number of 50 year olds using the bikes.
No data available that might explain this anomaly

6. This bar chart shows the popularity of station start points for trips.  	
---------------------------------------------------------------------------
The top 10 stations are : 
    1. Grove St PATH is by far the most popular starting point followed by :
    2. Hamilton Park
    3. Sip Ave
    4. Harborside
    5. Newport PATH
    6. Marin Light Rail
    7. Newport Pkwy
    8. Newark Ave
    9. City Hall
    10. Morris Canal


7. This map shows the popularity of station start points for trips. 	
--------------------------------------------------
The size of each marker indicates the number of trips started from this point. 
The most popular starting points are in or close to the downtown area.	
The top 10 stations are : 
    1. Grove St PATH is by far the most popular starting point followed by :
    2. Hamilton Park
    3. Sip Ave
    4. Harborside
    5. Newport PATH
    6. Marin Light Rail
    7. Newport Pkwy
    8. Newark Ave
    9. City Hall
    10. Morris Canal

8. This bar chart shows the station end points by popularity for trips. 	
---------------------------------------------------------------------------
Interesting to note that almost all the end points coincide with the start points
except for Columbus Dr at Exchange. I noticed some end points are in Manhattan but they
are in the single digits mainly,
The top 10 stations are : 
    1. Grove St PATH is by far the most popular starting point followed by :
    2. Hamilton Park
    3. Sip Ave
    4. Harborside
    5. Newport PATH
    6. Marin Light Rail
    7. Columbus Dr at Exchange
    8. Newport Pkwy
    9. Newark Ave
    10. City Hall



9. This map shows the station end points by popularity. 	
--------------------------------------------------------
Looks like most bike riders start and end their trips at the same point. 
Apart from Columus Drive. Also I noticed that a few trips ended in Manhattan
but those numbers are quite low.The size of the markers reflect their usage.

    1. Grove St PATH is by far the most popular starting point followed by :
    2. Hamilton Park
    3. Sip Ave
    4. Harborside
    5. Newport PATH
    6. Marin Light Rail
    7. Columbus Drive
    8. Newport Pkwy
    9. Newark Ave
    10. City Hall


10. Median and Total distance covered (km) by month  
---------------------------------------------------------------------
I created some new calculated fields, 
start and end points of a journey and used the distance
function to calculate the distance for each trip based on
their start and end points. From 810 to 880 meters seems
to be the median for each month, very little variations 
in median distance covered but total distance covered in 
July, August and September recorded the highest numbers.
Once again it shows the trips taken are seasonal.


11. Total trips, total distance (km), Avg distance, Avg trip duration by customer Type
--------------------------------------------------------------------------------------
Its interesting that average trip duration is higher for customers than subscribers, 
It could be customers are casual users who are sightseeing and/or doing multiple stops.
But in terms of total distance Subsribers travel more.
More likely commuters who ride everyday. 
And subscribers do more trips overall than customers.
If start and end times of the day and day of the week are available
further analysis could shed more light on these figures.

12. Total Trip duration and Distance covered by each bike
--------------------------------------------------------------------------
This tells the maintenance team how much usage each bike received over the year 
in km and the number of times it has been used.
The first column shows distance in km and the second shows the number of times that bike was used
for a trip

13. Average distance (km), Median distance (km) and Number of trips per bike
-----------------------------------------------------------------------------
This tells the maintenance team more information to decide which bikes will be due for maintenance.
The first column show the Total distance in km, the second Avg Distance in km and
 the third shows the number of trips for each bike.


**Finally, create your final presentation**

* Create a Tableau story that brings together the visualisations, requested maps, and dashboards.
* This is what will be presented to the officials, so be sure to make it professional, logical, and visually appealing.

## Considerations

Remember, the people reading your analysis will **NOT** be data analysts. Your audience will be city officials, public administrators, and heads of New York City departments. Your data and analysis needs to be presented in a way that is focused, concise, easy-to-understand, and visually compelling. Your visualisations should be colourful enough to be included in press releases, and your analysis should be thoughtful enough for dictating programmatic changes.

## Submission

Your final submission should include:

* A link to your Tableau Public workbook that includes:
  * 4-10 Total "Phenomenon" Visualisations
  * 2 Dashboards
  * 1 City Official Map
  * 1 Story
* A text or markdown file with your analysis on the phenomenons you uncovered from the data.

## Sharing Your Work
In order to share your work, we are asking that you will save your workbook as a .twbx file so that your TA's can grade them.

To save your workbook as a .twbx file, you will just need to select "Save As..." from the "File" dropdown. Then, select the .twbx option.

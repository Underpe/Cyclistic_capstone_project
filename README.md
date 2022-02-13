# Cyclistic_capstone_project
## Google Data Analytics Capstone Project : Case 1 - Cyclistic

The following case study is part of Google Data Analytics Professional Certificate capstone project. Along this work, taking the role of a junior data analyst, real-world task will be performed in order to answers the key business questions of Cyclistic, a bike -sharing company based in Chicago.

## Introduction
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.

In order to fulfill the different needs of their customers, the company offers flexibility on its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Lily Moreno, the marketing director, believes that maximizing the number of annual members will be key to future growth. For that, she believes there is a very good chance to convert casual riders into members rather than targeting new customers.

Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. In order to do that, however, the marketing analyst team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends.

## Business Task
The main task of this project is to analyze the last twelve months of historical data, to identify possible trends on the different behavior of casual riders and anual member riders. The ultimate objective of this analysis would be to help guide the future marketing tactics.

## The Data
Cyclistic’s historical trip data of the last twelve months (January to December of 2021) is provided by Motivate International Inc. to analyze and identify the different possible trends. Due to privacy reasons, this is public data does not show riders’ personally identifiable information such pass purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes.  

The data is current and relevant; but due to the COVID-19 pandemic, and the infection waves it has had along the data collection time, it won’t be possible to determine if any variation withing the analyzed months has been affected comparing to prior of the pandemic time.

At the same time, there are an important number of start and end stations name data observations that are missing.
For each month there is a .cvs file with the information of all rides performed withing that corresponding month. The variable collected in the dataset are the following ones:

-	ride_id		# Ride identification number
-	rideable_type	# Bicycle type 
-	started_at		# Starting date and time
-	ended_at		# Ending date and time
-	start_station_name	# Starting station name
-	start_station_id	# Starting station identification number
-	end_station_name	# Ending station name
-	end_station_id	# Ending station identification number
-	start_lat		# Starting latitude coordinate
-	start_lng		# Starting longitude coordinate
-	end_lat		# Ending latitude coordinate
-	end_lng		# Ending longitude coordinate
-	member_casual	# Type of customer (casual / member)

## Data process
For this part of the project, the tools that were used are Microsoft Excel and Rstudio.

Firstly, each .csv file has been observed on Excel, and any possible duplicate row has been checked. The correct data formatting off all the variables have been ensured.

A new column has been created to add the duration of each ride in minutes, called "ride_length_mins". This new variable shows some negative values, having the ride ending time before the starting one. These values have been taken as errors, as no rides could have less than zero seconds; those cases have been removed.
Two new columns have been created to represent the day of the week and the month where each ride took place, called “weekday” and “month” respectively.

Once the previous part was done, I moved to Rstudio to keep with the data processing. The corresponding libraries were loaded in order to set up the working environment.

All the steps taken during the data processing part on Rstudio can be found on this [link](Data_Process)

## Data Analysis
For this part of the project, both Rstudio and Tableau tools have been used. The whole description of the steps taken during this part on Rstudio can be found on this [link](Data_Analysis)

One of the first things observed during the initial analysis taken when calculating the mean, median, maximum and minimum ride lengths for casual and member rider, is that member users do have fewer ride lengths comparing with casual users. 
Observing the following **Plot No.1** it can easily see how casual users do rides almost with double length duration comparing with member users. The variation of the ride lengths, is more homogeneous within the week on member users than on casual user, where this last ones have the peak lengths on weekend days.

Checking the amount of rides for both user types on week days represented in **Plot No.2**, it can be observed how beside member users have more rides during the week, these ones are surpassed by casual users on weekend days,


**Plot No.1**

![Bicycles rides by average ride length and weekday](https://user-images.githubusercontent.com/99078887/152646478-003c7698-7c8f-41eb-a850-98ac0aacf119.jpeg)

**Plot No.2**

![Bicycles rides by rides amount and weekday](https://user-images.githubusercontent.com/99078887/152647128-b75fcc07-fcae-424e-b8fe-d434bcf25c2b.jpeg)

These differences could indicate a different purpose of each type of user when taking a ride. Casual users seem to be more active on weekend days, both by ride amounts and riding lengths. Whereas member users are more homogeneous on their usage behavior along the week.

If performing the same analysis on the monthly rides, similar trends are observed. The length of the rides of member users are more even during the whole year, while casual users ones have longer rides in time, mostly withing the first half of the year **(Plots No.3 and No.4)**

**Plot No.3**

![Bicycles rides by rides length and month (2)](https://user-images.githubusercontent.com/99078887/152648863-2d527dc9-153e-41fc-b522-021d1cbee432.jpeg)

**Plot No.4**

![Bicycles rides by rides lengh and month WRAP (2)](https://user-images.githubusercontent.com/99078887/152648883-c9947ce3-d2fd-4d9d-98c3-bd041b720945.jpeg)


When observing the rides amount by month, for both type of users, the highest amount of rides happen on warm months. For member users, the number of rides is quite uniform from June to October, whereas for casual riders, the amount of rides are at its highest on July and August. **(Plots No.5 and No.6)**

July and August are mainly holiday season months, and could happen the same as with weekend days, where casual riders use the bike-sharing service the most. On the other hand, member users have a more uniform usage of the service during the week days and also during the warm months. This behavior for member users could show their purpose is something happening more constantly, not affected by big changes, like the transportation to the work or studying places. For casual rides, their usage behavior could be more related with leisure time or holidays.


**Plot No.5**

![Bicycles rides by rides amount and month (2)](https://user-images.githubusercontent.com/99078887/152673874-1c781969-c1de-4c92-bb5b-267caaa66601.jpeg)

**Plot No.6**

![Bicycles rides by rides amount and month WRAP (2)](https://user-images.githubusercontent.com/99078887/152673904-1367c9bf-0f72-4814-b0e6-ce5907255d2a.jpeg)

Some differences could also be found on the type of bicycles that users use (**Plot No.7**). Member users tend to use more classic_bike type, while for casual users, the use of classic and electric type of bike is more even. At the same time, member users seems not to use docked_bike type; it could be related with the purpose of using the bikes for the transportation to work or studying places, as it could not be that convenient.

**Plot No.7**

![Bicycles rides by rideables ride amount  WRAP](https://user-images.githubusercontent.com/99078887/152687850-6362c09e-56a8-4809-8d3d-d79c9d9f9fdc.jpeg)


The final analysis has been performed with Tableau, to visualize the geographical location of each riding starting point for each type of user. With the cordinates of latitude and longitude provided in the data, the visualization of **Plot No.8** has been created. The amount of rides on each station are represented by the size of the circumference. It can be observed how casual riders are more located on the coastal area of the city, mainly on the Loop and Near north areas, that belong to the city venter and touristic places of the city; whereas member users, cover a wider range of the city, that are not that localized on the central areas.

**Plot No.8**

![Dashboard 1](https://user-images.githubusercontent.com/99078887/152687860-36f1c605-a662-44d6-a23b-87514ff4824d.png)


## Summary

Finally, after having performed the analysis, three main insights can be highlighted in the comparison between casual users and member users in the use of shared bicycles:

1) Member users are more regular in their sharing bike service usage during the whole year, beside the cold winter months. At the same time, these customers are also very regular when using the bicycles during the week days. On the other hand, casual users' peak usage along the year happens in July and August. This last one also happens to increase their service usage on weekends, bypassing member users' amount of rides on those days. From these results it could be understood that casual members use the service more for their leisure time and holidays, than member user; These last ones, instead, it seems their usage is more focus on transportation service to their work/educational places.
2) Member users' starting stations are also more spread all over the city than the casual uses. These last ones are more localized on the coastal areas of the city center. This also could reinforce the idea that casual users make more use of the service for leisure and tourism, compared to member users. 

Additionally, based on the analysis performed, I would like to mention some recommendations in order to propose actions that could make casual users convert into members:

1) A new type of subscription to attract casual users that is focused on the use of the bike service during the weekends, during the summer and holiday months, or a service limited to tourist and leisure areas.
2) Launch a marketing campaign during the holiday and summer stages, in the most central and coastal areas of the city, where casual members use the service stations the most.
3) Offering rewards or discounts for longer rides could attract casual users, as these ones tends to ride for longer times.


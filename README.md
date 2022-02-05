# Cyclistic_capstone_project
## Google Data Analytics Capstone Project : Case 1 - Cyclistic

The following case study is part of Google Data Analytics Professional Certificate capstone project. Along this work, taking the role of a junior data analyst, real-world task will be performed in order to answers the key business questions of Cyclistic, a bike -sharing company based in Chicago.

## Introduction
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime.

In order to fulfill the different needs of their customers, the company offers flexibility on its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

Cyclistic’s finance analysts have concluded that annual members are much more profitable than casual riders. Lily Moreno, the marketing director, believes that maximizing the number of annual members will be key to future growth. For that, she believes there is a very good chance to convert casual riders into members rather than targeting new customers.

Moreno has set a clear goal: Design marketing strategies aimed at converting casual riders into annual members. In order to do that, however, the marketing analyst team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. Moreno and her team are interested in analyzing the Cyclistic historical bike trip data to identify trends.

## Business Task
The main task of this project is to analyze the historical data of the last twelve months to identify possible trends on the different behavior on casual and member riders in order to help guide the future marketing tactics.

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

All the steps taken during the data processing part on Rstudio can be found on this [link]



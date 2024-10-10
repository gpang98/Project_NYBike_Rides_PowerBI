# NY Bike Rides Summary - Winter (Feb) and Summer (Aug) 2023 using Power BI

Dashboard showing Most Popular Winter Start Stations.
https://github.com/gpang98/Project_NYBike_Rides_PowerBI/blob/main/Images/01_Main_Dashboard_NYBikes_Rides_Start_Stations_Popularity.jpg 

Dashboard showing Most Popular Winter End Stations.
https://github.com/gpang98/Project_NYBike_Rides_PowerBI/blob/main/Images/02_Main_Dashboard_NYBike_Rides_End_Stations_Popularity.jpg

Dashboard showing Summer Summary.
https://github.com/gpang98/Project_NYBike_Rides_PowerBI/blob/main/Images/03_Main_Dashboard_NYBikes_Rides_Summer_Overview.jpg

Dashboard showing Winter Summary.
https://github.com/gpang98/Project_NYBike_Rides_PowerBI/blob/main/Images/04_Main_Dashboard_NYBikes_Rides_Winter_Overview.jpg


## Overview

This project analyzes and compares bike ride data in New York between the winter (Feb) and summer (Aug) 2023 seasons using Power BI. The dataset contains information about bike rides, including duration, distance, and other relevant attributes.

## Objective

The primary goal of this project is to:
- Analyze the differences in bike rides during winter and summer.
- Extract insights and patterns from the dataset related to seasonal variations.
- Visualize key metrics to highlight the differences between the seasons.


## Dataset

The dataset used for analysis are taken from the NYBike Rides websiete. https://citibikenyc.com/system-data
- Selected zip files are:
	- https://s3.amazonaws.com/tripdata/202302-citibike-tripdata.csv.zip (Feb 2023 which is considered Peak Winter in NY)
	- https://s3.amazonaws.com/tripdata/202308-citibike-tripdata.csv.zip  (Aug 2023 which is considered Peak Summer in NY)
- The original dataset has the following field:
	- Start and End Station Names
	- Start and End Station Latitudes and Longitudes
	- Start Time and End Time of each Rides
	- Ride Id
	- Start and End Station Id
	- Member Type (member or casual)
	- bike Type (classic, electric or docked)
- Please note that the original dataset have been randomly reduced to 20% of the original size for ease of loading and analysis in Power BI.  Hence, the conclusions derives here might not be representative of the original dataset.

## Tools and Libraries
- Python: Used for data preprocessing, initial analysis, and visualization.
- Pandas: Utilized for data manipulation and analysis.
- Matplotlib and Seaborn: Used for data visualization.
- Jupyter Notebook: Employed as the development environment.
- Since the Winter and Summer CSV too big for easy manipulation in Power BI, they are reduced to randonly 20% of the originla size before they are merged into one file (~215MB) and loaded to GitHub.  The GitHub large file `lfs` option is used to upload the file.
- Power BI & DAX: The main data manipulation and visualization to display the various Worksheet and Dashboards and published to GitHub.  Similary, GitHub `lfs` option is used to upload the Power BI `.pbix` file.


## Workflow
- The following are calculated using DAX in Power BI.
	- Distance Km (this is done using the Start (Lat/Long) and End (Lat/Long).  It is not the actual travelled distance but represent minimum distance travelled.
	- Trip Duration Minutes (From the Start and End Time)
	- Distance Km Bin size to generate Histogram plot since not able to access any pre-programmed histogram apps.
	- Trip Duration Minutes Bin for similar reason to the above.

## Usage

1. **Setup Environment:**
   - Download Power BI free version so that you can download the uploaded files and view within your local machine.

2. **Educational Purposes:**
   - Feel free to download the uploaded pages so that you can also explore the dataset and gain insights.

## Main Findings.
1. Summer (12.75mil minutes) recorded about three time more total trip durations than Winter (4.5mil).  Total Distance in Km is also about three times more (6.16mil vs 2.1mil).  Since the dataset is only 20% of the original, the actual otal might be about five times this numbers but the ratio should remain the same. 
2. Most of the popular start and end stations are located South of Central Park.  This area covers the busy business district of Manhattan.
3. Most rides are done by members who commute daily for work at around 8am and return around 5-6pm.  This is true for both winter and summer.
4. Most rides are done using classic bikes.
5. There are more rides during weekdays versus weekends.


## References

1. Inspired by lectures notes from Tableau application and ChatGPT.

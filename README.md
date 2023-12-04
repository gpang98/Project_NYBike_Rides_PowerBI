# NY Bike Rides Summary - Winter (Feb) and Summer (Aug) 2023

Main Dashboard link showing the interactive map.
https://public.tableau.com/views/NYBike_Winter_Feb_Aug23_Rides_D1/Dashboard1?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link

Dashboard showing Most Popular Winter Start and End Stations.
https://public.tableau.com/views/NYBike_Winter_Feb_Aug23_Rides_D2/Dashboard2?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link


Dashboard showing Winter Summary.
https://public.tableau.com/views/NYBike_Winter_Feb_Aug23_Rides_D3/Dashboard3?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link

Dashboard showing Summer Summary.
https://public.tableau.com/views/NYBike_Winter_Feb_Aug23_Rides_D4/Dashboard4?:language=en-GB&publish=yes&:display_count=n&:origin=viz_share_link


Story explaining the observed ride patterns during Winter Feb 2023.
https://public.tableau.com/shared/9F49N548B?:display_count=n&:origin=viz_share_link


## Overview

This project analyzes and compares bike ride data in New York between the winter and summer seasons. The dataset contains information about bike rides, including duration, distance, and other relevant attributes.

## Objective

The primary goal of this project is to:
- Analyze the differences in bike rides during winter and summer.
- Extract insights and patterns from the dataset related to seasonal variations.
- Visualize key metrics to highlight the differences between the seasons.
- Create a story focusing on the Winter period with regards to bike rides pattern.

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

## Tools and Libraries
- Python: Used for data preprocessing, initial analysis, and visualization.
- Pandas: Utilized for data manipulation and analysis.
- Matplotlib and Seaborn: Used for data visualization.
- Jupyter Notebook: Employed as the development environment.
- The Winter and Summer CSV are merged into one large file (>1GB) and loaded to Tableau.
- Tableau: The main data visualization to display the various Worksheet, Dashboards and Story and published to Tableau Public.


## Workflow
- The following are calculated field in Tableau.
	- Distance Km (this is done using the Start (Lat/Long) and End (Lat/Long).  It is not the actual travelled distance but represent minimum distance travelled.
	- Trip Duration Minutes (From the Start and End Time)

## Usage

1. **Setup Environment:**
   - Download Tableau Public so that you can download the uploaded files and view within your local machine.

2. **Educational Purposes:**
   - Feel free to download the uploaded pages so that you can also explore the dataset and gain insights.

## Main Findings.
1. Summer (64.38mil minutes) recorded about three time more total trip durations than Winter (22.85mil).  Total Distance in Km is also about three times more (8.1mil vs 3mil). 
2. Most of the popular start and end stations are located South of Central Park.  This area covers the busy business district of Manhattan.
3. Most rides are done by members who commute daily for work at around 8am and return around 5-6pm.  This is true for both winter and summer.
4. Most rides are done using classic bikes.
5. There are more rides during weekdays versus weekends.


## References

1. Inspired by lectures notes and ChatGPT.
2. Marketing 353, 2023, Creating Dashboard and Story in Tableau Desktop. https://www.youtube.com/watch?v=FgVnTwGqlfM 
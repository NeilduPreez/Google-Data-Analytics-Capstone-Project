# Google-Data-Analytics-Capstone-Project

This is the capstone project for the Google Data Analytics Certification. This is my  first project, so I decided to do the entire case study using Microsoft Excel.

## What is the business task?
Cyclistic is a fictional bike-share company in Chicago with more than 5,800 bicycles and 600 docking stations. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members. The director of marketing wants better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics.

## Description of all data sources used
The data can be found on divvy bicycle sharing services [website](https://divvy-tripdata.s3.amazonaws.com/index.html). The data has been made available by Motivate International Inc. under this [license](https://ride.divvybikes.com/data-license-agreement). The data is organized monthly in excel sheets.

## Documentation of any cleaning or manipulation of data
The data files were downloaded as .CSV files. I have saved them as an Excel Workbook. I have aligned all the data to the left to make it more uniform looking.

I have added a column “ride_length” that calculates the length of the ride by subtracting the “started_at” column from the “ended_at” column. I changed the format of this column to time HH:MM:SS.

I have added a “day_of_week” column (=WEEKDAY(C2,2)) that shows which day of the week each ride started, numbered from 1 to 7, 1 being Monday and 7 being Sunday.

## Analysis and visualizations
First, I wanted to see what are the total number of trips per month. I used the COUNT function to count the number of “ride_id” per month and then I created a column chart to visualize the data.

<img src="https://user-images.githubusercontent.com/127476880/224261893-a051efa3-33c7-4e01-8a41-a32718de6dc0.png" width="65%" height="65%"/>

There seems to be a trend, let's dig a bit deeper. I want to see if there is any difference between members and casual trips per month. I used the COUNTIF function to count the “member_casual” column so that we can get the monthly number of member and casual trips.

<img src="https://user-images.githubusercontent.com/127476880/224267844-d7f625c0-f7e9-4b5f-b189-cde9afa575e0.png" width="65%" height="65%"/>

The line graph shows that the trend is pretty much the same whether it’s a member or casual user. So now I want to find out what is the possible cause for this trend. 

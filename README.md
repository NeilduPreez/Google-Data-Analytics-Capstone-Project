# Google-Data-Analytics-Capstone-Project

This is the capstone project for the Google Data Analytics Certification. This is my  first project, so I decided to do the entire case study using Microsoft Excel.

## What is the business task?
Cyclistic is a fictional bike-share company in Chicago with more than 5,800 bicycles and 600 docking stations. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members. The director of marketing wants better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics.

## Description of all data sources used
The data can be found on divvy bicycle sharing services [website](https://divvy-tripdata.s3.amazonaws.com/index.html). The data has been made available by Motivate International Inc. under this [license](https://ride.divvybikes.com/data-license-agreement). The data is organized monthly in excel sheets and I used the data from January 2022 to December 2022.

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

I have a theory that there is a correlation between the weather and the number of trips. I created a pivot table to get the daily ride count and I found historical daily weather for Chicago from a website called wunderground.com. I created a scatterplot to visualize the data and you can clearly see the correlation. 

<img src="https://user-images.githubusercontent.com/127476880/224270413-236e7d21-30eb-43ba-b369-60ac2a012ec9.png" width="65%" height="65%"/>

I also used the CORREL function to calculate the correlation coefficient. The correlation coefficient between the daily weather and the daily rides are 0.91, which is a very strong correlation. And it makes sense, people don’t want to be on a bike when it’s cold outside, they would rather take the bus or a car.

The next thing I wanted to find out is: what is the average trip time between members and casual users. I used a pivot table to get the average trip time for members and casual users. I then created a column chart to visualize the data.

<img src="https://user-images.githubusercontent.com/127476880/224274187-0091f742-f019-4bfa-988b-1b386587daa6.png" width="65%" height="65%"/>

On average, casual riders spend more than twice the time on a trip compared to members. This is very interesting and it makes me think that members use the bikes to travel to work and casual riders use it more in a leisure type of way, such as weekends.

So now let’s see what are the number of rides per day of the week for members vs casual users. I created a pivot table to get the number of trips by day of the week for members and casual users. I used a clustered column chart to visualize the data.

<img src="https://user-images.githubusercontent.com/127476880/224274612-678ef2ee-d6a9-4b24-bfd7-a240459f2e11.png" width="65%" height="65%"/>

Our theory was correct, during the week the number of member rides are much more compared to casual users, but on weekends the number of casual users is more than the number of members.

## Recommendations based on my analysis
Cyclistic can look into offering some type of “leisure” annual membership that is only valid on weekends, this way casual users that mostly use the service during weekends are more likely to buy this type of membership, instead of a normal membership.

Based on the correlation of the weather and number of trips, I would recommend that Cyclistic asjust their pricing according to the seasons (increase prices during the summer and decrease the price during the winter).













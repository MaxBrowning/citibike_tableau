# citibike_tableau
Citi Bike is New York City's official bike share. Public data is available for all rides made through the system. The attached dashboards explore three phenomena found in the 2020 data of Citi Bike.

This project is unaffiliated with Citi Bike.

**Data Source**: https://www.citibikenyc.com/system-data

## Phenomena 1: User Demographic Data
![Screencap of Tableau dashboard with no filters selected](https://github.com/MaxBrowning/citibike_tableau/blob/main/Images/Phenomena%201%20User%20Demographic%20Data.JPG)

**Overview:** This dashboard highlights demographic data of bike riders in 2020, particularly highlighting gender, user type, and birth year.
**Analysis:**
On quick glance, three quick inferences can be made:
1) The majority of riders identify as male.
2) The majority of riders are subscribers.
3) The majority of riders were born in 1969.

However, on a closer examination, we can fairly quickly understand one of these phenomena. Filtering the data by 1969 (by clicking on the bar in Birth Year), we can see that an overwhelming majority are customers who did not provide gender data. This seems to suggest that many riders who select 1969 as their birth year are providing dummy information when required. Further examination would be necessary to determine how this impacts the full dataset.

**Interactive:** For greater flexibility in analyzing the data, click on any bar in the graphs to filter the data. For example, clicking on the "Subscriber" bar will filter all other graphs to only show data for subscribers.

## Phenomena 2: Bike Usage Rates
![Screencap of Tableau dashboard with no filters selected](https://github.com/MaxBrowning/citibike_tableau/blob/main/Images/Phenomena%202%20Bike%20Usage%20Rates.JPG)

**Overview:** This dashboard highlights bike usage rates.
**Analysis:**
In 2020, the average bike was ridden just 89 times. Half of bikes were ridden between 44 and 267 times. Our super-performing bikes were those ridden more than 600 times during 2020. These outlier bikes performed well above average. An area of future study would be looking into these bikes to understand if there is a common variable for their high usage rate - are they potentially more likely to be ridden to and from the most popular stations?

One interesting finding is in taking a closer look at the BikeIDs with the longest total trip duration. Each of the top 10 bike saw a greater number of rides from subscribers. They do, however, differ in their number of rides. Only four of the bikes had more than 600 distinct rides, implying that many of these bikes attracted longer rides or rides that were incorrectly ended.

**Interactive:** Click a rectangle in Total Trip Duration By BikeID to jump to that bike in the User Types and Count charts. Click the rectangle a second time to reset the filter.

## Phenomena 3: Station Usage Rates
![Screencap of six Cit iBike station maps with varying displays](https://github.com/MaxBrowning/citibike_tableau/blob/main/Images/Bike%20Station%20Usage%20Rates.JPG)

**Key:** Dark blue, larger circles indicate higher values whereas light teal, smaller circles indicate smaller values.
**Overview:** While "most popular" is generally used to imply count, popular bike stations may also be defined as those that attract longer rides. For this visual, I am looking at all 2020 data.

**Analysis:**
Very quickly we can see that area code 07302 have the most active bike stations, followed closely by 07306, 07304, and 07310.

There appears to be an anomaly when looking at the average trip length by ending station. Most maps do not attribute many rides to beginning or ending on the eastern portion of the map; however, we can see on the bottom-middle graph that the eastern stations have the longest average trips. This very likely points to a flaw in the data, rather than a trend, as the largest station averaged trips at more than 1 million seconds, despite not appearing on other lists.

Many stations show similar popularity as start and ending stations, indicating that they are likely in better locations. Likewise, stations that are less popular as starting stations were generally less popular as ending stations.

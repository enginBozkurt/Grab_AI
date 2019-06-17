# Grab_AI
Traffic  Management Project

![Screenshot_2](https://user-images.githubusercontent.com/30608533/59575813-a6a06f80-90c5-11e9-83fa-b9680dbe7170.jpg)


## PROBLEM STATEMENT

Economies in Southeast Asia are turning to AI to solve traffic congestion, which hinders mobility and economic growth. 

The first step in the push towards alleviating traffic congestion is to understand travel demand and travel patterns within the city.

Can we accurately forecast travel demand based on historical Grab bookings to predict areas and times with high travel demand?


## Dataset:
The given dataset contains normalized historical demand of a city, aggregated spatiotemporally within geohashes and over 15-minute intervals. The dataset spans over a two month period.


geohash6: encoded geographic location

day: days follow a sequential order and not a particular day of the month

timestamp: 15-minute intervals

demand: aggregated demand normalized with values from 0 to 1



## Exploratory Data Analysis

We can make the following assumptions and draw some conclusions from them about the trends in data:

- From the demand by day graphs, it is obvious that the demands are increasing in every five days and then we could notice the low demand in the following two days.
- From the demand by location (latitude and longitude) graphs, the southern and central locations have high demand.
- An interesting issue is that most of the coordinates lie in the Indian ocean.


## Feature Engineering

![cyclic-numeric-feature-transformation](https://user-images.githubusercontent.com/30608533/59575774-7ce74880-90c5-11e9-9f1a-2d9dd441a89f.png)



- I grouped the entire dataset by time (binned into quarter hours).
- I also added additional features based on the time and day of the week. 
- These features are transformed into sine and cosine forms for catching the relationship in cyclic numerical features.




## Machine Learning Approach
- Random Forest regression
The results show that the ability of the Random Forest algorithm is  to capture the complexities in the features, especially latitude and longitude

## Further improvements
 For further improvement,  Apache Spark can be used as Spark clusters for high-performance models.

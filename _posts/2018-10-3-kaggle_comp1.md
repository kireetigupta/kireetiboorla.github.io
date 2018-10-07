---
layout: post
title: "New York taxi time prediction"
date: 2018-03-16
---
Will be following this kernel for my EDA: https://www.kaggle.com/headsortails/nyc-taxi-eda-update-the-fast-the-curious


## Individual Feature Visualization

### Start and end locations.
Need to learn to plot geo data on maps in python.  **To do**

### Trip Duration
 1. Plot a histogram with log-x scale

### Other Visualizations
histograms of vndor_id,passenger_count,
plot number of pick ups per day, hour

## To do
1. Reformatting features
   1. break date-time into date and time columns
   2. 
2. checking consistency: Ideal to check for some consistency between columns that are related.
  1. trip_duration is based on pickup_datetime, dropoff_datetime ?
3. Visualization
  1. start,end locations on maps
  2. duration vs count
  3. other columns vs count
4. Feature selection
  1. day of the week vs Duration
  2. hour of the day vs duration
  3. month vs duration
  4. passenger_count vs duration
  5. passenger_count, vendor_id vs duration
5. Feature engineering
  1. trip distance
  2. trip speed
  3. bearing direction
  4. airport distance
6. Data Cleaning
  1. rows with longer than a day duration
  2. close to 24 hour trips with shorter distances.
  3. shorter than few minutes
  4. filter based on trip duration (less than 10 seconds, more than a day with lesser distance)\
  5. filter based on speed of the car( less than 100kmph


## TO learn
1. Kernel density estimation
2. distplot with just data being transformed as log but not the scale.
3.

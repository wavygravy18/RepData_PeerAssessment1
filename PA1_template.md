# Reproducible Research: Peer Assessment 1
## Loading and preprocessing the data

```r
library(knitr)
opts_chunk$set(echo = FALSE, results='asis')
```


## What is mean total number of steps taken per day?

Here is a histogram of the total number of steps per day.

```
## 
## Attaching package: 'dplyr'
```

```
## The following object is masked from 'package:stats':
## 
##     filter
```

```
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

![](PA1_template_files/figure-html/historgram-1.png)

Here is the mean total number of steps taken per day.
[1] 10766.19

Here is the median total number of steps taken per day.
[1] 10765

## What is the average daily activity pattern?

![](PA1_template_files/figure-html/averageactivitypattern-1.png)

The 5-minute interval, averaged across days, that contains the highest number of steps is:
Source: local data frame [1 x 2]

  interval mean_steps
1      835   206.1698

## Imputing missing values
The number of missing values is:
[1] 2304


This code replaces the missing values with the average for each interval.

```
## 
## Attaching package: 'data.table'
```

```
## The following objects are masked from 'package:dplyr':
## 
##     between, last
```

Here is a histogram of the total number of steps per day with the missing values filled in.
![](PA1_template_files/figure-html/NAsreplaced historgram-1.png)

Here is the mean total number of steps taken per day with the missing values filled in.
[1] 10766.19

Here is the median total number of steps taken per day with the missing values filled in.
[1] 10766.19


Yes, replacing the missing values does have an effect on the data. The columns in the replaced histogram are a little taller because now they have more data to count and the mean and median are the same in the new histogram.

## Are there differences in activity patterns between weekdays and weekends?

![](PA1_template_files/figure-html/weekdaysversusweekends-1.png)

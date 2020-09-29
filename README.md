# -Reproducible-Research-Course-Project-1

## Step 1  ## Code for reading in the dataset and/or processing the data

activity<-read.csv("activity.csv")

Exploring the basics of this data
```
dim(activity)
names(activity)
head(activity)
str(activity)
#total number of missing data
sum(is.na(activity$steps))/dim(activity)[[1]]
#transforming the date column into date format using lubridate
library(lubridate)
activity$date<-ymd(activity$date)
length(unique(activity$date))
```

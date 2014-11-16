First assignment
========================================================

First I read the activity.csv file:


```r
data = read.csv("activity.csv")
#head(data)
```

I plot a histogram and calculate mean and median:


```r
dataFactor <- as.factor(data$date)
stepsPerDay <- by(data$steps,dataFactor,sum, na.rm = F)
#stepsPerDay

#str(stepsPerDay)
histogram = hist(stepsPerDay, breaks = 100)
```

![plot of chunk unnamed-chunk-2](figure/unnamed-chunk-2.png) 

```r
meanValue = mean(stepsPerDay, na.rm = T)
meanValue
```

```
## [1] 10766
```

```r
medianValue = median(stepsPerDay, na.rm = T)
medianValue
```

```
## [1] 10765
```



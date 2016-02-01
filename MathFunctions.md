# Introduction #

> This page describes the usage for some math functions available on time series

# Details #

## Merge Time Series ##

Creates two regular time series with non-overlapping timewindows and merges them
using default settings. Gap is filled by missing values (-901.0 per HEC-DSS conventions)
```
>>> from vutils import *
>>> rts1=RegularTimeSeries('rts1','01jan1980 0100','1hour',[1,2,3,4,5])
>>> rts2=RegularTimeSeries('rts2','02jan1980 0100','1hour',[10,20,30,40,50])
>>> mrts=merge([rts1,rts2])
>>> from vdisplay import *
>>> tabulate(rts1,rts2,mrts)
```

## Moving Average, Period Average of Time Series ##

The functions for math operation are available in [vmath](http://dsm2-vista.googlecode.com/svn/trunk/vista/doc/pydocs/vmath.html). To do a moving average simply call vmath.mov\_avg with the desired back length and forward length
```
>>> import vmath
>>> time_series_weekly_avg = vmath.mov_avg(time_series,7,7)
```
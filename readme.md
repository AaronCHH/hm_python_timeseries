# Python-Time Series

[![hackmd-github-sync-badge](https://hackmd.io/GzREUXa0Tm6o3sbQLharmw/badge)](https://hackmd.io/GzREUXa0Tm6o3sbQLharmw)

## Book Chapter
* [McKinney(2022), Python for Data Analysis 3E, O'Reilly](https://www.oreilly.com/library/view/python-for-data/9781098104023/) | Ch11

## Books
* [Pal(2017), *Practical Time Series Analysis*, Packt](https://www.packtpub.com/product/practical-time-series-analysis/9781788290227)
* [Nielsen(2022), *Practical Time Series Analysis*, O'Reilly](https://www.oreilly.com/library/view/practical-time-series/9781492041641/)
----
## pd.date_range
```python==
dates = pd.date_range(start="2017-04-01", end="2017-04-30")
```

## modules
* [Time series - date functionality](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#timeseries-offset-aliases)
* [pandas.to_datetime](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html)
* [pandas.date_range](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html)

## Basic Conversion
* string to time
```python=
datetime.strptime('2018/7/11', '%Y/%m/%d')
```

* time to string
```python=
datetime.strftime(date.today(), '%Y/%m/%d')
```
or
```python=
date.today().strftime('%Y/%m/%d')
```

## [Python strptime()](https://www.programiz.com/python-programming/datetime/strptime)
* Example 1: string to datetime object
```python=
from datetime import datetime

date_string = "21 June, 2018"

print("date_string =", date_string)
print("type of date_string =", type(date_string))

date_object = datetime.strptime(date_string, "%d %B, %Y")

print("date_object =", date_object)
print("type of date_object =", type(date_object))
```
* Example 2: string to datetime object
```python=
from datetime import datetime

dt_string = "12/11/2018 09:15:32"

# Considering date is in dd/mm/yyyy format
dt_object1 = datetime.strptime(dt_string, "%d/%m/%Y %H:%M:%S")
print("dt_object1 =", dt_object1)

# Considering date is in mm/dd/yyyy format
dt_object2 = datetime.strptime(dt_string, "%m/%d/%Y %H:%M:%S")
print("dt_object2 =", dt_object2)
```

## [Python strftime()](https://www.programiz.com/python-programming/datetime/strftime)
* Example 1: datetime to string using strftime()
```python=
from datetime import datetime

now = datetime.now() # current date and time

year = now.strftime("%Y")
print("year:", year)

month = now.strftime("%m")
print("month:", month)

day = now.strftime("%d")
print("day:", day)

time = now.strftime("%H:%M:%S")
print("time:", time)

date_time = now.strftime("%m/%d/%Y, %H:%M:%S")
print("date and time:",date_time)	
```

* Example 2: Creating string from a timestamp
```python=
from datetime import datetime

timestamp = 1528797322
date_time = datetime.fromtimestamp(timestamp)

print("Date time object:", date_time)

d = date_time.strftime("%m/%d/%Y, %H:%M:%S")
print("Output 2:", d)	

d = date_time.strftime("%d %b, %Y")
print("Output 3:", d)

d = date_time.strftime("%d %B, %Y")
print("Output 4:", d)

d = date_time.strftime("%I%p")
print("Output 5:", d)
```


## Pandas
* string to time format
```python=
pd.to_datetime([sequence of objects])
# [sequence of objects]: string list, or series
```

* time to string format
```python=
from datetime import datetime

head_range = pd.date_range(start='2014-12-30', end='2015-01-05')

df = pd.DataFrame()
df['time_data'] = head_range
df['time_data2']= df['time_data'].apply(lambda x: datetime.strftime(x, '%Y-%m-%d'))
df['time_data3']= df['time_data'].apply(lambda x: x.strftime('%Y-%m-%d'))
df
```

* [pandas time range to string list](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html)
```python=
from datetime import datetime

head_range = pd.date_range(start='2014-12-30', end='2015-01-05')

dateList = [x.strftime('%Y-%m-%d') for x in head_range]
dateList
```
>>>>>>> eed1a419a1a76e726d07de2da1b60c255a75457f

## Tips
* [使用python插補時間序列](https://kknews.cc/zh-tw/code/52brmp2.html)
* [How to Convert Strings to Datetime in Pandas DataFrame](https://datatofish.com/strings-to-datetime-pandas/)
<<<<<<< HEAD
=======
* [Pandas resample() tricks you should know for manipulating time-series data](https://towardsdatascience.com/pandas-resample-tricks-you-should-know-for-manipulating-time-series-data-7e9643a7e7f3)

###### tags: `time series` `ts` `time` `python`# Python-Time Series

[![hackmd-github-sync-badge](https://hackmd.io/GzREUXa0Tm6o3sbQLharmw/badge)](https://hackmd.io/GzREUXa0Tm6o3sbQLharmw)

## Book Chapter
* [McKinney(2022), Python for Data Analysis 3E, O'Reilly](https://www.oreilly.com/library/view/python-for-data/9781098104023/) | Ch11

## Books
* [Pal(2017), *Practical Time Series Analysis*, Packt](https://www.packtpub.com/product/practical-time-series-analysis/9781788290227)
* [Nielsen(2022), *Practical Time Series Analysis*, O'Reilly](https://www.oreilly.com/library/view/practical-time-series/9781492041641/)
----
## pd.date_range
```python==
dates = pd.date_range(start="2017-04-01", end="2017-04-30")
```

## modules
* [Time series - date functionality](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#timeseries-offset-aliases)
* [pandas.to_datetime](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html)
* [pandas.date_range](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html)

## Basic Conversion
* string to time
```python=
datetime.strptime('2018/7/11', '%Y/%m/%d')
```

* time to string
```python=
datetime.strftime(date.today(), '%Y/%m/%d')
```
or
```python=
date.today().strftime('%Y/%m/%d')
```

## [Python strptime()](https://www.programiz.com/python-programming/datetime/strptime)
* Example 1: string to datetime object
```python=
from datetime import datetime

date_string = "21 June, 2018"

print("date_string =", date_string)
print("type of date_string =", type(date_string))

date_object = datetime.strptime(date_string, "%d %B, %Y")

print("date_object =", date_object)
print("type of date_object =", type(date_object))
```
* Example 2: string to datetime object
```python=
from datetime import datetime

dt_string = "12/11/2018 09:15:32"

# Considering date is in dd/mm/yyyy format
dt_object1 = datetime.strptime(dt_string, "%d/%m/%Y %H:%M:%S")
print("dt_object1 =", dt_object1)

# Considering date is in mm/dd/yyyy format
dt_object2 = datetime.strptime(dt_string, "%m/%d/%Y %H:%M:%S")
print("dt_object2 =", dt_object2)
```

## [Python strftime()](https://www.programiz.com/python-programming/datetime/strftime)
* Example 1: datetime to string using strftime()
```python=
from datetime import datetime

now = datetime.now() # current date and time

year = now.strftime("%Y")
print("year:", year)

month = now.strftime("%m")
print("month:", month)

day = now.strftime("%d")
print("day:", day)

time = now.strftime("%H:%M:%S")
print("time:", time)

date_time = now.strftime("%m/%d/%Y, %H:%M:%S")
print("date and time:",date_time)	
```

* Example 2: Creating string from a timestamp
```python=
from datetime import datetime

timestamp = 1528797322
date_time = datetime.fromtimestamp(timestamp)

print("Date time object:", date_time)

d = date_time.strftime("%m/%d/%Y, %H:%M:%S")
print("Output 2:", d)	

d = date_time.strftime("%d %b, %Y")
print("Output 3:", d)

d = date_time.strftime("%d %B, %Y")
print("Output 4:", d)

d = date_time.strftime("%I%p")
print("Output 5:", d)
```


## Pandas
* string to time format
```python=
pd.to_datetime([sequence of objects])
# [sequence of objects]: string list, or series
```
# Python-Time Series

[![hackmd-github-sync-badge](https://hackmd.io/GzREUXa0Tm6o3sbQLharmw/badge)](https://hackmd.io/GzREUXa0Tm6o3sbQLharmw)

## Book Chapter
* [McKinney(2022), Python for Data Analysis 3E, O'Reilly](https://www.oreilly.com/library/view/python-for-data/9781098104023/) | Ch11

## Books
* [Pal(2017), *Practical Time Series Analysis*, Packt](https://www.packtpub.com/product/practical-time-series-analysis/9781788290227)
* [Nielsen(2022), *Practical Time Series Analysis*, O'Reilly](https://www.oreilly.com/library/view/practical-time-series/9781492041641/)
----
## pd.date_range
```python==
dates = pd.date_range(start="2017-04-01", end="2017-04-30")
```

## modules
* [Time series - date functionality](https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html#timeseries-offset-aliases)
* [pandas.to_datetime](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html)
* [pandas.date_range](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html)

## Basic Conversion
* string to time
```python=
datetime.strptime('2018/7/11', '%Y/%m/%d')
```

* time to string
```python=
datetime.strftime(date.today(), '%Y/%m/%d')
```
or
```python=
date.today().strftime('%Y/%m/%d')
```

## [Python strptime()](https://www.programiz.com/python-programming/datetime/strptime)
* Example 1: string to datetime object
```python=
from datetime import datetime

date_string = "21 June, 2018"

print("date_string =", date_string)
print("type of date_string =", type(date_string))

date_object = datetime.strptime(date_string, "%d %B, %Y")

print("date_object =", date_object)
print("type of date_object =", type(date_object))
```
* Example 2: string to datetime object
```python=
from datetime import datetime

dt_string = "12/11/2018 09:15:32"

# Considering date is in dd/mm/yyyy format
dt_object1 = datetime.strptime(dt_string, "%d/%m/%Y %H:%M:%S")
print("dt_object1 =", dt_object1)

# Considering date is in mm/dd/yyyy format
dt_object2 = datetime.strptime(dt_string, "%m/%d/%Y %H:%M:%S")
print("dt_object2 =", dt_object2)
```

## [Python strftime()](https://www.programiz.com/python-programming/datetime/strftime)
* Example 1: datetime to string using strftime()
```python=
from datetime import datetime

now = datetime.now() # current date and time

year = now.strftime("%Y")
print("year:", year)

month = now.strftime("%m")
print("month:", month)

day = now.strftime("%d")
print("day:", day)

time = now.strftime("%H:%M:%S")
print("time:", time)

date_time = now.strftime("%m/%d/%Y, %H:%M:%S")
print("date and time:",date_time)	
```

* Example 2: Creating string from a timestamp
```python=
from datetime import datetime

timestamp = 1528797322
date_time = datetime.fromtimestamp(timestamp)

print("Date time object:", date_time)

d = date_time.strftime("%m/%d/%Y, %H:%M:%S")
print("Output 2:", d)	

d = date_time.strftime("%d %b, %Y")
print("Output 3:", d)

d = date_time.strftime("%d %B, %Y")
print("Output 4:", d)

d = date_time.strftime("%I%p")
print("Output 5:", d)
```


## Pandas
* string to time format
```python=
pd.to_datetime([sequence of objects])
# [sequence of objects]: string list, or series
```

* time to string format
```python=
from datetime import datetime

head_range = pd.date_range(start='2014-12-30', end='2015-01-05')

df = pd.DataFrame()
df['time_data'] = head_range
df['time_data2']= df['time_data'].apply(lambda x: datetime.strftime(x, '%Y-%m-%d'))
df['time_data3']= df['time_data'].apply(lambda x: x.strftime('%Y-%m-%d'))
df
```

* [pandas time range to string list](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html)
```python=
from datetime import datetime

head_range = pd.date_range(start='2014-12-30', end='2015-01-05')

dateList = [x.strftime('%Y-%m-%d') for x in head_range]
dateList
```

## Tips
* [使用python插補時間序列](https://kknews.cc/zh-tw/code/52brmp2.html)
* [How to Convert Strings to Datetime in Pandas DataFrame](https://datatofish.com/strings-to-datetime-pandas/)
* [Pandas resample() tricks you should know for manipulating time-series data](https://towardsdatascience.com/pandas-resample-tricks-you-should-know-for-manipulating-time-series-data-7e9643a7e7f3)

###### tags: `time series` `ts` `time` `python`
* time to string format
```python=
from datetime import datetime

head_range = pd.date_range(start='2014-12-30', end='2015-01-05')

df = pd.DataFrame()
df['time_data'] = head_range
df['time_data2']= df['time_data'].apply(lambda x: datetime.strftime(x, '%Y-%m-%d'))
df['time_data3']= df['time_data'].apply(lambda x: x.strftime('%Y-%m-%d'))
df
```

* [pandas time range to string list](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.date_range.html)
```python=
from datetime import datetime

head_range = pd.date_range(start='2014-12-30', end='2015-01-05')

dateList = [x.strftime('%Y-%m-%d') for x in head_range]
dateList
```

## Tips
* [使用python插補時間序列](https://kknews.cc/zh-tw/code/52brmp2.html)
* [How to Convert Strings to Datetime in Pandas DataFrame](https://datatofish.com/strings-to-datetime-pandas/)
* [Pandas resample() tricks you should know for manipulating time-series data](https://towardsdatascience.com/pandas-resample-tricks-you-should-know-for-manipulating-time-series-data-7e9643a7e7f3)

###### tags: `time series` `ts` `time` `python`
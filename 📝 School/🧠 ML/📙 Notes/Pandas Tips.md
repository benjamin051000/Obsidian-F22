# Helpful Pandas functions

```python
from pandas import DatetimeIndex as dt

# given a pandas DataFrame...
df = pd.read_csv(...)

# Makes a df with just the day, int encoded (Monday = 0)
day_of_week = pd.to_datetime(df["Date"]).dt.dayofweek

# Encode times as morning, afternoon, evening, night
pd.to_datetime(df["Time"]).dt.strftime("%H").astype("float")

hour_cat = pd.cut(hour, bins=[])...
```


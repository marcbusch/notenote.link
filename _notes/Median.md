---
title: Median
---
# Median

The **median** (or 50th percentile) is defined as the center value of an ordered array (or set of data points). If it lies between two values, the average of these two values is taken.

SQL:
```sql
  PERCENTILE_CONT(x, 0.5) OVER() AS median
```
Python:
```python
# pandas
mean = df_data.median()

# statistics
import statistics
median = statistics.median(array)
```

---
related to: [[Estimates of Location]] - [[Mean]] - [[Mode]]

references:
#type/🌲
#status/🟡

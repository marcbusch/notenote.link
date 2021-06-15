---
---
# Mean
The **mean** (or **average**) is defined as:

>$$\bar{x}=\frac{\sum_i^nx_i}{n}$$

## Trimmed mean
The mean is sensitive to outliers. In many situations it is therefore better to use the **trimmed mean** (i.e. excluding a fraction of the ordered data at the bottom and/or top).

Notes:
- The mean reflects the central tendency (i.e. *typical value*) only for normally distributed data


SQL:
```sql
  AVG(x)
```

Python:
```python
# pandas
mean = df_data.mean()

# statistics
import statistics
mean = statistics.mean(array)

#trimmed mean --> scipy
from scipy import stats
trimmed_mean = stats.trim_mean(array, 0.1)
```

---
related to: [[Estimates of Location]] - [[Median]] - [[Mode]]

#type/🌲
#status/🟡

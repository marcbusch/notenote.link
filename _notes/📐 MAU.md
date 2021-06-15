---
title: 📐 MAU
---
# 📐 MAU (monthly active user)
## Definition
>A **MAU** (monthly active user) for a specific day is a user who performed a [[meaningful activity]] within 30 days before (or on) that day.

## Notes
- When reporting monthly MAU numbers always check for is_mau **on the last day of the month** (end of month, EOM). See the example below.

## Data
field: `is_mau`

## Example
*Number of MAU users on the EU platform for each month of 2021:*
```sql
SELECT
  date,
  COUNTIF(is_mau) as number_of_MAUs
FROM
  miamed_bi_test_view.active_user_accounts_info_mat
WHERE
  region = 'eu'
  AND EXTRACT(YEAR FROM DATE(date)) = 2021
  AND EXTRACT(DAY FROM DATE(date)+1) = 1  --> last day of the month
GROUP BY 1
ORDER BY 1
```
---
related to: [[📐 DAU]] - [[📐 WAU]]
tags: #📐
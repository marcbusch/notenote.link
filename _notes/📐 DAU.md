---
title: 📐 DAU
---
# 📐 DAU (daily active user)
Definition:
>A **DAU** (daily active user) for a specific day is a user who performed a [[meaningful activity]] during the day.

## Data
field: `is_dau`

## Example
*Yesterday's number of active users on the EU platform:*
```sql
SELECT
  COUNTIF(is_dau) as number_of_DAUs
FROM
  miamed_bi_test_view.active_user_accounts_info_mat
WHERE
  region = 'eu'
  AND DATE(date) = CURRENT_DATE-1
```
---
related to: [[📐 WAU]] - [[📐 MAU]]

tags: #📐
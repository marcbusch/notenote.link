---
title: 📐 WAU
---
# 📐 WAU (weekly active user)
Definition:
>A **WAU** (weekly active user) for a specific day is a user who performed a [[meaningful activity]] within 7 days before (or on) that day.

## Data
field: `is_wau`

## Example
*Yesterday's number of weekly active users on the EU platform:*
```sql
SELECT
  COUNTIF(is_wau) as number_of_WAUs
FROM
  miamed_bi_test_view.active_user_accounts_info_mat
WHERE
  region = 'eu'
  AND DATE(date) = CURRENT_DATE-1
```
---
related to: [[📐 DAU]] - [[📐 MAU]]
tags: #📐
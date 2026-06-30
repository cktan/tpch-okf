---
type: Metric
title: Total Revenue
description: Sum of sales billing after discount is subtracted.
tags: [kpi, finance, revenue]
---

# Total Revenue

## Definition
Calculated as the sum of `l_extendedprice * (1 - l_discount)` across transactions.

## Query Formula

```sql
SELECT SUM(l_extendedprice * (1 - l_discount)) AS total_revenue
FROM lineitem;
```

## Source Fields
* Table: [Lineitem](../tables/lineitem.md)
* Fields: `l_extendedprice`, `l_discount`

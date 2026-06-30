---
type: Metric
title: Average Discount
description: The average discount percentage applied to order lines.
tags: [kpi, pricing]
---

# Average Discount

## Definition
Calculated as the arithmetic mean of the discount value applied to all line items.

## Query Formula

```sql
SELECT AVG(l_discount) AS average_discount
FROM lineitem;
```

## Source Fields
* Table: [Lineitem](../tables/lineitem.md)
* Fields: `l_discount`

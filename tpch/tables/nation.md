---
type: Table
title: Nation Table
description: Defines the nations associated with regions.
resource: tpch.nation
tags: [dimension, geography]
---

# Nation Table

Stores national jurisdictions mapped to geographic regions.

## Schema

| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `n_nationkey` | INTEGER | PRIMARY KEY | Unique nation key |
| `n_name` | CHAR(25) | NOT NULL | Nation name |
| `n_regionkey` | INTEGER | FOREIGN KEY | References [Region](region.md) |
| `n_comment` | VARCHAR(152) | | Remarks / notes |

## Relationships

* Child of [Region](region.md) via `n_regionkey`.
* Parent of [Supplier](supplier.md) via `s_nationkey`.
* Parent of [Customer](customer.md) via `c_nationkey`.

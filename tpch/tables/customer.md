---
type: Table
title: Customer Table
description: Stores buyer profile information.
resource: tpch.customer
tags: [dimension, customer]
---

# Customer Table

Stores details about customer accounts, geographic locations, and market segments.

## Schema

| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `c_custkey` | INTEGER | PRIMARY KEY | Unique customer identifier |
| `c_name` | VARCHAR(25) | NOT NULL | Customer name |
| `c_address` | VARCHAR(40) | NOT NULL | Customer address |
| `c_nationkey` | INTEGER | FOREIGN KEY | References [Nation](nation.md) |
| `c_phone` | CHAR(15) | NOT NULL | Phone number |
| `c_acctbal` | DECIMAL(15,2)| NOT NULL | Current account balance |
| `c_mktsegment` | CHAR(10) | NOT NULL | Market segment |
| `c_comment` | VARCHAR(117)| NOT NULL | Remarks and notes |

## Relationships

* Child of [Nation](nation.md) via `c_nationkey`.
* Parent of [Orders](orders.md) via `o_custkey`.

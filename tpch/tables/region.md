---
type: Table
title: Region Table
description: Defines the geographic regions for suppliers and customers.
resource: tpch.region
tags: [dimension, geography]
---

# Region Table

Stores regional geographic groupings (e.g., AFRICA, ASIA, EUROPE).

## Schema

| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `r_regionkey` | INTEGER | PRIMARY KEY | Unique region key |
| `r_name` | CHAR(25) | NOT NULL | Region name |
| `r_comment` | VARCHAR(152) | | Remarks / notes |

## Relationships

* Parent of [Nation](nation.md) via `r_regionkey`.

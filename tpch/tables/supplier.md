---
type: Table
title: Supplier Table
description: Stores details on companies supplying parts.
resource: tpch.supplier
tags: [dimension, supplier]
---

# Supplier Table

Stores supplier profiles, country location, contact details, and account balances.

## Schema

| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `s_suppkey` | INTEGER | PRIMARY KEY | Unique supplier identifier |
| `s_name` | CHAR(25) | NOT NULL | Supplier name |
| `s_address` | VARCHAR(40) | NOT NULL | Address |
| `s_nationkey` | INTEGER | FOREIGN KEY | References [Nation](nation.md) |
| `s_phone` | CHAR(15) | NOT NULL | Phone number |
| `s_acctbal` | DECIMAL(15,2)| NOT NULL | Account balance |
| `s_comment` | VARCHAR(101)| NOT NULL | Remarks and notes |

## Relationships

* Child of [Nation](nation.md) via `s_nationkey`.
* Parent of [PartSupp](partsupp.md) via `ps_suppkey`.
* Parent of [Lineitem](lineitem.md) via `l_suppkey`.

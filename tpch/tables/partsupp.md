---
type: Table
title: Part Supplier Table
description: Bridge table defining parts supplied by each supplier and costs.
resource: tpch.partsupp
tags: [bridge, inventory]
---

# Part Supplier Table

Tracks the wholesale inventory relationship between parts and suppliers.

## Schema

| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `ps_partkey` | INTEGER | PRIMARY KEY, FK | References [Part](part.md) |
| `ps_suppkey` | INTEGER | PRIMARY KEY, FK | References [Supplier](supplier.md) |
| `ps_availqty` | INTEGER | NOT NULL | Available inventory quantity |
| `ps_supplycost` | DECIMAL(15,2)| NOT NULL | Unit supply cost |
| `ps_comment` | VARCHAR(199)| NOT NULL | Remarks and notes |

## Relationships

* Child of [Part](part.md) via `ps_partkey`.
* Child of [Supplier](supplier.md) via `ps_suppkey`.
* Parent of [Lineitem](lineitem.md) via composite join key (`ps_partkey`, `ps_suppkey`) -> (`l_partkey`, `l_suppkey`).

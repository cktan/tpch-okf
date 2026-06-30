---
type: Table
title: Part Table
description: Stores description of parts available for manufacturing or sale.
resource: tpch.part
tags: [dimension, product]
---

# Part Table

Stores part details, size, container, manufacturer, and pricing catalog.

## Schema

| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `p_partkey` | INTEGER | PRIMARY KEY | Unique part identifier |
| `p_name` | VARCHAR(55) | NOT NULL | Part name |
| `p_mfgr` | CHAR(25) | NOT NULL | Manufacturer identifier |
| `p_brand` | CHAR(10) | NOT NULL | Brand designation |
| `p_type` | VARCHAR(25) | NOT NULL | Part category type |
| `p_size` | INTEGER | NOT NULL | Dimensions / size |
| `p_container` | CHAR(10) | NOT NULL | Container type |
| `p_retailprice` | DECIMAL(15,2)| NOT NULL | Standard retail price |
| `p_comment` | VARCHAR(23) | NOT NULL | Remarks and notes |

## Relationships

* Parent of [PartSupp](partsupp.md) via `ps_partkey`.
* Parent of [Lineitem](lineitem.md) via `l_partkey`.

---
type: Table
title: Lineitem Table
description: Detailed transaction items (the primary facts).
resource: tpch.lineitem
tags: [fact, sales]
---

# Lineitem Table

Granular transactional lines representing items purchased under parent orders. This is the largest fact table in TPC-H.

## Schema

| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `l_orderkey` | INTEGER | PRIMARY KEY, FK | References [Orders](orders.md) |
| `l_partkey` | INTEGER | FOREIGN KEY | References [Part](part.md) |
| `l_suppkey` | INTEGER | FOREIGN KEY | References [Supplier](supplier.md) |
| `l_linenumber` | INTEGER | PRIMARY KEY | Line item index number |
| `l_quantity` | DECIMAL(15,2)| NOT NULL | Quantity shipped |
| `l_extendedprice`| DECIMAL(15,2)| NOT NULL | Base unit price * quantity |
| `l_discount` | DECIMAL(15,2)| NOT NULL | Applied discount rate (0.00 to 1.00) |
| `l_tax` | DECIMAL(15,2)| NOT NULL | Applied tax rate |
| `l_returnflag` | CHAR(1) | NOT NULL | Return code (A, N, R) |
| `l_linestatus` | CHAR(1) | NOT NULL | Execution status (O, F) |
| `l_shipdate` | DATE | NOT NULL | Shipment date |
| `l_commitdate` | DATE | NOT NULL | Seller's commitment date |
| `l_receiptdate` | DATE | NOT NULL | Buyer's delivery receipt date |
| `l_shipinstruct` | CHAR(25) | NOT NULL | Delivery instructions |
| `l_shipmode` | CHAR(10) | NOT NULL | Shipping transport method |
| `l_comment` | VARCHAR(44) | NOT NULL | Remarks and notes |

## Relationships

* Child of [Orders](orders.md) via `l_orderkey`.
* Child of [Part](part.md) via `l_partkey`.
* Child of [Supplier](supplier.md) via `l_suppkey`.
* Child of [PartSupp](partsupp.md) via composite join key (`l_partkey`, `l_suppkey`) -> (`ps_partkey`, `ps_suppkey`).

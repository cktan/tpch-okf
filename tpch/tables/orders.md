---
type: Table
title: Orders Table
description: Stores header transactions for customer orders.
resource: tpch.orders
tags: [transaction, sales]
---

# Orders Table

Main transactional header representing checkout orders placed by customers.

## Schema

| Column Name | Data Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `o_orderkey` | INTEGER | PRIMARY KEY | Unique order key |
| `o_custkey` | INTEGER | FOREIGN KEY | References [Customer](customer.md) |
| `o_orderstatus` | CHAR(1) | NOT NULL | Order status (O, F, P) |
| `o_totalprice` | DECIMAL(15,2)| NOT NULL | Total transaction price |
| `o_orderdate` | DATE | NOT NULL | Creation date of order |
| `o_orderpriority`| CHAR(15) | NOT NULL | Priority class |
| `o_clerk` | CHAR(15) | NOT NULL | Processing clerk ID |
| `o_shippriority` | INTEGER | NOT NULL | Priority rating for shipment |
| `o_comment` | VARCHAR(79) | NOT NULL | Remarks / notes |

## Relationships

* Child of [Customer](customer.md) via `o_custkey`.
* Parent of [Lineitem](lineitem.md) via `l_orderkey`.

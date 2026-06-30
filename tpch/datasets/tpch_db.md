---
type: Dataset
title: TPC-H relational database
description: The main 3NF database modeling a global wholesale supplier transaction workload.
resource: jdbc:postgresql://localhost:5432/tpch
tags: [benchmark, OLAP]
---

# TPC-H Database

This database contains 8 tables modeling part sales, supplier relationships, inventory tracking, and customer orders.

## Tables Included

* [Region](../tables/region.md)
* [Nation](../tables/nation.md)
* [Supplier](../tables/supplier.md)
* [Part](../tables/part.md)
* [PartSupp](../tables/partsupp.md)
* [Customer](../tables/customer.md)
* [Orders](../tables/orders.md)
* [Lineitem](../tables/lineitem.md)

---
type: Index
title: TPC-H Tables Index
description: List of the 8 tables comprising the TPC-H decision support benchmark.
---

# TPC-H Database Tables

The database is structured in 3rd Normal Form (3NF) to support ad-hoc decision support query workloads.

## Dimension-like Tables

* [Region](region.md) - Geographic regions.
* [Nation](nation.md) - Nations associated with regions.
* [Supplier](supplier.md) - Suppliers of parts.
* [Part](part.md) - Parts catalog.
* [Customer](customer.md) - Customer profiles.

## Fact-like & Transactional Tables

* [PartSupp](partsupp.md) - Part-supplier relationship and inventory costs.
* [Orders](orders.md) - Customer transactions headers.
* [Lineitem](lineitem.md) - Granular item details (primary fact table).

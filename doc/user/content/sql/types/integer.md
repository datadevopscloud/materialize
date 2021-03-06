---
title: "Integer Data Types"
description: "Express signed integers"
menu:
  main:
    parent: 'sql-types'
aliases:
  - /sql/types/bigint
  - /sql/types/int
  - /sql/types/int4
  - /sql/types/int8
---

## `integer` info

Detail | Info
-------|------
**Size** | 4 bytes
**Aliases** | `int`, `int4`
**Catalog name** | `pg_catalog.int4`
**OID** | 23
**Range** | [-2,147,483,648, 2,147,483,647]

## `bigint` info

Detail | Info
-------|------
**Size** | 8 bytes
**Aliases** | `int8`
**Catalog name** | `pg_catalog.int8`
**OID** | 20
**Range** | [-9,223,372,036,854,775,808, 9,223,372,036,854,775,807]

## Details

### Valid casts

In addition to the casts listed below, all integer types can be cast to and from
all other integer types.

#### From `integer` or `bigint`

You can [cast](../../functions/cast) `integer` or `bigint` to:

- [`boolean`](../boolean)
- [`numeric`](../numeric)
- [`real`/`double precision`](../float)
- [`text`](../text)

#### To `integer` or `bigint`

You can [cast](../../functions/cast) the following types to `integer` or `bigint`:

- [`numeric`](../numeric)
- [`real`/`double precision`](../float)

## Examples

```sql
SELECT 123::integer AS int_v;
```
```nofmt
 int_v
-------
   123
```

<hr/>

```sql
SELECT 1.23::integer AS int_v;
```
```nofmt
 int_v
-------
     1
```

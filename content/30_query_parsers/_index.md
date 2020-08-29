---
title: "Query Parsers"
weight: 30
---
The query parser allows for complex filtering, sorting, the use of child relations and more.

Currently the filter parser supports

- columns
- with
- where
- orWhere
- whereIn
- orWhereIn
- whereNotIn
- orWhereNotIn
- whereBetween
- whereNotBetween
- orWhereBetween
- orWhereNotBetween
- withTrashed
- onlyTrashed
- scope
- sort
- join


**sort** allows for multiple sort targets for ascending and descending sorts.

**with** allow for loading child models.

**scope** allows for the use of Laravel query scopes 

**Joins** are also supported

Query results by default return all columns for the query, however you can use the columns filter to restrict which
columns are returned.

---
title: "Query Parsers"
weight: 30
---
The query parser allows for complex filtering, sorting, the use of child relations and more.

Currently the filter parser supports

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
- columns
- withTrashed
- onlyTrashed
- scope
- with
- sort
- join
- limit


**sort** allows for multiple sort targets for ascending and descending sorts.

**with** allow for loading child models.

**scope** allows for the use of Laravel query scopes 

**Joins** are also supported

**Columns** allows for specifying which columns are returned.

**Soft deletes** are also supported with the withTrashed and onlyTrashed filters.


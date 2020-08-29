---
title: "Query Scopes"
weight: 60
---
{{% notice warning %}}
This feature is a bit experimental at the moment.
{{% /notice %}}

example

    scope[]=myscope

Allows the use of [Laravel scopes](<https://laravel.com/docs/7.x/eloquent#query-scopes>)

the **scope** parameter should be the name of your scope less the preceding **scope**

e.g. If your scope is called **scopeActive** then you would just use **active**


---
title: "API Endpoints"
weight: 30
---

The api endpoints provided by the resource controller and extra controller methods provide the following route/actions


**GET api/modelname** -> controller@index 

Allows for query filtering on the url

**GET api/modelname/{id}** -> controller@show

**POST api/modelname** -> controller@store


The request body should be an array of field/values
e.g 

`['name' => 'foo', 'email' => 'bar@test.com']`

**PUT api/modelname/{id}** -> controller@update


The request body should be an array of field/values

e.g 

`['name' => 'foo', 'email' => 'bar@test.com']`

Updates can use filtering e.g.

**PUT api/modelname?where[]=id:eq:2** -> controller@update

**DELETE api/modelname/{id}** - controller@destroy

Deletes can use filtering e.g.

**DELETE api/modelname?where[]=id:eq:2** -> controller@destroy




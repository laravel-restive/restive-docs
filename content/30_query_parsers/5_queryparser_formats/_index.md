---
title: Query Formatting
weight: 5
---

## GET routes

For controller index routes, e.g. GET /resource query parameters are appended to the url.

### examples

given a route such as 

    Restive::resource('user', 'userController')
    
and a base url of 

    domain.com/user
   
query parameters can be added such as :-

    domain.com/user?where[]=status:eq:1&whereBetween[]=age:20:30&withTrashed$sort[]=-age&perPage=20
   
## PUT/DELETE routes

PUT (update) and DELETE routes don;t allow for query parameters in the url. In these cases we need to 
add the Restive query parameters into the body of the request. 

We also need to ensure that those query parameters don;t clash with any model fields we maight be passing
in the request (for model updates).

In these cases we can add a **@parser** field to the request body.

Again, given the route

    Restive::resource('user', 'userController')
    
and using http test code to show the request.

        $response = $this->delete("/user", ['@parser' => ['where' => ['id:eq:2']]]);

        $response = $this->put("/user", [
            'email' => 'dirk@holisticdetective.com',
            'name' => 'Dirk Gently',
            'age' => 45,
            '@parser' => ['where' => ['email:eq:dirk@holisticdetective.com']]
        ]);


     
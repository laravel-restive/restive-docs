---
title: Query Formatting
weight: 5
---

### examples

given a route such as 

    Restive::resource('user', 'userController')
    
and a base url of 

    domain.com/user
   
query parameters can be added such as :-

    domain.com/user?where[]=status:eq:1&whereBetween[]=age:20:30&withTrashed$sort[]=-age&perPage=20
   
## PUT/DELETE routes

PUT (update) and DELETE routes can add query parameters to the URL just like GET routes above,
although some options may not be meaningful in these contexts.

Again, given the route

    Restive::resource('user', 'userController')
    
and using http test code to show the request.

        $response = $this->delete("/user?where[]=id:eq:2");

        $response = $this->put("/user?where[]=email:eq:dirk@holisticdetective.com", [
            'email' => 'dirk@holisticdetective.com',
            'name' => 'Dirk Gently',
            'age' => 45,
        ]);


     
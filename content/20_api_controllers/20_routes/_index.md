---
title: "Routes"
weight: 20
---

Restive uses resource controllers for API routes. 
To define your routes for each controller you will need to add the following to your api routes file.

    Restive::resource('modelName', 'controller');


**modelName** is the model name you want to have api access.


**Controller** is the name of your controller class.

As an example. To use the dummy simple controller supplied by the project, your routing entries would be.

    Restive::resource('dummySimple', 'Api\DummySimpleController');


or to use the default User model that comes with Laravel

    Restive::resource('user', 'Api\UserController');



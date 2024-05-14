---
title: "API Controllers"
weight: 20
---

Restive provides an **ApiController** class that your controllers must [extend]({{< ref "20_api_controllers/10_controller_definition/_index.md" >}} "Controller Definition") to provide 
api access to your models.

Routes must be [defined]({{< ref "20_api_controllers/20_routes/_index.md" >}} "Routes") for each model you want to access, using the **Restive::resource** method.

The **routes** and the **controller** will allow access to various [api endpoints]({{< ref "20_api_controllers/30_api_endpoints/_index.md" >}} "API Endpoints"), which act like standard Laravel resource 
routes, with the addition of filtering/sorting query parameters.

The controller also provides [validation]({{< ref "20_api_controllers/40_validation/_index.md" >}} "Validation") 
on create/update methods and [pagination]({{< ref "20_api_controllers/50_pagination/_index.md" >}} "pagination") for the index method.

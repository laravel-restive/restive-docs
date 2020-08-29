---
title: "Controller Definition"
weight: 10
---

For each Laravel model you want to provide API access to you will need to create a Controller.

This should be placed in the standard Laravel location
e.g. **App/Http/Controllers** or a sub directory. Our suggestion is to use **App/Http/Controllers/Api**

The controller definition is fairly simple

    <?php
    namespace App\Http\Controllers\Api;

    use Restive\Controllers\ApiController;

    class DummySimpleController extends ApiController
    {
        protected $modelName = '\\Restive\\Models\\DummySimple';
    }

{{% notice info %}}
The **protected $modelName** defines the Eloquent Model that will be used by the controller. The factory class used will try and resolve the model
    from either your projects App folder or from the App/Models folder, If the Model is in one of these folders there is no need to namespace the model name. e.g. you could just do

        protected $modelName = 'ModelName';

{{% /notice %}}


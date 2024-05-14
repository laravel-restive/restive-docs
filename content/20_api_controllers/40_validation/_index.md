---
title: "Validation"
weight: 40
---

The base **ApiController** class that your controller extends contains calls
to Laravel's Validation system.

THe api controller uses a custom `FormRequest` class to allow validation errors to be returned as 
part of the json response. 

To create your own validator/form request class. 

For the controller you can set the request class that is used e.g. 

by setting 

    protected string $request = 'SomeRequest';

in the [controller]({{< ref "20_api_controllers/10_controller_definition/_index.md" >}}) definition 


The form request class needs to define 3 methods

## commonRules

        public function commonRules() : array

returns an array of Laravel rules that will be run on both model store & update methods.

## storeRules

    public function storeRules() : array

returns an array of Laravel rules that will be run on just the  model store method.

## updateRules

    public function updateRules() : array

returns an array of Laravel rules that will be run on just the  model update method.

## Examples

    public function commonRules() : array
    {
        return  [
            'age' => ['required'],
            'email' => ['required'],
        ];
    }

    public function updateRules() : array
    {
        return [
            'email' => ['unique:users,email,' . $this->id]
        ];
    }

{{% notice info %}}

Validation errors will be returned as part of the JSON response.

{{% /notice %}}

{{% notice info %}}

There is a [console command]({{< ref "45_console_commands/" >}}) to create a stub custom form request.

{{% /notice %}}

{{% notice warning %}}
The controller uses **$request->all()** to pass request fields
    to the model update/create methods. This could allow malicious users to update
    database fields that you did not want. You **must** therefore be very explicit
    in your models as to which fields can be used in this way. e.g. using the **$fillable** property.
{{% /notice %}}



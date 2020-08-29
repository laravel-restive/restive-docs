---
title: "Validation"
weight: 40
---

The base **ApiController** class that your controller extends contains calls
to Laravel's Validation system.

To use validation on your api request you must create a public **rules** method on
the model your controller accesses.

e.g.

    public function rules($id = 0)
    {
        return [
            'email' => 'required|unique:zcwilt_users'.($id ? ",email,$id" : ''),
            'name' => 'required'
        ];
    }

{{% notice info %}}
For update methods, the primary key value is passed as the **$id** parameter.
{{% /notice %}}


{{% notice warning %}}
The controller uses **$request->all()** to pass request fields
    to the model update/create methods. This could allow malicious users to update
    database fields that you did not want. You **must** therefore be very explicit
    in your models as to which fields can be used in this way. e.g. using the **$fillable** property.
{{% /notice %}}



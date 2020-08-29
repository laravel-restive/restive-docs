---
title: "Soft Deletes"
weight: 20
---

For models that support soft deletes, the query parser also provides 2 further filters.


## With Trashed

To show all entries for the model, even when soft deleted use

    withTrashed

## Only Trashed

To show only entries for the model that have been soft deleted use

    onlyTrashed

{{% notice info %}}
Using **withTrashed** or **onlyTrashed** on models that do not support **soft deletes** will result in an exception, with the error message being returned in the Json response.
``{"error":{"message":"Model does not support soft deletes","status_code":400}}``
{{% /notice %}}


{{% notice warning %}}
There is currently no way to force delete soft deleted items. This is on the todo list.
{{% /notice %}}

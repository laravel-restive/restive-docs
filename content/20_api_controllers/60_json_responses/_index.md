---
title: "JSON Responses & Error Handling"
weight: 60
---

The ApiController returns a JSON response for all endpoints.

Where possible it will catch grammar and validation errors and return those errors in the response.

It will also attempt to catch other exceptions and gracefully handle these.

As an example. 

If a models database definition has a unique column and calls to model create try to add an entry that adds a new 
model with a duplicate and there is no validation to catch duplicates, then this exception will return the exception message in the json 
response. It would be better here if there was validation logic to catch the duplicated unique column.

What ultimately is returned to the browser depends on a combination of settings.

If APP_DEBUG is set to true in your .env file then internal exceptions will be returned as error messages in the response with a 
corresponding status.





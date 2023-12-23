---
title: "JSON Responses"
weight: 60
---

The ApiController returns a JSON response for all endpoints.

Where possible it will catch grammar and validation errors and return those errors in the response.

There are some places it won't catch exceptions and those exceptions will cause calls to the API to throw uncaught exceptions.

As an example. 

If a models database definition has a unique column and calls to model create try to add an entry that adds a new 
model with a duplicate and there is no validation to catch duplicates, then an uncaught exception will be thrown.
You therefore must ensure that validation logic catches these errors.


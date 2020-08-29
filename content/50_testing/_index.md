---
title: "Testing"
weight: 50
---
Tests can be run within the package

``vendor/bin/phpunit``

or

``composer tests``

There is also a phpunit xml file for running tests with code coverage

``vendor/bin/phpunit -c phpunit-cc.xml``

or

``composer coverage``


{{% notice info %}}
To run the code coverage tests, you will need to install xdebug
{{% /notice %}}




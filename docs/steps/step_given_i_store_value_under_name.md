
Given I store "{value}" under "{name}"
=============================================================================================================

Usage example
-------------

```
Feature: zato-apitest docs

Scenario: Given I store "{value}" under "{name}"

    Given address "http://apitest-demo.zato.io"
    Given URL path "/demo/json"
    Given format "JSON"
    Given I store "Now, is that cool or is that cool?" under "msg"

    When the URL is invoked

    Then JSON Pointer "/action/msg" is "#msg"
```

Discussion
----------

Values stored under user-provided names can be referred to by prefixing them with a '#' sign.
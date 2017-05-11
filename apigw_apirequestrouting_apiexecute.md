# Assembly execution {#apigw_apirequestrouting_apiexecute .concept}

The API Gateway runs the API execute action to execute the assembly rule that is identified at the runtime for the incoming request.

The API execute action runs the assembly rule, and when an error occurs, runs the assembly error handler in the following process:

1.  The API execute action identifies the assembly rule that is defined for the target API.
2.  The API execute action runs the assembly rule.
3.  When an error occurs during the running of the assembly rule, or any actions in the assembly rule, the API execute action determines whether a catch setting is configured to handle this specific error.
    -   When a catch setting is found, the API execute action runs the error rule that is specified for the error.
    -   When a catch setting is not found but the default catch setting is configured, the API execute action runs the default error rule.
    -   When neither is found, the error is not handled. The API execute action saves the error information to be used by the API result action for response preparation.

**Parent topic:** [Request processing](apigw_apirequestrouting_apiprocessingrule.md)


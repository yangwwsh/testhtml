# Rate limiting {#apigw_apirequestrouting_apiratelimit .concept}

The API Gateway runs the API rate limit action to enforce the rate limit scheme that is defined for the target API or operation.

The API rate limit action enforces the rate limit scheme in the following process:

1.  The API rate limit action determines the rate limit scheme to enforce.
    -   If the subscriber is identified and the plan is matched during the API client identification phase, the API rate limit action checks whether the operation-level rate limit scheme is defined for the target operation:
        -   When defined, the action enforces the operation-level rate limit.
        -   When not defined, the action enforces the plan-level rate limit.
    -   If the subscriber is not identified during the client identification phase, the API rate limit action checks whether the default rate limit is configured.
        -   When configured, the action matches the default rate limit that is defined for the API collection.
        -   When not configured, the request is rejected.
2.  The action enforces rate limiting through the quota enforcement server.
    -   If the rate limit is not exceeded, the processing proceeds to the context population phase.
    -   If the rate limit is exceeded, the action examines whether the hard limit setting is enabled for the plan:
        -   When enabled, the request is rejected.
        -   When not enabled, the request is still processed with a warning.

**Parent topic:** [Request processing](apigw_apirequestrouting_apiprocessingrule.md)

**Related information**  


[Configuring the quota enforcement server](quotaenforcement_creatingquotaenforcementserver.html)


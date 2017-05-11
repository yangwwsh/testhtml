# Client identification {#apigw_apirequestrouting_apiclientidentification .concept}

The API Gateway runs the API client identification action to examine the API key credentials that are carried in the request and verify the subscription of the client.

1.  The API client identification action examines the API key credentials that are carried in the request against the API key security requirement of the target API.
    -   When the API does not have any security requirement or the API does not have any API key security requirement, the processing proceeds directly to the rate limiting phase.
    -   When the API has an API key security requirement, the request must meet the following conditions to pass the client identification check:

        -   The API key credentials must be placed in the location that is expected by the API key security requirement.
        -   When the API key security requirement requires the client ID, the request must carry the client ID in the expected location.
        -   When the API key security requirement requires the client ID and secret, the request must carry the client ID and secret in the expected location.
        The request is rejected when client identification fails.

2.  After the API key credentials pass the client identification check, the API client identification action checks whether an API subscriber exists in the API Gateway by matching the client ID and secret.
    -   If a subscriber is matched, the API client identification action retrieves the plans that the subscriber is subscribed to:
        -   If the target API is packaged in at least one of the subscribed plans, the action saves the matched plan to be used in the rate limiting phase.
        -   If the target API is not packaged in any of the subscribed plans, the request is rejected.
    -   If no subscriber is matched, the request is rejected.

**Parent topic:** [Request processing](apigw_apirequestrouting_apiprocessingrule.md)


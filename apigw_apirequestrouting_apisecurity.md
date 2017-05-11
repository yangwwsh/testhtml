# Security check {#apigw_apirequestrouting_apisecurity .concept}

The API Gateway runs the API security action to perform the security checks that are required by the matched API on the request.

The API Gateway performs API key security check in the client identification phase. In the security check phase, the API Gateway checks the request against the basic authentication and OAuth security requirements in the following procedure:

1.  The action determines the security requirements to enforce:
    -   If the target operation has its security requirements defined in the operation level, the action enforces the operation-level security requirements.
    -   If the target operation does not have operation-level security requirements, the action enforces the API-level security requirements.
    -   If the target operation does not have any security requirement in the API or operation level, the action allows the access to the API without security check. The processing proceeds to the context population phase.
2.  The action examines the credentials that are carried in the request against the security requirements to enforce:
    -   If the credentials fulfill at least one of the security requirements, the action allows the access to the API.
    -   If the credentials do not fulfill any of the security requirements, the request is rejected.

For information about how the supported types of security definition work to security an API, see the API security topic.

**Parent topic:** [Request processing](apigw_apirequestrouting_apiprocessingrule.md)

**Related information**  


[API security](apigw_securitydefinitions.md)


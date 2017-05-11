# Request processing {#apigw_apirequestrouting_preflow .concept}

After an API collection is matched, the API Gateway triggers the API processing rule of the collection to match the target API, enforce the constraints to execute the target API operation, prepare the context for the running of the operation, and execute the assembly rule of the API to respond to the request.

The API Gateway processes a request by interacting with the API context. For each transaction, a context is prepared before processing starts and is continuously updated during the transaction.

As shown in [Figure 1](#api_processing), the API Gateway uses an API processing rule, which comprises the following processing actions, to process the request. The API Gateway achieves each step of the process through running the corresponding processing action. You can click relevant component in the diagram for detailed instructions.

1.  The API Gateway runs the API routing action to match the target API to call. When no API is matched, the request is rejected.
2.  The API Gateway runs the API client identification action to examine the API key credentials that are carried in the API request and match the API plan through which the target API is made available to the client.
3.  The API Gateway runs the API rate limit action to enforce the rate limit scheme that is configured for the matching API plan. When the rate limit is reached, the request is rejected.
4.  The API Gateway runs the API security action to perform the security checks that are required by the target API and operation. When the security requirement is not fulfilled, the request is rejected.
5.  The API Gateway runs the API context action to populate the context variables for the assembly to access or manipulate.
6.  The API Gateway runs the API execute action to execute the assembly of the target API.
7.  The API Gateway runs the API result action to prepare the final response to the client based on the result from the API execute action.

When error occurs during the API request processing, the API Gateway runs the API error rule to handle the errors. A default API error rule comprises only the API result action.

 

![](apiflow.gif)

-   **[API routing](apigw_apirequestrouting_apirouting.md)**  
The API Gateway runs the API routing action to match the API to invoke.
-   **[Client identification](apigw_apirequestrouting_apiclientidentification.md)**  
The API Gateway runs the API client identification action to examine the API key credentials that are carried in the request and verify the subscription of the client.
-   **[Rate limiting](apigw_apirequestrouting_apiratelimit.md)**  
The API Gateway runs the API rate limit action to enforce the rate limit scheme that is defined for the target API or operation.
-   **[Security check](apigw_apirequestrouting_apisecurity.md)**  
The API Gateway runs the API security action to perform the security checks that are required by the matched API on the request.
-   **[Context population](apigw_apirequestrouting_apicontext.md)**  
The API Gateway runs the API context action to populate the context variables that the assembly actions act on or manipulate at run time.
-   **[Assembly execution](apigw_apirequestrouting_apiexecute.md)**  
The API Gateway runs the API execute action to execute the assembly rule that is identified at the runtime for the incoming request.
-   **[Response preparation](apigw_apirequestrouting_apiresult.md)**  
The API Gateway runs the API result action to prepare responses to the client based on the result from the API execute action.

**Parent topic:** [Routing of API requests](apigw_apirequestrouting.md)


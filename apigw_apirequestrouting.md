# Routing of API requests {#apigw_apirequestrouting .concept}

When API Gateway receives an API request through the handlers, the API Gateway first routes the request to a matching API collection. When the collection is matched, the API Gateway triggers the API processing rule of the API collection to execute the required API operation and respond to the API request. The API processing rule comprises a set of API actions in a defined sequence.

-   **[Collection routing](apigw_apirequestrouting_collection.md)**  
The API Gateway determines the API collection to route the request to by matching the request URL against the routing prefix of each API collection. The collection routing follows certain rules, you must take the rules into consideration when you design routing prefixes for your API collections.
-   **[Request processing](apigw_apirequestrouting_apiprocessingrule.md)**  
After an API collection is matched, the API Gateway triggers the API processing rule of the collection to match the target API, enforce the constraints to execute the target API operation, prepare the context for the running of the operation, and execute the assembly rule of the API to respond to the request.

**Parent topic:** [API Gateway](apigw_overview.md)


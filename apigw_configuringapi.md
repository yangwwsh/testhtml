# Developing APIs {#apigw_configuringapi .task}

The DataPower® Gateway stores each API as an API definition configuration. To develop an API, create an API definition.

You can create the following types of API definitions on the DataPower Gateway:

-   The REST API that is compliant with version 2.0 of the Swagger specification.
-   The OAuth 2.0 provider API that contains the authorization and token endpoints of an OAuth flow.

You need to define the following settings that are generic to both types of API.

-   The base path on which the API is served. All resources in a REST API are defined relative to its base path.
-   Optionally, the MIME types that the API can consume and produce. The MIME type definitions should be in compliance with RFC 6838. For example,application/json.
-   A list of paths to the API operations.
-   Optionally, the alternative security requirements to enforce for the API as a whole \(that is, there is a logical OR between the security requirements\). The security requirement that you apply to your API is the top-level security declaration. By default, the security requirement is applied to all operations in the API. However, for each API operation, you can override the top-level security by separately specifying security schemes to enforce on the operation level.
-   Optionally, the custom API properties.
-   Optionally, the streaming and flow control mode. Flow control cannot be enabled unless streaming is enabled.

    When the API Gateway sends or receives large static data, such as images, the memory footprint on DataPower Gateway can be large. You can reduce the memory footprint by enabling streaming and flow control.

    -   When streaming is enabled, the API Gateway passes message payloads through without parsing and the DataPower Gateway does not buffer the entire payload of a message into the memory.
    -   When flow control is enabled, the DataPower Gateway limits the number of message payloads that are received from the server or client, thereby, avoid too many data being buffered on DataPower Gateway.
    Data streaming is available when an assembly rule of the API definition meets one of the following requirements:

    -   The assembly rule includes only one assembly invoke action.
    -   The assembly rule includes only the assembly actions that never access the `message.body` context variable. The following assembly actions meet this requirement:
        -   Assembly switch action
        -   Assembly set variable action

For a REST API, you can optionally define the following settings.

-   The assembly that controls a specific aspect of processing during API invocation at run time.

For an OAuth API, you must also provide a list of OAuth specific settings.

The following procedure instructs how to create an API definition.

1.   In the search field, enter API. 
2.   From the search results, select **API Definition**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the base path, which is relative to the host, where the API is served. 
6.   Specify the MIME types that the API can consume. 
7.   Specify the MIME types that the API can produce. 
8.   Specify the API paths where the operations are available. 
9.   Specify the security requirements. 
10.  Specify the custom API properties. 
11.  Specify whether to enable streaming. 
12.  When data streaming is enabled, specify whether to enable flow control. 
13.  Select the type of API to create. 
    -   When you create a REST API, complete the following configuration.
        1.  Specify the assembly.
    -   When you create an OAuth API, complete the following configuration.
        1.  Specify whether the client type is public or confidential.
        2.  Specify the OAuth scope.
        3.  Select the method to obtain the access token for authorization.
        4.  Specify the basic authentication security definition to use to access the API.
        5.  Select the method to collect client credentials during the authorization process.
        6.  Select the method to grant authorization.
        7.  Enter the time that an access token remains valid.
        8.  Set whether to enable the use of refresh tokens. When enabled, complete the following settings.
            1.  Specify how many times the refresh token can be requested.
            2.  Specify the lifetime of the refresh token.
        9.  Set whether to enable the endpoint for token revocation.
        10. Set whether to enable the endpoint for token retrieval.
14.  Click **Apply** to save the changes to the running configuration. 
15.  Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

-   **[Creating an API path](apigw_configuringapipath.md)**  
An API path defines the API operations that are available on a single path.
-   **[Creating an API operation](apigw_configuringapioperation.md)**  
An API operation defines the HTTP method to execute against the resources. You can use GET, POST, PUT, DELETE, HEAD, PATCH, and OPTIONS operations for the API.
-   **[API security](apigw_securitydefinitions.md)**  
API Gateway allows you to secure your APIs through API key, basic authentication, and OAuth security schemes.
-   **[API properties](apigw_properties.md)**  
An API property is a type of context variable whose value is dependent on the API collection that the API is provisioned in. Collection-specific API properties allow you to use the same API definition in different API collections when a property in a collection requires a unique or different value.
-   **[Creating an assembly](apigw_configuringassembly.md)**  
An assembly defines the data processing capabilities of an API definition. When an API is matched for an API request, the API execute action in the API processing rule runs the assembly of the API to respond to the request. The information instructs how to create an assembly.

**Parent topic:** [API Gateway](apigw_overview.md)

**Related information**  


[RFC 6838: https://tools.ietf.org/html/rfc6838](http://tools.ietf.org/html/rfc6838)


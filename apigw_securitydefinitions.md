# API security {#apigw_securitydefinitions .concept}

API Gateway allows you to secure your APIs through API key, basic authentication, and OAuth security schemes.

You can declare the available security schemes to be used in your APIs by defining security definitions. A security definition provides details for each scheme. The API Gateway supports the following types of security definition:

 API key
 :   An API key security definition defines the credentials that an API requester must provide to the API Gateway to identify itself when the requester calls the API operations.

  Basic authentication
 :   A basic authentication security definition defines an authentication URL or an LDAP user registry to authenticate accesses to APIs. When you use basic authentication, the API client must provide a valid user name and password in the request.

  OAuth
 :   An OAuth security definition defines settings that control the access to APIs through the OAuth standard. By using an OAuth token, users can grant the API requester to access their information that is stored with another service provider without sharing their personal credentials.

 A security definition is not enforced unless you add the security definition as a security requirement at the API-level or the operation-level.

-   API-level security requirements are enforced on the API as a whole. By default, the security requirements are applied to all operations in the API.
-   Operation-level security requirements override the API-level security requirements.

An API or operation can have one or more security requirements. When multiple security requirements are configured, the API request needs to pass only the security checks that are defined by one of these system requirements. A security requirement comprises one or more security definitions. When multiple security definitions are specified, the API request must pass all security checks that are defined by the security definitions.

The following high-level procedure shows how to secure your APIs and operations:

1.  Define security definitions that are available to be used in your APIs.
2.  For each API to secure, configure the security requirements at the API-level.
3.  For operations that have operation-specific security requirements instead of inheriting the API-level security requirements, configure the security requirements at the operation-level.

-   **[Creating a security requirement](apigw_configuringsecurityrequirements.md)**  
An API security requirement defines the required security checks that an API request must pass to call the API or operation.
-   **[Creating an API key security definition](apigw_securitydefinitions_apikey.md)**  
Create an API key security definition to define the credentials that an API client must provide to the DataPower® Gateway to access an API.
-   **[Creating a basic authentication security definition](apigw_securitydefinitions_basicauth.md)**  
Create a basic authentication security definition to specify the authentication URL or LDAP user registry to authenticate accesses to APIs.
-   **[Creating an OAuth security definition](apigw_securitydefinitions_oauth.md)**  
Create an OAuth security definition to control accesses to an API through the OAuth authorization standard.
-   **[Creating an API LDAP registry](apigw_configuringldapregistry.md)**  
Create an API LDAP registry to define the LDAP server to authenticate incoming API requests.

**Parent topic:** [Developing APIs](apigw_configuringapi.md)


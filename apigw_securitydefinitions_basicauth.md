# Creating a basic authentication security definition {#apigw_securitydefinitions_basicauth .task}

Create a basic authentication security definition to specify the authentication URL or LDAP user registry to authenticate accesses to APIs.

You can authenticate users with an authentication URL or an LDAP registry.

-   When you use an authentication URL, the API Gateway sends the credentials that it collects from the API client to the endpoint that is specified in the URL for validation. When the user is authenticated, the authentication URL returns an HTTP `200 OK` response status code. All other HTTP response status codes result in an authentication failure and the access is denied.
-   When you use an LDAP registry, the API Gateway uses an LDAP server to authenticate the API client.

1.   In the search field, enter API. 
2.   From the search results, select **API Security Basic Authentication**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Select how to authenticate users. 
6.   When you authenticate users with an authentication URL, complete the following steps. 
    1.   Enter the URL to validate client credentials. 
    2.   Select the SSL client profile to secure connections between the DataPower® Gateway and the authentication server. 
7.   When you authenticate users with an LDAP registry, select the name of the API LDAP Registry configuration to authenticate the API request. 
8.   Click **Apply** to save the changes to the running configuration. 
9.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

To enforce the security scheme, add the basic authentication security definition into a security requirement of an API or operation.

**Parent topic:** [API security](apigw_securitydefinitions.md)

**Related information**  


[Creating an API LDAP registry](apigw_configuringldapregistry.md)

[Creating a security requirement](apigw_configuringsecurityrequirements.md)


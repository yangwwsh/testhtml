# Creating an API key security definition {#apigw_securitydefinitions_apikey .task}

Create an API key security definition to define the credentials that an API client must provide to the DataPower® Gateway to access an API.

The client ID type of security definition requires that an client must show the expected client ID to access the API.

The client secret type of security definition requires that an client must show the expected client secret to access the API.

You can require the API client to provide only the client ID, or both the client ID and client secret. When you require the API client to provide both the client ID and client secret, you must create two separate API key security definitions, one of type ID and the other of type Secret.

You can require the credentials to be sent in the request header or as query parameters. An API call fails if the required credentials are not included in the expected location.

**Note:** Regardless of whether the client credentials are sent in the request header or as query parameters, you must specify the same location for the client ID and client secret.

1.   In the search field, enter API. 
2.   From the search results, select **API Security API Key**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Select the location of the client credential. 
6.   Select the type of the client credential. 
7.   Enter the name of the API key. 
8.   Click **Apply** to save the changes to the running configuration. 
9.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

To enforce the security scheme, add the API key security definition into a security requirement of an API or operation.

**Parent topic:** [API security](apigw_securitydefinitions.md)

**Related information**  


[Creating a security requirement](apigw_configuringsecurityrequirements.md)


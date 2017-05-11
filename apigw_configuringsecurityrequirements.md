# Creating a security requirement {#apigw_configuringsecurityrequirements .task}

An API security requirement defines the required security checks that an API request must pass to call the API or operation.

You specify a security requirement by selecting one or more security definitions. When multiple security definitions are selected, the API request must pass all security checks that these security definitions specify.

The following rules apply when you specify a security requirement:

-   If you want to authenticate the API requester through API keys and require the requester to show both client ID and client secret, you must apply two API key security definitions, one authenticates the client ID and the other authenticates the client secret.
-   You cannot apply more than one basic authentication security definitions to an API.
-   You cannot apply more than one OAuth security definitions to an API.

1.   In the search field, enter API. 
2.   From the search results, select **API Security Requirement**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Select the security definition to enforce. 
6.   Click **Apply** to save the changes to the running configuration. 
7.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

Apply the security requirement:

-   To apply the requirement to all operations of an API, associate the security requirement to the API definition configuration.
-   To apply the requirement to an API operation, associate the security requirement to the API operation configuration.

**Parent topic:** [API security](apigw_securitydefinitions.md)

**Related information**  


[Developing APIs](apigw_configuringapi.md)

[Creating an API operation](apigw_configuringapioperation.md)


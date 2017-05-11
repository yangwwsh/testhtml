# Creating an OAuth security definition {#apigw_securitydefinitions_oauth .task}

Create an OAuth security definition to control accesses to an API through the OAuth authorization standard.

You can create an OAuth security definition that uses one of the following flows according to the OAuth grant type that you want to enforce. The following table shows the different types of OAuth flow and the corresponding OAuth grant types:

|OAuth flow|OAuth grant type|
|----------|----------------|
|Access code|Authorization Code|
|Application|Client Credentials|
|Implicit|Implicit OAuth|
|Password|Resource Owner Password Credentials|

1.   In the search field, enter API. 
2.   From the search results, select **API Security OAuth**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Select the OAuth flow to use. 
6.   Specify the scopes that you want to cover access to your API. 
7.   Click **Apply** to save the changes to the running configuration. 
8.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

To enforce the security scheme, add the OAuth security definition into a security requirement of an API or operation.

**Parent topic:** [API security](apigw_securitydefinitions.md)

**Related information**  


[Creating a security requirement](apigw_configuringsecurityrequirements.md)


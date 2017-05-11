# Creating an API operation {#apigw_configuringapioperation .task}

An API operation defines the HTTP method to execute against the resources. You can use GET, POST, PUT, DELETE, HEAD, PATCH, and OPTIONS operations for the API.

The following settings in the API operation override the corresponding setting in the configurations that reference the API operation.

-   The parameters that you specify here override the same parameters in the API path.
-   The security requirements that you specify here override the API-level security requirements.
-   You can set whether to remove the API-level consume declaration that is defined for the API. By default, the top-level consume declaration is applied to the operation. When removed, the operation can always be performed regardless of the content type.
-   You can set whether to remove the API-level security declaration that is defined for the API. By default, the top-level security declaration is applied to the operation. When removed, an API client can call the API operation without passing any security check.

1.   In the search field, enter API. 
2.   From the search results, select **API Operation**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the HTTP method to perform against the API. 
6.   Specify the ID of the operation. 
7.   Specify the parameters that are applicable for the operation. 
    1.   Click **Add** or **New**. 
    2.   Enter the parameter name. Parameter names are case-sensitive.
    3.   Set whether the parameter is required for a call to be valid. 
    4.   Select the type of the parameter. 
    5.   Select the location of the parameter. 
    6.   Depending on the location of the parameter, specify the schema or the extending format: 
        -   If the parameter is located in `body`, specify the schema that defines the type that is used for the body parameter.
        -   If the parameter is not located in `body`, specify the extending format for the parameter type that you specified in [7.d](#d24e102).
    7.   Click **Apply**. 
8.   Repeat the previous step to add another parameter. 
9.   Set whether to remove the API-level consume declaration for the operation. 
10.  When the top-level consume declaration is not removed, specify the MIME types that the API operation can consume. 
11.  Set whether to remove the API-level security declaration for the operation. 
12.  When the top-level security declaration is not removed, specify the security requirements to enforce for the operation. 
13.  Click **Apply** to save the changes to the running configuration. 
14.  Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Developing APIs](apigw_configuringapi.md)

**Related information**  


[API security](apigw_securitydefinitions.md)


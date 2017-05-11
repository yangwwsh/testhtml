# Creating an API path {#apigw_configuringapipath .task}

An API path defines the API operations that are available on a single path.

Provide the following information when you configure an API path:

-   The path, which is relative to the base path, where the operations are available.
-   The operations that are available on the path.
-   Optionally, the parameters that apply to all operations under this path. The parameters in the API path can be overridden by the parameters that are specified at the operation level.

1.   In the search field, enter API. 
2.   From the search results, select **API Path**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the path where the operations are served. 
6.   Specify the operations that are served in the path. 
7.   Define a parameter that is applicable for all operations under this path. 
    1.   Click **Add** or **New**. 
    2.   Enter the parameter name. Parameter names are case-sensitive.
    3.   Set whether the parameter is required for a call to be valid. 
    4.   Select the type of the parameter. 
    5.   Select the location of the parameter. 
    6.   Depending on the location of the parameter, specify the schema or the extending format: 
        -   If the parameter is located in `body`, specify the schema that defines the type that is used for the body parameter.
        -   If the parameter is not located in `body`, specify the extending format for the parameter type that you specified in [7.d](#paratype).
    7.   Click **Apply**. 
8.   Repeat the previous step to define another parameter. 
9.   Click **Apply** to save the changes to the running configuration. 
10.  Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Developing APIs](apigw_configuringapi.md)

**Related information**  


[Creating an API operation](apigw_configuringapioperation.md)


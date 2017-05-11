# Creating an assembly {#apigw_configuringassembly .task}

An assembly defines the data processing capabilities of an API definition. When an API is matched for an API request, the API execute action in the API processing rule runs the assembly of the API to respond to the request. The information instructs how to create an assembly.

To configure an assembly, you must define the assembly rule and optionally how to handle errors that occur during the assembly execution.

An assembly rule can comprise one or more assembly actions to apply to the API call. The assembly actions are run in order and act on different context variables of the API call. You can access and manipulate the variables in the API context by referencing the context variable in the assembly action configuration.

You can define catch settings to handle specific errors such as the assembly invoke action fails to connect the server or receives a non-200 message, or the assembly switch action fails to evaluate the given expression. Unhandled errors are saved for preparing the final response, for more information, see the response preparation topic.

1.   In the search field, enter API. 
2.   From the search results, select **Assembly**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the assembly rule that consists of one or more assembly actions to apply to the API call. 
6.   Specify a catch setting that defines how to handle a specific error in the assembly. 
    1.   Click **Add** or **New**. 
    2.   Enter the name of the error. 
    3.   Specify an error handler. 
    4.   Click **Apply**. 
    5.   Repeat the previous steps to add another error case. 
7.   Specify a default error rule to run when an uncaught error occurs. 
8.   Click **Apply** to save the changes to the running configuration. 
9.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

-   **[Adding a GatewayScript action](apigw_addinggatewayscriptaction.md)**  
Add a GatewayScript action to the assembly. The GatewayScript action uses a specified GatewayScript file in a directory on the DataPower® Gateway.
-   **[Adding an If action](apigw_addingifaction.md)**  
How to add an assembly If action.
-   **[Adding an invoke action to retrieve documents](apigw_addinginvokeaction.md)**  
An invoke action retrieves a document from a specified target URL from within the assembly. The invoke action sends a request that can include a payload to the target and stores the response in the specified variable in the API context.
-   **[Adding a parse action to the assembly](apigw_addingparseaction.md)**  
An assembly parse action controls the parsing of an input document which can be an XML or JSON document, or binary data from the API context. When a parse action is configured for an assembly rule, the parse settings that are associated with the parse action override the corresponding parser limits for input documents that are set by the XML manager.
-   **[Adding a set variable action](apigw_addingsetvariableaction.md)**  
You can add an assembly set variable action to set, add, or clear the variables in the API context.
-   **[Adding a switch action to choose which rule to use](apigw_addingswitchaction.md)**  
An assembly switch action evaluates the input context against a list of conditions and runs the corresponding API rule of the first condition that matches. Provide conditions with JavaScript expression and use an "otherwise" clause to run a designated rule when no condition matches.
-   **[Adding a throw action for a custom error message](apigw_addingthrowaction.md)**  
A throw action throws a custom error. This action ends the current assembly rule.
-   **[Adding a convert XML to JSON action](apigw_addingxmltojsonaction.md)**  
An XML to JSON action converts the payload of an API context from the extensible markup language \(XML\) format to JavaScript Object Notation \(JSON\) object.
-   **[Adding a validate JWT action](apigw_addingvalidatejwtaction.md)**  
A validate JWT action defines the cryptographic material and methods to validate a JSON Web Token \(JWT\) in an API call to secure access to your APIs.
-   **[Adding an XSLT action to run a stylesheet for the current payload](apigw_addingxsltaction.md)**  
You can use an assembly XSLT action to run a stylesheet for the current payload from the API context.
-   **[Accessing and manipulating an API context variable](apigw_referencingapicontextvariable.md)**  
You can access and manipulate a referenced API context variable through assembly actions. The information instructs how to reference a variable in the API context through the assembly actions.

**Parent topic:** [Developing APIs](apigw_configuringapi.md)

**Related information**  


[Assembly execution](apigw_apirequestrouting_apiexecute.md)

[Response preparation](apigw_apirequestrouting_apiresult.md)


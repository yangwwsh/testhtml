# Accessing and manipulating an API context variable {#apigw_referencingapicontextvariable .task}

You can access and manipulate a referenced API context variable through assembly actions. The information instructs how to reference a variable in the API context through the assembly actions.

Check the list of supported variables in the API context.

You can get or set the value for a referenced variable.

-   Get the value for a variable through one of the following methods:
    -   Through the assembly GatewayScript action, run a GatewayScript file that uses the `apim.getVariable()` API.
    -   Through the assembly GatewayScript action, run a GatewayScript file that uses the `context` object.
    -   Through the assembly XSLT action, run a stylesheet that uses the `apim:get-variable()` extension function.
    -   In a supported field of certain assembly actions, reference a variable inline.
-   Set the value for a variable through one of the following methods:
    -   Through the assembly set variable action.
    -   Through the assembly GatewayScript action, run a GatewayScript file that uses the `apim.setVariable()` API.
    -   Through the assembly GatewayScript action, run a GatewayScript file that uses the `context` object.
    -   Through the assembly XSLT action, run a stylesheet that uses the `apim:set-variable` extension element.

-    Through the assembly GatewayScript action 

    1.   Open the GatewayScript file for edit. 
    2.   Use the APIs in the `apim` module to get or set a variable. 
    3.   Associate the GatewayScript file to an assembly GatewayScript action. 
    For the syntax, see the information about the GatewayScript objects and modules for the API Gateway.

-    Through the assembly XSLT action 

    1.   Open the stylesheet for edit. 
    2.   Use the relevant API Gateway extension function and element to get or set a variable. 
    3.   Associate the stylesheet to an assembly XSLT action. 
    For the syntax, see the reference information about the `apim` extension functions and elements.

-    Inline reference 
    1.   In the assembly action configuration, locate the property that you want to use a context variable as the value. 
    2.   Enter `$(variable)`. 

        When the variable to reference is an API property, use one of the following methods:

        -   ```
$(api.properties.property\_name)
```

        -   ```
$(property\_name)
```

        Where, property\_name is the name of the property to reference.

        `$(api.properties.property\_name)` is the absolute expression to reference a property. The short form `$(property\_name)` applies only when the assembly action does not have a property with the same name. You can use inline reference of a custom API property for the following assembly action settings:

        -   The URL property of the assembly invoke action
        -   The variable name and variable assignment properties of the assembly set variable action
        -   The case property of the assembly switch action
        -   The error identifier and error text properties of the assembly throw action

**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

**Related information**  


[Adding a set variable action](apigw_addingsetvariableaction.md)

[Adding a GatewayScript action](apigw_addinggatewayscriptaction.md)

[Adding an XSLT action to run a stylesheet for the current payload](apigw_addingxsltaction.md)

[apim extension elements and functions](apigw_extensions.md)

[GatewayScript APIs for API management](apigateway_gatewayscript_general.md)


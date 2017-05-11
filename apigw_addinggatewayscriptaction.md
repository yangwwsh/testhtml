# Adding a GatewayScript action {#apigw_addinggatewayscriptaction .task}

Add a GatewayScript action to the assembly. The GatewayScript action uses a specified GatewayScript file in a directory on the DataPower® Gateway.

When the GatewayScript files calls the following APIs, you can add a parse action to the assembly.

-   `apim.readInput()`
-   `apim.readInputAsJSON()`
-   `apim.readInputAsBuffer()`
-   `apim.readInputAsXML()`

You can specify the location of the GatewayScript file with a URL or by referencing the `request.headers.X-SOURCE-URL` API context variable.

-   The URL must start with the local:, store:, or temporary: directory. For example, the location of the `test.js` script file is `local:///test.js`.
-   In the `request.headers.X-SOURCE-URL` API context variable, the X-SOURCE-URL indicates the URL that specifies the directory of the script file. Reference this variable with the `$(request.headers.X-SOURCE-URL)` format.

The GatewayScript file can use only the following GatewayScript object and modules:

-   `apim` module
-   `context` object
-   `fs` module
-   `multistep` module
-   `service-metadata` module

See the reference information about the GatewayScript objects and modules for the usage.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly GatewayScript**. 
3.   Specify the location of the script file. 
4.   Click **Add** or **New**. 
5.   Define the basic properties: Name, administrative state, and descriptive summary. 
6.   Specify the name and location of the GatewayScript file. 

**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

**Related information**  


[Adding a parse action to the assembly](apigw_addingparseaction.md)

[File management](filemanagement_directories.html)

[GatewayScript APIs for API management](apigateway_gatewayscript_general.md)


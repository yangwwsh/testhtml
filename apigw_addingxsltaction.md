# Adding an XSLT action to run a stylesheet for the current payload {#apigw_addingxsltaction .task}

You can use an assembly XSLT action to run a stylesheet for the current payload from the API context.

With the assembly XSLT action, you can perform the following actions within the assembly rule.

-   Read and update the current payload. To read the current payload, you must refer to the "/" document in your stylesheet. For example,

    ```
    <xsl:template match="/">
    </xsl:template>
    ```

    The current payload must be XML and parsed by a parse action in advance. Otherwise, the "/" document is initialized as empty. The generated output is used to update the current payload.

-   Get the original payload with the `apim:get-original-payload()` extension function.
-   Get the API context variable with the `apim:get-variable()` extension function.
-   Create or update the API context variable with the `apim:set-variable` extension element.
-   Get the API property with the `apim:get-api-property()` extension function.
-   Designate an error for and abort the execution of the current assembly rule with the `apim:reject` extension element.
-   Use other supported DP extension elements and functions to apply to the payload.

See the reference information about the `apim` extension elements and functions for the usage.

1.   In the search field, enter assembly. 
2.   From the search results, select **Assembly XSLT Action**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Select whether to use the current payload as the XSLT input. By default, the property is not enabled.
6.   Select the stylesheet to run. 
7.   Click **Apply** to save the changes to the running configuration. 
8.   Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

## Examples { .example}

-   Read the `/order/@date` from the current payload and save it into the `my.orderData` API context variable.

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <xsl:stylesheet version="1.0"
        xmlns:xsl="http://www.w3.org/1999/XSL/Transform"
        xmlns:apim="http://www.ibm.com/apimanagement"
        extension-element-prefixes="apim" exclude-result-prefixes="apim">
    
      <xsl:template match="/">
        <xsl:message>Found the order: <xsl:copy-of select="./order"/>
        <apim:set-variable name="'my.orderDate'" value="./order/@date"/>
      </xsl:template>
    </xsl:stylesheet>
    ```

-   Update the current payload with the generated XML document.

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <xsl:stylesheet version="1.0"
        xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
    
      <xsl:template match="/">
        <order>
          <item qty="2">Ink Cartridges</item>
          <item qty="300">Copy Paper</item>
        </order>
      </xsl:template>
    </xsl:stylesheet>
    ```


**Parent topic:** [Creating an assembly](apigw_configuringassembly.md)

**Related information**  


[apim extension elements and functions](apigw_extensions.md)

[Extension elements and functions](functions.html)


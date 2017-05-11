# `apim:reject` {#reject_apigatewayelement .reference}

Designates an error to and aborts the execution of current assembly rule.

## Namespace declaration { .section}

  2.  `xmlns:apim="http://www.ibm.com/apimanagement"`
 4.  `extension-element-prefixes="apim"`
  

## Syntax { .refsyn}

```
<apim:reject
  identifier="errorName"
  status-code="code"
  reason="reasonPhrase">
  text
</apim:reject>
```

## Attributes { .section}

 `identifier="errorName"`
 :   The optional `xs:string` that specifies the error name. The default value is `TransformError`.

  `status-code="code"`
 :   The optional `xs:integer` that specifies the HTTP status code. Enter a value in the range 400 - 999. The default value is 500.

  `reason="reasonPhrase"`
 :   The optional `xs:string` that specifies the HTTP reason phrase.

  text
 :   The `xs:string` that specifies the custom error message for the returned fault.

 ## Guidelines { .section}

The `apim:reject` extension element aborts the current assembly rule. The assembly actions that follow the assembly XSLT action are not executed. The API Gateway returns a fault message as the API response to the client.

## Examples { .example}

-   Call the `apim:reject` element to abort the current assembly rule with the status code 401.

    ```
    <xsl:template match="/">
        <apim:reject identifier="CustomError" status-code="401" 
            reason="Unauthorized">the error message...</apim:reject>
    </xsl:template>
    ```

-   The API Gateway returns the following fault message as the API response to the client in the preceding example.

    ```
    HTTP/1.0 401 Unauthorized
    Content-Type: application/json
    Connection: close
    
    {
      "name":"CustomError",
      "message":"the error message..."
    }
    ```


**Parent topic:** [Extension elements](apigw_extension_elements.md)


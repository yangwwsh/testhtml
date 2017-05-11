# `apim:get-variable()` {#get-variable_apigatewayfunction .reference}

Retrieves the value of the specified API context variable.

## Namespace declaration { .section}

  2.  `xmlns:apim="http://www.ibm.com/apimanagement"`
  

## Syntax { .refsyn}

apim:get-variable\(varname\)

## Parameters { .section}

 varname
 :   The `xs:string` that specifies the name of the API context variable.

 ## Guidelines { .section}

The `apim:get-variable` extension function returns the value of an API context variable.

When you want to retrieve the value of the specified API property, you can use `apim:get-variable('api.properties.propertyname')` or use `apim:get-api-property(propname)` directly. For example, the following syntax returns the same value.

-   `apim:get-variable('api.properties.foo')`
-   `apim:get-api-property('foo')`

## Results { .section}

The value of the specified API context variable.

## Example { .example}

```
<xsl:template match="/">
    <xsl:variable name="clientID" select="apim:get-variable('client.app.id')"/>
    ...
</xsl:template>
```

**Parent topic:** [Extension functions](apigw_extension_functions.md)

**Related information**  


[apim:get-api-property\(\)](get-api-property_apigatewayfunction.md)


# `apim:get-api-property()` {#get-api-property_apigatewayfunction .reference}

Retrieves the value of the specified API property.

## Namespace declaration { .section}

`xmlns:apim="http://www.ibm.com/apimanagement"`

## Syntax { .refsyn}

apim:get-api-property\(propname\)

## Parameters { .section}

 propname
 :   The `xs:string` that specifies the name of an API property.

 ## Guidelines { .section}

The `apim:get-api-property` extension function retrieves the value of the specified API property.

You can also use `apim:get-variable('api.properties.propertyname')` to retrieve the value of the specified API property.

## Results { .section}

The `xs:string` that contains the value of the API property.

## Example { .example}

```
<xsl:template match="/">
    <xsl:variable name="targetURL" select="apim:get-api-property('target-url')"/>
    ...
</xsl:template>
```

**Parent topic:** [Extension functions](apigw_extension_functions.md)

**Related information**  


[apim:get-variable\(\)](get-variable_apigatewayfunction.md)


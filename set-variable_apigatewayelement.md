# `apim:set-variable` {#set-variable_apigatewayelement .reference}

Assigns a value to an API context variable.

## Namespace declaration { .section}

  2.  `xmlns:apim="http://www.ibm.com/apimanagement"`
 4.  `extension-element-prefixes="apim"`
  

## Syntax { .refsyn}

```
<apim:set-variable
  name="name"
  value="value"/>
```

## Attributes { .section}

 `name="name"`
 :   The `xs:string` that specifies the name of the API context variable.

  `value="value"`
 :   Specifies the value of the API context variable.

 ## Guidelines { .section}

The `apim:set-variable` extension element assigns a value to an API context variable.

## Example { .example}

```
<xsl:template match="/">
    <apim:set-variable name="'my.orderDate'" value="./order/@date"/>
</xsl:template>
```

**Parent topic:** [Extension elements](apigw_extension_elements.md)


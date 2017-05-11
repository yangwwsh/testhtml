# `apim:get-original-payload()` {#get-original-payload_apigatewayfunction .reference}

Gets the original API payload for the assembly XSLT action.

## Namespace declaration { .section}

`xmlns:apim="http://www.ibm.com/apimanagement"`

## Syntax { .refsyn}

apim:get-original-payload\(\)

## Guidelines { .section}

The `apim:get-original-payload` extension function gets the original API payload for the assembly XSLT action. The original payload must be XML and parsed by a parse action first. Otherwise, this function returns empty.

## Results { .section}

An XML document that contains the original payload. Returns empty when the original payload is not XML or not parsed by a parse action.

## Example { .example}

Transform the original payload to update the current payload.

```
<xsl:template match="/">
    <xsl:variable name="originalPayload" select="apim:get-original-payload()"/>
    <Summary>
      <xsl:apply-templates select="$originalPayload//order"/>
    </Summary>
</xsl:template>
```

**Parent topic:** [Extension functions](apigw_extension_functions.md)


# Variables in the API context {#apigw_contextvariables .reference}

An API context is a set of variables. The input and output of the processing and assembly actions are stored in these variables. You can access and manipulate these variables by referencing them through assembly actions.

A context variable is relevant during an API call, for example, the input of the call, the path of the call, or the message during the call.

The following table shows a list of available API context variables on the API Gateway.

|Variable name|Description|
|-------------|-----------|
|`api.name`|The API title.|
|***`api.document`***|***The OpenAPI \(Swagger 2.0\) document.***|
|`api.root`|The API base path.|
|`api.version`|The version string of the API.|
|`api.endpoint.address`|The address of the API Gateway endpoint.|
|`api.endpoint.hostname`|The host name of the API Gateway endpoint, as requested by the application.|
|`api.operation.id`|The ID of the operation.|
|`api.operation.path`|The path of the operation as defined in OpenAPI \(Swagger 2.0\).|
|`api.org.id`|The organization ID of the API provider.|
|`api.org.name`|The organization short name of the API provider.|
|`api.type`|The API type: REST or SOAP.|
|`api.properties.propertyname`| Retrieves the values of properties that are set for this API. The property values are collection-specific.

 For more information about API properties, see [API properties](apigw_properties.md).

 |
|`plan.name`|The name of the plan.|
|`plan.id`|The unique identifier of the plan.|
|`plan.version`|The version number of the plan.|
|`plan.rate-limits`|The rate limit, that is, the number of API calls per time interval, of the plan.|
|`plan.rate-limits[index].value`|The value of the rate limit. The syntax is `Rate/IntervalUnit`.|
|`plan.rate-limits[index].hard-limit`|The setting of the hard limit.|
|`env.path`|The path segment that represents this collection.|
|`request.authorization`|The parsed HTTP `authorization` header.|
|`request.body`|The payload from the incoming request.|
|`request.content-type`|Normalized content-type value.|
|`request.date`|A date object that represents approximately when the request was received by the API Gateway.|
|`request.headers.headername`|The value of the named HTTP request header.|
|`request.parameters`|You can obtain your incoming parameters from path and query parameters.|
|`request.path`|The path section of the `request.uri` that starts with the base path of the API, including the '/' character that begins the base path.|
|`request.querystring`|The request query string without the leading question mark.|
|`request.search`|The request query string with the leading question mark.|
|`request.uri`|The full HTTP request URI from the application.|
|`request.verb`|The HTTP verb of this request.|
|`client.app.name`|The name of the application that is identified as having issued the request.|
|`client.app.id`|The client ID or application key that is received on the request.|
|`client.app.secret`|The client secret that is received in the request.|
|***`client.org.id`***|***The unique identification key of the organization that owns this application.***|
|***`client.org.name`***|***The name of the organization that owns this application.***|
|`message.body`|The payload of the request or response message.|
|`message.headers.name`|The value of the named HTTP request header.|
|`message.status.code`|The HTTP status code of the response.|
|`message.status.reason`|The HTTP reason phrase of the response.|
|***`oauth.access-token`***|***If the request is authenticated with OAuth, this variable contains the access token string.***|
|***`oauth.resource-owner`***|***If the request is authenticated with OAuth, this variable contains the name of the resource owner.***|
|***`oauth.scope`***|***If the request is authenticated with OAuth, this variable contains the scope of this access token.***|
|***`oauth.miscinfo`***|***This variable contains information explicitly included in the following headers:***|
|***`oauth.not-before`***|***If the request is authenticated with OAuth, this variable contains the date when the token was issued.***|
|***`oauth.not-after`***|***If the request is authenticated with OAuth, this variable contains the date when the token expires.***|
|`system.datetime`|Returns the current time in the system time zone in a JSON object.|
|`system.time.hour`|Returns a number 0 - 23 inclusive, representing the hour of the current time in the system time zone.|
|`system.time.minute`|Returns a number 0 - 59 inclusive representing the minute of the current time in the system time zone.|
|`system.time.seconds`|Returns a number 0 - 59 inclusive representing the seconds of the current time in the system time zone.|
|`system.date`|Returns a JSON object that represents the current date in the system time zone.|
|`system.date.day-of-week`|Returns a number 1 - 7 \(Monday to Sunday\) inclusive representing the day of the week in the system time zone.|
|`system.date.day-of-month`|Returns a number 1 - 31 representing the day of the month in the system time zone.|
|`system.date.year`|Returns a four-digit number that represents the year in the system time zone.|
|`system.timezone`|Returns a system time zone ISO 8601 identifier, which might include a sign, a two-digit hour, and minutes. For example, -04:00.|

**Parent topic:** [API Gateway](apigw_overview.md)


# API routing {#apigw_apirequestrouting_apirouting .concept}

The API Gateway runs the API routing action to match the API to invoke.

The API routing action matches the API to invoke in the following process:

1.  The API routing action extracts the following information from the request:
    -   HTTP method to perform
    -   Request URI
2.  The action then matches the API by matching the extracted information against the information of all available APIs in the API collection.
3.  When multiple APIs are matched, select the API with the longest base path.

The following example shows an API collection with five API entries available through different base paths. The HTTP method that is extracted from the API request is `POST`. The request URI with routing prefix excluded is `/resource`. Although both A and D in the following table are matched, D is selected because the base path of D is longer.

|Entry|API name|Base path|Operation path|Operation|
|-----|--------|---------|--------------|---------|
|A|X|`/`|`/resource`|`POST`|
|B|X|`/`|`/resource/{id}`|`GET`|
|C|Y|`/resource`|`/101`|`GET`|
|D|Y|`/resource`|`/`|`POST`|
|E|Y|`/resource`|`/{count}`|`GET`|

The output of the API routing action is an API that is described by the API name, path name, and operation name. The API processing then proceeds to the client identification phase. If no API is matched, the request is rejected.

In addition, the following rules apply:

-   The action selects the exactly matched candidate instead of the regex matched candidate. For example, if the parameter `{count}` in the operation path of E is `101`, a request with URL `http://<host>/resource/101` matches C and E. However, C is selected because C is the exact match.
-   When the target API operation is `POST`, the action checks whether the consumable content types are defined at the API and operation level. If the consumable types are defined, the action then examines the content type of the incoming request and drops the candidates whose consumable types do not match the content type of the request.

**Parent topic:** [Request processing](apigw_apirequestrouting_apiprocessingrule.md)


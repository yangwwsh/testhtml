# Collection routing {#apigw_apirequestrouting_collection .concept}

The API Gateway determines the API collection to route the request to by matching the request URL against the routing prefix of each API collection. The collection routing follows certain rules, you must take the rules into consideration when you design routing prefixes for your API collections.

For each API collection, the API Gateway uses the routing prefix of the collection to form a complete URI as follows and accepts only the incoming requests with this URI.

```
<routing prefix><base path><operation path>
```

 Routing prefix
 :   The API Gateway supports the following types of routing prefixes:

     URI
     :   When the routing prefix type is URI, the routing prefix must begin but not end with slash \(`/`\).

      Host name
     :   When the routing prefix type is host name, the prefix must not start or end with period \(`.`\). You need to specify only the first part of the host name \(with domain name excluded\); however, the request must use the complete URL with domain name included.

     You can use routing prefixes to organize your APIs into collections and subcollections. For example, if you have a collection of APIs serving for a certain purpose such as human resource, and the APIs are to be used by two segments of your organization, you might create two API collections with the organization name, purpose name, and segment name in the routing prefix.

    If the organization name is `myorg`, the APIs serve for purpose `hr`, and the two segments under the organization is `section1` and `section2`:

    -   When the routing prefix type is URI, the resulting routing prefixes are `/myorg/hr/section1` and `/myorg/hr/section2`.
    -   When the routing prefix type is host name, the resulting routing prefixes are `section1.hr.myorg` and `section2.hr.myorg`.

    The default routing prefix is slash \(`/`\) when the type is URI and blank when the type is host name. An API collection becomes the default collection in the API Gateway when the collection has a default routing prefix. The API Gateway routes a request to the default collection when other collections do not match. An API Gateway can have only one default collection; therefore, regardless of the prefix type, only one API collection can be configured with the default routing prefix.

 :   You can assign multiple routing prefixes to an API collection. For example, you might have a collection of APIs that are already published for the organization. However, cases such as rebranding of the organization might cause that you need to use this same set of APIs through a different URL. In such cases, you can use two different routing prefixes for the API collection during the transition from the old organization to the new organization.

  Base path
 :   Base path on which the API is served. A base path must begin but not end with slash \(`/`\).

  Operation path
 :   Relative path to the base path where the operations are available. An operation path must begin but not end with slash \(`/`\).

 When an API Gateway receives a request, the API Gateway determines the API collection to route the request to according to the following rules in sequence:

-   Rule 1: Match the URI-prefixed collections first and route to the collection whose routing prefix matches the most segments of the request URL.
-   Rule 2: When no collections are matched according to Rule 1, match the hostname-prefixed collections and route to the collection with the longest matched length of routing prefix.
-   Rule 3: When no collections are matched according to Rule 1 and 2, route to the URI-prefixed collection whose routing prefix is slash \(`/`\).
-   Rule 4: When no collections are matched according to Rule 1, 2, and 3, route to the hostname-prefixed collection whose routing prefix is blank.

The following table uses an example API Gateway with seven API collections to explain the collection routing rules.

|API collection name|Routing prefix type|Routing prefix|Base path|
|-------------------|-------------------|--------------|---------|
|A|URI|`/pet/cat`|`/api`|
|B|URI|`/pet/dog`|`/api`|
|C|URI|`/pet`|`/cat`|
|D|URI|`/pet2`|`/cat`|
|E|URI|`/`|`/xyz`|
|F|Host name|`pet`|`/cat`|
|G|Host name|`pet2`|`/cat`|

-   According to Rule 1:
    -   When the API Gateway receives a request with a URL of `http://<host>/pet2/cat/api`, the request is routed to collection D because only the prefix of D matches a complete section of the request URL.
    -   When the API Gateway receives a request with a URL of `https://<host>/pet/cat/api/pets`, although both A and C are matched, the request is routed to collection A because the routing prefix of collection A matches more segments of the request URL.
    -   When the API Gateway receives a request with a URL of `http://pet2.<subdomain>/pet2/cat/api`, although both D and G are matched, the request is routed to collection D because the URI-prefixed collection takes higher priority.
-   According to Rule 2, when the API Gateway receives a request with a URL of `http://pet20.<subdomain>/cat/api`, the request is routed to collection G because the matched string length of G is longer than F.
-   According to Rule 3, when the API Gateway receives a request with a URL of `https://<host>/food/...`, the request is routed to collection E because no collections are matched according to Rule 1 and 2.

**Parent topic:** [Routing of API requests](apigw_apirequestrouting.md)

**Related information**  


[Creating an API collection](apigw_configuringapicollection.md)


# Creating an API collection {#apigw_configuringapicollection .task}

An API collection packages the plans and subscribers to make APIs available to a specific group of API clients. The information instructs how to create an API collection.

To create an API collection, provide the following settings:

-   The routing prefixes that the API Gateway uses for collection routing. See the collection routing topic about how routing prefixes are used to match the target API collection for a request.

    **Tip:** Although you can specify different routing prefix types for the API collections in a single API Gateway, to gain the maximum performance, use only one type within an API Gateway.

-   The API plans to include in the API collection.
-   The API subscribers that are allowed to access the APIs in the API collection. The API Gateway identifies a client as an API subscriber through the API key security check. Therefore, to define an API subscriber, provide the following information:
    -   The client ID that identifies the subscriber.
    -   The hashed client secret that secures the client ID.
    -   Optionally, the name of the subscriber.
    -   Optionally, the subscription, which comprises a list of plans that the subscriber subscribes to.
-   Optionally, the default rate limit to apply for the requests that do not carry user credentials for API key security check.

**Note:** You should always use the default API processing rule and API error rule unless you clearly understand how the rules work and need customized rules for specific business requirements.

1.   In the search field, enter API. 
2.   From the search results, click **API Collection**. 
3.   Click **Add** or **New**. 
4.   Define the basic properties: Name, administrative state, and descriptive summary. 
5.   Specify the routing prefixes. To add a routing prefix, do the following steps: 
    1.   Specify the routing prefix type. 
    2.   Enter the routing prefix. 
    3.   Click **Done**. 
6.   Specify the default rate limit for API requests with no API key. 
7.   Specify the API plans to package in the API collection. 
8.   Specify the subscribers to allow access to the API collection. To add a subscriber, do the following steps: 
    1.   Click **Add**. 
    2.   Enter the client ID. 
    3.   Enter the client secret. 
    4.   Enter the subscriber name. 
    5.   Specify the subscription. 
    6.   Click **Done**. 
9.   Click **Apply** to save the changes to the running configuration. 
10.  Click **Save Configuration** or **Save changes** to save the changes to the persisted configuration. 

**Parent topic:** [Creating an API Gateway](apigw_configuringapigw.md)

**Related information**  


[Collection routing](apigw_apirequestrouting_collection.md)

[Creating an API plan](apigw_configuringapiplan.md)

[Creating an API subscription](apigw_configuringapisubscription.md)

